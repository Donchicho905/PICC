---
artifact_name: "Research Ledger"
artifact_id: "RL-001"
component: "Research Ledger"
state: "Aprobado"
version: "v2.0"
owner: "Direccion Comercial + Producto"
ssot_domain: "research.operations"
consumes:
  - "DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)"
  - "KM-001 (99_META/KNOWLEDGE_MODEL.md)"
produces:
  - "DOC-010 (02_VERDAD_COMERCIAL/Verdad_Comercial.md)"
feeds:
  - "DOC-014 (03_MODELO_COMERCIAL/Modelo_Comercial.md)"
  - "DOC-017 (04_TRUST/Trust_Architecture.md)"
  - "DOC-018 (05_PRODUCTO/Capability_Backlog.md)"
depends_on:
  - "DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)"
---
# Research Ledger

## Ficha de Trazabilidad
- ID: RL-001
- Estado: Aprobado
- Tipo: Ledger de investigaciones
- Objetivo: Registrar cada investigacion con hipótesis, fuentes, evidencia, insight y decision habilitada.
- Entradas:
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
- Salidas:
  - Historial permanente de investigaciones
  - Evidencia asociada
  - Insights y decisiones vinculadas
- Dependencias:
  - KM-001 (99_META/KNOWLEDGE_MODEL.md)
  - KG-001 (99_META/KNOWLEDGE_GRAPH.md)
- Documentos consumidos:
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
- Documentos actualizados:
  - DOC-010 (02_VERDAD_COMERCIAL/Verdad_Comercial.md)
- Responsable: Direccion Comercial + Producto
- Fecha: 2026-07-15
- Dominio SSOT: research.operations
- Version: v2.0
- Criterios de aceptación:
  - Cada investigacion tiene RID, owner, estado, fuentes y decision habilitada
  - El historial es auditable y no se pierde el motivo de la decision

## Campos minimos
RID, nombre, objetivo, categoria, hipotesis, prioridad, estado, owner, fuentes esperadas, fuentes encontradas, nivel de confianza, costo estimado, tiempo estimado, resultado, insight, decision habilitada, documentos afectados, fecha de ultima actualizacion.

## Regla de gobierno de cierre (obligatoria)

Ninguna investigacion puede cerrarse solo con insight.

Toda investigacion debe completar este flujo:

Investigacion -> Evidencia -> Hallazgos -> Insight -> Decision recomendada -> Capacidad impactada -> Documentos actualizados -> Backlog generado

Si falta uno de los elementos, el RID permanece abierto.

## Gates y readiness por RID (obligatorio)

Todo RID debe declarar dos gates independientes y su nivel de readiness:

- Gate A (metodologia): GO/NO GO.
- Gate B (readiness operativo): GO/GO CONDICIONADO/NO GO.
- Readiness: R0..R5.

Escala readiness:
- R0 No iniciado
- R1 Metodo definido
- R2 Fuentes identificadas
- R3 Accesos validados
- R4 Piloto aprobado
- R5 Investigacion lista para ejecutar

## Ledger inicial
| RID        | Nombre                                       | Categoria                 | Prioridad | Estado                                               | Owner                        | Fuentes esperadas                                                         | Fuentes encontradas                                               | Confianza | Costo | Tiempo | Resultado                                                                   | Insight                           | Decision habilitada                                                                                   | Docs afectados                       | Ultima actualizacion |
| ---------- | -------------------------------------------- | ------------------------- | --------- | ---------------------------------------------------- | ---------------------------- | ------------------------------------------------------------------------- | ----------------------------------------------------------------- | --------- | ----- | ------ | --------------------------------------------------------------------------- | --------------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------ | -------------------- |
| VC-RID-001 | Decision Readiness de Home (piloto)          | Investigacion Comercial   | P0        | Sprint 0 cerrado (Gate A GO, Gate B GO CONDICIONADO) | ZEUS + Marketing + Comercial | Sitio, analytics, CRM, Search Console, propuestas, entrevistas, benchmark | Evidencia primaria de Home no disponible en artefactos del sprint | Bajo      | Medio | Bajo   | Metodo validado en piloto; Decision Coverage=0% (0/6 decisiones soportadas) | Gate A=GO; Gate B=GO CONDICIONADO | Mantener ejecucion completa condicionada hasta elevar readiness operativo y mejorar Decision Coverage | DOC-007, DOC-010, DOC-006, RL-001    | 2026-07-15           |
| VC-RID-002 | Origen de demanda por referencia             | Investigacion Comercial   | P1        | Blocked (esperando GO de VC-RID-001)                 | Comercial                    | CRM, pipeline historico                                                   | Pendiente                                                         | Bajo      | Bajo  | Bajo   | Pendiente                                                                   | Pendiente                         | Estrategia comercial                                                                                  | Verdad Comercial, Modelado Comercial | 2026-07-15           |
| RID-003    | ICP de mayor margen y menor friccion         | Investigacion Cliente     | Alta      | Proposed                                             | Comercial + Producto         | CRM, feedback, pipeline                                                   | Pendiente                                                         | Bajo      | Alto  | Alto   | Pendiente                                                                   | Pendiente                         | Diseño del ICP                                                                                        | Modelo Comercial, Customer Journey   | 2026-07-15           |
| RID-004    | Clientes publicables y restricciones         | Investigacion Legal       | Alta      | Proposed                                             | Legal + Comercial            | Contratos, NDA, aprobaciones                                              | Pendiente                                                         | Bajo      | Alto  | Alto   | Pendiente                                                                   | Pendiente                         | Sistema de evidencia                                                                                  | Trust Architecture, Evidence Library | 2026-07-15           |
| RID-005    | Ciclo comercial por vertical                 | Investigacion Comercial   | Alta      | Proposed                                             | Revenue Ops                  | CRM, pipeline historico                                                   | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Customer Journey                                                                                      | Customer Journey, Roadmap            | 2026-07-15           |
| RID-006    | Motivos de perdida por etapa                 | Investigacion Comercial   | Alta      | Proposed                                             | Comercial                    | CRM, notas de perdida                                                     | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Trust Architecture                                                                                    | Trust Architecture, Governance       | 2026-07-15           |
| RID-007    | Inventario A/B/C de evidencia                | Investigacion Evidencia   | Alta      | Proposed                                             | Operaciones + Legal          | Proyectos, documentos, casos                                              | Pendiente                                                         | Bajo      | Alto  | Alto   | Pendiente                                                                   | Pendiente                         | Evidence Library                                                                                      | Evidence Library, Trust Architecture | 2026-07-15           |
| RID-008    | Claims publicables del sitio                 | Investigacion Mercado     | Alta      | Proposed                                             | Marketing + Comercial        | Sitio, decks, propuestas                                                  | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Arquitectura del sitio                                                                                | Trust Architecture, Marketing        | 2026-07-15           |
| RID-009    | Métricas no medidas                          | Investigacion Estrategica | Alta      | Proposed                                             | PMO + Finanzas               | CRM, analytics, proyectos                                                 | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Governance                                                                                            | Governance, North Star               | 2026-07-15           |
| RID-010    | Patrones de proyectos ganados                | Investigacion Comercial   | Media     | Proposed                                             | Producto + Comercial         | Casos ganados, postmortems                                                | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | ICP y propuesta de valor                                                                              | Modelo Comercial, Product Definition | 2026-07-15           |
| RID-011    | Patrones de proyectos perdidos               | Investigacion Comercial   | Media     | Proposed                                             | Comercial + Revenue Ops      | CRM, notas de perdida                                                     | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Modelo comercial                                                                                      | Modelo Comercial, Governance         | 2026-07-15           |
| RID-012    | Objeciones por etapa                         | Investigacion Cliente     | Alta      | Proposed                                             | Comercial + Customer Success | CRM, reuniones, llamadas                                                  | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Journey                                                                                               | Customer Journey, Trust Architecture | 2026-07-15           |
| RID-013    | Capacidades diferenciales vs commodity       | Investigacion Estrategica | Alta      | Proposed                                             | Estrategia + Comercial       | Benchmark, clientes, casos                                                | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Product model                                                                                         | Product Definition, Capability Model | 2026-07-15           |
| RID-014    | Riesgos legales de evidencia                 | Investigacion Legal       | Alta      | Proposed                                             | Legal                        | Contratos, aprobaciones                                                   | Pendiente                                                         | Bajo      | Alto  | Alto   | Pendiente                                                                   | Pendiente                         | Evidence Library                                                                                      | Evidence Library, Marketing          | 2026-07-15           |
| RID-015    | Conocimiento critico tacito                  | Investigacion Operativa   | Media     | Proposed                                             | PMO + Operaciones            | Responsables, procesos                                                    | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Knowledge Program                                                                                     | Knowledge Program, Governance        | 2026-07-15           |
| RID-016    | Tiempos de respuesta comercial               | Investigacion Comercial   | Alta      | Proposed                                             | Comercial                    | CRM, correos, timestamps                                                  | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Operating model                                                                                       | Customer Journey, Operating Model    | 2026-07-15           |
| RID-017    | Decisiones tardias por falta de comparadores | Investigacion Producto    | Alta      | Proposed                                             | Producto + Comercial         | Entrevistas, propuestas                                                   | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Decision Architecture                                                                                 | Decision Architecture, Product Model | 2026-07-15           |
| RID-018    | Costo de no calidad comercial                | Investigacion Financiera  | Media     | Proposed                                             | Finanzas + PMO               | Horas, retrabajos, propuestas                                             | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Governance                                                                                            | Governance, Economy of Knowledge     | 2026-07-15           |
| RID-019    | Dependencias externas de cierre              | Investigacion Operativa   | Media     | Proposed                                             | PMO + Comercial              | Clientes, terceros                                                        | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Operating model                                                                                       | Operating Model, Governance          | 2026-07-15           |
| RID-020    | Actividades a dejar de hacer                 | Investigacion Operativa   | Media     | Proposed                                             | Direccion + PMO              | Backlog, tiempos, tareas                                                  | Pendiente                                                         | Bajo      | Medio | Medio  | Pendiente                                                                   | Pendiente                         | Simplificacion operativa                                                                              | Operating Model, Roadmap             | 2026-07-15           |

## Readiness por RID (snapshot)

| RID              | Gate A      | Gate B          | Readiness | Nota                                                    |
| ---------------- | ----------- | --------------- | --------- | ------------------------------------------------------- |
| VC-RID-001       | GO          | GO CONDICIONADO | R2        | Pendiente elevar a R3 con condiciones R3-C1/R3-C2/R3-C3 |
| VC-RID-002       | NO EVALUADO | NO EVALUADO     | R1        | Bloqueado hasta Gate B=GO de VC-RID-001                 |
| RID-003..RID-020 | NO EVALUADO | NO EVALUADO     | R0        | Sin piloto metodologico especifico                      |

## Reglas del ledger
1. Todo RID debe apuntar a una decision habilitada o a una razon de descarte.
2. Todo hallazgo debe producir al menos un insight.
3. Todo insight debe impactar capacidades o documentos.
4. El ledger es append-only en principio; correcciones con rastro de version.

## Matriz de hallazgos accionables (obligatoria)

| Hallazgo              | Evidencia          | Impacto           | Riesgo                   | Capacidad afectada  | Prioridad | Recomendacion       | Documento a actualizar | Backlog generado  |
| --------------------- | ------------------ | ----------------- | ------------------------ | ------------------- | --------- | ------------------- | ---------------------- | ----------------- |
| Completar al ejecutar | Fuente verificable | Negocio/operacion | Probabilidad x severidad | Capacidad comercial | P0/P1/P2  | Decision accionable | DOC-ID y ruta          | RID/TASK derivado |
