# Caso Piloto — Chevrolet Pedregal (Sistema Pluvial y Techumbre)

**MODALIDAD: Pre-piloto retrospectivo (proyecto ya ejecutado, reconstruido desde currículum PICC — NO es sesión en vivo con cliente).**

Aclaración adicional de modalidad para este caso específico: al momento de esta reconstrucción (2026-07-16) el proyecto **no está en etapa de obra terminada, sino en etapa de COTIZACIÓN** (ver `proyecto.json`, campo `"etapa": "COTIZACION"`). Lo que sí está completamente ejecutado y documentado es el **diagnóstico técnico** (visita de levantamiento, memoria de cálculo pluvial, catálogo fotográfico de hallazgos y presupuesto). Este caso reconstruye qué habría capturado el Banco de Preguntas (DOC-057) si se hubiera aplicado como método formal durante esa etapa de diagnóstico ya realizada — no reconstruye una obra concluida. Se elige deliberadamente porque es el caso con mayor densidad de evidencia real de riesgo técnico materializado (deterioro de techumbre, filtraciones) disponible en el repositorio.

## Fuentes de datos usadas (única fuente de verdad para este caso)

- `C:\Development\DataManager\proyectos\CHEVROLET-2025-001\proyecto.json`
- `C:\Development\DataManager\proyectos\CHEVROLET-2025-001\CALCULO_PLUVIAL_CHEVROLET.md`
- `C:\Development\DataManager\proyectos\CHEVROLET-2025-001\PRESUPUESTO_CHEVROLET_PLUVIAL.md`
- `C:\Development\DataManager\proyectos\CHEVROLET-2025-001\08_FOTOS\visita2_20260302\CATALOGO_FOTOS_VISITA2.md` (descripciones textuales de 26 de 58 fotos revisadas; nunca se interpretó contenido visual no descrito en el texto del catálogo)
- `C:\Development\DataManager\proyectos\CV_PICC_GENERATOR\memoria_calculo_pluvial.txt`
- `C:\Development\DataManager\proyectos\CV_PICC_GENERATOR\analisis_llenado_cisternas.txt`

**Nota de trazabilidad importante:** este proyecto **no aparece listado en** `contenido_cv.txt` (el currículum comercial oficial de 24 proyectos de PICC). Es un proyecto real y operativo documentado en el repositorio interno de PICC (`DataManager/proyectos/CHEVROLET-2025-001/`), con datos técnicos verificables de mayor granularidad que cualquier proyecto del CV oficial. Se incluye en este pre-piloto porque el propio encargo de esta tarea lo identificó explícitamente como candidato fuerte por su evidencia real de deterioro de techumbre. Se documenta la discrepancia de fuente en vez de ocultarla (regla AI_EXECUTION_CONTRACT §15.9, "no ocultar incertidumbre").

**Nota adicional de trazabilidad:** `proyecto.json` registra `"elaborado_por": "BANDEJAS FODDER, SA DE CV"` para el reporte original de levantamiento (`Reporte_Levantamiento_Chevrolet_Pedregal.pdf`, no leído en este ejercicio — no se tuvo acceso a su contenido), mientras que `CALCULO_PLUVIAL_CHEVROLET.md` indica `"Elaboro: PICC Ingenieria / DEDALO-ZEUS"`. No se resuelve aquí si el levantamiento inicial lo hizo FODDER (jardín/paisajismo, otra empresa de Pablo) y el cálculo de ingeniería lo hizo PICC, o si hay una imprecisión en los metadatos. Se marca como **[DATO NO DISPONIBLE EN FUENTE]** cuál empresa facturaría el proyecto final.

---

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Chevrolet Pedregal — Rehabilitación Sistema Pluvial y Techumbre (CHEVROLET-2025-001) |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre datos de campo capturados 2025-12-09 (inicio) y 2026-03-02 (visita técnica 2, última actualización de cálculo Rev 4.0) |
| Facilitador | No aplica — no hubo sesión en vivo. Reconstrucción documental por agente IA bajo autorización ZEUS, no por Dirección/Comercial de PICC |
| ICP hipotético (referencia interna) | ICP-H02 (Industrial e instalaciones críticas) — hipótesis del reconstructor; el proyecto es una agencia automotriz con taller mecánico, área de lavado y techumbre industrial. No hay clasificación ICP formal registrada en las fuentes originales del proyecto, por lo tanto esta asignación es una inferencia, no un dato capturado en sesión |
| Duración de la "sesión" | No aplica (modalidad retrospectiva; no hubo sesión cronometrada) |

## 2. Resumen ejecutivo

El proyecto presenta un sistema pluvial con déficit de capacidad documentado entre 75% y 86.4% según la fuente consultada (ver discrepancia en sección 4). Se identificaron 6 hallazgos críticos en visita técnica real: canalón central insuficiente sin salidas intermedias, 4 coladeras del canalón lateral cegadas con concreto, colmena de abejas activa que bloquea intervención en una zona, estructura metálica oxidada, bajada pluvial exterior sin conexión al drenaje municipal, y una mancha de filtración ya visible dentro del taller mecánico — es decir, el riesgo de daño por agua **ya se había materializado parcialmente** al momento del diagnóstico. Recomendación principal: intervención por fases (urgente/mediano/largo plazo) antes de comprometer presupuesto en el alcance completo, dado que 64.7% de las partidas del presupuesto son estimadas, no verificadas en sitio.

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| Canalón central sin capacidad suficiente (ancho libre 8-10 cm, sin salidas intermedias en 30-35 m de recorrido), con grieta longitudinal continua | D (Riesgo técnico y de ejecución) | S4 — Riesgo crítico (filtración ya visible dentro del taller; riesgo de continuidad operativa y daño patrimonial) | E3 — Evidencia operativa (medido y fotografiado en visita técnica real, `CATALOGO_FOTOS_VISITA2.md`) | 5 (Qué riesgos existen) | Soportada — hay evidencia directa y medición |
| Filtración de agua ya visible en unión lámina-muro dentro del taller mecánico | D | S4 — Riesgo crítico (daño ya ocurriendo, no solo potencial) | E3 — Evidencia operativa (fotografiada, descrita como "mancha oscura... posible filtración") | 5 | Parcialmente soportada — se confirma la mancha, no se confirma con certeza absoluta que sea 100% pluvial (el catálogo dice "posiblemente relacionada") |
| 4 coladeras del canalón lateral cegadas con concreto (reducción deliberada o histórica de capacidad de drenaje) | D | S3 — Riesgo alto (agrava el déficit de capacidad; requiere decisión de rehabilitar o no) | E3 — Evidencia operativa (fotografiada y descrita explícitamente) | 5 | Soportada |
| Colmena de abejas activa en zona de intervención de cubierta | D | S3 — Riesgo alto (bloquea ejecución de una zona del alcance hasta resolverse; riesgo de seguridad laboral) | 5, 3 (alcance) | Soportada |
| Estructura metálica oxidada en zona de cubierta nueva | D | S2 — Riesgo medio (encarece o retrasa si no se trata antes de instalar lámina nueva) | E3 — Evidencia operativa (fotografiada) | 5 | Soportada |
| Bajada pluvial exterior sin conexión al drenaje municipal (descarga al aire a 1.5 m del piso) | D, E (regulatorio) | S2 — Riesgo medio (no cumplimiento normativo probable, no crítico de forma inmediata) | E3 — Evidencia operativa (fotografiada) | 5, 5 (regulatorio) | Parcialmente soportada — no se verificó normativa municipal aplicable exacta, `[DATO NO DISPONIBLE EN FUENTE]` |
| Presencia de lámina de asbesto en alcance de largo plazo (retiro certificado requerido) | E (regulatorio) | S3 — Riesgo alto (manejo de residuo peligroso, costo y cumplimiento regulatorio; `$50,604.75` en manifiesto y disposición según presupuesto) | E3 — Evidencia operativa (cuantificado en presupuesto, con partida `[OK]` para el manifiesto) | 5 | Soportada |
| 64.7% de las partidas del presupuesto son estimadas `[EST]`, no verificadas en sitio | C (presupuesto) | S2 — Riesgo medio (el presupuesto final puede variar significativamente respecto al estimado) | E3 — Evidencia operativa (cifra explícita en `PRESUPUESTO_CHEVROLET_PLUVIAL.md`: "Porcentaje estimado: 64.7%") | 4 (presupuesto) | No evaluable — el propio documento reconoce que la mayoría de partidas no están verificadas |
| Discrepancia entre `proyecto.json` (déficit 86.4%, 13 bajadas) y `PRESUPUESTO_CHEVROLET_PLUVIAL.md` (déficit 75%, 11 bajadas) | Brecha de método interno de PICC, no del proyecto del cliente | S1 — Riesgo bajo para el cliente, pero relevante para la fiabilidad del propio proceso de PICC | E1 — Señal aislada (detectada por el reconstructor, no verificada con el equipo que generó los documentos) | No aplica — esto no es un hallazgo del proyecto del cliente, se registra también como defecto en DOC-061 | No evaluable |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Área tributaria y gasto requerido tienen cifras distintas entre `proyecto.json` (Rev 4.0: área 767.10 m², gasto 57.40 L/s) y `memoria_calculo_pluvial.txt` (Zona 4: área 767.1 m², gasto 4.89 L/s) y `PRESUPUESTO_CHEVROLET_PLUVIAL.md` (gasto requerido 4.89 L/s, capacidad actual 1.20 L/s, déficit 75%) | Ausencia de verificación | Reconciliar cuál revisión de cálculo (Rev 2.0 a Rev 4.0 según `CALCULO_PLUVIAL_CHEVROLET.md`) es la vigente y cuál documento debe actualizarse para quedar consistente | PICC Ingeniería (autor de la memoria de cálculo) |
| Contenido del reporte original de levantamiento (`Reporte_Levantamiento_Chevrolet_Pedregal.pdf`) | Ausencia de verificación | No se leyó el PDF en este ejercicio (fuera del alcance de fuentes de texto autorizadas para este pre-piloto) | PICC / quien tenga el archivo original |
| Empresa responsable final de facturación/ejecución (FODDER vs. PICC) | Información no compartida / no definida en fuente | Confirmar internamente con Dirección quién factura el proyecto | Dirección PICC |
| Normativa municipal exacta aplicable a la descarga pluvial no conectada a drenaje | Ausencia de dato | Consulta con SACMEX o normativa local de Tlalpan | PICC / asesor regulatorio |
| 32 de 58 fotos de la visita 2 no fueron revisadas ni descritas en el catálogo | Ausencia de verificación | Revisar el resto de las fotos si se requiere evidencia adicional | Facilitador que revise el catálogo completo |

## 5. Recomendaciones priorizadas

1. Resolver la discrepancia de cifras de déficit (75% vs. 86.4%) y de número de bajadas (11 vs. 13) antes de presentar el presupuesto final al cliente — un documento con cifras inconsistentes daña la credibilidad del diagnóstico técnico.
2. Gestionar la colmena de abejas (fumigación o desalojo especializado) como paso previo obligatorio a cualquier intervención en la zona de cubierta afectada, dado que bloquea físicamente el alcance.
3. Priorizar la Fase 1 (Corto Plazo, $75,282.39 con IVA según el presupuesto) como intervención mínima defendible, dado que ya existe filtración activa documentada dentro del taller.
4. Verificar en sitio las partidas marcadas `[EST]` (64.7% del presupuesto) antes de comprometer al cliente con el monto de la Opción C ($2,698,799.04 con IVA), que depende en gran parte de estimaciones no confirmadas, especialmente el retiro de asbesto.
5. Documentar formalmente si la descarga pluvial exterior sin conexión a drenaje municipal representa un incumplimiento normativo actual, antes de que se convierta en un hallazgo de una autoridad externa.

## 6. Siguiente paso propuesto

- Siguiente paso concreto: cerrar la reconciliación de cifras entre los tres documentos de cálculo/presupuesto y presentar al cliente una única cifra de déficit y bajadas.
- Owner del siguiente paso: PICC Ingeniería (interno).
- Plazo sugerido: `[DATO NO DISPONIBLE EN FUENTE]` — ninguna fuente registra una fecha comprometida para esta reconciliación.

## 7. Límites del diagnóstico

> Este diagnóstico se basa en la información compartida durante la sesión del [no aplica — reconstrucción documental retrospectiva, no hubo sesión]. No sustituye una auditoría técnica, legal o financiera formal. Los hallazgos marcados como "no verificados" requieren confirmación antes de tomarse como base de decisión final.

Aclaración adicional: a diferencia de un caso piloto real, este resultado no fue validado con ningún cliente ni con el facilitador original del levantamiento. Es una reconstrucción hecha exclusivamente a partir de documentos técnicos ya existentes.

## 8. Firma / responsable

| Campo | Valor |
| --- | --- |
| Elaborado por | Agente IA (Claude, bajo autorización ZEUS/PICC), sesión 2026-07-16 |
| Revisado por | Pendiente — no revisado por Dirección PICC al momento de esta reconstrucción |
| Fecha de entrega al cliente | No aplica — este documento no se entrega al cliente. Es evidencia interna de pre-piloto |

---

## Hoja de Medición (DOC-060) — adaptada a modalidad retrospectiva

| # | Métrica | Valor en este caso | Nota de aplicabilidad |
| --- | --- | --- | --- |
| 1 | Tiempo de diagnóstico | NO APLICA — modalidad retrospectiva | No hubo sesión cronometrada; el trabajo de campo real (visita 2) tomó de 16:56 a 17:05 hrs (9 min de captura fotográfica), pero eso no equivale al protocolo completo de RiskDiag |
| 2 | Completitud | 15 de 24 preguntas del Banco (DOC-057) pudieron responderse con algún nivel de evidencia usando solo las fuentes documentales existentes (aprox. 62.5%); el resto requeriría preguntar directamente al cliente (ej. Bloque A urgencia, Bloque F confianza en proveedor, Bloque G siguiente paso) | Cálculo aproximado del reconstructor, no un conteo formal de sesión |
| 3 | Claridad percibida | NO APLICA — modalidad retrospectiva | Requiere cliente real respondiendo en Fase 5 |
| 4 | Utilidad percibida | NO APLICA — modalidad retrospectiva | Ídem |
| 5 | Gaps identificados | 5 (ver sección 4 de este documento) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | Hipótesis del reconstructor: SÍ — la evidencia de filtración activa dentro del taller sugeriría que este proyecto debería tratarse con mayor urgencia que "cotización en curso sin fecha límite" | No es un dato capturado del cliente; es una inferencia marcada explícitamente como tal |
| 7 | Reducción de retrabajo | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 8 | Intención de compartir | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 9 | Intención de avanzar | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 10 | Decisión afectada | SÍ, decisión 5 ("Qué riesgos existen") — el ejercicio retrospectivo sí habría podido mover esta decisión de "no evaluable" a "soportada" usando solo datos ya existentes | Evaluación del reconstructor sobre datos documentales, no sobre una sesión con el cliente |
| 11 | Señal comercial downstream | NO APLICA — modalidad retrospectiva | Requiere seguimiento real a 15 días con cliente real |
| 12 | Errores críticos | 1 (ver DEF-01 en Sheet de Defectos, DOC-061) | La discrepancia de cifras entre documentos internos se registra como defecto |
