# Caso Piloto — Nave Nissan Aeropuerto (Grupo Andrade / Partarrio)

**MODALIDAD: Pre-piloto retrospectivo, Ronda 2 (proyecto real en curso, reconstruido desde el expediente operativo — NO es sesión en vivo con cliente).**

Aclaración de modalidad: a diferencia de Bodega Mayran (`caso_mayran_bodega.md`, obra concluida) y de Chevrolet Pedregal (Ronda 1, en etapa de cotización con visita técnica ya realizada), este proyecto está en una etapa **más temprana**: propuesta técnica preliminar entregada (18-Mar-2026), visita a sitio ya completada, pero **presupuesto detallado todavía en proceso** al momento de esta reconstrucción (`INDICE_PROYECTO.md`: "EN DESARROLLO (40%)"). El valor de este caso es distinto a los dos anteriores: muestra qué habría capturado el Banco de Preguntas en la fase de **propuesta preliminar basada en reconocimiento fotográfico aéreo**, antes del levantamiento físico definitivo.

## Fuentes de datos usadas (única fuente de verdad para este caso)

- `C:\Development\DataManager\proyectos\NISSAN-ANDRADE-2026-001\INDICE_PROYECTO.md`
- `C:\Development\DataManager\proyectos\NISSAN-ANDRADE-2026-001\04_ENTREGABLES\PROPUESTA_PRELIMINAR_NISSAN_20260318.md`
- `C:\Development\DataManager\proyectos\NISSAN-ANDRADE-2026-001\08_FOTOS\CATALOGO_FOTOS_NISSAN.md` (descripciones textuales de las fotografías DJI y de sitio; nunca se interpretó contenido visual no descrito en el catálogo)
- `C:\Development\DataManager\proyectos\NISSAN-ANDRADE-2026-001\09_FINANZAS\CONTROL_GASTOS.md`

**Nota de trazabilidad:** este proyecto comparte cliente con `caso_mayran_bodega.md` (Grupo Andrade / Partarrio, contacto Rafael Chapa H., rchapa@partarrio.com). La propia propuesta técnica (`PROPUESTA_PRELIMINAR_NISSAN_20260318.md`, Sección 1) invoca explícitamente la relación previa con el cliente "a través del proyecto AEROPUERTO QarDeal" — un proyecto de infraestructura **distinto** al de este caso y al de Bodega Mayran, y que la memoria del sistema ZEUS registra como **CANCELADO** (corrección Pablo, 22-Jun-2026). Se documenta la mención porque forma parte del argumento de confianza de la propuesta ("no somos una empresa nueva para ustedes"), no porque este proyecto sea una continuación de aquel.

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Nave Nissan Aeropuerto — Remodelación de Nave Industrial (NISSAN-ANDRADE-2026-001) |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre datos capturados 06-Feb-2026 (vuelo de dron) y 18-Mar-2026 (propuesta técnica preliminar, última actualización documentada) |
| Facilitador | No aplica — no hubo sesión en vivo |
| ICP hipotético (referencia interna) | ICP-H02 (Industrial e instalaciones críticas) — agencia/taller automotriz de marca, con requisitos de imagen de marca, normativa de residuos peligrosos y ventilación mecánica. Inferencia del reconstructor, sin clasificación ICP formal en la fuente |
| Duración de la "sesión" | No aplica |

## 2. Resumen ejecutivo

El proyecto consiste en la remodelación de dos naves industriales (norte y sur) de una agencia/taller automotriz Nissan colindante con el AICM, para el mismo cliente de `caso_mayran_bodega.md`. A diferencia de ese caso, aquí **no existe todavía un presupuesto contratado**: la "Propuesta Técnica Preliminar" (18-Mar-2026) se elaboró a partir de reconocimiento fotográfico aéreo con dron (26 fotos) y de sitio (10 fotos), sin haberse verificado aún el interior de las naves. La propuesta documenta explícitamente su propio límite de confianza: "los rangos de costo son paramétricos y referenciales", con rangos de inversión que van de $1.2M (Alcance A, básico) a $22.8M MXN (Alcance C, demolición y obra nueva), una dispersión de casi 19x entre el escenario más bajo y el más alto. El hallazgo técnico principal —oxidación visible y probable filtración en la cubierta de la nave sur— es igual en naturaleza al hallazgo central de Chevrolet Pedregal (Ronda 1): un riesgo de deterioro de cubierta detectado por evidencia fotográfica antes de que se agrave, pero aquí con menor nivel de confianza (E2, evidencia fotográfica aérea sin verificación en sitio interior) que en Chevrolet (E3, visita técnica en piso con medición directa).

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| Oxidación visible y probable filtración en cubierta de nave secundaria (sur), lámina acanalada con estructura de fierro rojo, "estado de conservación: deficiente" | D (Riesgo técnico y de ejecución) | S3 — Riesgo alto (requiere intervención prioritaria según la propia propuesta, pero sin confirmación de filtración activa interior porque no se ha visitado el interior) | E2 — Evidencia parcial trazable (fotografía aérea con descripción explícita en el catálogo; "oxidación evidente y faltante de láminas en tramos", sin verificación en sitio interior) | 5 (Qué riesgos existen), 3 (alcance) | Parcialmente soportada — hay evidencia visual, no hay verificación directa |
| Dispersión de 19x entre el rango de inversión más bajo ($1.2M, Alcance A) y el más alto ($22.8M, Alcance C) sin que el cliente haya definido aún cuál alcance requiere | C (presupuesto) | S3 — Riesgo alto (el cliente no puede planear flujo de caja sin acotar el alcance; la decisión de presupuesto queda estructuralmente abierta) | E3 — Evidencia operativa (los tres escenarios y sus rangos están documentados explícitamente en la propuesta, con metodología de cálculo declarada: Construbase 62,826 insumos) | 4 (Qué presupuesto debo esperar) | No evaluable — depende de una decisión de alcance que el cliente aún no ha tomado |
| Trampa de grasas certificada, ventilación mecánica forzada para gases CO, e instalación eléctrica existente: los tres marcados explícitamente "PENDIENTE de verificar" / "no evaluable sin visita interior" en la propia propuesta | D, E (regulatorio) | S3 — Riesgo alto (trampa de grasas es obligatoria por normativa SAG CDMX para descarga a drenaje público; ventilación CO es crítica de seguridad en taller cerrado, NOM-001-STPS) | E1 — Señal aislada (mencionado como pendiente, sin ningún dato de estado actual) | 5, 9 (competencia técnica de PICC para anticiparlo) | No evaluable — el propio documento reconoce que no hay información suficiente aún |
| Necesidad de operar durante la obra o posibilidad de intervenir con nave desocupada — pregunta explícitamente listada como pendiente en la Sección 9 de la propuesta | D (Riesgo técnico y de ejecución) | S2 — Riesgo medio (afecta directamente la duración y el método constructivo, pero no bloquea el proyecto en sí) | E0 — No evidencia (pregunta abierta, sin respuesta del cliente documentada) | 3 (alcance), 5 | No evaluable |
| Atención del cliente dividida entre al menos 3 proyectos simultáneos con el mismo interlocutor (Rafael Chapa): este proyecto, Bodega Mayran (en ejecución activa con incidente de robo y déficit de flujo, ver `caso_mayran_bodega.md`) y la propuesta ORION-CYMIT mencionada en la bitácora de WhatsApp de Mayran (17-Mar-2026, "Rafael envía CV EMZO — propuesta ORION") | A (Contexto y urgencia) | S2 — Riesgo medio (riesgo de que este proyecto pierda prioridad frente a la obra activa de Mayran, que en el momento de esta reconstrucción tiene un déficit de flujo documentado) | E2 — Evidencia parcial trazable (la cita de visita técnica de este proyecto fue cancelada y reprogramada una vez según `INDICE_PROYECTO.md`; correlación temporal con la carga de trabajo de Mayran, no causalidad confirmada) | 1 (Debo actuar ahora), 14 (Siguiente paso) | Parcialmente soportada — hay evidencia de reprogramación, no hay confirmación explícita de la causa |
| Presencia de vehículo oficial (patrulla CDMX) en el patio, sugiriendo posible contrato de servicio institucional | D | S1 — Riesgo bajo (relevante solo para dimensionar el taller, no es un riesgo del proyecto de construcción en sí) | E1 — Señal aislada (observación visual puntual en una sola fotografía, sin confirmación documental de contrato) | 3 (alcance) | No evaluable |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Superficie exacta de cada nave — la propuesta trabaja con un rango de 1,200 a 1,900 m² ("hipótesis de superficie" a partir de fotografía aérea), no una medición | Ausencia de verificación | Visita técnica de diagnóstico con cinta métrica, ya listada como Fase 0 del proyecto | PICC / equipo de campo |
| Estado estructural interior (columnas, trabes, losa) | Ausencia de dato | Visita técnica interior — actualmente "PENDIENTE" según la propia propuesta | PICC |
| Estado de la instalación eléctrica existente, trampa de grasas y ventilación mecánica | Ausencia de dato | Visita técnica interior con checklist normativo | PICC |
| Presupuesto disponible del cliente ("rango orientativo") — listado explícitamente como pendiente en Sección 9 | Información no compartida / no definida en fuente | Pregunta directa al cliente en la próxima reunión | Rafael Chapa / Jose Romero Sabido |
| Giro específico de la nave (venta de vehículos nuevos, servicio/taller, o ambos) — afecta directamente el dimensionamiento de la ventilación CO y la trampa de grasas | Ausencia de definición | Pregunta directa al cliente | Rafael Chapa |
| Fecha deseada de inicio y entrega | Ausencia de dato | Pregunta directa al cliente | Rafael Chapa |

## 5. Recomendaciones priorizadas

1. No comprometer al cliente con ningún monto específico de los tres escenarios hasta cerrar la visita técnica interior — la dispersión de 19x entre alcances es demasiado amplia para servir de base de decisión sin acotar primero el alcance real.
2. Priorizar en la visita técnica interior la verificación de los tres elementos marcados "PENDIENTE" con mayor severidad regulatoria: trampa de grasas, ventilación mecánica CO, y estado de instalación eléctrica — son los tres con menor confianza de evidencia (E0-E1) y mayor severidad (S3).
3. Preguntar explícitamente si el cliente puede desocupar la nave durante la obra o si requiere continuidad operativa — esta única respuesta cambia sustancialmente el método constructivo y el tiempo de obra estimado (3-5 meses vs. posible fase por fase).
4. Dar seguimiento proactivo a la reprogramación de la visita técnica, considerando que el mismo cliente tiene un proyecto activo (Bodega Mayran) con un déficit de flujo de caja documentado que podría estar compitiendo por la atención de Rafael Chapa.
5. Antes de la propuesta formal, resolver si existe relación contractual real de servicio institucional (patrulla CDMX observada) — puede ser relevante para dimensionar capacidad del taller y para el argumento comercial de PICC.

## 6. Siguiente paso propuesto

- Siguiente paso concreto: reprogramar y ejecutar la visita técnica de diagnóstico (Fase 0 de la metodología propuesta), con checklist explícito de los 6 elementos listados en la Sección 9 de la propuesta ("Información Pendiente").
- Owner del siguiente paso: Rafael Chapa (coordinación) / Equipo PICC (ejecución).
- Plazo sugerido: `[DATO NO DISPONIBLE EN FUENTE]` — la propuesta solo indica "1 día" de duración para la visita, sin fecha comprometida.

## 7. Límites del diagnóstico

> Este diagnóstico se basa en la información compartida durante la sesión del [no aplica — reconstrucción documental retrospectiva, no hubo sesión]. No sustituye una auditoría técnica, legal o financiera formal. Los hallazgos marcados como "no verificados" requieren confirmación antes de tomarse como base de decisión final.

Aclaración adicional: la propuesta técnica preliminar que sirve de base a este caso fue elaborada por PICC/DEDALO explícitamente como material de venta preliminar ("No es cotización formal"), no como un diagnóstico de riesgo neutral. Esto significa que el propio documento fuente tiene un sesgo estructural hacia recomendar el Alcance B ("RECOMENDADO"), lo cual este reconstructor documenta pero no corrige — es una característica de la fuente, no un hallazgo de riesgo del cliente.

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
| 1 | Tiempo de diagnóstico | NO APLICA — modalidad retrospectiva | No hubo sesión cronometrada |
| 2 | Completitud | Aproximadamente 14 de 24 preguntas del Banco (DOC-057) respondibles con cita directa de fuente (~58%); varias preguntas adicionales quedan explícitamente marcadas "pendiente" en la propia fuente, lo cual el reconstructor cuenta como brecha identificada, no como respuesta | Cálculo aproximado del reconstructor. Menor que Mayran (~75%) porque el proyecto está en etapa más temprana (propuesta preliminar, sin visita técnica interior) |
| 3 | Claridad percibida | NO APLICA — modalidad retrospectiva | Requiere cliente real respondiendo en Fase 5 |
| 4 | Utilidad percibida | NO APLICA — modalidad retrospectiva | Ídem |
| 5 | Gaps identificados | 6 (ver sección 4) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | Hipótesis del reconstructor: SÍ — el hallazgo de oxidación/filtración de la nave sur debería tratarse con la misma urgencia relativa que el hallazgo equivalente de Chevrolet Pedregal (Ronda 1), aunque aquí la confianza es menor (E2 vs. E3) | Inferencia marcada explícitamente como tal |
| 7 | Reducción de retrabajo | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 8 | Intención de compartir | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 9 | Intención de avanzar | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 10 | Decisión afectada | Parcialmente — la decisión 4 (presupuesto) permanece "no evaluable" incluso después de la reconstrucción, porque depende de una elección de alcance que solo el cliente puede hacer | Evaluación del reconstructor sobre datos documentales |
| 11 | Señal comercial downstream | NO APLICA — modalidad retrospectiva | Requiere seguimiento real con cliente |
| 12 | Errores críticos | 0 | No se detectaron discrepancias internas de cifras en este caso (a diferencia de Chevrolet y Mayran); el riesgo aquí es la amplitud del rango, no una inconsistencia entre documentos |
