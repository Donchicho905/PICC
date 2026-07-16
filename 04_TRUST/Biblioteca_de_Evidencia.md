# Biblioteca de Evidencia

## Ficha de Trazabilidad
- ID: DOC-015
- Estado: 🟡 En desarrollo
- Tipo: Evidence Library — Registro operativo de activos de confianza del MVP
- Objetivo: Registrar todos los activos de evidencia disponibles o candidatos, con su nivel, permiso, brecha y prioridad para el Growth MVP V1.
- Entradas:
  - DOC-016 (04_TRUST/Sistema_de_Evidencia.md)
  - DOC-033 (08_IMPLEMENTACION/MVP.md — Sección 6 y 7)
- Salidas:
  - Inventario de trust assets con estado real
  - Shortlist de casos priorizada
  - Registro de permisos
- Dependencias:
  - DOC-017 (04_TRUST/Trust_Architecture.md)
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md)
- Documentos consumidos:
  - Trust_Architecture.md — tipos de trust assets
  - MVP.md — shortlist de casos y trust assets
- Responsable: Dirección + Operaciones + Marketing
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Cada activo tiene ID, nivel, permiso y surface asignados
  - Estado de evidencia es honesto; ningún gap se oculta
  - Shortlist de casos tiene prioridad y owner explícitos

## Estado general de la biblioteca al 2026-07-15

Ningún activo de evidencia ha alcanzado nivel E4 al inicio del Growth MVP V1.
Todos los activos listados aquí son candidatos, señales o parciales (E1-E2).
La biblioteca se activará operativamente conforme se construyan casos y se gestionen permisos.

## Registro de trust assets

### Activos de credencial institucional

| ID     | Asset                    | Tipo                  | ICP      | Nivel actual | Permiso                | Owner           | Estado operativo                                             | Brecha                                        | Prioridad |
| ------ | ------------------------ | --------------------- | -------- | ------------ | ---------------------- | --------------- | ------------------------------------------------------------ | --------------------------------------------- | --------- |
| TA-03  | Certificación ICREA CCRD | Credencial técnica    | H01      | E2           | Pendiente verificación | Dirección       | No publicable — requiere documentación de alcance            | Alcance exacto no documentado en repo         | P0        |
| TA-04  | Relación con Panduit     | Credencial partner    | H01      | E2           | Pendiente verificación | Dirección       | No publicable — tipo de relación no verificado               | Contrato o acuerdo no visto en repo           | P0        |
| TA-05a | 25+ años de experiencia  | Métrica institucional | H01, H02 | E2           | Interno                | Dirección       | No publicable definitivamente — requiere respaldo documental | Año exacto de fundación sin documento en repo | P0        |
| TA-05b | 100+ proyectos           | Métrica institucional | H01, H02 | E2           | Interno                | Dirección + Ops | No publicable definitivamente                                | Inventario de proyectos no existe en repo     | P0        |
| TA-05c | 50,000+ m² ejecutados    | Métrica institucional | H01, H02 | E2           | Interno                | Dirección + Ops | No publicable definitivamente                                | Metodología de cálculo no documentada         | P0        |
| TA-10  | Ficha de equipo técnico  | Activo institucional  | H01, H02 | E1           | Interno                | Dirección       | No publicable — sin perfil estructurado                      | Equipo no documentado con perfil publicable   | P1        |
| TA-11  | Registro legal / fiscal  | Activo institucional  | H01, H02 | E0-E2        | Interno                | Dirección       | No publicable en sitio — referencia interna solo             | No disponible en repo                         | P1        |

### Activos de casos y proyectos

| ID      | Asset                                      | Tipo          | ICP | Nivel actual | Permiso   | Owner           | Estado operativo                                          | Brecha                                                    | Prioridad    |
| ------- | ------------------------------------------ | ------------- | --- | ------------ | --------- | --------------- | --------------------------------------------------------- | --------------------------------------------------------- | ------------ |
| CASO-01 | Caso Data Center / infraestructura crítica | Caso de éxito | H01 | E0           | Pendiente | Dirección + Ops | No existe — por construir                                 | Sin caso documentado, sin permiso                         | P0 — crítico |
| CASO-02 | Caso instalación eléctrica industrial      | Caso de éxito | H02 | E0           | Pendiente | Dirección + Ops | No existe — por construir                                 | Sin caso documentado, sin permiso                         | P0 — crítico |
| CASO-03 | Caso HVAC crítico o industrial             | Caso de éxito | H02 | E0           | Pendiente | Dirección + Ops | No existe — por construir                                 | Sin caso documentado, sin permiso                         | P0           |
| CASO-04 | Caso remodelación o adecuación corporativa | Caso de éxito | H03 | E1           | Pendiente | Dirección       | No publicable — sin documentación ni permiso              | Señal de actividad corporativa pero sin caso estructurado | P1           |
| CASO-05 | Caso desarrollo inmobiliario / amenity     | Caso de éxito | H04 | E1           | Pendiente | Dirección       | No publicable — señal real (BeGrand) pero sin caso formal | Datos sensibles; cliente no contactado                    | P1           |
| CASO-06 | Caso residencial premium                   | Caso de éxito | H06 | E1           | Pendiente | Dirección       | No publicable                                             | Señal de actividad residencial sin detalle                | P2           |

### Activos de metodología y proceso

| ID     | Asset                                     | Tipo                   | ICP      | Nivel actual | Permiso       | Owner               | Estado operativo                      | Brecha                                 | Prioridad |
| ------ | ----------------------------------------- | ---------------------- | -------- | ------------ | ------------- | ------------------- | ------------------------------------- | -------------------------------------- | --------- |
| TA-07a | Proceso de trabajo de PICC (5 pasos)      | Metodología            | H01, H02 | E0           | N/A — interno | Operaciones         | No publicable — hipótesis no validada | Proceso no documentado ni verificado   | P0        |
| TA-07b | Metodología de obra en operación          | Metodología específica | H02      | E0           | N/A — interno | Operaciones         | No publicable                         | Metodología no existe como documento   | P0        |
| TA-07c | Discovery técnico / checklist de proyecto | Metodología            | H01, H02 | E0           | N/A — interno | Comercial + Técnico | No existe — por crear                 | Sin framework de discovery documentado | P0        |

### Activos de referencia y testimonios

| ID    | Asset                     | Tipo       | ICP           | Nivel actual | Permiso   | Owner                 | Estado operativo | Brecha                                       | Prioridad |
| ----- | ------------------------- | ---------- | ------------- | ------------ | --------- | --------------------- | ---------------- | -------------------------------------------- | --------- |
| TA-08 | Referencia autorizada H01 | Referencia | H01           | E0           | Pendiente | Dirección + Comercial | No existe        | Sin referencias estructuradas ni autorizadas | P1        |
| TA-09 | Referencia autorizada H02 | Referencia | H02           | E0           | Pendiente | Dirección + Comercial | No existe        | Sin referencias estructuradas ni autorizadas | P1        |
| TA-12 | Testimonios de clientes   | Testimonio | H02, H03, H05 | E0           | Pendiente | Dirección + Comercial | No existe        | Sin testimonios estructurados ni autorizados | P2        |

### Activos visuales

| ID    | Asset                                | Tipo   | ICP           | Nivel actual | Permiso   | Owner                 | Estado operativo            | Brecha                              | Prioridad |
| ----- | ------------------------------------ | ------ | ------------- | ------------ | --------- | --------------------- | --------------------------- | ----------------------------------- | --------- |
| TA-06 | Fotografías de proyectos con permiso | Visual | H01, H02, H03 | E0           | Pendiente | Dirección + Marketing | No existe inventario activo | Sin inventario de fotos autorizadas | P0        |

## Shortlist priorizada de casos para construir

| Posición | Caso                                            | ICP | Por qué es prioritario                            | Bloqueador principal                                     | Owner de levantamiento |
| -------- | ----------------------------------------------- | --- | ------------------------------------------------- | -------------------------------------------------------- | ---------------------- |
| 1        | CASO-01 — Data Center o infraestructura crítica | H01 | ICP prioritario; no hay ninguna evidencia de caso | Identificar proyecto candidato + permiso                 | Dirección              |
| 2        | CASO-02 — Instalación industrial eléctrica      | H02 | ICP prioritario 2; essential para ruta H02        | Identificar proyecto candidato + permiso                 | Dirección + Ops        |
| 3        | CASO-03 — HVAC industrial o crítico             | H02 | Refuerza ruta H02 con segunda disciplina visible  | Identificar proyecto candidato + permiso                 | Dirección + Ops        |
| 4        | CASO-04 — Corporativo / oficinas                | H03 | Extiende cobertura a tercer ICP                   | Identificar proyecto con imagen autorizada               | Dirección              |
| 5        | CASO-05 — Desarrollo inmobiliario               | H04 | Hay señal real pero datos sensibles               | Gestionar permiso de cliente; verificar confidencialidad | Dirección              |

## Registro de permisos

| ID asset | Cliente               | Tipo de permiso solicitado | Fecha solicitud | Respuesta | Alcance autorizado | Restricciones | Owner     |
| -------- | --------------------- | -------------------------- | --------------- | --------- | ------------------ | ------------- | --------- |
| CASO-01  | Pendiente identificar | Por definir                | —               | —         | —                  | —             | Dirección |
| CASO-02  | Pendiente identificar | Por definir                | —               | —         | —                  | —             | Dirección |
| CLM-03   | Panduit               | Uso de logotipo            | —               | —         | —                  | —             | Dirección |

## Próximos pasos operativos

1. Identificar proyecto candidato para CASO-01 desde archivo histórico o memoria del equipo.
2. Identificar proyecto candidato para CASO-02.
3. Verificar alcance de certificación ICREA y documentar.
4. Auditar relación con Panduit y obtener autorización de uso de logo.
5. Levantar inventario de fotos disponibles internamente y clasificar permisos.
6. Documentar proceso de trabajo interno para validar hipótesis de TA-07a.


---

## Alpha Gate 01 — Hallazgos sobre activos visuales y credenciales (2026-07-15)

### Confirmación de estado E0 en activos visuales

El snapshot simultáneo de `picc.com.mx`, `picc.com.mx/en` y `picc.com.mx/fr` confirmó que las tres imágenes del sitio son de Unsplash:

| Asset en sitio                | URL de origen                    | Confirmación  | Impacto                             |
| ----------------------------- | -------------------------------- | ------------- | ----------------------------------- |
| Imagen Hero (fondo principal) | Unsplash — construcción genérica | Confirmado E0 | Invalida claim implícito CLM-IMP-01 |
| Foto de equipo                | Unsplash — equipo genérico       | Confirmado E0 | Invalida claim implícito CLM-IMP-02 |
| Foto de Data Center           | Unsplash — Data Center genérico  | Confirmado E0 | Invalida claim implícito CLM-IMP-03 |

**Acción**: TA-06 permanece en E0. Estado operativo actualizado de "No existe inventario activo" a "Activos del sitio actual son de stock; no publicables como imágenes propias de PICC."

### Actualización de estado TA-06

| Campo            | Valor anterior              | Valor actual                                                                      |
| ---------------- | --------------------------- | --------------------------------------------------------------------------------- |
| Nivel actual     | E0                          | E0 — confirmado post-auditoría                                                    |
| Estado operativo | No existe inventario activo | Las 3 imágenes en producción son de Unsplash; no representan obra o equipo propio |
| Acción           | Levantar inventario         | Confirmar si existen fotos propias en archivo; planificar sesión fotográfica      |

### Estado de permisos de logotipos

| Logotipo   | Uso en sitio                                             | Estado de autorización                             | Riesgo                     | Acción recomendada                                                 |
| ---------- | -------------------------------------------------------- | -------------------------------------------------- | -------------------------- | ------------------------------------------------------------------ |
| PANDUIT    | ES: sin calificador / EN: "Certified" / FR: "Partenaire" | Sin verificar — sin autorización formal en repo    | ALTO — RSK-01              | Obtener autorización escrita antes de próxima publicación (DEC-04) |
| ICREA CCRD | Aparece en badge de Hero y en footer                     | Sin verificar — sin acuerdo de uso de logo en repo | MEDIO — RSK-01 relacionado | Verificar con ICREA vigencia y términos de uso del logo (EVB-12)   |

### Actualización del Registro de permisos

| ID asset                   | Tercero | Tipo de permiso                    | Fecha solicitud | Respuesta | Estado        | Owner     |
| -------------------------- | ------- | ---------------------------------- | --------------- | --------- | ------------- | --------- |
| CLM-IMP-04 (logo Panduit)  | Panduit | Uso de logotipo en sitio web       | —               | —         | No solicitado | Dirección |
| CLM-IMP-05 (logo ICREA)    | ICREA   | Uso de logotipo en sitio web       | —               | —         | No verificado | Dirección |
| CLM-CRD-05 (relación tipo) | Panduit | Certificación o partnership formal | —               | —         | No verificado | Dirección |

### Hallazgo de inconsistencia en credencial ICREA (BKL-P0-02)

La versión ES del sitio afirma "Diseño Nivel I al VI ICREA" mientras que EN y FR afirman "Tier II and III Design". Esto no puede resolverse con el documento disponible en el repo; requiere consulta directa con Dirección (DEC-02).

**Impacto en TA-03 (Certificación ICREA CCRD)**:

| Campo            | Valor anterior                                    | Valor actual                                                                                                   |
| ---------------- | ------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Nivel actual     | E2                                                | E1 — revisado a la baja por inconsistencia entre versiones                                                     |
| Estado operativo | No publicable — requiere documentación de alcance | No publicable — inconsistencia activa entre idiomas; requiere resolución antes de publicar en cualquier idioma |
| Acción           | Verificar alcance exacto con Dirección            | Responder DEC-02; unificar los tres idiomas simultáneamente                                                    |

