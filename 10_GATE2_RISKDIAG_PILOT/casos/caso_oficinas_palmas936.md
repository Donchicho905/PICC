# Caso Piloto — Acondicionamiento de Oficinas Palmas 936

**MODALIDAD: Pre-piloto retrospectivo, Ronda 2 (proyecto real en etapa de análisis, reconstruido desde el expediente operativo — NO es sesión en vivo con cliente).**

## Corrección de encuadre — léase antes que el resto del documento

El encargo que originó esta reconstrucción identificó `PALMAS-2026-001` como candidato para la categoría **"casa habitación"**, agrupándolo junto con `Presupuesto_Casa_Las_Palmas` (el mismo proyecto, indexado con otro nombre de carpeta — ver más abajo) como posible expediente residencial. **Esto es incorrecto y se corrige aquí explícitamente, con evidencia directa de la fuente:**

- `RESUMEN_PROYECTO.md` (línea 1, título): *"RESUMEN PROYECTO PALMAS 936"*, con nombre de proyecto *"Acondicionamiento Oficinas PALMAS 936"* y tipo *"Remodelación - Oficinas Comerciales DE LUJO"*.
- `PROYECTO_INFO.json` (`proyecto.tipo`): *"COMERCIAL - OFICINAS"*.
- El catálogo de espacios (`CATALOGO_ESPACIOS.md`) enumera exclusivamente programas de oficina: "Oficina de Gerente", "Sala de Trabajo A/Oficina 1", "Sala de Juntas", "Recepción", "Área Operativa" (con estaciones de trabajo), "SITE (Servidor)", "Impresión", "Archivo Móvil" — cero espacios de vivienda (sin recámaras, sin cocina residencial, sin sala de estar familiar).

Este es un hallazgo relevante para la propia disciplina de captura de PICC/ZEUS: el proyecto fue etiquetado como candidato residencial en el encargo original probablemente por el nombre coloquial "Casa Las Palmas" usado en la carpeta índice `Presupuesto_Casa_Las_Palmas/HISTORIAL.md` (que apunta a los mismos archivos físicos que `PALMAS-2026-001/`, confirmado por fecha y tamaño de archivo idénticos en ambos índices) — pero el contenido real de esos archivos describe, sin ambigüedad, un fit-out de oficinas comerciales de lujo, no una casa. Se documenta esta discrepancia en la Sección 6 de `08_Sintesis_Prepiloto_Retrospectivo.md` y en el Sheet de Defectos (DOC-061).

**Consecuencia práctica:** este documento reclasifica el caso a la categoría **oficinas**, que el encargo original asumía sin expediente disponible más allá de párrafos de currículum (Kuehne+Nagel WTC, Pabellón Bosques, Rubén Darío, Oficinas Lago Iseo — ver Sección 6 de la síntesis). Esto **resuelve** la categoría de oficinas con un expediente real, y **deja abierta y sin resolver** la categoría de casa habitación (ver `08_Sintesis_Prepiloto_Retrospectivo.md`, Sección 8, para el detalle de por qué `OREA-2026-001` / `Remodelacion_Casa_Familia_Orea` no alcanza el umbral de calidad).

## Fuentes de datos usadas (única fuente de verdad para este caso)

- `C:\Development\DataManager\proyectos\PALMAS-2026-001\RESUMEN_PROYECTO.md`
- `C:\Development\DataManager\proyectos\PALMAS-2026-001\PROYECTO_INFO.json`
- `C:\Development\DataManager\proyectos\PALMAS-2026-001\CATALOGO_ESPACIOS.md`
- `C:\Development\DataManager\proyectos\PALMAS-2026-001\ANALISIS_SOBREPRECIOS_R17.md`
- Metadatos de `C:\Development\DataManager\proyectos\Presupuesto_Casa_Las_Palmas\HISTORIAL.md` (índice ERP, confirma que es el mismo proyecto, no uno adicional)

No se leyeron en este ejercicio (fuera del alcance de fuentes de texto priorizadas, y de tamaño/formato que exceden lo razonable para esta reconstrucción): `PRESUPUESTO_NEODATA.md` (49.2 KB, presupuesto detallado completo), los 12 archivos `COTIZACION_VYD_PALMAS*.xlsx` (versiones v2 a v12, formato Excel), `CATALOGO_INSTALACIONES.md`, `CATALOGO_MUROS_ACABADOS.md`, `CATALOGO_MOBILIARIO.md`, `PROYECTO_PCI.md`, `PROYECTO_CABLEADO_ESTRUCTURADO.md`, ni los entregables PDF/dashboard en `entregables/`. Su existencia se registra como evidencia adicional disponible pero no consumida, no como afirmación de su contenido.

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Acondicionamiento Oficinas Palmas 936 (PALMAS-2026-001) |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre datos capturados 27-Ene-2026 (documento inicial) y 18-Mar-2026 (análisis de sobreprecios, DEDALO) |
| Facilitador | No aplica — no hubo sesión en vivo |
| ICP hipotético (referencia interna) | Ninguno de H01 (Data Center) o H02 (Industrial) aplica con precisión — es un fit-out comercial de oficinas de lujo. Se trata como ICP genérico "Todos" para efectos de aplicabilidad del Banco de Preguntas |
| Duración de la "sesión" | No aplica |

## 2. Resumen ejecutivo

El proyecto es el acondicionamiento de ~145-200 m² (la propia fuente no reconcilia esta discrepancia — ver Sección 4) de oficinas comerciales de lujo en Palmas 936, CDMX, con especificación premium documentada (porcelanato rectificado, cristal templado, CCTV y control de acceso Hikvision, HVAC VRF). El expediente muestra un patrón distinto a los otros dos casos de esta ronda: **no hay evidencia de riesgo técnico de obra** (nunca se llegó a ejecutar), sino evidencia de **gobernanza de costos interna de PICC**: un análisis de sobreprecio generado por DEDALO (18-Mar-2026) identificó que la revisión de presupuesto R17 ($5,771,640) podía reducirse ~32% ($1,530,731 de ahorro potencial) mediante renegociación de proveedores, principalmente en mobiliario MillerKnoll (-59%, de $1,344,089 a $550,000). El propio análisis registra que el proyecto quedó **congelado por decisión del cliente/Pablo**: *"Estado: GUARDADO — Pablo dijo 'PALMAS LUEGO LA ANALIZAMOS'"*. Esto convierte al caso en un ejemplo útil y distinto: muestra cómo el Banco de Preguntas se comporta ante un proyecto que nunca llegó a la etapa de decisión de compra, con abundante evidencia técnica pero sin ninguna evidencia de intención o urgencia del comprador.

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| Sobreprecio de hasta 32% en la revisión de presupuesto R17 frente a precios de mercado, concentrado en mobiliario MillerKnoll (-59%) y HVAC VRF (-19%) | C (presupuesto) | S3 — Riesgo alto para la viabilidad del proyecto (un sobreprecio de esta magnitud puede ser motivo suficiente para que el cliente descarte o congele el proyecto, como de hecho ocurrió) | E3 — Evidencia operativa (`ANALISIS_SOBREPRECIOS_R17.md`, tabla completa por partida con precios de mercado comparados, ej. Herman Miller Aeron $803 USD documentado explícitamente) | 4 (Qué presupuesto debo esperar), 13 (Propuesta comparable y económicamente defendible) | Soportada — hay evidencia cuantificada y accionable |
| Discrepancia de área total del proyecto: `RESUMEN_PROYECTO.md` declara "~200 m² (pendiente verificar)" mientras que `PROYECTO_INFO.json` declara "145 m²" y `CATALOGO_ESPACIOS.md` calcula 147.31 m² por suma de espacios — tres cifras distintas para la misma superficie | B (Alcance y definición técnica) | S2 — Riesgo medio (una base de área inconsistente afecta directamente la precisión del presupuesto derivado) | E2 — Evidencia parcial trazable (los tres documentos existen y son consultables, la inconsistencia es verificable por lectura directa) | 3 (Qué alcance necesito), 4 | No evaluable — el propio expediente no resuelve cuál cifra es la vigente |
| Capacidad de carga de losa no verificada, condicionada a si el nivel es mezanine — marcado explícitamente "ALTA" prioridad de verificación en el propio resumen, especialmente relevante para el Archivo Móvil | D (Riesgo técnico y de ejecución) | S3 — Riesgo alto (si la losa no soporta la carga de archivo móvil, cambia el diseño estructural del entrepiso) | E1 — Señal aislada (mencionado como pendiente por el propio equipo de PICC, sin ninguna verificación estructural documentada) | 5 (Qué riesgos existen) | No evaluable |
| Ausencia total de nombre de cliente, contacto o interlocutor en cualquiera de las fuentes consultadas | A (Contexto y urgencia) | S1 — Riesgo bajo para el proyecto técnico, pero crítico para la trazabilidad comercial | E0 — No evidencia (ningún documento de los consultados nombra al cliente) | 1 (Debo actuar ahora), 12 (Defender la contratación ante otros) | No evaluable |
| Proyecto congelado sin fecha de reactivación ("GUARDADO — Pablo dijo 'PALMAS LUEGO LA ANALIZAMOS'") | A, G (Siguiente paso) | S2 — Riesgo medio (representa horas de ingeniería y análisis ya invertidas sin conversión a obra, un patrón de riesgo comercial más que técnico) | E3 — Evidencia operativa (la propia nota de estado en `ANALISIS_SOBREPRECIOS_R17.md` es una cita textual, no una inferencia) | 14 (Qué siguiente paso debo tomar) | Soportada (el estado "no evaluable qué sigue" está, en sí mismo, documentado con certeza) |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Reconciliación de las tres cifras de área total (200 m², 145 m², 147.31 m²) entre los tres documentos consultados | Ausencia de verificación | Levantamiento físico en sitio, ya identificado como pendiente crítico en el propio `RESUMEN_PROYECTO.md` | PICC / equipo de campo |
| Verificación de capacidad de carga de losa (si es mezanine) | Ausencia de dato | Estudio estructural en sitio | PICC Ingeniería / estructurista |
| Identidad del cliente y del interlocutor de decisión | Información no compartida / no definida en fuente | No se pudo inferir de ninguno de los documentos consultados en este ejercicio | Dirección PICC (fuera del alcance de este pre-piloto) |
| Estado actual del proyecto (¿sigue "guardado" a la fecha de esta reconstrucción, 2026-07-16, cuatro meses después de la nota del 18-Mar?) | Ausencia de verificación | Consultar a Pablo directamente sobre el estado vigente | ZEUS / Dirección PICC |
| Contenido de `PRESUPUESTO_NEODATA.md` y las 12 versiones de `COTIZACION_VYD_PALMAS*.xlsx` — no leídos en este ejercicio, podrían contener información adicional relevante para completar más preguntas del Banco | Ausencia de verificación (por alcance de este ejercicio, no por ausencia de la fuente) | Revisión dedicada de esos archivos en una iteración futura si el proyecto se reactiva | Quien retome el caso |

## 5. Recomendaciones priorizadas

1. Antes de reactivar el proyecto, reconciliar las tres cifras de área (200 / 145 / 147.31 m²) — es la base de cualquier presupuesto posterior y actualmente no hay una cifra única defendible.
2. Si el proyecto se reactiva, usar directamente el análisis de sobreprecios de DEDALO (`ANALISIS_SOBREPRECIOS_R17.md`) como punto de partida de renegociación antes de generar una nueva ronda de cotización desde cero — ya contiene comparables de mercado específicos y accionables.
3. Verificar la capacidad de carga de losa antes de comprometer cualquier diseño de archivo móvil o mobiliario pesado, dado que quedó marcada como pendiente de prioridad "ALTA" desde enero y no hay evidencia de que se haya resuelto.
4. Registrar formalmente en el ERP quién es el cliente/interlocutor de este proyecto — su ausencia total en el expediente es, en sí misma, un hallazgo de higiene de captura relevante para cualquier proyecto futuro similar.
5. Decidir explícitamente si el proyecto sigue vivo o se cierra formalmente como "en pausa indefinida" — la nota "GUARDADO" sin fecha de revisión es un estado ambiguo que ya lleva aproximadamente 4 meses sin actualización visible en el expediente consultado.

## 6. Siguiente paso propuesto

- Siguiente paso concreto: confirmar con Pablo si el proyecto sigue activo y, de ser así, retomar con el levantamiento físico pendiente antes de cualquier nueva ronda de cotización.
- Owner del siguiente paso: Pablo Carducci / Dirección PICC.
- Plazo sugerido: `[DATO NO DISPONIBLE EN FUENTE]` — ninguna fuente registra una fecha de revisión programada para el estado "GUARDADO".

## 7. Límites del diagnóstico

> Este diagnóstico se basa en la información compartida durante la sesión del [no aplica — reconstrucción documental retrospectiva, no hubo sesión]. No sustituye una auditoría técnica, legal o financiera formal. Los hallazgos marcados como "no verificados" requieren confirmación antes de tomarse como base de decisión final.

Aclaración adicional: este caso tiene una limitación distinta a los otros dos de esta ronda — no es que falte evidencia, es que la evidencia disponible es mayoritariamente técnica/de costos y prácticamente nula en lo comercial (sin cliente identificado, sin urgencia declarada, sin siguiente paso). Esto demuestra que el Banco de Preguntas puede tener alta completitud en los Bloques B, C y D (alcance, presupuesto, riesgo técnico) y aun así fallar estructuralmente en los Bloques A, F y G (contexto/urgencia, confianza institucional, siguiente paso) cuando la fuente es un expediente de ingeniería sin el correspondiente registro comercial.

## 8. Firma / responsable

| Campo | Valor |
| --- | --- |
| Elaborado por | Agente IA (Claude, bajo autorización ZEUS/PICC), sesión 2026-07-16 |
| Revisado por | Pendiente — no revisado por Dirección PICC al momento de esta reconstrucción |
| Fecha de entrega al cliente | No aplica — este documento no se entrega al cliente. Es evidencia interna de pre-piloto |

---

## Hoja de Medición (DOC-060) — adaptada a modalidad retrospectiva

| # | Métrica | Valor en este caso | Nota de aplicabilidad |
| --- | --- | --- | --- |
| 1 | Tiempo de diagnóstico | NO APLICA — modalidad retrospectiva | No hubo sesión cronometrada |
| 2 | Completitud | Aproximadamente 10 de 24 preguntas del Banco (DOC-057) respondibles con cita directa de fuente (~42%). Fuerte en Bloques B, C y D (alcance, presupuesto, riesgo técnico); prácticamente vacío en Bloques A, F y G (contexto/urgencia, confianza institucional, siguiente paso) | Cálculo aproximado del reconstructor. Es el más bajo de los tres casos de esta ronda, pero muy por encima de los casos basados solo en CV de la Ronda 1 (~12.5%-21%) |
| 3 | Claridad percibida | NO APLICA — modalidad retrospectiva | Requiere cliente real respondiendo en Fase 5 |
| 4 | Utilidad percibida | NO APLICA — modalidad retrospectiva | Ídem |
| 5 | Gaps identificados | 5 (ver sección 4) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | No aplica de forma significativa — el proyecto ya está en pausa por decisión explícita, no hay prioridad que cambiar sin una decisión externa de reactivación | Inferencia marcada explícitamente como tal |
| 7 | Reducción de retrabajo | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 8 | Intención de compartir | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 9 | Intención de avanzar | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 10 | Decisión afectada | Parcialmente — la decisión 4 (presupuesto) se movió de "no evaluable" a "soportada" gracias al análisis de sobreprecios ya existente; la decisión 1 (actuar ahora) permanece "no evaluable" porque no hay urgencia ni cliente documentados | Evaluación del reconstructor sobre datos documentales |
| 11 | Señal comercial downstream | NO APLICA — modalidad retrospectiva | Requiere seguimiento real con cliente |
| 12 | Errores críticos | 1 (ver DEF-08 en Sheet de Defectos, DOC-061) | Discrepancia de área total no reconciliada entre tres documentos del mismo proyecto, más el hallazgo de encuadre incorrecto documentado en la Sección "Corrección de encuadre" de este caso |
