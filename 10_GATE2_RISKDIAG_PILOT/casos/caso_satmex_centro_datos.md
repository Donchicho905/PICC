# Caso Piloto — Centro de Datos de Satélites Mexicanos (Satmex)

**MODALIDAD: Pre-piloto retrospectivo (proyecto ya ejecutado, reconstruido desde currículum PICC — NO es sesión en vivo con cliente).**

## Fuentes de datos usadas (única fuente de verdad para este caso)

- `C:\Development\DataManager\proyectos\CV_PICC_GENERATOR\assets\data\contenido_cv.txt`, sección "CENTRO DE DATOS DE SATÉLITES MEXICANOS", líneas 140-156.

No se encontró ningún documento adicional para este proyecto en el repositorio operativo de PICC más allá de la entrada del currículum.

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Centro de Datos de Satélites Mexicanos (Satmex) |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre proyecto ejecutado 2022-2023 |
| Facilitador | No aplica — reconstrucción documental por agente IA bajo autorización ZEUS |
| ICP hipotético (referencia interna) | ICP-H01 (Infraestructura crítica / Data Center) — es el caso del currículum con mayor especificidad técnica de clasificación formal (ICREA III, Uptime Institute) |
| Duración de la "sesión" | No aplica |

## 2. Resumen ejecutivo

Este es el caso del currículum oficial con mayor densidad de especificación técnica: clasificación ICREA III explícitamente referenciada contra el estándar de Uptime Institute, redundancia N+1 en sistemas críticos, climatización de precisión con respaldo, detección/extinción de incendios, control de acceso biométrico y CCTV, piso falso técnico. Aun así, igual que los otros dos casos de Data Center del CV, no hay ninguna cifra de presupuesto, plazo, incidente o testimonio del cliente. La reconstrucción retrospectiva logra clasificar mejor el **alcance técnico** que los casos Ixtapaluca/Data Nation, pero sigue sin poder evaluar **riesgo real vivido**.

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| Sin evidencia de si la clasificación ICREA III fue certificada por auditor externo o es una declaración de PICC sobre el diseño entregado | E (regulatorio), F (confianza institucional) | S2 — Riesgo medio, inferido: una clasificación ICREA no certificada por tercero es menos defendible ante stakeholders del cliente | E1 — Señal aislada (el CV menciona la clasificación junto a "Uptime Institute" entre paréntesis, sin aclarar si Uptime certificó el proyecto o si PICC solo diseñó "bajo" ese estándar) | 5, 9, 10 | Parcialmente soportada |
| Redundancia N+1 declarada "en todos los sistemas críticos" sin especificar cuáles sistemas se consideraron críticos | B (alcance) | S1 — Riesgo bajo (ambigüedad de alcance, no necesariamente un defecto técnico) | E0 — No evidencia (frase genérica del CV, sin lista de sistemas) | 3 | No evaluable |
| Sin ninguna cifra de presupuesto, plazo o incidente durante la ejecución | D, C | No evaluable | E0 | 4, 5 | No evaluable |
| Cliente (Satélites Mexicanos / Satmex) es una entidad de alto perfil técnico — no hay registro de si el proyecto generó una relación continua o fue un caso único | F (confianza institucional) | S1 — Riesgo bajo | E0 | 6, 12 (defender contratación ante otros) | No evaluable |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Soporte documental de la certificación ICREA III (si existe un certificado formal vs. diseño "bajo" el estándar) | Ausencia de verificación | Solicitar el documento de certificación al archivo de PICC o al cliente | Dirección PICC |
| Lista de sistemas cubiertos por la redundancia N+1 | Ausencia de definición | Documentar el alcance técnico exacto entregado | PICC Ingeniería |
| Presupuesto, plazo, resultado, satisfacción del cliente | Ausencia de dato | No existe en ninguna fuente autorizada para este ejercicio | Dirección PICC / archivo comercial |
| Estado de la relación comercial actual con Satmex (¿sigue siendo cliente?) | Información no compartida | Consultar con Comercial | Comercial PICC |

## 5. Recomendaciones priorizadas

1. Este es el caso del CV con mayor potencial como Knowledge Product o caso de referencia técnica (mayor especificidad de estándares), pero antes de usarlo como claim público verificar si "ICREA III (Uptime Institute)" es una certificación real u obtenida, para no violar la regla de evidencia de AI_EXECUTION_CONTRACT (§6.3: "si una cifra no está verificada, no se presenta como hecho").
2. Documentar la lista exacta de sistemas con redundancia N+1 para poder defender el claim ante un comprador técnico exigente (perfil ICP-H01).
3. Confirmar si existe relación comercial vigente con Satmex — si la hay, es un candidato natural para el piloto en vivo real (no retrospectivo) de RiskDiag, dado que ya hay una relación de confianza establecida.

## 6. Siguiente paso propuesto

- Siguiente paso concreto: verificar el estatus de certificación ICREA III y la vigencia de la relación con el cliente.
- Owner del siguiente paso: Dirección PICC / Comercial.
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
| 2 | Completitud | 5 de 24 preguntas del Banco pudieron responderse con algún nivel de evidencia (aprox. 21%) — la más alta de los 3 casos de Data Center del CV, por la mayor especificidad técnica del texto original | — |
| 3 | Claridad percibida | NO APLICA | — |
| 4 | Utilidad percibida | NO APLICA | — |
| 5 | Gaps identificados | 4 (ver sección 4) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | No evaluable | — |
| 7 | Reducción de retrabajo | NO APLICA | — |
| 8 | Intención de compartir | NO APLICA | — |
| 9 | Intención de avanzar | NO APLICA | — |
| 10 | Decisión afectada | Parcialmente — el ejercicio logró mover la decisión 5 ("qué riesgos existen") de "no evaluable" a "parcialmente soportada" únicamente respecto al riesgo de certificación no verificada; el resto de riesgos quedó "no evaluable" | — |
| 11 | Señal comercial downstream | NO APLICA | — |
| 12 | Errores críticos | 0 | No se detectaron defectos del método; la limitación es de fuente |
