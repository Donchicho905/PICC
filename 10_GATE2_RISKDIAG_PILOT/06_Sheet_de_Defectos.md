# Sheet de Defectos — RiskDiag V1

## Ficha de Trazabilidad
- ID: DOC-061
- Estado: 🟡 En desarrollo
- Tipo: Gate 2 — Defect Log
- Objetivo: Definir la bitácora donde se registran errores, fallas o fricciones del propio proceso de diagnóstico durante la ejecución del piloto, para que el veredicto de cierre (DOC-062) pueda distinguir entre "el método funciona pero falló la ejecución" y "el método en sí tiene un defecto estructural".
- Entradas:
  - DOC-056 (10_GATE2_RISKDIAG_PILOT/01_Protocolo_Piloto.md) — fases donde puede ocurrir un defecto
  - AI_EXECUTION_CONTRACT.md — sección 13 (Definition of Done: "los riesgos y vacíos quedan visibles")
- Salidas:
  - Bitácora de defectos por caso
  - Clasificación de severidad de defecto
- Dependencias:
  - DOC-060 (10_GATE2_RISKDIAG_PILOT/05_Hoja_de_Medicion.md) — métrica 12 (errores críticos) se alimenta de esta bitácora
  - DOC-062 (10_GATE2_RISKDIAG_PILOT/07_Plantilla_Veredicto_ZEUS.md) — consume esta bitácora
- Documentos consumidos:
  - Ninguno adicional
- Documentos generados:
  - Una fila por defecto detectado
- Responsable: Facilitador (registro) + Dirección (revisión de severidad Alta/Crítica)
- Fecha: 2026-07-16
- Criterios de aceptación:
  - Todo defecto tiene severidad, fase donde ocurrió y acción correctiva propuesta
  - Los defectos de severidad Alta o Crítica quedan visibles para el veredicto de cierre
  - No se oculta ni minimiza un defecto para que el piloto "se vea bien" (principio AI_EXECUTION_CONTRACT §15.9: no ocultar incertidumbre)

---

## Qué es un "defecto" en este contexto

Un defecto es cualquier falla en el proceso de diagnóstico, no en el proyecto del cliente. Ejemplos: una pregunta del banco que resultó ambigua, un hallazgo mal clasificado, un tiempo de sesión que se excedió sin cerrar el protocolo, un cliente que no entendió el resultado, un dato capturado incorrectamente.

Esta bitácora **no** registra los riesgos del proyecto del cliente (eso vive en DOC-059). Registra fallas del método RiskDiag mismo.

## Escala de severidad de defecto

| Severidad | Criterio |
| --- | --- |
| Baja | Fricción menor, no afectó el resultado ni la percepción del cliente |
| Media | Requirió ajuste sobre la marcha; pudo afectar la calidad del hallazgo pero no invalidó el caso |
| Alta | El defecto afectó materialmente la calidad o confiabilidad del resultado entregado al cliente |
| Crítica | El defecto invalida el caso como evidencia útil para el veredicto de cierre (ej. el cliente recibió información incorrecta, o el protocolo no pudo completarse) |

## Formato de la bitácora

| Defecto ID | Caso ID | Fecha | Fase (DOC-056) donde ocurrió | Descripción | Severidad | Hipótesis de causa raíz | Impacto en el caso | Acción correctiva | Estado | Owner |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DEF-01 | | | | | | | | | Abierto / Cerrado | |
| DEF-02 | | | | | | | | | | |

## Reglas de registro

1. Todo defecto de severidad Alta o Crítica debe registrarse el mismo día del caso, no después.
2. La "hipótesis de causa raíz" debe distinguir si el origen es: (a) el diseño del Banco de Preguntas, (b) las Reglas de Clasificación, (c) la ejecución del facilitador, o (d) una condición externa del cliente/proyecto no controlable.
3. Un defecto de causa (a) o (b) es información valiosa para una futura V2 del banco o de las reglas — no se corrige el documento durante el piloto (mismo principio que en DOC-057: no modificar mientras el piloto está en curso), se documenta para la iteración siguiente.
4. Un defecto de causa (c) es responsabilidad del facilitador y debe reportarse sin filtro — omitirlo viola AI_EXECUTION_CONTRACT §15.9.
5. Todo defecto Crítico debe evaluarse contra los criterios de detención del protocolo (DOC-056 sección 3): si el defecto refleja uno de esos criterios, el caso se marca como inválido para el conteo del piloto, no se descarta silenciosamente.

## Resumen de defectos por caso (para consolidación en DOC-062)

| Caso ID | Defectos Baja | Defectos Media | Defectos Alta | Defectos Crítica | Caso válido para veredicto |
| --- | --- | --- | --- | --- | --- |
| CASO-PILOTO-01 | | | | | Sí / No |
| CASO-PILOTO-02 | | | | | Sí / No |
| CASO-PILOTO-03 | | | | | Sí / No |
