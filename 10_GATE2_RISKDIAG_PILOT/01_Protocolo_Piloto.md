# Protocolo del Piloto — RiskDiag V1

## Ficha de Trazabilidad
- ID: DOC-056
- Estado: 🟡 En desarrollo
- Tipo: Gate 2 — Pilot Protocol
- Objetivo: Definir el procedimiento paso a paso, manual y reproducible, para correr un diagnóstico de riesgo RiskDiag con un cliente o proyecto real de PICC, de forma que 3-5 casos puedan ejecutarse con el mismo método y sean comparables entre sí.
- Entradas:
  - DOC-055 (99_META/ZEUS_OLYMPUS_INTEGRATION_ASSESSMENT_V1.md) — sección 18, autorización de alcance de Gate 2
  - DOC-052 (AI_EXECUTION_CONTRACT.md) — principios inmutables y criterios de detención
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md) — universo base de decisiones del comprador
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md) — perfiles ICP-H01/H02 y riesgos percibidos
  - DOC-017 (04_TRUST/Trust_Architecture.md) — niveles de evidencia E0-E5
- Salidas:
  - Procedimiento operativo del piloto (fases, roles, tiempos, criterios de detención)
  - Checklist de preparación por caso
- Dependencias:
  - DOC-057 (10_GATE2_RISKDIAG_PILOT/02_Banco_de_Preguntas.md)
  - DOC-058 (10_GATE2_RISKDIAG_PILOT/03_Reglas_de_Clasificacion.md)
  - DOC-059 (10_GATE2_RISKDIAG_PILOT/04_Plantilla_de_Resultado.md)
- Documentos consumidos:
  - 00_IMPLEMENTATION_REPORT.md — sección "Active Program (Single Next Sprint)"
- Documentos generados:
  - Un resultado por caso usando DOC-059
  - Registro de métricas por caso usando DOC-060
  - Registro de defectos por caso usando DOC-061
- Responsable: Dirección + Comercial (ejecución humana)
- Fecha: 2026-07-16
- Criterios de aceptación:
  - El protocolo puede ejecutarse por una persona sin depender de memoria externa ni de esta conversación
  - No requiere software, web, chatbot ni agente autónomo
  - Cada paso tiene entrada, salida, responsable y duración estimada
  - El protocolo distingue explícitamente qué se hace con el cliente y qué se hace internamente

---

## 0. Advertencia de alcance

Este documento describe un procedimiento **100% manual**, ejecutado por una persona de PICC (Dirección o Comercial) con papel, formulario o documento de texto. No implica construir ninguna herramienta, formulario web, base de datos ni integración. RiskDiag en esta fase es un **método**, no un producto de software.

El piloto cubre entre 3 y 5 casos reales. El objetivo no es vender ni cerrar: es generar evidencia de si el método RiskDiag reduce incertidumbre y acelera decisión mejor que el proceso actual de PICC.

---

## 1. Roles del piloto

| Rol | Responsable | Función |
| --- | --- | --- |
| Facilitador del diagnóstico | Dirección o Comercial designado | Conduce la sesión, aplica el banco de preguntas, documenta respuestas |
| Cliente / contraparte del proyecto | Persona real del proyecto piloto | Responde el diagnóstico sobre su propio proyecto |
| Clasificador | Mismo facilitador o Dirección | Aplica las reglas de clasificación (DOC-058) sobre las respuestas capturadas |
| Registrador de métricas | Facilitador | Llena la Hoja de Medición (DOC-060) durante y después de la sesión |
| Registrador de defectos | Facilitador | Llena el Sheet de Defectos (DOC-061) si algo falla durante el proceso |
| Emisor del veredicto de cierre | Dirección (rol ZEUS del piloto) | Aplica la Plantilla de Veredicto (DOC-062) al cierre de los 3-5 casos |

Una sola persona puede cubrir varios roles en un caso pequeño, pero cada rol debe quedar identificado por nombre en el resultado del caso.

---

## 2. Fases del protocolo

### Fase 0 — Selección y preparación del caso

**Entrada:** lista de proyectos o clientes candidatos (reales, no hipotéticos).
**Salida:** 1 caso confirmado con fecha de sesión.
**Duración estimada:** 15-30 min.

Pasos:
1. Elegir un proyecto real, activo o reciente, de preferencia alineado a ICP-H01 o ICP-H02 (mayor madurez de hipótesis según DOC-013), aunque cualquier proyecto real de PICC es válido para el piloto.
2. Confirmar que existe una persona disponible (interna o del cliente) que pueda responder sobre el proyecto con conocimiento directo.
3. Registrar: nombre del proyecto (o código si es sensible), ICP hipotético, fecha, facilitador asignado.
4. Verificar disponibilidad de al menos 45-60 minutos continuos para la sesión.
5. Preparar copia impresa o digital del Banco de Preguntas (DOC-057) y de la Plantilla de Resultado (DOC-059).

Criterio de detención: si no hay proyecto real disponible, no se simula un caso. Se documenta el bloqueo y se espera al siguiente candidato.

### Fase 1 — Apertura de la sesión

**Duración estimada:** 5 min.

Pasos:
1. Explicar el propósito: "vamos a mapear los riesgos de tu proyecto para que la decisión que tomes esté mejor informada", sin prometer resultados ni presentarlo como venta.
2. Aclarar que el diagnóstico es gratuito, no vinculante y no sustituye una propuesta formal.
3. Confirmar que las respuestas pueden documentarse internamente (sin necesidad de exponer datos sensibles del cliente fuera de PICC).

### Fase 2 — Aplicación del Banco de Preguntas

**Entrada:** DOC-057.
**Salida:** respuestas capturadas por bloque.
**Duración estimada:** 25-40 min.

Pasos:
1. Recorrer los bloques del Banco de Preguntas en el orden definido (ver DOC-057).
2. Registrar la respuesta textual o resumida de cada pregunta relevante al proyecto (no todas las preguntas aplican a todos los casos; ver reglas de aplicabilidad por ICP en DOC-057).
3. Marcar explícitamente las preguntas que el cliente no puede o no quiere responder ("sin dato" no es lo mismo que "riesgo bajo").
4. No interpretar ni clasificar todavía: solo capturar.

### Fase 3 — Clasificación

**Entrada:** respuestas de Fase 2.
**Salida:** hallazgos clasificados (severidad, nivel de evidencia, tipo de brecha, decisión afectada).
**Duración estimada:** 20-30 min (puede hacerse después de la sesión, sin el cliente presente).

Pasos:
1. Aplicar las reglas de DOC-058 a cada respuesta relevante.
2. Vincular cada hallazgo a una decisión del comprador del universo de DOC-012 (Decision_Architecture.md).
3. Identificar gaps críticos: información que falta y que bloquea una decisión importante.
4. Priorizar hallazgos por severidad y por si cambian la prioridad del proyecto.

### Fase 4 — Redacción del resultado

**Entrada:** hallazgos clasificados de Fase 3.
**Salida:** documento de resultado usando DOC-059.
**Duración estimada:** 20-30 min.

Pasos:
1. Llenar la Plantilla de Resultado (DOC-059) completa.
2. Revisar que ningún hallazgo se presente como certeza si la evidencia es E0-E1 (ver regla de publicabilidad en DOC-017, aplicada aquí al contexto interno del diagnóstico, no a claims públicos de PICC).
3. Redactar recomendación de siguiente paso.

### Fase 5 — Entrega al cliente

**Duración estimada:** 15-20 min (puede ser en la misma sesión o en una llamada de seguimiento).

Pasos:
1. Compartir el resultado con el cliente (formato PDF o documento simple; no requiere plataforma).
2. Capturar reacción inmediata: ¿fue claro?, ¿le sirvió?, ¿cambia algo su prioridad?
3. Registrar intención declarada: ¿quiere avanzar?, ¿lo compartiría con alguien más en su organización?

### Fase 6 — Registro de métricas y defectos

**Duración estimada:** 10-15 min.

Pasos:
1. Llenar la Hoja de Medición (DOC-060) con los 12 indicadores definidos.
2. Si algo falló durante el proceso (pregunta ambigua, tiempo excedido, cliente confundido, dato no capturable), registrarlo en el Sheet de Defectos (DOC-061).

### Fase 7 — Cierre del piloto (después de 3-5 casos)

**Duración estimada:** 60-90 min, una sola vez.

Pasos:
1. Consolidar la Hoja de Medición de todos los casos.
2. Consolidar el Sheet de Defectos de todos los casos.
3. Aplicar la Plantilla de Veredicto ZEUS (DOC-062).
4. Registrar el veredicto en `99_META/DECISION_HISTORY.md` como una nueva decisión, si el piloto llega a ejecutarse (fuera del alcance de este Gate 2 documental).

---

## 3. Criterios de detención del piloto (heredados de AI_EXECUTION_CONTRACT §14)

Detener un caso o el piloto completo si:
1. El cliente revela que el proyecto es hipotético o especulativo, no real.
2. Una pregunta del banco requiere inventar un dato que PICC no tiene forma de verificar.
3. El cliente pide que el diagnóstico se use como compromiso contractual o cotización formal.
4. Aparece información sensible que no puede documentarse sin autorización explícita.
5. El facilitador detecta que el resultado podría presentarse como claim público de PICC sin evidencia (ver DOC-016, reglas de publicación).

---

## 4. Qué este protocolo NO cubre

- No cubre automatización, formulario digital, ni CRM.
- No cubre scoring numérico automatizado (la clasificación es manual, ver DOC-058).
- No cubre la ejecución real de los 3-5 casos — eso lo hace un humano de PICC después de este Gate 2.
- No cubre integración con ZEUS, OLYMPUS, DAVINCI ni BrickEye (prohibido por DOC-055 sección 19).
