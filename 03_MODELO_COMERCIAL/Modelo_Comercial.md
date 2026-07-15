# Modelo Comercial

## Ficha de Trazabilidad

- ID: DOC-014
- Estado: 🟡 En desarrollo
- Tipo: Buyer System - Modelo Comercial V1
- Objetivo: Traducir el Buyer System en una logica comercial que priorice compradores, decisiones y surfaces antes que un catalogo de servicios.
- Entradas:
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md)
  - DOC-011 (03_MODELO_COMERCIAL/Customer_Journey.md)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Salidas:
  - Criterios de calificacion y descalificacion comercial
  - Recomendacion de foco MVP
  - Prioridades de surfaces y evidencia
- Dependencias:
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
  - RL-001 (02_VERDAD_COMERCIAL/RESEARCH_LEDGER.md)
- Documentos consumidos:
  - DOC-002 (00_MASTER_PLAN/MASTER_PLAN_PICC_NEXT_V3.md)
  - DOC-007 (02_VERDAD_COMERCIAL/Auditoria_Sitio.md)
  - evidencia publica y fuentes internas usadas en Buyer System V1
- Documentos generados:
  - DOC-020 (05_PRODUCTO/Capability_Model.md)
  - 00_IMPLEMENTATION_REPORT.md
- Responsable: Direccion Comercial + Producto
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Supuestos explicitados
  - decisiones comerciales trazables por ICP
  - foco MVP justificable con evidencia disponible y brechas declaradas

## Principio rector

PICC no debe organizar su sistema comercial desde lo que quiere vender, sino desde lo que el comprador intenta decidir y lo que le impide avanzar.

La pregunta central de este artefacto es:

- que decision del comprador debemos facilitar primero para convertir confianza en conversacion, oportunidad y contrato.

## Lectura comercial actual de PICC

### Lo que si aparece con claridad en evidencia publica

- PICC se presenta como empresa de construccion e infraestructura en Mexico. [Hecho verificado]
- La especializacion diferencial visible hoy es Data Centers e infraestructura critica. [Hecho verificado]
- La Home publica certificaciones y estandares visibles: ICREA CCRD y PANDUIT. [Hecho verificado]
- El sitio tambien comunica servicios de construccion comercial, industrial, remodelaciones, instalaciones electricas, cableado y climatizacion. [Hecho verificado]
- Existe CTA directo a contacto, correo, telefono y WhatsApp. [Hecho verificado]

### Lo que todavia no puede sostenerse como verdad comercial cerrada

- Que Data Centers sea hoy el segmento que mas cierra negocio. [Informacion faltante]
- Que industrial o corporativo sean mas rentables o mas faciles de cerrar. [Informacion faltante]
- Que el mensaje de Home este alineado con el pipeline real. [Informacion faltante]
- Que existan casos publicables suficientes para convertir la promesa en confianza demostrada. [Informacion faltante]

## Que compra realmente el comprador

El comprador no compra solo construccion. Compra una combinacion de:

- reduccion de riesgo tecnico;
- reduccion de riesgo de ejecucion;
- claridad de alcance y presupuesto;
- capacidad de defender la decision frente a terceros;
- continuidad operativa;
- una contraparte confiable para coordinar varias disciplinas.

## Hipotesis de propuesta de valor por familia de ICP

| Familia de ICP              | Lo que probablemente compra            | Riesgo que quiere reducir                                           | Estado epistemologico |
| --------------------------- | -------------------------------------- | ------------------------------------------------------------------- | --------------------- |
| Infraestructura critica     | Certidumbre tecnica y continuidad      | downtime, mala especificacion, proveedor incorrecto                 | Evidencia parcial     |
| Industrial                  | Ejecucion segura sin frenar operacion  | paro, retrabajo, sobrecosto, instalaciones deficientes              | Evidencia parcial     |
| Corporativo / oficinas      | Adecuacion funcional y defendible      | mala experiencia de usuario, retraso, propuesta no comparable       | Hipotesis             |
| Desarrollador inmobiliario  | Claridad de viabilidad y ejecucion     | direccion equivocada, proveedor no integral, inversion mal asignada | Evidencia parcial     |
| Inversionista con terreno   | Diagnostico y siguiente paso confiable | gastar sin claridad, mala decision patrimonial                      | Evidencia parcial     |
| Cliente privado high-ticket | Tranquilidad y calidad integral        | mala calidad, sobrecosto, mala experiencia                          | Hipotesis             |

## Criterios de calificacion comercial V1

Una oportunidad sube de prioridad si cumple varios de estos criterios:

1. El problema es costoso si se decide mal.
2. El comprador reconoce riesgo tecnico u operativo.
3. PICC puede aportar diferenciacion creible, no solo mano de obra.
4. Existe posibilidad de mostrar evidencia relevante o construirla rapido.
5. El siguiente paso natural es consultivo: visita, diagnostico o propuesta comparativa.
6. El alcance requiere coordinacion multidisciplinaria.

## Criterios de descalificacion temprana V1

Una oportunidad baja de prioridad si se observa alguno de estos patrones:

1. Compra puramente commodity con comparacion casi solo por precio.
2. No existe dolor relevante si el proveedor falla.
3. El comprador no valora especializacion, certificacion ni metodologia.
4. El ticket y la complejidad no justifican el modelo consultivo de PICC.
5. El alcance depende de permisos, datos o presupuesto que nadie controla todavia.

## Recomendacion comercial para el MVP

### ICP prioritario 1

- ICP-H01 Infraestructura critica y Data Centers.
- Motivo: hoy es el unico ICP donde la promesa publica visible ya muestra una especializacion diferencial concreta.
- Riesgo: la evidencia visible es de mensaje y certificacion, no de casos trazables cerrados.

### ICP prioritario 2

- ICP-H02 Industrial e instalaciones criticas.
- Motivo: permite aprovechar la misma base tecnica de energia, climatizacion y ejecucion con una superficie de mercado potencialmente mas amplia.
- Riesgo: falta confirmar cierres, margen y ciclo real.

### ICP de continuidad

- ICP-H04 Desarrollador inmobiliario mediano.
- Motivo: hay señales reales de operacion del ecosistema en proyectos relacionados, pero la narrativa comercial actual no lo sostiene todavia con la misma claridad que infraestructura critica.
- Riesgo: sin casos publicables y sin cartera estructurada puede distraer el MVP.

## Modelo de intervencion comercial esperado

| Etapa                | Intervencion digital dominante                          | Intervencion humana dominante               |
| -------------------- | ------------------------------------------------------- | ------------------------------------------- |
| Descubrimiento       | Home, servicios, surfaces sectoriales, LinkedIn         | Ninguna o minima                            |
| Consideracion        | casos, trust assets, comparadores, contenido            | llamada exploratoria o respuesta consultiva |
| Shortlist            | pagina sectorial, caso comparable, matriz de evidencia  | diagnostico, visita o reunion tecnica       |
| Propuesta            | documento comparable, alcances, riesgos, siguiente paso | liderazgo comercial y tecnico               |
| Negociacion y cierre | seguimiento, referencias, clarificacion de supuestos    | direccion, comercial y operaciones          |

## Que no debe hacer el MVP

- intentar hablarle igual a todos los segmentos.
- esconder la falta de evidencia real.
- prometer resultados no rastreables.
- invertir primero en diseno visual antes de resolver decisiones del comprador.

## Preguntas abiertas que afectan el modelo

- que porcentaje del negocio real de PICC viene de infraestructura critica, industrial, corporativo, desarrollador o privado.
- cuales segmentos pagan mejor y cobran mas rapido.
- donde existe evidencia publicable suficiente para construir confianza hoy.
- cual es el costo real de perseguir segmentos con bajo fit.

## Decision comercial vigente

Hasta tener CRM, cartera, perdidos/ganados y permisos de casos, el Buyer System V1 debe tratar a los ICPs como hipotesis operativas y no como segmentacion definitiva.