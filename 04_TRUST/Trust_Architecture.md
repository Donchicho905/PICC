# Trust Architecture

## Ficha de Trazabilidad
- ID: DOC-017
- Estado: 🟡 En desarrollo
- Tipo: Trust and Evidence Map V1
- Objetivo: Definir que evidencia necesita PICC para sostener claims, soportar decisiones de comprador y reducir friccion comercial.
- Entradas:
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - RL-001 (02_VERDAD_COMERCIAL/RESEARCH_LEDGER.md)
- Salidas:
  - Mapa de requisitos de evidencia
  - Matriz de brechas de informacion
  - Regla de publicabilidad y permiso de uso
- Dependencias:
  - DOC-007 (02_VERDAD_COMERCIAL/Auditoria_Sitio.md)
  - DOC-014 (03_MODELO_COMERCIAL/Modelo_Comercial.md)
- Documentos consumidos:
  - evidencia publica de `picc.com.mx`
  - fuentes internas y externas observadas en Buyer System V1
- Documentos generados:
  - DOC-020 (05_PRODUCTO/Capability_Model.md)
- Responsable: Direccion + Comercial + Operaciones
- Fecha: 2026-07-15
- Criterios de aceptación:
  - cada claim importante tiene nivel de evidencia esperado
  - las brechas distinguen ausencia de dato vs ausencia de permiso
  - el documento permite priorizar trust assets por ICP

## Principio rector

Sin evidencia trazable no hay claim defendible. Sin permiso de uso no hay publicacion segura. Sin estructura de acceso no hay escalamiento confiable del sistema comercial.

## Niveles de evidencia

| Nivel | Nombre                     | Descripcion                                                                      | Uso permitido                                       |
| ----- | -------------------------- | -------------------------------------------------------------------------------- | --------------------------------------------------- |
| E0    | No evidencia               | opinion, memoria oral o inferencia sin documento                                 | no publicable, no usable para claims                |
| E1    | Señal aislada              | correo, cotizacion, conversacion o prueba puntual no representativa              | usable solo como indicio interno                    |
| E2    | Evidencia parcial trazable | activo real con fuente identificable pero sin set completo de contexto o permiso | usable internamente y con extrema cautela externa   |
| E3    | Evidencia operativa        | caso, referencia, propuesta o entregable con datos suficientes y trazabilidad    | usable en venta asistida, no necesariamente publica |
| E4    | Evidencia publicable       | caso o claim con permiso, validacion y material verificable                      | usable en sitio, decks y materiales comerciales     |
| E5    | Evidencia sistemica        | evidencia repetida, estructurada y medible en cartera o historico                | usable para posicionamiento y mejora continua       |

## Tipos de trust assets requeridos

1. Casos comparables por ICP.
2. Credenciales tecnicas y certificaciones verificadas.
3. Referencias autorizadas.
4. Metodologias de discovery, diagnostico y ejecucion.
5. Propuestas comparables y estructuras de alcance.
6. Evidencia visual autorizada.
7. Datos de desempeno comercial: win/loss, tiempos, recompra, referral.
8. Permisos de uso y reglas de sensibilidad.

## Evidence Requirements Map

| ICP     | Decision a soportar                            | Tipo de evidencia requerida                | Nivel objetivo | Estado V1 | Fuente actual           | Brecha principal                                    | Owner sugerido          |
| ------- | ---------------------------------------------- | ------------------------------------------ | -------------- | --------- | ----------------------- | --------------------------------------------------- | ----------------------- |
| ICP-H01 | PICC entiende Data Centers                     | caso comparable + credencial tecnica       | E4             | E2        | Home                    | falta caso autorizado comparable                    | Direccion + Operaciones |
| ICP-H01 | PICC es tecnicamente competente                | certificaciones + metodologia + equipo     | E4             | E2        | Home                    | claims sin paquete de verificacion interno          | Direccion               |
| ICP-H01 | Puedo defender su contratacion                 | propuesta comparable + referencia          | E3-E4          | E0        | no accesible            | sin propuestas auditadas ni referencias autorizadas | Comercial               |
| ICP-H02 | PICC opera bien en entorno industrial          | caso industrial + metodologia en operacion | E4             | E1        | Home                    | falta caso industrial visible                       | Operaciones             |
| ICP-H02 | El riesgo operativo esta controlado            | checklist de seguridad y fases             | E3             | E0        | no accesible            | discovery no estructurado                           | Operaciones + Comercial |
| ICP-H03 | PICC ejecuta oficinas/comercial con calidad    | casos visuales + tiempos + referencias     | E4             | E1        | Home                    | falta activo visual y testimonial                   | Comercial               |
| ICP-H03 | La propuesta es comparable                     | plantilla de alcance + exclusiones         | E3             | E0        | no accesible            | propuestas no auditadas                             | Comercial               |
| ICP-H04 | PICC acompana viabilidad y ejecucion           | framework por fases + comparables          | E3-E4          | E1        | ecosistema externo      | falta asset publicable y framework propio           | Direccion + Comercial   |
| ICP-H04 | Puedo presentarlo a socios                     | board pack + caso + riesgos                | E3             | E0        | no accesible            | no existen materiales de comite observados          | Direccion               |
| ICP-H05 | PICC me orienta desde terreno/proyecto         | arbol de decision + caso patrimonial       | E3             | E1        | caso puntual Rocablocks | falta repeticion y estructura                       | Comercial               |
| ICP-H06 | PICC entrega confianza residencial high-ticket | fotos + referencias + proceso              | E4             | E1        | Home                    | falta evidencia autorizada                          | Comercial               |

## Claim Register V1

| Claim o promesa                            | Fuente visible actual | Nivel observado | Publicable hoy  | Riesgo si se usa mal                     | Accion                           |
| ------------------------------------------ | --------------------- | --------------- | --------------- | ---------------------------------------- | -------------------------------- |
| Especializacion en Data Centers            | Home                  | E2              | Si, con cautela | sobrepromesa sin caso comparable publico | verificar casos y armar asset    |
| Certificaciones ICREA / CCRD               | Home                  | E2              | Si, con cautela | claim no trazado internamente            | resguardar prueba documental     |
| Partnership o relacion con Panduit         | Home                  | E2              | Si, con cautela | confusion de alcance de partnership      | aclarar terminos exactos         |
| 25+ años de experiencia                    | Home                  | E2              | Si, con cautela | cifra no auditada en repo                | crear respaldo institucional     |
| 100+ proyectos                             | Home                  | E2              | Si, con cautela | numero no desglosado                     | crear inventario de proyectos    |
| 50,000+ m2 construidos                     | Home                  | E2              | Si, con cautela | metrica sin metodologia visible          | documentar fuente                |
| Cobertura industrial/comercial/residencial | Home                  | E2              | Si, con cautela | amplitud sin profundidad                 | priorizar ICPs y probar sectores |

## Matriz de brechas de informacion

| Brecha                                      | Tipo de brecha          | ICPs afectados               | Impacto    | Urgencia   | Como se cierra                                 |
| ------------------------------------------- | ----------------------- | ---------------------------- | ---------- | ---------- | ---------------------------------------------- |
| No hay CRM historico accesible              | Acceso a datos          | Todos                        | Muy alto   | Alta       | export de pipeline, win/loss y etapas          |
| No hay propuestas reales auditadas          | Evidencia operativa     | Todos, especialmente H01-H04 | Muy alto   | Alta       | muestreo de propuestas cerradas y perdidas     |
| No hay permisos de uso de casos/testimonios | Legal/publicabilidad    | Todos                        | Alto       | Alta       | registro de permisos y sensibilidad            |
| No hay casos sectoriales publicados         | Asset comercial         | H01-H04, H06                 | Alto       | Alta       | levantar 1 caso por ICP prioritario            |
| No hay referencias autorizadas              | Trust asset             | Todos                        | Alto       | Media-alta | shortlist de clientes y script de autorizacion |
| No hay Analytics/Search Console             | Inteligencia de demanda | Todos                        | Medio-alto | Media      | acceso tecnico y dashboard                     |
| No hay framework de discovery versionado    | Metodo comercial        | H01-H05                      | Alto       | Alta       | crear diagnosticos repetibles por ICP          |
| No hay inventario de claims con respaldo    | Gobernanza              | Todos                        | Alto       | Alta       | registry de claims y evidencia                 |

## Reglas de publicabilidad

- Un claim solo sube a sitio o deck publico cuando alcanza E4.
- Un claim E2 puede sostener exploracion interna o venta asistida con nota de cautela, no posicionamiento fuerte.
- Un caso con datos sensibles sin permiso no se publica, aunque sea tecnicamente potente.
- Una referencia verbal sin autorizacion no se presenta como testimonio.
- Una metrica agregada debe documentar fuente, periodo y criterio de conteo.

## Trust assets prioritarios por secuencia

1. Paquete de credenciales verificadas para ICP-H01.
2. Caso comparable o mini-case de infraestructura critica.
3. Checklist de discovery y diagnostico para H01-H02-H04.
4. Inventario de claims con respaldo documental.
5. Referencias autorizadas y fotos publicables.
6. Muestreo de propuestas para entender defendibilidad comercial.

## Implicaciones operativas

- Trust no es solo contenido: tambien es acceso, permiso, estructura y disciplina.
- La principal limitacion del Buyer System V1 no parece ser ausencia total de experiencia, sino ausencia de empaquetado y trazabilidad.
- El sitio actual puede captar interes, pero no cierra solo decisiones complejas sin activos de confianza complementarios.
