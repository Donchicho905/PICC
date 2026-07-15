# Auditoria Sitio

## Ficha de Trazabilidad
- ID: DOC-007
- Estado: 🟡 En desarrollo
- Tipo: Investigacion ejecutable
- Objetivo: Validar el motor de investigacion mediante un piloto controlado sobre la Home de PICC antes de ejecutar VC-RID-001 completo.
- Entradas:
  - RL-001 (02_VERDAD_COMERCIAL/RESEARCH_LEDGER.md)
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
  - DOC-010 (02_VERDAD_COMERCIAL/Verdad_Comercial.md)
- Salidas:
  - Metodo validado/no validado
  - Hallazgos metodologicos
  - Resultado Gate A y Gate B
- Dependencias:
  - Acceso a sitio y activos digitales de PICC
  - Acceso a analytics, CRM y Search Console
  - Entrevistas con Comercial, Operaciones y Direccion
- Documentos consumidos:
  - DOC-044 (99_META/REPOSITORY_RULES.md)
  - DOC-045 (99_META/SYSTEM_MAP.md)
  - DOC-046 (INDEX.md)
- Documentos actualizados por ejecucion:
  - DOC-010 (02_VERDAD_COMERCIAL/Verdad_Comercial.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
  - DOC-015 (04_TRUST/Biblioteca_de_Evidencia.md)
  - DOC-014 (03_MODELO_COMERCIAL/Modelo_Comercial.md)
  - DOC-028 (07_GOBIERNO/Governance.md)
- Responsable: ZEUS (CIO) + Marketing + Comercial
- Fecha: 2026-07-15
- Criterios de aceptación:
  - Flujo completo probado en piloto
  - Trazabilidad de evidencia demostrada
  - Gate A y Gate B justificados por separado


## VC-RID-001

## Sprint 0 - Validacion del motor de investigacion

### Alcance del piloto

Caso controlado: Home del sitio de PICC unicamente.

Objetivo del piloto: validar robustez metodologica, no terminar auditoria completa del sitio.

### Ejecucion del flujo completo (piloto)

1. Pregunta:
  - La Home actual representa capacidades reales y claims verificables?
2. Hipotesis:
  - H1: la Home contiene claims parcialmente verificables.
  - H2: hay claims sin respaldo trazable.
3. Obtencion de evidencia:
  - Repositorio PICC: sin URL operativa ni snapshot formal de Home en artefactos actuales.
  - Fuentes externas del sitio: no disponibles en este sprint dentro del entorno de trabajo.
4. Validacion:
  - La evidencia disponible no permite confirmar ni refutar claims de la Home con confianza media/alta.
5. Hallazgos:
  - El metodo detecta correctamente bloqueo por falta de insumo primario verificable.
  - El proceso evita conclusiones inventadas y mantiene investigacion abierta.
6. Insight:
  - Sin activo minimo de captura de Home (URL/snapshot/versionado), cualquier conclusion seria fragil.
7. Decision recomendada:
  - Gate A (metodologia): GO.
  - Gate B (readiness operativo): GO CONDICIONADO.
8. Capacidad impactada:
  - Gobierno de investigacion y venta consultiva basada en evidencia.
9. Documentos afectados:
  - DOC-006, RL-001, DOC-007, DOC-010.
10. Backlog generado:
  - Condicion R3-C1: registrar URL canonica y owner digital.
  - Condicion R3-C2: capturar snapshot versionado de Home con fecha.
  - Condicion R3-C3: habilitar acceso de lectura a analytics y Search Console.

### Matriz de hallazgos del piloto

| Hallazgo                                                               | Evidencia                                                       | Impacto                                        | Riesgo                               | Capacidad afectada                   | Prioridad | Recomendacion                                                     | Documento a actualizar | Backlog generado |
| ---------------------------------------------------------------------- | --------------------------------------------------------------- | ---------------------------------------------- | ------------------------------------ | ------------------------------------ | --------- | ----------------------------------------------------------------- | ---------------------- | ---------------- |
| No existe insumo primario verificable de la Home en artefactos activos | Busqueda en repo sin URL/snapshot operativo                     | Impide validar claims con confianza media/alta | Conclusiones no reproducibles        | Gobierno de investigacion            | P0        | Mantener Gate B en GO CONDICIONADO y cerrar condicion R3-C1/R3-C2 | DOC-007, RL-001        | R3-C1, R3-C2     |
| Falta acceso operativo a datos de desempeno digital para el piloto     | Analytics/Search Console no disponibles en evidencia del sprint | Reduce trazabilidad de decisiones comerciales  | Sesgo por interpretacion cualitativa | Venta consultiva basada en evidencia | P0        | Mantener Gate B en GO CONDICIONADO y cerrar condicion R3-C3       | DOC-007, DOC-010       | R3-C3            |

### Auditoria critica del metodo

#### Que funciono

- El flujo obliga trazabilidad y evita cierre por opinion.
- La taxonomia dato/evidencia/hallazgo/insight/decision reduce ambiguedad.
- El formato de hallazgos accionables facilita decisiones ejecutivas.

#### Que fue ambiguo

- Criterio minimo de evidencia primaria para canales web no estaba explicitado.
- Umbral cuantitativo para pasar de confianza baja a media no estaba definido para piloto digital.

#### Que sobra

- Ningun paso sobra en el flujo nuclear para investigaciones comerciales.

#### Que falta

- Requisito de readiness previo a ejecucion (pre-flight) para confirmar insumos minimos.
- Registro formal de bloqueos metodologicos por RID.

#### Informacion dificil de obtener

- Snapshot verificable de Home con version y fecha.
- Metricas reales de comportamiento digital sin acceso a herramientas.

#### Que puede automatizarse

- Inventario de claims por pagina.
- Clasificacion inicial de evidencia por completitud.
- Generacion base de matriz de hallazgos.

#### Que requiere juicio humano

- Interpretacion estrategica de impacto comercial.
- Priorizacion de decisiones bajo restricciones de negocio.
- Validacion legal/publicable de evidencia.

#### Cambios propuestos antes de ejecutar VC-RID-001 completo

- Introducir checklist de readiness de evidencia primaria por canal.
- Exigir definicion de owner de dato por cada fuente critica.
- Registrar explicitamente condicion GO/NO GO previa a ejecucion completa.

### Activos reutilizables identificados (sin crear aun)

- Catalogo de Claims: alto valor; gobierno en DOC-010 y RL-001.
- Catalogo de Evidencias: alto valor; gobierno en DOC-015 y RL-001.
- Catalogo de Brechas: valor medio-alto; gobierno en DOC-010 y DOC-028.
- Catalogo de Recomendaciones: alto valor; gobierno en DOC-028 y RL-001.
- Catalogo de Capacidades Impactadas: alto valor; gobierno en DOC-014 y DOC-028.

### Lista de mejoras detectadas (no implementadas automaticamente)

1. Problema: falta criterio de readiness de insumos.
  - Evidencia: piloto bloqueado por ausencia de fuente primaria.
  - Impacto: alto.
  - Propuesta: checklist pre-flight obligatorio por RID.
  - Riesgos: retraso inicial de cada investigacion.
  - Beneficios: mayor reproducibilidad y trazabilidad.
  - Esfuerzo: bajo.
  - Compatibilidad: alta con arquitectura actual.

2. Problema: ambiguedad en umbrales de confianza para digital.
  - Evidencia: no se pudo escalar de confianza baja.
  - Impacto: medio-alto.
  - Propuesta: definir umbrales por tipo de fuente (primaria/secundaria).
  - Riesgos: sobrecarga de criterios.
  - Beneficios: comparabilidad entre investigadores.
  - Esfuerzo: bajo.
  - Compatibilidad: alta.

3. Problema: no existe registro formal de bloqueos metodologicos por RID.
  - Evidencia: bloqueo documentado de forma ad-hoc.
  - Impacto: medio.
  - Propuesta: seccion fija de bloqueos en salida de RID.
  - Riesgos: burocracia si se sobredimensiona.
  - Beneficios: visibilidad y gestion de riesgo.
  - Esfuerzo: bajo.
  - Compatibilidad: alta.

### Gates de cierre Sprint 0

- Gate A - Validacion metodologica: GO.
  - Justificacion: flujo completo probado, taxonomia operativa util, criterios reproducibles.
- Gate B - Readiness operativo: GO CONDICIONADO.
  - Justificacion: metodo listo, pero faltan insumos para ejecucion completa.
  - Condiciones para elevar Gate B a GO:
    - R3-C1: URL canonica y owner digital registrados.
    - R3-C2: snapshot versionado de Home con fecha.
    - R3-C3: accesos de lectura a analytics y Search Console.

## Evolucion metodologica hacia Decision Readiness

### Antes

- Claim-Evidence Readiness: el foco principal era validar si un claim podia publicarse.

### Ahora

- Decision Readiness: el foco principal es validar si una superficie comercial ayuda al comprador a tomar decisiones relevantes con menor incertidumbre y mayor confianza.

Cambio clave:
- Unidad de valor pasa de claim publicable a decision de compra habilitada.

## Matriz de Decision Readiness - Home (piloto)

Supuesto de contexto del piloto:
- No hay snapshot verificable de Home ni URL canonica registrada en artefactos activos.
- La matriz se emite como diagnostico de readiness, no como veredicto de performance final del sitio.

| Claim o mensaje principal (Home)           | ICP objetivo                    | Etapa journey              | Decision que intenta facilitar              | Evidencia que lo respalda                             | Nivel de confianza | Riesgo si es cuestionado                     | Owner evidencia         | Accion recomendada |
| ------------------------------------------ | ------------------------------- | -------------------------- | ------------------------------------------- | ----------------------------------------------------- | ------------------ | -------------------------------------------- | ----------------------- | ------------------ |
| Propuesta de valor principal de PICC       | Direccion/Compras B2B           | Consideracion              | Vale la pena evaluar a PICC en shortlist?   | No verificable en artefactos del sprint               | Bajo               | Alto (perdida de oportunidad y credibilidad) | Marketing + Comercial   | Priorizar          |
| Mensaje de confianza institucional         | Direccion/Stakeholders          | Awareness -> Consideracion | Puedo confiar en esta empresa?              | Sin evidencia primaria trazable en piloto             | Bajo               | Alto (riesgo reputacional)                   | Direccion + Marketing   | Fortalecer         |
| Mensaje de experiencia/proyectos similares | Cliente tecnico/comercial       | Consideracion              | Tiene experiencia comparable a mi caso?     | Sin casos verificados vinculados en Home              | Bajo               | Alto (objecion de experiencia)               | Comercial + Operaciones | Reescribir         |
| Mensaje de reduccion de riesgo             | Comprador responsable de riesgo | Consideracion -> Decision  | Reduce realmente mi riesgo de ejecucion?    | Sin evidencia de outcomes verificables en piloto      | Bajo               | Alto (riesgo legal/comercial)                | Operaciones + Legal     | Fortalecer         |
| Mensaje de capacidad tecnica               | Area tecnica/operativa cliente  | Consideracion              | Tiene capacidad tecnica suficiente?         | Evidencia no disponible en Decision Surface analizada | Bajo               | Medio-alto                                   | Producto + Operaciones  | Reescribir         |
| Mensaje de diferenciacion competitiva      | Direccion/Compras               | Consideracion              | Que la hace diferente frente a competencia? | Sin benchmark trazable conectado a Home en piloto     | Bajo               | Medio-alto                                   | Estrategia + Comercial  | Priorizar          |

## Decision Coverage - definicion y resultado del piloto

Decisiones criticas evaluadas en Home (piloto):
1. Puedo confiar en esta empresa?
2. Tiene experiencia en proyectos similares?
3. Reduce realmente mi riesgo?
4. Tiene capacidad tecnica necesaria?
5. Vale la pena incluirla en mi shortlist?
6. Que la hace diferente de la competencia?

Formula:
- Decision Coverage (%) = (Decisiones criticas soportadas / Total de decisiones criticas evaluadas) x 100

Regla de decision soportada:
- Mensaje explicito + evidencia trazable con confianza media/alta + owner de vigencia + accion definida.

Resultado del piloto Home:
- Decisiones criticas soportadas: 0
- Total de decisiones criticas evaluadas: 6
- Decision Coverage actual: 0%

Interpretacion:
- El 0% no significa que la Home sea inutil; significa que el sistema actual no dispone aun de evidencia trazable suficiente para certificar soporte de decisiones en esta superficie.

## Modelo reutilizable para Decision Surfaces

Aplicable sin cambios a Home, casos, propuestas, PDFs, reportes, presentaciones, landing pages, herramientas y LinkedIn.

Paso 1: Identificar decisiones criticas del comprador por ICP y etapa.

Paso 2: Mapear mensajes de la Decision Surface a esas decisiones.

Paso 3: Vincular evidencia trazable por mensaje (fuente, fecha, owner, confianza).

Paso 4: Evaluar riesgo de cuestionamiento por mensaje/decision.

Paso 5: Emitir accion recomendada por mensaje:
- Mantener
- Fortalecer
- Reescribir
- Eliminar
- Priorizar

Paso 6: Calcular Decision Coverage de la superficie.

Paso 7: Traducir hallazgos a decisiones, capacidades impactadas, documentos a actualizar y backlog.

## Analisis critico de la vision: Sistema de Ingenieria Comercial

### A favor

- Describe mejor el objetivo real: convertir evidencia en decisiones comerciales superiores de forma repetible.
- Alinea marketing, comercial, operaciones y trust bajo una misma logica de valor.
- Permite medir avance por reduccion de incertidumbre y mejora de capacidades, no por volumen documental.

### En contra

- Puede percibirse como concepto amplio y generar sobre-ingenieria si no se delimita alcance.
- Riesgo de desviar foco a framework antes que resultados de negocio si no hay disciplina de priorizacion.

### Recomendacion

- Adoptarla como hipotesis rectora operativa (no como cambio arquitectonico formal inmediato).
- Validarla por resultados en 2-3 ciclos de Decision Surfaces antes de institucionalizarla como definicion oficial del proyecto.

## Recomendaciones de ajuste al Research OS (derivadas)

1. Priorizar RIDs por decision bloqueada de comprador y retorno esperado de aprendizaje.
2. Hacer obligatorio Decision Coverage en toda investigacion de superficie comercial.
3. Exigir owner de vigencia de evidencia por mensaje critico.
4. Registrar explicitamente decision habilitada y capacidad del negocio fortalecida en cada RID.
5. Evitar apertura de nuevos RIDs si no existe decision bloqueada prioritaria.

## Cierre de iteracion (sin abrir nuevos RIDs)

- No se proponen nuevos RIDs en esta iteracion.
- Se mantiene VC-RID-001 como piloto metodologico para validar Decision Readiness en Home.

### Readiness de VC-RID-001

- Nivel actual: R2 (Fuentes identificadas).
- Meta inmediata: R3 (Accesos validados).
- Criterio de entrada a ejecucion completa: R5 + Gate A GO + Gate B GO.

### Definition of Ready / Definition of Done para VC-RID-001

DoR VC-RID-001 (estado actual: parcial):
- [x] Objetivo aprobado.
- [x] Owner asignado.
- [x] Fuentes identificadas.
- [ ] Accesos disponibles.
- [x] Criterios de aceptacion definidos.
- [x] Riesgos registrados.

DoD VC-RID-001 (estado actual: no alcanzado):
- [ ] Evidencia validada.
- [ ] Hallazgos completos.
- [ ] Decisiones emitidas.
- [ ] Capacidades impactadas identificadas.
- [ ] Documentos actualizados.
- [ ] Backlog generado.



## Contenido Base
- Consolida hechos, brechas y riesgos verificables.
- Base obligatoria para modelado comercial.

