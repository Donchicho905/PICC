# Banco de Preguntas — RiskDiag V1

## Ficha de Trazabilidad
- ID: DOC-057
- Estado: 🟡 En desarrollo
- Tipo: Gate 2 — Question Bank
- Objetivo: Proveer el set de preguntas que el facilitador aplica durante un diagnóstico de riesgo, organizado por bloque de riesgo y vinculado al universo de decisiones del comprador ya mapeado en Decision_Architecture.md, para que las respuestas puedan clasificarse de forma consistente entre casos.
- Entradas:
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md) — universo base de 14 decisiones
  - DOC-013 (03_MODELO_COMERCIAL/ICPs.md) — riesgos percibidos, criterios de compra y señales por ICP
  - DOC-017 (04_TRUST/Trust_Architecture.md) — tipos de evidencia requerida por ICP
- Salidas:
  - Banco de preguntas por bloque, con propósito y decisión vinculada
  - Regla de aplicabilidad por ICP
- Dependencias:
  - DOC-056 (10_GATE2_RISKDIAG_PILOT/01_Protocolo_Piloto.md)
- Documentos consumidos:
  - Ninguno adicional
- Documentos generados:
  - Respuestas capturadas por caso (no versionadas en este repo; viven en el resultado de cada caso, DOC-059)
- Responsable: Dirección + Comercial
- Fecha: 2026-07-16
- Criterios de aceptación:
  - Cada pregunta tiene un propósito explícito y una decisión del comprador a la que sirve
  - El banco cubre los riesgos ya documentados en ICPs.md (no inventa categorías de riesgo nuevas sin base)
  - El banco distingue preguntas obligatorias de preguntas condicionales por ICP

---

## Principio de diseño

Este banco de preguntas es sobre **el proyecto del cliente**, no sobre PICC. No se usa para generar claims públicos de PICC ni para sustituir el Sistema de Evidencia (DOC-016), que gobierna lo que PICC puede afirmar de sí misma. RiskDiag diagnostica el riesgo del proyecto del comprador; el resultado ayuda al comprador a decidir, no es un vehículo de marketing.

Cada pregunta se etiqueta con:
- **Bloque**: categoría de riesgo.
- **Decisión servida**: ID de la decisión del universo base (DOC-012), del 1 al 14.
- **Aplicabilidad**: Todos los ICP, o ICP específico (H01/H02 priorizados; el resto se marca como extensión futura).
- **Obligatoria/Condicional**: si se pregunta siempre o solo si aplica.

## Universo base de decisiones (referencia, ver DOC-012)

1. Debo actuar ahora.
2. Necesito construir, remodelar, invertir o estudiar primero.
3. Qué alcance necesito.
4. Qué presupuesto debo esperar.
5. Qué riesgos existen.
6. Vale la pena considerar a PICC.
7. PICC entiende un proyecto como el mío.
8. Tiene experiencia comparable.
9. Es técnicamente competente.
10. Es institucionalmente confiable.
11. Qué la hace diferente.
12. Puedo defender su contratación ante otros.
13. Su propuesta es comparable y económicamente defendible.
14. Qué siguiente paso debo tomar.

RiskDiag se concentra sobre todo en las decisiones 1, 2, 3, 4, 5 y 14, con apoyo indirecto a 7, 8 y 12 (el diagnóstico en sí mismo es evidencia de que "PICC entiende mi proyecto").

---

## Bloque A — Contexto y urgencia (decisiones 1, 2)

| ID | Pregunta | Decisión servida | Aplicabilidad | Tipo |
| --- | --- | --- | --- | --- |
| A-01 | ¿Qué problema o evento hace que este proyecto sea relevante ahora? | 1 | Todos | Obligatoria |
| A-02 | ¿Qué pasa si este proyecto no avanza en los próximos 3-6 meses? | 1 | Todos | Obligatoria |
| A-03 | ¿El proyecto es nuevo, una ampliación, o una corrección de algo que ya falló? | 2 | Todos | Obligatoria |
| A-04 | ¿Existe una fecha límite externa (contrato, regulación, evento, cliente)? | 1 | Todos | Obligatoria |
| A-05 | ¿Quién más dentro de tu organización necesita estar de acuerdo para avanzar? | 12 | Todos | Obligatoria |

## Bloque B — Alcance y definición técnica (decisión 3)

| ID | Pregunta | Decisión servida | Aplicabilidad | Tipo |
| --- | --- | --- | --- | --- |
| B-01 | ¿El alcance del proyecto ya está definido por escrito (planos, especificación, memoria)? | 3 | Todos | Obligatoria |
| B-02 | ¿Quién definió ese alcance y qué tan reciente es? | 3 | Todos | Obligatoria |
| B-03 | ¿Hay requisitos de continuidad operativa mientras se ejecuta (no se puede detener la operación)? | 3, 5 | ICP-H01, ICP-H02 | Condicional |
| B-04 | ¿Hay requisitos de certificación, nivel de servicio o estándar técnico específico (ej. ICREA, redundancia, HVAC de precisión)? | 3, 5, 9 | ICP-H01 | Condicional |
| B-05 | ¿El alcance depende de decisiones de otras disciplinas que aún no están cerradas (arquitectura, ingeniería, permisos)? | 3, 5 | Todos | Obligatoria |

## Bloque C — Presupuesto y viabilidad económica (decisión 4)

| ID | Pregunta | Decisión servida | Aplicabilidad | Tipo |
| --- | --- | --- | --- | --- |
| C-01 | ¿Existe un presupuesto aprobado o un rango estimado para este proyecto? | 4 | Todos | Obligatoria |
| C-02 | ¿Ese presupuesto está confirmado o es una estimación preliminar sin aprobación formal? | 4 | Todos | Obligatoria |
| C-03 | ¿Quién controla la aprobación final del gasto? | 4, 12 | Todos | Obligatoria |
| C-04 | ¿Existen otros proyectos compitiendo por el mismo presupuesto? | 1, 4 | Todos | Obligatoria |

## Bloque D — Riesgo técnico y de ejecución (decisión 5)

| ID | Pregunta | Decisión servida | Aplicabilidad | Tipo |
| --- | --- | --- | --- | --- |
| D-01 | ¿Qué riesgo técnico te preocupa más de este proyecto? | 5 | Todos | Obligatoria |
| D-02 | ¿Ha habido experiencias previas negativas con proveedores en proyectos similares? | 5, 6 | Todos | Obligatoria |
| D-03 | ¿Existe riesgo de interrupción de operación durante la ejecución? | 5 | ICP-H01, ICP-H02 | Condicional |
| D-04 | ¿Hay condiciones de sitio no verificadas (estructura existente, instalaciones ocultas, condiciones de terreno)? | 5 | Todos | Obligatoria |
| D-05 | ¿Existen dependencias de terceros (proveedores, permisos, otras obras) fuera del control del cliente? | 5 | Todos | Obligatoria |
| D-06 | ¿Qué tan crítico es el tiempo de inactividad si algo sale mal (horas, días, semanas)? | 5 | ICP-H01, ICP-H02 | Condicional |

## Bloque E — Regulatorio y permisos (decisión 5)

| ID | Pregunta | Decisión servida | Aplicabilidad | Tipo |
| --- | --- | --- | --- | --- |
| E-01 | ¿El proyecto requiere permisos, licencias o autorizaciones específicas? | 5 | Todos | Obligatoria |
| E-02 | ¿Esos permisos ya están gestionados, en trámite, o no iniciados? | 5 | Todos | Obligatoria |
| E-03 | ¿Existe algún requisito normativo sectorial aplicable (ej. seguridad industrial, protección civil, normas eléctricas)? | 5, 9 | Todos | Obligatoria |

## Bloque F — Institucional y confianza (decisiones 6, 10)

| ID | Pregunta | Decisión servida | Aplicabilidad | Tipo |
| --- | --- | --- | --- | --- |
| F-01 | ¿Qué necesitas ver o saber de un proveedor para confiar en que puede ejecutar este proyecto? | 6, 10 | Todos | Obligatoria |
| F-02 | ¿Has comparado o piensas comparar con otros proveedores? ¿Cuántos? | 6 | Todos | Obligatoria |
| F-03 | ¿Qué haría que descartaras a un proveedor de inmediato? | 6, 5 | Todos | Obligatoria |

## Bloque G — Siguiente paso (decisión 14)

| ID | Pregunta | Decisión servida | Aplicabilidad | Tipo |
| --- | --- | --- | --- | --- |
| G-01 | Si este diagnóstico te da claridad, ¿cuál sería tu siguiente paso? | 14 | Todos | Obligatoria |
| G-02 | ¿Quién más necesita ver este resultado antes de que tú puedas avanzar? | 12, 14 | Todos | Obligatoria |
| G-03 | ¿En qué plazo esperarías tomar una decisión sobre este proyecto? | 1, 14 | Todos | Obligatoria |

---

## Regla de aplicabilidad

- Las preguntas marcadas "Todos" se aplican en cualquier caso piloto, sin importar el ICP.
- Las preguntas marcadas "ICP-H01" o "ICP-H02" se aplican solo si el proyecto corresponde a ese perfil (infraestructura crítica/Data Center o industrial, según DOC-013). Si el caso piloto pertenece a otro ICP (H03-H06), esas preguntas se omiten y se documenta la omisión en el resultado — no se fuerza la pregunta a un contexto donde no aplica.
- Si el facilitador identifica un riesgo relevante que no está cubierto por este banco, lo documenta como hallazgo abierto en el resultado (DOC-059) y lo reporta para una futura versión del banco (V2), sin modificar este documento durante el piloto.

## Total de preguntas del banco V1

24 preguntas obligatorias/condicionales distribuidas en 7 bloques (A-G).
