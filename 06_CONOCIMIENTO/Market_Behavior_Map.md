# Market Behavior Map V1

## Ficha de trazabilidad
- ID: DOC-050
- Estado: 🟢 Aprobado
- Tipo: Market Behavior Map
- Objetivo: Explicar el movimiento del mercado de infraestructura critica desde primeros principios: triggers, actores, poder, riesgo, informacion, confianza y reactivacion.
- Entradas:
  - DOC-047 (06_CONOCIMIENTO/Market_Knowledge_Map.md)
  - DOC-048 (06_CONOCIMIENTO/Buyer_Curiosity_Map.md)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Salidas:
  - Trigger Graph
  - Stakeholder Graph
  - Buying Committee Graph
  - Opportunity Lifecycle
  - Trust Lifecycle
  - Information Flow Map
  - Influence Graph
  - Competitive Dynamics Map
  - Behavioral Demand Flywheel
  - Information Gap Matrix
  - Method of Validation
- Dependencias:
  - DOC-045 (99_META/SYSTEM_MAP.md)
  - DOC-046 (INDEX.md)
  - DOC-047 (06_CONOCIMIENTO/Market_Knowledge_Map.md)
- Documentos consumidos:
  - evidencia publica de `picc.com.mx`
  - conversaciones estrategicas aprobadas
  - modelos previos congelados como contexto
- Documentos generados:
  - base para Buyer Curiosity Engine V1
- Responsable: Direccion + Comercial + Producto
- Fecha: 2026-07-15
- Criterios de aceptacion:
  - El modelo explica causalidad, transicion, conflicto, poder y retroalimentacion
  - Los nodos se expresan primero en lenguaje neutral de mercado
  - Las afirmaciones estan separadas de las hipotesis
  - El resultado alimenta directamente el siguiente sprint

## Estándar epistemológico

| Tag | Significado | Uso |
| --- | --- | --- |
| FACT-PICC | Evidencia real proveniente de PICC | Solo cuando exista trazabilidad interna |
| FACT-EXT | Evidencia externa verificable | Solo cuando la fuente sea observable |
| PARTIAL | Evidencia parcial o indirecta | Usable como indicio, no como cierre |
| INFERENCE | Inferencia razonada | Requiere validacion posterior |
| HYPOTHESIS | Hipotesis pendiente de validacion | No tratar como hecho |
| UNKNOWN | Informacion faltante | Debe investigarse |

## Tesis central
Una oportunidad comercial nace, avanza, se bloquea o se reactiva por cambios en riesgo percibido, poder interno, disponibilidad de evidencia y velocidad de circulacion de informacion.

## 1. Trigger Graph

### Canon de triggers observables

| Trigger ID | Nombre | Dominio | Tipo | Descripcion | Actor que lo detecta | Actor afectado | ICP relacionado | Urgencia | Severidad | Impacto potencial | Decision que activa | Evidencia observable | Tiempo de reaccion | Probabilidad de proyecto | Senales publicas | Senales privadas | Canal donde puede detectarse | Estado epistemologico | Fuente requerida |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| TRG-001 | Caida operacional | Operativo | Incidente | Caida que interrumpe continuidad o servicio | Operaciones | Direccion / TI / Produccion | H01-H04 | Alta | Critica | Proyecto correctivo o preventivo | Corregir, redisenar o invertir | ticket, incidente, SLA roto | Horas o dias | Alta | downtime visible, quejas, retraso | llamada interna, correo, WhatsApp | internos + comites | INFERENCE | PICC audit + entrevistas |
| TRG-002 | Microparos recurrentes | Operativo | Degradacion | Paros breves acumulados que revelan fragilidad | Operaciones | Dueño tecnico | H02-H04 | Alta | Alta | Proyecto de modernizacion | Aumentar resiliencia | logs, scrap, OEE | Dias o semanas | Media-alta | patrones de falla | reuniones operativas | operacion + hojas de calculo | INFERENCE | historial de incidentes |
| TRG-003 | Perdida de redundancia | Operativo | Obsolescencia | Eliminacion de respaldo o N+1 efectivo | Dueño tecnico | Sponsor | H01-H02 | Alta | Critica | Proyecto urgente | Restaurar redundancia | mantenimiento diferido, equipo obsoleto | Horas o dias | Alta | equipos fuera de vida | memorias internas | reuniones + auditorias | HYPOTHESIS | asset inventory |
| TRG-004 | Auditoria interna | Operativo | Auditoria | Revisa continuidad, cumplimiento o capacidad | Compliance | Direccion | H01-H06 | Media-alta | Alta | Proyecto de cumplimiento | Cerrar brecha detectada | hallazgos, no conformidades | Dias a semanas | Media | agenda de auditoria | checklist interno | auditoria | FACT-EXT | informe de auditoria |
| TRG-005 | Expansion de capacidad | Estrategico | Crecimiento | Incremento de carga, usuarios o metros | Direccion | Operaciones | H01-H04 | Alta | Alta | Proyecto nuevo | Ampliar infraestructura | plan de crecimiento, forecast | Semanas | Alta | anuncio, plan capex | junta directiva | comites + presentaciones | INFERENCE | plan estrategico |
| TRG-006 | Nearshoring | Estrategico | Mercado | Entrada de nuevas operaciones por relocalizacion | Direccion | Desarrollo / Operaciones | H02-H04 | Media-alta | Alta | Proyecto nuevo | Preparar infraestructura | expansion industrial regional | Meses | Media-alta | prensa, anuncios | conversaciones con consultores | prensa + asociaciones | FACT-EXT | fuentes sectoriales |
| TRG-007 | Nuevo cliente ancla | Estrategico | Ingreso | Cliente grande fuerza capacidad o SLA | Comercial / Direccion | Operaciones | H02-H05 | Alta | Alta | Proyecto nuevo | Aumentar capacidad | contrato, demanda nueva | Semanas | Alta | anuncio comercial | pipeline interno | CRM + comites | HYPOTHESIS | CRM y propuestas |
| TRG-008 | Fusión o adquisicion | Estrategico | Cambio de ownership | Reordena prioridades y arquitectura | Direccion | Finanzas / TI | H01-H05 | Alta | Alta | Proyecto o pausa | Unificar o consolidar | comunicados, integration plan | Semanas a meses | Media | prensa financiera | reuniones cerradas | prensa + board | FACT-EXT | comunicado corporativo |
| TRG-009 | Nueva norma | Regulatorio | Cambio regulatorio | Ajusta requisitos de continuidad o seguridad | Compliance | Dueño tecnico | H01-H06 | Media-alta | Alta | Proyecto de cumplimiento | Adecuar instalaciones | norma publicada | Dias a meses | Media-alta | boletines regulatorios | interpretacion interna | organismos + consultoria | FACT-EXT | texto normativo |
| TRG-010 | Requerimiento de cliente | Regulatorio | Contrato | Cliente pide certificacion, nivel o evidencia | Comercial | Sponsor / legal | H01-H04 | Alta | Alta | Proyecto habilitador | Cumplir requisito | RFP, SOW, anexos | Dias o semanas | Alta | solicitud formal | correo, RFP, junta | propuesta + contrato | FACT-PICC | requerimiento comercial |
| TRG-011 | Aumento de costo energetico | Financiero | Presion economica | Sube costo de operar continuidad | Finanzas | Direccion | H01-H04 | Media-alta | Alta | Proyecto de eficiencia | Redisenar consumo | facturas, forecast | Semanas | Media-alta | alza tarifas | modelo financiero interno | Finanzas + comites | FACT-EXT | tarifas y facturas |
| TRG-012 | Presion de margen | Financiero | Presupuesto | Menor margen obliga a postergar o justificar | Finanzas | Sponsor | H02-H05 | Media | Alta | Proyecto o pausa | Posponer o priorizar | P&L, forecast | Semanas | Media | planes de austeridad | comites financieros | board + excel | INFERENCE | estado financiero |
| TRG-013 | Cambio de director | Humano/politico | Poder | Nuevo lider redefine agenda y veto | Direccion | Todos | H01-H06 | Alta | Alta | Reactivacion o bloqueo | Repriorizar | anuncio interno | Dias a semanas | Media-alta | rumor de cambio | reuniones politicas | comites + red interna | FACT-EXT | organigrama |
| TRG-014 | Crisis reputacional | Humano/politico | Crisis | Incidente visible acelera decision | Comunicacion / Direccion | Todos | H01-H06 | Alta | Critica | Proyecto urgente | Contener riesgo | prensa, redes, incidentes | Horas o dias | Alta | menciones publicas | conversaciones cerradas | medios + WhatsApp | FACT-EXT | prensa y monitoreo |
| TRG-015 | IA / automatizacion | Tecnologico | Transformacion | Mayor densidad o automatizacion exige capacidad | TI / Operaciones | Dueño tecnico | H01-H04 | Media | Alta | Proyecto de modernizacion | Modernizar arquitectura | roadmap de IA | Meses | Media | adopcion de IA | talleres internos | estrategia + TI | INFERENCE | roadmap tecnologico |
| TRG-016 | Incompatibilidad tecnica | Tecnologico | Fallo de arquitectura | Sistemas no se integran o colisionan | TI / Ingenieria | Dueño tecnico | H01-H04 | Alta | Alta | Proyecto correctivo | Sustituir o adaptar | incidentes, pruebas fallidas | Dias a semanas | Media-alta | error de integracion | QA interno | soporte tecnico | HYPOTHESIS | bitacora tecnica |

### Reglas de lectura
- Un trigger puede activar observacion, no necesariamente proyecto.
- El mismo trigger puede reactivarse si el contexto cambia.
- La misma organizacion puede tener triggers simultaneos con prioridades distintas.

## 2. Stakeholder Graph

| Stakeholder ID | Rol organizacional | Funcion dentro de la oportunidad | Objetivos | KPI | Incentivos | Miedos | Riesgo personal | Riesgo profesional | Poder formal | Influencia informal | Capacidad de veto | Lenguaje preferido | Informacion requerida | Evidencia creible | Criterio de exito | Criterio de rechazo | Canal preferido | Etapa de mayor influencia | Relacion con otros actores | Estado epistemologico |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| STK-001 | Iniciador | Detona la conversacion | Resolver dolor o oportunidad | tiempo de respuesta | agilidad, visibilidad | ser ignorado | bajo | medio | baja | media | baja | simple, practico | primera respuesta | caso comparable | abrir la conversacion | ser desestimado | WhatsApp/email | Inicio | sponsor temprano | HYPOTHESIS |
| STK-002 | Usuario | Vive el impacto diario | Continuidad y facilidad de uso | uptime, facilidad | menos friccion | interrupciones | medio | medio | baja | media | baja | tecnico-operativo | como cambia su trabajo | demostracion funcional | que le simplifique operacion | mas complejidad | reunion/visita | Exploracion | dueño tecnico | INFERENCE |
| STK-003 | Dueño tecnico | Define viabilidad tecnica | Resiliencia y compatibilidad | disponibilidad, MTTR | control tecnico | mala arquitectura | medio | alto | alta | media | media | tecnico | limites, supuestos, riesgos | planos, pruebas, casos | que la solucion funcione | riesgos ocultos | reunion tecnica | Definicion | usuario + proveedor + integrador | INFERENCE |
| STK-004 | Sponsor | Empuja el proyecto | Avance estrategico | avance de comite | logro, rapidez | quedar mal ante direccion | alto | alto | media | alta | media | ejecutivo | impacto, riesgo, costo | board pack, benchmark | aprobar y avanzar | incertidumbre alta | correo, presentacion | Caso interno | evaluador + finanzas | HYPOTHESIS |
| STK-005 | Beneficiario | Recibe el resultado | Mejor desempeño operativo | OEE, continuidad | mejora real | ser excluido | bajo | medio | baja | media | baja | operativo | como le afecta | casos, before/after | mejora tangible | impacto nulo | reunion | Ejecucion | usuario | PARTIAL |
| STK-006 | Influencer | Orienta la opinion | Calidad de la decision | recomendaciones aceptadas | reputacion tecnica | perder credibilidad | medio | medio | baja | alta | media | tecnico/referencial | comparables | referencias, benchmarks | que su recomendacion sea valida | sesgo de proveedor | reuniones, llamadas | Shortlist | sponsor/dueño tecnico | INFERENCE |
| STK-007 | Evaluador | Compara opciones | Reducir riesgo y sesgo | score de comparacion | rigor | elegir mal | medio | alto | media | media | media | comparativo | trade-offs | matrices, propuestas, casos | opcion defendible | inconsistencia | PDF, spreadsheet | Shortlist | sponsor + compras | HYPOTHESIS |
| STK-008 | Compras | Controla proceso | Cumplimiento y precio | cumplimiento, ahorro | control | sobreprecio | medio | alto | alta | media | alta | contractual | alcance, precio, terminos | propuesta clara | expediente completo | ambiguedad | email/PDF | Aprobacion | legal + finanzas | INFERENCE |
| STK-009 | Finanzas | Custodia presupuesto | Riesgo financiero defendible | ROI, payback | disciplina | CAPEX injustificado | alto | alto | alta | media | alta | economico | costo total, sensibilidad | modelo financiero | aprobacion defendible | payback debil | board pack | Caso interno | sponsor + compras | INFERENCE |
| STK-010 | Juridico | Revisa riesgo legal | Contrato y responsabilidad | exposicion legal | control | clausulas malas | medio | alto | media | media | media | legal | terminos, permisos, claims | contrato, permisos | riesgo acotado | ambiguedad contractual | PDF/email | Revisión | compras + sponsor | PARTIAL |
| STK-011 | Compliance | Valida cumplimiento | Cerrar brechas normativas | hallazgos cerrados | reputacion institucional | sancion | alto | alto | media | media | media | normativo | norma y evidencias | auditoria, certificados | cumplimiento | brecha abierta | auditoria | Definicion | juridico + tecnico | FACT-EXT |
| STK-012 | Seguridad | Minimiza incidentes | Continuidad segura | incidentes, hallazgos | proteccion | pérdida de control | alto | alto | media | media | media | riesgo/operativo | riesgos, controles | checklists, incidentes | seguro y estable | vulnerabilidad | reunion | Definicion | operativo + compliance | INFERENCE |
| STK-013 | Aprobador | Da el si final | Balance riesgo/retorno | decision final | cierre | equivocarse | alto | muy alto | alta | alta | alta | ejecutivo | resumen, opciones | board pack, comparables | aprobar | dudas persistentes | comité | Cierre | sponsor, finanzas, jurídico | INFERENCE |
| STK-014 | Firmante | Formaliza compromiso | Cerrar contrato | contrato firmado | avance | responsabilidad contractual | alto | muy alto | alta | media | alta | contractual | clausulas, alcance | contrato final | firmar | riesgo no cerrado | firma | Contratación | compras + legal | INFERENCE |
| STK-015 | Pagador | Libera recursos | Asegurar valor por dinero | desembolso | control presupuestal | gasto improductivo | alto | alto | alta | media | alta | financiero | presupuesto, hitos | ROI, hitos, riesgo | desembolsar | incertidumbre alta | comite financiero | Aprobacion | sponsor + compras | INFERENCE |
| STK-016 | Bloqueador | Frenar proyecto | Evitar error o carga | no avanzar | protegerse | pérdida de control | alto | medio | media | alta | alta | critico | riesgos, evidencia | comparables, límites | no generar daño | exceso de riesgo | reuniones cerradas | Cualquier etapa | veto | INFERENCE |
| STK-017 | Veto | Detener decision | Bloquear por riesgo | ninguna | defensa institucional | quedar expuesto | alto | muy alto | alta | alta | alta | politico/ejecutivo | incertidumbre, compliance | evidencia fuerte | retirar veto | alarma o debilidad | comite | Aprobacion | aprobador + jurídico | HYPOTHESIS |
| STK-018 | Operador posterior | Operar la solucion | Estabilidad postproyecto | uptime, facilidad | continuidad | complejidad operativa | medio | alto | baja | media | baja | operativo | manuales, soporte | evidencias de operación | operar sin sorpresas | diseño inmanejable | correo/reunión | Ejecucion | usuario + tecnico | PARTIAL |

## 3. Buying Committee Graph

### Secuencia tipica de incorporacion
1. Iniciador detecta problema o trigger.
2. Dueño tecnico valida si el problema es real.
3. Sponsor decide si merece caso interno.
4. Finanzas entra cuando aparece presupuesto o sensibilidad de inversión.
5. Compras entra cuando el proceso formal se activa.
6. Juridico y compliance aparecen cuando hay contrato, riesgo o evidencia sensible.
7. Aprobador y firmante intervienen al cierre.
8. Operador posterior valida la factibilidad de operación.

### Cambios de poder por etapa
- Inicio: domina el iniciador o el dueño tecnico.
- Definicion: domina el dueño tecnico.
- Caso interno: domina el sponsor.
- Shortlist: domina evaluador + compras.
- Revisión financiera: domina finanzas.
- Revisión legal/compliance: domina jurídico y compliance.
- Cierre: domina aprobador/firmante.
- Postproyecto: domina operador posterior.

### Conflictos tipicos
- Sponsor quiere avanzar; finanzas quiere postergar.
- Dueño tecnico quiere la mejor arquitectura; compras empuja a menor precio.
- Compliance exige evidencia; comercial quiere velocidad.
- Operador posterior pide simplicidad; aprobador pide reducción de riesgo.

### Materiales que circulan
- Notas de reunion.
- Hojas de calculo.
- PDFs comparativos.
- Board pack.
- Propuestas.
- Matrices de riesgo.
- Evidencia tecnica.
- Correos con aprobaciones.

### Informacion que no circula facilmente
- Riesgos politicos internos.
- Que actor tiene el veto real.
- Costo de equivocacion personal.
- Preferencias ocultas por proveedor.
- Dudas tecnicas no admitidas en publico.

## 4. Opportunity Lifecycle

| Estado | Definicion | Entrada | Salida | Trigger de transicion | Actor dominante | Decision | Incertidumbre | Riesgo | Evidencia | Informacion | Tiempo estimado | Senal de avance | Senal de estancamiento | Senal de muerte | Senal de reactivacion | Superficie relevante | Intervencion comercial posible | Razon de perdida | Dato requerido |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 Riesgo tolerado | El riesgo existe pero se acepta | estado normal | señal latente | nuevo stress | sponsor o dueño tecnico | seguir igual | baja | acumulacion silenciosa | historico | operacion | variable | rutina | normalizacion | ningun cambio | incidente externo | interna | ninguna | inercia | baseline |
| 2 Señal latente | Hay friccion pero no nombre | ruido operativo | trigger detectado | observacion repetida | usuario/dueño tecnico | prestar atencion | media | subestimacion | indicios | reuniones, logs | dias-semanas | preguntas nuevas | ignora patron | desaparece | detecta aumento | meetings | diagnostico ligero | no se reconoce | frecuencia |
| 3 Trigger detectado | Evento observables cambia urgencia | señal latente | problema reconocido | incidente, norma, costo | quien detecta | abrir tema | media-alta | escalamiento | evidencia inicial | correo, WhatsApp | horas-dias | alarma | se oculta | se resuelve solo | nueva alarma | omnicanal | alerta/triage | se minimiza | tipo trigger |
| 4 Problema reconocido | Se nombra la friccion | trigger | exploracion informal | consenso preliminar | dueño tecnico | explorar | alta | costo visible | síntoma y contexto | reunión | dias | lenguaje comun | ambiguedad | negacion | repeticion | reunion | conversacion | no hay sponsor | caso comparables |
| 5 Exploracion informal | Se buscan opciones sin proceso | problema | definicion preliminar | curiosidad del sponsor | sponsor | entender alcance | alta | elegir mal | notas, referencias | calls, LinkedIn, IA | dias-semanas | mas preguntas | falta de foco | se diluye | presión externa | IA/reunion | orientacion | sin owner | mapa actores |
| 6 Definicion preliminar | Se delimita el problema | exploracion | caso interno | workshop / due diligence | sponsor + dueño técnico | priorizar | media-alta | sesgo de alcance | boceto de alcance | talleres | dias-semanas | alcance explicitado | indefinicion | se archiva | nueva evidencia | workshop | discovery | requisitos difusos | definicion |
| 7 Caso interno | Se arma narrativa interna | definicion | presupuesto posible | sponsor decide llevar | sponsor | justificar | alta | rechazo interno | memo, costos | board pack | dias-semanas | sponsor activo | ausencia de defensa | muere en comité | cambio de poder | board pack | business case | no defendible | ROI/TCO |
| 8 Presupuesto posible | Hay espacio presupuestal | caso interno | requisitos en construcción | ciclo capex | finanzas | reservar recursos | alta | recorte | presupuesto, forecast | excel | semanas | espacio asignado | congelamiento | corte presupuestal | mejora financiera | reunión | ajuste financiero | presupuesto insuficiente | capex |
| 9 Requisitos en construcción | Se afinan condiciones | presupuesto | búsqueda de alternativas | alineación técnica | dueño tecnico | definir requerimientos | alta | mal planteo | criterios, restricciones | docs, reuniones | semanas | criterios claros | requisitos vagos | se reemplaza | cliente nuevo | reunión | moldear oferta | requisito incoherente | criterios |
| 10 Búsqueda de alternativas | Se comparan caminos | requisitos | longlist | búsqueda activa | evaluador + compras | comparar | alta | shortlist sesgada | comparables | internet, proveedores | dias-semanas | mas proveedores | comparacion superficial | proceso dirigido | evidencia nueva | web/IA | comparativa | no existe mercado | alternativas |
| 11 Longlist | Lista amplia de opciones | busqueda | shortlist | filtrado inicial | evaluador | filtrar | media | overload | fichas | propuestas | dias | lista controlable | demasiadas opciones | cae por inercia | mayor claridad | PDF/Excel | pre-calificacion | falta fit | criterios |
| 12 Shortlist | Opciones finales | longlist | diagnostico | invitacion a diagnostico | sponsor + tecnico | elegir finalistas | media-alta | error de elección | casos, referencias | reuniones | dias | 2-3 opciones | comparación paralizada | excluido | nueva evidencia | reuniones | diagnostico | falta confianza | evidence pack |
| 13 Diagnostico | Se profundiza y valida | shortlist | propuesta | workshop técnico | dueño técnico | validar capacidad | alta | alcance falso | discovery, site visit | sesiones | dias-semanas | precisión | evasivas | abandono | evidencia fuerte | visita/taller | consultivo | falta claridad | diagnóstico |
| 14 Propuesta | Se presenta solución | diagnostico | revision tecnica | envío de propuesta | comercial | avanzar | alta | propuesta débil | alcance/costo | PDF | dias | revisión formal | demora | no se revisa | urgencia | proposal | apoyo comercial | confusa | alcance |
| 15 Revisión técnica | Se prueba factibilidad | propuesta | revisión financiera | técnico acepta | dueño técnico | aceptar arquitectura | alta | fallos técnicos | planos, supuestos | meetings | dias-semanas | preguntas concretas | silencio | rechazo | respuesta sólida | técnica | clarificación | falta detalle | supuestos |
| 16 Revisión financiera | Se prueba el caso económico | tecnica | aprobación | finanzas valida | finanzas | aprobar inversión | alta | no cierra ROI | ROI/TCO | excel | dias-semanas | sensibilidad aceptada | recortes | no pasa | presupuesto liberado | board pack | defensa económica | payback débil | modelo |
| 17 Aprobación | Decisión final interna | financiera | negociación | acuerdo ejecutivo | aprobador | autorizar | alta | responsabilidad | paquete final | comité | dias | si condicionado | devolucion | cae | legitimidad reforzada | comité | cierre | veto | evidencia final |
| 18 Negociación | Se ajustan terminos | aprobación | contratación | terminos aceptados | compras/legal | cerrar contrato | media | retraso | contrato | llamadas/correos | dias-semanas | ultimato | fricción | ruptura | concesion | correo/contrato | cierre | clausulas | terminos |
| 19 Contratación | Firma y compromiso | negociación | pausa o ejecucion | firma final | firmante | comprometerse | alta | incumplimiento | contrato | PDF/firma | dias | contrato firmado | firma lenta | cancelacion | firma nueva | contrato | onboarding | riesgo legal | firma |
| 20 Pausa | Se congela temporalmente | cualquier anterior | reactivación / pérdida | crisis interna | sponsor | esperar | alta | olvido | estado del proyecto | reuniones | dias-semanas | reactivación de sponsor | silencio | muerte | trigger nuevo | internal | seguimiento | otras prioridades | owner |
| 21 Congelamiento | Pausa larga sin cierre | pausa | pérdida o reactivación | cambio de contexto | sponsor | suspender | media | oportunidad muerta | no avance | correo | semanas-meses | reactivación | no hay contacto | muerto | nueva crisis | email | reengage | presupuesto | evento nuevo |
| 22 Pérdida | Se pierde la oportunidad | cualquier | cierre negativo | decisión contraria | sponsor/comité | abandonar | alta | pérdida de pipeline | reason lost | CRM | dias | reason recorded | desinterés | fin | nuevo patrocinador | CRM | win/loss | precio/riesgo | motivo pérdida |
| 23 Cancelación | Se elimina el proyecto | cualquier | cierre total | cambio estratégico | dirección | abortar | alta | desperdicio | stop memo | board | dias | cierre formal | archivo | fin | nueva necesidad | board | win/loss | no prioridad | motivo |
| 24 Reactivación | Regresa un proyecto pausado | pausa/congelamiento | ejecución | nuevo trigger | sponsor | reabrir | alta | repetición de problemas | nueva evidencia | reuniones | dias-semanas | nueva reunión | tibio | no retorna | nueva urgencia | internal | reengage | trigger cambiado | señal |
| 25 Ejecución | Se implementa la solución | contratación | evaluación | inicio de obra | operador posterior | operar bien | alta | ejecución fallida | avance, hitos | reuniones, reportes | semanas-meses | hitos cumplidos | atraso | falla | seguimiento | obra | soporte | desviación | avance |
| 26 Evaluación | Se mide resultado | ejecución | expansión | review post | sponsor + operador | validar éxito | media | arrepentimiento | desempeño | KPI | semanas-meses | KPIs mejoran | dudas | no valor | evidencia positiva | dashboard | postventa | valor no capturado | KPI |
| 27 Expansión | Se amplía alcance | evaluación | referencia | mejora comprobada | sponsor | escalar | media-alta | sobrecarga | lessons learned | comites | meses | nuevas fases | estancamiento | no escala | caso fuerte | board/comite | upsell | sin confianza | desempeño |
| 28 Referencia | Se vuelve ejemplo | expansión | nueva oportunidad | permiso y aprendizaje | sponsor/usuario | recomendar | media | reputación | testimonio/caso | redes, referidos | meses | nueva demanda | aislado | no referencia | nueva consulta | public/partners | referral | permiso | autorización |

## 5. Trust Lifecycle

| Evento | Etapa afectada | Actor afectado | Severidad | Reversibilidad | Costo de recuperacion | Evidencia | Accion preventiva | Accion correctiva |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Evidencia verificable | cualquier | sponsor/tecnico | positiva | alta | bajo-medio | caso, dato, permiso | documentar | reforzar con comparables |
| Respuesta rapida | inicio | iniciador | positiva | alta | bajo | SLA | SLA claro | disculpa y respuesta |
| Diagnostico preciso | exploracion | dueño tecnico | positiva | alta | medio | assessment | discovery robusto | aclarar supuestos |
| Claridad de limites | validacion | legal/finanzas | positiva | alta | bajo | alcance y exclusiones | definir limites | corregir expectativas |
| Caso comparable | shortlist | evaluador | positiva | media-alta | medio | caso E4 | levantar casos | explicar contexto |
| Transparencia | aprobacion | aprovador | positiva | alta | medio | riesgos y limites | disclosure | aclarar gaps |
| Consistencia | todo | todos | positiva | alta | bajo | mismo mensaje | governance | corregir textos |
| Referencia | validacion | sponsor | positiva | media | medio | autorizacion | pedir permiso | formalizar referencia |
| Cumplimiento | contratacion | juridico/compliance | positiva | media | medio | permisos y contratos | legal review | rectificar contrato |
| Seguimiento | ejecucion | operador | positiva | alta | medio | hitos y reportes | cadencia | recuperar ritmo |
| Claim cuestionado | validacion | sponsor/tecnico | negativa | media | alto | inconsistencias | auditar | corregir o retirar |
| Inconsistencia multilenguaje | validacion | tecnico | negativa | media | alto | versiones distintas | control de version | unificar copy |
| Fotografia de stock | autoridad | tecnico | negativa | media | medio | imagenes stock | fotos reales | reemplazo |
| Logo sin permiso | legal | juridico | negativa | media | alto | falta autorizacion | permiso escrito | retirar logo |
| Dato inflado | aprobacion | finanzas | negativa | media-baja | alto | cifras sin fuente | registry | rectificar numero |
| Respuesta tardia | inicio | iniciador | negativa | media | medio | SLA fallido | SLA operativo | seguimiento |
| Propuesta confusa | revision | evaluador | negativa | media | medio | alcance ambiguo | plantilla clara | refactorizar |
| Sobrepromesa | validacion | aprobador | negativa | media | alto | claim absoluto | limitar lenguaje | retractar |
| Error tecnico | ejecucion | operador | negativa | media | alto | incidente | QA | correccion |
| Cambio de alcance opaco | negociacion | compras/legal | negativa | media | medio-alto | change order | control de cambios | re-explicar |
| Silencio | cualquier | sponsor | negativa | media | medio | no respuesta | follow-up | reengage |
| Falta de owner | cualquier | todos | negativa | media | medio | ausencia responsable | owner claro | reasignar |
| Evidencia insuficiente | shortlist/aprobacion | sponsor/finanzas | negativa | alta | alto | gaps | evidence pack | completar evidencia |

## 6. Information Flow Map

| Flujo | Origen | Receptor | Intermediario | Formato | Momento | Credibilidad | Distorsion posible | Decision impactada | Riesgo | Oportunidad para PICC | Trazabilidad |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Busqueda inicial | Google | iniciador | algoritmo | results | latencia | media | SEO/noise | exploracion | sesgo | aparecer con marco util | baja |
| Consulta IA | IA conversacional | sponsor/tecnico | prompt | texto | exploracion | media-alta | alucinacion/resumen | comparacion | falsa precision | ser referencia | baja-media |
| Red profesional | LinkedIn | sponsor | contactos | post/DM | latencia a evaluacion | media | posicionamiento | shortlist | reputacion | autoridad | media |
| Video | YouTube | usuario/tecnico | creator | video | exploracion | media | simplificacion | aprendizaje | sesgo visual | explicacion de conceptos | media |
| Mensajeria | WhatsApp | iniciador/sponsor | chat | texto/audio | continuo | alta interna | resumen parcial | avance rápido | ambiguedad | seguimiento | baja |
| Correo | email | compras/legal/finanzas | hilo | texto/PDF | evaluación | media-alta | omision | aprobación | perdidas de contexto | formalizacion | alta |
| Reunión | reunion | comité | facilitador | verbal | definicion/aprobacion | media | memoria selectiva | caso interno | ruido politico | claridad y trust | media |
| Presentacion | deck | aprobador | sponsor | slides | caso interno | media-alta | sesgo narrativo | aprobacion | maquillaje | board pack | alta |
| Propuesta | PDF/propuesta | evaluador/compras | comercial | PDF | revision | media-alta | alcance opaco | contratacion | confusión | comparabilidad | alta |
| Hoja de calculo | Excel | finanzas/evaluador | analista | spreadsheet | revisión financiera | media-alta | supuestos ocultos | presupuesto | modelo fragil | decision economics | media |
| Comite | board | aprobador/veto | sponsor | verbal+docs | aprobacion | media | politica interna | firma | vetos | influir narrativa | media |
| Colegas | informal | usuario | par | verbal | exploracion | media | rumor | opinion | sesgo | inteligencia social | baja |
| Consultores | consultores | sponsor | externo | memo/call | exploracion | media-alta | dependencia | definicion | agenda externa | benchmark | media |
| Integradores | integradores | dueño tecnico | externo | reunión/PDF | evaluacion | media | sesgo proveedor | arquitectura | lock-in | partnership | media |
| Fabricantes | fabricantes | tecnico/compras | externo | datasheet | evaluacion | media-alta | marketing técnico | comparacion | overclaim | co-evidencia | media |
| Asociaciones | asociaciones | sponsor | red | evento/report | exploracion | media | sesgo reputacional | autoridad | peer pressure | posicionamiento | media |
| Organismos | organismos | compliance | regulador | norma | revisión | alta | interpretacion | cumplimiento | sanción | claridad | alta |
| Auditorias | auditorias | compliance/juridico | auditor | informe | revision | alta | hallazgos parciales | continuidad | brechas | oportunidad de diagnostico | alta |
| Eventos | evento | sponsor/tecnico | organizer | charla | exploracion | media | networking superficial | curiosidad | ruido | entrada inicial | media |
| Partners | partner | sponsor | aliado | referral | exploracion | media-alta | sesgo relacional | shortlist | dependencia | co-sell | media |
| Medios especializados | medio | sponsor | editor | articulo | exploracion | media | framing | opinion | reputacion | autoridad | media |

## 7. Influence Graph

| Nodo | Tipo de influencia | Alcance | Audiencia | Credibilidad | Intereses | Decisiones afectadas | Etapa | Conflicto potencial | Relacion con PICC | Oportunidad | Riesgo | Estado de evidencia |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Fabricantes | tecnico/comercial | medio-alto | tecnicos/compras | media-alta | vender componentes | comparacion, especificacion | exploracion a shortlist | sesgo de especificacion | indirecta | co-evidencia | lock-in | PARTIAL |
| Integradores | tecnico/operativo | medio | tecnico/compras | media | ganar alcance | shortlist, arquitectura | evaluacion | competencia directa | variable | referral/alianza | commoditizacion | HYPOTHESIS |
| Consultores | estrategico | alto | sponsor/comite | media-alta | influir agenda | definicion, aprobacion | exploracion a aprobacion | agenda propia | indirecta | autoridad | sesgo de recomendacion | PARTIAL |
| Certificadores | normativo | medio | compliance/tecnico | alta | validacion | cumplimiento | definicion | rigidez | indirecta | legitimar | retraso | FACT-EXT |
| Asociaciones | reputacional | medio | sponsor | media | visibilidad | exploracion | latente a evaluacion | ruido de marca | indirecta | acceso | superficialidad | PARTIAL |
| Universidades | tecnico | bajo-medio | tecnico | media | conocimiento | definicion | exploracion | lentitud | baja | marco | desconexion | HYPOTHESIS |
| Gobierno | regulatorio | alto | compliance/direccion | alta | cumplimiento | requisitos | revision | carga burocratica | indirecta | claridad | sancion | FACT-EXT |
| Medios especializados | reputacional | medio | sponsor | media | audiencia | exploracion | latente | framing | indirecta | autoridad | sobreexposicion | PARTIAL |
| Aseguradoras | economico/riesgo | medio | finanzas | media-alta | reducir riesgo | aprobacion | revision financiera | exigencia | indirecta | case for risk | costo | HYPOTHESIS |
| Financiadores | economico | medio | finanzas/direccion | media | retorno | aprobacion | caso interno | restriccion | indirecta | viabilidad | retraso | HYPOTHESIS |

## 8. Competitive Dynamics Map

### Factores de ganancia/perdida
- Relacion.
- Confianza.
- Incumbencia.
- Recomendacion.
- Marca.
- Especializacion.
- Evidencia.
- Precio.
- Claridad.
- Velocidad.
- Compliance.
- Capacidad financiera.
- Disponibilidad.
- Capacidad tecnica.
- Reduccion de riesgo.
- Propuesta.
- Negociacion.
- Politica interna.
- Proceso dirigido.

### Tipos de compra
- Por relacion.
- Por urgencia.
- Por licitacion.
- Por comite.
- Por proveedor incumbente.
- Por recomendacion.
- Por defensa reputacional.
- Por precio.
- Por especializacion.
- Por cumplimiento.
- Por disponibilidad inmediata.

### Patrones competitivos
- Competencia abierta: mayor comparacion, evidencia y precio.
- Proceso parcialmente dirigido: especificaciones y sesgos previos ya influyen.
- Proceso totalmente dirigido: decision práctica antes del RFP.
- Comparacion simulada: el proceso aparenta abierto pero ya existe favorito.
- Compra defensiva: se prioriza reducir culpa o riesgo percibido.
- Compra transformacional: se busca cambio de arquitectura o capacidad.

## 9. Behavioral Demand Flywheel

Trigger -> atencion -> curiosidad -> investigacion -> confianza -> conversacion -> oportunidad -> proyecto -> evidencia -> referencia -> nuevas señales -> nueva demanda.

### Salidas de cada vuelta
- Nuevos actores.
- Nuevas relaciones.
- Referencias.
- Evidencia.
- Datasets.
- Preguntas.
- Benchmarks.
- Comunidad.
- Autoridad.
- Partners.
- Oportunidades adyacentes.
- Expansion.

### Conexion con otros motores
- Knowledge Flywheel: convierte evidencia en aprendizaje reutilizable.
- Demand Engine: convierte aprendizaje en atraccion y conversion.
- Growth System: convierte oportunidad en ejecucion comercial.
- Commercial Operating Model: convierte oportunidad en trato y entrega.
- Buyer Curiosity Engine futuro: convierte curiosidad en inventario de preguntas y activos.

## 10. Behavioral risks
- Confundir interes con intencion.
- Exceso de confianza por una sola senal.
- Politica interna que invalida el caso tecnico.
- Silencio del sponsor por miedo al veto.
- Cambios de contexto que congelan el proyecto.
- Informacion incorrecta circulando como verdad.
- Evidencia insuficiente para comites complejos.

## 11. Behavioral hypotheses
- H1: La mayor parte del avance ocurre cuando un trigger crea riesgo visible para un sponsor.
- H2: La informacion tecnica por si sola no mueve el proyecto si no hay defensa interna.
- H3: La confianza cambia por ciclos y no por una sola interaccion.
- H4: El cuello de botella principal es la circulacion de informacion entre actores, no la disponibilidad del servicio.
- H5: La reactivacion ocurre cuando reaparece un trigger de alto costo o cambia el poder interno.

## 12. Information Gap Matrix

| Dato faltante | Comportamiento afectado | Decision bloqueada | Fuente | Owner | Metodo de obtencion | Esfuerzo | Prioridad | Fecha objetivo | Artefacto consumidor |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CRM historico | secuencia y razones de avance | priorizacion real | CRM | Comercial | export + limpieza | medio | alta | 2026-08-15 | MBM / Buyer Curiosity |
| Propuestas ganadas/perdidas | win/loss y comparacion | factores de victoria | propuestas | Comercial | muestreo documental | medio-alto | alta | 2026-08-15 | MBM / Decision Architecture |
| Razones de perdida | muerte y pausa | riesgo de abandono | CRM + entrevistas | Comercial | codificacion de perdidas | medio | alta | 2026-08-15 | MBM / Demand Engine |
| Duracion por etapa | tiempo de transicion | ciclos y friccion | CRM + reuniones | Comercial | analisis de timestamps | medio | alta | 2026-08-31 | MBM / Growth |
| Objeciones frecuentes | conversacion y veto | mensaje y evidencia | llamadas/correos | Comercial | codificacion de objeciones | medio | alta | 2026-08-31 | Buyer Curiosity Engine |
| Stakeholders reales | comite y veto | mapeo de influencia | entrevistas | Direccion | entrevistas estructuradas | medio | alta | 2026-08-31 | MBM |
| Permisos de uso | confianza y publicabilidad | uso de evidencia | juridico/terceros | Direccion | registro formal | medio | alta | 2026-08-15 | Trust / MBM |
| Analytics | flujo y conversion | surfaces efectivas | GA4/Search Console | Marketing | acceso tecnico | bajo-medio | media-alta | 2026-08-15 | MBM / Demand Engine |
| Comportamiento en IA | curiosidad y comparacion | surfaces emergentes | prompts reales | Comercial | entrevistas y observacion | medio | media | 2026-09-15 | Buyer Curiosity |
| Casos autorizados | confianza y comparabilidad | shortlist y aprobacion | clientes | Direccion | gestion de permiso | medio-alto | alta | 2026-08-31 | Trust / MBM |

## 13. Method of validation

### Fuentes y metodos
- Entrevistas internas.
- Entrevistas con clientes.
- Analisis de oportunidades ganadas.
- Analisis de oportunidades perdidas.
- Revision de correos.
- Analisis de propuestas.
- Analisis de tiempos por etapa.
- Entrevistas con partners.
- Observacion de procesos de compra.
- Fuentes externas y benchmark sectorial.

### Muestra minima sugerida
- 5-8 entrevistas internas.
- 5-8 entrevistas con clientes o exclientes.
- 10 oportunidades ganadas o perdidas codificadas.
- 10 propuestas revisadas.
- 10 correos o hilos de decision.
- 3 partners relevantes.

### Sesgos y limites
- Sesgo de recuerdo.
- Sesgo de exito.
- Sesgo de disponibilidad.
- Sesgo de cortesía.
- Sesgo de confirmacion.
- Limite: lo observado no equivale a todo el mercado.

### Criterios de confianza
- Alta: repeticion en varias fuentes y actores.
- Media: una fuente fuerte + confirmacion parcial.
- Baja: una sola observacion aislada.

## 14. Implicaciones para PICC

| Comportamiento relevante | Senal que PICC podria detectar | Momento de intervencion | Evidencia que deberia ofrecer | Surface apropiada | Actor objetivo | Capacidad requerida | Riesgo | Posible producto de conocimiento | Posible CTA |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Trigger operativo | incidente, microparo, auditoria | despues de la senal | comparables y diagnostico | LinkedIn, WhatsApp, reunion | dueño tecnico | diagnostico rapido | entrar tarde | scorecard / checklist | diagnostico |
| Trigger estrategico | expansion, nearshoring, nueva sede | antes del budget | roadmap, riesgo, capacidad | reportes, reuniones | sponsor | framing ejecutivo | sobrepromesa | brief ejecutivo | reunion |
| Trigger regulatorio | norma, inspeccion, certificacion | antes del deadline | cumplimiento y brecha | email, PDF, comite | compliance | claridad normativa | evidencia insuficiente | mapa regulatorio | revisión |
| Trigger financiero | capex, costo energia, downtime | en preparacion de presupuesto | ROI/TCO | board pack, Excel | finanzas | modelo economico | caso debil | calculadora/modelo | business case |
| Trigger humano/politico | cambio director, crisis reputacional | reactivacion o bloqueo | riesgo y control | correo, reunion | sponsor | lectura politica | veto oculto | memo ejecutivo | conversation |
| Trigger tecnologico | IA, densidad, incompatibilidad | evaluacion de arquitectura | limites, capacidad, riesgo | IA, PDF, reunion | tecnico | claridad tecnica | sesgo de proveedor | comparador | diagnóstico |

## 15. Integracion con Market Knowledge Map
- El Market Knowledge Map define dominios, problemas, riesgos y preguntas.
- El Market Behavior Map define transicion, poder, conflicto, informacion y cambio.
- Juntos explican que existe y como se mueve.
- Este artefacto alimenta el futuro Buyer Curiosity Engine sin crear preguntas todavia.

## 16. Recomendacion para PICC
- Detectar triggers antes que la competencia.
- Priorizar actores con mayor capacidad de veto.
- Intervenir con evidencia comparativa y no solo con discurso.
- Construir materiales para comites, no solo para individuos.
- Mapear pausas, congelamientos y reactivaciones como oportunidades reales.

## 17. Riesgos del modelo
- Sobreajuste a observaciones de PICC.
- Confundir hipótesis con hechos.
- Exceso de granularidad que ralentice uso.
- Falta de datos historicos para validar transiciones.
- Sesgo hacia triggers visibles y no silenciosos.

## 18. Preguntas abiertas
- ¿Qué triggers tienen mayor tasa de reactivacion?
- ¿Que actor domina realmente la narrativa por ICP?
- ¿Donde mueren mas oportunidades: antes de caso interno o en revision financiera?
- ¿Que informacion circula menos de la que deberia?
- ¿Que eventos de perdida de confianza son mas costosos?

## 19. Criterio de cierre
Este modelo es util si explica por que, cuando y como cambia el comportamiento de los actores, y no solo enumera participantes o etapas.
