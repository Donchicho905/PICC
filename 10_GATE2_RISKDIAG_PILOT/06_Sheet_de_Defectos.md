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
| DEF-06 | CASO-PREPILOTO-MAYRAN | 2026-07-16 | Fase 3 (Clasificación) | Discrepancia de -28% entre el costo calculado por el sistema paramétrico interno de PICC/DEDALO (`ANALISIS_DIFERENCIAS.md`: $588,293.58 / $472,898.84 según fase) y el precio finalmente cotizado y contratado al cliente ($829,980 / $996,466.17 con IVA). No es un defecto del Banco ni de las Reglas de Clasificación — es evidencia de la brecha entre pricing paramétrico interno y precio comercial final | Media | (d) condición externa del proceso de pricing de PICC — la estimación original usa precios de mercado de subcontratista con margen alto; el sistema calcula costos directos propios. Documentado y explicado en la propia fuente (`ANALISIS_DIFERENCIAS.md`, Sección "Conclusiones") | El caso Bodega Mayran se registró con ambas cifras y se marcó explícitamente como hallazgo de proceso interno, no de riesgo del cliente | Ninguna acción sobre el Banco/Reglas de Clasificación V1. Recomendación operativa (fuera del alcance de este pre-piloto): la propia fuente ya recomienda "mantener precio de estimación original para cotizar" y "usar precios del sistema para control interno" | Cerrado (aprendizaje documentado, la propia fuente ya lo resolvió operativamente) | Dirección PICC |
| DEF-07 | CASO-PREPILOTO-MAYRAN | 2026-07-16 | Fase 3 (Clasificación) | Segunda discrepancia de -20.8% entre una cotización temprana hallada en la carpeta `CARDEAL-2026-001` ($1,257,991.21 con IVA, fechada 21-Feb-2026, 39 partidas detalladas) y el monto contratado según `HISTORIAL.md` ($996,466.17 con IVA, propuesta formal fechada 21-Ene-2026 — es decir, un mes *antes* de la cotización de mayor monto). A diferencia de DEF-06, esta discrepancia no tiene explicación documentada en ninguna fuente consultada | Alta | No se pudo determinar con las fuentes disponibles si la causa es (a)/(b) del método RiskDiag (no aplica, es discrepancia de precio del proyecto, no de clasificación) o (d) condición externa — probablemente dos rondas de cotización del mismo proyecto sin reconciliación documentada, pero no se pudo confirmar la secuencia real | El caso Bodega Mayran documentó ambas cifras y marcó la decisión de presupuesto (DOC-012 #4) como "no evaluable" para esta brecha específica, en vez de forzar una conclusión | Recomendado a Dirección PICC en `caso_mayran_bodega.md` Sección 5, punto 3: reconciliar antes de que se repita en otro proyecto del mismo cliente | Abierto | Dirección PICC / Rafael Chapa |
| DEF-08 | CASO-PREPILOTO-PALMAS-OFICINAS | 2026-07-16 | Fase 0 (Selección y preparación del caso) | El proyecto `PALMAS-2026-001` fue identificado en el encargo original como candidato para la categoría "casa habitación", agrupado con la carpeta índice `Presupuesto_Casa_Las_Palmas`. La lectura directa de la fuente (`RESUMEN_PROYECTO.md`, `PROYECTO_INFO.json`, `CATALOGO_ESPACIOS.md`) muestra sin ambigüedad que es un proyecto de acondicionamiento de **oficinas comerciales**, no de vivienda. Además, dentro del propio proyecto, tres documentos (`RESUMEN_PROYECTO.md`, `PROYECTO_INFO.json`, `CATALOGO_ESPACIOS.md`) reportan tres cifras de área total distintas (200 m², 145 m², 147.31 m²) sin reconciliar | Alta | (d) condición externa — el nombre coloquial de la carpeta índice ERP ("Casa Las Palmas") es engañoso respecto al contenido real del proyecto; el área no reconciliada es un defecto de captura del propio expediente de PICC, anterior a este ejercicio | Se corrigió el encuadre explícitamente en `caso_oficinas_palmas936.md` (sección "Corrección de encuadre"), reclasificando el caso a Oficinas. Esto resolvió la categoría de oficinas (sin expediente disponible antes de esta corrección) y dejó pendiente, sin forzar, la categoría de casa habitación | Recomendado a Dirección PICC renombrar la carpeta índice ERP para evitar que el error de clasificación se repita, y reconciliar las tres cifras de área antes de reactivar el proyecto | Abierto | Dirección PICC / CONSUL (mantenimiento del ERP) |
| DEF-09 | N/A (gap, no caso) | 2026-07-16 | Fase 0 (Selección y preparación del caso) | Dos categorías solicitadas en el encargo (casa habitación, data centers) no alcanzaron el umbral de calidad para generar un caso nuevo. Casa habitación: los únicos candidatos (`OREA-2026-001` / `Remodelacion_Casa_Familia_Orea`, confirmados como el mismo proyecto cancelado) solo tienen físicamente en el repositorio un índice ERP y 1 fotografía sin procesar — los documentos sustantivos que el índice lista no están presentes en este repositorio. Data centers: no se localizó ningún expediente nuevo (`ORION-CYMIT` es seguridad perimetral para CIMMYT, no un Data Center; las menciones de "HYPERION" en `output/` son manifiestos de agente, no expedientes de cliente) | Alta | (d) condición externa — ausencia real de expediente en el repositorio para ambas categorías, no un defecto del método ni de la búsqueda | Ninguno sobre el método — se documenta el gap honestamente en vez de forzar un caso pobre o duplicar los 3 casos de Data Center ya hechos en Ronda 1 | Ninguna acción sobre el Banco/Reglas de Clasificación. Recomendación operativa: si PICC concreta un proyecto residencial o de Data Center con expediente real en el futuro, usarlo para completar estas dos categorías | Abierto (gap de evidencia, no de método) | Dirección PICC |

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

## Resumen de defectos — Ronda 2 (2026-07-16, ver DOC-063 sección 8 — tampoco cuentan como insumo de DOC-062)

| Caso ID (pre-piloto, Ronda 2) | Defectos Baja | Defectos Media | Defectos Alta | Defectos Crítica | Caso válido como evidencia preparatoria |
| --- | --- | --- | --- | --- | --- |
| CASO-PREPILOTO-MAYRAN | 0 | 1 (DEF-06) | 1 (DEF-07) | 0 | Sí, como evidencia preparatoria únicamente |
| CASO-PREPILOTO-NISSAN-ANDRADE | 0 | 0 | 0 | 0 | Sí, como evidencia preparatoria únicamente |
| CASO-PREPILOTO-PALMAS-OFICINAS | 0 | 0 | 1 (DEF-08) | 0 | Sí, como evidencia preparatoria únicamente |
| (gap: casa habitación, data centers) | 0 | 0 | 1 (DEF-09, compartido entre ambas categorías) | 0 | No aplica — no se generó caso, se documentó el gap |
