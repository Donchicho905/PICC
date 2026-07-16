# Sistema de Evidencia

## Ficha de Trazabilidad
- ID: DOC-016
- Estado: 🟡 En desarrollo
- Tipo: Evidence System — Reglas operativas del Growth MVP V1
- Objetivo: Definir las reglas de evidencia que gobiernan qué puede publicarse, cómo se clasifica y qué proceso sigue para ser validado y autorizado.
- Entradas:
  - DOC-017 (04_TRUST/Trust_Architecture.md)
  - DOC-033 (08_IMPLEMENTACION/MVP.md)
- Salidas:
  - Reglas operativas de evidencia
  - Proceso de construcción y validación de activos
  - Claim Register operativo
- Dependencias:
  - DOC-015 (04_TRUST/Biblioteca_de_Evidencia.md)
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md)
- Documentos consumidos:
  - Trust_Architecture.md — niveles E0-E5
  - ICPs.md — regla epistemológica
- Documentos generados:
  - DOC-015 (04_TRUST/Biblioteca_de_Evidencia.md)
- Responsable: Dirección + Comercial
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Todo claim tiene nivel de evidencia asignado
  - Ningún claim E0-E1 se publica como afirmación fuerte
  - Existe proceso de subida de evidencia documentado
  - La diferencia entre ausencia de dato y ausencia de permiso está clara

## Niveles de evidencia (referencia desde Trust_Architecture)

| Nivel | Nombre                     | Uso permitido                             |
| ----- | -------------------------- | ----------------------------------------- |
| E0    | No evidencia               | No publicable, no usable para claims      |
| E1    | Señal aislada              | Solo indicios internos                    |
| E2    | Evidencia parcial trazable | Interno y cautela externa máxima          |
| E3    | Evidencia operativa        | Venta asistida; no necesariamente pública |
| E4    | Evidencia publicable       | Sitio, decks, materiales comerciales      |
| E5    | Evidencia sistémica        | Posicionamiento y mejora continua         |

## Reglas operativas de publicación

1. Ningún claim llega a surface pública sin nivel E4 como mínimo.
2. Un claim E2 puede usarse en venta asistida con nota de cautela verbal; no en copy de sitio.
3. Un activo con datos sensibles sin permiso explícito del cliente no se publica, aunque sea técnicamente poderoso.
4. Una referencia verbal sin autorización formal no se presenta como testimonio.
5. Una métrica agregada (años, proyectos, m²) debe tener fuente documental interna antes de publicarse.
6. Un logotipo de partner solo se usa si existe acuerdo o autorización documentada.
7. Todo caso en sitio requiere revisión previa con el cliente si la publicación incluye nombre, foto o dato identificable.

## Diferencia entre tipos de brecha

| Tipo de brecha             | Descripción                                                          | Acción recomendada                                       |
| -------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------- |
| Ausencia de dato           | El hecho existió o existe pero no está documentado                   | Documentar internamente antes de publicar                |
| Ausencia de permiso        | El dato existe y está documentado pero el cliente no autorizó su uso | Solicitar permiso; si se niega, anonimizar o no publicar |
| Ausencia de evidencia real | No existe el caso o la experiencia que se quiere afirmar             | No publicar; generar evidencia real primero              |
| Dato no verificado         | El claim circula internamente pero nunca fue corroborado             | Auditar antes de usar                                    |

## Proceso de construcción y validación de assets

### Paso 1 — Identificación
- ¿De qué proyecto o capacidad se quiere generar evidencia?
- ¿Quién es el responsable interno de ese proyecto?
- ¿Existe documentación técnica o de cierre?

### Paso 2 — Clasificación inicial
- Asignar nivel de evidencia provisional (E0–E3).
- Identificar tipo de brecha: dato, permiso o ausencia real.

### Paso 3 — Gestión de permiso
- Contactar al cliente o stakeholder correspondiente.
- Definir alcance de autorización: nombre, foto, datos, testimonio.
- Registrar la autorización en la Biblioteca de Evidencia.

### Paso 4 — Empaquetamiento
- Redactar el asset (caso, claim, métrica, referencia) según el formato de DOC-033 Sección 7.
- Revisar que el asset no incluya datos fuera del permiso.
- Asignar ID en Biblioteca de Evidencia.

### Paso 5 — Validación
- Revisión interna: Dirección confirma que el asset es técnicamente correcto.
- Si el permiso lo exige: enviar borrador al cliente para aprobación.
- Clasificar como E4 solo después de aprobación completa.

### Paso 6 — Publicación
- El asset E4 puede publicarse en la surface asignada.
- Registrar fecha de publicación y surface en Biblioteca de Evidencia.
- Definir fecha de revisión periódica.

### Paso 7 — Mantenimiento
- Revisar cada asset al menos anualmente.
- Si el cliente retira el permiso: retirar de superficie pública en < 48h.
- Si el dato cambia (empresa cierra, datos incorrectos): actualizar o retirar.

## Claim Register operativo del MVP

| Claim ID | Claim o promesa                                       | Surface actual    | Nivel observado | Publicable hoy          | Acción requerida                                                 | Owner                   | Fecha de revisión |
| -------- | ----------------------------------------------------- | ----------------- | --------------- | ----------------------- | ---------------------------------------------------------------- | ----------------------- | ----------------- |
| CLM-01   | Especialización en Data Centers                       | Home              | E2              | Publicable condicionada | Auditar alcance real y respaldar con caso                        | Dirección               | 2026-08-15        |
| CLM-02   | Certificación ICREA CCRD                              | Home              | E2              | Publicable condicionada | Documentar alcance exacto de la certificación                    | Dirección               | 2026-08-01        |
| CLM-03   | Panduit                                               | Home              | E2              | Publicable condicionada | Verificar tipo de relación y obtener autorización de uso de logo | Dirección               | 2026-08-01        |
| CLM-04   | 25+ años de experiencia                               | Home              | E2              | Publicable condicionada | Verificar año de fundación con documento                         | Dirección               | 2026-08-01        |
| CLM-05   | 100+ proyectos                                        | Home              | E2              | Publicable condicionada | Levantar inventario y contar con criterio definido               | Dirección + Operaciones | 2026-08-15        |
| CLM-06   | 50,000+ m² ejecutados                                 | Home              | E2              | Publicable condicionada | Verificar metodología de cálculo y fuente                        | Dirección + Operaciones | 2026-08-15        |
| CLM-07   | Cobertura nacional e internacional                    | Home              | E2              | Publicable condicionada | Definir qué proyectos sustentan cobertura internacional          | Dirección               | 2026-09-01        |
| CLM-08   | Integración de todas las disciplinas bajo un contrato | Propuesta / rutas | E2              | No publicable todavía   | Documentar con al menos 1 caso real                              | Dirección + Operaciones | 2026-09-01        |
| CLM-09   | Metodología de obra en operación                      | Ruta H02          | E0              | No publicable todavía   | Documentar proceso real validado por operaciones                 | Operaciones             | 2026-09-15        |
| CLM-10   | Proceso de trabajo en 5 pasos                         | Home S6 / rutas   | E0-E1           | No publicable todavía   | Validar que el proceso descrito refleja la práctica real         | Operaciones + Comercial | 2026-08-15        |

## SLA del sistema de evidencia

| Actividad                                 | SLA objetivo                                             |
| ----------------------------------------- | -------------------------------------------------------- |
| Clasificar un nuevo asset entrante        | 48h desde identificación                                 |
| Solicitar permiso a cliente               | < 5 días hábiles desde identificación del caso candidato |
| Empaquetar caso una vez con permiso       | < 10 días hábiles                                        |
| Retirar asset si permiso se revoca        | < 48h                                                    |
| Revisión periódica de Claim Register      | Mensual                                                  |
| Auditoría completa de evidencia publicada | Trimestral                                               |


---

# ALPHA GATE 01 — Claim–Evidence–Permission Audit

## Fecha de auditoría: 2026-07-15
## Versiones auditadas: ES (picc.com.mx), EN (picc.com.mx/en), FR (picc.com.mx/fr)
## Método: Snapshot directo de las tres versiones del sitio en producción.

---

## Snapshot versionado del sitio

### Metadata común a las tres versiones

| Campo               | Valor                                                                          |
| ------------------- | ------------------------------------------------------------------------------ |
| Dominio             | picc.com.mx                                                                    |
| Copyright footer    | © 2025 PICC                                                                    |
| Teléfono            | +52 55 6808 2156                                                               |
| WhatsApp            | +52 55 6808 2156                                                               |
| Correo              | contacto@picc.com.mx                                                           |
| Dirección           | Montes Urales 755, Col. Lomas de Chapultepec, Miguel Hidalgo, CDMX, C.P. 11000 |
| Idiomas disponibles | ES, EN, FR                                                                     |
| Fecha del snapshot  | 2026-07-15                                                                     |
| Imagen Hero (fondo) | Unsplash — no es imagen propia de obra de PICC                                 |
| Imagen equipo       | Unsplash — no es imagen propia del equipo de PICC                              |
| Imagen Data Center  | Unsplash — no es imagen propia de Data Center de PICC                          |

### Secciones de la Home (estructura común a las tres versiones)

1. Navbar: logo, links de navegación, selector de idioma.
2. Hero: headline principal, sub-copy, métricas en ticker, CTA principal y secundario.
3. Nosotros / About: texto descriptivo de trayectoria, 4 íconos con métricas, imagen lateral.
4. Data Centers / Critical Infrastructure: descripción de especialización, 6 sub-capacidades, logos ICREA y PANDUIT.
5. Servicios / Services: 8 tarjetas de servicio.
6. Equipo / Team: descripción, 4 disciplinas con íconos, 3 imágenes (todas de Unsplash).
7. CTA final: párrafo de llamada, botón de contacto.
8. Footer: links, contacto, copyright.

### Diferencias entre versiones de idioma

| Claim o elemento       | ES                                | EN                              | FR                                | Riesgo de inconsistencia                                                              |
| ---------------------- | --------------------------------- | ------------------------------- | --------------------------------- | ------------------------------------------------------------------------------------- |
| Niveles de Data Center | "Diseño Nivel I al VI ICREA"      | "Tier II and III Design"        | "Conception Tier II et III"       | ALTO — ES afirma Nivel I-VI; EN y FR afirman solo Tier II-III. Contradicción directa. |
| Panduit en hero        | "PANDUIT" (sin calificador)       | "PANDUIT Certified"             | "PANDUIT Partenaire"              | MEDIO — distinción entre "Certified" y "Partner" afecta el alcance del claim          |
| Footer PANDUIT         | "ICREA CCRD                       | PANDUIT"                        | "ICREA CCRD                       | PANDUIT Certified"                                                                    | MEDIO — inconsistencia en calificación |
| Referentes             | "referentes en el sector"         | "industry leaders"              | "leaders du secteur"              | BAJO — posicionamiento como líder sin caso que lo respalde                            |
| Panduit garantía       | "PANDUIT con garantía de 25 años" | "PANDUIT with 25-year warranty" | "PANDUIT avec garantie de 25 ans" | MEDIO — esta garantía es de PANDUIT como fabricante, no de PICC                       |
| Cableado BICSI         | Sin mención en ES                 | "PANDUIT and BICSI certified"   | "Certifiés PANDUIT et BICSI"      | MEDIO — BICSI aparece en EN y FR; ausente en ES                                       |

---

## Inventario completo de claims

### Grupo A — Claims de métricas institucionales

| Claim ID   | Texto exacto (ES)                                                         | EN equivalente                                                            | FR equivalente                                                           | Sección          | Estado de inconsistencia  |
| ---------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ---------------- | ------------------------- |
| CLM-MET-01 | "25+ años del fundador"                                                   | "25+ Founder's Years"                                                     | "25+ ans du fondateur"                                                   | Hero ticker      | Consistente entre idiomas |
| CLM-MET-02 | "30+ años del equipo"                                                     | "30+ Team's Years"                                                        | "30+ ans de l'équipe"                                                    | Hero ticker      | Consistente entre idiomas |
| CLM-MET-03 | "100+ proyectos exitosos"                                                 | "100+ Successful Projects"                                                | "100+ Projets Réussis"                                                   | Hero ticker      | Consistente entre idiomas |
| CLM-MET-04 | "50,000+ m² construidos"                                                  | "50,000+ m² Built"                                                        | "50,000+ M² Construits"                                                  | Hero ticker      | Consistente entre idiomas |
| CLM-MET-05 | "25+ años de experiencia en construcción"                                 | "25+ years of experience in construction"                                 | "25+ ans d'expérience dans la construction"                              | Hero sub-copy    | Consistente               |
| CLM-MET-06 | "más de 25 años de experiencia en el sector de la construcción"           | "over 25 years of experience in the construction sector"                  | "plus de 25 ans d'expérience dans le secteur de la construction"         | Sección Nosotros | Consistente               |
| CLM-MET-07 | "Más de 25 años de experiencia en construcción e infraestructura crítica" | "Over 25 years of experience in construction and critical infrastructure" | "Plus de 25 ans d'expérience en construction et infrastructure critique" | Footer           | Consistente               |

### Grupo B — Claims de credenciales y certificaciones

| Claim ID   | Texto exacto (ES)                                                                     | EN equivalente                                       | FR equivalente                                         | Sección                   | Estado de inconsistencia                                                 |
| ---------- | ------------------------------------------------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------ | ------------------------- | ------------------------------------------------------------------------ |
| CLM-CRD-01 | "Certificación ICREA CCRD"                                                            | "ICREA CCRD Certification"                           | "Certification ICREA CCRD"                             | Hero badge                | Consistente                                                              |
| CLM-CRD-02 | "Certificados ICREA — CCRD Data Centers"                                              | "ICREA Certified — CCRD Data Centers"                | "Certifiés ICREA — CCRD Data Centers"                  | Íconos Nosotros           | Consistente                                                              |
| CLM-CRD-03 | "Diseño Nivel I al VI ICREA" (ES) vs "Tier II and III Design" (EN/FR)                 | "Tier II and III Design"                             | "Conception Tier II et III"                            | Hero badge / Data Centers | INCONSISTENTE — riesgo alto                                              |
| CLM-CRD-04 | "Proyectos ejecutivos bajo estándar ICREA-Std-131 con ingeniería de detalle completa" | "Executive projects under ICREA-Std-131 standard"    | "Projets exécutifs selon la norme ICREA-Std-131"       | Data Centers              | Consistente en EN y FR                                                   |
| CLM-CRD-05 | "PANDUIT" / "PANDUIT Certified" / "PANDUIT Partenaire"                                | "PANDUIT Certified"                                  | "PANDUIT Partenaire"                                   | Hero badge y footer       | INCONSISTENTE — calificador diferente entre idiomas                      |
| CLM-CRD-06 | "Infraestructura PANDUIT con garantía de 25 años y documentación completa"            | "PANDUIT infrastructure with 25-year warranty"       | "Infrastructure PANDUIT avec garantie de 25 ans"       | Data Centers              | Consistente; riesgo semántico: la garantía es del fabricante, no de PICC |
| CLM-CRD-07 | Sin mención en ES                                                                     | "PANDUIT and BICSI certified for structured cabling" | "Certifiés PANDUIT et BICSI pour le câblage structuré" | Equipo                    | INCONSISTENTE — ES omite BICSI                                           |
| CLM-CRD-08 | "ICREA CCRD" (footer)                                                                 | "ICREA CCRD" (footer)                                | "ICREA CCRD" (footer)                                  | Footer                    | Consistente                                                              |

### Grupo C — Claims de capacidad técnica por disciplina

| Claim ID   | Texto exacto (ES)                                                                   | Sección      | Disciplina               |
| ---------- | ----------------------------------------------------------------------------------- | ------------ | ------------------------ |
| CLM-CAP-01 | "Sistemas UPS con redundancia N+1, transferencias automáticas y respaldo eléctrico" | Data Centers | Energía crítica          |
| CLM-CAP-02 | "HVAC de precisión para control de temperatura y humedad en ambientes críticos"     | Data Centers | Climatización            |
| CLM-CAP-03 | "Detección temprana y supresión con agentes limpios FM-200 o Novec"                 | Data Centers | Protección incendios     |
| CLM-CAP-04 | "Control de acceso biométrico, CCTV y videovigilancia 24/7"                         | Data Centers | Seguridad                |
| CLM-CAP-05 | "Sistemas eléctricos de media y baja tensión"                                       | Servicios    | Instalaciones eléctricas |
| CLM-CAP-06 | "Sistemas HVAC comerciales e industriales"                                          | Servicios    | Climatización            |
| CLM-CAP-07 | "Edificios corporativos, oficinas y espacios comerciales de alta gama"              | Servicios    | Construcción comercial   |
| CLM-CAP-08 | "Desarrollos residenciales y proyectos de vivienda de lujo"                         | Servicios    | Residencial premium      |
| CLM-CAP-09 | "Naves industriales, bodegas y plantas de producción"                               | Servicios    | Industrial               |
| CLM-CAP-10 | "Renovación de espacios comerciales y corporativos"                                 | Servicios    | Remodelaciones           |

### Grupo D — Claims de equipo

| Claim ID   | Texto exacto (ES)                                                                                                      | Sección                       | Nota                                                                               |
| ---------- | ---------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ---------------------------------------------------------------------------------- |
| CLM-EQP-01 | "equipo de profesionales con más de 30 años de trayectoria en ingeniería civil, eléctricas, HVAC y telecomunicaciones" | Nosotros                      | Ambiguo: ¿el equipo tiene 30+ años cada uno o el equipo existe desde hace 30 años? |
| CLM-EQP-02 | "equipos multidisciplinarios de profesionales con décadas de experiencia en sus respectivas áreas"                     | Equipo                        | Genérico; no cuantificado                                                          |
| CLM-EQP-03 | "garantizando resultados de primer nivel en cada proyecto"                                                             | Equipo                        | Promesa absoluta sin evidencia                                                     |
| CLM-EQP-04 | "Profesionales con 30+ años en estructuras y obra civil"                                                               | Equipo — Ingeniería Civil     | Ambiguo: ¿todos o alguno?                                                          |
| CLM-EQP-05 | "Expertos en sistemas de potencia e infraestructura crítica"                                                           | Equipo — Ingeniería Eléctrica | No cuantificado                                                                    |
| CLM-EQP-06 | "Especialistas en HVAC de precisión y sistemas industriales"                                                           | Equipo — Climatización        | No cuantificado                                                                    |

### Grupo E — Claims de posicionamiento y diferenciación

| Claim ID   | Texto exacto (ES)                                                         | EN                                                             | FR                                                                 | Sección         |
| ---------- | ------------------------------------------------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------------------ | --------------- |
| CLM-POS-01 | "Construimos el Futuro de la Infraestructura en México"                   | "Building the Future of Infrastructure in Mexico"              | "Construire l'Avenir de l'Infrastructure au Mexique"               | H1 / Headline   |
| CLM-POS-02 | "nos posiciona como referentes en el sector"                              | "positions us as industry leaders"                             | "nous positionne comme leaders du secteur"                         | Nosotros        |
| CLM-POS-03 | "Nuestra Especialidad Desde 2020"                                         | "Our Specialty Since 2020"                                     | "Notre Spécialité Depuis 2020"                                     | Sub-badge       |
| CLM-POS-04 | "listos para llevar tu infraestructura crítica al siguiente nivel"        | "ready to take your critical infrastructure to the next level" | "prêts à porter votre infrastructure critique au niveau supérieur" | CTA final       |
| CLM-POS-05 | "Más de 25 años de experiencia en construcción e infraestructura crítica" | "Over 25 years of experience..."                               | "Plus de 25 ans d'expérience..."                                   | Footer          |
| CLM-POS-06 | "Cobertura — Nacional e Internacional"                                    | "Coverage — National & International"                          | "Couverture — Nationale et Internationale"                         | Íconos Nosotros |

### Grupo F — Claims implícitos estructurales y visuales

| Claim ID   | Claim implícito                                         | Origen                                   | Riesgo                                                |
| ---------- | ------------------------------------------------------- | ---------------------------------------- | ----------------------------------------------------- |
| CLM-IMP-01 | "Somos una empresa con experiencia visual real en obra" | Fotos de Unsplash en Hero y Data Centers | ALTO — fotos no son propias                           |
| CLM-IMP-02 | "Tenemos equipo propio visible"                         | Foto de equipo de Unsplash               | ALTO — no es el equipo real de PICC                   |
| CLM-IMP-03 | "Tenemos proyectos de Data Center realizados"           | Foto de DC de Unsplash                   | ALTO — no es instalación propia de PICC               |
| CLM-IMP-04 | "PANDUIT avala nuestra capacidad técnica"               | Logotipo de Panduit en el sitio          | MEDIO — implica aval sin especificar tipo de relación |
| CLM-IMP-05 | "ICREA certifica nuestra capacidad"                     | Logotipo de ICREA en el sitio            | MEDIO — requiere verificar alcance y vigencia         |

---

## Matriz Claim–Decision–Evidence–Permission

| Claim ID   | Texto base                                                 | ICP      | Etapa Journey  | Decisión que intenta soportar   | Importancia | Calidad               | Permiso      | Riesgo                                                            | Acción                                                       | Publicabilidad              | Surface futura      | Notas                                                                |
| ---------- | ---------------------------------------------------------- | -------- | -------------- | ------------------------------- | ----------- | --------------------- | ------------ | ----------------------------------------------------------------- | ------------------------------------------------------------ | --------------------------- | ------------------- | -------------------------------------------------------------------- |
| CLM-MET-01 | 25+ años del fundador                                      | H01, H02 | Descubrimiento | Es institucionalmente confiable | Alta        | E2                    | Sin validar  | Legal/reputacional: cifra sin fuente documental                   | Verificar con Dirección + documento                          | PC                          | Home S2, footer     | BKL-P0-01. Distinguir años del fundador vs. años de la empresa PICC. |
| CLM-MET-02 | 30+ años del equipo                                        | H01, H02 | Descubrimiento | Es institucionalmente confiable | Alta        | E2                    | Sin validar  | Reputacional: ambigüedad suma vs. promedio                        | Verificar y aclarar                                          | PC                          | Home S2             | BKL-P0-01                                                            |
| CLM-MET-03 | 100+ proyectos exitosos                                    | H01, H02 | Consideración  | Tiene experiencia comparable    | Alta        | E2                    | Sin validar  | Reputacional: "exitosos" implica definición que no existe         | Definir criterio + inventariar                               | PC                          | Home S2, rutas      | BKL-P0-01. ¿100 contratos? ¿100 fases? Aclarar.                      |
| CLM-MET-04 | 50,000+ m² construidos                                     | H01, H02 | Consideración  | Tiene experiencia comparable    | Alta        | E2                    | Sin validar  | Reputacional: metodología de cálculo no definida                  | Definir metodología + sumar datos reales                     | PC                          | Home S2             | BKL-P0-01                                                            |
| CLM-CRD-01 | Certificación ICREA CCRD                                   | H01      | Validación     | Es técnicamente competente      | Crítica     | E2                    | Sin validar  | Técnico/reputacional: alcance interno no verificado               | Verificar alcance exacto con Dirección                       | PC                          | Home S2, Ruta H01   | BKL-P0-02                                                            |
| CLM-CRD-03 | Nivel I-VI (ES) vs Tier II-III (EN/FR)                     | H01      | Validación     | Es técnicamente competente      | Crítica     | E0 en estado actual   | Sin validar  | MUY ALTO — contradicción verificable entre idiomas                | Resolver con Dirección ANTES de publicar                     | NP hasta resolver           | Home S2, Ruta H01   | Bloqueador crítico.                                                  |
| CLM-CRD-04 | "ICREA-Std-131 con ingeniería de detalle completa"         | H01      | Validación     | Es técnicamente competente      | Alta        | E1                    | Sin validar  | Técnico: implica capacidad no evidenciada                         | Verificar con Operaciones                                    | PC                          | Ruta H01            | Si existe proyecto real: documentar.                                 |
| CLM-CRD-05 | PANDUIT / "Certified" / "Partenaire"                       | H01      | Validación     | Es técnicamente competente      | Alta        | E2                    | Sin validar  | ALTO — inconsistencia entre idiomas; uso de logo sin autorización | Verificar tipo de relación + autorización de logo            | PC o NP                     | Home S2, Ruta H01   | BKL-P0-03                                                            |
| CLM-CRD-06 | "garantía de 25 años PANDUIT"                              | H01      | Validación     | Reduce mi riesgo                | Alta        | E2                    | Condicionada | MEDIO — puede interpretarse como garantía de PICC                 | Reformular: "garantía del fabricante de 25 años"             | PC — requiere reformulación | Ruta H01            | Claim verdadero en origen pero puede inducir confusión.              |
| CLM-CRD-07 | BICSI (solo EN/FR)                                         | H01      | Validación     | Es técnicamente competente      | Media       | E1                    | Sin validar  | MEDIO — inconsistencia entre idiomas                              | Verificar si existe certificación + decidir si incluir en ES | PC                          | Equipo, Ruta H01    |                                                                      |
| CLM-CAP-01 | UPS con redundancia N+1                                    | H01      | Validación     | Tiene capacidad técnica         | Alta        | E1                    | Sin validar  | Técnico: afirma capacidad sin caso                                | Verificar con Operaciones                                    | PC                          | Ruta H01            |                                                                      |
| CLM-CAP-02 | HVAC de precisión para ambientes críticos                  | H01, H02 | Validación     | Tiene capacidad técnica         | Alta        | E1                    | Sin validar  | Técnico                                                           | Verificar con Operaciones                                    | PC                          | Ruta H01/H02        |                                                                      |
| CLM-CAP-03 | Supresión FM-200 o Novec                                   | H01      | Validación     | Tiene capacidad técnica         | Alta        | E1                    | Sin validar  | Técnico: puede requerir licencias específicas                     | Verificar si PICC ejecuta directamente o subcontrata         | PC o NP                     | Ruta H01            | Si subcontratado: reformular.                                        |
| CLM-CAP-04 | Seguridad biométrica, CCTV 24/7                            | H01      | Validación     | Tiene capacidad técnica         | Media       | E1                    | Sin validar  | Técnico                                                           | Verificar con Operaciones                                    | PC                          | Ruta H01            |                                                                      |
| CLM-CAP-05 | Sistemas eléctricos media y baja tensión                   | H01, H02 | Consideración  | PICC entiende mi caso           | Alta        | E2                    | Condicionada | Bajo                                                              | Mantener con caso de soporte en P1                           | PA con cautela              | Home S5, Ruta H02   | Capacidad con más base verificable del sitio.                        |
| CLM-CAP-06 | Sistemas HVAC comerciales e industriales                   | H01, H02 | Consideración  | PICC entiende mi caso           | Alta        | E2                    | Condicionada | Bajo                                                              | Mantener con caso                                            | PA con cautela              | Home S5, Ruta H02   |                                                                      |
| CLM-CAP-07 | Edificios corporativos, oficinas alta gama                 | H03      | Consideración  | PICC entiende mi caso           | Media       | E1                    | Sin validar  | Bajo                                                              | Mantener si existe historial                                 | PC                          | Servicios           |                                                                      |
| CLM-CAP-08 | Residencial y vivienda de lujo                             | H06      | Consideración  | PICC entiende mi caso           | Baja        | E1                    | Sin validar  | Bajo                                                              | Mantener como servicio secundario                            | PC                          | Servicios           | No es ICP prioritario en MVP Alpha.                                  |
| CLM-CAP-09 | Naves industriales, bodegas y plantas                      | H02      | Consideración  | PICC entiende mi caso           | Alta        | E1-E2                 | Sin validar  | Bajo                                                              | Respaldar con CASO-02                                        | PC                          | Servicios, Ruta H02 |                                                                      |
| CLM-EQP-01 | Equipo 30+ años en civil, eléctrica, HVAC, telecom         | H01, H02 | Validación     | Es institucionalmente confiable | Alta        | E1                    | Sin validar  | Reputacional: ambigüedad                                          | Verificar y reformular con perfiles reales                   | PC                          | Home S2, Equipo     | BKL-P0-01 relacionado                                                |
| CLM-EQP-03 | "garantizando resultados de primer nivel en cada proyecto" | H01, H02 | Validación     | Reduce mi riesgo                | Alta        | E0                    | Sin validar  | ALTO — promesa absoluta sin evidencia                             | Eliminar o reformular sin absoluto                           | NP                          | Equipo              |                                                                      |
| CLM-POS-01 | "Construimos el Futuro de la Infraestructura en México"    | H01, H02 | Descubrimiento | ¿Esto es para mí?               | Alta        | E0 — mensaje, no fact | N/A          | Bajo                                                              | Mantener como mensaje de marca                               | PA (mensaje)                | Hero H1             | No es un fact. Aceptable como posicionamiento de marca.              |
| CLM-POS-02 | "referentes en el sector" / "industry leaders"             | H01, H02 | Descubrimiento | Vale la pena considerar a PICC  | Alta        | E0                    | Sin validar  | Reputacional: liderazgo sin respaldo externo                      | Reformular con alcance más específico y defensible           | PC — reformular             | Nosotros            |                                                                      |
| CLM-POS-03 | "Nuestra Especialidad Desde 2020"                          | H01      | Descubrimiento | Es técnicamente competente      | Alta        | E2                    | Condicionada | Bajo                                                              | Mantener                                                     | PA con cautela              | Hero                | Coherente con narrativa de pandemia.                                 |
| CLM-POS-04 | "llevar tu infraestructura crítica al siguiente nivel"     | H01, H02 | CTA            | Qué siguiente paso debo tomar   | Media       | E0 — copy de CTA      | N/A          | Bajo                                                              | Mantener como copy de CTA                                    | PA (copy)                   | CTA final           |                                                                      |
| CLM-POS-06 | "Cobertura — Nacional e Internacional"                     | H01, H04 | Consideración  | Tiene experiencia comparable    | Media       | E1                    | Sin validar  | Reputacional: "internacional" sin proyecto visible                | Verificar; retirar "Internacional" si no hay evidencia       | PC o NP en "Internacional"  | Nosotros            |                                                                      |
| CLM-IMP-01 | Fotos de Unsplash como imágenes propias                    | H01, H02 | Todos          | Tenemos historia visual real    | Crítica     | E0                    | Sin permiso  | ALTO — buyer técnico detecta fotos de stock                       | Reemplazar con fotos reales (BKL-P0-12)                      | NP en su estado actual      | Todo el sitio       | Bloqueador de credibilidad.                                          |
| CLM-IMP-02 | Foto de equipo de Unsplash                                 | H01, H02 | Validación     | El equipo es real y visible     | Alta        | E0                    | Sin permiso  | ALTO                                                              | Reemplazar con foto real del equipo                          | NP                          | Sección Equipo      |                                                                      |
| CLM-IMP-03 | Foto de Data Center de Unsplash                            | H01      | Validación     | Han construido Data Centers     | Crítica     | E0                    | Sin permiso  | MUY ALTO                                                          | Reemplazar con instalación propia o quitar                   | NP                          | Data Centers, Hero  | Bloqueador crítico para H01.                                         |
| CLM-IMP-04 | Logotipo PANDUIT sin especificación de relación            | H01      | Validación     | Es técnicamente competente      | Alta        | E2                    | Sin validar  | ALTO — uso de logo sin autorización formal                        | Verificar + obtener autorización                             | PC hasta permiso            | Home, Ruta H01      | BKL-P0-03                                                            |
| CLM-IMP-05 | Logotipo ICREA                                             | H01      | Validación     | Es técnicamente competente      | Alta        | E2                    | Sin validar  | MEDIO                                                             | Verificar vigencia y términos de uso del logo                | PC                          | Home, Ruta H01      | BKL-P0-02 relacionado                                                |

---

## Decision Coverage — Estado real post-auditoría

### ICP-H01 — Data Centers e Infraestructura Crítica

| Decisión del comprador                | Estado                 | Claim(s) que aportan                       | Brecha principal                                                    |
| ------------------------------------- | ---------------------- | ------------------------------------------ | ------------------------------------------------------------------- |
| ¿Vale la pena seguir explorando PICC? | Parcialmente soportada | CLM-POS-01, CLM-MET-01 a 04                | Cifras sin respaldo documental; fotos de stock reducen credibilidad |
| ¿PICC entiende mi tipo de proyecto?   | Parcialmente soportada | CLM-CRD-01, CLM-POS-03                     | Sin caso visible de DC; especialización declarada no probada        |
| ¿Tiene experiencia comparable?        | No soportada           | CLM-MET-03                                 | Sin inventario; sin caso de DC publicable; fotos son de stock       |
| ¿Tiene capacidad técnica?             | Parcialmente soportada | CLM-CRD-01, CLM-CAP-01 a 04                | ICREA sin alcance verificado; capacidades técnicas sin caso real    |
| ¿Reduce mi riesgo?                    | No soportada           | CLM-EQP-03 (NP)                            | Promesa absoluta sin evidencia                                      |
| ¿Es institucionalmente confiable?     | Parcialmente soportada | CLM-MET-01/02, datos de contacto           | Fotos de equipo son de stock; cifras sin respaldo documental        |
| ¿Qué la diferencia?                   | No soportada           | Ningún claim específico                    | No hay diferenciador articulado más allá de la certificación        |
| ¿Puedo incluirla en shortlist?        | Parcialmente soportada | Combinación de certificación + trayectoria | Sin caso para validar técnicamente; sin referencia                  |
| ¿Cuál es el siguiente paso?           | Parcialmente soportada | WhatsApp, correo, CTA consulta             | CTA genérica; sin diagnóstico estructurado; SLA no visible          |

**Cobertura estimada H01: 30–35%**

### ICP-H02 — Industrial e Instalaciones Críticas

| Decisión del comprador                | Estado                 | Claim(s) que aportan             | Brecha principal                                                  |
| ------------------------------------- | ---------------------- | -------------------------------- | ----------------------------------------------------------------- |
| ¿Vale la pena seguir explorando PICC? | Parcialmente soportada | CLM-POS-01, CLM-MET-01 a 04      | Mismo problema que H01                                            |
| ¿PICC entiende mi tipo de proyecto?   | No soportada           | CLM-CAP-09 (mencionado)          | Sin narrativa ni caso industrial; la Home es de DC                |
| ¿Tiene experiencia comparable?        | No soportada           | Ningún claim específico para H02 | Sin caso industrial                                               |
| ¿Tiene capacidad técnica?             | Parcialmente soportada | CLM-CAP-05, CLM-CAP-06           | Eléctrico e HVAC mencionados; sin contexto de obra en operación   |
| ¿Reduce mi riesgo?                    | No soportada           | Ningún claim relevante           | No hay mención de continuidad operativa ni metodología industrial |
| ¿Es institucionalmente confiable?     | Parcialmente soportada | Idem H01                         | Misma brecha                                                      |
| ¿Qué la diferencia?                   | No soportada           | Ningún claim                     | Sin mensaje diferenciador para H02                                |
| ¿Puedo incluirla en shortlist?        | No soportada           | Insuficiente                     | Sin caso ni referencia para H02                                   |
| ¿Cuál es el siguiente paso?           | Parcialmente soportada | WhatsApp, correo                 | CTA no diferenciada para H02                                      |

**Cobertura estimada H02: 20–25%**

---

## Claim Set oficial provisional

### A. Claims prioritarios para Home (máximo 7)

| #    | Texto factual base                                                                                         | Decisión que soporta                               | Evidencia actual | Condición de publicación                                                                                     | Límites                                                           | Owner     | Fecha revisión            |
| ---- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------- | --------- | ------------------------- |
| H-01 | "PICC nace de más de 25 años de experiencia del fundador en construcción e infraestructura."               | Es institucionalmente confiable                    | E2               | PC — verificar año de inicio con Dirección                                                                   | No decir "25 años de la empresa"; distinguir fundador vs. empresa | Dirección | 2026-08-01                |
| H-02 | "Desde 2020, especializados en Data Centers e infraestructura crítica certificada ICREA CCRD."             | Es técnicamente competente / PICC entiende mi caso | E2               | PC — verificar alcance exacto de ICREA CCRD con Dirección                                                    | No afirmar Nivel I-VI sin resolver la inconsistencia ES/EN/FR     | Dirección | 2026-08-01                |
| H-03 | "Equipo multidisciplinario con trayectoria en ingeniería civil, eléctrica, HVAC y telecomunicaciones."     | Es institucionalmente confiable                    | E2               | PC — verificar perfiles reales; reformular si las cifras de años no son exactas                              | No usar "30+ años cada uno" sin verificar individualmente         | Dirección | 2026-08-01                |
| H-04 | "Materiales PANDUIT con garantía de fabricante de 25 años en cableado estructurado."                       | Reduce mi riesgo / Es técnicamente competente      | E2               | PC — verificar tipo de relación con Panduit y autorización de logotipo                                       | No presentar como garantía de PICC; es garantía del fabricante    | Dirección | 2026-08-01                |
| H-05 | "Instalaciones eléctricas de media y baja tensión, HVAC de precisión y cableado estructurado certificado." | PICC entiende mi caso                              | E2               | PC — mantener como capacidades hasta tener al menos 1 caso                                                   | No afirmar resultado; presentar como capacidad                    | Comercial | 2026-09-01                |
| H-06 | "Atendemos proyectos en toda la República Mexicana."                                                       | Tiene cobertura                                    | E2               | PC — verificar si existe evidencia de proyectos fuera de CDMX; retirar "Internacional" hasta tener evidencia | No usar "Internacional" sin proyecto real fuera de México         | Dirección | 2026-08-01                |
| H-07 | "[N] proyectos concluidos, [M] m² ejecutados."                                                             | Tiene experiencia comparable                       | E0               | NP hasta tener inventario + criterio de conteo definido                                                      | No publicar cifras sin metodología documentada                    | Dirección | Bloqueado hasta BKL-P0-01 |

### B. Claims para Ruta ICP-H01

| #      | Texto factual base                                                                                                    | Decisión                   | Evidencia | Condición                                                                          | Owner               |
| ------ | --------------------------------------------------------------------------------------------------------------------- | -------------------------- | --------- | ---------------------------------------------------------------------------------- | ------------------- |
| H01-01 | "Diseño y construcción de Data Centers bajo estándar ICREA-Std-131."                                                  | Es técnicamente competente | E2        | PC — verificar alcance de la certificación; idealmente con 1 caso                  | Dirección + Técnico |
| H01-02 | "Integración de disciplinas: energía crítica, HVAC de precisión, cableado certificado y protección contra incendios." | Tiene capacidad técnica    | E2        | PC — verificar cuáles disciplinas ejecuta PICC directamente y cuáles subcontrata   | Operaciones         |
| H01-03 | "UPS con redundancia N+1 y transferencias automáticas."                                                               | Tiene capacidad técnica    | E1        | PC — verificar si existe proyecto donde se implementó                              | Técnico             |
| H01-04 | "Materiales PANDUIT con garantía de fabricante de 25 años."                                                           | Reduce mi riesgo           | E2        | PC — aclarar que la garantía es del fabricante; verificar autorización de logotipo | Dirección           |
| H01-05 | "Certificación ICREA CCRD para Data Centers."                                                                         | Es técnicamente competente | E2        | PC — verificar alcance exacto: ¿diseño, construcción, certificación o las tres?    | Dirección           |

### C. Claims para Ruta ICP-H02

| #      | Texto factual base                                                                                  | Decisión                | Evidencia | Condición                                                        | Owner       |
| ------ | --------------------------------------------------------------------------------------------------- | ----------------------- | --------- | ---------------------------------------------------------------- | ----------- |
| H02-01 | "Instalaciones eléctricas de media y baja tensión para naves industriales y plantas de producción." | PICC entiende mi caso   | E2        | PC — respaldar con CASO-02; no presentar como caso sin evidencia | Operaciones |
| H02-02 | "Sistemas HVAC para ambientes industriales y comerciales."                                          | Tiene capacidad técnica | E2        | PC — idem H02-01                                                 | Operaciones |
| H02-03 | "[A verificar con Operaciones] Metodología de ejecución por fases para instalaciones en operación." | Reduce mi riesgo        | E0        | NP hasta verificar y documentar proceso real                     | Operaciones |
| H02-04 | "Cableado estructurado certificado para instalaciones industriales."                                | Tiene capacidad técnica | E2        | PC — idem H02-01                                                 | Operaciones |

### D. Claims bloqueados (NP hasta resolución)

| Claim ID         | Claim                                                      | Causa del bloqueo                         | Owner de resolución   | Acción requerida                                 |
| ---------------- | ---------------------------------------------------------- | ----------------------------------------- | --------------------- | ------------------------------------------------ |
| CLM-CRD-03       | Nivel I-VI vs Tier II-III                                  | Contradicción entre versiones ES/EN/FR    | Dirección             | Decidir alcance real y unificar los tres idiomas |
| CLM-EQP-03       | "garantizando resultados de primer nivel en cada proyecto" | Promesa absoluta sin evidencia            | Dirección + Comercial | Eliminar o reformular sin absoluto               |
| CLM-IMP-01/02/03 | Fotos de Unsplash como imágenes propias                    | No son imágenes propias de PICC           | Dirección + Marketing | Reemplazar con fotos reales (BKL-P0-12)          |
| H-07             | Cifras de proyectos y m²                                   | Sin inventario ni criterio de conteo      | Dirección             | Inventariar y definir metodología (BKL-P0-01)    |
| CLM-POS-06       | "Cobertura Internacional"                                  | Sin evidencia de proyecto fuera de México | Dirección             | Verificar; retirar si no hay evidencia           |

---

## Backlog de evidencia priorizado — Alpha Gate 01

| ID     | Claim afectado          | Decisión bloqueada                 | Evidencia faltante                                             | Fuente probable                   | Owner                   | Permiso requerido    | Esfuerzo   | Impacto  | Prioridad    | Fecha objetivo    | Surface bloqueada     |
| ------ | ----------------------- | ---------------------------------- | -------------------------------------------------------------- | --------------------------------- | ----------------------- | -------------------- | ---------- | -------- | ------------ | ----------------- | --------------------- |
| EVB-01 | CLM-CRD-03              | Es técnicamente competente         | Alcance exacto de ICREA CCRD + nivel/tier real                 | Dirección + certificado           | Dirección               | Interno              | Muy bajo   | Crítico  | P0 inmediata | 2026-07-22        | Home S2, Ruta H01     |
| EVB-02 | CLM-CRD-05 / CLM-IMP-04 | Es técnicamente competente         | Tipo de relación Panduit + autorización de logotipo            | Dirección + Panduit               | Dirección               | Autorización Panduit | Bajo       | Crítico  | P0 inmediata | 2026-07-22        | Home S2, Ruta H01     |
| EVB-03 | CLM-MET-01/05/07        | Es institucionalmente confiable    | Año de inicio de actividad del fundador documentado            | Dirección + documento             | Dirección               | Interno              | Muy bajo   | Alto     | P0 inmediata | 2026-07-22        | Home S2, Hero, Footer |
| EVB-04 | CLM-MET-03              | Tiene experiencia comparable       | Inventario de proyectos con criterio de conteo                 | Dirección + Operaciones + archivo | Dirección + Operaciones | Interno              | Bajo-medio | Alto     | P0           | 2026-07-31        | Home S2, Nosotros     |
| EVB-05 | CLM-MET-04              | Tiene experiencia comparable       | M² reales con metodología de cálculo                           | Dirección + Operaciones           | Dirección + Operaciones | Interno              | Bajo-medio | Alto     | P0           | 2026-07-31        | Home S2, Nosotros     |
| EVB-06 | CLM-IMP-01/02/03        | Historia visual real               | Fotos propias con permiso de cliente                           | Dirección + archivo o cliente     | Dirección + Marketing   | Permiso de cliente   | Medio      | Muy alto | P0           | 2026-07-31        | Todo el sitio         |
| EVB-07 | CLM-POS-06              | Tiene cobertura                    | Al menos 1 proyecto fuera de CDMX o México                     | Dirección + Operaciones           | Dirección               | Interno              | Muy bajo   | Medio    | P0           | 2026-07-22        | Nosotros              |
| EVB-08 | CLM-EQP-01/04           | Es institucionalmente confiable    | Perfil real de al menos 3 miembros del equipo                  | Dirección + RH                    | Autorización del equipo | Bajo                 | Alto       | P1       | 2026-08-15   | Sección Equipo    |
| EVB-09 | CLM-CRD-07              | Es técnicamente competente         | Verificar si alguien tiene certificación BICSI                 | Dirección + equipo                | Interno                 | Muy bajo             | Medio      | P1       | 2026-08-01   | Equipo, Ruta H01  |
| EVB-10 | CLM-CAP-01              | Tiene capacidad técnica            | Proyecto donde PICC implementó UPS N+1                         | Dirección + Operaciones           | Permiso de cliente      | Alto                 | Alto       | P1       | 2026-08-31   | Ruta H01          |
| EVB-11 | CLM-CAP-03              | Tiene capacidad técnica            | Confirmar si PICC ejecuta supresión directamente o subcontrata | Operaciones                       | Interno                 | Muy bajo             | Medio      | P0       | 2026-07-22   | Ruta H01          |
| EVB-12 | CLM-IMP-05              | Es técnicamente competente         | Vigencia de certificación ICREA y términos de uso de logo      | ICREA / Dirección                 | Autorización ICREA      | Bajo                 | Alto       | P0       | 2026-07-22   | Home, Ruta H01    |
| EVB-13 | H02-03                  | Reduce mi riesgo (H02)             | Proceso de obra en operación documentado                       | Operaciones                       | Interno                 | Bajo-medio           | Alto       | P0       | 2026-07-31   | Ruta H02          |
| EVB-14 | CASO-01                 | Tiene experiencia comparable (H01) | Caso real de DC con permiso de cliente                         | Dirección + cliente               | Autorización formal     | Alto                 | Muy alto   | P1       | 2026-08-31   | Ruta H01, Home S5 |
| EVB-15 | CASO-02                 | PICC entiende mi caso (H02)        | Caso real de instalación industrial con permiso                | Dirección + cliente               | Autorización formal     | Alto                 | Muy alto   | P1       | 2026-08-31   | Ruta H02, Home S5 |

---

## Riesgos legales y reputacionales identificados

| ID     | Riesgo                                                          | Severidad                                                       | Claims afectados       | Mitigación recomendada                                                      |
| ------ | --------------------------------------------------------------- | --------------------------------------------------------------- | ---------------------- | --------------------------------------------------------------------------- |
| RSK-01 | Uso de logotipo Panduit sin autorización formal                 | Alto — posible reclamación legal                                | CLM-CRD-05, CLM-IMP-04 | Obtener autorización por escrito antes de próxima publicación               |
| RSK-02 | Fotos de Unsplash como imágenes propias                         | Alto — pérdida de credibilidad + verificar licencia comercial   | CLM-IMP-01/02/03       | Verificar licencia; planificar sustitución con fotos propias                |
| RSK-03 | Inconsistencia ICREA Nivel I-VI vs Tier II-III                  | Alto — cualquier buyer técnico de DC detectará la contradicción | CLM-CRD-03             | Resolver con Dirección e ICREA; actualizar los tres idiomas simultáneamente |
| RSK-04 | Cifras de proyectos y m² sin respaldo documental                | Medio — si se audita externamente, daña credibilidad            | CLM-MET-03/04          | No escalar en propuestas sin inventario verificado                          |
| RSK-05 | "Garantía de 25 años" puede interpretarse como garantía de PICC | Medio — puede generar expectativas contractuales                | CLM-CRD-06             | Reformular explicitando que es garantía del fabricante Panduit              |
| RSK-06 | "Cobertura Internacional" sin evidencia                         | Bajo-medio — sobrepromesa de alcance                            | CLM-POS-06             | Retirar hasta tener proyecto fuera de México                                |
| RSK-07 | "Resultados de primer nivel en cada proyecto" promesa absoluta  | Medio — puede generar expectativa contractual                   | CLM-EQP-03             | Reformular o eliminar                                                       |

---

## Decisiones requeridas de Dirección

| #      | Pregunta                                                                                                           | Urgencia | Impacto | Bloquea                      |
| ------ | ------------------------------------------------------------------------------------------------------------------ | -------- | ------- | ---------------------------- |
| DEC-01 | ¿Cuál es el año exacto de inicio de actividad del fundador? ¿Y de PICC como empresa?                               | P0       | Alto    | CLM-MET-01, H-01, EVB-03     |
| DEC-02 | ¿Cuál es exactamente el alcance de ICREA CCRD? ¿Diseño, construcción, certificación de obra? ¿Para qué nivel/tier? | P0       | Crítico | CLM-CRD-01 a 03, EVB-01      |
| DEC-03 | ¿Qué tipo de relación tiene PICC con Panduit? ¿Distribuidor, partner certificado, partner preferente?              | P0       | Alto    | CLM-CRD-05, EVB-02, RSK-01   |
| DEC-04 | ¿Hay autorización formal de Panduit para usar su logotipo?                                                         | P0       | Alto    | CLM-IMP-04, RSK-01           |
| DEC-05 | ¿PICC ejecuta directamente la supresión de incendios FM-200/Novec o la subcontrata?                                | P0       | Medio   | CLM-CAP-03, EVB-11           |
| DEC-06 | ¿Existe algún proyecto fuera de México que sustente la cobertura internacional?                                    | P0       | Medio   | CLM-POS-06, EVB-07           |
| DEC-07 | ¿Cuántos proyectos se han ejecutado y con qué criterio de conteo?                                                  | P0       | Alto    | CLM-MET-03, EVB-04           |
| DEC-08 | ¿Cuáles son los m² reales ejecutados y con qué metodología de medición?                                            | P0       | Alto    | CLM-MET-04, EVB-05           |
| DEC-09 | ¿Hay fotos propias de proyectos o del equipo que puedan usarse con permiso?                                        | P0       | Crítico | CLM-IMP-01/02/03, EVB-06     |
| DEC-10 | ¿Quién es el responsable comercial que recibe leads? ¿Cuál es el SLA real que PICC puede comprometer hoy?          | P0       | Alto    | Proceso de respuesta interna |

---

## Estado de BKL-P0-01/02/03 al cierre del Alpha Gate 01

| Ítem      | Estado                                                                              | Criterios cumplidos                                        | Criterios pendientes                                         |
| --------- | ----------------------------------------------------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------ |
| BKL-P0-01 | En proceso — auditoría ejecutada; validación con Dirección pendiente                | Inventario completo; clasificación E0-E5; acción por claim | Respuestas a DEC-01, DEC-07, DEC-08; fotos propias (EVB-06)  |
| BKL-P0-02 | En proceso — auditoría ejecutada; alcance interno no verificado                     | Claim inventariado; inconsistencia ES/EN/FR identificada   | Respuesta a DEC-02; resolución de CLM-CRD-03                 |
| BKL-P0-03 | En proceso — auditoría ejecutada; tipo de relación y permiso de logo no confirmados | Claim inventariado; riesgo documentado; acción definida    | Respuestas a DEC-03 y DEC-04; autorización formal de Panduit |

Nota: los tres ítems no pueden cerrarse como completados hasta que Dirección responda DEC-01 a DEC-10. La auditoría documental está completa. La validación con fuente primaria es el paso bloqueante.

---

## Recomendación GO / NO GO

**Veredicto: GO CONDICIONADO para diseño de la Home**

Puede comenzar en paralelo con la resolución de claims, con las siguientes condiciones estrictas:

1. Ningún claim E0 o NP puede usarse en el diseño como texto real; solo como placeholder etiquetado.
2. Las fotos de Unsplash deben tratarse como placeholders; no como imágenes aprobadas.
3. La inconsistencia ICREA (Nivel I-VI vs Tier II-III) debe resolverse antes de publicar cualquier versión del sitio.
4. El logotipo de Panduit no debe aparecer en el diseño final sin autorización formal.
5. Las cifras de proyectos y m² deben estar verificadas antes de producción.

Lo que puede empezar ahora:
- Diseño de arquitectura y layout de la Home con placeholders.
- Redacción de copy de rutas H01 y H02 con claims PC o PA.
- Diseño del formulario de preevaluación.
- Redacción de CNT-01 y CNT-02.

Lo que no puede empezar hasta resolver los bloqueos:
- Producción final de Home con claims sin verificar.
- Publicación de cualquier versión del sitio con claims NP en su estado actual.
- Uso del logotipo de Panduit en diseño final sin autorización.

