# Plantilla de Veredicto ZEUS — Cierre del Piloto RiskDiag V1

## Ficha de Trazabilidad
- ID: DOC-062
- Estado: 🟡 En desarrollo
- Tipo: Gate 2 — Verdict Template
- Objetivo: Definir el formato y las reglas de decisión que ZEUS (o quien Pablo designe con esa autoridad) usa al cierre de los 3-5 casos del piloto RiskDiag para emitir un veredicto de GO, GO CONDICIONADO, PIVOT o NO GO, con base en los criterios de aceptación ya autorizados en 00_IMPLEMENTATION_REPORT.md.
- Entradas:
  - 00_IMPLEMENTATION_REPORT.md — sección "Active Program", punto 4 (criterios de aceptación autorizados)
  - DOC-060 (10_GATE2_RISKDIAG_PILOT/05_Hoja_de_Medicion.md) — consolidado de métricas
  - DOC-061 (10_GATE2_RISKDIAG_PILOT/06_Sheet_de_Defectos.md) — consolidado de defectos
  - DOC-055 (99_META/ZEUS_OLYMPUS_INTEGRATION_ASSESSMENT_V1.md) — criterio de reversión de la decisión diferida (sección 17)
- Salidas:
  - Veredicto formal del piloto (GO / GO CONDICIONADO / PIVOT / NO GO)
  - Próximo paso autorizado según el veredicto
- Dependencias:
  - Todos los documentos de 10_GATE2_RISKDIAG_PILOT/
- Documentos consumidos:
  - Resultados de los 3-5 casos (DOC-059 por caso)
- Documentos generados:
  - Un veredicto único al cierre del piloto, a registrar en 99_META/DECISION_HISTORY.md cuando el piloto se ejecute
- Responsable: ZEUS (autoridad evaluadora, ver DOC-055) o quien Pablo designe explícitamente
- Fecha: 2026-07-16
- Criterios de aceptación:
  - El veredicto usa exclusivamente los criterios ya autorizados, sin agregar criterios nuevos no documentados
  - El veredicto distingue explícitamente entre falla de ejecución y falla de método
  - El veredicto no autoriza, por sí mismo, ninguna integración con OLYMPUS/ZEUS/DAVINCI/BrickEye (eso permanece bloqueado hasta Gate 3, ver DOC-055 sección 19)

---

## 1. Cuándo se aplica este documento

Solo al cierre de un piloto real de 3-5 casos ejecutados siguiendo el Protocolo (DOC-056). No aplica a evaluaciones parciales con menos de 3 casos completos y válidos (ver DOC-061, columna "Caso válido para veredicto").

## 2. Insumos requeridos antes de emitir veredicto

Checklist previo:
- [ ] Al menos 3 casos con resultado entregado (DOC-059) y clasificado.
- [ ] Hoja de Medición (DOC-060) consolidada para todos los casos.
- [ ] Sheet de Defectos (DOC-061) consolidado, incluyendo la columna "caso válido".
- [ ] Métrica 11 (señal comercial downstream) cerrada o explícitamente marcada "pendiente" con fecha de cierre estimada.

Si falta cualquiera de estos insumos, el veredicto no puede emitirse — se documenta como "veredicto diferido por insumo incompleto", no se fuerza una conclusión.

## 3. Criterios de aceptación (heredados literalmente de 00_IMPLEMENTATION_REPORT.md)

| Criterio autorizado | Cómo se evalúa con las métricas de DOC-060 |
| --- | --- |
| Uso en casos reales | Número de casos válidos ≥ 3 (ver DOC-061) |
| Salida comprensible | Claridad percibida (métrica 3) promedio ≥ 4/5 |
| Efecto en decisión | Decisión afectada (métrica 10) = Sí en al menos 2 de 3 casos |
| Reducción de tiempo/confusión/retrabajo | Utilidad percibida (métrica 4) promedio ≥ 4/5 Y Reducción de retrabajo (métrica 7) = Sí en al menos 1 caso |
| Resultado compartible | Intención de compartir (métrica 8) = Sí en al menos 1 caso |
| Disciplina de evidencia | Completitud (métrica 2) promedio ≥ 70% Y ningún hallazgo E0-E1 presentado como certeza (auditar DOC-059 de cada caso contra DOC-058 sección 5) |
| Intención de reutilización | Intención de avanzar (métrica 9) = Sí o Tal vez en al menos 2 de 3 casos |
| Señal de decisión/comercial downstream | Señal comercial downstream (métrica 11) = Sí en al menos 1 caso, o explícitamente pendiente con seguimiento activo |
| Defectos registrados | Sheet de Defectos (DOC-061) completo para todos los casos, sin defectos Críticos sin resolver ni documentar |

## 4. Regla de veredicto

### GO
Se cumplen **todos** los criterios de la tabla de la Sección 3, y no hay defectos Críticos abiertos.

**Significado:** RiskDiag V1 demuestra valor real con compradores reales. Puede proponerse como Knowledge Product formal (ver DOC-048-ALPHA, Knowledge Product Alpha) y considerarse evidencia hacia el Gate 3 de DOC-055 (Evidence of measurable value). No implica, por sí mismo, ninguna integración con OLYMPUS.

**Próximo paso autorizado:** Documentar el resultado en `99_META/DECISION_HISTORY.md` como nueva decisión D-00XX y proponer a Pablo la formalización de RiskDiag como producto operativo (fuera del alcance de este Gate 2 documental — requiere nueva autorización).

### GO CONDICIONADO
Se cumplen la mayoría de los criterios (al menos 6 de 9), pero uno o más criterios quedan en zona gris, o hay defectos Altos sin resolver que afectan confianza pero no invalidan el piloto.

**Significado:** El método tiene señal positiva pero necesita ajuste antes de escalar.

**Próximo paso autorizado:** Documentar qué criterios fallaron y por qué. Proponer una V2 acotada del Banco de Preguntas o las Reglas de Clasificación (según lo que indiquen los defectos de DOC-061) antes de correr casos adicionales.

### PIVOT
Menos de 6 de 9 criterios se cumplen, pero al menos 1 caso mostró señal clara de valor (ej. decisión afectada = Sí, o señal comercial = Sí), sugiriendo que el problema no es el concepto sino la ejecución del método actual.

**Significado:** El diagnóstico de riesgo como categoría tiene mérito, pero el diseño actual del banco de preguntas, las reglas de clasificación o el formato de resultado no está funcionando como está.

**Próximo paso autorizado:** Rediseñar el banco de preguntas o el formato de resultado (no el concepto) y correr un nuevo ciclo de 3 casos antes de reintentar el veredicto.

### NO GO
Menos de 4 de 9 criterios se cumplen, o hay defectos Críticos que invalidan más de 1 caso, o ningún caso mostró señal de decisión o comercial.

**Significado:** No hay evidencia de que el diagnóstico estructurado de riesgo, en esta forma, mejore la decisión del comprador frente al método actual de PICC.

**Próximo paso autorizado:** Cerrar el experimento RiskDiag V1. Documentar el aprendizaje en `99_META/DECISION_HISTORY.md`. No se reintenta sin evidencia nueva (mismo principio de reversión que D-0020 en DOC-055).

## 5. Formato del veredicto final

```
VEREDICTO DEL PILOTO RISKDIAG V1

Fecha de cierre: __________
Casos válidos evaluados: __ / __
Veredicto: [ GO | GO CONDICIONADO | PIVOT | NO GO ]

Resumen de criterios cumplidos: __ / 9

Tabla de criterios (Sección 3) con resultado real:
[pegar tabla llena]

Hallazgos cualitativos relevantes:
- ...

Defectos Críticos o Altos sin resolver:
- ...

Recomendación explícita:
- ...

Próximo paso autorizado (según Sección 4):
- ...

Restricciones que se mantienen vigentes:
- Ninguna integración con OLYMPUS/ZEUS/DAVINCI/BrickEye queda autorizada por este veredicto (DOC-055 sección 19).
- Cualquier escalamiento a producto formal requiere nueva autorización explícita de Pablo.

Firma / autoridad evaluadora: __________
```

## 6. Advertencia final

Este veredicto es una decisión sobre el **método RiskDiag**, no sobre integración de PICC NEXT con el ecosistema OLYMPUS. El criterio de reversión de la Decisión Diferida (DOC-055, sección 17) requiere, entre otras condiciones, "caso real ejecutado" y "métrica de valor verificable" — un veredicto GO de este documento aporta esa evidencia, pero no reabre automáticamente la evaluación de integración. Reabrir esa evaluación requiere que ZEUS lo determine explícitamente con los 5 criterios simultáneos de DOC-055 sección 17.
