# Growth MVP V1 — Diseño funcional completo

## Ficha de Trazabilidad
- ID: DOC-033
- Estado: 🟡 En diseño
- Tipo: Growth MVP V1 — Plano funcional ejecutable
- Objetivo: Diseñar el recorrido mínimo completo desde descubrimiento hasta oportunidad calificada, sin código ni estética final.
- Entradas:
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md)
  - DOC-011 (03_MODELO_COMERCIAL/Customer_Journey.md)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
  - DOC-020 (05_PRODUCTO/Capability_Model.md)
  - DOC-014 (03_MODELO_COMERCIAL/Modelo_Comercial.md)
- Salidas:
  - Arquitectura funcional de Home
  - Rutas ICP-H01 e ICP-H02
  - Propuestas de valor verificables
  - Trust assets y sistema de casos
  - Diseño de Preevaluación PICC
  - Formulario de captura justificado
  - Flujo interno del lead
  - Content MVP
  - Decision Coverage objetivo
  - Backlog P0/P1/P2 (ver DOC-018)
  - Métricas instrumentables
- Dependencias:
  - DOC-015 (04_TRUST/Biblioteca_de_Evidencia.md)
  - DOC-016 (04_TRUST/Sistema_de_Evidencia.md)
  - DOC-018 (05_PRODUCTO/Capability_Backlog.md)
  - DOC-022 (05_PRODUCTO/Product_Roadmap.md)
- Documentos consumidos:
  - Buyer System V1 completo
  - evidencia publica de picc.com.mx
- Documentos generados:
  - DOC-018 (05_PRODUCTO/Capability_Backlog.md)
  - DOC-016 (04_TRUST/Sistema_de_Evidencia.md)
  - DOC-015 (04_TRUST/Biblioteca_de_Evidencia.md)
  - DOC-022 (05_PRODUCTO/Product_Roadmap.md)
- Responsable: Direccion + Comercial + Producto
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Existe arquitectura funcional de Home por sección
  - Existen dos rutas prioritarias completas por ICP
  - Propuesta de valor con clasificación de publicabilidad
  - Trust assets priorizados con brecha explícita
  - Preevaluación diseñada end-to-end
  - Formulario justificado campo por campo
  - Flujo interno del lead con owner y SLA
  - Content MVP con máximo piezas especificadas
  - Decision Coverage objetivo por surface
  - Backlog P0/P1/P2 sin funcionalidades V2/V3
  - Métricas con fuente, owner y baseline
  - Sin claims inventados
  - Datos faltantes registrados explícitamente

---

## 0. Restricciones del diseño

- No código ni desarrollo frontend o backend.
- No estética final, colores, tipografías ni renders.
- No cotización automática definitiva.
- No reabrir SHDLS.
- No redefinir ICPs sin evidencia nueva.
- No avanzar funcionalidades V2 o V3.
- No presentar hipótesis como hechos.
- Toda promesa debe clasificarse como publicable ahora, publicable condicionada, o no publicable todavía.

---

## 1. Confirmación de ICPs del MVP

ICPs tomados directamente de DOC-013 sin redefinición.

### ICP-H01 — Infraestructura crítica y Data Centers

- Nombre funcional: Responsable corporativo de infraestructura crítica o Data Center. [Evidencia parcial]
- Hipótesis: buyer con problema reconocido que busca comparación técnica. [Hipótesis]
- Prioridad en MVP: 1.
- Problema principal: crecimiento de demanda digital, riesgo de continuidad, certificación o ampliación. [Hipótesis]
- Riesgos dominantes: costo, plazo, proveedor incorrecto, reputación, aprobación interna. [Evidencia parcial]
- Decisiones críticas a soportar: Vale la pena considerar a PICC / Es técnicamente competente / Puedo defender la contratación.
- Evidencia requerida: certificaciones, caso comparable, metodología, equipo, referencia. [Información faltante]
- Surfaces relevantes: Home → Ruta H01 → Preevaluación → Reunión.
- Estado: hipótesis con evidencia parcial. No declarar definitivo.

### ICP-H02 — Industrial e instalaciones críticas

- Nombre funcional: Director o propietario de empresa industrial con necesidad de instalaciones críticas, eléctricas o HVAC. [Evidencia parcial]
- Hipótesis: buyer con necesidad operativa concreta y tiempo comprimido. [Hipótesis]
- Prioridad en MVP: 2.
- Problema principal: crecer capacidad, rehabilitar instalaciones o reducir riesgo operativo sin parar producción. [Hipótesis]
- Riesgos dominantes: plazo, calidad, operación en curso, proveedor incorrecto, seguridad. [Hipótesis]
- Decisiones críticas a soportar: PICC entiende un proyecto como el mío / Es institucionalmente confiable / Qué siguiente paso debo tomar.
- Evidencia requerida: caso industrial, metodología de obra en operación, referencia, equipo. [Información faltante]
- Surfaces relevantes: Home → Ruta H02 → Preevaluación → Reunión.
- Estado: hipótesis con evidencia parcial. No declarar definitivo.

---

## 2. Objetivo del MVP

Diseñar el recorrido mínimo funcional:

```
Descubrimiento
      ↓
Home o entrada sectorial
      ↓
Comprensión del problema
      ↓
Prueba de capacidad
      ↓
Caso o evidencia
      ↓
Preevaluación / diagnóstico
      ↓
Captura estructurada
      ↓
Respuesta comercial
      ↓
Reunión
```

El MVP no es completo si únicamente mejora la Home. Debe existir una ruta funcional completa desde la primera visita hasta una oportunidad comercial calificada.

---

## 3. Arquitectura funcional de la Home

La Home es el punto de entrada principal. No es solo página de presentación. Es la primera superficie de decisión del comprador.

Principio de diseño: la Home debe ayudar al buyer a reconocerse, confirmar que PICC entiende su problema, y saber qué hacer a continuación.

### Sección 1 — Hero

| Campo                    | Contenido                                                                                                                                                                                                               |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Activar reconocimiento inmediato del comprador correcto y capturar intención de avance                                                                                                                                  |
| ICP principal            | ICP-H01 (con señal inclusiva hacia ICP-H02)                                                                                                                                                                             |
| Decisión del comprador   | ¿Esto es para mí? / ¿PICC entiende lo que necesito?                                                                                                                                                                     |
| Incertidumbre que reduce | Si llegué al lugar correcto                                                                                                                                                                                             |
| Mensaje propuesto        | "Infraestructura crítica diseñada para no fallar. Data Centers, instalaciones industriales y sistemas de alta disponibilidad para organizaciones que no pueden parar." [Publicable condicionada — verificar tono final] |
| Evidencia requerida      | Ninguna extensa — el mensaje debe ser suficiente para una primera orientación                                                                                                                                           |
| CTA                      | Botón primario: "Cuéntanos tu proyecto" → Preevaluación. Botón secundario: "Ver qué hacemos" → Ruta H01 o H02 según señal                                                                                               |
| Surface de destino       | Preevaluación o ruta ICP                                                                                                                                                                                                |
| Métrica                  | CTR a CTA primario; CTR a rutas por ICP                                                                                                                                                                                 |
| Owner                    | Marketing / Comercial                                                                                                                                                                                                   |
| Datos faltantes          | No hay analytics activos para validar variantes de mensaje; las frases son hipótesis de copy. Requiere prueba.                                                                                                          |

### Sección 2 — Prueba inmediata de capacidad

| Campo                    | Contenido                                                                                                                                                                                                         |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Reducir incertidumbre técnica con credenciales concretas antes de que el comprador salga                                                                                                                          |
| ICP principal            | ICP-H01, ICP-H02                                                                                                                                                                                                  |
| Decisión del comprador   | ¿Es técnicamente competente? / ¿Vale la pena seguir leyendo?                                                                                                                                                      |
| Incertidumbre que reduce | Si PICC tiene la base técnica necesaria                                                                                                                                                                           |
| Mensaje propuesto        | Certificaciones: ICREA CCRD. Alianzas: Panduit. Métricas: 25+ años, 100+ proyectos, 50,000+ m² ejecutados. [Publicable condicionada — todas las métricas requieren respaldo documental interno antes de publicar] |
| Evidencia requerida      | Documentos que respalden cada métrica + permiso de uso de logotipos de partners                                                                                                                                   |
| CTA                      | Ninguno en esta sección — diseñada para retener, no para redirigir                                                                                                                                                |
| Surface de destino       | Flujo natural hacia Sección 3                                                                                                                                                                                     |
| Métrica                  | Tiempo en página; scroll depth                                                                                                                                                                                    |
| Owner                    | Dirección                                                                                                                                                                                                         |
| Datos faltantes          | No hay respaldo interno auditado de 25+ años ni 100+ proyectos; no se verificó contrato o acuerdo con Panduit. Requiere revisión antes de publicación definitiva.                                                 |

### Sección 3 — Rutas por tipo de comprador o proyecto

| Campo                    | Contenido                                                                                                                                                                                                                                                                                                                    |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Permitir que el comprador se identifique y tome la ruta correcta sin necesidad de leer toda la Home                                                                                                                                                                                                                          |
| ICP principal            | ICP-H01, ICP-H02 (y señal a H03/H04 como rutas futuras)                                                                                                                                                                                                                                                                      |
| Decisión del comprador   | ¿PICC entiende un proyecto como el mío?                                                                                                                                                                                                                                                                                      |
| Incertidumbre que reduce | Si llegué al proveedor correcto para mi tipo de proyecto                                                                                                                                                                                                                                                                     |
| Mensaje propuesto        | Tarjetas o módulos: "Data Centers e infraestructura crítica" / "Instalaciones industriales y HVAC" / "Proyectos corporativos y oficinas" / "Desarrollo inmobiliario". Cada tarjeta con descripción del tipo de proyecto y dolor principal. [Publicable condicionada — requiere definición de cuántas rutas se activan en V1] |
| Evidencia requerida      | Al menos 1 caso o descripción de alcance real por ruta activada                                                                                                                                                                                                                                                              |
| CTA                      | Botón por tarjeta → Ruta ICP correspondiente                                                                                                                                                                                                                                                                                 |
| Surface de destino       | Ruta ICP-H01 / Ruta ICP-H02                                                                                                                                                                                                                                                                                                  |
| Métrica                  | Distribución de clics por ruta; porcentaje de visits que toman alguna ruta                                                                                                                                                                                                                                                   |
| Owner                    | Comercial / Marketing                                                                                                                                                                                                                                                                                                        |
| Datos faltantes          | No hay analytics para conocer distribución real de perfil de visitante. Hipótesis de orden de tarjetas.                                                                                                                                                                                                                      |

### Sección 4 — Diferenciador principal

| Campo                    | Contenido                                                                                                                                                                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Separar a PICC de competidores genéricos mediante una afirmación verificable sobre cómo trabaja                                                                                                                                                               |
| ICP principal            | ICP-H01, ICP-H02                                                                                                                                                                                                                                              |
| Decisión del comprador   | ¿Qué la hace diferente? / ¿Por qué no usar otro contratista que conozco?                                                                                                                                                                                      |
| Incertidumbre que reduce | Si la diferencia entre PICC y otro proveedor justifica el esfuerzo de evaluarlos                                                                                                                                                                              |
| Mensaje propuesto        | "No somos un proveedor de materiales. Somos el integrador responsable del proyecto completo: diseño, ejecución, coordinación de disciplinas y entrega operativa." [Hipótesis — requiere validación con dirección antes de publicar. Publicable condicionada.] |
| Evidencia requerida      | Metodología documentada + al menos 1 caso que pruebe integración multidisciplinaria                                                                                                                                                                           |
| CTA                      | Texto: "Conoce cómo trabajamos" → Sección 6                                                                                                                                                                                                                   |
| Surface de destino       | Sección de metodología en misma página o ruta ICP                                                                                                                                                                                                             |
| Métrica                  | Tiempo en sección; CTR a "Cómo trabajamos"                                                                                                                                                                                                                    |
| Owner                    | Dirección + Comercial                                                                                                                                                                                                                                         |
| Datos faltantes          | No existe metodología documentada publicable. Este mensaje no puede publicarse en nivel E4 sin ese respaldo.                                                                                                                                                  |

### Sección 5 — Proyectos o casos destacados

| Campo                    | Contenido                                                                                                                                                                                                                                                                                  |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Objetivo                 | Proporcionar evidencia concreta de capacidad real antes de solicitar acción                                                                                                                                                                                                                |
| ICP principal            | ICP-H01, ICP-H02                                                                                                                                                                                                                                                                           |
| Decisión del comprador   | ¿Tiene experiencia comparable? / ¿Ha hecho proyectos como el mío?                                                                                                                                                                                                                          |
| Incertidumbre que reduce | Si pueden ejecutar proyectos del tamaño y tipo del comprador                                                                                                                                                                                                                               |
| Mensaje propuesto        | 2 a 3 mini-cards de proyecto con: tipo de proyecto, reto principal, resultado verificable, imagen o visual. Formato: "Cliente: sector [no nombre si no hay permiso]. Proyecto: [tipo]. Resultado: [métrica o descripción]. [Publicable condicionada — ningún caso es publicable hoy en E4] |
| Evidencia requerida      | Mínimo 1 caso E4 para H01 y 1 para H02 con permiso de publicación, imagen y datos verificables                                                                                                                                                                                             |
| CTA                      | "Ver caso completo" → página de caso. Mientras no haya caso E4: omitir o usar placeholder estructural                                                                                                                                                                                      |
| Surface de destino       | Página de caso o contacto                                                                                                                                                                                                                                                                  |
| Métrica                  | Consumo de casos; CTR de cards; tiempo en sección                                                                                                                                                                                                                                          |
| Owner                    | Dirección + Marketing                                                                                                                                                                                                                                                                      |
| Datos faltantes          | No hay ningún caso en E4. Esta sección no puede operar en modo completo en el lanzamiento inicial. Se recomienda placeholder con "Próximas referencias disponibles" o mini-case con texto sin imagen hasta obtener caso completo.                                                          |

### Sección 6 — Cómo trabaja PICC

| Campo                    | Contenido                                                                                                                                                                                                                                           |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Mostrar el proceso y metodología para reducir incertidumbre sobre cómo será trabajar con PICC                                                                                                                                                       |
| ICP principal            | ICP-H01, ICP-H02                                                                                                                                                                                                                                    |
| Decisión del comprador   | ¿Cómo funciona? / ¿Tengo idea de qué esperar si contrato?                                                                                                                                                                                           |
| Incertidumbre que reduce | Incertidumbre sobre el proceso, plazos, coordinación y responsabilidades                                                                                                                                                                            |
| Mensaje propuesto        | Pasos visibles del proceso: 1. Diagnóstico / 2. Propuesta técnica / 3. Diseño / 4. Ejecución coordinada / 5. Entrega y verificación. Con descripción breve por paso. [Hipótesis de proceso — requiere validación interna. Publicable condicionada.] |
| Evidencia requerida      | Proceso real documentado y validado por operaciones                                                                                                                                                                                                 |
| CTA                      | "Inicia tu diagnóstico" → Preevaluación                                                                                                                                                                                                             |
| Surface de destino       | Preevaluación PICC                                                                                                                                                                                                                                  |
| Métrica                  | CTR a preevaluación desde esta sección                                                                                                                                                                                                              |
| Owner                    | Operaciones + Comercial                                                                                                                                                                                                                             |
| Datos faltantes          | El proceso descrito es hipótesis. No se auditaron propuestas ni entregables reales. Requiere validación antes de publicar como proceso definitivo.                                                                                                  |

### Sección 7 — Evidencia institucional

| Campo                    | Contenido                                                                                                                                                                                                                   |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Confirmar que PICC es una empresa real, estable y con trayectoria                                                                                                                                                           |
| ICP principal            | ICP-H01, ICP-H02                                                                                                                                                                                                            |
| Decisión del comprador   | ¿Es institucionalmente confiable? / ¿Existe como empresa seria?                                                                                                                                                             |
| Incertidumbre que reduce | Riesgo institucional: si la empresa desaparece, incumple o no tiene estructura                                                                                                                                              |
| Mensaje propuesto        | Fundación: año. Equipo: número de personas. Cobertura geográfica. Sectores. Registros y certificaciones. Logotipos de certificadores o partners con permiso. [Publicable condicionada — verificar datos exactos y permisos] |
| Evidencia requerida      | Acta constitutiva o dato de fundación verificable, conteo de equipo actual, permiso de logos                                                                                                                                |
| CTA                      | Ninguno en esta sección; refuerza la decisión de continuar                                                                                                                                                                  |
| Surface de destino       | Flujo natural                                                                                                                                                                                                               |
| Métrica                  | Scroll depth hasta esta sección                                                                                                                                                                                             |
| Owner                    | Dirección                                                                                                                                                                                                                   |
| Datos faltantes          | Año exacto de fundación no verificado en repo. Tamaño de equipo no documentado. Permisos de logos no registrados.                                                                                                           |

### Sección 8 — Conocimiento o herramienta útil

| Campo                    | Contenido                                                                                                                                                                                                                                 |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Ofrecer valor antes de pedir acción comercial; capturar a buyers en etapa de exploración                                                                                                                                                  |
| ICP principal            | ICP-H01 (primario), ICP-H02                                                                                                                                                                                                               |
| Decisión del comprador   | ¿Debo actuar ahora? / ¿Cómo sé si mi proyecto está bien definido?                                                                                                                                                                         |
| Incertidumbre que reduce | Incertidumbre sobre si el proyecto está listo para cotizar o requiere trabajo previo                                                                                                                                                      |
| Mensaje propuesto        | Checklist descargable o guía breve: "10 preguntas antes de contratar un integrador de infraestructura crítica". Alternativa: artículo de alta intención vinculado. [Publicable ahora — si se redacta con información verificable interna] |
| Evidencia requerida      | Conocimiento real del equipo técnico, no contenido genérico                                                                                                                                                                               |
| CTA                      | "Descargar checklist" o "Leer guía" → captura de correo o entrada a preevaluación                                                                                                                                                         |
| Surface de destino       | Lead magnet / Preevaluación                                                                                                                                                                                                               |
| Métrica                  | Descargas o clics; correos capturados por este canal                                                                                                                                                                                      |
| Owner                    | Marketing + Técnico                                                                                                                                                                                                                       |
| Datos faltantes          | Checklist no existe todavía. Es pieza P0 del Content MVP.                                                                                                                                                                                 |

### Sección 9 — Preevaluación / diagnóstico

| Campo                    | Contenido                                                                                                                                                                                                                                                                 |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Convertir intención en primer contacto calificado                                                                                                                                                                                                                         |
| ICP principal            | ICP-H01, ICP-H02                                                                                                                                                                                                                                                          |
| Decisión del comprador   | ¿Qué siguiente paso debo tomar? / ¿Vale la pena hablar con ellos antes de tener todo definido?                                                                                                                                                                            |
| Incertidumbre que reduce | Si iniciar contacto es útil aunque el proyecto no esté completamente definido                                                                                                                                                                                             |
| Mensaje propuesto        | "¿Tienes un proyecto en mente pero aún no sabes si está listo para cotizar? Solicita una Preevaluación sin costo. Revisamos tu contexto y te orientamos en 48 horas." [Publicable condicionada — el SLA de 48 horas requiere compromiso operativo real antes de publicar] |
| Evidencia requerida      | Proceso de respuesta real documentado y operativamente comprometido                                                                                                                                                                                                       |
| CTA                      | "Solicitar Preevaluación" → Formulario                                                                                                                                                                                                                                    |
| Surface de destino       | Formulario de captura                                                                                                                                                                                                                                                     |
| Métrica                  | CTR a formulario; inicios de preevaluación                                                                                                                                                                                                                                |
| Owner                    | Comercial                                                                                                                                                                                                                                                                 |
| Datos faltantes          | SLA de respuesta no auditado. Proceso interno no formalizado todavía.                                                                                                                                                                                                     |

### Sección 10 — CTA final

| Campo                    | Contenido                                                                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo                 | Capturar al buyer que llegó al final de la Home sin haber actuado antes                                                                                       |
| ICP principal            | ICP-H01, ICP-H02                                                                                                                                              |
| Decisión del comprador   | ¿Qué siguiente paso debo tomar?                                                                                                                               |
| Incertidumbre que reduce | Fricción del "¿y ahora qué hago?" al llegar al final de la página                                                                                             |
| Mensaje propuesto        | Dos opciones claras: "Solicitar Preevaluación" y "Contactar directamente". Número y WhatsApp visibles. Nombre del responsable de contacto. [Publicable ahora] |
| Evidencia requerida      | Número activo, WhatsApp activo, nombre real del contacto                                                                                                      |
| CTA                      | Formulario de preevaluación o contacto directo                                                                                                                |
| Surface de destino       | Formulario / WhatsApp / correo                                                                                                                                |
| Métrica                  | CTR; fuente de contacto; completación de formulario                                                                                                           |
| Owner                    | Comercial                                                                                                                                                     |
| Datos faltantes          | No hay mapeo actual de qué porcentaje de contactos llegan por WhatsApp vs formulario vs correo.                                                               |

---

## 4. Rutas prioritarias por ICP

### Ruta ICP-H01 — Data Centers e Infraestructura Crítica

#### Contexto del comprador
Director de infraestructura, TI, facilities o expansión en empresa con operación digital crítica. Necesidad de ampliar, construir o certificar. Tiene presión de uptime, auditoría o cumplimiento. [Hipótesis]

#### Problema principal
No puede permitirse que un Data Center falle por error de diseño, ejecución deficiente o proveedor sin experiencia certificada. El costo de una falla supera ampliamente el costo del proyecto. [Hipótesis]

#### Resultado deseado
Infraestructura funcionando según estándar ICREA o equivalente, en el plazo comprometido, con la redundancia prometida, y con un integrador que se haga responsable de todo el alcance. [Hipótesis]

#### Riesgos que enfrenta
- Proveedor sin experiencia en infraestructura crítica certificada. [Evidencia parcial]
- Integración deficiente entre disciplinas: eléctrico, HVAC, cableado, fire suppression. [Hipótesis]
- Incumplimiento de plazo que impacta operación o lanzamiento. [Hipótesis]
- Imposibilidad de defender la elección ante comité interno. [Hipótesis]

#### Propuesta de valor para H01
"PICC diseña, construye y verifica Data Centers e infraestructura crítica con conocimiento certificado ICREA, integración completa de disciplinas y responsabilidad sobre el proyecto completo." [Publicable condicionada — requiere al menos 1 caso auditable y verificación de alcance real de certificación]

#### Capacidades PICC relevantes
- Diseño y construcción de Data Centers. [Evidencia parcial]
- Instalaciones eléctricas de media y baja tensión. [Hecho verificado]
- Climatización y HVAC de precisión. [Hecho verificado]
- Cableado estructurado. [Hecho verificado]
- Certificación ICREA CCRD. [Evidencia parcial — requiere verificar alcance exacto]
- Alianza o relación con Panduit. [Evidencia parcial — requiere verificar términos]
- Coordinación integral de disciplinas. [Hipótesis]

#### Evidencia para esta ruta
- Mínima necesaria: sección con credenciales, certificaciones y descripción de alcance. [Disponible parcialmente]
- Deseable para conversión: 1 caso comparable con datos y permiso. [No disponible — gap P0]
- Óptima: 2+ casos, metodología documentada, referencias autorizadas. [No disponible]

#### Casos recomendados para esta ruta
- Caso A: proyecto de Data Center o sala de servidores con alcance completo (eléctrico + HVAC + cableado). [Por levantar]
- Caso B: retrofit o ampliación de infraestructura crítica con continuidad operativa. [Por levantar]

#### Metodología visible
Proceso de trabajo en 5 pasos: Diagnóstico técnico → Diseño y especificación → Propuesta de alcance → Ejecución coordinada → Verificación y entrega. [Hipótesis — requiere validación operativa antes de publicar]

#### Preguntas frecuentes anticipadas
1. ¿PICC puede trabajar en instalaciones en operación?
2. ¿Cuál es el alcance exacto de la certificación ICREA?
3. ¿Cómo coordinan las disciplinas en un solo contrato?
4. ¿Cuántos proyectos de Data Center han hecho?
5. ¿Pueden hacer el proyecto completo o solo partes?
6. ¿Qué pasa si hay un problema durante la ejecución?
7. ¿Tienen referencias de proyectos similares?

Respuestas a estas preguntas son backlog de contenido P0. No publicar sin respaldo real.

#### CTA de la ruta
Primario: "Solicitar Preevaluación de mi proyecto" → Formulario.
Secundario: "Hablar con un especialista" → WhatsApp / correo.

#### Diagnóstico diferenciado para H01
Pregunta de calificación clave: "¿Tu proyecto requiere cumplir algún estándar de disponibilidad o certificación? (Tier, ICREA, ASHRAE, etc.)."
Si sí: lead clasificado como H01 alto valor. Asignar a comercial + técnico en < 24 horas.
Si no: evaluar si el proyecto tiene características críticas igualmente antes de desclasificar.

#### Siguiente paso
Preevaluación PICC → Reunión técnica-comercial → Propuesta de alcance.

---

### Ruta ICP-H02 — Instalaciones Industriales y HVAC Crítico

#### Contexto del comprador
Director general, de operaciones o mantenimiento de planta o empresa industrial. Necesita ampliar capacidad, rehabilitar instalaciones o mejorar confiabilidad sin paralizar producción. [Hipótesis]

#### Problema principal
No puede parar o comprometer la operación durante la obra. El costo de una hora de paro es cuantificable y significativo. Necesita un contratista que lo entienda antes de presentar una propuesta. [Hipótesis]

#### Resultado deseado
Instalaciones mejoradas o nuevas, ejecutadas sin afectar el flujo productivo, con documentación de lo realizado y personal que supervise hasta la entrega. [Hipótesis]

#### Riesgos que enfrenta
- Contratista que no dimensiona el impacto de la obra en la operación. [Hipótesis]
- Calidad de instalación que compromete seguridad o eficiencia futura. [Hipótesis]
- Plazos que se extienden y generan sobrecostos o cierres forzados. [Hipótesis]
- Proveedor que no cumple normativa de seguridad industrial. [Hipótesis]

#### Propuesta de valor para H02
"PICC ejecuta instalaciones industriales críticas — eléctricas, HVAC y cableado — con metodología de obra en operación, coordinando para minimizar impacto en producción." [Publicable condicionada — requiere validación de que esta promesa refleja capacidad real documentada]

#### Capacidades PICC relevantes
- Instalaciones eléctricas industriales. [Hecho verificado]
- Climatización industrial y HVAC. [Hecho verificado]
- Cableado estructurado industrial. [Hecho verificado]
- Obra en instalaciones en operación. [Hipótesis]
- Coordinación de subcontratistas. [Hipótesis]
- Documentación técnica y entrega. [Hipótesis]

#### Evidencia para esta ruta
- Mínima necesaria: descripción de tipos de proyecto industrial y disciplinas. [Disponible]
- Deseable para conversión: 1 caso industrial con reto de operación continua. [No disponible — gap P0]
- Óptima: 2 casos, checklist de obra en operación, referencia. [No disponible]

#### Casos recomendados para esta ruta
- Caso A: instalación eléctrica en planta activa con fases para no parar línea. [Por levantar]
- Caso B: HVAC en nave industrial con continuidad operativa y entrega documentada. [Por levantar]

#### Metodología visible
Proceso: Levantamiento en sitio → Planificación de fases por impacto operativo → Propuesta técnica → Ejecución por ventanas → Pruebas y entrega. [Hipótesis — requiere validación]

#### Preguntas frecuentes anticipadas
1. ¿Pueden trabajar sin parar mi producción?
2. ¿Qué tan rápido pueden empezar?
3. ¿Qué normas de seguridad industrial cumplen?
4. ¿Quién supervisa la obra en mi planta?
5. ¿Pueden hacer diagnóstico antes de proponer?
6. ¿Cuánto tarda un proyecto típico?
7. ¿Tienen experiencia en mi tipo de industria?

#### CTA de la ruta
Primario: "Solicitar visita técnica" o "Preevaluación de instalaciones" → Formulario H02.
Secundario: "Hablar con un especialista industrial" → WhatsApp.

#### Diagnóstico diferenciado para H02
Pregunta de calificación clave: "¿El proyecto requiere ejecutarse mientras la planta sigue operando?"
Si sí: lead H02 alto valor. Asignar técnico especializado en < 48 horas para agenda de visita.
Si no: continuar evaluación de alcance antes de clasificar.

#### Siguiente paso
Preevaluación PICC o visita técnica directa → Discovery en sitio → Propuesta técnica por fases.

---

## 5. Propuesta de valor

### Propuesta general de PICC

| Campo                  | Contenido                                                                                                                                                                                                  |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Problema               | Proyectos de infraestructura crítica, industrial o corporativa que involucran múltiples disciplinas técnicas y donde una mala ejecución tiene consecuencias operativas y económicas significativas         |
| Resultado              | Instalaciones técnicamente correctas, ejecutadas por un integrador responsable del proyecto completo, que no transfiere el riesgo al cliente                                                               |
| Mecanismo              | Diseño + coordinación multidisciplinaria + ejecución directa + verificación y entrega documentada                                                                                                          |
| Evidencia              | Certificaciones ICREA CCRD, relación con Panduit, 25+ años de fundador, 100+ proyectos, 50,000+ m² ejecutados [Publicable condicionada — todas requieren respaldo interno antes de publicación definitiva] |
| Diferenciador          | Integración de disciplinas bajo un solo responsable vs. múltiples contratistas descoordinados [Hipótesis — no demostrado en caso público]                                                                  |
| Riesgo reducido        | Riesgo técnico, de coordinación, de plazo y de reputación interna del tomador de decisión                                                                                                                  |
| Objeciones anticipadas | Costo vs. contratistas individuales / No conozco referencias / ¿Tienen capacidad para mi tamaño?                                                                                                           |
| Límites de la promesa  | PICC no garantiza plazos sin información completa del proyecto. No autogestiona permisos de terceros. No desarrolla diseño arquitectónico. [Hipótesis — verificar límites reales]                          |
| Clasificación          | Publicable condicionada en su totalidad. No publicar sin caso auditable + validación de diferenciador.                                                                                                     |

### Propuesta para ICP-H01

| Campo           | Contenido                                                                                                                                                                  |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Problema        | Riesgo de downtime, incumplimiento de certificación o falla en infraestructura crítica por proveedor sin experiencia especializada                                         |
| Resultado       | Data Center o infraestructura crítica certificable, redundante y entregada con documentación técnica completa                                                              |
| Mecanismo       | Diseño certificado + integración eléctrica + HVAC de precisión + cableado + verificación ICREA                                                                             |
| Evidencia       | Certificación ICREA CCRD [Evidencia parcial — verificar alcance exacto]; Panduit [Evidencia parcial — verificar términos]; métricas de proyectos [Publicable condicionada] |
| Diferenciador   | Certificación + integración en un solo contratista [Hipótesis]                                                                                                             |
| Riesgo reducido | Downtime, falla de certificación, proveedor sin experiencia crítica, dificultad de defensa ante comité                                                                     |
| Objeciones      | Costo / ¿Han hecho proyectos de mi escala? / ¿Son solo instaladores o realmente integran?                                                                                  |
| Límites         | No garantizar uptime durante ejecución sin plan acordado. No proponer si el proyecto no es crítico por naturaleza.                                                         |
| Clasificación   | No publicable todavía como promesa fuerte. Publicable condicionada como descripción de capacidad.                                                                          |

### Propuesta para ICP-H02

| Campo           | Contenido                                                                                                                                 |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Problema        | Necesidad de mejorar instalaciones críticas sin parar producción, con contratista que no entiende el entorno industrial                   |
| Resultado       | Instalaciones mejoradas ejecutadas en fases sin impacto crítico a la operación, documentadas y verificadas                                |
| Mecanismo       | Levantamiento en sitio + planificación por fases de impacto mínimo + ejecución técnica + entrega documentada                              |
| Evidencia       | Disciplinas industriales confirmadas [Hecho verificado]; metodología de obra en operación [Hipótesis]; casos industriales [No disponible] |
| Diferenciador   | Planificación por impacto operativo antes de proponer [Hipótesis]                                                                         |
| Riesgo reducido | Paro de producción, incumplimiento técnico, proveedor sin norma de seguridad industrial                                                   |
| Objeciones      | ¿Han trabajado en mi industria? / ¿Cuánto afectan la producción? / ¿Son más caros que mi proveedor actual?                                |
| Límites         | No proponer obra en operación sin levantamiento real previo. No autogestionar permisos de seguridad del cliente.                          |
| Clasificación   | No publicable todavía como promesa fuerte. Publicable condicionada con casos reales.                                                      |

---

## 6. Trust Assets del MVP

| Asset ID | Asset                                     | Decisión que soporta                                      | ICP           | Evidencia disponible | Permiso                | Owner                   | Brecha                                                                 | Esfuerzo estimado | Prioridad | Surface                   |
| -------- | ----------------------------------------- | --------------------------------------------------------- | ------------- | -------------------- | ---------------------- | ----------------------- | ---------------------------------------------------------------------- | ----------------- | --------- | ------------------------- |
| TA-01    | Caso Data Center / infra crítica          | Es técnicamente competente / Tiene experiencia comparable | H01           | E0                   | Pendiente              | Dirección + Operaciones | Sin caso documentado ni permiso                                        | Alto              | P0        | Ruta H01 / Home Sección 5 |
| TA-02    | Caso instalación industrial               | PICC entiende un proyecto como el mío                     | H02           | E0                   | Pendiente              | Dirección + Operaciones | Sin caso documentado ni permiso                                        | Alto              | P0        | Ruta H02 / Home Sección 5 |
| TA-03    | Certificaciones ICREA CCRD documentadas   | Es técnicamente competente                                | H01           | E2                   | Pendiente verificación | Dirección               | Alcance exacto de certificación no documentado en repo                 | Bajo              | P0        | Home / Ruta H01           |
| TA-04    | Términos de relación Panduit              | Es técnicamente competente                                | H01           | E2                   | Pendiente              | Dirección               | Tipo de relación no verificado; puede ser distribuidor, partner u otro | Bajo              | P0        | Home / Ruta H01           |
| TA-05    | Respaldo de métricas: años, proyectos, m² | Es institucionalmente confiable                           | H01, H02      | E2                   | Interno                | Dirección               | Ninguna métrica tiene fuente documental en repo                        | Bajo              | P0        | Home Sección 2            |
| TA-06    | Fotografías de proyectos con permiso      | Tiene experiencia comparable                              | H01, H02      | E0                   | Pendiente              | Dirección + Marketing   | Sin inventario de fotos autorizadas                                    | Medio             | P0        | Home / Casos / Rutas      |
| TA-07    | Metodología de trabajo documentada        | Cómo funciona / Qué esperar                               | H01, H02      | E0                   | N/A (interno)          | Operaciones + Comercial | Sin proceso documentado verificado                                     | Medio             | P0        | Sección 6 / Ruta ICP      |
| TA-08    | Referencia autorizada H01                 | Puedo defender la contratación                            | H01           | E0                   | Pendiente              | Dirección               | Sin referencias autorizadas para publicar                              | Alto              | P1        | Ruta H01                  |
| TA-09    | Referencia autorizada H02                 | Puedo defender la contratación                            | H02           | E0                   | Pendiente              | Dirección               | Sin referencias autorizadas para publicar                              | Alto              | P1        | Ruta H02                  |
| TA-10    | Ficha de equipo técnico                   | Es institucionalmente confiable                           | H01, H02      | E1                   | Interno                | Dirección               | Equipo no documentado con perfil publicable                            | Bajo-medio        | P1        | Home / Rutas              |
| TA-11    | Registro legal / fiscal / cumplimiento    | Es institucionalmente confiable                           | H01, H02, H04 | E0-E2                | Interno                | Dirección               | No disponible en repo                                                  | Bajo              | P1        | Home Sección 7            |
| TA-12    | Testimonios de clientes                   | Puedo confiar en su criterio                              | H02, H03, H05 | E0                   | Pendiente              | Dirección + Comercial   | Sin testimonios estructurados ni autorizados                           | Alto              | P2        | Home / Casos              |
| TA-13    | Comparativo de propuesta vs. alternativas | Su propuesta es comparable                                | H01, H04      | E0                   | N/A                    | Comercial               | Sin propuestas auditadas                                               | Alto              | P2        | Propuesta / Reunión       |
| TA-14    | FAQ técnica publicable                    | Es técnicamente competente                                | H01, H02      | E0                   | N/A                    | Técnico + Comercial     | Sin respuestas redactadas ni validadas                                 | Medio             | P1        | Rutas ICP                 |

---

## 7. Sistema de casos de éxito V1

### Formato estándar de caso

Cada caso PICC deberá contener los siguientes campos en orden:

1. **Ficha técnica**: tipo de proyecto, año, ubicación (a nivel ciudad o zona si hay restricción de confidencialidad), superficie, disciplinas involucradas, alcance principal.
2. **Contexto**: tipo de organización, situación previa al proyecto.
3. **Problema o reto**: qué necesitaba resolver, qué riesgo existía.
4. **Alcance de PICC**: qué hizo PICC exactamente, qué quedó excluido.
5. **Decisiones técnicas relevantes**: por qué se eligieron ciertas soluciones técnicas.
6. **Proceso**: cómo se ejecutó; fases; coordinación.
7. **Resultado**: qué cambió para el cliente.
8. **Métricas verificables**: si las hay — superficie instalada, potencia, tiempo de ejecución, uptime alcanzado, fases completadas.
9. **Evidencia visual**: fotografías, planos o renders con permiso explícito del cliente.
10. **Testimonio o responsable**: nombre o cargo del referente de cliente, solo si hay permiso. Si no: omitir.
11. **Restricciones de publicación**: nivel de confidencialidad, qué puede mostrarse y qué no.
12. **CTA relacionado**: qué acción se sugiere al lector al terminar el caso.

### Reglas del sistema de casos

- Un caso solo llega a la biblioteca si el permiso está confirmado por escrito o verbal explícito documentado.
- No publicar nombre del cliente sin permiso, aunque sea conocido públicamente.
- No publicar fotos de obra con personas sin consentimiento.
- Un caso sin métricas verificables puede publicarse si tiene contexto, proceso y resultado descritos honestamente.
- Un caso E3 puede usarse en venta asistida aunque no se publique en sitio.

### Shortlist de casos potenciales V1

| Caso ID | Descripción tentativa                                        | ICP relevante | Fuerza comercial | Calidad de evidencia actual | Permiso actual | Completitud | Esfuerzo para convertir | Prioridad    |
| ------- | ------------------------------------------------------------ | ------------- | ---------------- | --------------------------- | -------------- | ----------- | ----------------------- | ------------ |
| CASO-01 | Data Center o sala servidores — proyecto completo            | H01           | Muy alta         | E1-E2                       | Pendiente      | Baja        | Alto                    | P0 — crítico |
| CASO-02 | Instalación eléctrica industrial en planta activa            | H02           | Alta             | E1-E2                       | Pendiente      | Baja        | Alto                    | P0 — crítico |
| CASO-03 | Proyecto de climatización industrial o HVAC crítico          | H02           | Alta             | E1-E2                       | Pendiente      | Baja        | Medio-alto              | P0           |
| CASO-04 | Remodelación o adecuación corporativa/oficinas               | H03           | Media            | E1                          | Pendiente      | Baja        | Medio                   | P1           |
| CASO-05 | Proyecto de desarrollo inmobiliario (amenity o urbanización) | H04           | Alta             | E1 (señal BeGrand)          | Pendiente      | Muy baja    | Alto                    | P1           |
| CASO-06 | Proyecto residencial premium o patrimonial                   | H06           | Media            | E1                          | Pendiente      | Baja        | Medio                   | P2           |

**Nota de estado**: no existe ningún caso en nivel E4 al 2026-07-15. La shortlist representa candidatos potenciales que requieren levantamiento activo, permiso de cliente y empaquetamiento. CASO-01 y CASO-02 son bloqueadores del MVP.

### Proceso de construcción de caso

1. Identificar proyecto candidato desde memoria del equipo o archivo interno.
2. Validar que el cliente pueda ser contactado.
3. Solicitar permiso de uso con alcance definido (nombre, foto, métricas, testimonio).
4. Entrevistar al responsable de PICC del proyecto.
5. Complementar con documentos técnicos existentes.
6. Redactar borrador de caso.
7. Revisar con cliente si el permiso lo requiere.
8. Clasificar nivel de evidencia y superficie permitida.
9. Agregar a Biblioteca de Evidencia.

---

## 8. Preevaluación PICC — Diseño

### Nombre

"Preevaluación PICC" se mantiene como nombre provisional. Evaluación del nombre:

| Alternativa                | Ventaja                              | Desventaja                                                       | Veredicto             |
| -------------------------- | ------------------------------------ | ---------------------------------------------------------------- | --------------------- |
| Preevaluación PICC         | Claro, propio, no genérico           | Suena a proceso interno, no a beneficio para el cliente          | Provisional           |
| Diagnóstico de Proyecto    | Centra en el cliente, no en PICC     | Puede generar expectativa de entrega de planos o informe técnico | A evaluar             |
| Preevaluación Técnica      | Suena técnico y serio                | Puede disuadir a buyers más comerciales (H04)                    | A evaluar con H01/H02 |
| Consulta inicial sin costo | Claro en beneficio para el comprador | Puede atraer consultas sin calificación                          | Riesgo comercial      |

Recomendación: usar "Diagnóstico de Proyecto — sin costo" como nombre de cara al comprador, manteniendo "Preevaluación PICC" como nombre interno del proceso. Validar con dirección comercial antes de publicar.

### Promesa

"Revisamos el contexto de tu proyecto y te damos una orientación técnica inicial sobre alcance, factibilidad y pasos recomendados. Sin costo. Sin compromiso de contratación."

### Alcance

- PICC recibe la información básica del proyecto.
- PICC revisa con criterio técnico y comercial.
- PICC devuelve una orientación: ¿es el tipo de proyecto donde PICC agrega valor? ¿Qué información adicional necesita? ¿Cuál sería un siguiente paso razonable?
- No es una cotización definitiva.
- No es un diseño ni especificación técnica.
- No es un compromiso de precio.

### Qué recibe el prospecto

- Respuesta en 48 horas hábiles con: confirmación de recibo, indicación de si el proyecto cabe en el perfil PICC, preguntas adicionales si se necesitan, y propuesta de siguiente paso (reunión técnica o solicitud de información adicional).
- Si el proyecto no encaja: PICC lo dice claramente, sin dejar al prospecto en silencio.

### Qué no recibe

- Cotización.
- Diseño o especificación.
- Presupuesto definitivo.
- Acceso a materiales internos de PICC.
- Compromiso de ejecución.

### Tiempo objetivo

- Respuesta inicial: 48 horas hábiles desde envío. [Requiere compromiso operativo real antes de publicar]
- Primera reunión técnica si aplica: dentro de 5 días hábiles desde respuesta positiva.

### Preguntas de la preevaluación

#### Bloque A — Tipo de proyecto (1-2 preguntas)
1. ¿Cuál describe mejor tu proyecto? (opciones: Data Center / Infraestructura crítica, Instalación industrial / planta / bodega, Oficinas o espacio corporativo, Desarrollo inmobiliario, Residencial o patrimonio, Otro).
2. ¿En qué etapa está tu proyecto? (opciones: Idea / exploración, Prefactibilidad / presupuesto inicial, Diseño, Listo para cotizar, En ejecución y necesito apoyo puntual).

#### Bloque B — Contexto y urgencia (2-3 preguntas)
3. ¿Cuál es el principal reto o preocupación de tu proyecto?
4. ¿Tienes una fecha objetivo o restricción de tiempo relevante?
5. ¿El proyecto requiere ejecutarse mientras sigues operando? (Solo para H02 — puede ser condicional)

#### Bloque C — Contacto (3-4 campos)
6. Nombre.
7. Empresa.
8. Teléfono o WhatsApp.
9. Correo.

Documento o plano opcional: campo de carga de archivo no obligatorio.

### Criterio de elegibilidad

Un proyecto es elegible para Preevaluación PICC si:
- Involucra al menos una disciplina técnica instalada (eléctrico, HVAC, cableado, obra).
- El alcance implica complejidad técnica o riesgo operativo.
- El comprador tiene capacidad de decisión o influencia sobre el proyecto.

No es elegible si:
- Es solo solicitud de materiales o suministro.
- Es mantenimiento preventivo rutinario de bajo valor.
- No hay ningún tomador de decisión identificado.

### Scoring

| Dimensión        | Señal alta valor                            | Señal baja valor                |
| ---------------- | ------------------------------------------- | ------------------------------- |
| Tipo de proyecto | Data Center, planta industrial, desarrollo  | Solo mantenimiento o suministro |
| Etapa            | Listo para cotizar o diseño                 | Idea sin fecha ni presupuesto   |
| Urgencia         | Fecha concreta o restricción operativa      | Sin urgencia definida           |
| Reto declarado   | Riesgo operativo, certificación, criticidad | Solo precio                     |
| Empresa          | Corporativo, industrial o desarrollador     | Particular sin contexto         |

### Asignación interna

| Score                                                 | Asignación                                               |
| ----------------------------------------------------- | -------------------------------------------------------- |
| Alto (3+ señales altas)                               | Comercial senior + Técnico en < 24 horas                 |
| Medio (1-2 señales altas)                             | Comercial en < 48 horas                                  |
| Bajo (0 señales altas o criterios de no elegibilidad) | Respuesta estándar y registro; no asignar tiempo técnico |

### Validación humana

Toda preevaluación es revisada por una persona antes de responder. DAVINCI puede apoyar en síntesis de contexto y borrador de respuesta, pero la decisión y el envío son del responsable comercial.

### Respuesta

- Respuesta positiva: "Revisamos tu proyecto. Parece ser exactamente el tipo de caso donde PICC puede agregar valor. Te propongo una llamada de 30 minutos para entender mejor el contexto antes de proponer cualquier cosa. ¿Cuándo tienes disponibilidad?"
- Respuesta con preguntas adicionales: "Recibimos tu solicitud. Para orientarte mejor, necesito un dato adicional: [pregunta específica]. Cuando lo tenga te respondo en 24 horas."
- Respuesta de descarte honesto: "Revisamos tu proyecto. En este momento el tipo de alcance que describes no es el perfil en que PICC tiene más experiencia para agregar valor. Te sugiero [opción o referencia si es posible]." (Solo si el desajuste es claro.)

### CTA posterior

Después de respuesta positiva → agendar reunión técnica-comercial.
Después de reunión → propuesta de alcance o siguiente paso.

### SLA

| Paso                   | SLA objetivo                                       |
| ---------------------- | -------------------------------------------------- |
| Acuse de recibo        | 2 horas en horario hábil                           |
| Respuesta con criterio | 48 horas hábiles                                   |
| Propuesta de reunión   | Dentro de la respuesta o en < 24 horas adicionales |
| Fecha de reunión       | < 5 días hábiles desde respuesta positiva          |

### Owner

- Responsable de clasificación: Comercial (con apoyo de ZEUS para síntesis).
- Responsable de respuesta: Comercial senior.
- Responsable de reunión: Comercial + Técnico por ICP.

### Métricas de preevaluación

- Número de preevaluaciones iniciadas por semana.
- Porcentaje de finalización del formulario.
- Distribución por ICP de formularios completados.
- Porcentaje que recibe respuesta dentro de SLA.
- Porcentaje que avanza a reunión.
- Porcentaje que avanza a propuesta.
- Tasa de conversión de preevaluación a oportunidad calificada.

---

## 9. Formulario de captura justificado

### Principio

El formulario debe pedir solo lo necesario para clasificar y responder. Cada campo que se agrega aumenta el abandono. Priorizar captura mínima con enriquecimiento progresivo.

### Versión inicial del formulario (paso 1)

| Campo                                       | Razón                                                            | Decisión habilitada                         | Obligatorio | Uso                       | Riesgo de abandono |
| ------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------- | ----------- | ------------------------- | ------------------ |
| Tipo de proyecto (selección)                | Permite clasificar ICP inmediatamente                            | Asignación, prioridad, respuesta            | Sí          | Clasificación y respuesta | Bajo               |
| Etapa del proyecto (selección)              | Permite calibrar urgencia y profundidad de respuesta             | Scoring de urgencia                         | Sí          | Priorización              | Bajo               |
| Principal reto o preocupación (texto libre) | Captura intención real y contexto; imposible inferir             | Calificación y personalización de respuesta | Sí          | Respuesta y scoring       | Bajo-medio         |
| Nombre                                      | Permite personalizar respuesta                                   | Comunicación básica                         | Sí          | CRM y respuesta           | Mínimo             |
| Empresa                                     | Permite investigación básica pre-reunión                         | Calificación y contexto                     | Sí          | Scoring e investigación   | Bajo               |
| Teléfono o WhatsApp                         | Canal de respuesta rápida, preferido en México                   | Contacto                                    | Sí          | Respuesta inmediata       | Bajo               |
| Correo                                      | Canal formal de seguimiento                                      | Respuesta y CRM                             | Sí          | CRM y seguimiento         | Mínimo             |
| Fecha deseada                               | Calibra urgencia                                                 | Priorización                                | No          | Scoring                   | Bajo               |
| Documento o plano (carga opcional)          | Acelera el discovery técnico si el prospecto lo tiene disponible | Calificación técnica anticipada             | No          | Investigación previa      | Mínimo             |

Campos excluidos de paso 1 con justificación:
- Presupuesto estimado: genera abandono; se obtiene mejor en reunión después de trust establecido.
- Superficie exacta: no necesaria para clasificar; se obtiene en discovery.
- Ubicación específica: suficiente con ciudad o zona, no dirección exacta.

### Versión enriquecida (paso 2 — opcional / reunión)

Campos a obtener en la reunión o segundo contacto:
- Presupuesto estimado o rango.
- Restricciones de tiempo o fases.
- Otros proveedores considerados.
- Documentos técnicos disponibles.
- Tomadores de decisión involucrados.

### Regla de progresividad

Si el comprador completa el paso 1 y avanza a reunión, el paso 2 se obtiene en conversación, no en formulario. No crear barrera de enriquecimiento antes del primer contacto humano.

---

## 10. Flujo interno del lead

```
Lead recibido (formulario, WhatsApp o correo)
         ↓
Registro (CRM o sistema provisional)
         ↓
Clasificación por ICP y scoring
         ↓
Elegibilidad
         ↓
Asignación interna
         ↓
Investigación preliminar
         ↓
Respuesta al prospecto
         ↓
Reunión técnica-comercial
         ↓
Propuesta de alcance o descarte documentado
```

### Detalle por paso

| Paso                 | Responsable                     | Sistema habilitador                                                                                 | Entrada                                | Salida                                                                           | SLA                             | Criterio                                                                           | Métrica                                           | Excepción                                                        |
| -------------------- | ------------------------------- | --------------------------------------------------------------------------------------------------- | -------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------- | ---------------------------------------------------------------- |
| Recepción            | Sistema (formulario o canal)    | Formulario web / WhatsApp / correo                                                                  | Datos del formulario o mensaje         | Notificación al responsable                                                      | Inmediato o <2h                 | Cualquier envío completo                                                           | Número de leads recibidos                         | Lead incompleto: solicitar dato faltante antes de registrar      |
| Registro             | Comercial                       | CRM provisional (hoja, CRM o ZEUS)                                                                  | Notificación                           | Lead registrado con ICP tentativo y fecha                                        | <2h hábiles                     | Todo lead debe tener registro antes de responder                                   | Porcentaje de leads registrados en <2h            | Lead duplicado: fusionar registros                               |
| Clasificación        | ZEUS + Comercial                | ZEUS para síntesis; Comercial para validación                                                       | Lead registrado + datos del formulario | ICP asignado, score de prioridad, resumen de contexto                            | <4h hábiles                     | Clasificación basada en tipo de proyecto + reto + empresa                          | Distribución de clasificaciones por ICP           | Lead ambiguo: comercial decide con criterio propio               |
| Elegibilidad         | Comercial                       | Criterios del Sección 8                                                                             | Clasificación                          | Veredicto: elegible / no elegible / información insuficiente                     | <4h hábiles                     | Criterios definidos en Preevaluación                                               | Porcentaje elegibles vs. total                    | Caso borde: escalar a Dirección                                  |
| Asignación           | Comercial                       | CRM / calendario                                                                                    | Elegibilidad + score                   | Owner asignado con fecha límite de respuesta                                     | <4h hábiles para alto score     | Score alto: comercial senior + técnico. Medio: comercial. Bajo: respuesta estándar | Cumplimiento de asignación en tiempo              | Owner no disponible: backup designado                            |
| Investigación        | ZEUS + Comercial + DAVINCI      | ZEUS para research de empresa; DAVINCI para análisis de contexto; BrickEye si hay datos de proyecto | Datos de lead + empresa declarada      | Brief de contexto: empresa, sector, posibles proyectos previos, señales públicas | <24h                            | Solo para leads alto y medio score                                                 | Porcentaje con brief preparado antes de reunión   | Sin información pública: brief vacío, anotar y proceder          |
| Respuesta            | Comercial                       | Correo / WhatsApp                                                                                   | Brief + clasificación                  | Respuesta enviada al prospecto con siguiente paso                                | 48h hábiles (SLA público)       | Toda respuesta debe proponer un siguiente paso concreto                            | Porcentaje de respuestas dentro de SLA            | Lead sin respuesta posible (datos inválidos): registrar y cerrar |
| Reunión              | Comercial + Técnico             | Calendario / videollamada / visita                                                                  | Respuesta positiva                     | Reunión agendada                                                                 | <5 días hábiles desde respuesta | Toda reunión debe terminar con un acuerdo de siguiente paso                        | Tasa de agendamiento desde respuesta positiva     | Cancelación: reagendar en <48h                                   |
| Propuesta o descarte | Comercial + Técnico + Dirección | Plantilla de propuesta (por crear)                                                                  | Información de reunión                 | Propuesta formal o descarte documentado                                          | Variable según complejidad      | Propuesta en < 10 días hábiles para H01/H02 estándar                               | Tasa de conversión a propuesta; razón de descarte | Descarte: registrar razón para win/loss                          |

### Papel de tecnologías y agentes

| Actor     | Rol                                                                                       | No es owner de                                                     |
| --------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| ZEUS      | Clasificación de ICP, research de empresa, síntesis de brief, análisis de formulario      | La decisión comercial de elegibilidad ni la respuesta al prospecto |
| DAVINCI   | Análisis de contexto de proyecto, borrador de respuesta preliminar, síntesis de propuesta | La validación técnica del alcance ni el compromiso comercial       |
| BrickEye  | Estimación de contexto de proyecto si hay datos de superficie o tipo de obra              | La decisión de precio ni la propuesta final                        |
| Comercial | Clasificación validada, respuesta, reunión, propuesta                                     | Ejecución técnica                                                  |
| Técnico   | Discovery técnico, validación de alcance, propuesta técnica                               | Clasificación comercial ni respuesta al lead                       |
| Dirección | Aprobación de propuestas complejas, decisiones de elegibilidad en casos borde             | Gestión de leads rutinarios                                        |

---

## 11. Content MVP

### Principio

Máximo contenido mínimo necesario para apoyar las decisiones del MVP. Calidad e intención sobre volumen.

### Inventario de piezas

| ID     | Título provisional                                                     | ICP      | Pregunta que responde                                     | Decisión del comprador                                 | Intención                    | Evidencia requerida                                                   | Formato                             | CTA                                 | Surface                   | Owner               | Métrica                                        | Mantenimiento                                    |
| ------ | ---------------------------------------------------------------------- | -------- | --------------------------------------------------------- | ------------------------------------------------------ | ---------------------------- | --------------------------------------------------------------------- | ----------------------------------- | ----------------------------------- | ------------------------- | ------------------- | ---------------------------------------------- | ------------------------------------------------ |
| CNT-01 | Cómo planear un Data Center sin comprometer disponibilidad             | H01      | ¿Qué debo considerar antes de contratar?                  | Debo actuar ahora / Vale la pena considerar a PICC     | Alta intención / decisión    | Conocimiento técnico interno del equipo                               | Artículo largo / guía               | Solicitar Preevaluación             | Ruta H01 / blog / SEO     | Técnico + Marketing | Visitas, tiempo en página, CTR a Preevaluación | Revisión anual o ante cambio de estándar técnico |
| CNT-02 | Cómo ejecutar instalaciones industriales sin parar producción          | H02      | ¿Cómo sé si el contratista entiende mi entorno?           | PICC entiende un proyecto como el mío                  | Alta intención / confianza   | Proceso real de obra en operación                                     | Artículo / guía práctica            | Solicitar visita técnica            | Ruta H02 / blog / SEO     | Técnico + Marketing | Visitas, tiempo, CTR                           | Revisión anual                                   |
| CNT-03 | Cómo elegir a un integrador antes de contratar: 5 criterios técnicos   | H01, H02 | ¿Por qué debo comparar? ¿Qué debo pedir?                  | Vale la pena considerar a PICC / Qué la hace diferente | Alta intención / comparación | Criterios reales que diferencias integradoras de contratistas simples | Artículo / checklist                | Descargar checklist                 | Blog / Ruta ICP / Home S8 | Comercial + Técnico | Visitas, descargas                             | Revisión cada 6 meses                            |
| CNT-04 | Qué exige un Data Center de clase empresarial: guía de certificaciones | H01      | ¿Cuáles son los estándares que debo conocer?              | Es técnicamente competente                             | Trust / confianza técnica    | Conocimiento de ICREA, Tier, ASHRAE                                   | Guía técnica                        | Consultar a PICC sobre tu caso      | Ruta H01 / Home           | Técnico             | Visitas, tiempo, consultas                     | Revisión ante cambio normativo                   |
| CNT-05 | Lista de verificación antes de contratar instalaciones industriales    | H02      | ¿Estoy listo para contratar? / ¿Qué debo tener preparado? | Qué alcance necesito / Qué siguiente paso              | Alta intención / captura     | Proceso real de levantamiento y discovery                             | Checklist descargable (lead magnet) | Descargar / Solicitar Preevaluación | Home S8 / Ruta H02        | Técnico + Comercial | Descargas, conversión a formulario             | Revisión semestral                               |

### Notas del Content MVP

- CNT-01 y CNT-02 son piezas P0: habilitan las rutas ICP y SEO básico de alta intención.
- CNT-03 es la pieza de mayor alcance (sirve a ambos ICPs) y tiene potencial de referral y uso en reuniones.
- CNT-04 es trust-building para H01; importante para la etapa de validación.
- CNT-05 es el lead magnet de la Home S8; habilita captura de correo antes del formulario de preevaluación.
- No crear más piezas hasta medir el rendimiento de estas cinco.
- Ninguna pieza debe publicarse con información no verificada internamente.

---

## 12. Decision Coverage objetivo del MVP

### Definición de meta

La meta del MVP no es 100% de cobertura. Es el nivel mínimo que permite operar responsablemente: atraer al buyer correcto, sostener su consideración, facilitar su decisión y capturar la oportunidad.

### Coverage por surface con MVP activo

| Surface                | Cobertura actual (pre-MVP)    | Cobertura objetivo post-MVP          | Decisiones cubiertas                                                         | Decisiones aún no cubiertas                                               | Nota                                                                        |
| ---------------------- | ----------------------------- | ------------------------------------ | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Home                   | 25% — parcial e inconsistente | 55-65%                               | Debo actuar ahora / Vale la pena considerar a PICC / Qué siguiente paso      | Es técnicamente competente (sin caso) / Puedo defender la contratación    | Requiere TA-01 a TA-07                                                      |
| Ruta ICP-H01           | 0% — no existe                | 65-70%                               | PICC entiende mi caso / Es técnicamente competente / Qué siguiente paso      | Tiene experiencia comparable (requiere caso) / Puedo defender ante comité | Requiere CASO-01 para pasar de 50% a 70%                                    |
| Ruta ICP-H02           | 0% — no existe                | 60-65%                               | PICC entiende mi caso / Es institucionalmente confiable / Qué siguiente paso | PICC entiende obra en operación (sin metodología publicable)              | Requiere CASO-02 y metodología documentada                                  |
| Casos                  | 0% — no existen               | 75-80% cuando haya 1 caso E4 por ICP | Tiene experiencia comparable / Es técnicamente competente                    | Puedo defender ante comité (requiere propuesta comparable)                | Depende de CASO-01 y CASO-02                                                |
| Preevaluación          | 0% — no existe                | 85-90%                               | Qué siguiente paso / Qué alcance necesito / Qué riesgos existen              | Propuesta comparable                                                      | Diseñada específicamente para reducir incertidumbre de decisión de contacto |
| Contacto y seguimiento | 30% — parcial, sin ICP        | 70-75%                               | Qué siguiente paso / Quién responde / Cuándo                                 | Propuesta comparable y defendible                                         | Requiere SLA y proceso formalizado                                          |

### Umbral mínimo para lanzar responsablemente

El MVP puede lanzarse cuando:
- Home tiene cobertura ≥ 50% en decisiones críticas de H01 y H02.
- Rutas ICP existen aunque no tengan caso completo.
- Preevaluación está diseñada y operable (aunque sea manualmente).
- Existe al menos un trust asset E3+ para H01 y H02 (puede ser metodología o credencial, no necesariamente caso publicable).
- El proceso de respuesta tiene SLA real, no solo prometido.

El MVP no debe lanzarse sin:
- Proceso de respuesta formalizado.
- Al menos 1 asset de credencial verificado (certificaciones o métricas con respaldo).
- CTA específico por ICP en funcionamiento.

---

## 13. Métricas del MVP

### Registro de métricas

| ID     | Evento                                              | Fuente                             | Owner                 | Frecuencia | Baseline actual                    | Meta inicial (hipótesis)                              | Limitación                                                 |
| ------ | --------------------------------------------------- | ---------------------------------- | --------------------- | ---------- | ---------------------------------- | ----------------------------------------------------- | ---------------------------------------------------------- |
| MET-01 | Visitas calificadas (con perfil ICP identificable)  | Analytics (a habilitar)            | Marketing             | Semanal    | Desconocido — sin Analytics activo | ≥ 50 visitas/mes a rutas ICP                          | Sin Analytics no hay baseline; primera lectura en semana 4 |
| MET-02 | Avance a rutas prioritarias (H01, H02) desde Home   | Analytics — clics en CTAs de rutas | Marketing             | Semanal    | 0% — rutas no existen              | ≥ 25% de visitas Home navegan a una ruta ICP          | Hipótesis sin referencia previa                            |
| MET-03 | Consumo de casos (visitas a páginas de caso)        | Analytics                          | Marketing             | Semanal    | 0% — casos no existen              | ≥ 40% de visitas a ruta consumen caso                 | Requiere CASO-01 y CASO-02 primero                         |
| MET-04 | Inicio de preevaluación (llegada al formulario)     | Analytics                          | Comercial + Marketing | Semanal    | 0% — formulario no existe          | ≥ 10% de visitas calificadas inician formulario       | Hipótesis; ajustar tras semana 4                           |
| MET-05 | Finalización de preevaluación (envío de formulario) | Formulario + CRM                   | Comercial             | Semanal    | 0                                  | ≥ 70% de inicios completan formulario                 | Tasa de abandono es desconocida sin datos previos          |
| MET-06 | Oportunidades calificadas generadas                 | CRM                                | Comercial             | Mensual    | 0                                  | ≥ 3 oportunidades calificadas/mes en primeros 3 meses | Hipótesis de rampa                                         |
| MET-07 | Tiempo de respuesta (envío a respuesta de PICC)     | CRM / registro manual              | Comercial             | Por lead   | Sin registro                       | < 48h hábiles para 100% de leads                      | Sin sistema de registro hoy                                |
| MET-08 | Reuniones generadas                                 | CRM / calendario                   | Comercial             | Mensual    | Desconocido                        | ≥ 60% de respuestas positivas resultan en reunión     | Sin datos de conversión previos                            |
| MET-09 | Propuestas generadas                                | CRM                                | Comercial             | Mensual    | Desconocido                        | ≥ 40% de reuniones avanzan a propuesta                | Hipótesis; ajustar con primeros datos reales               |
| MET-10 | Proyectos en shortlist                              | CRM                                | Comercial + Dirección | Mensual    | Desconocido                        | ≥ 2 proyectos en shortlist / mes en mes 2+            | Hipótesis                                                  |
| MET-11 | Pipeline generado (estimado de valor)               | CRM                                | Dirección             | Mensual    | Desconocido                        | Sin meta inicial — registrar para aprender            | Sin referencia de ticket promedio                          |
| MET-12 | Decision Coverage score                             | Auditoría interna                  | Producto              | Trimestral | H01: ~25%, H02: ~20%               | H01: ≥ 65%, H02: ≥ 60% en mes 3                       | Métrica manual, sin automatización                         |
| MET-13 | Trust assets E4 activos                             | Biblioteca de Evidencia            | Dirección + Marketing | Mensual    | 0                                  | ≥ 1 caso E4 para H01 y 1 para H02 en mes 2            | Depende de permisos de cliente                             |
| MET-14 | Porcentaje de leads con ICP clasificable            | CRM                                | Comercial + ZEUS      | Mensual    | Desconocido                        | ≥ 80% de leads tienen ICP asignado                    | Requiere sistema de clasificación funcionando              |
| MET-15 | Porcentaje de leads con causa de pérdida registrada | CRM                                | Comercial             | Mensual    | 0%                                 | ≥ 90% de leads descartados tienen razón registrada    | Sin sistema de registro hoy                                |

### Instrumentación mínima necesaria

1. Google Analytics 4 habilitado y con eventos básicos de clic configurados.
2. Formulario de preevaluación con confirmación de envío trackeada.
3. CRM básico o hoja estructurada con campos: lead ID, fecha, ICP, score, estado, SLA, resultado, razón de pérdida.
4. Calendario compartido para reuniones con registro de asistencia.
5. Registro semanal de trust assets activos.

Sin esta instrumentación mínima, el MVP puede operar pero no puede aprender.

