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

## Defectos registrados en el pre-piloto retrospectivo (2026-07-16, ver DOC-063)

Los siguientes defectos se detectaron durante el pre-piloto retrospectivo (reconstrucción de 4 casos usando proyectos ya documentados del currículum PICC, sin sesión en vivo con cliente). Se registran aquí siguiendo el mismo formato, agregando entradas nuevas sin borrar las plantillas DEF-01/DEF-02 de arriba, conforme a la instrucción explícita del sprint de no ocultar hallazgos negativos.

| Defecto ID | Caso ID | Fecha | Fase (DOC-056) donde ocurrió | Descripción | Severidad | Hipótesis de causa raíz | Impacto en el caso | Acción correctiva | Estado | Owner |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DEF-03 | CASO-PREPILOTO-CHEVROLET | 2026-07-16 | Fase 3 (Clasificación) | Discrepancia de cifras entre `proyecto.json` (déficit 86.4%, 13 bajadas existentes) y `PRESUPUESTO_CHEVROLET_PLUVIAL.md` (déficit 75%, 11 bajadas) para el mismo proyecto. No es un defecto del Banco de Preguntas ni de las Reglas de Clasificación, sino de la disciplina documental interna de PICC en un proyecto real | Media | (d) condición externa del proyecto — documentos internos de PICC generados en momentos distintos del proceso de cotización que no se reconciliaron entre sí; no es causa (a) diseño del Banco ni (b) Reglas de Clasificación | El caso Chevrolet Pedregal se registró con ambas cifras y se marcó explícitamente como brecha sin resolver, siguiendo la regla de no forzar una conclusión única sin evidencia | Documentar y recomendar reconciliación antes de presentar cifras al cliente real (ver Sección 5, recomendación 1, de `caso_chevrolet_pedregal.md`) | Abierto | PICC Ingeniería |
| DEF-04 | CASO-PREPILOTO-IXTAPALUCA, CASO-PREPILOTO-DATANATION, CASO-PREPILOTO-SATMEX | 2026-07-16 | Fase 2 (Aplicación del Banco de Preguntas) | Con la única fuente disponible (`contenido_cv.txt`), la completitud del Banco de Preguntas cayó a 12.5%-21% en los 3 casos de Centro de Datos, muy por debajo del umbral de aceptación de completitud definido en DOC-062 (≥70% promedio). El CV comercial no está diseñado para capturar riesgo, presupuesto, cronograma ni satisfacción del cliente | Alta | (d) condición externa — la fuente disponible (CV de marketing) no es apta para el propósito del Banco de Preguntas, que fue diseñado para una sesión en vivo con el cliente, no para retrocapturarse de un documento comercial | Los 3 casos de Data Center del pre-piloto quedaron con la mayoría de sus 24 preguntas sin respuesta y con la mayoría de decisiones del universo base en estado "No evaluable" | No es un defecto a corregir en el Banco ni en las Reglas de Clasificación V1 — es evidencia de que la modalidad retrospectiva tiene un techo de utilidad bajo cuando la única fuente es un CV comercial. Ver recomendación explícita en DOC-063 de no sustituir el piloto en vivo con este ejercicio | Cerrado (aprendizaje documentado, no requiere acción sobre el método) | ZEUS / Dirección PICC |
| DEF-05 | CASO-PREPILOTO-CHEVROLET | 2026-07-16 | Fase 0 (Selección y preparación del caso) | El proyecto Chevrolet Pedregal no aparece en `contenido_cv.txt` (el currículum oficial de 24 proyectos), pese a ser el caso con mayor densidad de evidencia técnica real del repositorio de PICC. Se usó como fuente adicional un directorio de proyecto operativo (`proyectos/CHEVROLET-2025-001/`) fuera de la ruta originalmente asumida por el encargo (`CV_PICC_GENERATOR/assets/data/`) | Media | (d) condición externa — el encargo asumió una ubicación de archivo que no coincidía con la estructura real del repositorio; se verificó y documentó la ruta real antes de usarla | Ninguno sobre la calidad del caso en sí (la fuente real usada es más rica que el CV); sí genera una discrepancia entre "proyectos del currículum oficial" (mandato original de la tarea) y "proyectos reales de PICC" (lo efectivamente usado) | Documentado explícitamente en la sección de fuentes de `caso_chevrolet_pedregal.md` y en DOC-063. Se recomienda que una futura versión del currículum comercial de PICC evalúe incorporar Chevrolet Pedregal si el proyecto se concreta | Cerrado (documentado, no invalida el caso) | ZEUS |

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

## Resumen de defectos del pre-piloto retrospectivo (2026-07-16 — NO son los casos piloto reales de DOC-062)

Esta tabla es informativa del pre-piloto documental (DOC-063). No sustituye ni cuenta como insumo para el checklist de veredicto de DOC-062, que exige explícitamente casos ejecutados en sesión real con cliente (ver DOC-062, Sección 1).

| Caso ID (pre-piloto) | Defectos Baja | Defectos Media | Defectos Alta | Defectos Crítica | Caso válido como evidencia preparatoria |
| --- | --- | --- | --- | --- | --- |
| CASO-PREPILOTO-CHEVROLET | 0 | 1 (DEF-03), 1 (DEF-05) | 0 | 0 | Sí, como evidencia preparatoria únicamente |
| CASO-PREPILOTO-IXTAPALUCA | 0 | 0 | 1 (DEF-04, compartido con los 3 casos de Data Center) | 0 | Sí, como evidencia preparatoria únicamente |
| CASO-PREPILOTO-DATANATION | 0 | 0 | 1 (DEF-04, compartido) | 0 | Sí, como evidencia preparatoria únicamente |
| CASO-PREPILOTO-SATMEX | 0 | 0 | 1 (DEF-04, compartido) | 0 | Sí, como evidencia preparatoria únicamente |
