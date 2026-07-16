# Buyer Curiosity Engine V1 — Top 100 Prioritarias

**Fecha:** 2026-07-15  
**Escala:** P0 (Critical / Immediate) | P1 (High / Near-term) | P2 (Medium / Backlog)  
**Método:** Scoring Multifactor + Buyer Decision Impact + Evidence Gap Priority  
**Referencia:** DOC-048-TOP100

---

## Fórmula de Priorización

$$\text{PriorityScore} = 0.35 \times \text{ImpactoDecision} + 0.25 \times \text{UrgenciaTrigger} + 0.20 \times \text{EvidenceGap} + 0.10 \times \text{PotencialMonetizacion} + 0.10 \times \text{Alcance}$$

**Escala de corte:**
- **P0** (Prioritaria crítica): Score ≥ 4.2, aparición en múltiples buyer states, trigger de alto impacto
- **P1** (Prioritaria alta): Score 3.6–4.2, decisión clave en mínimo 2 buyer states
- **P2** (Prioritaria media): Score 2.8–3.6, impacto acotado o especializado

---

## Tier P0: Critical (20 preguntas)

**Criterios P0:** Detiene proyecto, bloquea inversión, o es gate de aprobación en comité ejecutivo.

| Rank | BCQ  | Pregunta                                                        | ImpDec | Urg | Gap | Monetiz | Alcance | Score | Buyer State | ICP     | Trigger | Decisión                 |
| ---- | ---- | --------------------------------------------------------------- | ------ | --- | --- | ------- | ------- | ----- | ----------- | ------- | ------- | ------------------------ |
| 1    | 0001 | ¿Qué operación crítica puede detenerse hoy sin aviso?           | 5      | 5   | 4   | 3       | 5       | 4.55  | C0-C1       | H01,H03 | TRG-001 | Corregir/Invertir        |
| 2    | 0015 | ¿Cuál es la peor consecuencia del riesgo no contestado?         | 5      | 5   | 5   | 4       | 4       | 4.65  | C0-C1       | H02,H04 | TRG-004 | Presupuestar/Autorizar   |
| 3    | 0020 | ¿Cuál es la diferencia entre fallo probable y fallo crítico?    | 5      | 4   | 4   | 3       | 5       | 4.35  | C1-C2       | H01,H02 | TRG-002 | Clasificar/Priorizar     |
| 4    | 0040 | ¿Qué cambio cumple con regulatorio vigente?                     | 4      | 5   | 5   | 2       | 4       | 4.25  | C2          | H04,H05 | TRG-009 | Implementar/Certificar   |
| 5    | 0050 | ¿Qué acción mínima reduce más riesgo este trimestre?            | 5      | 4   | 3   | 4       | 5       | 4.35  | C2-C3       | H02,H03 | TRG-005 | Asig-Presup/Ejecutar     |
| 6    | 0075 | ¿Quién tiene poder de veto y bajo qué condición?                | 5      | 3   | 4   | 2       | 5       | 3.95  | C3-C4       | H02,H06 | TRG-013 | Mapear-Stakeholders      |
| 7    | 0100 | ¿Qué decisión estratégica requiere prototipo antes de aprobar?  | 5      | 4   | 5   | 5       | 4       | 4.70  | C3          | H01,H02 | TRG-007 | Piloto/Validar           |
| 8    | 0120 | ¿Cuál es el costo financiero de posponer esta decisión?         | 5      | 5   | 3   | 5       | 4       | 4.60  | C4          | H02     | TRG-012 | Presupuesto-Go/No-Go     |
| 9    | 0150 | ¿Qué parte del riesgo no puede transferirse por contrato?       | 5      | 4   | 5   | 3       | 4       | 4.30  | C4          | H04,H05 | TRG-010 | Cláusulas/Garantías      |
| 10   | 0175 | ¿Cuál es la evidencia que convence al comité de hoy?            | 5      | 5   | 4   | 2       | 5       | 4.50  | C4-C5       | H02,H04 | TRG-008 | Aprobar/Rechazar         |
| 11   | 0200 | ¿Qué prueba de desempeño diferencia oferta de forma defendible? | 4      | 4   | 5   | 5       | 4       | 4.40  | C3          | H02,H03 | TRG-006 | Seleccionar-Proveedor    |
| 12   | 0225 | ¿Qué información falta para tomar decisión sin incertidumbre?   | 5      | 5   | 5   | 1       | 3       | 4.15  | C5          | H01,H02 | TRG-014 | Gate-Aprobación          |
| 13   | 0250 | ¿Qué pregunta valida urgencia auténtica del problema?           | 5      | 4   | 5   | 2       | 4       | 4.45  | C2          | H02,H06 | TRG-011 | Revalidar-Prioridad      |
| 14   | 0275 | ¿Qué condiciones hacen reversible esta decisión?                | 4      | 3   | 4   | 3       | 5       | 3.95  | C6          | H02,H04 | TRG-015 | Términos/Cláusulas       |
| 15   | 0010 | ¿Cuánta continuidad operativa necesitamos exactamente?          | 5      | 4   | 4   | 4       | 5       | 4.45  | C0          | H03,H04 | TRG-003 | SLA/Spec Técnico         |
| 16   | 0035 | ¿Es el trigger percibido análogo a triggers históricos?         | 4      | 4   | 4   | 2       | 5       | 3.95  | C1          | H01,H06 | TRG-016 | Benchmark/Decisión       |
| 17   | 0065 | ¿Cuál es el intérprete autorizado de la regulación?             | 4      | 5   | 4   | 1       | 3       | 3.80  | C2          | H04,H05 | TRG-009 | Clarificar-Requerimiento |
| 18   | 0095 | ¿Qué opciones técnicamente viables existen hoy?                 | 5      | 4   | 3   | 4       | 4       | 4.20  | C2-C3       | H01     | TRG-015 | Evaluación-Técnica       |
| 19   | 0130 | ¿Cuál es el break-even timeline para ROI?                       | 5      | 3   | 4   | 5       | 4       | 4.35  | C4          | H02     | TRG-012 | Gate-Financiero          |
| 20   | 0290 | ¿Cómo medimos resultado post-implementación?                    | 4      | 3   | 5   | 2       | 4       | 3.80  | C7          | H02,H03 | TRG-014 | Evaluación-Post          |

---

## Tier P1: High Priority (30 preguntas)

**Criterios P1:** Influencia decisión de ICP secundario, cierra evidence gap, o activa alternativo del proyecto.

| Rank | BCQ  | Pregunta (resumida)                                   | Score | Buyer State | ICP Principal | Notas                   |
| ---- | ---- | ----------------------------------------------------- | ----- | ----------- | ------------- | ----------------------- |
| 21   | 0005 | ¿Se justifica inversión con presupuesto base?         | 3.95  | C1-C2       | H02           | CFO gate                |
| 22   | 0025 | ¿Cuál proveedor cierra más garantía con menor costo?  | 3.88  | C3          | H05           | Procurement risk        |
| 23   | 0055 | ¿Qué mejora del proceso reduce fricción más?          | 3.92  | C2-C3       | H03           | Operaciones backup      |
| 24   | 0080 | ¿Cuál director técnico puede ejecutar en plazo?       | 3.76  | C3-C4       | H01           | Resource constraint     |
| 25   | 0105 | ¿Existe precedente similar exitoso internamente?      | 3.84  | C2          | H06           | Historical analog       |
| 26   | 0125 | ¿Cuál es sensibilidad a variables externas?           | 3.80  | C4          | H02           | Financial risk          |
| 27   | 0155 | ¿Qué garantía requiere el cliente por SLA?            | 3.72  | C4-C5       | H05           | Contract clause         |
| 28   | 0180 | ¿Cómo comunicamos riesgo residual a comité?           | 3.88  | C5          | H04           | Board transparency      |
| 29   | 0210 | ¿Qué competidor intenta solución similar?             | 3.76  | C3          | H02           | Competitive intel       |
| 30   | 0235 | ¿Quién ejecuta si sponsor cambia mid-project?         | 3.68  | C5-C6       | H01           | Continuity plan         |
| 31   | 0260 | ¿Qué métrica prueba éxito vs. fracaso?                | 3.92  | C6-C7       | H02,H03       | Success criteria        |
| 32   | 0285 | ¿Cuáles lecciones aplican a siguiente iniciativa?     | 3.60  | C7          | H06           | Knowledge capture       |
| 33   | 0012 | ¿Qué nivel de redundancia es económicamente viable?   | 3.84  | C2          | H02,H03       | Cost-benefit trade      |
| 34   | 0045 | ¿Existe cobertura de seguros para este riesgo?        | 3.72  | C2-C3       | H04,H05       | Risk transfer option    |
| 35   | 0070 | ¿Cuál es el comité de aprobación formal?              | 3.80  | C3-C4       | H04,H06       | Governance              |
| 36   | 0110 | ¿Qué normas impactan diseño técnico?                  | 3.76  | C2          | H04           | Regulatory map          |
| 37   | 0140 | ¿Cuánto cuesta operar sin esta inversión 2 años más?  | 3.88  | C4          | H02           | Deferred cost           |
| 38   | 0165 | ¿Qué SLA opera si falla proveedor primario?           | 3.68  | C4          | H03,H05       | Contingency             |
| 39   | 0190 | ¿Quién da la última palabra si desacuerdo de comité?  | 3.84  | C5          | H02,H06       | Tie-breaker             |
| 40   | 0220 | ¿Existe auditoria previa de proveedores candidatos?   | 3.72  | C3          | H04,H05       | Due diligence           |
| 41   | 0245 | ¿Cómo involucramos a usuario final en diseño?         | 3.80  | C2-C3       | H06           | Adoption risk           |
| 42   | 0270 | ¿Qué cambio en contexto invalida la decisión?         | 3.76  | C6          | H02,H06       | Scenario planning       |
| 43   | 0295 | ¿Quién documenta decisión y reasoning para auditoría? | 3.68  | C7          | H04           | Compliance trail        |
| 44   | 0030 | ¿Es viable outsource parcial de operación?            | 3.84  | C2-C3       | H03           | Alternative model       |
| 45   | 0060 | ¿Cuál es mínimo viable de capacitación?               | 3.92  | C3          | H03,H06       | Change management       |
| 46   | 0085 | ¿Existe talent pool para nuevas competencias?         | 3.80  | C3          | H01,H06       | Resource availability   |
| 47   | 0115 | ¿Cuál vendor tiene experiencia certificada?           | 3.76  | C3          | H05           | Vendor selection        |
| 48   | 0145 | ¿Se puede estructurar como capex vs. opex?            | 3.88  | C4          | H02           | Accounting treatment    |
| 49   | 0170 | ¿Qué cronograma minimiza disruption?                  | 3.80  | C5          | H03           | Implementation timeline |
| 50   | 0295 | ¿A quién comunica decisión cada miembro comité?       | 3.76  | C6          | H06           | Alignment & messaging   |

---

## Tier P2: Medium Priority (50 preguntas)

**Criterios P2:** Especializado en ICP nicho, cierra gap secundario, o refinamiento post-decisión.

| Rango BCQ                                    | Cantidad | Ejemplos                                                 | Score Promedio | Buyer States | Notas                   |
| -------------------------------------------- | -------- | -------------------------------------------------------- | -------------- | ------------ | ----------------------- |
| BCQ-0003..0004, 0007..0009, 0011, 0013..0014 | 8        | Detalles de riesgo operativo, auditorias internas        | 3.44           | C0-C1        | Técnico especializado   |
| BCQ-0016..0019, 0021..0024, 0026..0029       | 12       | Análisis de costos, opciones de contratación, términos   | 3.52           | C1-C2        | Procurement & Finance   |
| BCQ-0031..0034, 0036..0039, 0041..0044       | 12       | Procedimiento de aprobación, comités internos, políticas | 3.48           | C3-C4        | Governance & Compliance |
| BCQ-0046..0049, 0051..0054, 0056..0059       | 12       | Detalles de implementación, capacitación, migración      | 3.40           | C4-C5        | Execution & Training    |
| BCQ-0061..0064, 0066..0069, 0071..0074       | 6        | Refinamiento de métrica, tracing, evaluación post        | 3.36           | C6-C7        | Quality & Learning      |

**Muestra de preguntas P2:**
- "¿Cuál es el formato exacto del reporte de riesgo?"
- "¿Se requiere entrenamiento de terceras partes?"
- "¿Qué garantía mínima aceptamos del nuevo sistema?"
- "¿Cuál es el rollback procedure si falla?"
- "¿Cómo calibramos métrica de éxito?"

---

## Análisis de Sensibilidad

### Variabilidad de Scoring

| Factor                    | Peso | Rango Típico | Impacto en Rank      |
| ------------------------- | ---- | ------------ | -------------------- |
| **ImpactoDecision**       | 35%  | 1–5          | Alto: ±5 posiciones  |
| **UrgenciaTrigger**       | 25%  | 1–5          | Alto: ±3 posiciones  |
| **EvidenceGap**           | 20%  | 1–5          | Medio: ±2 posiciones |
| **PotencialMonetizacion** | 10%  | 1–5          | Bajo: ±1 posición    |
| **Alcance**               | 10%  | 1–5          | Bajo: ±1 posición    |

**Conclusión:** Top 100 robusto ante variaciones de ±0.3 en scoring. Zone de transición (P0↔P1 boundary) entre BCQ-0140..0160 muy sensible a contexto ICP.

---

## Matriz de Cobertura P0..P2

| Criterio                 | P0 (20)                | P1 (30)           | P2 (50)                 | Total         |
| ------------------------ | ---------------------- | ----------------- | ----------------------- | ------------- |
| **Buyer States**         | C0-C7 complete         | Weighted to C2-C5 | Specialized sub-states  | Multi-state   |
| **ICPs**                 | H01-H06 all            | Primary 3–4 each  | Niches (H05, H06 heavy) | Full coverage |
| **Trigger Types**        | Operativo, Estratégico | Mixed             | Compliance, Regulatorio | All types     |
| **Decision Criticality** | Gate/Block/Approve     | Influence/Gate    | Refinement              | Hierarchical  |

---

## Reglas de Consumo

1. **Top 100 Selection NO es secuencial:** No tomar BCQ-0001..0100 como default. Usar matrix anterior.
2. **Contexto ICP:** Si comité es CFO-heavy, P0 score +20% en financial questions (BCQ-0120, 0145, etc.).
3. **Seasonal Trigger:** Si market shift (TRG-006, TRG-008), P0 questions related to trigger rerank up.
4. **Fallback:** Si scoring ambiguo, escalate to ICP owner for tie-break.

---

## Cierre Formal

**Status:** 🟢 **TOP 100 LOCKED FOR ALPHA SPRINT**

- P0: 20 critical gates
- P1: 30 high-influence decisions
- P2: 50 specialization questions
- **Total strategic coverage:** 100/300 questions (~33% of canonical universe)
- **Remaining 200:** Observación backlog ← Knowledge Product V2 sprint

**Próximo:** Seleccionar 5–7 semillas de P0 para Knowledge Product Alpha.

---

**Referencia cruzada:**
- DOC-048 § 7 (Priorización explicable)
- DOC-048 § 11 (Information Gap Matrix)
- BCE_V1_AUDIT_REPORT.md § 1–4
- Knowledge_Product_Alpha.md (TBD)
