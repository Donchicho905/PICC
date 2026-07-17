# Reglas de Clasificación — RiskDiag V1

## Ficha de Trazabilidad
- ID: DOC-058
- Estado: 🟡 En desarrollo
- Tipo: Gate 2 — Classification Rules
- Objetivo: Definir cómo el facilitador clasifica las respuestas capturadas con el Banco de Preguntas (DOC-057) en severidad de riesgo, nivel de confianza de la información y tipo de brecha, de forma consistente entre los 3-5 casos del piloto.
- Entradas:
  - DOC-057 (10_GATE2_RISKDIAG_PILOT/02_Banco_de_Preguntas.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md) — niveles de evidencia E0-E5
  - DOC-016 (04_TRUST/Sistema_de_Evidencia.md) — tipos de brecha (dato, permiso, evidencia real, no verificado)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md) — reglas de "decisión soportada / parcialmente soportada / no soportada / no evaluable"
- Salidas:
  - Escala de severidad de riesgo
  - Escala de confianza de la respuesta
  - Regla de vinculación hallazgo → decisión del comprador
- Dependencias:
  - DOC-059 (10_GATE2_RISKDIAG_PILOT/04_Plantilla_de_Resultado.md) — consume esta clasificación
- Documentos consumidos:
  - Ninguno adicional
- Documentos generados:
  - Hallazgos clasificados por caso (viven en DOC-059 de cada caso)
- Responsable: Dirección
- Fecha: 2026-07-16
- Criterios de aceptación:
  - Toda respuesta capturada recibe severidad, confianza y tipo de brecha
  - Ningún hallazgo se presenta como certeza si la confianza es baja
  - La escala reutiliza, sin redefinir, los niveles de evidencia E0-E5 ya aprobados en Trust_Architecture.md

---

## 1. Principio rector

RiskDiag no inventa una taxonomía de evidencia nueva. Reutiliza los niveles E0-E5 ya aprobados en Trust_Architecture.md, aplicados aquí al **riesgo del proyecto del cliente** en lugar de a los claims públicos de PICC. Esto evita duplicar gobierno de evidencia y mantiene una sola fuente de verdad por dominio (regla de REPOSITORY_RULES.md, principio 6).

## 2. Escala de severidad de riesgo

| Severidad | Nombre | Criterio |
| --- | --- | --- |
| S0 | Sin riesgo identificado | La respuesta no revela ningún riesgo relevante para la decisión que sirve |
| S1 | Riesgo bajo | El riesgo existe pero es manejable con práctica estándar; no bloquea ninguna decisión del universo base |
| S2 | Riesgo medio | El riesgo puede generar sobrecosto, retraso o fricción, pero no detiene el proyecto |
| S3 | Riesgo alto | El riesgo puede detener, encarecer significativamente o comprometer la viabilidad del proyecto si no se gestiona |
| S4 | Riesgo crítico | El riesgo, si se materializa, implica pérdida grave (seguridad, continuidad operativa, incumplimiento regulatorio, pérdida patrimonial) |

## 3. Escala de confianza de la respuesta (adaptada de E0-E5)

| Nivel | Nombre (heredado de DOC-017) | Aplicación en RiskDiag |
| --- | --- | --- |
| E0 | No evidencia | Respuesta es opinión o supuesto del cliente sin documento ni verificación posible en la sesión |
| E1 | Señal aislada | El cliente menciona un dato puntual no verificado (ej. "creo que el presupuesto es de X") |
| E2 | Evidencia parcial trazable | El cliente cita una fuente identificable (documento, cotización, correo) pero no se revisó en la sesión |
| E3 | Evidencia operativa | El cliente muestra o cita el documento/dato directamente durante la sesión |
| E4 | Evidencia publicable | El dato está documentado, verificado, y el cliente autoriza su uso en el resultado escrito |
| E5 | Evidencia sistémica | No aplica en un solo caso piloto; se reserva para cuando exista un patrón repetido entre varios casos |

Regla dura: ningún hallazgo con confianza E0 o E1 puede presentarse en la Plantilla de Resultado (DOC-059) como una conclusión firme. Debe presentarse explícitamente como "riesgo declarado, no verificado" (ver Sección 5).

## 4. Tipo de brecha (heredado de DOC-016, aplicado al proyecto del cliente)

| Tipo de brecha | Descripción | Acción recomendada en el resultado |
| --- | --- | --- |
| Ausencia de dato | El cliente no tiene la información porque no se ha generado | Recomendar generarla antes de avanzar a propuesta |
| Ausencia de verificación | La información existe pero no se verificó en la sesión | Marcar como pendiente de verificación, no como hecho |
| Ausencia de definición | El proyecto aún no tiene ese elemento definido (alcance, presupuesto, permiso) | Recomendar como siguiente paso explícito |
| Información no compartida | El cliente prefiere no compartir el dato en esta etapa | Respetar; no forzar; documentar como "no disponible por decisión del cliente" |

## 5. Regla de redacción según confianza

| Confianza | Cómo se redacta en el resultado |
| --- | --- |
| E0-E1 | "El cliente reporta que... (no verificado en esta sesión)" |
| E2 | "Según [fuente citada por el cliente]... (no revisado directamente)" |
| E3-E4 | "Se confirmó que..." |

Esta regla replica el principio de DOC-016 ("si la evidencia es parcial, debe decirse") aplicado al diagnóstico del cliente en vez de a los claims de PICC.

## 6. Vinculación hallazgo → decisión del comprador

Cada hallazgo debe vincularse a al menos una decisión del universo base de DOC-012 (numeradas 1-14). Un hallazgo sin decisión vinculada no se incluye en el resultado — evita ruido sin propósito (principio de REPOSITORY_RULES.md: "todo artefacto debe tener un único propósito").

Para cada hallazgo relevante, se clasifica el estado de la decisión que afecta usando la misma regla ya definida en Decision_Architecture.md:

- **Soportada**: el cliente tiene información suficiente y verificada para decidir.
- **Parcialmente soportada**: existe información pero incompleta, no verificada o insuficiente.
- **No soportada**: la información existe pero contradice o complica la decisión.
- **No evaluable**: no hay información suficiente ni siquiera para diagnosticar.

## 7. Priorización de hallazgos para el resultado final

Orden de prioridad para incluir un hallazgo en la Plantilla de Resultado:
1. Severidad S3-S4 con cualquier nivel de confianza.
2. Severidad S2 con confianza E2 o mayor.
3. Hallazgos que bloquean una decisión marcada "No evaluable".
4. Hallazgos S0-S1 se mencionan solo si el cliente los señaló como preocupación explícita.

## 8. Qué esta regla NO hace

- No asigna un "score" numérico automático ni pondera factores algorítmicamente — la clasificación es manual y cualitativa en V1.
- No sustituye el juicio del facilitador; es una guía de consistencia, no un árbol de decisión mecánico.
- No genera ningún claim público de PICC ni alimenta el Claim Register de DOC-016.
