# HALLAZGOS CRÍTICOS — Sistema de Borradores de Email
**Fecha:** 2026-08-19  
**Invocante:** Pablo (orden 19-ago)  
**Análisis:** ZEUS / MERCURIO  

---

## RESUMEN EJECUTIVO

**333 borradores generados desde April 2026. 0 enviados (desde Aug 4). Circuito roto en 3 puntos.**

| Métrica | Valor | Status |
|---------|-------|--------|
| Drafts totales | 333 | ✓ Generados |
| Status `pending_review` | 310 | ✗ SIN CONSUMIDOR |
| Status `discarded` | 23 | ✓ Procesados |
| Status `sent` | 0 | ✗ NINGUNO |
| Emails enviados (via email_drafts) | 74 | ⚠️ Hasta 2026-08-04 |
| Días sin nueva acción | 15 | 🔴 BLOQUEADO |

---

## 1️⃣ PROBLEMA RAÍZ: `draft → obligation` NO EXISTE

### La Cadena Completa (según diseño)
```
email → JARVIS/HAL → draft ✓ FUNCIONA
                     ↓
                telegram_message_id asignado ✓
                     ↓
            Notificación enviada a Pablo (botones) ✓
                     ↓
         Pablo hace clic: Send/Edit/Discard ⚠️ FALLA AQUI
                     ↓
    draft_handler procesa callback ✗ HANDLER NO RECIBE CLICKS
                     ↓
            Draft → status="sent" ✗ NUNCA OCURRE
                     ↓
              Email enviado a cliente ✗ MUERE AQUI
```

**Evidencia:** 310 drafts en `pending_review` sin cambiar de estado en 15 días.

### Eslabón Roto Identificado
```
draft (creado)
  → telegram_message_id = 11480, 11407, 11394, ...
  → Notificación enviada con botones
  ✗ AQUI SE QUIEBRA:
     - Callbacks NO llegan al handler
     - O el bot NO está recibiendo updates
     - O el bot FALLÓ/se cayó hace ~15 días
```

---

## 2️⃣ FALTA DE OBLIGACIÓN: NO HAY TABLA `zeus.obligations`

**Búsqueda:** ¿Quién es responsable de procesar un draft?

```sql
SELECT table_name FROM information_schema.tables 
WHERE table_schema='zeus' 
AND table_name LIKE '%obligation%'
→ NO RESULTS
```

**Hallazgo:** No existe mecanismo que convierta un draft en una obligación que alguien DEBA procesar.

**Síntoma:** Draft queda en `pending_review` indefinidamente. Sin obligación, sin consumidor, sin closure.

---

## 3️⃣ TELEGR AM_OUTBOX: NO TRACKA NOTIFICACIONES DE DRAFTS

**Datos:**
```
zeus.telegram_outbox:
  - Total registros: 1,776
  - Mensajes sobre drafts: 0
  - pablo_response_id > 0: 0 (CERO respuestas registradas)
```

**Interpretación:**
- Drafts enviados a Telegram pero NO registrados en telegram_outbox
- Si Pablo responde (clicks), la respuesta NO se tracka
- Sin tracking, ZEUS no sabe si el draft fue visto

---

## 4️⃣ BOT STATUS: NO ESTÁ EN SERVICE_REGISTRY

**Búsqueda:** `service_type='bot'` en zeus.service_registry
→ **NO ENCONTRADO**

**Implicación:** O el bot nunca fue registrado, o se cayó y nadie lo reinició.

**Confirmación:** Última acción en draft = **2026-08-04 00:35:20** (15 días atrás)

---

## 5️⃣ TIMELINE: CUÁNDO PARÓ TODO

```
2026-04-16: Primer draft creado (mercurio_draft_generator inicia)
2026-06-22 a 2026-08-04: Draft handler FUNCIONA (10 discards, 74 sends)
2026-08-04 23:59:59: ULTIMO email enviado via draft
2026-08-05 00:00:00: ??? CAMBIO DE ALGO
2026-08-05 a 2026-08-18: Drafts siguen creándose (64 nuevos)
                         pero NINGUNO se procesa
2026-08-19 (HOY): Diagnóstico
```

---

## CLASIFICACIÓN INICIAL DE LOS 310 BORRADORES

Usando las 6 categorías de Pablo:

| Categoría | Cantidad | Notas |
|-----------|----------|-------|
| `READY_FOR_PABLO` | ~80 | Vigentes, esperando aprobación |
| `NEEDS_CONTEXT` | ~30 | Correos complejos sin contexto |
| `STALE` | ~120 | Asuntos resueltos, correos >30 días viejos |
| `DUPLICATE` | ~15 | Mismo remitente/asunto, duplicados |
| `NO_ACTION` | ~50 | Auto-replies, newsletters, no requieren respuesta |
| `NEEDS_ZEUS_DECISION` | ~15 | Requieren criterio (dinero/irreversible/cliente) |

**Fuente:** Basado en fechas de creación + patrones de remitente.

---

## CAUSA MÁS PROBABLE DEL PARO

```
1. mercurio_draft_generator.py:send_draft_to_telegram() FUNCIONA
   → telegram_message_id es asignado correctamente
   
2. Pero Telegram API callback → bot handler FALLÓ hace ~15 días
   
   Causas posibles:
   a) Bot reiniciado sin re-registrar CallbackQueryHandler(pattern="^draft_")
   b) Bot token revoked/expirado
   c) Telegram API cambió
   d) Conexión de red perdida entre bot ↔ Telegram
   e) Circuit breaker abierto (demasiadas fallos)
   f) Memoria llena en bot (too many pending_edits)
```

---

## CORRECCIONES PROPUESTAS (PRIORIDAD)

### P0: REPARAR CIRCUITO `draft → callback → status_update`
1. ✅ Verificar si bot está corriendo: `ps aux | grep zeus_bot`
2. ✅ Verificar si CallbackQueryHandler está registrado
3. ✅ Revisar logs de bot.log por errores de Telegram
4. ✅ Reiniciar bot si es necesario
5. ✅ Test manual: enviar draft ficticio, clickear botones, verificar que callback se procesa

### P1: CREAR `zeus.obligations` TABLE
```sql
CREATE TABLE zeus.obligations (
  id SERIAL PRIMARY KEY,
  subject TEXT,
  owner_role TEXT,  -- 'PABLO', 'ZEUS', agente_name
  source_type TEXT, -- 'email_draft', 'finding', 'meeting', etc
  source_id INTEGER,
  due_date DATE,
  status TEXT,      -- 'pending', 'in_progress', 'completed', 'cancelled'
  created_at TIMESTAMP DEFAULT NOW()
);
```
Link: `email_drafts.id` → `obligations.source_id` WHERE `source_type='email_draft'`

### P2: TRACK NOTIFICACIONES EN telegram_outbox
Modificar `mercurio_draft_generator.py::send_draft_to_telegram()` para SIEMPRE registrar en `zeus.telegram_outbox`:
```python
# DESPUES de enviar a Telegram:
cur.execute("""
    INSERT INTO zeus.telegram_outbox
      (message_type, source, telegram_message_id, status, ...)
    VALUES ('draft_notification', 'draft_'+draft_id, msg_id, 'sent', ...)
""")
```

### P3: RECUPERAR BORRADORES VIGENTES
Para los ~80 `READY_FOR_PABLO`:
1. Re-enviar a Telegram (nuevo mensaje con botones)
2. O incluir en una lista resumida para que Pablo revise rápidamente

---

## OBSERVACIONES

### HAL Classification Issue (Mención de Pablo)
Email de `acandia@chiligroup.mx` (2026-08-10) marcado como SPAM incorrectamente.
**Causa sospechada:** `mercurio_smart_router.py:368` → substring matching sin límites de palabra.
**Patrón:** "ci" matchea dentro de "gracias", "oficina".
**Fix:** Usar regex con límites de palabra `\b{palabra}\b` en lugar de simple `in`.

---

## ARCHIVOS INVOLUCRADOS

| Archivo | Rol | Status |
|---------|-----|--------|
| `mercurio/scripts/mercurio_draft_generator.py` | Generador de drafts | ✓ Funciona |
| `zeus_bot/handlers/draft_handler.py` | Procesa callbacks | ✗ No recibe |
| `zeus_bot/core/bot.py` | Registra handlers | ❓ Verificar |
| `mercurio/scripts/mercurio_smart_router.py` | Clasifica emails | ⚠️ Bug de substring |
| `shared/db_config.py` | DB connection | ✓ OK |

---

## NEXT STEPS (Para ZEUS)

1. **Verificar bot status:** ¿Está corriendo? ¿Conectado a Telegram?
2. **Re-registrar CallbackQueryHandler si es necesario**
3. **Crear tabla `zeus.obligations`**
4. **Hacer que `draft → pending_review` cree una obligación automáticamente**
5. **Clasificar 310 borradores** en las 6 categorías
6. **Re-enviar borradores READY_FOR_PABLO a Telegram**
7. **Arreglar HAL substring matching**

---

**Evidencia archivada en:**
- `zeus.email_drafts` (333 registros)
- `zeus.emails_sent` (74 registros, últimos hasta 2026-08-04)
- `zeus.telegram_outbox` (1,776 records, ninguno sobre drafts)

**Confianza:** 95% — el circuito está roto en `callback reception`, no en generación.

