# Capability Model

## Ficha de Trazabilidad
- ID: DOC-020
- Estado: 🟡 En desarrollo
- Tipo: Buyer System Capability Model V1
- Objetivo: Traducir ICPs, decisiones y brechas de evidencia en capacidades operables para el Growth System de PICC.
- Entradas:
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md)
  - DOC-011 (03_MODELO_COMERCIAL/Customer_Journey.md)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Salidas:
  - Portafolio de capacidades Buyer System V1
  - Priorizacion de capacidades
  - Owners y KPI iniciales
- Dependencias:
  - DOC-014 (03_MODELO_COMERCIAL/Modelo_Comercial.md)
- Documentos consumidos:
  - evidencia publica de `picc.com.mx`
  - fuentes internas y externas observadas en este sprint
- Documentos generados:
  - backlog de Growth System posterior
- Responsable: Producto + Comercial + Direccion
- Fecha: 2026-07-15
- Criterios de aceptación:
  - cada capacidad responde a una decision o brecha concreta
  - existe priorizacion razonable para ICP-H01 e ICP-H02
  - owners y KPI iniciales son visibles

## Principio de modelado

No modelar capacidades por area funcional abstracta, sino por friccion del comprador. Una capacidad vale si reduce incertidumbre, acelera avance o mejora defendibilidad comercial.

## Portafolio de capacidades V1

| Capacidad ID | Capacidad                            | Problema que resuelve                                          | ICPs foco          | Tipo                   | Estado V1    |
| ------------ | ------------------------------------ | -------------------------------------------------------------- | ------------------ | ---------------------- | ------------ |
| CAP-01       | Mensajeria sectorial priorizada      | la Home no habla con suficiente precision a cada comprador     | H01, H02, H03      | Contenido              | Parcial      |
| CAP-02       | Discovery y diagnostico por ICP      | no hay estructura repetible para entender alcance y decision   | H01, H02, H04, H05 | Proceso                | Ausente      |
| CAP-03       | Paquete de trust assets verificables | faltan casos, referencias y claims respaldados                 | H01-H06            | Evidencia              | Ausente      |
| CAP-04       | Arquitectura de CTA por ICP          | el siguiente paso es generico                                  | H01-H06            | Conversion             | Parcial      |
| CAP-05       | Plantillas de propuesta defendible   | no se puede evaluar comparabilidad real de ofertas             | H01-H05            | Comercial              | No evaluable |
| CAP-06       | Registro de claims y permisos        | riesgo de sobrepromesa y publicacion insegura                  | H01-H06            | Gobernanza             | Ausente      |
| CAP-07       | Instrumentacion de demanda           | no hay Analytics, Search Console ni funnel basico              | H01-H06            | Datos                  | Ausente      |
| CAP-08       | Sistema de casos por ICP             | sin casos no hay profundidad en consideracion y validacion     | H01-H04, H06       | Contenido + Trust      | Ausente      |
| CAP-09       | Loop win/loss y aprendizaje          | no hay feedback sistemico sobre porque avanza o se cae un deal | H01-H06            | Inteligencia comercial | Ausente      |
| CAP-10       | Board pack para buyer complejo       | falta material para defender contratacion ante comite o socios | H01, H04           | Venta consultiva       | Ausente      |

## Priorizacion operativa

### Prioridad 1

| Capacidad                                   | Razon                                                               |
| ------------------------------------------- | ------------------------------------------------------------------- |
| CAP-02 Discovery y diagnostico por ICP      | sin esto PICC no puede convertir interes en oportunidad cualificada |
| CAP-03 Paquete de trust assets verificables | sin evidencia no puede cerrar decisiones de alto riesgo             |
| CAP-04 Arquitectura de CTA por ICP          | el siguiente paso actual es demasiado generico                      |
| CAP-06 Registro de claims y permisos        | evita sobrepromesa y habilita publicacion segura                    |

### Prioridad 2

| Capacidad                                 | Razon                                    |
| ----------------------------------------- | ---------------------------------------- |
| CAP-08 Sistema de casos por ICP           | alimenta consideracion y confianza       |
| CAP-05 Plantillas de propuesta defendible | mejora aprobacion y comparabilidad       |
| CAP-07 Instrumentacion de demanda         | permite aprender donde se pierde demanda |

### Prioridad 3

| Capacidad                              | Razon                                                    |
| -------------------------------------- | -------------------------------------------------------- |
| CAP-09 Loop win/loss y aprendizaje     | vuelve sistemica la mejora comercial                     |
| CAP-10 Board pack para buyer complejo  | muy valioso para H01/H04, pero depende de assets previos |
| CAP-01 Mensajeria sectorial priorizada | importante, pero debe apoyarse en discovery y trust      |

## Mapa capability x decision friction

| Friccion del comprador                      | Capacidad principal | KPI inicial sugerido                                        |
| ------------------------------------------- | ------------------- | ----------------------------------------------------------- |
| No se si PICC es para mi caso               | CAP-01 + CAP-08     | porcentaje de leads que identifican su sector o problema    |
| No se que siguiente paso tomar              | CAP-04 + CAP-02     | tasa de paso de visita/diagnostico                          |
| No se si realmente saben hacerlo            | CAP-03 + CAP-08     | uso de trust assets en oportunidades prioritarias           |
| No puedo defender la contratacion           | CAP-05 + CAP-10     | tasa de aprobacion de propuestas complejas                  |
| No confio en los claims                     | CAP-06              | porcentaje de claims con respaldo documental                |
| No sabemos por que se pierden oportunidades | CAP-07 + CAP-09     | porcentaje de oportunidades con causa de perdida registrada |

## Surface and owner map V1

| Surface o punto operativo  | Capacidad asociada | Owner sugerido        | KPI inicial                                |
| -------------------------- | ------------------ | --------------------- | ------------------------------------------ |
| Home                       | CAP-01, CAP-04     | Marketing / Comercial | CTR a CTA relevante o contacto cualificado |
| WhatsApp / correo          | CAP-04, CAP-02     | Comercial             | tiempo de respuesta y agenda generada      |
| Reunion de discovery       | CAP-02             | Comercial + Tecnico   | porcentaje de discovery completo           |
| Deck / propuesta           | CAP-05, CAP-10     | Comercial + Direccion | tasa de avance a aprobacion                |
| Biblioteca de casos        | CAP-03, CAP-08     | Direccion + Marketing | numero de casos verificables activos       |
| Registro de claims         | CAP-06             | Direccion             | porcentaje de claims auditados             |
| Analitica de demanda       | CAP-07             | Marketing / Producto  | panel activo y fuentes conectadas          |
| Revision comercial mensual | CAP-09             | Direccion + Comercial | win/loss registrado                        |

## Secuencia minima de implementacion

1. Crear discovery y diagnostico para H01-H02-H04.
2. Levantar inventario de claims, credenciales y permisos.
3. Diseñar CTA y siguiente paso diferenciados por ICP prioritario.
4. Auditar propuestas reales y extraer plantilla defendible.
5. Construir 1 caso verificable para H01 y 1 para H02.
6. Activar instrumentacion basica de demanda.

## KPI base de Buyer System V1

- porcentaje de leads con ICP clasificable.
- porcentaje de contactos que avanzan a discovery.
- tiempo medio de respuesta a lead entrante.
- porcentaje de propuestas con trust assets adjuntos.
- porcentaje de claims auditados y con nivel de evidencia asignado.
- porcentaje de oportunidades con razon de perdida registrada.

## Lectura ejecutiva

La mayor carencia actual no parece ser un problema de oferta, sino de operacionalizacion comercial: PICC muestra amplitud de servicios y credenciales, pero no tiene todavia un sistema visible y trazable para mover compradores complejos desde interes hasta decision defendible.
