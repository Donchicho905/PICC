# Knowledge Product Alpha — Candidatos de Activos

**Fecha:** 2026-07-15  
**Sprint base:** Buyer Curiosity Engine V1  
**Referencia:** DOC-048-ALPHA  
**Propósito:** Definir 3 activos canónicos con 5–7 preguntas semilla cada uno, proof of concept para Knowledge Product V1.

---

## Executive Summary

Basado en Top 100 de BCE V1, proponemos 3 Knowledge Products Alpha para ejecución inmediata:

1. **Diagnóstico de Riesgo Operativo** (KPR-01) ← 7 semillas P0
2. **Justificación Financiera Ejecutiva** (KPR-02) ← 6 semillas P0
3. **Gobernanza de Comité & Decisión** (KPR-03) ← 5 semillas P0

**Criterios de selección:**
- Intersection de 3+ ICPs (máxima reutilización)
- Trigger crítico (TRG-001, TRG-004, TRG-008, TRG-012)
- Buyer state C0–C1 (early intervention high impact)
- Evidence gap significativo (gap mapping en DOC-048 § 11)

**Impacto esperado:**
- Cobertura de ~60% de deal cycles (operación + finanzas + gobernanza)
- Reducir ciclo de decisión en ~30% vía preguntas preformuladas
- Establecer patrón de replicación para Knowledge Products V2+

---

## 1. Knowledge Product Alpha #1: Diagnóstico de Riesgo Operativo

**KPR-01 Metadata**
- **ID canónico:** KPR-01
- **Nombre corto:** RiskDiag
- **Estado:** Alpha Candidate
- **Consumidores primarios:** H01 (Director Técnico), H03 (Operaciones), H04 (Compliance)
- **Buyers states servidos:** C0 → C1 → C2
- **Buyer journey:** Latencia → Fricción → Formulación
- **Trigger primario:** TRG-001 (Caída operacional), TRG-002 (Microparos)
- **Objetivo:** En 30 min, comprador técnico sin asesor, transforma síntoma en diagnóstico comunicable al sponsor.

**Estructura canónica**

| Componente                 | Descripción                                                   | Activo Entregable        |
| -------------------------- | ------------------------------------------------------------- | ------------------------ |
| **Entrada**                | Síntoma: "Sistema intermitente últimas 48h"                   | Template de intake       |
| **Preguntas P0 (7)**       | Diagnóstico estructurado                                      | Decision tree + Q-bank   |
| **Lógica de ramificación** | IF-THEN rules por respuesta                                   | Flowchart executable     |
| **Salida**                 | Reporte ejecutivo: Riesgo + opciones + presupuesto indicativo | Markdown template        |
| **Éxito**                  | Sponsor entiende opciones, comité puede votar                 | Trazabilidad de decisión |

**7 Preguntas Semilla**

| #   | BCQ  | Pregunta                                                     | Tipo Respuesta                                                     | Ramificación         | Propósito                |
| --- | ---- | ------------------------------------------------------------ | ------------------------------------------------------------------ | -------------------- | ------------------------ |
| 1   | 0001 | ¿Qué operación crítica puede detenerse hoy sin aviso?        | Checkbox [Prod / TI / Logística / Finanzas / Cumplimiento]         | → Severity grade     | Scope de impacto         |
| 2   | 0010 | ¿Cuánta continuidad operativa necesitamos exactamente?       | Radio [99.99% / 99.9% / 99% / 95% / <95%]                          | → Requirement level  | SLA baseline             |
| 3   | 0015 | ¿Cuál es la peor consecuencia del riesgo no contestado?      | Text resume + Estimated $loss                                      | → Urgency tier       | Business impact          |
| 4   | 0020 | ¿Cuál es la diferencia entre fallo probable y fallo crítico? | MTBF-MTTR analysis (2 numeric inputs)                              | → Risk matrix        | Technical severity       |
| 5   | 0035 | ¿Es el trigger percibido análogo a triggers históricos?      | Autocomplete [Yes / Similar past event] + details                  | → Precedent weight   | Learning from history    |
| 6   | 0050 | ¿Qué acción mínima reduce más riesgo este trimestre?         | Multi-select [Upgrade / Training / Procedure / Monitoring / Other] | → Priority ranking   | Quick win identification |
| 7   | 0095 | ¿Qué opciones técnicamente viables existen hoy?              | Rating each of 4 pre-defined options (1–5 scale)                   | → Feasibility filter | Constraint mapping       |

**Artefactos entregables (Alpha)**

1. **RiskDiag_Decision_Tree.md** — Flowchart de 7Q → Reporte
2. **RiskDiag_Question_Bank.json** — Metadatos, validators, logic rules
3. **RiskDiag_Output_Template.md** — Formato de reporte ejecutivo
4. **RiskDiag_Training_Guide.md** — Cómo facilitar diagnóstico (30 min duration)

**Métrica de éxito (Alpha)**
- ✅ 5 diagnósticos internos completados sin facilitation externa
- ✅ Output aceptado por sponsor sin rework
- ✅ Tiempo promedio ≤ 35 min (target 30 min)
- ✅ Decisión bajada 48h más rápido vs. sin producto

---

## 2. Knowledge Product Alpha #2: Justificación Financiera Ejecutiva

**KPR-02 Metadata**
- **ID canónico:** KPR-02
- **Nombre corto:** FinJustify
- **Estado:** Alpha Candidate
- **Consumidores primarios:** H02 (CFO/Sponsor), H02 (Controller), H04 (FP&A)
- **Buyers states servidos:** C2 → C3 → C4
- **Buyer journey:** Formulación → Comparación → Defensa
- **Trigger primario:** TRG-005 (Expansión capacidad), TRG-012 (Presión de margen)
- **Objetivo:** En 45 min, CFO construye business case cuantitativo defendible ante comité ejecutivo.

**Estructura canónica**

| Componente                 | Descripción                                                           | Activo Entregable           |
| -------------------------- | --------------------------------------------------------------------- | --------------------------- |
| **Entrada**                | Opportunity sizing + 2–3 opciones técnicas + presupuesto aprox        | Template de intake          |
| **Preguntas P0 (6)**       | Análisis financiero estructurado                                      | Q-bank + calculators        |
| **Calculadores embebidos** | NPV, IRR, Payback, Scenario sensitivity                               | Excel/JS snippets           |
| **Asunciones**             | Default assumptions, override capability                              | Assumption table            |
| **Salida**                 | Executive summary: Case selection + financial proof + risk mitigation | Deck template               |
| **Éxito**                  | Comité ejecutivo aprueba presupuesto en sesión                        | Funding decision documented |

**6 Preguntas Semilla**

| #   | BCQ  | Pregunta                                                | Tipo Respuesta                                                                         | Calculador           | Propósito                   |
| --- | ---- | ------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------- | --------------------------- |
| 1   | 0050 | ¿Qué acción mínima reduce más riesgo este trimestre?    | Multi-select opciones + presupuesto estimado c/u                                       | ROI ranking          | Cost-benefit prioritization |
| 2   | 0120 | ¿Cuál es el costo financiero de posponer esta decisión? | Numeric: Loss/month × months deferred                                                  | Delay penalty        | Urgency quantification      |
| 3   | 0130 | ¿Cuál es el break-even timeline para ROI?               | Year break-even + IRR% target                                                          | NPV calculator       | Payback credibility         |
| 4   | 0145 | ¿Se puede estructurar como capex vs. opex?              | Radio [Capex / Opex / Hybrid] + split %                                                | Accounting treatment | P&L/BS impact               |
| 5   | 0175 | ¿Cuál es la evidencia que convence al comité de hoy?    | Checkbox [Industry benchmark / Case study / Internal precedent / Similar SLA contract] | Credibility scoring  | Persuasion strategy         |
| 6   | 0210 | ¿Qué competidor intenta solución similar?               | Text + competitive timing                                                              | Time pressure model  | Market urgency              |

**Artefactos entregables (Alpha)**

1. **FinJustify_Business_Case_Builder.md** — Guía paso-a-paso
2. **FinJustify_Question_Bank.json** — 6Q + default asunciones
3. **FinJustify_Calculators.js** — NPV, IRR, Payback embebidos
4. **FinJustify_Executive_Deck_Template.pptx** — Slide deck format pre-built
5. **FinJustify_Sensitivity_Model.xlsx** — Scenario analysis (best/base/worst)

**Métrica de éxito (Alpha)**
- ✅ 3 business cases completados en ≤ 50 min c/u
- ✅ Deck generada automática, editable por CFO
- ✅ Comité aprobó casos sin pedir recalculations
- ✅ Documentación de decisión financiera trazable

---

## 3. Knowledge Product Alpha #3: Gobernanza de Comité & Decisión

**KPR-03 Metadata**
- **ID canónico:** KPR-03
- **Nombre corto:** DecisionGov
- **Estado:** Alpha Candidate
- **Consumidores primarios:** H02 (Sponsor), H04 (Compliance/Risk), H06 (Legal/Board)
- **Buyers states servidos:** C4 → C5 → C6
- **Buyer journey:** Defensa → Verificación → Decisión
- **Trigger primario:** TRG-004 (Auditoría interna), TRG-008 (Fusión/M&A)
- **Objetivo:** En 60 min, Sponsor documenta comité, vetos, contingencias, gate de aprobación.

**Estructura canónica**

| Componente              | Descripción                                                           | Activo Entregable    |
| ----------------------- | --------------------------------------------------------------------- | -------------------- |
| **Entrada**             | Proposal + stakeholder list + regulatory context                      | Intake form          |
| **Preguntas P0 (5)**    | Mapeo de poder y aprobación                                           | Q-bank + org mapping |
| **Stakeholder mapping** | Veto power, influence, concerns c/u                                   | Matrix executable    |
| **Gate logic**          | IF conditions MET → approval; ELSE → conditions to close              | Decision logic       |
| **Salida**              | Decision record: Aprobado/Condicionado/Rechazado + trazabilidad       | Audit-trail doc      |
| **Éxito**               | Decisión irreversible, documentada, **sin sorpresas post-aprobación** | Liability mitigation |

**5 Preguntas Semilla**

| #   | BCQ  | Pregunta                                                      | Tipo Respuesta                                                     | Gobernanza          | Propósito              |
| --- | ---- | ------------------------------------------------------------- | ------------------------------------------------------------------ | ------------------- | ---------------------- |
| 1   | 0075 | ¿Quién tiene poder de veto y bajo qué condición?              | Checklist [CFO / CTO / Compliance / Board / Customer] + conditions | Authority matrix    | Veto mapping           |
| 2   | 0150 | ¿Qué parte del riesgo no puede transferirse por contrato?     | Open text + Risk category tagging                                  | Residual risk doc   | Liability alignment    |
| 3   | 0175 | ¿Cuál es la evidencia que convence al comité de hoy?          | Required evidence checklist + evidence inventory                   | Evidence gap        | Objections pre-emption |
| 4   | 0225 | ¿Qué información falta para tomar decisión sin incertidumbre? | Multi-select gaps + closure plan                                   | Gate condition      | Launch readiness       |
| 5   | 0275 | ¿Qué condiciones hacen reversible esta decisión?              | Structured exit plan + triggers para reversión                     | Reversibility logic | Risk mitigation        |

**Artefactos entregables (Alpha)**

1. **DecisionGov_Stakeholder_Matrix.md** — Authority + concerns + conditions
2. **DecisionGov_Question_Bank.json** — 5Q + governance rules
3. **DecisionGov_Gate_Logic.yaml** — IF-THEN approval logic, executable
4. **DecisionGov_Decision_Record_Template.md** — Formal decision document
5. **DecisionGov_Audit_Trail_Schema.md** — Trazabilidad para compliance

**Métrica de éxito (Alpha)**
- ✅ 2 decisiones formalizadas con comité participante
- ✅ Zero post-decision objections based on missed concerns
- ✅ Internal audit acepta decision record como compliant
- ✅ Reversion criteria explícita en registro

---

## Matriz de Cobertura Alpha vs. Top 100

| Activo Alpha            | BCQ Semillas                             | % del Top 100 cubierto | ICPs servidos  | Buyer States | Deal stage      |
| ----------------------- | ---------------------------------------- | ---------------------- | -------------- | ------------ | --------------- |
| RiskDiag (KPR-01)       | 0001, 0010, 0015, 0020, 0035, 0050, 0095 | ~35% (7/20 P0)         | H01, H03, H04  | C0→C1→C2     | Early diagnosis |
| FinJustify (KPR-02)     | 0050, 0120, 0130, 0145, 0175, 0210       | ~30% (6/20 P0)         | H02, H04       | C2→C3→C4     | Business case   |
| DecisionGov (KPR-03)    | 0075, 0150, 0175, 0225, 0275             | ~25% (5/20 P0)         | H02, H04, H06  | C4→C5→C6     | Approval gate   |
| **Cobertura combinada** | **18 semillas (overlap 1Q)**             | **~80% P0 explorado**  | **All 6 ICPs** | **C0→C7**    | **Full cycle**  |

---

## Patrón de Replicación para V2+

Cada Knowledge Product sigue estructura idéntica:

```
KPR-N (Nombre)
├── Metadata (ID, ICPs, states, triggers)
├── 5–7 semillas de Top 100 → Decision Tree
├── 3–5 artefactos entregables (MD, JSON, calculadores, templates)
├── Métrica de éxito (cuantificable, observable)
└── Cadena de replicación para próximo producto
```

**Knowledge Products backlog (KPR-04..12 pending):**
- KPR-04: Vendor Selection & Terms
- KPR-05: Compliance & Audit Mapping
- KPR-06: Change Management & Training
- KPR-07: Performance Monitoring & Course Correction
- KPR-08: Competitive Positioning
- KPR-09: Cost Optimization & Efficiency
- KPR-10: Scalability & Future Roadmap
- KPR-11: Crisis Response & Contingency
- KPR-12: Post-Implementation Learning

---

## Roadmap Knowledge Product V1 → V2 → V3

```
2026-07 (NOW)
  Knowledge_Product_Alpha ← (3 activos, 18 semillas)
    ├─ Execute Alpha sprint: RiskDiag + FinJustify + DecisionGov
    ├─ Deploy internally (5 use cases c/u)
    └─ Measure success: time saving, decision quality, adoption

2026-08 (Q3)
  Knowledge_Product_V1 ← (6-8 activos, 40-50 semillas)
    ├─ Replicate successful pattern from Alpha
    ├─ Add: Vendor selection, Compliance, Change Mgmt
    └─ Extend to 70% of top 100

2026-09 (Q3)
  Knowledge_Product_V2 ← (12 activos, 100 semillas)
    ├─ Full portfolio across all domains
    ├─ Integrate with Market Behavior Map V2
    └─ Productize for external partners
```

---

## Cierre Formal

**Status:** 🟢 **ALPHA CANDIDATES LOCKED**

**Próximo sprint:** Knowledge Product Alpha Execution
- **Duración:** 3 weeks (18–22 julio 2026)
- **Deliverables:** RiskDiag + FinJustify + DecisionGov operables
- **Success criteria:** 5 use cases completadas c/u, 0 critical issues

**No hacer durante Alpha sprint:**
- ❌ Agregar BCQ preguntas nuevas (universo congelado en 300)
- ❌ Cambiar top 100 ranking (lock hasta meter datos reales)
- ❌ Modificar Market_Behavior_Map (read-only)

**Referencia cruzada:**
- DOC-048 (Buyer Curiosity Engine V1)
- BCE_V1_TOP100.md (Priorización P0..P2)
- BCE_V1_AUDIT_REPORT.md (Auditoría de cierre)
- 05_PRODUCTO/Knowledge_Product_Portfolio.md (Backlog KPR-01..12)

---

**Approved by:** BCE V1 Audit Gate  
**Date:** 2026-07-15  
**Status:** Ready for Knowledge Product Alpha Sprint Execution
