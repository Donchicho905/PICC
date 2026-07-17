# Caso Piloto — Caso-02

**MODALIDAD: Pre-piloto retrospectivo (proyecto ya ejecutado, reconstruido desde currículum PICC — NO es sesión en vivo con cliente).**

## Fuentes de datos usadas (única fuente de verdad para este caso)

- `C:\Development\DataManager\proyectos\CV_PICC_GENERATOR\assets\data\contenido_cv.txt`, sección "CASO-02", líneas 80-100.

No se encontró ningún documento adicional (memoria de cálculo, presupuesto, fotos, reportes) para este proyecto en el repositorio operativo de PICC más allá de la entrada del currículum. Este caso se reconstruye **exclusivamente** con lo que dice el CV — es, deliberadamente, el ejercicio de "qué tan lejos se puede llegar con la fuente mínima disponible".

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Caso-02 |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre proyecto ejecutado 2024-2025 |
| Facilitador | No aplica — no hubo sesión en vivo. Reconstrucción documental por agente IA bajo autorización ZEUS |
| ICP hipotético (referencia interna) | ICP-H01 (Infraestructura crítica / Data Center) — clasificación explícita según naturaleza del proyecto (Centro de Datos, ICREA, UPS), consistente con la ficha de ICP-H01 en `03_MODELO_COMERCIAL/ICPs.md` |
| Duración de la "sesión" | No aplica |

## 2. Resumen ejecutivo

El CV describe un proyecto ejecutivo y de construcción completo de un Centro de Datos, incluyendo cálculo eléctrico bajo Norma Mexicana e ICREA, sistema UPS, climatización especializada y cableado certificado, con garantía extendida de 3 años. El nivel de detalle disponible es alto en alcance técnico (qué se hizo) pero **extremadamente bajo en riesgo, presupuesto, cronograma y resultado** — no hay una sola cifra de costo, plazo real de ejecución, incidente, ni testimonio del cliente en la fuente. La reconstrucción de riesgo con este nivel de detalle es débil por diseño de la fuente (un CV comercial no está hecho para documentar riesgo).

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| El CV no reporta ningún incidente, retraso o sobrecosto — ausencia total de señal de riesgo materializado o no materializado | D (Riesgo técnico) | S0/No evaluable — no hay dato suficiente ni para clasificar severidad | E0 — No evidencia (el CV es un documento de marketing, no un reporte de riesgo; la ausencia de menciones de problemas no equivale a ausencia de problemas) | 5 (Qué riesgos existen) | No evaluable |
| Requisito de cálculo eléctrico bajo Norma Mexicana e ICREA (certificación técnica exigente) | B (alcance), E (regulatorio) | S2 — Riesgo medio, inferido: proyectos ICREA suelen tener requisitos de auditoría y redundancia que, si no se cumplen desde diseño, generan retrabajo | E1 — Señal aislada (el CV menciona el estándar como cumplido, no describe el proceso de verificación ni una auditoría de tercero) | 3, 5, 9 (competencia técnica) | Parcialmente soportada — el CV afirma cumplimiento, no lo evidencia con documento de certificación |
| Garantía extendida de 3 años sobre instalaciones eléctricas y sistema UPS | F (confianza institucional) | S1 — Riesgo bajo (la existencia de garantía es una señal positiva, no un riesgo) | E1 — Señal aislada (mencionado en el CV, no se dispone del documento de garantía ni de sus condiciones) | 6, 10 | Parcialmente soportada |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Nombre real del cliente (el CV usa "Data Center Facility" como nombre genérico, probablemente por confidencialidad) | Información no compartida | Confirmar si el nombre real puede documentarse internamente sin publicarse | Dirección PICC / relación con cliente |
| Presupuesto real del proyecto | Ausencia de dato | No existe en ninguna fuente autorizada para este ejercicio | Dirección PICC / archivo comercial |
| Cronograma real vs. planeado, y si hubo desviación | Ausencia de dato | Ídem | PMO / Dirección PICC |
| Cualquier incidente técnico, cambio de alcance o disputa durante ejecución | Ausencia de dato | Ídem | PMO / Dirección PICC |
| Retroalimentación del cliente tras la entrega | Ausencia de dato | Ídem | Comercial / Dirección PICC |

## 5. Recomendaciones priorizadas

1. Este proyecto es un excelente candidato para un caso piloto **en vivo real** (no retrospectivo) precisamente porque el CV no contiene el detalle necesario — solo el cliente o el equipo de proyecto original puede llenar las brechas de la sección 4.
2. Antes de usar este proyecto como evidencia pública de capacidad ICREA, verificar si existe el certificado o constancia formal del cumplimiento normativo mencionado.
3. Si se decide usar como Knowledge Product o caso de referencia comercial, obtener autorización explícita del cliente para nombrarlo (ver regla de manejo de datos sensibles en DOC-059 y proceso de DOC-016).

## 6. Siguiente paso propuesto

- Siguiente paso concreto: identificar internamente quién fue el responsable de proyecto de Caso-02 y solicitarle, en una sesión real (no retrospectiva), las respuestas al Banco de Preguntas completo.
- Owner del siguiente paso: Dirección PICC.
- Plazo sugerido: `[DATO NO DISPONIBLE EN FUENTE]`.

## 7. Límites del diagnóstico

> Este diagnóstico se basa en la información compartida durante la sesión del [no aplica — reconstrucción documental retrospectiva, no hubo sesión]. No sustituye una auditoría técnica, legal o financiera formal. Los hallazgos marcados como "no verificados" requieren confirmación antes de tomarse como base de decisión final.

## 8. Firma / responsable

| Campo | Valor |
| --- | --- |
| Elaborado por | Agente IA (Claude, bajo autorización ZEUS/PICC), sesión 2026-07-16 |
| Revisado por | Pendiente |
| Fecha de entrega al cliente | No aplica |

---

## Hoja de Medición (DOC-060) — adaptada a modalidad retrospectiva

| # | Métrica | Valor en este caso | Nota de aplicabilidad |
| --- | --- | --- | --- |
| 1 | Tiempo de diagnóstico | NO APLICA — modalidad retrospectiva | — |
| 2 | Completitud | 4 de 24 preguntas del Banco pudieron responderse con algún nivel de evidencia (aprox. 17%) — el resto no tiene ningún dato en la fuente disponible | Este número por sí mismo es el hallazgo más importante de este caso: con solo un CV comercial, la completitud del método cae drásticamente frente a Caso-01 |
| 3 | Claridad percibida | NO APLICA | — |
| 4 | Utilidad percibida | NO APLICA | — |
| 5 | Gaps identificados | 5 (ver sección 4) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | No evaluable — no hay dato suficiente para inferir prioridad | — |
| 7 | Reducción de retrabajo | NO APLICA | — |
| 8 | Intención de compartir | NO APLICA | — |
| 9 | Intención de avanzar | NO APLICA | — |
| 10 | Decisión afectada | NO — con esta fuente el ejercicio retrospectivo no logró mover ninguna decisión del universo base de "no evaluable" a "soportada" | Evaluación explícita del reconstructor |
| 11 | Señal comercial downstream | NO APLICA | — |
| 12 | Errores críticos | 0 | No se detectaron defectos del método en este caso; el problema es la pobreza de la fuente, no el Banco de Preguntas ni las Reglas de Clasificación |
