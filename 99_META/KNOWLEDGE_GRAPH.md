# Knowledge Graph

## Ficha de Trazabilidad

- ID: KG-001
- Estado: 🟢 Aprobado
- Tipo: Modelo lógico de relaciones
- Objetivo: Representar las relaciones entre investigaciones, evidencia, hallazgos, insights, decisiones y documentos sin construir tecnologia de grafo aun.
- Entradas:
  - KM-001 (99_META/KNOWLEDGE_MODEL.md)
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
- Salidas:
  - Relaciones canónicas
  - Vistas navegables
- Dependencias:
  - KM-001 (99_META/KNOWLEDGE_MODEL.md)
- Documentos consumidos:
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
- Documentos generados:
  - DOC-046 (INDEX.md)
  - DOC-045 (99_META/SYSTEM_MAP.md)
- Responsable: Arquitectura de conocimiento
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Un nodo o relación se entiende sin ambigüedad

## Relaciones canónicas

- INVESTIGATION_TESTS_HYPOTHESIS
- INVESTIGATION_USES_SOURCE
- SOURCE_PRODUCES_EVIDENCE
- EVIDENCE_SUPPORTS_FINDING
- EVIDENCE_CONTRADICTS_FINDING
- FINDING_PRODUCES_INSIGHT
- INSIGHT_SUPPORTS_DECISION
- DECISION_REJECTS_HYPOTHESIS
- DECISION_UPDATES_DOCUMENT
- DECISION_PRIORITIZES_CAPABILITY
- RISK_BLOCKS_DECISION
- ASSUMPTION_REQUIRES_VALIDATION
- DOCUMENT_CONSUMES_INSIGHT
- DOCUMENT_IS_SSOT_FOR_DOMAIN
- ASSET_ENABLES_CAPABILITY

## Regla

El Knowledge Graph es el modelo lógico central; el Knowledge Tree es solo una proyección navegable para humanos.
