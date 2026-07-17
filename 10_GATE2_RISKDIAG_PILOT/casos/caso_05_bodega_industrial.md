# Caso Piloto — Caso-05 (Rehabilitación de Cubierta Post-Incendio)

**MODALIDAD: Pre-piloto retrospectivo, Ronda 2 (proyecto ya ejecutado y entregado, reconstruido desde el expediente operativo real de PICC — NO es sesión en vivo con cliente).**

Aclaración de modalidad: a diferencia de los 4 casos de la Ronda 1 (2026-07-16, primera tanda), este proyecto está **100% concluido y entregado** (Acta de Entrega-Recepción firmada 17-Abr-2026, avance físico final 100%). Esto lo distingue de Caso-01 (que seguía en etapa de cotización) y permite reconstruir el ciclo completo: levantamiento → cotización → discrepancia interna de precios → ejecución → incidente en obra → cobranza → cierre. Es el caso con el ciclo de vida más completo disponible en el repositorio de PICC a la fecha de esta reconstrucción.

## Fuentes de datos usadas (única fuente de verdad para este caso)

- `C:\Development\DataManager\proyectos\CASO-05-PROY\proyecto.json`
- `C:\Development\DataManager\proyectos\CASO-05-PROY\HISTORIAL.md`
- `C:\Development\DataManager\proyectos\CASO-05-PROY\10_REPORTES\ACTA_ENTREGA_RECEPCION_CASO05_20260417.md`
- `C:\Development\DataManager\proyectos\CASO-05-PROY\10_REPORTES\REPORTE_AVANCE_03_20260318.md`
- `C:\Development\DataManager\proyectos\CASO-05-PROY\09_FINANZAS\ESTADO_CUENTA.md`
- `C:\Development\DataManager\proyectos\CASO-05-PROY\archivo_historico\ANALISIS_DIFERENCIAS.md`
- `C:\Development\DataManager\proyectos\CASO-05-COT-TEMPRANA\cotizacion_temprana_caso05.pdf` (presupuesto detallado por partidas, 21-Feb-2026 — ver Sección 4, discrepancia de fuente)
- `C:\Development\DataManager\proyectos\CASO-05-PROY\07_FOTOS_AVANCE\` (nombres de archivo con fecha y descripción de las 5 subcarpetas: `01_ESTRUCTURA`, `02_INSTALACIONES`, `03_ACABADOS`, `04_GENERAL`, `05_INCIDENTE_AICM`) — solo se usaron nombres de archivo con fecha y descripción textual, nunca se interpretó contenido visual no descrito en el nombre o en un documento asociado

**Nota de trazabilidad crítica — hallazgo de esta reconstrucción:** el proyecto **CASO-06-PROY** (ver `caso_06_nave_automotriz.md`) y este proyecto comparten el mismo cliente (**[CLIENTE-A]**, contacto Rafael Chapa H.). Además, el Acta de Entrega-Recepción de este proyecto (Sección II) identifica al cliente formal como **[CLIENTE-A] (razón social), marca comercial [CLIENTE-A-MARCA]** (alquiler de automóviles sin chofer, RFC [omitido], con domicilio fiscal en [ciudad omitida]). Esto **NO es el mismo proyecto** que "[PROYECTO-HOMONIMO-CANCELADO]", declarado **CANCELADO** en la memoria del sistema ZEUS (corrección Pablo, 22-Jun-2026). Son dos entidades homónimas distintas:
1. **[CLIENTE-A-MARCA] (marca comercial de [CLIENTE-A] (razón social))** — cliente de [CLIENTE-A], renta de autos sin chofer, es el cliente que firma el Acta de este proyecto (Caso-05).
2. **[PROYECTO-HOMONIMO-CANCELADO]** — un proyecto de infraestructura distinto y ya cancelado, mencionado en `CASO-06-PROY/04_ENTREGABLES/PROPUESTA_PRELIMINAR_CASO06_20260318.md` como antecedente de relación comercial con el mismo [CLIENTE-A] ("Rafael Chapa y [CLIENTE-A] conocen la capacidad de PICC a través del proyecto [PROYECTO-HOMONIMO-CANCELADO]").

Se documenta esta distinción explícitamente porque la carpeta `CASO-05-COT-TEMPRANA` (nombre parecido a "[CLIENTE-A-MARCA]" por error de captura/homofonía) contiene en realidad una **cotización temprana de este mismo proyecto Caso-05** (mismo cliente, misma dirección de obra, mismo código interno alterno "[CLIENTE-A]-2026-001", fechada 21-Feb-2026), no un proyecto de oficinas ni el proyecto cancelado del aeropuerto. Ver Sección 4 para el detalle de la discrepancia de cifras entre esa cotización temprana y el contrato final.

**Nota adicional de trazabilidad:** el contratista que firma el Acta de Entrega-Recepción es **BANDEJAS FODDER, SA DE CV** (empresa de Pablo Carducci, no PICC directamente), representada por Rafael Chapa Hammeken. La factura CFDI en el expediente (`CFDI-ESM831024PX0-10FC2-I-127015C.pdf/.xml`) corresponde a un RFC distinto (ESM831024PX0), no verificado en este ejercicio — **[DATO NO DISPONIBLE EN FUENTE]** sobre a qué entidad corresponde ese RFC exactamente.

---

## 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto | Caso-05 — Rehabilitación Cubierta Post-Incendio |
| Fecha del "diagnóstico" reconstruido | Reconstrucción hecha 2026-07-16, sobre un ciclo de proyecto completo: levantamiento 17-Ene-2026 → entrega 17-Abr-2026 |
| Facilitador | No aplica — no hubo sesión en vivo. Reconstrucción documental por agente IA bajo autorización ZEUS |
| ICP hipotético (referencia interna) | ICP-H02 (Industrial e instalaciones críticas) — hipótesis del reconstructor; bodega industrial con daño estructural por incendio. No hay clasificación ICP formal registrada en las fuentes |
| Duración de la "sesión" | No aplica (modalidad retrospectiva) |

## 2. Resumen ejecutivo

El proyecto reconstruye la rehabilitación de una bodega industrial de 675 m² (126 m² dañados) tras un incendio, para el cliente [CLIENTE-A] / [CLIENTE-A] ("[CLIENTE-A-MARCA]"). El ciclo completo está documentado: levantamiento técnico (17-Ene), propuesta económica formal ($996,466.17 MXN con IVA, 21-Ene), inicio de obra (3-Feb), un **incidente de robo de material eléctrico** en zona AICM (10-Mar) que detuvo parcialmente la partida eléctrica, un **déficit de flujo de caja documentado y cuantificado** por cobranza tardía del Anticipo 2 (29 días sin cobrar, alerta explícita "NO ENVIADO — email formal de cobro nunca se envió"), y cierre con Acta de Entrega-Recepción firmada sin observaciones del cliente (17-Abr). El expediente incluye además un **análisis de discrepancia interna de precios** (`ANALISIS_DIFERENCIAS.md`, DEDALO, 19-Ene) que muestra que el sistema de cotización paramétrica de PICC calculó un costo -28% menor al precio final cotizado al cliente, y una **segunda discrepancia** entre la cotización temprana hallada en `CASO-05-COT-TEMPRANA` ($1,257,991.21 con IVA, 21-Feb) y el monto finalmente contratado y facturado ($996,466.17 con IVA) — una diferencia de -20.8% entre dos documentos de precio para el mismo proyecto, sin que el expediente explique la reconciliación.

## 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| Robo de tablero eléctrico (y probable medidor) en local ALL-54 AICM, 10-Mar-2026, que detuvo parcialmente la Partida 07 (instalación eléctrica) | D (Riesgo técnico y de ejecución) | S3 — Riesgo alto (detiene una partida completa, requiere reposición y coordinación con CFE) | E3 — Evidencia operativa (`REPORTE_AVANCE_03_20260318.md` Sección 6; audio de Rafael Chapa transcrito en `ESTADO_CUENTA.md`: "se llevaron la caja completa") | 5 (Qué riesgos existen) | Soportada — hay evidencia directa, ubicación, fecha y transcripción |
| Déficit de flujo de caja de obra por cobranza tardía del Anticipo 2 (-$50,342.86 saldo libre neto, 29 días sin cobrar al 25-Mar, "email formal de cobro nunca se envió") | C (presupuesto) | S3 — Riesgo alto (compromete pago a subcontratista Heyman, $208,650 pendientes, y genera préstamos personales de Pablo a la obra) | E3 — Evidencia operativa (`ESTADO_CUENTA.md`, cifras exactas y fecha de último contacto documentadas) | 4 (Qué presupuesto debo esperar), 5 | Soportada |
| Discrepancia de -28% entre el costo calculado por el sistema paramétrico interno de PICC ($588,293.58 / $472,898.84 según fase) y el precio cotizado al cliente ($829,980 / $996,466.17 con IVA) | Brecha de método interno de PICC, no del proyecto del cliente | S1 — Riesgo bajo para el cliente (el margen resultó favorable a PICC, no hay evidencia de sobreprecio dañino), pero relevante para la disciplina de pricing interna | E3 — Evidencia operativa (`ANALISIS_DIFERENCIAS.md`, tabla completa por fase y partida) | No aplica al proyecto del cliente — se registra como hallazgo de proceso interno de PICC (ver DEF-06 en Sheet de Defectos) | No evaluable (es evidencia de método de pricing, no de riesgo del cliente) |
| Discrepancia de -20.8% entre la cotización temprana hallada en `CASO-05-COT-TEMPRANA` ($1,257,991.21 con IVA, 21-Feb-2026, 39 partidas detalladas) y el monto finalmente contratado ($996,466.17 con IVA, 21-Ene-2026 según `HISTORIAL.md`) para el mismo proyecto | Brecha de método interno de PICC | S2 — Riesgo medio (dos documentos de precio distinto para el mismo cliente y proyecto, sin reconciliación documentada visible) | E2 — Evidencia parcial trazable (ambos documentos existen y son consultables, pero no hay nota que explique cuál es la versión vigente o por qué cambió) | 4 | No evaluable — el expediente no aclara la secuencia exacta (¿cuál cotización se presentó primero al cliente?) |
| Condiciones de sitio no verificadas descubiertas durante ejecución (vigueta caída reparada en canalón, mencionada en WhatsApp 03-Mar sin estar en el alcance original documentado) | D | S2 — Riesgo medio (trabajo adicional no cotizado explícitamente, absorbido dentro del alcance sin orden de cambio visible en el expediente) | E2 — Evidencia parcial trazable (mencionado en bitácora de actividad WhatsApp de `ESTADO_CUENTA.md`, no hay orden de cambio formal documentada) | 5, 3 (alcance) | Parcialmente soportada |
| Retiro de asbesto y manejo de residuo peligroso como partida crítica de cumplimiento regulatorio | E (regulatorio) | S3 — Riesgo alto (manejo de residuo peligroso; requiere manifiesto certificado) | E3 — Evidencia operativa (partida explícita en presupuesto de `CASO-05-COT-TEMPRANA`, "Retiro de vegetacion invasiva" y limpieza confirmadas; manifiesto de residuos en `ANALISIS_DIFERENCIAS.md` Fase 1) | 5 | Soportada |
| Préstamos personales de Pablo a la obra ($23,050.02) y adelantos contra utilidades ($14,295.99 por compra de hardware GPU no relacionado con la obra) sin reembolso al momento del último dato disponible | C (presupuesto) | S2 — Riesgo medio (mezcla de finanzas personales y de proyecto; riesgo de trazabilidad contable) | E3 — Evidencia operativa (montos, fechas y método de pago documentados en `ESTADO_CUENTA.md`) | 4 | Parcialmente soportada — el reembolso queda condicionado al cobro del Anticipo 2, que a su vez está bloqueado |

## 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| Reconciliación entre la cotización de `CASO-05-COT-TEMPRANA` ($1,257,991.21, 21-Feb) y el monto contratado en `HISTORIAL.md` ($996,466.17, propuesta formal fechada 21-Ene, es decir un mes *antes* de la cotización de mayor monto) | Ausencia de verificación | Confirmar con Rafael Chapa/Dirección PICC cuál de las dos cotizaciones se presentó realmente al cliente y por qué existe una posterior con monto mayor si el contrato ya estaba cerrado en fecha anterior | Dirección PICC / Rafael Chapa |
| Impacto presupuestal exacto del robo de tablero eléctrico (10-Mar) — el reporte de avance lo marca "PENDIENTE — definir impacto en presupuesto electrico AICM" sin cifra de reposición | Ausencia de dato | Cotizar la reposición del tablero y definir si el costo lo absorbe PICC, el cliente, o un reclamo de seguro | PICC Ingeniería / Rafael Chapa |
| Identidad exacta del RFC en el CFDI del expediente (ESM831024PX0), distinto del RFC del contratista firmante del Acta (BFO120802N42, Bandejas Fodder) | Información no compartida / no definida en fuente | Verificar internamente qué entidad facturó y por qué difiere del contratista firmante | Dirección PICC |
| Estado final del reembolso a Pablo de los préstamos personales ($23,050.02) y del adelanto de hardware ($14,295.99) — el expediente solo documenta el estado hasta el 25-Mar-2026, sin confirmación de cierre financiero final pese a que la obra se entregó 17-Abr | Ausencia de verificación | Actualizar `ESTADO_CUENTA.md` con el cierre financiero real posterior al 25-Mar | CRONOS / HEFESTO |
| Naturaleza del "Contacto Ali" mencionado el 19-Mar en la bitácora de WhatsApp ("quiere platicar", naturaleza desconocida) | Ausencia de dato | Sin información suficiente para inferir — se documenta la mención tal cual aparece en la fuente | Rafael Chapa / Pablo |
| Orden de cambio formal para la vigueta caída reparada en canalón — se menciona en bitácora de actividad pero no hay documento de orden de cambio en el expediente | Ausencia de definición | Verificar si el trabajo adicional se absorbió dentro del margen o si generó una nota de cargo no capturada en el expediente | PICC Ingeniería |

## 5. Recomendaciones priorizadas

1. Enviar de inmediato el cobro formal del Anticipo 2 en cualquier proyecto activo con el mismo patrón de cobranza pasiva — este caso muestra que "facturado pero sin solicitud formal de pago" generó 29 días de deficit de flujo y préstamos personales de Pablo a la obra. Esto es un patrón de proceso, no un hallazgo aislado de este proyecto.
2. Definir un protocolo de seguridad de materiales en obra para proyectos ubicados en o cerca de instalaciones de alta vigilancia como el AICM — el robo de tablero eléctrico generó una detención parcial de partida sin mecanismo de mitigación documentado previamente.
3. Reconciliar las dos cotizaciones (`CASO-05-COT-TEMPRANA` vs. el monto de `HISTORIAL.md`) antes de que esta discrepancia se repita en otro proyecto del mismo cliente — mismo patrón que DEF-03 de la Ronda 1 (Caso-01).
4. Separar contablemente los préstamos personales de Pablo y los adelantos contra utilidades de los costos directos de obra, con fecha de cierre explícita, para evitar que la trazabilidad financiera del proyecto quede abierta después de la entrega formal.
5. Documentar formalmente (orden de cambio firmada) cualquier trabajo adicional descubierto en sitio, como la reparación de vigueta caída, en vez de absorberlo silenciosamente dentro del alcance original.

## 6. Siguiente paso propuesto

- Siguiente paso concreto: cerrar el estado financiero final del proyecto (confirmar cobro de Anticipo 2, saldo final, reembolsos a Pablo) y reconciliar las dos cotizaciones de precio distintas.
- Owner del siguiente paso: CRONOS/HEFESTO (cierre financiero) + Dirección PICC (reconciliación de cotizaciones).
- Plazo sugerido: `[DATO NO DISPONIBLE EN FUENTE]` — ninguna fuente registra una fecha comprometida para este cierre posterior al 25-Mar-2026.

## 7. Límites del diagnóstico

> Este diagnóstico se basa en la información compartida durante la sesión del [no aplica — reconstrucción documental retrospectiva, no hubo sesión]. No sustituye una auditoría técnica, legal o financiera formal. Los hallazgos marcados como "no verificados" requieren confirmación antes de tomarse como base de decisión final.

Aclaración adicional: a diferencia de un caso piloto real, este resultado no fue validado con ningún cliente ni con el equipo que ejecutó la obra. Es una reconstrucción hecha exclusivamente a partir de documentos ya existentes (incluida una bitácora de WhatsApp ya procesada por MERCURIO/HEFESTO, no mensajes originales revisados directamente por este reconstructor).

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
| 2 | Completitud | Aproximadamente 18 de 24 preguntas del Banco (DOC-057) respondibles con cita directa de fuente (~75%). Las 4 preguntas condicionales de ICP-H01/H02 no todas aplican a una bodega de almacenamiento sin operación crítica continua (B-03, D-03, D-06 se marcan como no aplicables al tipo de proyecto, no como brecha) | Cálculo aproximado del reconstructor, es el más alto de los 6 casos reconstruidos a la fecha (Rondas 1 y 2) |
| 3 | Claridad percibida | NO APLICA — modalidad retrospectiva | Requiere cliente real respondiendo en Fase 5 |
| 4 | Utilidad percibida | NO APLICA — modalidad retrospectiva | Ídem |
| 5 | Gaps identificados | 6 (ver sección 4) | Conteo directo |
| 6 | Cambio de prioridad (hipotético) | Hipótesis del reconstructor: SÍ — el patrón de cobranza pasiva (nunca se envió solicitud formal) es un riesgo de proceso repetible que debería tratarse como acción preventiva en todo proyecto activo, no solo en este caso | Inferencia marcada explícitamente como tal |
| 7 | Reducción de retrabajo | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 8 | Intención de compartir | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 9 | Intención de avanzar | NO APLICA — modalidad retrospectiva | Requiere respuesta del cliente |
| 10 | Decisión afectada | SÍ, decisiones 4 y 5 — el ejercicio retrospectivo movió ambas de "parcialmente soportada" a "soportada" usando datos ya existentes | Evaluación del reconstructor sobre datos documentales |
| 11 | Señal comercial downstream | NO APLICA — modalidad retrospectiva | Requiere seguimiento real con cliente |
| 12 | Errores críticos | 2 (ver DEF-06 y DEF-07 en Sheet de Defectos, DOC-061) | Dos discrepancias de precio distintas detectadas en el mismo proyecto |
