# Caso Piloto — Caso-08 (Nave Industrial + Oficinas, entidad relacionada nueva)

**MODALIDAD: Pre-piloto retrospectivo, Ronda 3 (proyecto real activo en fase de diseño, reconstruido desde expediente operativo DAVINCI — NO es sesión en vivo con cliente).**

Aclaración de modalidad: a diferencia de Caso-05 (obra concluida) y Caso-06 (propuesta preliminar sin presupuesto contratado), este proyecto está en una etapa intermedia: **ACTIVO, Fase DISEÑO**, con presupuesto formal ya emitido y en dos revisiones sucesivas, la segunda de ellas "en espera de cliente". Es el primer caso del pre-piloto reconstruido directamente desde el sistema DAVINCI (folios, hitos de cobro y expediente estructurado en base de datos), no desde carpetas de proyecto sueltas.

## Fuentes de datos usadas (única fuente de verdad para este caso)

- Reporte técnico DEDALO, 16-Jul-2026 (`project_code: ZEUS-GATE2-EVIDENCIA-0001`, estado COMPLETADO) — Sección 1 (folios, hitos de cobro, expediente, documentos, notas DAVINCI) y Sección 4 (veredicto RiskDiag, fila derecha de la tabla comparativa).
- Consulta original: `davinci.proyectos`, `davinci.cotizaciones`, `davinci.expediente_items`, `davinci.hitos_cobro` (vía réplica PG DEDALO), citadas en el reporte fuente.

## Nota de identidad de cliente — entidad relacionada pero NO confirmada como la misma

El proyecto de este caso está registrado en el sistema DAVINCI bajo un cliente cuya **razón social es distinta** a la del cliente formal de Caso-05/Caso-06 (`[CLIENTE-A]`). El reporte fuente (Sección 1) identifica al cliente registrado como una comercializadora vehicular con razón social propia, y señala que la entidad de `[CLIENTE-A]` aparece en este expediente únicamente como **arrendatario** (rol de inquilino del inmueble en construcción), no como cliente contratante.

Ambas entidades pertenecen al mismo grupo comercial que también aparece en Caso-05 y Caso-06, y el proyecto de este caso comparte el mismo interlocutor operativo (Pablo Carducci, vía PICC/Bandejas Fodder). Sin embargo, **no hay RFC de la razón social registrada como cliente de este proyecto disponible para cruzar contra el RFC de `[CLIENTE-A]`** (ver `PICC_CLAVE_ANONIMIZACION_CONFIDENCIAL.md` para el detalle no anonimizado de ambos RFC). Por lo tanto, siguiendo la misma disciplina de evidencia aplicada en Caso-05/Caso-06 (no inferir identidad sin dato verificable), este caso se trata como una **entidad distinta y nueva**: `[CLIENTE-B]`.

**Se documenta explícitamente:** `[CLIENTE-B]` está relacionado con `[CLIENTE-A]` (mismo grupo comercial, y `[CLIENTE-A]` aparece como arrendatario del inmueble de este proyecto), pero **no está confirmado como la misma entidad legal** — es una duda documentada, no resuelta por inferencia débil. Esta decisión de codificación fue tomada por ZEUS antes de la ejecución de este caso y no se reabre en esta reconstrucción.

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Caso-08 — Nave Industrial (guardado de vehículos) + Oficinas |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre expediente DAVINCI activo (Fase DISEÑO, revisión de presupuesto más reciente 09-Jul-2026, ajuste de partida 16-Jul-2026) |
| Facilitador | No aplica — no hubo sesión en vivo. Reconstrucción documental por agente IA bajo autorización ZEUS |
| ICP hipotético (referencia interna) | ICP-H02 (Industrial e instalaciones críticas) — hipótesis del reconstructor; nave industrial + oficinas con arrendatario operador de flotilla vehicular. No hay clasificación ICP formal registrada en las fuentes |
| Duración de la "sesión" | No aplica (modalidad retrospectiva) |

## 2. Resumen ejecutivo

El proyecto consiste en una nave industrial para guardado de vehículos más oficinas, sobre dos predios catastrales (766 m² combinados), para un cliente (`[CLIENTE-B]`) cuya razón social es distinta a la del cliente de Caso-05/Caso-06 pero pertenece al mismo grupo comercial. El expediente DAVINCI documenta un ciclo de cotización con **escalada de alcance a mitad de proceso**: una primera revisión de presupuesto fue sustituida por una segunda, con incremento de monto, después de que el segundo de los dos predios resultó tener condiciones de sitio no verificadas al momento de la primera revisión (un cuarto, techumbre y estructura/cimentación que faltaban y no estaban contempladas). El expediente incluye 70 ítems registrados (fotografías, notas, otros documentos y un render), documentación regulatoria municipal, memoria de cálculo estructural, y una referencia de presupuesto de un competidor. La segunda revisión de presupuesto está en estado "enviada, en espera de cliente" — el proyecto no tiene aún presupuesto aprobado por el cliente al momento de esta reconstrucción.

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| Escalada de alcance entre dos revisiones de presupuesto del mismo folio: Revisión A ("SUSTITUIDA", $1,149,926 s/IVA) reemplazada por Revisión B ("ENVIADA — en espera de cliente", $1,213,824 s/IVA), ambas fechadas 09-Jul-2026, por hallazgos de condiciones de sitio no documentadas en uno de los dos predios (cuarto, techumbre sencilla para 2 autos, estructura y cimentación faltantes) | D (Riesgo técnico y de ejecución) | S3 — Riesgo alto (incremento de monto de +5.6% entre dos revisiones el mismo día, sobre un presupuesto todavía no aprobado por el cliente; señal de que el levantamiento inicial no capturó el alcance real de uno de los dos predios) | E3 — Evidencia operativa (reporte DEDALO, Sección 1, tabla "Folios DAVINCI" con ambos montos, estados y fecha; motivo de Revisión B citado explícitamente) | 3 (Qué alcance necesito), 4 (Qué presupuesto debo esperar) | No evaluable — la Revisión B está "en espera de cliente", por lo que la decisión de presupuesto del cliente para este proyecto sigue abierta al momento de esta reconstrucción |
| Ajuste posterior de partida dentro de la misma Revisión B: minisplit ajustado de $25,000 a $12,500 el 16-Jul-2026, una semana después de emitida la revisión | C (presupuesto) | S2 — Riesgo medio (cambio de precio unitario del -50% en una partida específica, después de enviada la cotización al cliente, sin que el expediente aclare si el monto total de $1,213,824 ya refleja este ajuste) | E2 — Evidencia parcial trazable (reporte DEDALO, Sección 1, nota "16-Jul: ajuste minisplit $25,000 a $12,500", sin cifra de monto total post-ajuste) | 4, 13 (Su propuesta es comparable y económicamente defendible) | No evaluable — el expediente no aclara si el monto de $1,213,824 s/IVA ya incorpora este ajuste o si el monto final es distinto |
| Pendientes regulatorios y legales abiertos al 23-Jun-2026 (escrituras de los dos predios, Director Responsable de Obra, estudio de suelos) sin actualización posterior documentada en el reporte fuente (16-Jul-2026) | E (regulatorio) | S3 — Riesgo alto (escrituras y DRO son condición habilitante para iniciar obra formalmente; sin actualización en 3+ semanas desde la última nota registrada) | E2 — Evidencia parcial trazable (reporte DEDALO, Sección 1, "Notas DAVINCI clave registradas": "Pendientes abiertos al 23-Jun: escrituras predios, DRO, estudio suelos" — dato con antigüedad de más de 3 semanas respecto a la fecha del reporte) | 5 (Qué riesgos existen), 3 | Parcialmente soportada — hay evidencia de que el pendiente existe, no hay evidencia de su estado actual |
| Discrepancia de superficie entre el predio catastral (766 m², suma de dos predios de 583.07 m² y 183.05 m²) y una medición de campo mencionada como descartada (1,408 m²) | B (alcance) | S2 — Riesgo medio (una diferencia de casi el doble entre dos mediciones del mismo terreno, aunque el expediente confirma cuál de las dos se usó como base de diseño) | E3 — Evidencia operativa (reporte DEDALO, Sección 1, nota: "Area = 766 m2 catastral... El campo (1,408 m2) fue descartado por Pablo") | 3 | Soportada — el expediente documenta explícitamente cuál medición se adoptó y por qué se descartó la otra, aunque no explica la causa de la diferencia original |
| Referencia a presupuesto de un competidor conservada en el expediente como documento de comparación | F (institucional y confianza) | S1 — Riesgo bajo para la ejecución del proyecto, mayor relevancia para la posición comercial de PICC frente al cliente | E3 — Evidencia operativa (reporte DEDALO, Sección 1, tabla de documentos: "DOC ... Presupuesto del Competidor (referencia)", archivo `.docx` en el expediente) | 6 (Vale la pena considerar a PICC), 13 | Soportada como hecho de expediente (existe el documento); no evaluable sobre si el cliente decidió con base en esa comparación |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Estado actual de escrituras de los dos predios, Director Responsable de Obra y estudio de suelos — última actualización documentada es de 23-Jun-2026, más de tres semanas antes de la fecha del reporte fuente | Ausencia de verificación | Actualizar el expediente DAVINCI con el estado vigente de cada pendiente | Dirección PICC / equipo de campo del proyecto |
| Respuesta del cliente a la Revisión B del presupuesto ($1,213,824 s/IVA), en estado "enviada, en espera de cliente" al momento del reporte fuente | Ausencia de definición | Seguimiento comercial directo con el cliente para obtener aprobación o retroalimentación | PICC Comercial |
| Monto final de la Revisión B tras el ajuste de partida de minisplit (16-Jul-2026) — el reporte fuente no aclara si $1,213,824 s/IVA ya incorpora el ajuste o si existe un monto posterior no reflejado en la tabla de folios | Ausencia de dato | Verificar en el JSON vivo de presupuesto (ruta interna del reporte fuente, no reproducida aquí por regla de anonimización) cuál es el monto vigente | PICC Ingeniería / DEDALO |
| Identidad legal exacta de `[CLIENTE-B]` respecto a `[CLIENTE-A]` — sin RFC de la razón social registrada como cliente de este proyecto disponible para comparar contra el RFC de `[CLIENTE-A]` | Información no compartida / no definida en fuente | Obtener RFC de la razón social cliente de este proyecto y cruzarlo contra el RFC de `[CLIENTE-A]` ya conocido | Dirección PICC / Administración |
| Motivo de negocio detrás del uso del inmueble como arrendamiento a `[CLIENTE-A]` en vez de operación directa del cliente contratante | Ausencia de dato | Pregunta directa al cliente sobre el modelo de negocio del inmueble | PICC Comercial |

## 5. Recomendaciones priorizadas

1. No presentar la Revisión B como presupuesto final hasta confirmar si el ajuste de minisplit del 16-Jul-2026 ya está reflejado en el monto de $1,213,824 s/IVA — un cliente que reciba una cifra desactualizada en cualquier dirección (de más o de menos) puede interpretar el cambio como falta de control interno.
2. Actualizar de inmediato el estado de escrituras, DRO y estudio de suelos — son condición habilitante para iniciar obra y llevan más de tres semanas sin actualización documentada, el mismo patrón de "dato viejo sin verificar" identificado como riesgo repetible en otros casos del pre-piloto (ver Caso-06, brecha de superficie/estado estructural).
3. Documentar formalmente, antes de que se repita, el protocolo de levantamiento que permitió que el segundo predio llegara a Revisión A sin capturar el cuarto, techumbre y estructura/cimentación faltantes — evitar que la escalada de alcance de este caso se convierta en un patrón repetido en otros proyectos con múltiples predios.
4. Verificar y documentar formalmente el RFC de la razón social cliente de este proyecto para cerrar, con evidencia y no con inferencia, la pregunta de si `[CLIENTE-B]` es o no la misma entidad legal que `[CLIENTE-A]` — relevante para la exposición de riesgo comercial concentrado del mismo grupo (ver Síntesis del Pre-piloto, Sección 9).
5. Dar seguimiento comercial activo a la Revisión B "en espera de cliente" — sin este seguimiento, el proyecto puede quedar indefinidamente en un estado de presupuesto no aprobado sin que quede registrado por qué.

## 6. Siguiente paso propuesto

- Siguiente paso concreto: obtener respuesta del cliente a la Revisión B del presupuesto y actualizar el estado de los tres pendientes regulatorios/legales (escrituras, DRO, estudio de suelos).
- Owner del siguiente paso: PICC Comercial (seguimiento de Revisión B) + PICC Ingeniería/Dirección (actualización de pendientes regulatorios).
- Plazo sugerido: `[DATO NO DISPONIBLE EN FUENTE]` — ninguna fuente consultada registra una fecha comprometida para el cierre de estos pendientes.

## 7. Límites del diagnóstico

> Este diagnóstico se basa en la información compartida durante la sesión del [no aplica — reconstrucción documental retrospectiva, no hubo sesión]. No sustituye una auditoría técnica, legal o financiera formal. Los hallazgos marcados como "no verificados" requieren confirmación antes de tomarse como base de decisión final.

Aclaración adicional: este caso se reconstruyó a partir de un reporte de consulta a base de datos (DEDALO, 16-Jul-2026), no del expediente físico completo. Los montos, estados y fechas citados corresponden a lo registrado en `davinci.cotizaciones` y `davinci.expediente_items` a la fecha de esa consulta; cualquier actualización posterior del proyecto no está reflejada aquí.

## 8. Firma / responsable

| Campo | Valor |
| --- | --- |
| Elaborado por | Agente IA (Claude, bajo autorización ZEUS/PICC), sesión 2026-07-16 |
| Revisado por | Pendiente — no revisado por Dirección PICC al momento de esta reconstrucción |
| Fecha de entrega al cliente | No aplica — este documento no se entrega al cliente. Es evidencia interna de pre-piloto |

---

## Banco de Preguntas — respuestas por pregunta (DOC-057), con cita de fuente

Fuente única para todas las respuestas: Reporte técnico DEDALO, 16-Jul-2026 (`ZEUS-GATE2-EVIDENCIA-0001`), Sección 1 salvo donde se indique Sección 4 (veredicto RiskDiag). Clasificación de confianza según DOC-058 Sección 3.

| ID | Pregunta | Respuesta | Confianza | Cita de fuente |
| --- | --- | --- | --- | --- |
| A-01 | Problema/evento que hace relevante el proyecto ahora | No respondible — el reporte no documenta un evento disparador explícito | — | No hay dato en Sección 1 ni 4 |
| A-02 | Qué pasa si no avanza en 3-6 meses | No respondible | — | No hay dato en la fuente |
| A-03 | ¿Nuevo, ampliación o corrección? | Parcial — se infiere obra nueva (nave + oficinas) sobre predios sin construcción previa documentada | E2 | Sección 1, "Nombre completo: ... Nave Industrial (guardado autos) + Oficinas"; Fase DISEÑO |
| A-04 | Fecha límite externa | No respondible | — | No hay dato en la fuente |
| A-05 | Quién más debe aprobar internamente | Parcial — el proceso de aprobación pasa por "el cliente" de forma genérica, sin nombrar a la persona o cargo específico | E2 | Sección 1, tabla de folios, estado "ENVIADA — en espera de cliente" |
| B-01 | Alcance definido por escrito | Sí | E3 | Sección 1, tabla de documentos: catálogo de conceptos v2 (766 m², 38 partidas), presupuesto v3, generadores de obra (41 conceptos) |
| B-02 | Quién definió el alcance y qué tan reciente | Sí | E3 | Sección 1, folios fechados 09-Jul-2026 (Rev A y B) y ajuste 16-Jul-2026 |
| B-03 | Continuidad operativa durante ejecución (condicional ICP-H02) | No respondible — brecha, no dato disponible | — | No hay dato en la fuente |
| B-04 | Certificación/nivel de servicio específico (condicional ICP-H01) | No aplica — proyecto no es ICP-H01 | N/A | Regla de aplicabilidad DOC-057 |
| B-05 | Alcance depende de otras disciplinas no cerradas | Sí | E3 | Sección 1, "Pendientes abiertos al 23-Jun: escrituras predios, DRO, estudio suelos" |
| C-01 | Presupuesto aprobado o rango estimado | Sí | E3 | Sección 1, tabla de folios: $1,149,926 (Rev A) y $1,213,824 (Rev B) s/IVA |
| C-02 | Presupuesto confirmado o preliminar sin aprobación | Sí | E3 | Sección 1, estado Rev B: "ENVIADA — en espera de cliente" |
| C-03 | Quién controla la aprobación final del gasto | Parcial | E2 | Sección 1, estado "en espera de cliente" (sin nombrar aprobador específico) |
| C-04 | Otros proyectos compitiendo por el mismo presupuesto | No respondible | — | No hay dato en la fuente sobre este proyecto de forma aislada |
| D-01 | Riesgo técnico que más preocupa | Sí | E3 | Sección 1, "Motivo Rev B: Predio B simplificado (cuarto... techumbre... estructura/cimentacion B que faltaban)" |
| D-02 | Experiencias previas negativas con proveedores | No respondible | — | No hay dato en la fuente |
| D-03 | Riesgo de interrupción de operación durante ejecución (condicional) | No respondible | — | No hay dato en la fuente |
| D-04 | Condiciones de sitio no verificadas | Sí | E3 | Sección 1, motivo de Rev B (mismo dato que D-01, hallazgo central de este caso) |
| D-05 | Dependencias de terceros fuera del control del cliente | Sí | E3 | Sección 1, pendientes de escrituras/DRO/estudio de suelos (mismo dato que B-05) |
| D-06 | Criticidad del tiempo de inactividad (condicional) | No respondible | — | No hay dato en la fuente |
| E-01 | Requiere permisos, licencias o autorizaciones | Sí | E3 | Sección 1, documentos "Plan tramites y restricciones" y "Brief DRO" |
| E-02 | Permisos gestionados/en trámite/no iniciados | Parcial | E2 | Sección 1, "Pendientes abiertos al 23-Jun" sin actualización posterior a la fecha del reporte |
| E-03 | Requisito normativo sectorial aplicable | Sí | E3 | Sección 1, documento "Investigacion regulatoria [municipal]" |
| F-01 | Qué necesita ver el cliente para confiar | No respondible | — | No hay dato en la fuente |
| F-02 | Comparación con otros proveedores | Sí | E3 | Sección 1, documento "Presupuesto del Competidor (referencia)" |
| F-03 | Qué haría descartar a un proveedor de inmediato | No respondible | — | No hay dato en la fuente |
| G-01 | Siguiente paso si el diagnóstico da claridad | No respondible | — | No hay dato en la fuente |
| G-02 | Quién más necesita ver el resultado | No respondible | — | No hay dato en la fuente |
| G-03 | Plazo esperado para tomar la decisión | No respondible | — | No hay dato en la fuente |

**Resumen:** de 28 preguntas aplicables (excluida B-04, condicional ICP-H01 no aplicable a este proyecto), 11 se respondieron con evidencia E3 ("Sí"), 4 con evidencia E2 ("Parcial") y 13 quedaron sin dato ("No respondible"). Total respondible (Sí + Parcial) = 15 de 24, usando el mismo denominador de referencia empleado en Caso-01/05/06/07 (~63%).

---

## Hoja de Medición (DOC-060) — adaptada a modalidad retrospectiva

| # | Métrica | Valor en este caso | Nota de aplicabilidad |
| --- | --- | --- | --- |
| 1 | Tiempo de diagnóstico | NO APLICA — modalidad retrospectiva | No hubo sesión cronometrada |
| 2 | Completitud | 15 de 24 preguntas del Banco respondibles con cita directa de fuente (~63%), sobre 28 preguntas aplicables (ver tabla arriba) | Cálculo del reconstructor, aplicando las Reglas de Clasificación de forma estricta pregunta por pregunta, no el estimado agregado del reporte fuente (que reportaba ~80% a nivel de 8 criterios de veredicto, no de las 24 preguntas del banco) |
| 3 | Claridad percibida | NO APLICA — modalidad retrospectiva | Requiere cliente real respondiendo en Fase 5 |
| 4 | Utilidad percibida | NO APLICA — modalidad retrospectiva | Ídem |
| 5 | Gaps identificados | 5 (ver Sección 4) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | Hipótesis del reconstructor: SÍ — la escalada de alcance entre Rev A y Rev B debería tratarse como una señal de proceso a corregir en el protocolo de levantamiento de múltiples predios, no solo como un hallazgo aislado de este caso | Inferencia marcada explícitamente como tal |
| 7 | Reducción de retrabajo | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 8 | Intención de compartir | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 9 | Intención de avanzar | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 10 | Decisión afectada | Decisiones 3 y 4 permanecen "no evaluable" — el proyecto no tiene aún presupuesto aprobado por el cliente al momento de esta reconstrucción | Evaluación del reconstructor sobre datos documentales |
| 11 | Señal comercial downstream | NO APLICA — modalidad retrospectiva | Requiere seguimiento real con cliente |
| 12 | Errores críticos | 1 (ver DEF-10 en Sheet de Defectos) — la escalada de alcance entre Rev A y Rev B, con ajuste posterior de partida no reconciliado con el monto total | Hallazgo de discrepancia documentado en la bitácora de defectos |
