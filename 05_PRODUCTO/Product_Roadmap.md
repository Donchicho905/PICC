# Product Roadmap

## Ficha de Trazabilidad
- ID: DOC-022
- Estado: 🟡 En desarrollo
- Tipo: Growth MVP V1 — Hoja de ruta de releases
- Objetivo: Secuenciar la implementación del Growth MVP V1 en releases con criterios de avance claros y dependencias explícitas.
- Entradas:
  - DOC-018 (05_PRODUCTO/Capability_Backlog.md)
  - DOC-033 (08_IMPLEMENTACION/MVP.md)
- Salidas:
  - Secuencia de releases
  - Criterios de avance entre releases
  - Hitos medibles
- Dependencias:
  - DOC-015 (04_TRUST/Biblioteca_de_Evidencia.md)
  - DOC-016 (04_TRUST/Sistema_de_Evidencia.md)
- Responsable: Producto + Dirección
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Cada release tiene contenido, criterio de avance y owner
  - Las dependencias entre releases son explícitas
  - No hay funcionalidades V2/V3 en MVP Alpha o Beta
  - El roadmap puede ejecutarse sin reinterpretar estrategia

## Principio de release

Cada release requiere criterios de éxito medibles antes de avanzar al siguiente. No se cierra un release sin haber evaluado al menos sus métricas críticas.

---

## MVP Alpha — Lanzamiento mínimo responsable

### Contenido

Todos los ítems BKL-P0-01 al BKL-P0-16 del Capability Backlog.

Resumen de capacidades:
- Claims auditados (años, proyectos, m², ICREA, Panduit).
- Arquitectura de Home aprobada.
- Ruta ICP-H01 publicada.
- Ruta ICP-H02 publicada.
- Proceso de trabajo documentado y validado.
- Formulario de preevaluación funcional.
- Proceso interno de respuesta con SLA.
- CRM básico activo.
- Analytics GA4 instalado con eventos de CTA y formulario.
- Fotografías de proyectos con permiso publicadas.
- CTA diferenciada por ICP.
- CNT-01: guía Data Center publicada.
- CNT-02: guía instalaciones industriales publicada.
- CNT-05: checklist descargable con captura de correo.

### Criterios de avance a MVP Beta

Todos los criterios deben cumplirse antes de declarar Alpha completo:

| Criterio                           | Fuente                    | Umbral mínimo                                                  |
| ---------------------------------- | ------------------------- | -------------------------------------------------------------- |
| Claims auditados y respaldados     | Claim Register en DOC-016 | 100% de CLM-01 a CLM-06 tienen fuente interna                  |
| Rutas H01 y H02 publicadas         | Sitio activo              | Ambas rutas accesibles con contenido completo                  |
| Formulario de preevaluación activo | Envíos reales             | Al menos 1 envío procesado correctamente                       |
| SLA de respuesta operando          | Registro en CRM           | 100% de leads reciben respuesta en <48h por 2 semanas seguidas |
| GA4 activo con eventos             | Analytics                 | Eventos de CTA y formulario disparando correctamente           |
| Proceso interno formalizado        | Documento aprobado        | Protocolo escrito y aprobado por Dirección                     |
| Fotografías con permiso publicadas | Sitio                     | Mínimo 3 fotos con permiso confirmado                          |

### Estimación de esfuerzo

Esfuerzo total Alpha: bajo-medio. La mayor parte del trabajo es documental, de auditoría y de contenido. El bloqueador más probable es el tiempo de auditoría de claims y la obtención de fotos con permiso.

---

## MVP Beta — Mejora de conversión y profundidad

### Contenido

Todos los ítems BKL-P1-01 al BKL-P1-11 del Capability Backlog.

Resumen de capacidades:
- CASO-01: caso Data Center publicable (E4).
- CASO-02: caso industrial publicable (E4).
- CNT-03: artículo de comparación de integradoras.
- CNT-04: guía de certificaciones Data Center.
- Ficha de equipo técnico publicable.
- Referencia autorizada H01 y H02.
- Search Console habilitado.
- FAQ técnica por ICP publicada.
- Plantilla de propuesta defendible.
- Inventario de proyectos históricos.

### Criterios de avance a V1.1+

| Criterio                                                  | Fuente                  | Umbral mínimo                             |
| --------------------------------------------------------- | ----------------------- | ----------------------------------------- |
| Al menos 1 caso E4 publicado para H01                     | Biblioteca de Evidencia | CASO-01 en E4 con permiso confirmado      |
| Al menos 1 caso E4 publicado para H02                     | Biblioteca de Evidencia | CASO-02 en E4 con permiso confirmado      |
| Decision Coverage H01 ≥ 65%                               | Auditoría interna       | Evaluación manual de decisiones cubiertas |
| Decision Coverage H02 ≥ 60%                               | Auditoría interna       | Evaluación manual de decisiones cubiertas |
| Tasa de respuesta en SLA ≥ 95%                            | CRM                     | Durante el período Beta                   |
| Al menos 3 oportunidades calificadas generadas            | CRM                     | Por mes durante 2 meses consecutivos      |
| Plantilla de propuesta usada en al menos 1 propuesta real | Registro interno        | Aprobada o en uso                         |

### Aprendizaje requerido antes de Beta

Antes de lanzar Beta, revisar:
- ¿Qué ICP está generando más contactos? ¿Coincide con H01 y H02?
- ¿Dónde se cae el funnel? ¿En el formulario, en la respuesta o en la reunión?
- ¿Los claims auditados son suficientes o hay claims en uso que aún no tienen respaldo?

---

## MVP V1.1+ — Aprendizaje y escala

### Contenido

Todos los ítems BKL-P2-01 al BKL-P2-08 del Capability Backlog.

Resumen de capacidades:
- CASO-03: HVAC industrial.
- CASO-04: corporativo.
- Loop win/loss estructurado.
- Testimonios publicables.
- Board pack para buyer complejo.
- Ruta ICP-H03.
- Dashboard de métricas.
- Programa de contenido ampliado.

### Principio de ingreso a V1.1+

No iniciar V1.1+ mientras:
- Los casos H01 y H02 no estén publicados.
- El funnel desde formulario a oportunidad no esté instrumentado.
- No haya al menos 10 leads registrados con clasificación completa.

---

## Bloqueadores críticos del roadmap

| Bloqueador                                 | Impacto                                                          | Alpha/Beta                     | Resolución sugerida                                              |
| ------------------------------------------ | ---------------------------------------------------------------- | ------------------------------ | ---------------------------------------------------------------- |
| No hay casos E4                            | Sin Decision Coverage adecuado en rutas ICP                      | Bloquea paso Alpha→Beta        | Identificar proyectos candidatos esta semana; gestionar permiso  |
| No hay auditoría de claims institucionales | Riesgo reputacional y legal si se publica con datos sin respaldo | Bloquea MVP Alpha              | Dedicar 1 día a auditoría interna con Dirección                  |
| No hay acceso a Analytics / Search Console | Sin aprendizaje de demanda ni funnel visible                     | Bloquea aprendizaje post-Alpha | Gestionar acceso técnico al sitio                                |
| No hay proceso de respuesta formalizado    | Los leads capturados no se responden con consistencia            | Bloquea lanzamiento            | Protocolizar en documento; aprobado antes de publicar formulario |
| No hay fotos autorizadas                   | Sin evidencia visual, la Home pierde credibilidad                | Bloquea MVP Alpha funcional    | Inventariar fotos existentes y gestionar permisos                |

## Gobierno del roadmap

- Revisión de avance: quincenal durante Alpha.
- Revisión de avance: mensual durante Beta y V1.1+.
- Responsable de avance: Dirección + Comercial + Producto.
- Criterio de pausa: si el SLA de respuesta cae por debajo del 80% por 2 semanas, pausar captación y resolver el proceso interno antes de continuar.
- Criterio de pivote: si después de 60 días de Beta no se generan oportunidades calificadas para H01, revisar el mensaje y el ICP antes de ampliar el presupuesto de captación.

