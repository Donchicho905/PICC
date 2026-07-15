# Customer Journey

## Ficha de Trazabilidad
- ID: DOC-011
- Estado: 🟡 En desarrollo
- Tipo: Buyer Journey V1
- Objetivo: Mapear el recorrido del comprador por ICP desde la necesidad hasta la referencia, dejando visibles preguntas, decisiones, objeciones, evidencias y señales.
- Entradas:
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Salidas:
  - Buyer Journey por ICP
  - puntos de contacto y CTA por etapa
  - datos faltantes por etapa
- Dependencias:
  - RL-001 (02_VERDAD_COMERCIAL/RESEARCH_LEDGER.md)
  - DOC-007 (02_VERDAD_COMERCIAL/Auditoria_Sitio.md)
- Documentos consumidos:
  - Home publica de `picc.com.mx`
  - fuentes operativas del ecosistema leidas en este sprint
- Documentos generados:
  - DOC-014 (03_MODELO_COMERCIAL/Modelo_Comercial.md)
  - DOC-020 (05_PRODUCTO/Capability_Model.md)
- Responsable: Direccion Comercial + Producto
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Cada ICP tiene journey explicito
  - Las hipotesis se distinguen de los hechos
  - Cada etapa deja clara la decision y el dato faltante

## Como leer este documento

- Cada tabla sintetiza contexto, pregunta dominante, decision, objecion o riesgo, evidencia buscada, surface, CTA, intervencion, owner, señales y KPI.
- La mayoria de los journeys son hipotesis operativas sustentadas en evidencia parcial; no deben leerse como comportamiento ya validado por CRM.

## Etapas canonicas

1. Reconoce una necesidad u oportunidad.
2. Intenta comprender el problema.
3. Investiga alternativas.
4. Define requisitos.
5. Compara proveedores o soluciones.
6. Construye shortlist.
7. Valida confianza.
8. Solicita conversacion o diagnostico.
9. Evalua propuesta.
10. Obtiene aprobacion interna.
11. Negocia.
12. Contrata.
13. Evalua ejecucion.
14. Repite o refiere.

## ICP-H01 - Infraestructura critica y Data Centers

| Etapa | Contexto y pregunta dominante                                | Decision necesaria               | Incertidumbre / riesgo / objecion     | Informacion y evidencia buscada                | Surface / CTA                         | Intervencion PICC / owner | Señal de avance / abandono / KPI                                                                  | Dato faltante             |
| ----- | ------------------------------------------------------------ | -------------------------------- | ------------------------------------- | ---------------------------------------------- | ------------------------------------- | ------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------- |
| 1     | Operacion critica crece. ¿Debo actuar ahora?                 | Activar proyecto                 | Riesgo de postergar vs CAPEX          | Tendencia de demanda, riesgo de downtime       | Home / ver servicios                  | Digital / Marketing       | avance: consulta inicial; abandono: seguir operando igual; KPI: visitas a infraestructura critica | trigger real del problema |
| 2     | ¿Es un problema de disponibilidad, capacidad o cumplimiento? | Enmarcar el problema             | Mala definicion tecnica               | Lista de sintomas, riesgos, auditorias         | Home + contacto / solicitar consulta  | Humana ligera / Comercial | avance: describe dolor; abandono: problema difuso; KPI: formularios calificados                   | auditorias y SLA reales   |
| 3     | ¿A quien considero?                                          | Abrir comparacion                | Temor a proveedor sin especializacion | Credenciales, certificaciones, servicios       | Home / ver Data Centers               | Digital / Marketing       | avance: navega a infra critica; abandono: rebote; KPI: click a servicios                          | competidores evaluados    |
| 4     | ¿Que alcance necesito?                                       | Definir diseno, retrofit o build | Sobredimensionar o subdimensionar     | Metodologia, alcances, disciplinas             | Reunion / diagnostico                 | Comercial + Tecnico       | avance: pide visita; abandono: no define alcance; KPI: diagnosticos agendados                     | formato de discovery      |
| 5     | ¿Que proveedores entienden esto?                             | Comparar soluciones              | Propuestas no comparables             | Casos, metodologia, estandares                 | Caso / propuesta preliminar           | Comercial + Operaciones   | avance: pide comparativo; abandono: solo precio; KPI: shortlist rate                              | casos publicables         |
| 6     | ¿PICC entra a shortlist?                                     | Incluir o excluir                | Duda de experiencia comparable        | Casos, equipo, certificacion, cobertura        | Pagina sectorial futura / CTA reunion | Comercial                 | avance: shortlist; abandono: pide solo brochure; KPI: shortlist by ICP                            | cartera comparables       |
| 7     | ¿Puedo confiar tecnica e institucionalmente?                 | Validar confianza                | Riesgo reputacional y tecnico         | Certificaciones, equipo, referencias           | Trust assets / contacto               | Direccion + Comercial     | avance: solicita referencias; abandono: compliance bloquea; KPI: trust validation rate            | referencias autorizadas   |
| 8     | ¿Vale la pena una conversacion?                              | Agendar diagnostico              | Temor a perder tiempo                 | Agenda, experto asignado, siguiente paso claro | WhatsApp / correo / agenda            | Comercial + Tecnico       | avance: reunion agendada; abandono: ghosting; KPI: meeting set rate                               | script de discovery       |
| 9     | ¿La propuesta es defendible?                                 | Evaluar propuesta                | Propuesta poco clara o riesgosa       | Alcance, riesgos, fases, supuestos             | Propuesta                             | Comercial + Operaciones   | avance: feedback tecnico; abandono: no responde; KPI: proposal progression                        | benchmarks de costo       |
| 10    | ¿Como la apruebo internamente?                               | Obtener aprobacion               | Comite y finanzas                     | comparables, riesgos mitigados, credenciales   | deck / propuesta                      | Direccion + Comercial     | avance: pide material interno; abandono: se cae en comite; KPI: approval support rate             | champions internos        |
| 11    | ¿Que termino debo negociar?                                  | Ajustar alcance y condiciones    | Riesgo contractual y economico        | hitos, exclusiones, SLA                        | Propuesta + reunion                   | Comercial + Legal         | avance: redlines; abandono: silencio; KPI: negotiation cycle                                      | terminos recurrentes      |
| 12    | ¿Contrato a PICC?                                            | Firmar                           | Ultima duda de confianza              | cierre claro, siguiente paso, equipo ejecutor  | contrato / kickoff                    | Direccion + Operaciones   | avance: kickoff; abandono: delay; KPI: close rate                                                 | tiempos de cierre         |
| 13    | ¿La ejecucion confirma la promesa?                           | Evaluar desempeno                | Incumplimiento                        | avance, comunicacion, entregables              | seguimiento / portal futuro           | Operaciones               | avance: hitos cumplidos; abandono: escalacion; KPI: delivery health                               | metricas de satisfaccion  |
| 14    | ¿Los volveria a contratar?                                   | Recompra o referencia            | Mala experiencia                      | caso, testimonio, expansion                    | seguimiento / caso                    | Direccion + Comercial     | avance: referencia; abandono: cierre frio; KPI: repeat/referral rate                              | NPS y testimonios         |

## ICP-H02 - Industrial e instalaciones criticas

| Etapa | Contexto y pregunta dominante                     | Decision necesaria    | Incertidumbre / riesgo / objecion     | Informacion y evidencia buscada          | Surface / CTA                  | Intervencion PICC / owner | Señal de avance / abandono / KPI                                                       | Dato faltante            |
| ----- | ------------------------------------------------- | --------------------- | ------------------------------------- | ---------------------------------------- | ------------------------------ | ------------------------- | -------------------------------------------------------------------------------------- | ------------------------ |
| 1     | Hay una falla, expansion o adecuacion. ¿Actuo ya? | Priorizar proyecto    | costo de no hacer nada                | impacto operativo                        | Home / contacto                | Digital / Marketing       | avance: llamada por problema puntual; abandono: pospone CAPEX; KPI: inbound industrial | frecuencia de trigger    |
| 2     | ¿Es un tema de obra, electrico o HVAC?            | Definir problema      | diagnostico incompleto                | checklist tecnico                        | contacto / diagnostico         | Comercial + Tecnico       | avance: comparte fotos o planos; abandono: informacion minima; KPI: discovery depth    | formato estandar         |
| 3     | ¿Quien puede resolver sin frenar operacion?       | Abrir alternativas    | miedo a paro o retrabajo              | experiencia en operacion viva            | Home + servicios               | Digital / Comercial       | avance: revisa industrial; abandono: compra por precio; KPI: service page CTR          | casos en operacion       |
| 4     | ¿Que requisitos debo exigir?                      | Fijar requerimientos  | seguridad y continuidad               | metodologia, seguridad, fases            | reunion / visita               | Tecnico + Operaciones     | avance: visita; abandono: alcance difuso; KPI: site visits                             | matriz de seguridad      |
| 5     | ¿Como comparo opciones?                           | Comparar proveedores  | propuestas poco comparables           | tiempos, fases, riesgos, equipo          | propuesta preliminar           | Comercial                 | avance: pide comparativo; abandono: licitacion cerrada; KPI: compare-ready proposals   | comparables reales       |
| 6     | ¿PICC entra a shortlist?                          | Incluir               | duda sobre especializacion industrial | experiencia, instalaciones, coordinacion | sectorial futura / CTA reunion | Comercial                 | avance: shortlist; abandono: proveedor incumbente; KPI: shortlist rate                 | pipeline por industria   |
| 7     | ¿Confio en la ejecucion?                          | Validar confianza     | incumplimiento y seguridad            | equipo, supervision, referencias         | trust assets                   | Direccion + Operaciones   | avance: due diligence; abandono: compliance; KPI: trust checks                         | referencias industriales |
| 8     | ¿Agendo visita o diagnostico?                     | Reunirse              | disponibilidad y costo de tiempo      | agenda clara, experto correcto           | WhatsApp / correo              | Comercial                 | avance: visita confirmada; abandono: no contesta; KPI: meeting set                     | response SLA actual      |
| 9     | ¿La propuesta cuida operacion y costo?            | Evaluar propuesta     | paro no previsto                      | fases, riesgos, exclusiones              | propuesta                      | Comercial + Operaciones   | avance: comentarios; abandono: objecion costo; KPI: proposal progression               | costo de paro            |
| 10    | ¿Pasa el filtro interno?                          | Aprobar               | compras vs operaciones                | argumentos economicos y tecnicos         | deck / propuesta               | Direccion + Comercial     | avance: pide version comite; abandono: freeze; KPI: approval support                   | mapa de stakeholders     |
| 11    | ¿Que negocio cierro?                              | Negociar terminos     | alcance y tiempos                     | hitos, exclusiones, forma de trabajo     | reunion / propuesta            | Comercial + Legal         | avance: redlines; abandono: cambio de prioridad; KPI: negotiation days                 | terminos frecuentes      |
| 12    | ¿Contrato?                                        | Firmar                | riesgo final de proveedor             | equipo ejecutor, arranque                | contrato / kickoff             | Direccion + Operaciones   | avance: PO o contrato; abandono: pausa; KPI: win rate                                  | lead time legal          |
| 13    | ¿Cumplen sin afectar produccion?                  | Evaluar ejecucion     | retrasos o incidentes                 | seguimiento y control                    | seguimiento                    | Operaciones               | avance: hitos; abandono: escalacion; KPI: on-time execution                            | metricas reales          |
| 14    | ¿Los vuelvo a llamar?                             | Recompra o referencia | experiencia final                     | resultados y relacion                    | seguimiento                    | Comercial + Direccion     | avance: nueva solicitud; abandono: cierre frio; KPI: repeat business                   | historial recompra       |

## ICP-H03 - Corporativo, oficinas e instalaciones comerciales

| Etapa | Contexto y pregunta dominante           | Decision necesaria          | Incertidumbre / riesgo / objecion | Informacion y evidencia buscada       | Surface / CTA        | Intervencion PICC / owner | Señal de avance / abandono / KPI                                              | Dato faltante           |
| ----- | --------------------------------------- | --------------------------- | --------------------------------- | ------------------------------------- | -------------------- | ------------------------- | ----------------------------------------------------------------------------- | ----------------------- |
| 1     | Mudanza o adecuacion. ¿Debo moverme ya? | Abrir proyecto              | fecha y presupuesto               | impacto en operacion                  | Home / contacto      | Digital                   | avance: consulta; abandono: pausa interna; KPI: inbound corporativo           | volumen real            |
| 2     | ¿Que problema quiero resolver?          | Definir necesidad           | alcance difuso                    | layout, instalaciones, imagen         | contacto / reunion   | Comercial                 | avance: comparte contexto; abandono: muy vago; KPI: discovery quality         | plantillas              |
| 3     | ¿Que alternativas hay?                  | Comparar tipos de proveedor | despacho vs contratista           | oferta integral, experiencia          | Home + servicios     | Digital                   | avance: revisa remodelaciones; abandono: rebote; KPI: CTR comercial           | competencia observada   |
| 4     | ¿Que requisitos debe cumplir?           | Definir requerimientos      | aprobacion de usuarios            | tiempos, acabados, operacion          | reunion / visita     | Comercial + Tecnico       | avance: visita; abandono: no define; KPI: visits                              | requisitos frecuentes   |
| 5     | ¿Como comparo propuestas?               | Comparar                    | heterogeneidad de alcances        | comparables, exclusiones, metodologia | propuesta preliminar | Comercial                 | avance: pide comparativo; abandono: precio puro; KPI: compare-ready proposals | benchmark               |
| 6     | ¿PICC entra a shortlist?                | Incluir                     | falta de caso visible             | experiencia, equipo, confiabilidad    | sectorial futura     | Comercial                 | avance: shortlist; abandono: proveedor de confianza; KPI: shortlist rate      | casos publicados        |
| 7     | ¿Confio en ellos?                       | Validar confianza           | calidad y tiempos                 | referencias, fotos, casos             | trust assets         | Direccion + Comercial     | avance: due diligence; abandono: dudas; KPI: trust conversion                 | referencias autorizadas |
| 8     | ¿Agendo conversacion?                   | Reunirse                    | costo de tiempo                   | siguiente paso claro                  | WhatsApp / correo    | Comercial                 | avance: meeting; abandono: ghosting; KPI: meeting set                         | cadencia actual         |
| 9     | ¿La propuesta es defendible?            | Evaluar                     | alcance incierto                  | cronograma, fases, costo, riesgos     | propuesta            | Comercial + Operaciones   | avance: feedback; abandono: se enfria; KPI: proposal progression              | win/loss data           |
| 10    | ¿Pasa internamente?                     | Aprobar                     | comite y presupuesto              | version ejecutiva                     | deck / propuesta     | Direccion                 | avance: share internally; abandono: freeze; KPI: internal approval assist     | who approves            |
| 11    | ¿Negocio bien?                          | Negociar                    | ajuste de alcance                 | terminos, fases                       | reunion              | Comercial                 | avance: redlines; abandono: desaparece; KPI: negotiation cycle                | objeciones reales       |
| 12    | ¿Contrato?                              | Firmar                      | ultima comparacion                | claridad de arranque                  | contrato             | Direccion + Operaciones   | avance: firma; abandono: pausa; KPI: close rate                               | procurement process     |
| 13    | ¿La ejecucion fue ordenada?             | Evaluar                     | disruption                        | seguimiento, calidad                  | seguimiento          | Operaciones               | avance: recepcion; abandono: reclamos; KPI: delivery quality                  | satisfaction data       |
| 14    | ¿Los refiero o repito?                  | Recomendar                  | experiencia final                 | cierre y relacion                     | seguimiento          | Comercial                 | avance: nueva fase; abandono: sin seguimiento; KPI: repeat/referral           | referral data           |

## ICP-H04 - Desarrollador inmobiliario mediano

| Etapa | Contexto y pregunta dominante         | Decision necesaria | Incertidumbre / riesgo / objecion   | Informacion y evidencia buscada      | Surface / CTA         | Intervencion PICC / owner | Señal de avance / abandono / KPI                                                   | Dato faltante         |
| ----- | ------------------------------------- | ------------------ | ----------------------------------- | ------------------------------------ | --------------------- | ------------------------- | ---------------------------------------------------------------------------------- | --------------------- |
| 1     | Hay un predio o proyecto. ¿Lo activo? | Abrir estudio      | mercado y factibilidad              | siguiente paso claro                 | Home / contacto       | Digital                   | avance: solicita viabilidad; abandono: pausa inversion; KPI: inbound dev           | pipeline dev          |
| 2     | ¿Que problema resolver primero?       | Enfocar fase       | mezcla de permisos, costo, producto | diagnostico inicial                  | reunion               | Comercial + Tecnico       | avance: comparte info; abandono: informacion minima; KPI: discovery quality        | info de predio        |
| 3     | ¿Estudio, diseno o ejecucion?         | Elegir ruta        | secuencia incorrecta                | metodologia por fase                 | contenido futuro      | Comercial                 | avance: pide propuesta de fase; abandono: salta entre opciones; KPI: phase clarity | tasas por fase        |
| 4     | ¿Que requisitos importan?             | Definir alcance    | permisos, retorno, producto         | riesgos, dependencias                | reunion / diagnostico | Tecnico + Comercial       | avance: workshop; abandono: indefinicion; KPI: scoped diagnostics                  | playbook desarrollo   |
| 5     | ¿Que proveedores comparo?             | Comparar           | despacho parcial vs integrador      | casos, catalogos, costos, criterio   | propuesta / caso      | Comercial                 | avance: pide comparativo; abandono: incumbente fijo; KPI: compare-ready            | comparables reales    |
| 6     | ¿PICC entra a shortlist?              | Incluir            | duda sobre escala y experiencia     | proyectos similares, equipo, proceso | cases future          | Comercial                 | avance: shortlist; abandono: sin fit; KPI: shortlist dev                           | casos publicables     |
| 7     | ¿Confio para estudiar o ejecutar?     | Validar confianza  | inversion mal dirigida              | referencias, entregables, rigor      | trust assets          | Direccion                 | avance: diligence; abandono: duda de experiencia; KPI: trust conversion            | references            |
| 8     | ¿Agendo diagnostico?                  | Reunirse           | costo de tiempo                     | diagnostico y salida concreta        | correo / WhatsApp     | Comercial                 | avance: reunion; abandono: silencio; KPI: meeting set                              | agenda owners         |
| 9     | ¿La propuesta me ayuda a decidir?     | Evaluar            | propuesta ornamental                | fases, riesgos, supuestos            | propuesta             | Comercial + Tecnico       | avance: feedback; abandono: enfriamiento; KPI: proposal progression                | proposal templates    |
| 10    | ¿Lo aprueban socios o inversionistas? | Aprobar            | comite / capital                    | material defendible                  | deck / propuesta      | Direccion                 | avance: share; abandono: no fondea; KPI: approval assist                           | who approves          |
| 11    | ¿Negocio alcance y honorarios?        | Negociar           | sensibilidad a costo                | hitos, exclusiones                   | reunion               | Comercial                 | avance: redlines; abandono: cambio de direccion; KPI: negotiation cycle            | fee benchmarks        |
| 12    | ¿Contrato?                            | Firmar             | indecision final                    | arranque y equipo                    | contrato              | Direccion                 | avance: firma; abandono: ghosting; KPI: win rate                                   | close reasons         |
| 13    | ¿La ejecucion confirma viabilidad?    | Evaluar            | desviacion                          | control y seguimiento                | seguimiento           | Operaciones               | avance: hitos; abandono: conflictos; KPI: execution health                         | cost/performance data |
| 14    | ¿Repito en otro proyecto?             | Recompra           | experiencia final                   | resultado y confianza                | seguimiento           | Comercial + Direccion     | avance: nueva fase o nuevo predio; abandono: cierre frio; KPI: repeat dev          | repeat data           |

## ICP-H05 - Propietario o inversionista con terreno

| Etapa | Contexto y pregunta dominante           | Decision necesaria        | Incertidumbre / riesgo / objecion | Informacion y evidencia buscada | Surface / CTA         | Intervencion PICC / owner | Señal de avance / abandono / KPI                                                | Dato faltante       |
| ----- | --------------------------------------- | ------------------------- | --------------------------------- | ------------------------------- | --------------------- | ------------------------- | ------------------------------------------------------------------------------- | ------------------- |
| 1     | Tengo un terreno o idea. ¿Hago algo?    | Activar exploracion       | no saber por donde empezar        | siguiente paso simple           | Home / contacto       | Digital                   | avance: pide orientacion; abandono: lo deja en pausa; KPI: discovery leads      | volumen             |
| 2     | ¿Que problema resolver?                 | Entender objetivo         | confusion entre deseo y alcance   | preguntas guiadas               | contacto              | Comercial                 | avance: describe objetivo; abandono: conversa sin avanzar; KPI: discovery calls | intake actual       |
| 3     | ¿A quien consulto?                      | Abrir alternativas        | desconfianza de proveedor         | credenciales y proceso          | Home                  | Digital                   | avance: navega y pregunta; abandono: solo pide precio; KPI: engaged sessions    | source mix          |
| 4     | ¿Que necesito definir?                  | Delimitar predio/proyecto | falta de datos                    | checklist                       | diagnostico           | Comercial + Tecnico       | avance: comparte info; abandono: no tiene datos; KPI: data completion           | checklist real      |
| 5     | ¿Que proveedores comparo?               | Comparar                  | propuestas no comparables         | escenarios y pasos              | propuesta inicial     | Comercial                 | avance: pide escenario; abandono: compra commodity; KPI: proposal progression   | competitor behavior |
| 6     | ¿PICC entra a shortlist?                | Incluir                   | falta de confianza                | experiencia y claridad          | futura landing / caso | Comercial                 | avance: shortlist; abandono: no contesta; KPI: shortlist rate                   | references          |
| 7     | ¿Confio para avanzar?                   | Validar confianza         | miedo a perder dinero             | quien responde, proceso, casos  | trust assets          | Direccion                 | avance: pide visita; abandono: dudas; KPI: trust conversion                     | testimonials        |
| 8     | ¿Agendo visita?                         | Reunirse                  | costo de tiempo                   | visita o diagnostico claro      | WhatsApp              | Comercial                 | avance: agenda; abandono: no fija fecha; KPI: visit set rate                    | response SLA        |
| 9     | ¿La propuesta aclara el siguiente paso? | Evaluar                   | propuesta vaga                    | alcance, rangos, supuestos      | propuesta             | Comercial                 | avance: responde; abandono: silencio; KPI: proposal response                    | proposal template   |
| 10    | ¿Lo apruebo con familia o socios?       | Aprobar                   | dudas patrimoniales               | claridad de riesgos             | deck simple           | Comercial + Direccion     | avance: comparte; abandono: pausa; KPI: approval support                        | approver map        |
| 11    | ¿Negocio?                               | Negociar                  | presupuesto y confianza           | hitos y alcances                | reunion               | Comercial                 | avance: redlines; abandono: desaparece; KPI: negotiation cycle                  | typical objections  |
| 12    | ¿Contrato?                              | Firmar                    | ultima duda                       | quien ejecuta y como arranca    | contrato              | Direccion                 | avance: firma; abandono: pausa; KPI: close rate                                 | close data          |
| 13    | ¿La ejecucion me dio tranquilidad?      | Evaluar                   | ansiedad por calidad/costo        | seguimiento y transparencia     | seguimiento           | Operaciones               | avance: feedback; abandono: reclamos; KPI: satisfaction                         | satisfaction data   |
| 14    | ¿Los recomiendo?                        | Referir                   | experiencia final                 | cierre correcto                 | seguimiento           | Comercial                 | avance: referencia; abandono: sin respuesta; KPI: referrals                     | referral data       |

## ICP-H06 - Cliente privado high-ticket

| Etapa | Contexto y pregunta dominante                       | Decision necesaria | Incertidumbre / riesgo / objecion | Informacion y evidencia buscada | Surface / CTA      | Intervencion PICC / owner | Señal de avance / abandono / KPI                                                 | Dato faltante   |
| ----- | --------------------------------------------------- | ------------------ | --------------------------------- | ------------------------------- | ------------------ | ------------------------- | -------------------------------------------------------------------------------- | --------------- |
| 1     | Quiero construir o remodelar. ¿Ahora es el momento? | Abrir proyecto     | presupuesto y timing              | ejemplos y proceso              | Home / contacto    | Digital                   | avance: consulta; abandono: pospone; KPI: residential inquiries                  | volume          |
| 2     | ¿Que necesito realmente?                            | Definir necesidad  | idea difusa                       | preguntas guiadas               | contacto           | Comercial                 | avance: brief; abandono: no define; KPI: discovery quality                       | intake format   |
| 3     | ¿A quien considero?                                 | Abrir alternativas | miedo a proveedor incorrecto      | referencias y presencia         | Home               | Digital                   | avance: pide info; abandono: solo precio; KPI: engaged leads                     | source mix      |
| 4     | ¿Que requisitos debo fijar?                         | Delimitar alcance  | calidad vs presupuesto            | checklist y riesgos             | diagnostico        | Comercial + Tecnico       | avance: visita; abandono: no comparte info; KPI: visit set                       | checklist       |
| 5     | ¿Como comparo propuestas?                           | Comparar           | propuestas no equivalentes        | alcances, tiempos, acabados     | propuesta          | Comercial                 | avance: pide comparativo; abandono: compra por precio; KPI: proposal progression | benchmark       |
| 6     | ¿PICC entra a shortlist?                            | Incluir            | falta de caso visible             | fotos, referencias, proceso     | caso futuro        | Comercial                 | avance: shortlist; abandono: duda; KPI: shortlist rate                           | cases           |
| 7     | ¿Confio en ellos?                                   | Validar confianza  | reputacion y calidad              | referencias, trato, seguimiento | trust assets       | Direccion                 | avance: pide visita detallada; abandono: ghosting; KPI: trust conversion         | references      |
| 8     | ¿Agendo conversacion?                               | Reunirse           | privacidad y tiempo               | experto correcto                | WhatsApp / llamada | Comercial                 | avance: agenda; abandono: no contesta; KPI: meeting set                          | SLA             |
| 9     | ¿La propuesta me da tranquilidad?                   | Evaluar            | sobrecosto y calidad              | supuestos, fases, materiales    | propuesta          | Comercial + Operaciones   | avance: feedback; abandono: silencio; KPI: proposal response                     | cost ranges     |
| 10    | ¿Lo apruebo con familia?                            | Aprobar            | sensibilidad al gasto             | claridad de decisiones          | deck simple        | Comercial                 | avance: la comparte; abandono: pausa; KPI: approval support                      | family dynamics |
| 11    | ¿Negocio bien?                                      | Negociar           | alcance y precio                  | hitos, exclusiones              | reunion            | Comercial                 | avance: redlines; abandono: se enfria; KPI: negotiation cycle                    | objections      |
| 12    | ¿Contrato?                                          | Firmar             | ultima duda                       | arranque y responsable          | contrato           | Direccion                 | avance: firma; abandono: no define; KPI: close rate                              | close data      |
| 13    | ¿La ejecucion estuvo a la altura?                   | Evaluar            | calidad y comunicacion            | seguimiento visible             | seguimiento        | Operaciones               | avance: hitos; abandono: conflicto; KPI: satisfaction                            | service metrics |
| 14    | ¿Los recomendaria?                                  | Referir            | experiencia final                 | resultado y trato               | seguimiento        | Comercial                 | avance: referencia; abandono: cierre frio; KPI: referrals                        | referral data   |

## Observaciones de metodo

- ICP-H01 e ICP-H02 tienen mejor soporte en etapas tempranas por la Home actual.
- ICP-H04, ICP-H05 y ICP-H06 dependen mucho mas de diagnostico humano y evidencia todavia no estructurada.
- Ningun journey debe tomarse como validado hasta contrastarlo contra CRM, ganados/perdidos y entrevistas con direccion o comercial.
