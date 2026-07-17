# Hoja de Medición — RiskDiag V1

## Ficha de Trazabilidad
- ID: DOC-060
- Estado: 🟡 En desarrollo
- Tipo: Gate 2 — Measurement Sheet
- Objetivo: Definir las 12 métricas autorizadas (00_IMPLEMENTATION_REPORT.md, sección "Active Program", punto 5) que se capturan en cada caso del piloto RiskDiag, con su definición operativa, momento de captura y fuente de dato, para que el veredicto de cierre (DOC-062) tenga base cuantitativa comparable entre los 3-5 casos.
- Entradas:
  - 00_IMPLEMENTATION_REPORT.md — sección "Active Program (Single Next Sprint)", punto 5 (lista autorizada de métricas)
  - DOC-056 (10_GATE2_RISKDIAG_PILOT/01_Protocolo_Piloto.md)
- Salidas:
  - Tabla de métricas por caso
  - Definición operativa de cada métrica
- Dependencias:
  - DOC-059 (10_GATE2_RISKDIAG_PILOT/04_Plantilla_de_Resultado.md)
  - DOC-062 (10_GATE2_RISKDIAG_PILOT/07_Plantilla_Veredicto_ZEUS.md) — consume esta hoja
- Documentos consumidos:
  - Ninguno adicional
- Documentos generados:
  - Una fila de esta hoja por caso ejecutado (registro fuera de este repo si contiene datos de cliente identificables)
- Responsable: Facilitador (captura) + Dirección (consolidación)
- Fecha: 2026-07-16
- Criterios de aceptación:
  - Las 12 métricas coinciden exactamente con las autorizadas en 00_IMPLEMENTATION_REPORT.md
  - Cada métrica tiene definición operativa, no solo nombre
  - Cada métrica indica cuándo y cómo se captura

---

## Tabla maestra de las 12 métricas autorizadas

| # | Métrica | Definición operativa | Cómo se captura | Cuándo se captura | Escala |
| --- | --- | --- | --- | --- | --- |
| 1 | Tiempo de diagnóstico | Minutos totales desde inicio de Fase 1 hasta cierre de Fase 5 del protocolo (DOC-056) | Cronómetro o reloj, anotado por el facilitador | Durante la sesión | Minutos |
| 2 | Completitud | Porcentaje de preguntas obligatorias del Banco (DOC-057) que se respondieron con algún nivel de confianza (E0 o mayor) | Conteo de preguntas respondidas / preguntas obligatorias aplicables al caso | Al cierre de Fase 2 | % |
| 3 | Claridad percibida | Qué tan claro le resultó al cliente el resultado entregado | Pregunta directa al cliente en Fase 5: "del 1 al 5, ¿qué tan claro fue este diagnóstico?" | Fase 5, inmediatamente tras la entrega | Escala 1-5 |
| 4 | Utilidad percibida | Qué tan útil le resultó al cliente el resultado para su decisión | Pregunta directa: "del 1 al 5, ¿qué tan útil te resultó para decidir?" | Fase 5 | Escala 1-5 |
| 5 | Gaps identificados | Número de brechas de información registradas en la sección 4 de la Plantilla de Resultado (DOC-059) | Conteo directo del documento de resultado | Al cierre de Fase 4 | Número entero |
| 6 | Cambio de prioridad | Si el cliente reporta que el diagnóstico cambió la prioridad relativa del proyecto dentro de su organización | Pregunta directa en Fase 5: "¿esto cambia la prioridad de este proyecto para ti?" (Sí/No/No sabe) | Fase 5 | Sí / No / No sabe |
| 7 | Reducción de retrabajo | Si el cliente identifica que el diagnóstico evita repetir trabajo ya hecho o mal encaminado (ej. releer un alcance mal definido) | Pregunta directa: "¿esto te evita repetir o corregir algo que ya habías hecho?" (Sí/No/No aplica) | Fase 5 | Sí / No / No aplica |
| 8 | Intención de compartir | Si el cliente declara que compartiría el resultado con alguien más en su organización | Pregunta directa (también capturada en G-02 del Banco de Preguntas) | Fase 5 | Sí / No / No sabe |
| 9 | Intención de avanzar | Si el cliente declara intención de dar un siguiente paso concreto con PICC | Pregunta directa (también capturada en G-01) | Fase 5 | Sí / No / Tal vez |
| 10 | Decisión afectada | Si el diagnóstico ayudó a resolver, mover de estado o clarificar al menos una decisión del universo base (DOC-012) | Comparación: estado de la decisión antes vs. después de la sesión, según el facilitador | Fase 3-4 | Sí / No, por decisión (1-14) |
| 11 | Señal comercial downstream | Si el caso genera un evento comercial posterior verificable (reunión agendada, solicitud de propuesta, contacto adicional) en los 15 días posteriores | Seguimiento del facilitador a 15 días | Follow-up, 15 días después | Sí / No / Pendiente |
| 12 | Errores críticos | Número de defectos de severidad Alta o Crítica registrados en el Sheet de Defectos (DOC-061) para ese caso | Conteo del Sheet de Defectos | Al cierre del caso | Número entero |

---

## Formato de captura por caso

Para cada caso ejecutado, se llena una fila con las 12 métricas. Se recomienda una tabla simple (hoja de cálculo local, no necesariamente en este repo si contiene datos de cliente identificables):

| Caso ID | 1. Tiempo (min) | 2. Completitud (%) | 3. Claridad (1-5) | 4. Utilidad (1-5) | 5. Gaps (n) | 6. Cambio prioridad | 7. Reducción retrabajo | 8. Intención compartir | 9. Intención avanzar | 10. Decisión afectada | 11. Señal comercial | 12. Errores críticos |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CASO-PILOTO-01 | | | | | | | | | | | | |
| CASO-PILOTO-02 | | | | | | | | | | | | |
| CASO-PILOTO-03 | | | | | | | | | | | | |
| CASO-PILOTO-04 (opcional) | | | | | | | | | | | | |
| CASO-PILOTO-05 (opcional) | | | | | | | | | | | | |

## Reglas de consolidación

1. No promediar escalas Sí/No/Tal vez — se reportan como proporción (ej. "3 de 4 casos: Sí").
2. Las escalas 1-5 (claridad, utilidad) se promedian y se reporta también el rango (mínimo-máximo).
3. La métrica 11 (señal comercial downstream) no puede cerrarse hasta que pasen 15 días desde cada caso — el veredicto de cierre (DOC-062) debe esperar a que el último caso cumpla ese plazo, o marcar explícitamente esa métrica como "pendiente" en el veredicto.
4. Ningún caso con dato faltante en una métrica se descarta; se marca "no capturado" y se documenta la razón en el Sheet de Defectos si aplica.
