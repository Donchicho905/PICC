# Plantilla de Resultado — RiskDiag V1

## Ficha de Trazabilidad
- ID: DOC-059
- Estado: 🟡 En desarrollo
- Tipo: Gate 2 — Result Template
- Objetivo: Definir el documento estándar que se entrega al cliente y se archiva internamente al cierre de cada caso del piloto RiskDiag, para que los 3-5 casos sean comparables y auditable.
- Entradas:
  - DOC-057 (10_GATE2_RISKDIAG_PILOT/02_Banco_de_Preguntas.md)
  - DOC-058 (10_GATE2_RISKDIAG_PILOT/03_Reglas_de_Clasificacion.md)
- Salidas:
  - Estructura fija del documento de resultado por caso
- Dependencias:
  - DOC-056 (10_GATE2_RISKDIAG_PILOT/01_Protocolo_Piloto.md) — Fase 4
- Documentos consumidos:
  - Ninguno adicional
- Documentos generados:
  - Un archivo de resultado por caso (fuera de este repo o en carpeta local de casos; no se versiona con datos de cliente sin autorización — ver sección "Manejo de datos sensibles")
- Responsable: Facilitador del caso
- Fecha: 2026-07-16
- Criterios de aceptación:
  - El resultado es legible por el cliente sin necesitar contexto adicional de PICC ni de este repositorio
  - Ningún hallazgo E0-E1 aparece como certeza (ver DOC-058 sección 5)
  - El resultado incluye siempre una recomendación de siguiente paso

---

## Nota sobre manejo de datos sensibles

Esta es una **plantilla**, no un caso real. Ningún resultado de un caso piloto real (con datos de cliente) debe subirse a este repositorio sin autorización explícita del cliente, siguiendo las mismas reglas de permiso ya definidas en DOC-016 (Sistema de Evidencia). Los resultados de casos reales viven fuera de este repositorio o en una carpeta local no versionada, salvo que el cliente autorice su uso como caso publicable — en cuyo caso pasa por el proceso de DOC-016, no por este documento.

---

## ESTRUCTURA DEL DOCUMENTO DE RESULTADO

### 1. Encabezado del caso

| Campo | Valor |
| --- | --- |
| Nombre del proyecto (o código si es sensible) | |
| Fecha del diagnóstico | |
| Facilitador | |
| ICP hipotético (referencia interna, no se muestra al cliente) | |
| Duración de la sesión | |

### 2. Resumen ejecutivo (máximo 5 líneas)

Qué se diagnosticó, cuántos riesgos se identificaron por nivel de severidad, y cuál es la recomendación principal. Debe poder leerse en menos de 1 minuto.

### 3. Mapa de riesgos identificados

| Riesgo | Bloque (DOC-057) | Severidad (DOC-058) | Confianza (DOC-058) | Decisión del comprador afectada (DOC-012) | Estado de la decisión |
| --- | --- | --- | --- | --- | --- |
| | | | | | |

Reglas de llenado:
- Ordenar de mayor a menor severidad.
- Redactar cada riesgo siguiendo la regla de confianza de DOC-058 sección 5 ("el cliente reporta que...", "se confirmó que...").
- No incluir hallazgos S0 salvo que el cliente los haya señalado como preocupación explícita.

### 4. Brechas de información identificadas

| Brecha | Tipo (DOC-058) | Qué se necesita para cerrarla | Quién la puede cerrar |
| --- | --- | --- | --- |
| | | | |

### 5. Recomendaciones priorizadas

Lista corta (máximo 5) de acciones recomendadas, ordenadas por impacto en reducir el riesgo más severo. Cada recomendación debe ser accionable por el cliente, no solo "hay que investigar más".

### 6. Siguiente paso propuesto

- Siguiente paso concreto (ej. reunión técnica, cotización preliminar, definición de alcance).
- Owner del siguiente paso (PICC o cliente).
- Plazo sugerido.

### 7. Límites del diagnóstico

Texto fijo obligatorio en todo resultado:

> "Este diagnóstico se basa en la información compartida durante la sesión del [fecha]. No sustituye una auditoría técnica, legal o financiera formal. Los hallazgos marcados como 'no verificados' requieren confirmación antes de tomarse como base de decisión final."

### 8. Firma / responsable

| Campo | Valor |
| --- | --- |
| Elaborado por | |
| Revisado por (si aplica) | |
| Fecha de entrega al cliente | |

---

## Checklist de calidad antes de entregar

- [ ] Todo hallazgo tiene severidad y confianza asignada.
- [ ] Ningún hallazgo E0-E1 se redactó como certeza.
- [ ] Cada hallazgo está vinculado a una decisión del universo base.
- [ ] El resumen ejecutivo puede leerse en menos de 1 minuto.
- [ ] Existe al menos un siguiente paso concreto con owner.
- [ ] El texto de límites del diagnóstico (sección 7) está presente sin modificar.
