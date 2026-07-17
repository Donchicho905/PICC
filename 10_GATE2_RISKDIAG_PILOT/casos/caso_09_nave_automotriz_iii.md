# Caso Piloto — Caso-09 (Concesionario / Showroom Automotriz, mismo cliente que Caso-05/Caso-06)

**MODALIDAD: Pre-piloto retrospectivo, Ronda 3 (proyecto real activo con presupuesto aprobado, reconstruido desde expediente operativo DAVINCI — NO es sesión en vivo con cliente).**

Aclaración de modalidad: como Caso-08, este proyecto se reconstruyó desde el sistema DAVINCI (folios, hitos de cobro, expediente estructurado), no desde carpetas sueltas. A diferencia de Caso-08 (presupuesto en revisión, sin aprobar), este proyecto tiene presupuesto **APROBADO** por el cliente, con una particularidad relevante para la disciplina de evidencia interna de PICC: el registro en el sistema fue **retroactivo** respecto a la aprobación real del cliente, y el reporte fuente documenta una discrepancia de monto entre el registro retroactivo y el contrato confirmado directamente por Pablo Carducci.

## Fuentes de datos usadas (única fuente de verdad para este caso)

- Reporte técnico DEDALO, 16-Jul-2026 (`project_code: ZEUS-GATE2-EVIDENCIA-0001`, estado COMPLETADO) — Sección 2 (folios, hitos de cobro, expediente, documentos, notas DAVINCI) y Sección 4 (veredicto RiskDiag, fila izquierda de la tabla comparativa).
- Consulta original: `davinci.proyectos`, `davinci.cotizaciones`, `davinci.expediente_items`, `davinci.hitos_cobro` (vía réplica PG DEDALO), citadas en el reporte fuente.

## Nota de identidad de cliente — mismo cliente que Caso-05/Caso-06

El reporte fuente (Sección 2) registra este proyecto para el mismo grupo comercial de Caso-05 y Caso-06. La decisión de codificación, tomada por ZEUS antes de esta reconstrucción con confianza **ALTA**, es que este proyecto corresponde al mismo cliente formal `[CLIENTE-A]` ya usado en `caso_05_bodega_industrial.md` y `caso_06_nave_automotriz.md`, con base en tres coincidencias documentadas en el reporte fuente y en la clave de anonimización interna (no reproducidas aquí por regla de anonimización): coincidencia de ubicación (domicilio fiscal registrado de `[CLIENTE-A]`), coincidencia de marca comercial del proyecto, y coincidencia del grupo comercial ya identificado en Caso-05/Caso-06. Este caso usa el código `[CLIENTE-A]`, sin reabrir esa decisión.

**Consecuencia de encuadre (ver también Síntesis del Pre-piloto, Sección 9):** con este caso, `[CLIENTE-A]` acumula tres proyectos en el pre-piloto (Caso-05, Caso-06, Caso-09), más el proyecto de entidad relacionada pero no confirmada de Caso-08 (`[CLIENTE-B]`) — una concentración de cliente relevante para la lectura agregada del ejercicio.

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Caso-09 — Concesionario / Showroom Automotriz (remodelación de local existente) |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre expediente DAVINCI activo (Fase DISEÑO, folio único APROBADO 10-Jul-2026, ajuste de partida 16-Jul-2026) |
| Facilitador | No aplica — no hubo sesión en vivo. Reconstrucción documental por agente IA bajo autorización ZEUS |
| ICP hipotético (referencia interna) | ICP-H02 (Industrial e instalaciones críticas) — hipótesis del reconstructor; showroom/concesionario de marca con requisitos de imagen comercial e instalación eléctrica especializada (iluminación). No hay clasificación ICP formal registrada en las fuentes |
| Duración de la "sesión" | No aplica (modalidad retrospectiva) |

## 2. Resumen ejecutivo

El proyecto consiste en la remodelación de un local existente para un concesionario/showroom automotriz, para el cliente `[CLIENTE-A]` (mismo cliente de Caso-05 y Caso-06). El expediente DAVINCI documenta un folio único con estado **APROBADO** (10-Jul-2026, $577,325 s/IVA), pero el propio reporte fuente señala explícitamente que se trató de un **registro retroactivo** en el sistema: el catálogo de conceptos fue aprobado e impreso por el cliente el 03-Jul-2026, con folio "pre-sistema" (es decir, antes de que existiera el registro formal en DAVINCI). El monto registrado ($577,325 s/IVA) incluye ya un ajuste posterior del 16-Jul-2026 (dos minisplits de $24,890 c/u a $12,500 c/u). El hallazgo más relevante de este caso es que **el reporte fuente cita textualmente que el contrato real confirmado por Pablo el 10-Jul-2026 era de $602,105 s/IVA, antes del ajuste de minisplits** — una cifra distinta a la registrada en el sistema, sin que el expediente reconcilie ambos montos. El expediente incluye 161 ítems (79 fotografías, 70 notas), documentación técnica extensa de especialidades (clima, eléctrico, iluminación) y un plano de iluminación con 52 luminarias.

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| Discrepancia entre el monto registrado en el sistema DAVINCI como folio APROBADO ($577,325 s/IVA, ya con el ajuste de minisplits del 16-Jul) y el monto que el reporte fuente cita textualmente como "el contrato real confirmado por Pablo 10-Jul" ($602,105 s/IVA, antes del ajuste de minisplits) | C (presupuesto) | S3 — Riesgo alto (dos cifras de contrato distintas para el mismo folio, sin documento de reconciliación en el expediente; riesgo de que el monto cobrado al cliente no coincida con lo efectivamente contratado) | E3 — Evidencia operativa (reporte DEDALO, Sección 2, cita textual: *"El contrato real confirmado por Pablo 10-Jul era $602,105 s/IVA antes del ajuste de minisplits"*) | 4 (Qué presupuesto debo esperar), 13 (Su propuesta es comparable y económicamente defendible) | No evaluable — el expediente no aclara si la diferencia de aproximadamente $24,780 s/IVA corresponde solo al ajuste de minisplits documentado o si hay una brecha adicional sin explicar |
| Registro retroactivo del catálogo aprobado: el cliente aprobó e imprimió el catálogo el 03-Jul-2026 con un folio "pre-sistema", y el registro formal en DAVINCI ocurrió después, fechado 10-Jul-2026 | A (Contexto y urgencia) / C (presupuesto) | S2 — Riesgo medio (no es un riesgo del proyecto del cliente en sí, pero sí una brecha de disciplina de registro interno que puede generar ambigüedad sobre cuál documento es la versión contractual vigente) | E3 — Evidencia operativa (reporte DEDALO, Sección 2, nota explícita: "Registro retroactivo del catalogo aprobado por cliente (impreso 03-Jul con folio pre-sistema)") | 4 | No evaluable — mismo hallazgo que la fila anterior, comparten causa raíz |
| Programa arquitectónico definido solo parcialmente según el propio veredicto del reporte fuente (partidas de área techada y de seguridad perimetral documentadas, sin memoria de programa arquitectónico completa) | B (Alcance y definición técnica) | S2 — Riesgo medio (el alcance de obra civil está definido en partidas presupuestales, pero el reporte fuente clasifica explícitamente esta cobertura como "Parcial", no "Sí") | E2 — Evidencia parcial trazable (reporte DEDALO, Sección 4, tabla de veredicto: "Programa arquitectonico definido: Parcial (partidas...)" — clasificación del propio DEDALO, respetada sin sobre-optimizar) | 3 (Qué alcance necesito) | Parcialmente soportada — se respeta la clasificación "Parcial" ya asignada por la fuente |
| Datos del terreno/predio clasificados como "Parcial" por tratarse de remodelación de un local existente, sin diagnóstico estructural documentado del inmueble | D (Riesgo técnico y de ejecución) | S3 — Riesgo alto (remodelar sin diagnóstico estructural de un local existente puede descubrir condiciones no previstas durante la ejecución, el mismo patrón de riesgo materializado en Caso-08 con los predios de ese proyecto) | E2 — Evidencia parcial trazable (reporte DEDALO, Sección 4, tabla de veredicto: "Datos del terreno/predio: Parcial (local existente)"; Sección 4, cobertura estimada: "falta... diagnostico estructural del local") | 5 (Qué riesgos existen), 3 | No evaluable — el propio reporte fuente reconoce esta brecha sin resolverla |
| Contexto regulatorio clasificado como "Parcial" — trámites de rampa vehicular fueron investigados por un agente externo (22-Jun-2026), sin confirmación de estado de gestión posterior | E (regulatorio) | S2 — Riesgo medio (el trámite de rampa vehicular es relevante para la operación del showroom, con investigación hecha pero sin cierre documentado) | E2 — Evidencia parcial trazable (reporte DEDALO, Sección 2, nota: "Tramites rampa vehicular ... investigados por APOLO 22-Jun"; Sección 4, veredicto: "Contexto regulatorio: Parcial (tramites rampa)") | 5 | Parcialmente soportada |
| Ausencia total de referencia de competidor o de mercado — el propio veredicto del reporte fuente marca explícitamente "No" en este criterio, a diferencia de Caso-08 donde sí existe un documento de presupuesto de competidor | F (Institucional y confianza) | S1 — Riesgo bajo (no es un riesgo técnico ni financiero del proyecto, es una brecha de evidencia comercial) | E3 — Evidencia operativa de ausencia (reporte DEDALO, Sección 4, tabla de veredicto: fila "Referencia de competidor/mercado": "No" — clasificación explícita del propio DEDALO, respetada sin inferencia) | 6 (Vale la pena considerar a PICC), 13 | No evaluable — no hay dato para evaluar esta decisión en este caso |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Reconciliación entre el monto registrado en el sistema ($577,325 s/IVA) y el monto de contrato confirmado por Pablo ($602,105 s/IVA antes del ajuste de minisplits) — el reporte fuente cita ambas cifras sin explicar la diferencia completa | Ausencia de verificación | Confirmar con el catálogo físico impreso (03-Jul-2026, en poder de Pablo según el reporte fuente) cuál es el monto contractual real y corregir el registro en DAVINCI si corresponde | Dirección PICC / DEDALO (administración del sistema DAVINCI) |
| Diagnóstico estructural del local existente — no realizado o no documentado al momento del reporte fuente | Ausencia de dato | Programar visita técnica de diagnóstico estructural antes de iniciar obra de remodelación | PICC Ingeniería |
| Estado de gestión actual de los trámites de rampa vehicular — investigados 22-Jun-2026, sin actualización posterior en el reporte fuente (16-Jul-2026, más de 3 semanas después) | Ausencia de verificación | Confirmar con la autoridad correspondiente el estado del trámite | PICC / equipo de campo |
| Referencia de competidor o de mercado para este proyecto específico — a diferencia de Caso-08, no existe ningún documento de este tipo en el expediente | Ausencia de dato | No es indispensable para la ejecución técnica, pero cierra una brecha de posición comercial si el cliente comparó opciones sin que quede registrado | PICC Comercial |
| Estado final del giro completo del showroom (marca, exclusividad de exhibición, requisitos de imagen de marca del fabricante representado) — el expediente documenta especificaciones de diseño (colores, materiales) pero no el contrato de representación de marca en sí | Información no compartida / no definida en fuente | Pregunta directa al cliente sobre requisitos contractuales de marca aplicables al diseño | PICC Comercial / Cliente |

## 5. Recomendaciones priorizadas

1. Reconciliar de inmediato la discrepancia entre $577,325 s/IVA (registrado en sistema) y $602,105 s/IVA (contrato confirmado por Pablo) antes de emitir cualquier factura o hito de cobro sobre este folio — es el hallazgo de mayor severidad de este caso y afecta directamente la facturación.
2. Programar el diagnóstico estructural del local existente antes de iniciar obra, aplicando la misma lección que dejó la escalada de alcance de Caso-08: condiciones de sitio no verificadas generan retrabajo y ajustes de presupuesto a mitad de proceso.
3. Confirmar el estado actual de los trámites de rampa vehicular — investigados hace más de 3 semanas sin cierre documentado, mismo patrón de "dato viejo sin verificar" ya señalado en Caso-08.
4. Establecer, para proyectos con este mismo cliente (`[CLIENTE-A]`), un protocolo de registro de folio en el momento de la aprobación real del cliente, no de forma retroactiva — evitar que se repita la ambigüedad entre fecha de aprobación real y fecha de registro en sistema.
5. Dado que este es el tercer proyecto de `[CLIENTE-A]` en el pre-piloto (más un cuarto de entidad relacionada, Caso-08), evaluar formalmente en Dirección PICC la exposición de concentración de cliente antes de aceptar proyectos adicionales del mismo grupo comercial sin ajustar condiciones de pago o garantías.

## 6. Siguiente paso propuesto

- Siguiente paso concreto: reconciliar el monto de contrato ($577,325 vs. $602,105 s/IVA) contra el catálogo físico impreso el 03-Jul-2026, y corregir el registro DAVINCI si corresponde.
- Owner del siguiente paso: Dirección PICC (reconciliación de monto) + DEDALO (corrección de registro en sistema, si aplica).
- Plazo sugerido: `[DATO NO DISPONIBLE EN FUENTE]` — ninguna fuente consultada registra una fecha comprometida para esta reconciliación.

## 7. Límites del diagnóstico

> Este diagnóstico se basa en la información compartida durante la sesión del [no aplica — reconstrucción documental retrospectiva, no hubo sesión]. No sustituye una auditoría técnica, legal o financiera formal. Los hallazgos marcados como "no verificados" requieren confirmación antes de tomarse como base de decisión final.

Aclaración adicional: este caso se reconstruyó a partir de un reporte de consulta a base de datos (DEDALO, 16-Jul-2026), no del expediente físico completo ni del catálogo impreso mencionado en la fuente. Los montos, estados y fechas citados corresponden a lo registrado en `davinci.cotizaciones` y `davinci.expediente_items` a la fecha de esa consulta.

## 8. Firma / responsable

| Campo | Valor |
| --- | --- |
| Elaborado por | Agente IA (Claude, bajo autorización ZEUS/PICC), sesión 2026-07-16 |
| Revisado por | Pendiente — no revisado por Dirección PICC al momento de esta reconstrucción |
| Fecha de entrega al cliente | No aplica — este documento no se entrega al cliente. Es evidencia interna de pre-piloto |

---

## Banco de Preguntas — respuestas por pregunta (DOC-057), con cita de fuente

Fuente única para todas las respuestas: Reporte técnico DEDALO, 16-Jul-2026 (`ZEUS-GATE2-EVIDENCIA-0001`), Sección 2 salvo donde se indique Sección 4 (veredicto RiskDiag). Donde el propio reporte fuente ya clasificó una cobertura como "Parcial" o "No" en su tabla de veredicto (Sección 4), esa clasificación se respeta aquí sin sobre-optimizarla con inferencia adicional no citada.

| ID | Pregunta | Respuesta | Confianza | Cita de fuente |
| --- | --- | --- | --- | --- |
| A-01 | Problema/evento que hace relevante el proyecto ahora | No respondible | — | No hay dato en Sección 2 ni 4 |
| A-02 | Qué pasa si no avanza en 3-6 meses | No respondible | — | No hay dato en la fuente |
| A-03 | ¿Nuevo, ampliación o corrección? | Parcial — se infiere remodelación de local existente, no obra nueva | E2 | Sección 4, veredicto "Datos del terreno/predio: Parcial (local existente)" |
| A-04 | Fecha límite externa | No respondible | — | No hay dato en la fuente |
| A-05 | Quién más debe aprobar internamente | Parcial — el catálogo fue "aprobado por cliente" de forma genérica, sin nombrar cargo/rol específico más allá del contacto ya documentado en Caso-06 | E2 | Sección 2, "Registro retroactivo del catalogo aprobado por cliente" |
| B-01 | Alcance definido por escrito | Sí | E3 | Sección 2, tabla de documentos: catálogo de conceptos APROBADO, presupuesto v2, generadores de obra |
| B-02 | Quién definió el alcance y qué tan reciente | Sí | E3 | Sección 2, catálogo aprobado impreso 03-Jul-2026, folio registrado 10-Jul-2026 |
| B-03 | Continuidad operativa durante ejecución (condicional ICP-H02) | No respondible | — | No hay dato en la fuente |
| B-04 | Certificación/nivel de servicio específico (condicional ICP-H01) | No aplica — proyecto no es ICP-H01 | N/A | Regla de aplicabilidad DOC-057 |
| B-05 | Alcance depende de otras disciplinas no cerradas | Parcial | E2 | Sección 4, veredicto "falta... diagnostico estructural del local" |
| C-01 | Presupuesto aprobado o rango estimado | Sí | E3 | Sección 2, folio APROBADO $577,325 s/IVA (10-Jul-2026) |
| C-02 | Presupuesto confirmado o preliminar sin aprobación | Parcial — formalmente "APROBADO", pero el propio reporte documenta que el registro fue retroactivo y que existe una segunda cifra de contrato ($602,105) sin reconciliar | E2 | Sección 2, "Registro retroactivo..." y cita textual del contrato real confirmado por Pablo |
| C-03 | Quién controla la aprobación final del gasto | Parcial | E2 | Sección 2, "aprobado por cliente" (sin nombre/cargo específico) |
| C-04 | Otros proyectos compitiendo por el mismo presupuesto | No respondible en este reporte de forma aislada (el contexto cruzado de concentración de cliente se documenta como hallazgo de síntesis, no como respuesta directa a esta pregunta) | — | No hay dato en Sección 2 sobre este proyecto en particular |
| D-01 | Riesgo técnico que más preocupa | Parcial — inferido del veredicto de cobertura parcial en programa arquitectónico y datos de terreno, no una declaración directa del cliente | E2 | Sección 4, veredicto "Programa arquitectonico definido: Parcial", "Datos del terreno/predio: Parcial" |
| D-02 | Experiencias previas negativas con proveedores | No respondible | — | No hay dato en la fuente |
| D-03 | Riesgo de interrupción de operación durante ejecución (condicional) | No respondible | — | No hay dato en la fuente |
| D-04 | Condiciones de sitio no verificadas | Parcial | E2 | Sección 4, "Datos del terreno/predio: Parcial (local existente)"; Sección 4, cobertura estimada "falta... diagnostico estructural del local" |
| D-05 | Dependencias de terceros fuera del control del cliente | Parcial | E2 | Sección 2, trámites de rampa vehicular investigados por agente externo (dependencia de autoridad) |
| D-06 | Criticidad del tiempo de inactividad (condicional) | No respondible | — | No hay dato en la fuente |
| E-01 | Requiere permisos, licencias o autorizaciones | Sí | E3 | Sección 2, "Tramites rampa vehicular ... investigados" |
| E-02 | Permisos gestionados/en trámite/no iniciados | Parcial | E2 | Sección 2, investigados 22-Jun-2026 sin estado de gestión posterior documentado |
| E-03 | Requisito normativo sectorial aplicable | Parcial | E2 | Sección 4, veredicto "Contexto regulatorio: Parcial (tramites rampa)" |
| F-01 | Qué necesita ver el cliente para confiar | No respondible | — | No hay dato en la fuente |
| F-02 | Comparación con otros proveedores | No — el propio veredicto del reporte fuente marca explícitamente "No" en referencia de competidor/mercado para este proyecto | — (clasificación explícita de ausencia) | Sección 4, veredicto "Referencia de competidor/mercado: No" |
| F-03 | Qué haría descartar a un proveedor de inmediato | No respondible | — | No hay dato en la fuente |
| G-01 | Siguiente paso si el diagnóstico da claridad | No respondible | — | No hay dato en la fuente |
| G-02 | Quién más necesita ver el resultado | No respondible | — | No hay dato en la fuente |
| G-03 | Plazo esperado para tomar la decisión | No respondible | — | No hay dato en la fuente |

**Resumen:** de 28 preguntas aplicables (excluida B-04, condicional ICP-H01 no aplicable a este proyecto), 4 se respondieron con evidencia E3 ("Sí"), 10 con evidencia E2 ("Parcial"), 1 con clasificación explícita de ausencia heredada del veredicto DEDALO ("No" citado, F-02) y 13 quedaron sin dato ("No respondible"). Total respondible (Sí + Parcial) = 14 de 24, usando el mismo denominador de referencia empleado en Caso-01/05/06/07/08 (~58%).

---

## Hoja de Medición (DOC-060) — adaptada a modalidad retrospectiva

| # | Métrica | Valor en este caso | Nota de aplicabilidad |
| --- | --- | --- | --- |
| 1 | Tiempo de diagnóstico | NO APLICA — modalidad retrospectiva | No hubo sesión cronometrada |
| 2 | Completitud | 14 de 24 preguntas del Banco respondibles con cita directa de fuente (~58%), sobre 28 preguntas aplicables (ver tabla arriba) | Cálculo del reconstructor, más conservador que el estimado agregado del reporte fuente (~70% a nivel de 8 criterios de veredicto) porque exige cita directa por cada una de las 24 preguntas del banco, no una cobertura temática amplia |
| 3 | Claridad percibida | NO APLICA — modalidad retrospectiva | Requiere cliente real respondiendo en Fase 5 |
| 4 | Utilidad percibida | NO APLICA — modalidad retrospectiva | Ídem |
| 5 | Gaps identificados | 5 (ver Sección 4) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | Hipótesis del reconstructor: SÍ — la discrepancia de monto contractual debería resolverse antes de cualquier facturación sobre este folio, con la misma urgencia relativa que un hallazgo de severidad S3 en cualquier otro caso del pre-piloto | Inferencia marcada explícitamente como tal |
| 7 | Reducción de retrabajo | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 8 | Intención de compartir | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 9 | Intención de avanzar | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 10 | Decisión afectada | Decisión 4 (presupuesto) permanece "no evaluable" pese al folio formalmente APROBADO, porque el propio expediente documenta dos cifras de contrato distintas sin reconciliar | Evaluación del reconstructor sobre datos documentales |
| 11 | Señal comercial downstream | NO APLICA — modalidad retrospectiva | Requiere seguimiento real con cliente |
| 12 | Errores críticos | 1 (ver DEF-11 en Sheet de Defectos) — discrepancia de monto contractual entre el registro retroactivo en sistema y el contrato confirmado directamente por Pablo | Hallazgo de discrepancia documentado en la bitácora de defectos |
