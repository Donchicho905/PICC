# ICPs

## Ficha de Trazabilidad
- ID: DOC-013
- Estado: 🟡 En desarrollo
- Tipo: Buyer System - ICP Portfolio V1
- Objetivo: Formular hipotesis accionables de ICP para PICC sin presentar inferencias como hechos cerrados.
- Entradas:
  - DOC-002 (00_MASTER_PLAN/MASTER_PLAN_PICC_NEXT_V3.md)
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
  - RL-001 (02_VERDAD_COMERCIAL/RESEARCH_LEDGER.md)
  - DOC-007 (02_VERDAD_COMERCIAL/Auditoria_Sitio.md)
- Salidas:
  - Portafolio de ICPs como hipotesis
  - Matriz de priorizacion provisional
  - Recomendacion de ICPs para MVP
- Dependencias:
  - DOC-011 (03_MODELO_COMERCIAL/Customer_Journey.md)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Documentos consumidos:
  - 00_IMPLEMENTATION_REPORT.md
  - evidencia publica de https://picc.com.mx/
  - fuentes internas y externas leidas en este sprint
- Documentos generados:
  - DOC-014 (03_MODELO_COMERCIAL/Modelo_Comercial.md)
  - DOC-020 (05_PRODUCTO/Capability_Model.md)
- Responsable: Direccion Comercial + Producto
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Hipotesis explicitas y etiquetadas epistemologicamente
  - Priorizacion provisional defendible
  - Ningun ICP presentado como verdad definitiva sin evidencia suficiente

## Regla epistemologica

Usar estas etiquetas en todo el Buyer System V1:

- Hecho verificado: corroborado en fuente primaria observada en este sprint.
- Evidencia parcial: existe una señal real, pero no alcanza para cerrar decision definitiva.
- Hipotesis: inferencia de trabajo util, no validada todavia.
- Informacion faltante: dato critico no accesible, no estructurado o inexistente en este sprint.

## Fuentes utilizadas para construir ICP Portfolio V1

| Fuente                                       | Acceso     | Fecha observada | Owner o custodio                    | Confiabilidad | Limitaciones                                                            | Datos personales o confidenciales |
| -------------------------------------------- | ---------- | --------------- | ----------------------------------- | ------------- | ----------------------------------------------------------------------- | --------------------------------- |
| `https://picc.com.mx/`                       | Disponible | 2026-07-15      | Owner digital no registrado en repo | Media         | Sin Analytics, Search Console ni snapshot versionado interno            | No evidente; informacion publica  |
| `02_VERDAD_COMERCIAL/Auditoria_Sitio.md`     | Disponible | 2026-07-15      | PICC repo                           | Alta          | Piloto metodologico, no evidencia comercial exhaustiva                  | No                                |
| `02_VERDAD_COMERCIAL/RESEARCH_LEDGER.md`     | Disponible | 2026-07-15      | PICC repo                           | Alta          | Estado de investigacion, no CRM real                                    | No                                |
| `00_MASTER_PLAN/MASTER_PLAN_PICC_NEXT_V3.md` | Disponible | 2026-07-15      | PICC repo                           | Media         | Documento estrategico, no prueba de mercado por si mismo                | No                                |
| `rocablocks_email_body.json`                 | Disponible | 2026-06-16      | Pablo / proveedor externo           | Alta          | Es un caso puntual de abastecimiento, no cartera completa               | Si                                |
| `rocablocks_cotizacion_text.txt`             | Disponible | 2026-06-16      | Pablo / proveedor externo           | Alta          | Caso puntual y centrado en compra de materiales                         | Si                                |
| `ICOMMERCE/README.md`                        | Disponible | 2026-05-04      | APOLO / ZEUS                        | Media         | Proyecto de canal, no evidencia de cierre comercial de PICC             | No significativo                  |
| `ARISTOTELES_RESEARCH/CONTEXTO.md`           | Disponible | 2026-05-30      | ARISTOTELES                         | Media         | Solo referencia findings en `zeus.knowledge`; no se accedio a los facts | No                                |
| `BEGRAND_PARK/CONTEXTO.md`                   | Disponible | 2026-05-30      | DEDALO                              | Media         | Proyecto activo de diseno, no caso cerrado publicable                   | Puede contener datos de cliente   |
| `GOBERNANZA_PORTAFOLIO_2026-07-07.md`        | Disponible | 2026-07-07      | ATENEA / ZEUS                       | Media         | Portafolio global, no solo PICC; parte de la data es indirecta          | Si                                |

## Fuentes no disponibles en este sprint

- CRM historico de PICC.
- Analytics de `picc.com.mx`.
- Search Console.
- export de oportunidades ganadas y perdidas.
- cartera estructurada de clientes publicables.
- contratos y permisos de uso publicitario.
- facts detallados de `zeus.knowledge` sobre PICC.
- activos DAVINCI y BrickEye vinculados formalmente a compradores PICC.

## Portafolio de hipotesis ICP V1

| ICP ID  | Hipotesis de comprador                                                                                  | Soporte actual    | Comentario                                                                       |
| ------- | ------------------------------------------------------------------------------------------------------- | ----------------- | -------------------------------------------------------------------------------- |
| ICP-H01 | Responsable corporativo de infraestructura critica o Data Center                                        | Evidencia parcial | Fuerte alineacion con Home, certificaciones y mensaje principal del sitio        |
| ICP-H02 | Director o propietario de empresa industrial con necesidad de instalaciones criticas, electricas o HVAC | Evidencia parcial | Coherente con servicios industriales del sitio; falta cartera y cierres          |
| ICP-H03 | Responsable corporativo de oficinas, HQ o instalaciones comerciales                                     | Evidencia parcial | El sitio menciona oficinas y remodelaciones; faltan casos y pipeline             |
| ICP-H04 | Desarrollador inmobiliario mediano                                                                      | Evidencia parcial | Hay señal real en BeGrand y actividad de obra/diseno; falta evidencia publicable |
| ICP-H05 | Propietario o inversionista con terreno o proyecto para detonar                                         | Evidencia parcial | Caso Bosque Esmeralda muestra demanda de proyecto puntual; falta repeticion      |
| ICP-H06 | Cliente privado de construccion o remodelacion de ticket significativo                                  | Hipotesis         | El sitio menciona residencial premium; falta evidencia estructurada              |

## Fichas de ICP

### ICP-H01 - Infraestructura critica y Data Centers

**Identidad comercial**
- ID: ICP-H01.
- Nombre funcional: Responsable corporativo de infraestructura critica o Data Center. [Evidencia parcial]
- Tipo de organizacion: empresa con operacion digital critica, corporativo intensivo en disponibilidad o desarrollador/operador de Data Center. [Hipotesis]
- Rol comprador: director de infraestructura, facilities, tecnologia o expansion. [Hipotesis]
- Influenciadores: operaciones, seguridad, IT, energia, procurement. [Hipotesis]
- Aprobadores: direccion general, finanzas, comite de inversion. [Hipotesis]
- Usuarios tecnicos: electricidad, HVAC, cableado, fire suppression, seguridad. [Hecho verificado]
- Posible bloqueador: compliance, procurement o responsable de riesgo. [Hipotesis]

**Situacion**
- Problema detonante: crecimiento de demanda digital, riesgo de continuidad, certificacion, ampliacion o adecuacion de infraestructura. [Hipotesis]
- Proyecto tipico: diseno, construccion o retrofit de Data Center e infraestructura critica. [Hecho verificado]
- Etapa de madurez: comprador con problema ya reconocido y necesidad de comparacion tecnica. [Hipotesis]
- Presupuesto o ticket: informacion faltante.
- Plazo: urgencia media a alta por continuidad o lanzamiento. [Hipotesis]
- Ubicacion: nacional e internacional segun Home. [Evidencia parcial]
- Restricciones: uptime, redundancia, certificacion, seguridad, aprobacion interna. [Evidencia parcial]

**Objetivo**
- Resultado economico: evitar caidas costosas y proteger retorno de infraestructura. [Hipotesis]
- Resultado operativo: continuidad y capacidad disponible. [Hipotesis]
- Resultado tecnico: cumplir estandar ICREA, energia, climatizacion y seguridad. [Evidencia parcial]
- Resultado personal o reputacional: defender una decision tecnica sin falla visible. [Hipotesis]

**Riesgos percibidos**
- costo, plazo, calidad, proveedor incorrecto, incertidumbre tecnica, aprobacion de comite, reputacion y operacion en curso. [Evidencia parcial]

**Criterios de compra**
- experiencia comparable, certificaciones, metodologia, cumplimiento, evidencia, especializacion y confianza personal. [Evidencia parcial]

**Señales**
- Señales de intencion: consulta sobre certificacion, redundancia, adecuacion critica, visita tecnica. [Hipotesis]
- Señales de urgencia: ampliacion inmediata, riesgo de downtime, auditoria o cumplimiento. [Hipotesis]
- Señales de buen fit: habla de criticidad, SLA, energia, climatizacion y seguridad. [Hipotesis]
- Señales de bajo fit: solo busca precio unitario sin riesgo critico asociado. [Hipotesis]
- Señales de abandono: el problema se relega a mantenimiento menor o se mueve a proveedor ultra especializado no EPC. [Hipotesis]

**Evidencia requerida**
- Inmediata: credenciales visibles, servicios, certificaciones. [Hecho verificado]
- Tecnica: casos comparables, metodologia, matrices de riesgo, estandares. [Informacion faltante]
- Economica: rango presupuestal, TCO, comparables de alcance. [Informacion faltante]
- Institucional: empresa, equipo, cobertura, trayectoria. [Evidencia parcial]
- Legal: permisos de uso de casos y certificaciones. [Informacion faltante]

### ICP-H02 - Industrial e instalaciones criticas

**Identidad comercial**
- ID: ICP-H02.
- Nombre funcional: Director o propietario de empresa industrial con necesidad de infraestructura, instalaciones electricas o climatizacion. [Evidencia parcial]
- Tipo de organizacion: planta, nave, operador logistico o empresa intensiva en instalaciones. [Hipotesis]
- Rol comprador: director general, operaciones, mantenimiento o proyectos. [Hipotesis]
- Influenciadores: mantenimiento, seguridad, compras, ingenieria. [Hipotesis]
- Aprobadores: direccion y finanzas. [Hipotesis]
- Usuarios tecnicos: obra civil, electrico, HVAC, cableado. [Hecho verificado]
- Posible bloqueador: compras por precio o proveedor actual. [Hipotesis]

**Situacion**
- Problema detonante: crecer capacidad, reconfigurar nave, rehabilitar instalaciones o reducir riesgo operativo. [Hipotesis]
- Proyecto tipico: nave, bodega, planta, electrico, HVAC, remodelacion industrial. [Hecho verificado]
- Etapa de madurez: suele llegar con necesidad operativa concreta y tiempo comprimido. [Hipotesis]
- Presupuesto o ticket: informacion faltante.
- Plazo: corto a medio. [Hipotesis]
- Ubicacion: Mexico, con sesgo probable CDMX/EdoMex por señales observadas. [Hipotesis]
- Restricciones: continuidad de operacion, seguridad, CAPEX y tiempos de paro. [Hipotesis]

**Objetivo**
- Resultado economico: ejecutar sin parar operacion o con minima afectacion. [Hipotesis]
- Resultado operativo: mejorar capacidad o confiabilidad. [Hipotesis]
- Resultado tecnico: instalaciones correctas, seguras y documentadas. [Hipotesis]
- Resultado personal o reputacional: no equivocarse con un contratista que comprometa produccion. [Hipotesis]

**Riesgos percibidos**
- plazo, calidad, incumplimiento, operacion en curso, seguridad, proveedor incorrecto. [Hipotesis]

**Criterios de compra**
- velocidad, especializacion, experiencia comparable, metodologia y confianza. [Hipotesis]

**Señales**
- intencion: solicitud de visita, revision de alcance, fotos o levantamiento. [Hipotesis]
- urgencia: obra condicionada por operacion, expansion o falla. [Hipotesis]
- buen fit: reconoce costo de interrupcion y busca integrador serio. [Hipotesis]
- bajo fit: compra solo commodity o requiere puro suministro. [Hipotesis]
- abandono: congela CAPEX o regresa a mantenimiento interno. [Hipotesis]

**Evidencia requerida**
- Inmediata: servicios industriales, electrico, HVAC, cobertura. [Hecho verificado]
- Tecnica: casos industriales, metodologia de obra en operacion, seguridad. [Informacion faltante]
- Economica: comparables de alcance y costo de interrupcion evitada. [Informacion faltante]
- Institucional: equipo multidisciplinario y trayectoria. [Evidencia parcial]
- Legal: permisos de uso de casos, seguridad y compliance. [Informacion faltante]

### ICP-H03 - Corporativo, oficinas e instalaciones comerciales

**Identidad comercial**
- ID: ICP-H03.
- Nombre funcional: Responsable corporativo de oficinas, HQ o instalaciones comerciales. [Evidencia parcial]
- Tipo de organizacion: corporativo, multi-site office, retail premium o empresa en reubicacion. [Hipotesis]
- Rol comprador: facilities, proyectos, administracion o direccion. [Hipotesis]
- Influenciadores: usuarios internos, RH, operaciones, IT, compras. [Hipotesis]
- Aprobadores: direccion, finanzas y comite interno. [Hipotesis]
- Usuarios tecnicos: facilities, electrico, climatizacion, cableado. [Hipotesis]
- Posible bloqueador: procurement o arrendador del inmueble. [Hipotesis]

**Situacion**
- Problema detonante: adecuacion, remodelacion, mudanza, crecimiento o correccion de instalaciones. [Hipotesis]
- Proyecto tipico: oficina, espacio comercial, remodelacion corporativa, cableado, climatizacion. [Hecho verificado]
- Etapa de madurez: reconoce necesidad, pero suele comparar varias alternativas. [Hipotesis]
- Presupuesto o ticket: informacion faltante.
- Plazo: medio, con ventanas cortas de ejecucion. [Hipotesis]
- Ubicacion: zonas corporativas urbanas. [Hipotesis]
- Restricciones: continuidad parcial de uso, imagen corporativa, aprobacion interna. [Hipotesis]

**Objetivo**
- Resultado economico: ejecutar sin sobrecostos fuertes. [Hipotesis]
- Resultado operativo: habilitar espacio funcional y utilizable rapido. [Hipotesis]
- Resultado tecnico: instalaciones correctas y acabado premium. [Hipotesis]
- Resultado personal o reputacional: entregar una solucion presentable y defendible. [Hipotesis]

**Riesgos percibidos**
- plazo, calidad, reputacion, proveedor incorrecto, comparabilidad de propuesta. [Hipotesis]

**Criterios de compra**
- experiencia comparable, velocidad, metodologia, presentacion y confianza. [Hipotesis]

**Señales**
- intencion: requiere visita, layout, alcances o propuesta. [Hipotesis]
- urgencia: fecha de ocupacion o contrato de arrendamiento. [Hipotesis]
- buen fit: valora ejecucion integral y coordinacion. [Hipotesis]
- bajo fit: solo compara precio por m2 sin valorar riesgo operativo. [Hipotesis]
- abandono: posterga mudanza o cambia de inmueble. [Hipotesis]

**Evidencia requerida**
- Inmediata: servicios comerciales y oficinas. [Hecho verificado]
- Tecnica: casos de remodelacion corporativa, tiempos y acabados. [Informacion faltante]
- Economica: rangos de alcance comparables. [Informacion faltante]
- Institucional: equipo y cumplimiento. [Evidencia parcial]
- Legal: permisos de uso de casos y testimonios. [Informacion faltante]

### ICP-H04 - Desarrollador inmobiliario mediano

**Identidad comercial**
- ID: ICP-H04.
- Nombre funcional: Desarrollador inmobiliario mediano. [Evidencia parcial]
- Tipo de organizacion: desarrollador, family office inmobiliario o vehiculo de proyecto. [Hipotesis]
- Rol comprador: director general, desarrollo, obra o socios. [Hipotesis]
- Influenciadores: arquitectura, costos, financiamiento, comercializacion. [Hipotesis]
- Aprobadores: socios, consejo, inversionistas. [Hipotesis]
- Usuarios tecnicos: arquitectura, estructural, MEP, obra. [Hipotesis]
- Posible bloqueador: uso de suelo, permisos, financiamiento o socios. [Hipotesis]

**Situacion**
- Problema detonante: evaluar viabilidad, disenar, cotizar o ejecutar un desarrollo o espacio amenity. [Evidencia parcial]
- Proyecto tipico: proyecto inmobiliario, amenity premium, urbanizacion o adecuacion de predio. [Evidencia parcial]
- Etapa de madurez: oscila entre idea, prefactibilidad y diseno. [Hipotesis]
- Presupuesto o ticket: informacion faltante.
- Plazo: medio a largo. [Hipotesis]
- Ubicacion: zonas metropolitanas y residenciales. [Evidencia parcial]
- Restricciones: permisos, mercado, preventa, inversion y aprobacion de socios. [Hipotesis]

**Objetivo**
- Resultado economico: maximizar retorno del proyecto. [Hipotesis]
- Resultado operativo: avanzar a diseno/costo/obra con menor incertidumbre. [Hipotesis]
- Resultado tecnico: definir un proyecto viable y ejecutable. [Hipotesis]
- Resultado personal o reputacional: evitar errores de direccion o proveedor. [Hipotesis]

**Riesgos percibidos**
- mercado, costo, plazo, permisos, proveedor incorrecto, aprobacion de comite o socios. [Hipotesis]

**Criterios de compra**
- experiencia comparable, lectura de negocio, confianza personal, capacidad integral. [Hipotesis]

**Señales**
- intencion: solicita conceptos, planos, catalogo, viabilidad o presupuestos. [Evidencia parcial]
- urgencia: presion de inversion, preventa o hito de proyecto. [Hipotesis]
- buen fit: busca acompanamiento tecnico-comercial, no solo mano de obra. [Hipotesis]
- bajo fit: ya llega con contratista cerrado y solo pide precio espejo. [Hipotesis]
- abandono: congela inversion, no responde o reorienta el producto. [Hipotesis]

**Evidencia requerida**
- Inmediata: experiencia en construccion y proyectos complejos. [Evidencia parcial]
- Tecnica: casos comparables, catalogos, planos, metodologia y capacidades. [Evidencia parcial]
- Economica: presupuesto preliminar, rango de costo y logica de faseo. [Informacion faltante]
- Institucional: equipo y trayectoria. [Evidencia parcial]
- Legal: permisos de publicacion, contratos y restricciones de uso. [Informacion faltante]

### ICP-H05 - Propietario o inversionista con terreno

**Identidad comercial**
- ID: ICP-H05.
- Nombre funcional: Propietario o inversionista con terreno o proyecto por detonar. [Evidencia parcial]
- Tipo de organizacion: persona fisica patrimonial, sociedad de inversion o familia. [Hipotesis]
- Rol comprador: dueno directo o representante del patrimonio. [Hipotesis]
- Influenciadores: familia, arquitecto, asesor financiero, asesor inmobiliario. [Hipotesis]
- Aprobadores: propietario o pequeno comite familiar. [Hipotesis]
- Usuarios tecnicos: arquitecto o asesor externo. [Hipotesis]
- Posible bloqueador: falta de definicion, presupuesto o confianza. [Hipotesis]

**Situacion**
- Problema detonante: quiere activar un terreno, jardin, predio o propiedad sin claridad total de alcance. [Evidencia parcial]
- Proyecto tipico: adecuacion, paisajismo, vivienda, amenity o desarrollo pequeño/mediano. [Evidencia parcial]
- Etapa de madurez: temprana a intermedia. [Hipotesis]
- Presupuesto o ticket: informacion faltante.
- Plazo: variable. [Hipotesis]
- Ubicacion: residencial o patrimonial. [Evidencia parcial]
- Restricciones: definicion incompleta, sensibilidad al costo, permisos y comparacion informal de proveedores. [Hipotesis]

**Objetivo**
- Resultado economico: que el proyecto agregue valor sin perder control del gasto. [Hipotesis]
- Resultado operativo: tener claridad de siguiente paso y alcance. [Hipotesis]
- Resultado tecnico: confirmar que lo que imagina es viable. [Hipotesis]
- Resultado personal o reputacional: no cometer un error caro con su patrimonio. [Hipotesis]

**Riesgos percibidos**
- proveedor incorrecto, sobrecosto, baja calidad, indefinicion tecnica. [Hipotesis]

**Criterios de compra**
- confianza personal, claridad, experiencia comparable y acompanamiento. [Hipotesis]

**Señales**
- intencion: pide cotizacion, referencias de material o visita. [Hecho verificado]
- urgencia: evento, entrega, decision patrimonial o ventana de obra. [Hipotesis]
- buen fit: reconoce que necesita guia y no solo precio. [Hipotesis]
- bajo fit: busca solo precio de material o compara commodity. [Hipotesis]
- abandono: silencio prolongado despues de cotizacion inicial. [Evidencia parcial]

**Evidencia requerida**
- Inmediata: contacto claro, propuesta de servicio y credenciales basicas. [Hipotesis]
- Tecnica: fotos, soluciones comparables, proceso y alcances. [Informacion faltante]
- Economica: rangos de inversion y escenarios. [Informacion faltante]
- Institucional: quien ejecuta y con que experiencia. [Evidencia parcial]
- Legal: contrato y condiciones. [Informacion faltante]

### ICP-H06 - Cliente privado high-ticket

**Identidad comercial**
- ID: ICP-H06.
- Nombre funcional: Cliente privado de construccion o remodelacion de ticket significativo. [Hipotesis]
- Tipo de organizacion: persona fisica con patrimonio alto o familia. [Hipotesis]
- Rol comprador: dueno, pareja o representante patrimonial. [Hipotesis]
- Influenciadores: arquitecto, interiorista, familia. [Hipotesis]
- Aprobadores: dueno y familia. [Hipotesis]
- Usuarios tecnicos: asesor externo. [Hipotesis]
- Posible bloqueador: sensibilidad reputacional, confianza y tiempos. [Hipotesis]

**Situacion**
- Problema detonante: quiere construir, remodelar o adecuar un espacio premium. [Hipotesis]
- Proyecto tipico: residencial premium o remodelacion integral. [Evidencia parcial]
- Etapa de madurez: desde idea hasta comparacion de propuestas. [Hipotesis]
- Presupuesto o ticket: informacion faltante.
- Plazo: medio. [Hipotesis]
- Ubicacion: residencial premium. [Hipotesis]
- Restricciones: privacidad, confianza, calidad y seguimiento cercano. [Hipotesis]

**Objetivo**
- Resultado economico: invertir bien sin sorpresas. [Hipotesis]
- Resultado operativo: resolver el proyecto con una sola contraparte confiable. [Hipotesis]
- Resultado tecnico: obtener calidad y detalle. [Hipotesis]
- Resultado personal o reputacional: tranquilidad y control del proceso. [Hipotesis]

**Riesgos percibidos**
- calidad, plazo, proveedor incorrecto, sobrecosto y reputacion. [Hipotesis]

**Criterios de compra**
- confianza personal, referencias, calidad visible, metodologia y atencion. [Hipotesis]

**Señales**
- intencion: solicita visita, propuesta o materiales. [Hipotesis]
- urgencia: evento, mudanza o necesidad familiar. [Hipotesis]
- buen fit: valora servicio integral y comunicacion. [Hipotesis]
- bajo fit: solo busca mano de obra barata o compra minima. [Hipotesis]
- abandono: largas pausas sin definicion ni presupuesto. [Hipotesis]

**Evidencia requerida**
- Inmediata: presencia, contacto y credenciales basicas. [Evidencia parcial]
- Tecnica: casos comparables, fotos, acabados y seguimiento. [Informacion faltante]
- Economica: rangos y escenarios de alcance. [Informacion faltante]
- Institucional: equipo y quien responde. [Evidencia parcial]
- Legal: contrato y privacidad. [Informacion faltante]

## Matriz de priorizacion provisional

| ICP     | Oportunidad potencial | Experiencia real observada | Evidencia disponible | Margen potencial | Probabilidad de cierre | Ciclo comercial | Capital de trabajo | Riesgo de ejecucion | Competencia | Facilidad de acceso | Capacidad operativa | Valor estrategico | Confianza del ranking |
| ------- | --------------------- | -------------------------- | -------------------- | ---------------- | ---------------------- | --------------- | ------------------ | ------------------- | ----------- | ------------------- | ------------------- | ----------------- | --------------------- |
| ICP-H01 | Alta                  | Media                      | Media                | Alta             | Media                  | Medio-largo     | Alto               | Alto                | Alta        | Media               | Media               | Muy alta          | Media                 |
| ICP-H02 | Alta                  | Media                      | Media-baja           | Media-alta       | Media                  | Medio           | Medio-alto         | Medio-alto          | Alta        | Media               | Media               | Alta              | Media-baja            |
| ICP-H03 | Media                 | Baja-media                 | Baja                 | Media            | Media-baja             | Medio           | Medio              | Medio               | Alta        | Media               | Media               | Media             | Baja                  |
| ICP-H04 | Alta                  | Media                      | Baja-media           | Alta             | Media-baja             | Largo           | Alto               | Alto                | Alta        | Baja-media          | Media               | Alta              | Baja                  |
| ICP-H05 | Media                 | Baja-media                 | Baja-media           | Media            | Baja-media             | Variable        | Medio              | Medio               | Media       | Media               | Media-baja          | Media             | Baja                  |
| ICP-H06 | Media                 | Baja                       | Baja                 | Media            | Baja-media             | Variable        | Medio              | Medio               | Alta        | Media               | Media-baja          | Baja-media        | Baja                  |

## Ranking provisional y recomendacion MVP

1. ICP-H01 - Infraestructura critica y Data Centers. [Confianza media]
2. ICP-H02 - Industrial e instalaciones criticas. [Confianza media-baja]
3. ICP-H04 - Desarrollador inmobiliario mediano. [Confianza baja]
4. ICP-H03 - Corporativo, oficinas e instalaciones comerciales. [Confianza baja]
5. ICP-H05 - Propietario o inversionista con terreno. [Confianza baja]
6. ICP-H06 - Cliente privado high-ticket. [Confianza baja]

### Recomendacion para MVP

**ICP prioritario 1**
- ICP-H01.
- Razon: es el unico perfil con alineacion explicita entre promesa publica, certificaciones visibles y especializacion declarada en Home.

**ICP prioritario 2**
- ICP-H02.
- Razon: aprovecha la misma base tecnica del sitio y puede capturar demanda mas amplia sin abandonar el eje de infraestructura critica.

**ICP de continuidad**
- ICP-H04.
- Razon: existe señal operativa real en el ecosistema, pero la evidencia publicable y la narrativa comercial todavia no son suficientes para ponerlo al frente del MVP.

## Investigaciones que pueden cambiar el ranking

- CRM y oportunidades historicas por tipo de cliente.
- proyectos ganados/perdidos por segmento.
- margen real por clase de proyecto.
- capital de trabajo requerido por segmento.
- razones de compra y abandono por ICP.
- permisos de publicacion para casos y testimonios.
- evidencia real de cierres en Data Centers, industrial y corporativo.

