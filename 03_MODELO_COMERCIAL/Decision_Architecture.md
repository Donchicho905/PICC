# Decision Architecture

## Ficha de Trazabilidad
- ID: DOC-012
- Estado: 🟡 En desarrollo
- Tipo: Decision Journey V1
- Objetivo: Hacer visibles las decisiones que controlan el avance de cada ICP y el estado actual de soporte comercial de PICC.
- Entradas:
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md)
  - DOC-011 (03_MODELO_COMERCIAL/Customer_Journey.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Salidas:
  - Registro de decisiones por ICP
  - Cobertura de decision V1
  - Brechas y acciones requeridas
- Dependencias:
  - DOC-007 (02_VERDAD_COMERCIAL/Auditoria_Sitio.md)
  - RL-001 (02_VERDAD_COMERCIAL/RESEARCH_LEDGER.md)
- Documentos consumidos:
  - evidencia publica de `picc.com.mx`
  - fuentes internas y externas usadas en Buyer System V1
- Documentos generados:
  - DOC-014 (03_MODELO_COMERCIAL/Modelo_Comercial.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Responsable: Direccion Comercial + Producto
- Fecha: 2026-07-15
- Criterios de aceptación:
  - cada ICP tiene decisiones criticas visibles
  - las brechas estan explicitadas
  - Decision Coverage no confunde falta de acceso con mal desempeno probado

## Regla de soporte de decision

Una decision se considera:

- Soportada: mensaje claro + evidencia trazable + permiso de uso + ubicacion adecuada + siguiente paso comprensible.
- Parcialmente soportada: existe mensaje o credencial visible, pero falta trazabilidad interna, permiso o profundidad.
- No soportada: la superficie existe pero no ayuda a resolver la decision.
- No evaluable: no existe acceso suficiente para juzgar la decision.

## Universo base de decisiones

1. Debo actuar ahora.
2. Necesito construir, remodelar, invertir o estudiar primero.
3. Que alcance necesito.
4. Que presupuesto debo esperar.
5. Que riesgos existen.
6. Vale la pena considerar a PICC.
7. PICC entiende un proyecto como el mio.
8. Tiene experiencia comparable.
9. Es tecnicamente competente.
10. Es institucionalmente confiable.
11. Que la hace diferente.
12. Puedo defender su contratacion ante otros.
13. Su propuesta es comparable y economicamente defendible.
14. Que siguiente paso debo tomar.

## Decision Journey por ICP

| ICP     | Etapa | Decision critica                                     | Importancia | Evidencia minima suficiente                             | Surface principal           | Owner PICC              | Estado actual de soporte | Brecha                                         | Accion requerida                             |
| ------- | ----- | ---------------------------------------------------- | ----------- | ------------------------------------------------------- | --------------------------- | ----------------------- | ------------------------ | ---------------------------------------------- | -------------------------------------------- |
| ICP-H01 | 1-2   | Debo actuar ahora                                    | Alta        | pain claro + riesgo de downtime + CTA consultiva        | Home                        | Marketing               | Parcialmente soportada   | falta prueba de casos y trigger real           | capturar dolores reales y CTA de diagnostico |
| ICP-H01 | 3-4   | Que alcance necesito                                 | Alta        | metodologia, discovery, disciplinas, matriz de riesgos  | Reuniones / propuesta       | Comercial + Tecnico     | No evaluable             | no hay discovery documentado publico           | crear oferta de diagnostico                  |
| ICP-H01 | 5-6   | Vale la pena considerar a PICC                       | Alta        | credenciales + experiencia comparable + especializacion | Home / sectorial futura     | Comercial               | Parcialmente soportada   | no hay caso comparable visible                 | construir caso sectorial                     |
| ICP-H01 | 7     | Es tecnicamente competente                           | Alta        | certificacion + equipo + caso + metodologia             | Home + trust assets         | Direccion + Operaciones | Parcialmente soportada   | falta trazabilidad interna de claims           | verificar claims y permisos                  |
| ICP-H01 | 9-10  | Puedo defender su contratacion                       | Alta        | propuesta comparable + riesgos + referencias            | Propuesta                   | Direccion + Comercial   | No evaluable             | no se revisaron propuestas reales              | auditar propuestas existentes                |
| ICP-H01 | 11-12 | Que siguiente paso debo tomar                        | Alta        | siguiente paso claro + owner + tiempos                  | WhatsApp / correo / reunion | Comercial               | Parcialmente soportada   | CTA generica, no diagnostico especializado     | redefinir CTA por ICP                        |
| ICP-H02 | 1-2   | Debo actuar ahora                                    | Alta        | problema operativo cuantificado                         | Home / contacto             | Marketing               | Parcialmente soportada   | no hay narrativa industrial por dolor          | crear mensaje de continuidad operativa       |
| ICP-H02 | 3-4   | Necesito construir, adecuar o corregir instalaciones | Alta        | checklist de decision y discovery                       | Reunion                     | Comercial + Tecnico     | No evaluable             | sin checklist publico ni interno versionado    | crear checklist industrial                   |
| ICP-H02 | 5-6   | PICC entiende un proyecto como el mio                | Alta        | caso industrial comparable + metodologia en operacion   | Sectorial futura            | Comercial               | No soportada             | sitio no muestra caso industrial concreto      | levantar caso industrial                     |
| ICP-H02 | 7     | Es institucionalmente confiable                      | Media-alta  | equipo, supervision, cobertura, referencias             | Trust assets                | Direccion               | Parcialmente soportada   | referencias no accesibles                      | obtener referencias autorizadas              |
| ICP-H02 | 9-10  | Su propuesta es comparable y defendible              | Alta        | fases, riesgos, impacto operativo                       | Propuesta                   | Comercial + Operaciones | No evaluable             | sin propuestas auditadas                       | revisar propuestas previas                   |
| ICP-H02 | 11-12 | Que siguiente paso debo tomar                        | Alta        | visita o diagnostico con owner claro                    | WhatsApp / correo           | Comercial               | Parcialmente soportada   | CTA no diferencia industrial                   | CTA por ICP                                  |
| ICP-H03 | 1-2   | Debo actuar ahora                                    | Media       | trigger de mudanza/remodelacion y costo de espera       | Home                        | Marketing               | Parcialmente soportada   | no hay mensaje por dolor corporativo           | crear narrativa de adecuacion                |
| ICP-H03 | 3-4   | Que requisitos debo definir                          | Alta        | alcance, tiempos, usuarios, instalaciones               | Reunion                     | Comercial               | No evaluable             | falta framework de discovery corporativo       | crear framework                              |
| ICP-H03 | 5-6   | Vale la pena considerar a PICC                       | Media-alta  | casos, fotos, remodelacion, oficinas                    | Sectorial futura            | Comercial               | No soportada             | sitio no muestra oficina/caso visible          | levantar casos                               |
| ICP-H03 | 7     | Puedo confiar en la ejecucion                        | Media-alta  | referencias y calidad visible                           | Trust assets                | Direccion               | No evaluable             | evidencia visual y referencias faltan          | inventario de activos                        |
| ICP-H03 | 9-10  | La propuesta es comparable                           | Alta        | alcance, exclusiones, cronograma                        | Propuesta                   | Comercial               | No evaluable             | sin propuestas auditadas                       | auditar propuestas                           |
| ICP-H03 | 11-12 | Que siguiente paso debo tomar                        | Media-alta  | CTA consultiva y agenda simple                          | Correo / WhatsApp           | Comercial               | Parcialmente soportada   | CTA demasiado generica                         | CTA por journey                              |
| ICP-H04 | 1-2   | Necesito estudiar, disenar o ejecutar primero        | Alta        | metodo por fases, riesgos, decision tree                | Diagnostico                 | Comercial + Tecnico     | No soportada             | no existe arbol de decision visible            | crear framework de faseo                     |
| ICP-H04 | 3-4   | Que alcance y viabilidad necesito                    | Alta        | discovery, viabilidad, permisos, costos                 | Reunion / propuesta         | Tecnico + Comercial     | No evaluable             | faltan datos de viabilidad reales              | inventario de viabilidad                     |
| ICP-H04 | 5-6   | PICC entiende un proyecto como el mio                | Alta        | caso desarrollo/complejidad equivalente                 | Casos futuros               | Comercial               | Parcialmente soportada   | hay señales ecosistema pero no publicables     | validar permisos                             |
| ICP-H04 | 7     | Puedo confiar en ellos para orientar inversion       | Alta        | referencias, proceso, entregables                       | Trust assets                | Direccion               | No evaluable             | referencias y entregables no estructurados     | estructurar activos                          |
| ICP-H04 | 9-10  | Puedo defender su contratacion ante socios           | Alta        | propuesta, comparables, riesgos                         | Deck / propuesta            | Direccion               | No evaluable             | faltan materiales de comite                    | plantilla de board pack                      |
| ICP-H04 | 11-12 | Que siguiente paso debo tomar                        | Alta        | diagnostico, visita o fase 1 clara                      | WhatsApp / correo           | Comercial               | Parcialmente soportada   | CTA no diferencia developer                    | CTA de viabilidad                            |
| ICP-H05 | 1-2   | Debo activar el terreno ahora                        | Media-alta  | oportunidad, riesgo de no accionar, paso inicial        | Home / contacto             | Marketing               | No soportada             | sitio no habla a este comprador directo        | evaluar landing futura                       |
| ICP-H05 | 3-4   | Necesito construir, estudiar o cotizar primero       | Alta        | decision tree y checklist                               | Diagnostico                 | Comercial               | No evaluable             | falta framework simple                         | crear framework                              |
| ICP-H05 | 5-6   | Vale la pena considerar a PICC                       | Media       | claridad y confianza personal                           | Contacto / caso futuro      | Comercial               | Parcialmente soportada   | no hay casos patrimoniales visibles            | reunir casos                                 |
| ICP-H05 | 7     | Puedo confiar en su criterio                         | Alta        | trato, proceso, referencias                             | Trust assets                | Direccion               | No evaluable             | no hay referencias autorizadas                 | obtener referencias                          |
| ICP-H05 | 9-10  | La propuesta me orienta                              | Alta        | escenarios, rangos, riesgos                             | Propuesta                   | Comercial               | No evaluable             | propuestas no auditadas                        | revisar propuestas                           |
| ICP-H05 | 11-12 | Que siguiente paso debo tomar                        | Alta        | visita y owner claro                                    | WhatsApp                    | Comercial               | Parcialmente soportada   | CTA generica                                   | CTA patrimonial                              |
| ICP-H06 | 1-2   | Debo remodelar o construir ahora                     | Media       | dolor y urgencia personal                               | Home                        | Marketing               | No soportada             | sitio no habla a este caso de forma directa    | decidir si vale la pena                      |
| ICP-H06 | 3-4   | Que alcance necesito                                 | Media-alta  | checklist, visuales, proceso                            | Reunion                     | Comercial               | No evaluable             | falta asset residencial                        | evidencia y proceso                          |
| ICP-H06 | 5-6   | Vale la pena considerar a PICC                       | Media       | confianza, calidad y trato                              | Caso futuro                 | Comercial               | Parcialmente soportada   | hay promesa residencial pero no prueba visible | reunir activos                               |
| ICP-H06 | 7     | Puedo confiar en ellos                               | Alta        | referencias, fotos, seguimiento                         | Trust assets                | Direccion               | No evaluable             | faltan referencias y fotos autorizadas         | resolver permisos                            |
| ICP-H06 | 9-10  | La propuesta me da tranquilidad                      | Alta        | alcance y claridad de costos                            | Propuesta                   | Comercial               | No evaluable             | no hay propuestas revisadas                    | revisar archivo historico                    |
| ICP-H06 | 11-12 | Que siguiente paso debo tomar                        | Media-alta  | visita y owner claro                                    | WhatsApp                    | Comercial               | Parcialmente soportada   | CTA generica                                   | CTA consultiva                               |

## Decision Coverage V1

### Cobertura por ICP

| ICP     | Soportadas | Parcialmente soportadas | No soportadas | No evaluables | Nivel de confianza |
| ------- | ---------- | ----------------------- | ------------- | ------------- | ------------------ |
| ICP-H01 | 0          | 4                       | 0             | 2             | Baja-media         |
| ICP-H02 | 0          | 3                       | 1             | 2             | Baja               |
| ICP-H03 | 0          | 2                       | 1             | 3             | Baja               |
| ICP-H04 | 0          | 2                       | 1             | 3             | Baja               |
| ICP-H05 | 0          | 2                       | 1             | 3             | Baja               |
| ICP-H06 | 0          | 2                       | 1             | 3             | Baja               |

### Cobertura por etapa

| Etapa                         | Lectura V1                                                                    |
| ----------------------------- | ----------------------------------------------------------------------------- |
| Descubrimiento (1-2)          | Parcial: la Home activa interes y credenciales, pero no por ICP detallado     |
| Consideracion (3-6)           | Baja: faltan sectoriales, casos y comparadores                                |
| Validacion (7-8)              | Baja: faltan referencias autorizadas y trust assets trazables                 |
| Propuesta y aprobacion (9-12) | No evaluable: no hubo acceso a propuestas reales o CRM                        |
| Postventa (13-14)             | No evaluable: no hay datos estructurados de satisfaccion, recompra o referral |

### Cobertura por surface

| Surface              | Estado V1    | Comentario                                                                   |
| -------------------- | ------------ | ---------------------------------------------------------------------------- |
| Home                 | Parcial      | credenciales y servicios visibles, pero sin casos ni prueba interna trazable |
| Paginas de servicios | Parcial      | el contenido parece resumido dentro de Home, no por ICP                      |
| Paginas sectoriales  | No soportada | no observadas en repo o sitio                                                |
| Casos de exito       | No soportada | no observados                                                                |
| Propuestas           | No evaluable | sin acceso                                                                   |
| Correo y WhatsApp    | Parcial      | CTA existe, no journey especifico                                            |
| Reuniones            | No evaluable | no hay material estructurado                                                 |
| Portal del cliente   | No soportada | no existe evidencia                                                          |

## Principales brechas

1. Falta evidencia publicable de experiencia comparable.
2. Falta discovery estructurado por ICP.
3. Falta auditar propuestas reales y rutas de aprobacion.
4. Falta separar CTA y siguiente paso por ICP.
5. Falta estructurar datos de ganados, perdidos, recompra y referral.

## Acciones siguientes derivadas

- Priorizar surfaces y trust assets para ICP-H01 e ICP-H02.
- Auditar propuestas reales antes de afirmar que PICC gana por metodologia o comparabilidad.
- Convertir discovery y diagnostico en artefactos repetibles.
- Levantar casos y referencias con permiso de uso.

---

## Decision Coverage V2 — Post-auditoría Alpha Gate 01 (2026-07-15)

La cobertura V2 reemplaza las estimaciones previas con medición post-snapshot de las tres versiones del sitio en producción.

### Cobertura cuantificada H01 e H02

| ICP     | Decisiones totales evaluadas | Soportadas | Parcialmente soportadas | No soportadas | No evaluables | Cobertura efectiva estimada | Delta vs V1                                 |
| ------- | ---------------------------- | ---------- | ----------------------- | ------------- | ------------- | --------------------------- | ------------------------------------------- |
| ICP-H01 | 9                            | 0          | 3                       | 2             | 4             | 30–35%                      | Sin cambio sustancial                       |
| ICP-H02 | 9                            | 0          | 2                       | 3             | 4             | 20–25%                      | Sin cambio sustancial — peor de lo estimado |

**Nota sobre cobertura efectiva**: Se calcula como (soportadas + 0.5 × parcialmente soportadas) / total. El 0.5 penaliza las parciales por ausencia de trazabilidad interna.

### Factores de reducción detectados en auditoría

Los siguientes factores reducen la cobertura real por debajo de la visual:

1. **Fotos de Unsplash**: Todo el material visual del sitio (Hero, equipo, Data Center) es stock, no imágenes propias. Un buyer técnico de H01 puede detectarlo fácilmente. Esto invalida efectivamente los claims implícitos CLM-IMP-01/02/03.
2. **Inconsistencia ICREA ES vs EN/FR**: ES dice "Nivel I al VI" mientras EN y FR dicen "Tier II and III". Un comprador H01 que revisa las dos versiones percibe incompetencia o deshonestidad.
3. **Claim absoluto en equipo**: "garantizando resultados de primer nivel en cada proyecto" — genera expectativa contractual sin respaldo (CLM-EQP-03).
4. **Métricas sin metodología visible**: 100+ proyectos y 50,000+ m² no tienen fuente ni criterio de conteo. Para un buyer técnico de H01, esto puede ser señal de marketing vacío.
5. **Logotipo Panduit sin calificación uniforme**: ES no califica, EN dice "Certified", FR dice "Partenaire". Inconsistencia visible entre idiomas.

### Brecha más crítica para H01 (post-auditoría)

La decisión "¿Tiene experiencia comparable?" (etapa de Validación) está **no soportada** por ausencia de:
- Ningún caso de Data Center publicable.
- Ninguna foto propia de obra.
- Alcance de ICREA sin documento verificable.

Esta decisión es el paso de calificación más importante antes de que H01 pase a solicitar propuesta.

### Brecha más crítica para H02 (post-auditoría)

La decisión "¿PICC entiende mi tipo de proyecto?" está **no soportada** por:
- La Home habla principalmente de Data Centers, no de industrial.
- No existe una ruta diferenciada para H02.
- No hay ningún caso industrial visible.

### Acción prioritaria derivada de cobertura V2

| Acción                                          | ICP      | Decisión desbloqueada                  | Owner                 | Esfuerzo | Impacto  |
| ----------------------------------------------- | -------- | -------------------------------------- | --------------------- | -------- | -------- |
| Resolver inconsistencia ICREA ES/EN/FR          | H01      | Es técnicamente competente             | Dirección             | Muy bajo | Crítico  |
| Obtener y publicar mínimo 3 fotos propias       | H01, H02 | Tiene experiencia comparable           | Dirección + Marketing | Medio    | Muy alto |
| Construir y publicar CASO-01 (Data Center)      | H01      | Tiene experiencia comparable           | Dirección + Ops       | Alto     | Muy alto |
| Construir y publicar CASO-02 (Industrial)       | H02      | PICC entiende mi caso                  | Dirección + Ops       | Alto     | Muy alto |
| Diseñar ruta diferenciada para H02              | H02      | PICC entiende mi caso / siguiente paso | Comercial + Producto  | Medio    | Alto     |
| Obtener autorización formal de logotipo Panduit | H01      | Es técnicamente competente             | Dirección             | Bajo     | Alto     |
