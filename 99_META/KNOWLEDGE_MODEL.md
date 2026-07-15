# Knowledge Model

## Ficha de Trazabilidad

- ID: KM-001
- Estado: 🟢 Aprobado
- Tipo: Modelo semántico mínimo viable
- Objetivo: Definir el lenguaje común del sistema de conocimiento de PICC NEXT sin sobrearquitectura.
- Entradas:
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
  - DOC-002 (00_MASTER_PLAN/MASTER_PLAN_PICC_NEXT_V3.md)
- Salidas:
  - Entidades canónicas
  - Relaciones canónicas
  - Reglas de validez
- Dependencias:
  - DOC-044 (99_META/REPOSITORY_RULES.md)
- Documentos consumidos:
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
- Documentos generados:
  - DOC-045 (99_META/KNOWLEDGE_GRAPH.md)
  - DOC-046 (INDEX.md)
- Responsable: Arquitectura de conocimiento
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Modelo mínimo, útil y sin sinónimos redundantes

## Entidades mínimas

Investigation, Question, Hypothesis, Source, Evidence, Finding, Insight, Decision, Assumption, Risk, Capability, Asset, Document, Domain, Person.

## Reglas

1. Cada entidad tiene ID permanente.
2. Cada entidad tiene estados permitidos.
3. Toda relación debe ser canónica.
4. No crear entidades nuevas salvo necesidad demostrada.

## Proyección documental

El Knowledge Model se implementa inicialmente con Markdown + YAML + tablas + IDs + relaciones explícitas.
