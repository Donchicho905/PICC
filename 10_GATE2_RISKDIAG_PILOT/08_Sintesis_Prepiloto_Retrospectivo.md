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
  - `C:\Development\DataManager\proyectos\CASO-01-PROY\` (proyecto.json, CALCULO_PLUVIAL_CASO-01.md, PRESUPUESTO_CASO-01_PLUVIAL.md, catálogo de fotos)
  - `C:\Development\DataManager\proyectos\CV_PICC_GENERATOR\memoria_calculo_pluvial.txt`, `analisis_llenado_cisternas.txt`
- Salidas:
  - 4 archivos de caso reconstruidos en `10_GATE2_RISKDIAG_PILOT/casos/`
  - Este documento de síntesis
  - Actualización de DOC-061 con defectos DEF-03 a DEF-05
- Dependencias:
  - Ninguna hacia adelante — este documento no es insumo obligatorio de DOC-062 (ver Sección 5)
- Documentos consumidos:
  - Los 4 archivos de `10_GATE2_RISKDIAG_PILOT/casos/` (caso_01_techumbre_comercial.md, caso_02_centro_datos_i.md, caso_03_centro_datos_ii.md, caso_04_centro_datos_iii.md)
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
| Caso-01 (`caso_01_techumbre_comercial.md`) | Documentación operativa real del proyecto (`proyectos/CASO-01-PROY/`) — **no está en el CV oficial** | Comercial/industrial — rehabilitación pluvial y techumbre | ICP-H02 (hipótesis) | ~62.5% (15/24 preguntas) |
| Caso-02 (`caso_02_centro_datos_i.md`) | Currículum oficial (`contenido_cv.txt`) únicamente | Data Center | ICP-H01 | ~17% (4/24 preguntas) |
| Caso-03 (`caso_03_centro_datos_ii.md`) | Currículum oficial (`contenido_cv.txt`) únicamente | Data Center Tier II | ICP-H01 | ~12.5% (3/24 preguntas) |
| Caso-04 — Caso-04 (`caso_04_centro_datos_iii.md`) | Currículum oficial (`contenido_cv.txt`) únicamente | Data Center ICREA III | ICP-H01 | ~21% (5/24 preguntas) |

## 3. Qué se validó del método

1. **El Banco de Preguntas (DOC-057) es aplicable sin modificación a proyectos de naturaleza muy distinta** (rehabilitación pluvial industrial vs. Data Centers de alta especificación técnica). No fue necesario inventar preguntas nuevas ni forzar preguntas fuera de contexto — se usó el mecanismo ya previsto de "omitir y documentar" para las preguntas ICP-específicas que no aplicaban.
2. **Las Reglas de Clasificación (DOC-058) permitieron clasificar de forma consistente incluso con evidencia muy dispar entre casos.** El caso Caso-01, con evidencia E3 abundante, y los tres casos de Data Center, con evidencia mayormente E0-E1, se clasificaron con la misma escala sin necesidad de ajustarla.
3. **La regla de "ningún hallazgo E0-E1 se presenta como certeza" (DOC-058, Sección 5) se pudo aplicar de forma disciplinada.** En los 3 casos de Data Center, la mayoría de los hallazgos quedaron redactados explícitamente como inferencias del reconstructor, no como hechos — el método obliga a esa honestidad incluso cuando la fuente es pobre.
4. **El vínculo hallazgo → decisión del comprador (universo de 14 decisiones, DOC-012) funcionó en todos los casos** sin necesidad de agregar una decisión nueva al universo base.
5. **El caso Caso-01 confirma la hipótesis de partida del sprint:** con evidencia real suficiente (memoria de cálculo, catálogo fotográfico con descripciones, presupuesto), el método sí habría anticipado explícitamente el riesgo de deterioro/filtración de techumbre antes de que se agravara — la filtración interior ya visible en el taller mecánico se habría capturado en Bloque D (riesgo técnico) con severidad S4, exactamente el tipo de hallazgo que el diseño del método pretende priorizar (DOC-058, Sección 7, regla de priorización 1: "Severidad S3-S4 con cualquier nivel de confianza").

## 4. Qué falló o generó dudas (ver también DOC-061, DEF-03 a DEF-05)

1. **Completitud del Banco cae drásticamente (12.5%-21%) cuando la única fuente es el currículum comercial oficial**, muy por debajo del umbral de aceptación de 70% que exige DOC-062 para el criterio "Disciplina de evidencia". Esto no es un defecto del Banco de Preguntas ni de las Reglas de Clasificación — es una limitación estructural de la modalidad retrospectiva cuando se usa una fuente que no fue diseñada para capturar riesgo (ver DEF-04).
2. **Se encontró una discrepancia de cifras dentro de la propia documentación interna de PICC** en el caso Caso-01 (déficit de capacidad pluvial reportado como 75% en un documento y 86.4% en otro; 11 vs. 13 bajadas existentes). Esto no es un defecto del método RiskDiag, pero es un hallazgo relevante para la disciplina de evidencia interna de PICC en general (ver DEF-03).
3. **El proyecto con mayor riqueza de evidencia (Caso-01) no forma parte del currículum comercial oficial** (`contenido_cv.txt`), lo que generó una desviación respecto a la instrucción original del sprint de usar "proyectos del currículum PICC". Se documenta esta desviación explícitamente en vez de forzar el uso exclusivo de proyectos con poca evidencia solo por estar en el CV (ver DEF-05 y razonamiento en Sección 6).
4. **Ninguna de las 8 métricas de percepción/intención de DOC-060 pudo capturarse** (claridad, utilidad, cambio de prioridad declarado, reducción de retrabajo declarada, intención de compartir, intención de avanzar, señal comercial downstream) — son estructuralmente imposibles de obtener sin un cliente real respondiendo en una sesión. Esto confirma que DOC-060 está correctamente diseñado para sesión en vivo, no para modalidad retrospectiva.
5. **El estado de las decisiones del universo base (DOC-012) quedó mayormente "No evaluable" en los 3 casos de Data Center**, no porque la decisión no importe, sino porque la fuente no contiene la información necesaria para evaluarla siquiera. Esto es consistente con el diseño de DOC-058 (Sección 6, regla de "No evaluable"), pero deja en evidencia que un CV de 24 proyectos, por sí solo, no es una base suficiente para un ejercicio de validación completo del método.

## 5. Recomendación explícita — este pre-piloto NO cierra el Gate 2

**Este pre-piloto retrospectivo es evidencia preparatoria, no evidencia de cierre de Gate 2.** No sustituye el piloto en vivo de 3-5 casos reales con clientes reales que exige el Protocolo (DOC-056) y que es requisito de entrada del veredicto ZEUS (DOC-062, Sección 1: "Solo al cierre de un piloto real de 3-5 casos ejecutados siguiendo el Protocolo"). Las razones concretas:

1. Ninguna de las 8 métricas de percepción/intención del cliente (métricas 3, 4, 6, 7, 8, 9, 11 de DOC-060) pudo capturarse, y son precisamente las métricas que sostienen la mayoría de los criterios de aceptación de DOC-062 (Sección 3): claridad percibida, utilidad percibida, intención de compartir, intención de avanzar, señal comercial downstream.
2. El Protocolo (DOC-056) exige explícitamente que un caso simulado nunca se documente como caso real ("Criterio de detención... si no hay proyecto real disponible, no se simula un caso"). Este pre-piloto no simula proyectos — usa datos reales — pero tampoco ejecuta una sesión real; es una categoría distinta que el Protocolo no contempló y que este documento distingue explícitamente para no generar ambigüedad.
3. El checklist previo de DOC-062 (Sección 2) exige "al menos 3 casos con resultado entregado y clasificado" en el contexto de un piloto ejecutado — los 4 casos de este documento no fueron entregados a ningún cliente, por lo tanto no cumplen ese requisito aunque tengan el mismo formato de resultado.

**Próximo paso autorizado:** un humano de PICC (Dirección o Comercial) ejecuta el Protocolo (DOC-056) sobre 3-5 proyectos reales en sesión en vivo, tal como ya lo establece D-0021 en `99_META/DECISION_HISTORY.md`. Este pre-piloto no cambia ni acelera esa necesidad — solo reduce el riesgo de que el Banco de Preguntas o las Reglas de Clasificación fallen estructuralmente durante la sesión real, porque ya se probaron contra datos reales sin encontrar defectos de diseño (Sección 3, DEF-04 y DEF-05 son limitaciones de fuente, no del método).

## 6. Nota sobre la elección de casos

Se priorizó incluir Caso-01 pese a no estar en el currículum comercial oficial porque es, con amplio margen, el proyecto con mayor densidad de evidencia real de riesgo técnico disponible en el repositorio de PICC — y porque el objetivo explícito de este sprint fue "ver si el método hubiera anticipado riesgos que de hecho ocurrieron". Los otros tres proyectos (Caso-02, Caso-03, Caso-04) sí provienen exclusivamente del currículum oficial y muestran, de forma honesta, el techo de utilidad del método cuando la única fuente disponible es un documento de marketing. Ambos resultados —uno rico, tres pobres— son útiles: el primero confirma que el método captura bien el riesgo cuando hay evidencia; los otros tres confirman que el método no puede compensar la ausencia de evidencia, y que ningún nivel de sofisticación en el Banco de Preguntas sustituye una sesión real con quien vivió el proyecto.

## 7. Evaluación honesta de calidad de datos por caso

| Caso | Calidad de datos disponible | Justificación |
| --- | --- | --- |
| Caso-01 | **Alta** | Memoria de cálculo con 4 revisiones, presupuesto desglosado por fase, catálogo fotográfico con 26 descripciones textuales de hallazgos reales, datos técnicos estructurados en `proyecto.json`. Es el único caso con evidencia de nivel E3 (evidencia operativa) en múltiples hallazgos |
| Caso-02 | **Pobre** | Solo el texto del CV comercial (unas 20 líneas). Sin presupuesto, cronograma, incidentes o testimonio. Explícitamente reconocido como pobre en `caso_02_centro_datos_i.md`, Sección 2 |
| Caso-03 | **Pobre** | Igual que el anterior; adicionalmente con una ambigüedad de alcance (proyecto ejecutivo vs. construcción) que el propio CV no aclara |
| Caso-04 | **Pobre, con matiz** | Texto del CV más específico técnicamente que los otros dos (menciona Uptime Institute, N+1, biométrico), pero sigue sin presupuesto, cronograma ni resultado. Es el "menos pobre de los pobres", no un caso de datos suficientes |

---

## 8. Ronda 2 (2026-07-16) — Caso-05, Caso-06 y corrección de encuadre CASO-07→Oficinas

Pablo pidió relanzar el pre-piloto usando dos proyectos adicionales con expediente rico (`CASO-05-PROY` y `CASO-06-PROY`, ambos localizados en `C:\Development\DataManager\proyectos\`, no en el repositorio PICC), y ampliar la cobertura a las categorías **casa habitación, oficinas y data centers**. Esta ronda agrega 3 casos nuevos (`caso_05_bodega_industrial.md`, `caso_06_nave_automotriz.md`, `caso_07_oficinas_comerciales.md`) y documenta explícitamente dos categorías que **no alcanzaron el umbral de calidad** para generar un caso nuevo (casa habitación, data centers).

### 8.1 Casos nuevos

| Caso | Fuente principal | Tipo de proyecto | Completitud del Banco lograda |
| --- | --- | --- | --- |
| Caso-05 (`caso_05_bodega_industrial.md`) | Expediente operativo completo — proyecto.json, Acta de Entrega-Recepción, 3 reportes de avance, estado de cuenta con bitácora WhatsApp, análisis de discrepancia de precios interno | Industrial — rehabilitación post-incendio, **obra concluida y entregada** | ~75% (18/24) |
| Caso-06 (`caso_06_nave_automotriz.md`) | Propuesta técnica preliminar + catálogo de fotos con análisis dron/sitio + índice de proyecto | Industrial/automotriz — remodelación de nave, **etapa preliminar, sin visita técnica interior** | ~58% (14/24) |
| Oficinas Caso-07 (`caso_07_oficinas_comerciales.md`) | Resumen de proyecto + catálogo de espacios + análisis de sobreprecios DEDALO | **Comercial — Oficinas** (reclasificado, ver 8.2) | ~42% (10/24) |

### 8.2 Hallazgo de encuadre — CASO-07-PROY no es un caso de "casa habitación"

El encargo original identificó `CASO-07-PROY` (indexado también bajo el nombre de carpeta `[CARPETA-INDICE-CASO-07]`) como candidato para la categoría "casa habitación". La lectura directa de la fuente contradice esa clasificación de forma inequívoca: `RESUMEN_PROYECTO.md` titula el proyecto "Caso-07 (Acondicionamiento Oficinas)" y `PROYECTO_INFO.json` declara `"tipo": "COMERCIAL - OFICINAS"`. El catálogo de espacios (`CATALOGO_ESPACIOS.md`) enumera exclusivamente programa de oficina (oficina de gerente, sala de juntas, recepción, área operativa con estaciones de trabajo, SITE) — cero espacios residenciales.

Este hallazgo se trata como una corrección de dato, no como un error del encargo: el nombre coloquial "[nombre coloquial de Caso-07]" usado en el índice ERP (`[CARPETA-INDICE-CASO-07]/HISTORIAL.md`) es engañoso porque el proyecto real detrás de ese nombre es un fit-out comercial. Se recomienda a Dirección PICC renombrar esa carpeta índice para evitar que el mismo error de clasificación se repita en el futuro (ver Sheet de Defectos, DEF-08).

**Consecuencia:** la categoría "oficinas", que el encargo original asumía sin expediente disponible (solo párrafos de currículum: [clientes de oficinas del currículum PICC, sin expediente dedicado] — ninguno con carpeta de proyecto dedicada localizada en `proyectos/`), queda **resuelta** con `caso_07_oficinas_comerciales.md`. La categoría "casa habitación" queda **sin resolver** (ver 8.3).

### 8.3 Categorías sin caso nuevo — gaps documentados explícitamente

#### Casa habitación — NO se generó caso nuevo

Se investigaron los tres candidatos señalados en el encargo:

- `CASO-07-PROY` / `[CARPETA-INDICE-CASO-07]`: reclasificado a Oficinas (ver 8.2), no es un caso residencial.
- `[CARPETA-CANDIDATO-CASA-HABITACION]` y `[PROY-CANDIDATO-CASA]`: se verificó que son **el mismo proyecto** indexado bajo dos nombres de carpeta distintos (mismos archivos, mismas fechas, mismo monto financiero de $350,000 registrado como "[FAMILIA-CANDIDATA-CASA] - Remodelacion integral"). El proyecto está marcado **❌ CANCELADO** en su índice ERP ("PROYECTO CANCELADO - No go. Confirmado por Pablo 2026-06-10"). Al inspeccionar el contenido físico disponible en el repositorio (`[PROY-CANDIDATO-CASA]/`), solo existen 1 fotografía (`IMG_9238.heic`, formato no procesado en este ejercicio) y el archivo índice `HISTORIAL.md` — los documentos de cotización de cocina, planos escaneados y levantamiento fotográfico que el índice lista **no están físicamente presentes en este repositorio** (probablemente residen en OneDrive, fuera del alcance de este ejercicio documental). No es posible responder con cita directa de fuente ninguna pregunta sustantiva del Banco más allá de la cronología y el monto cancelado.
- No se localizó ningún otro candidato: una búsqueda de carpetas con patrón `casa|resid|depto|departamento` en `proyectos/` solo devolvió las dos carpetas de [FAMILIA-CANDIDATA-CASA] ya evaluadas.

**Conclusión:** casa habitación permanece sin expediente rico disponible en este repositorio a la fecha de esta reconstrucción. No se fuerza un caso con datos insuficientes — se documenta el gap (ver DEF-09).

#### Data centers — NO se generó caso nuevo (no se repiten los 3 casos ya hechos en Ronda 1)

Se investigaron los candidatos señalados en el encargo:

- `[PROY-CANDIDATO-DESCARTADO]/RFQ_CONSOLIDADO_20260325.md`: es un proyecto de **sistemas de seguridad perimetral** (CCTV Avigilon, alarma Honeywell, iluminación solar, malla perimetral, planta de emergencia Tesla Powerwall, garitas) para **[CLIENTE-INSTITUCIONAL-DESCARTADO]** (Centro Internacional de Mejoramiento de Maíz y Trigo, instituto de investigación agrícola), explícitamente marcado en la propia fuente como *"INDEPENDIENTE del proyecto Aeropuerto [CLIENTE-A-MARCA]"*. No es un Data Center.
- Búsqueda de "HYPERION" (agente Director de Data Centers) en `output/`: todas las coincidencias son manifiestos de agentes y documentos de arquitectura del ecosistema ZEUS, ninguna es un expediente de proyecto real de cliente.
- Búsqueda de "data center" / "centro de datos" en `proyectos/`: no arrojó ninguna carpeta de proyecto dedicada más allá de las menciones ya usadas en los 3 casos pobres de la Ronda 1 (`contenido_cv.txt`).

**Conclusión:** no existe nuevo expediente de Data Center en este repositorio. Reconstruir un cuarto caso de Data Center con la misma fuente pobre (CV comercial) no aportaría información nueva — ya se documentó exhaustivamente en la Ronda 1 (DEF-04) que el techo de completitud con esa fuente es 12.5%-21%. Se documenta el gap sin duplicar trabajo ya hecho (ver DEF-09).

### 8.4 Tabla comparativa de calidad de datos — todos los casos (Ronda 1 + Ronda 2)

| Caso | Ronda | Categoría | Calidad de datos | % Banco respondible | Fuente principal | Hallazgo relevante |
| --- | --- | --- | --- | --- | --- | --- |
| Caso-01 | 1 | Comercial/industrial | **Alta** | ~62.5% (15/24) | Memoria de cálculo + presupuesto + catálogo fotográfico | Filtración activa ya materializada en taller; discrepancia interna de cifras (DEF-03) |
| Caso-05 | 2 | Industrial | **Muy alta** | ~75% (18/24) | Ciclo completo levantamiento→entrega+finanzas+WhatsApp | Robo de material en obra (AICM); dos discrepancias de precio distintas (DEF-06, DEF-07); cobranza pasiva documentada con impacto de flujo cuantificado |
| Caso-06 | 2 | Industrial/automotriz | **Media-alta** | ~58% (14/24) | Propuesta técnica preliminar + catálogo fotográfico dron | Dispersión de 19x entre escenarios de presupuesto sin alcance definido; mismo cliente que Caso-05 con posible atención dividida |
| Oficinas Caso-07 | 2 | Comercial — Oficinas | **Media** | ~42% (10/24) | Catálogo técnico + análisis de sobreprecios | Fuerte en alcance/presupuesto/riesgo técnico, vacío en contexto comercial (sin cliente identificado); proyecto congelado sin fecha de reactivación; discrepancia de área no reconciliada (DEF-08) |
| Caso-02 | 1 | Data Center | **Pobre** | ~17% (4/24) | Solo CV comercial | Techo de utilidad del método con fuente de marketing |
| Caso-03 | 1 | Data Center | **Pobre** | ~12.5% (3/24) | Solo CV comercial | Ambigüedad de alcance no aclarada por el CV |
| Caso-04 | 1 | Data Center | **Pobre, con matiz** | ~21% (5/24) | Solo CV comercial | Técnicamente más específico, sigue sin presupuesto/cronograma |
| *(Casa habitación)* | 2 | Casa habitación | **Sin caso** | No aplica | `[PROY-CANDIDATO-CASA]` insuficiente (proyecto cancelado, solo índice + 1 foto no procesada) | Gap documentado, no forzado (ver 8.3) |
| *(Oficinas — vía CV)* | — | Oficinas | **Sin caso vía CV** | No aplica | Resuelto por reclasificación de CASO-07 (ver 8.2), no por el currículum comercial | — |

### 8.5 Patrón transversal confirmado en Ronda 2

La Ronda 1 concluyó que el método (Banco de Preguntas + Reglas de Clasificación) no mostró defectos de diseño, y que el factor limitante es la fuente de datos. La Ronda 2 **confirma y matiza** esa conclusión con un patrón nuevo: la completitud del Banco no depende solo de "cuánta documentación existe", sino de **qué tipo** de documentación existe. Oficinas Caso-07 tiene abundante documentación técnica (catálogos, presupuestos, análisis de sobreprecios) pero completitud media (~42%) porque casi toda esa documentación responde a los Bloques B, C y D (alcance, presupuesto, riesgo técnico) y prácticamente nada a los Bloques A, F y G (contexto/urgencia, confianza institucional, siguiente paso) — bloques que solo un cliente real puede responder en sesión viva. Esto refuerza, con un mecanismo distinto al de la Ronda 1, la misma recomendación de Sección 5: ningún volumen de documentación técnica sustituye la sesión en vivo que exige DOC-062.

## 9. Ronda 3 (2026-07-16) — Caso-08 y Caso-09, evidencia de sistema DAVINCI y concentración de cliente

Pablo autorizó a ZEUS incorporar dos proyectos activos adicionales, reconstruidos por primera vez directamente desde el sistema DAVINCI (folios de `davinci.cotizaciones`, expediente de `davinci.expediente_items`, hitos de `davinci.hitos_cobro`) en vez de carpetas de proyecto sueltas, vía un reporte de consulta preparado por DEDALO. Esta ronda agrega 2 casos nuevos (`caso_08_nave_automotriz_ii.md`, `caso_09_nave_automotriz_iii.md`) y resuelve explícitamente una pregunta de identidad de cliente entre ambos proyectos y los de la Ronda 2.

### 9.1 Casos nuevos

| Caso | Fuente principal | Tipo de proyecto | Completitud del Banco lograda (cálculo propio de este ejercicio, 24 preguntas de referencia) |
| --- | --- | --- | --- |
| Caso-08 (`caso_08_nave_automotriz_ii.md`) | Reporte de consulta a sistema DAVINCI (folios, expediente, notas) | Industrial — nave para guardado de vehículos + oficinas, presupuesto en dos revisiones, la segunda sin aprobar | ~63% (15/24) |
| Caso-09 (`caso_09_nave_automotriz_iii.md`) | Reporte de consulta a sistema DAVINCI (folios, expediente, notas) | Industrial/comercial — remodelación de local existente a concesionario/showroom, presupuesto APROBADO con registro retroactivo | ~58% (14/24) |

### 9.2 Decisión de identidad de cliente — un caso confirma, un caso queda abierto

Esta ronda resolvió una pregunta de identidad de cliente entre los dos proyectos nuevos y el cliente ya codificado como `[CLIENTE-A]` en Caso-05 y Caso-06:

- **Caso-09 = mismo cliente que `[CLIENTE-A]`, confianza ALTA.** La decisión se apoyó en tres coincidencias documentadas en la fuente y en la clave de anonimización interna (no reproducidas en el repositorio PICC por regla de anonimización): coincidencia de ubicación (domicilio fiscal registrado de `[CLIENTE-A]`), coincidencia de marca comercial del proyecto, y coincidencia del mismo grupo comercial ya identificado en Caso-05/Caso-06. Se usó el código `[CLIENTE-A]` sin generar un código nuevo.
- **Caso-08 = entidad relacionada pero NO confirmada como la misma, confianza insuficiente para unificar.** El cliente registrado en el sistema DAVINCI para este proyecto tiene una razón social **distinta** a la de `[CLIENTE-A]`, con `[CLIENTE-A]` apareciendo en el expediente únicamente como **arrendatario** del inmueble (rol de inquilino, no de cliente contratante). Sin RFC de la razón social registrada como cliente de Caso-08 disponible para cruzar contra el RFC de `[CLIENTE-A]`, no hay evidencia suficiente para tratar ambas entidades como la misma persona moral, aunque ambas pertenecen al mismo grupo comercial. Se asignó un código nuevo, `[CLIENTE-B]`, verificando primero en la clave de anonimización que ninguna letra distinta de A estuviera ya reservada (solo `[CLIENTE-A]` existía antes de esta ronda). El caso documenta explícitamente esta duda como no resuelta, sin forzarla por inferencia débil.

### 9.3 Hallazgo de concentración de cliente

Con el cierre de esta ronda, `[CLIENTE-A]` tiene ahora **tres casos** en el pre-piloto (Caso-05, Caso-06, Caso-09) — el cliente con mayor presencia individual en todo el ejercicio (7 casos totales con expediente en Rondas 2 y 3, más los 4 casos pobres de Ronda 1) — más **un caso adicional de entidad relacionada pero no confirmada** del mismo grupo comercial (Caso-08, `[CLIENTE-B]`). Esto no es un hallazgo sobre el método RiskDiag en sí, sino una observación operativa relevante para Dirección PICC: casi la mitad de los casos con expediente rico de este pre-piloto (3 de 6, excluyendo los 4 casos pobres de currículum de Ronda 1) provienen del mismo grupo comercial, lo cual es consistente con la recomendación ya hecha en Caso-06 (Sección 5, punto 4) de dar seguimiento proactivo a la carga de trabajo compartida entre proyectos de un mismo cliente, y con la recomendación nueva de Caso-09 (Sección 5, punto 5) de evaluar formalmente la exposición de concentración de cliente antes de aceptar proyectos adicionales del mismo grupo.

### 9.4 Hallazgos de disciplina de evidencia — dos discrepancias de monto contractual

Esta ronda, igual que la Ronda 2 con Caso-05, encontró discrepancias de cifra dentro de la propia documentación interna de PICC, no en el proyecto del cliente:

1. **Caso-08:** escalada de alcance a mitad de cotización — dos revisiones del mismo folio el mismo día (09-Jul-2026), con incremento de +5.6% por condiciones de sitio no verificadas en uno de los dos predios, más un ajuste de partida posterior (16-Jul-2026) sin reconciliar contra el monto total (ver DEF-10).
2. **Caso-09:** discrepancia entre el monto registrado en sistema como APROBADO ($577,325 s/IVA) y el monto que la fuente cita textualmente como el contrato real confirmado directamente por Pablo ($602,105 s/IVA antes de un ajuste posterior) — con el agravante de que el registro en sistema fue retroactivo respecto a la aprobación real del cliente (ver DEF-11).

Ambos hallazgos siguen el mismo patrón ya visto en Caso-05 (DEF-07): el método RiskDiag no falla al capturarlos — al contrario, el Bloque C (presupuesto) y las Reglas de Clasificación (marcar la decisión de presupuesto como "no evaluable" cuando hay dos cifras sin reconciliar) funcionaron exactamente como fueron diseñados. El defecto es de disciplina documental interna de PICC, no del método.

### 9.5 Tabla comparativa de calidad de datos — todos los casos (Rondas 1+2+3)

| Caso | Ronda | Categoría | Calidad de datos | % Banco respondible | Fuente principal | Hallazgo relevante |
| --- | --- | --- | --- | --- | --- | --- |
| Caso-01 | 1 | Comercial/industrial | **Alta** | ~62.5% (15/24) | Memoria de cálculo + presupuesto + catálogo fotográfico | Filtración activa ya materializada en taller; discrepancia interna de cifras (DEF-03) |
| Caso-05 | 2 | Industrial | **Muy alta** | ~75% (18/24) | Ciclo completo levantamiento→entrega+finanzas+WhatsApp | Robo de material en obra; dos discrepancias de precio distintas (DEF-06, DEF-07); cobranza pasiva documentada con impacto de flujo cuantificado |
| Caso-06 | 2 | Industrial/automotriz | **Media-alta** | ~58% (14/24) | Propuesta técnica preliminar + catálogo fotográfico dron | Dispersión de 19x entre escenarios de presupuesto sin alcance definido; mismo cliente que Caso-05 con posible atención dividida |
| Oficinas Caso-07 | 2 | Comercial — Oficinas | **Media** | ~42% (10/24) | Catálogo técnico + análisis de sobreprecios | Fuerte en alcance/presupuesto/riesgo técnico, vacío en contexto comercial; discrepancia de área no reconciliada (DEF-08) |
| Caso-08 | 3 | Industrial (entidad relacionada, `[CLIENTE-B]`) | **Media-alta** | ~63% (15/24) | Reporte de consulta a sistema DAVINCI (folios, expediente) | Escalada de alcance entre dos revisiones de presupuesto el mismo día; identidad de cliente relacionada pero no confirmada (DEF-10) |
| Caso-09 | 3 | Industrial/comercial (`[CLIENTE-A]`) | **Media-alta** | ~58% (14/24) | Reporte de consulta a sistema DAVINCI (folios, expediente) | Discrepancia de monto contractual entre registro retroactivo y contrato confirmado directamente por Pablo (DEF-11); tercer caso del mismo cliente en el pre-piloto |
| Caso-02 | 1 | Data Center | **Pobre** | ~17% (4/24) | Solo CV comercial | Techo de utilidad del método con fuente de marketing |
| Caso-03 | 1 | Data Center | **Pobre** | ~12.5% (3/24) | Solo CV comercial | Ambigüedad de alcance no aclarada por el CV |
| Caso-04 | 1 | Data Center | **Pobre, con matiz** | ~21% (5/24) | Solo CV comercial | Técnicamente más específico, sigue sin presupuesto/cronograma |
| *(Casa habitación)* | 2 | Casa habitación | **Sin caso** | No aplica | Proyecto candidato cancelado, solo índice + 1 foto no procesada | Gap documentado, no forzado (ver 8.3) |
| *(Oficinas — vía CV)* | — | Oficinas | **Sin caso vía CV** | No aplica | Resuelto por reclasificación de CASO-07 (ver 8.2) | — |

### 9.6 Patrón transversal confirmado en Ronda 3

Los reportes de sistema DAVINCI (Caso-08, Caso-09) confirman un patrón distinto al de las carpetas de proyecto sueltas de Rondas 1 y 2: la completitud del Banco (~58-63%) es consistentemente media-alta cuando la fuente es un sistema transaccional estructurado (folios, hitos, expediente clasificado por tipo), porque ese tipo de fuente responde bien a los Bloques B y C (alcance, presupuesto) casi por diseño del propio sistema, pero sigue sin poder responder los Bloques A, F y G (contexto/urgencia, confianza institucional, siguiente paso) — el mismo techo estructural ya confirmado en la Ronda 2 con Oficinas Caso-07. Esto refuerza, con una tercera fuente de datos distinta (CV comercial en Ronda 1, expedientes documentales en Ronda 2, sistema DAVINCI en Ronda 3), la misma conclusión de Sección 5: ningún tipo de fuente documental, por estructurada que sea, sustituye la sesión en vivo que exige DOC-062.

