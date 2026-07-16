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

