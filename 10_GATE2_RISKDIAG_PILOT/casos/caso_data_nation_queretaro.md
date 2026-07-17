# Caso Piloto — Data Nation, Centro de Datos Querétaro

**MODALIDAD: Pre-piloto retrospectivo (proyecto ya ejecutado, reconstruido desde currículum PICC — NO es sesión en vivo con cliente).**

## Fuentes de datos usadas (única fuente de verdad para este caso)

- `C:\Development\DataManager\proyectos\CV_PICC_GENERATOR\assets\data\contenido_cv.txt`, sección "DATA NATION - CENTRO DE DATOS QUERÉTARO", líneas 158-170.

No se encontró ningún documento adicional para este proyecto en el repositorio operativo de PICC más allá de la entrada del currículum.

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Data Nation — Centro de Datos Querétaro |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre proyecto ejecutado 2022-2023 |
| Facilitador | No aplica — reconstrucción documental por agente IA bajo autorización ZEUS |
| ICP hipotético (referencia interna) | ICP-H01 (Infraestructura crítica / Data Center) — el CV lo describe explícitamente como "Centro de Datos Tier II" |
| Duración de la "sesión" | No aplica |

## 2. Resumen ejecutivo

El CV describe un proyecto ejecutivo (no de construcción física completa, según la fuente — el campo dice "Proyecto ejecutivo: PICC" sin mencionar "Construcción: PICC" como en otros casos del CV) de un Centro de Datos Tier II, con diseño arquitectónico, ingeniería eléctrica de media y baja tensión, sistemas CRAC y memorias de cálculo. Al igual que el caso Ixtapaluca, el nivel de detalle de riesgo, costo y resultado es prácticamente nulo. Un hallazgo relevante de este ejercicio: la ambigüedad sobre si PICC ejecutó la construcción o solo el proyecto ejecutivo es en sí misma información importante que el Banco de Preguntas (Bloque B, alcance) habría capturado en segundos con una pregunta directa al cliente.

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| Ambigüedad sobre si el alcance de PICC incluyó construcción física o solo proyecto ejecutivo | B (alcance) | S1 — Riesgo bajo para el proyecto en sí, pero S2 para la claridad comercial del caso (afecta si PICC puede reclamarlo como "obra construida" en su portafolio) | E1 — Señal aislada (inferencia por ausencia de la palabra "Construcción" en el campo de responsables, comparado con el patrón de otros proyectos del mismo CV) | 3 (alcance), 7 (PICC entiende un proyecto como el mío) | No evaluable — requiere confirmación directa |
| Sin información de si hubo certificación Tier II formal por un tercero (Uptime Institute u otro) | E (regulatorio), F (confianza institucional) | S2 — Riesgo medio, inferido: un Data Center "Tier II" sin certificación formal expone al cliente a que la clasificación no sea defendible ante terceros | E0 — No evidencia (el CV usa el término "Tier II" sin mencionar certificación de organismo alguno, a diferencia del caso Satmex que sí menciona "clasificación ICREA III (Uptime Institute)") | 5, 9 | No evaluable |
| Sin ninguna cifra de presupuesto, plazo o incidente | D (riesgo técnico) | No evaluable | E0 | 4, 5 | No evaluable |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Alcance real (proyecto ejecutivo únicamente vs. construcción completa) | Ausencia de definición en la fuente disponible | Confirmar internamente con el equipo que ejecutó el proyecto | PMO / Dirección PICC |
| Certificación Tier II formal (si existe) | Ausencia de dato | Solicitar documento de certificación si existe | Dirección PICC / cliente |
| Presupuesto, plazo, resultado, satisfacción del cliente | Ausencia de dato | No existe en ninguna fuente autorizada para este ejercicio | Dirección PICC / archivo comercial |

## 5. Recomendaciones priorizadas

1. Aclarar internamente y por escrito si "Data Nation" fue un proyecto de solo ingeniería/diseño o de construcción completa — esto afecta cómo se puede presentar el caso en futuras propuestas comerciales (evitar sobre-reclamar alcance, ver principio 3 de AI_EXECUTION_CONTRACT: "No inventar datos, claims o evidencia").
2. Si el proyecto se usa como evidencia de capacidad Tier II, verificar si existe soporte de certificación; si no existe, ajustar el lenguaje comercial a "diseñado bajo criterios Tier II" en vez de "Centro de Datos Tier II" para no implicar una certificación que no está confirmada.
3. Como en el caso Ixtapaluca, este proyecto es mejor candidato para un piloto en vivo real que para evidencia retrospectiva, dado lo limitado de la fuente.

## 6. Siguiente paso propuesto

- Siguiente paso concreto: identificar al responsable de proyecto de Data Nation Querétaro y aplicar el Banco de Preguntas completo en sesión real.
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
| 2 | Completitud | 3 de 24 preguntas del Banco pudieron responderse con algún nivel de evidencia (aprox. 12.5%) | La completitud más baja de los 4 casos del pre-piloto |
| 3 | Claridad percibida | NO APLICA | — |
| 4 | Utilidad percibida | NO APLICA | — |
| 5 | Gaps identificados | 3 (ver sección 4) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | No evaluable | — |
| 7 | Reducción de retrabajo | NO APLICA | — |
| 8 | Intención de compartir | NO APLICA | — |
| 9 | Intención de avanzar | NO APLICA | — |
| 10 | Decisión afectada | NO — no se pudo mover ninguna decisión de "no evaluable" a "soportada" con esta fuente | — |
| 11 | Señal comercial downstream | NO APLICA | — |
| 12 | Errores críticos | 0 | No se detectaron defectos del método; la limitación es de fuente, no de diseño del Banco o de las Reglas de Clasificación |
