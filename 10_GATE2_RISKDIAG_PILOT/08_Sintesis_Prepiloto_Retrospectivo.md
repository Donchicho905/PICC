# Síntesis del Pre-piloto Retrospectivo — RiskDiag V1

## Ficha de Trazabilidad
- ID: DOC-063
- Estado: 🟡 En desarrollo
- Tipo: Gate 2 — Retrospective Pre-Pilot Synthesis
- Objetivo: Consolidar y evaluar el resultado de reconstruir 4 casos usando proyectos reales ya documentados del currículum operativo de PICC (sin sesión en vivo con cliente), para validar mecánicamente si el Banco de Preguntas (DOC-057) y las Reglas de Clasificación (DOC-058) funcionan de forma consistente contra datos reales, antes de que un humano de PICC ejecute el piloto real de 3-5 casos exigido por DOC-062.
- Entradas:
  - DOC-056 (10_GATE2_RISKDIAG_PILOT/01_Protocolo_Piloto.md)
  - DOC-057 (10_GATE2_RISKDIAG_PILOT/02_Banco_de_Preguntas.md)
  - DOC-058 (10_GATE2_RISKDIAG_PILOT/03_Reglas_de_Clasificacion.md)
  - DOC-059 (10_GATE2_RISKDIAG_PILOT/04_Plantilla_de_Resultado.md)
  - DOC-060 (10_GATE2_RISKDIAG_PILOT/05_Hoja_de_Medicion.md)
  - DOC-061 (10_GATE2_RISKDIAG_PILOT/06_Sheet_de_Defectos.md), entradas DEF-03 a DEF-05
  - `C:\Development\DataManager\proyectos\CV_PICC_GENERATOR\assets\data\contenido_cv.txt`
  - `C:\Development\DataManager\proyectos\CHEVROLET-2025-001\` (proyecto.json, CALCULO_PLUVIAL_CHEVROLET.md, PRESUPUESTO_CHEVROLET_PLUVIAL.md, catálogo de fotos)
  - `C:\Development\DataManager\proyectos\CV_PICC_GENERATOR\memoria_calculo_pluvial.txt`, `analisis_llenado_cisternas.txt`
- Salidas:
  - 4 archivos de caso reconstruidos en `10_GATE2_RISKDIAG_PILOT/casos/`
  - Este documento de síntesis
  - Actualización de DOC-061 con defectos DEF-03 a DEF-05
- Dependencias:
  - Ninguna hacia adelante — este documento no es insumo obligatorio de DOC-062 (ver Sección 5)
- Documentos consumidos:
  - Los 4 archivos de `10_GATE2_RISKDIAG_PILOT/casos/` (caso_chevrolet_pedregal.md, caso_centro_datos_ixtapaluca.md, caso_data_nation_queretaro.md, caso_satmex_centro_datos.md)
- Documentos generados:
  - Ninguno adicional
- Responsable: ZEUS (bajo autorización del sprint), ejecución agente IA
- Fecha: 2026-07-16
- Criterios de aceptación:
  - El documento distingue explícitamente entre "el método funciona" y "la fuente disponible es pobre"
  - El documento no presenta este pre-piloto como sustituto del piloto real exigido por DOC-062
  - Todo hallazgo negativo queda registrado en DOC-061, sin ocultarse

---

## 1. Qué es y qué NO es este documento

Este documento sintetiza un ejercicio **documental y retrospectivo**: reconstruir 4 "casos" de RiskDiag usando proyectos reales de PICC ya documentados, sin sesión en vivo con ningún cliente. No hay facilitador humano, no hay cliente respondiendo, no hay las 8 métricas de percepción/intención de DOC-060 (claridad, utilidad, cambio de prioridad declarado por el cliente, reducción de retrabajo declarada, intención de compartir, intención de avanzar, señal comercial downstream).

**Este documento NO es, ni pretende ser, el piloto de 3-5 casos reales exigido por el veredicto ZEUS final (DOC-062).** Es evidencia preparatoria: sirve para detectar si el Banco de Preguntas y las Reglas de Clasificación tienen defectos de diseño *antes* de gastar el tiempo de un cliente real en una sesión en vivo. Ver Sección 5 para la recomendación explícita sobre esta distinción.

## 2. Casos reconstruidos

| Caso | Fuente principal | Tipo de proyecto | ICP hipotético | Completitud del Banco lograda |
| --- | --- | --- | --- | --- |
| Chevrolet Pedregal (`caso_chevrolet_pedregal.md`) | Documentación operativa real del proyecto (`proyectos/CHEVROLET-2025-001/`) — **no está en el CV oficial** | Comercial/industrial — rehabilitación pluvial y techumbre | ICP-H02 (hipótesis) | ~62.5% (15/24 preguntas) |
| Centro de Datos Ixtapaluca (`caso_centro_datos_ixtapaluca.md`) | Currículum oficial (`contenido_cv.txt`) únicamente | Data Center | ICP-H01 | ~17% (4/24 preguntas) |
| Data Nation Querétaro (`caso_data_nation_queretaro.md`) | Currículum oficial (`contenido_cv.txt`) únicamente | Data Center Tier II | ICP-H01 | ~12.5% (3/24 preguntas) |
| Satmex — Centro de Datos de Satélites Mexicanos (`caso_satmex_centro_datos.md`) | Currículum oficial (`contenido_cv.txt`) únicamente | Data Center ICREA III | ICP-H01 | ~21% (5/24 preguntas) |

## 3. Qué se validó del método

1. **El Banco de Preguntas (DOC-057) es aplicable sin modificación a proyectos de naturaleza muy distinta** (rehabilitación pluvial industrial vs. Data Centers de alta especificación técnica). No fue necesario inventar preguntas nuevas ni forzar preguntas fuera de contexto — se usó el mecanismo ya previsto de "omitir y documentar" para las preguntas ICP-específicas que no aplicaban.
2. **Las Reglas de Clasificación (DOC-058) permitieron clasificar de forma consistente incluso con evidencia muy dispar entre casos.** El caso Chevrolet, con evidencia E3 abundante, y los tres casos de Data Center, con evidencia mayormente E0-E1, se clasificaron con la misma escala sin necesidad de ajustarla.
3. **La regla de "ningún hallazgo E0-E1 se presenta como certeza" (DOC-058, Sección 5) se pudo aplicar de forma disciplinada.** En los 3 casos de Data Center, la mayoría de los hallazgos quedaron redactados explícitamente como inferencias del reconstructor, no como hechos — el método obliga a esa honestidad incluso cuando la fuente es pobre.
4. **El vínculo hallazgo → decisión del comprador (universo de 14 decisiones, DOC-012) funcionó en todos los casos** sin necesidad de agregar una decisión nueva al universo base.
5. **El caso Chevrolet Pedregal confirma la hipótesis de partida del sprint:** con evidencia real suficiente (memoria de cálculo, catálogo fotográfico con descripciones, presupuesto), el método sí habría anticipado explícitamente el riesgo de deterioro/filtración de techumbre antes de que se agravara — la filtración interior ya visible en el taller mecánico se habría capturado en Bloque D (riesgo técnico) con severidad S4, exactamente el tipo de hallazgo que el diseño del método pretende priorizar (DOC-058, Sección 7, regla de priorización 1: "Severidad S3-S4 con cualquier nivel de confianza").

## 4. Qué falló o generó dudas (ver también DOC-061, DEF-03 a DEF-05)

1. **Completitud del Banco cae drásticamente (12.5%-21%) cuando la única fuente es el currículum comercial oficial**, muy por debajo del umbral de aceptación de 70% que exige DOC-062 para el criterio "Disciplina de evidencia". Esto no es un defecto del Banco de Preguntas ni de las Reglas de Clasificación — es una limitación estructural de la modalidad retrospectiva cuando se usa una fuente que no fue diseñada para capturar riesgo (ver DEF-04).
2. **Se encontró una discrepancia de cifras dentro de la propia documentación interna de PICC** en el caso Chevrolet (déficit de capacidad pluvial reportado como 75% en un documento y 86.4% en otro; 11 vs. 13 bajadas existentes). Esto no es un defecto del método RiskDiag, pero es un hallazgo relevante para la disciplina de evidencia interna de PICC en general (ver DEF-03).
3. **El proyecto con mayor riqueza de evidencia (Chevrolet Pedregal) no forma parte del currículum comercial oficial** (`contenido_cv.txt`), lo que generó una desviación respecto a la instrucción original del sprint de usar "proyectos del currículum PICC". Se documenta esta desviación explícitamente en vez de forzar el uso exclusivo de proyectos con poca evidencia solo por estar en el CV (ver DEF-05 y razonamiento en Sección 6).
4. **Ninguna de las 8 métricas de percepción/intención de DOC-060 pudo capturarse** (claridad, utilidad, cambio de prioridad declarado, reducción de retrabajo declarada, intención de compartir, intención de avanzar, señal comercial downstream) — son estructuralmente imposibles de obtener sin un cliente real respondiendo en una sesión. Esto confirma que DOC-060 está correctamente diseñado para sesión en vivo, no para modalidad retrospectiva.
5. **El estado de las decisiones del universo base (DOC-012) quedó mayormente "No evaluable" en los 3 casos de Data Center**, no porque la decisión no importe, sino porque la fuente no contiene la información necesaria para evaluarla siquiera. Esto es consistente con el diseño de DOC-058 (Sección 6, regla de "No evaluable"), pero deja en evidencia que un CV de 24 proyectos, por sí solo, no es una base suficiente para un ejercicio de validación completo del método.

## 5. Recomendación explícita — este pre-piloto NO cierra el Gate 2

**Este pre-piloto retrospectivo es evidencia preparatoria, no evidencia de cierre de Gate 2.** No sustituye el piloto en vivo de 3-5 casos reales con clientes reales que exige el Protocolo (DOC-056) y que es requisito de entrada del veredicto ZEUS (DOC-062, Sección 1: "Solo al cierre de un piloto real de 3-5 casos ejecutados siguiendo el Protocolo"). Las razones concretas:

1. Ninguna de las 8 métricas de percepción/intención del cliente (métricas 3, 4, 6, 7, 8, 9, 11 de DOC-060) pudo capturarse, y son precisamente las métricas que sostienen la mayoría de los criterios de aceptación de DOC-062 (Sección 3): claridad percibida, utilidad percibida, intención de compartir, intención de avanzar, señal comercial downstream.
2. El Protocolo (DOC-056) exige explícitamente que un caso simulado nunca se documente como caso real ("Criterio de detención... si no hay proyecto real disponible, no se simula un caso"). Este pre-piloto no simula proyectos — usa datos reales — pero tampoco ejecuta una sesión real; es una categoría distinta que el Protocolo no contempló y que este documento distingue explícitamente para no generar ambigüedad.
3. El checklist previo de DOC-062 (Sección 2) exige "al menos 3 casos con resultado entregado y clasificado" en el contexto de un piloto ejecutado — los 4 casos de este documento no fueron entregados a ningún cliente, por lo tanto no cumplen ese requisito aunque tengan el mismo formato de resultado.

**Próximo paso autorizado:** un humano de PICC (Dirección o Comercial) ejecuta el Protocolo (DOC-056) sobre 3-5 proyectos reales en sesión en vivo, tal como ya lo establece D-0021 en `99_META/DECISION_HISTORY.md`. Este pre-piloto no cambia ni acelera esa necesidad — solo reduce el riesgo de que el Banco de Preguntas o las Reglas de Clasificación fallen estructuralmente durante la sesión real, porque ya se probaron contra datos reales sin encontrar defectos de diseño (Sección 3, DEF-04 y DEF-05 son limitaciones de fuente, no del método).

## 6. Nota sobre la elección de casos

Se priorizó incluir Chevrolet Pedregal pese a no estar en el currículum comercial oficial porque es, con amplio margen, el proyecto con mayor densidad de evidencia real de riesgo técnico disponible en el repositorio de PICC — y porque el objetivo explícito de este sprint fue "ver si el método hubiera anticipado riesgos que de hecho ocurrieron". Los otros tres proyectos (Ixtapaluca, Data Nation, Satmex) sí provienen exclusivamente del currículum oficial y muestran, de forma honesta, el techo de utilidad del método cuando la única fuente disponible es un documento de marketing. Ambos resultados —uno rico, tres pobres— son útiles: el primero confirma que el método captura bien el riesgo cuando hay evidencia; los otros tres confirman que el método no puede compensar la ausencia de evidencia, y que ningún nivel de sofisticación en el Banco de Preguntas sustituye una sesión real con quien vivió el proyecto.

## 7. Evaluación honesta de calidad de datos por caso

| Caso | Calidad de datos disponible | Justificación |
| --- | --- | --- |
| Chevrolet Pedregal | **Alta** | Memoria de cálculo con 4 revisiones, presupuesto desglosado por fase, catálogo fotográfico con 26 descripciones textuales de hallazgos reales, datos técnicos estructurados en `proyecto.json`. Es el único caso con evidencia de nivel E3 (evidencia operativa) en múltiples hallazgos |
| Centro de Datos Ixtapaluca | **Pobre** | Solo el texto del CV comercial (unas 20 líneas). Sin presupuesto, cronograma, incidentes o testimonio. Explícitamente reconocido como pobre en `caso_centro_datos_ixtapaluca.md`, Sección 2 |
| Data Nation Querétaro | **Pobre** | Igual que el anterior; adicionalmente con una ambigüedad de alcance (proyecto ejecutivo vs. construcción) que el propio CV no aclara |
| Satmex | **Pobre, con matiz** | Texto del CV más específico técnicamente que los otros dos (menciona Uptime Institute, N+1, biométrico), pero sigue sin presupuesto, cronograma ni resultado. Es el "menos pobre de los pobres", no un caso de datos suficientes |
