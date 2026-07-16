# Decision Experience Alpha

## Ficha de trazabilidad
- ID: DOC-051
- Estado: En desarrollo
- Tipo: Decision Experience Design
- Objetivo: Diseñar la primera experiencia comercial real de PICC que lleve a un comprador desde trigger inicial hasta solicitud de reunion con decision quality measurable.
- Entradas:
  - DOC-048 (06_CONOCIMIENTO/Buyer_Curiosity_Map.md)
  - DOC-048-TOP100 (06_CONOCIMIENTO/BCE_V1_TOP100.md)
  - DOC-048-ALPHA (06_CONOCIMIENTO/Knowledge_Product_Alpha.md)
  - DOC-050 (06_CONOCIMIENTO/Market_Behavior_Map.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Restricciones:
  - No reabrir SHDLS, Growth System, Buyer System, Decision System, Buyer Curiosity Engine, Market Behavior Map, Buyer Curiosity Map.
  - No ampliar universo de preguntas.
  - No crear frameworks nuevos.
- Responsable: Comercial + Producto + Direccion
- Fecha: 2026-07-15

---

## 0. Analisis critico previo (antes de ejecutar)

### Lo correcto de la orden
1. Cambia el foco de arquitectura a decision outcomes reales.
2. Obliga a disenar journeys, no documentos aislados.
3. Pone la vara en decision movement, no en CTR cosmetico.

### Riesgos de ejecutar la orden literalmente
1. Riesgo de sobrecarga: un journey demasiado largo mata conversion temprana.
2. Riesgo de friccion prematura: pedir datos de contacto muy pronto reduce avance.
3. Riesgo de evidencia tardia: si la prueba aparece tarde, el buyer no confia y abandona.
4. Riesgo de salto de ICP: una experiencia unica para todos degrada relevancia.

### Mejora propuesta
1. Diseñar un journey adaptativo de 3 capas:
- Capa 1: orientacion y diagnostico rapido (sin friccion de datos).
- Capa 2: justificacion (riesgo + finanzas) con evidencia dosificada.
- Capa 3: activacion comercial (pre-evaluacion, reunion, propuesta).
2. Definir CTAs progresivos por madurez decisional, no por funnel tradicional.
3. Medir avance por Decision Stages completados, no solo por clicks.

### Decision de diseno
Se adopta una experiencia centrada en una decision primaria:
- Decidir si iniciar ahora un proyecto de continuidad/infraestructura critica con soporte PICC.

---

## 1. Objetivo

### Decision a acelerar
Acelerar la decision: "Iniciar o no iniciar ahora un proyecto de mitigacion de riesgo operativo con caso financiero defendible".

### Por que es la primera decision
1. Es la decision mas transversal entre H01, H02 y H04.
2. Conecta trigger real (riesgo operativo) con presupuesto (CFO gate).
3. Tiene mayor probabilidad de mover reunion comercial de calidad.

---

## 2. ICP objetivo

### ICP inicial
ICP primario: H02 (CFO/Sponsor) con co-participacion de H01 (Director Tecnico).

### Justificacion
1. H02 habilita o bloquea presupuesto.
2. H01 valida factibilidad tecnica.
3. Esta dupla concentra el punto real de avance o pausa en decisiones complejas.

---

## 3. Trigger

Trigger de entrada principal:
- "Aumento de riesgo operativo percibido + presion de costo de no actuar en el trimestre".

Trigger mapping aprobado:
- TRG-001 (caida operacional)
- TRG-012 (presion de margen/costo)

Evento observable que activa entrada:
- Incidente, microparos, auditoria interna, o warning financiero por continuidad fragil.

---

## 4. Pregunta inicial

Pregunta inicial del recorrido (desde BCE):
- BCQ-0001: "Que operacion critica puede detenerse hoy sin aviso?"

Razon de seleccion:
1. Abre decision desde riesgo real, no desde catalogo.
2. Es comprensible para tecnico y financiero.
3. Permite enrutar inmediatamente a RiskDiag sin pedir datos personales.

---

## 5. Decision Journey (optimo, no literal)

## Etapas

| Etapa                                    | Estado comprador | Que piensa                       | Duda principal                        | Riesgo percibido             | Evidencia necesaria                             | Condicion de avance              |
| ---------------------------------------- | ---------------- | -------------------------------- | ------------------------------------- | ---------------------------- | ----------------------------------------------- | -------------------------------- |
| 1. Entrada por trigger                   | C0-C1            | "Algo se puede romper pronto"    | "Es grave o ruido?"                   | Paro operativo               | Señal de severidad y benchmark minimo           | Completa 3 preguntas diagnostico |
| 2. Diagnostico guiado (RiskDiag)         | C1-C2            | "Necesito claridad"              | "Que tan expuestos estamos?"          | Subestimar impacto           | Resultado sintetico de riesgo + impacto         | Recibe score de riesgo + 2 rutas |
| 3. Ruta de decision                      | C2-C3            | "Que opciones tengo?"            | "Mitigo parcial o proyecto completo?" | Elegir mala opcion           | Matriz opciones trade-off                       | Selecciona ruta preferida        |
| 4. Justificacion financiera (FinJustify) | C3-C4            | "Debo defender esto"             | "Como lo justifico economicamente?"   | Rechazo presupuestal         | Delay cost + payback + sensibilidad             | Genera mini business case        |
| 5. Evidencia comparativa                 | C4-C5            | "Quiero probar que no es teoria" | "Hay casos comparables reales?"       | Falta de credibilidad        | Caso comparable + claim con estado de evidencia | Marca evidencia como suficiente  |
| 6. Decision readiness (DecisionGov-lite) | C5-C6            | "Que objeciones quedan?"         | "Quien puede vetar?"                  | Bloqueo politico interno     | Checklist de vetos/condiciones                  | Completa pre-evaluacion          |
| 7. Activacion comercial                  | C6               | "Estoy listo para avanzar"       | "Con quien hablo y para que?"         | Reunion improductiva         | Agenda propuesta + outputs previos              | Solicita reunion                 |
| 8. Handshake a propuesta                 | C6-C7            | "Quiero plan concreto"           | "Cual es el siguiente paso formal?"   | Desalineacion de expectativa | Scope preliminar + criterio de exito            | Acepta briefing para propuesta   |

### Principio de UX decisional
Cada etapa solo pide la informacion minima para desbloquear la siguiente decision.

---

## 6. Decision Surfaces

| Surface                  | Funcion en experiencia                 | Input             | Output                   | Riesgo si falla                   |
| ------------------------ | -------------------------------------- | ----------------- | ------------------------ | --------------------------------- |
| Home (entry)             | Captura trigger y orienta por problema | Trigger declarado | Ruta a diagnostico       | Rebote por mensaje generico       |
| Landing de problema      | Aterriza contexto sectorial            | Tipo de riesgo    | Inicio de RiskDiag       | Baja relevancia percibida         |
| Diagnostico (RiskDiag)   | Convierte sintoma en score y opciones  | BCQ semilla       | Riesgo sintetizado       | Ambiguedad y abandono             |
| Calculadora (FinJustify) | Convierte riesgo en decision economica | Costos/tiempos    | Business case breve      | Rechazo por numeros debiles       |
| Caso comparable          | Refuerza confianza por evidencia       | Contexto buyer    | Patrón "caso similar"    | Objecion "no aplica a mi caso"    |
| Documento ejecutivo      | Resume para comite                     | Outputs previos   | 1-pager decision-ready   | Friccion para socializar decision |
| Pre-evaluacion PICC      | Califica readiness y agenda reunion    | Datos minimos     | Recomendacion de reunion | Reunion sin calidad               |
| Reunión                  | Alinea alcance y siguiente paso        | Dossier decision  | Brief para propuesta     | No avance a propuesta             |
| Propuesta                | Formaliza compromiso                   | Brief validado    | Propuesta defendible     | Ciclo largo/retrabajo             |

---

## 7. Knowledge Products utilizados

| Momento | Knowledge Product               | Por que aparece ahi                      | Decision que ayuda                            |
| ------- | ------------------------------- | ---------------------------------------- | --------------------------------------------- |
| Etapa 2 | RiskDiag (KPR-01)               | Primero se reduce incertidumbre tecnica  | "Existe riesgo real y accionable?"            |
| Etapa 4 | FinJustify (KPR-02)             | Luego se traduce a lenguaje CFO          | "Se aprueba invertir ahora?"                  |
| Etapa 6 | DecisionGov (KPR-03, modo lite) | Antes de CTA fuerte se limpia veto/poder | "Esta lista la decision para comite/reunion?" |

Regla de orquestacion:
- No mostrar los 3 productos al inicio.
- Mostrar el siguiente producto solo cuando la etapa anterior desbloqueo decision.

---

## 8. Evidence Journey

| Etapa | Evidencia mostrada                          | Confianza que genera                       | Objecion que elimina            |
| ----- | ------------------------------------------- | ------------------------------------------ | ------------------------------- |
| 1-2   | Señales de riesgo + metodologia diagnostico | "No estoy improvisando"                    | "Esto es marketing"             |
| 3     | Matriz comparativa de opciones              | "Puedo evaluar trade-offs"                 | "Solo hay una salida sesgada"   |
| 4     | Calculo de costo de no actuar + payback     | "Puedo defender presupuesto"               | "No hay caso financiero"        |
| 5     | Caso comparable con alcance y limites       | "Esto ya funciono en contexto similar"     | "Mi caso es demasiado distinto" |
| 6     | Checklist de vetos + readiness score        | "Veo riesgos politicos antes de exponerme" | "Comite me va a frenar"         |
| 7-8   | Documento ejecutivo + agenda reunion        | "La reunion tiene objetivo real"           | "Solo me quieren vender"        |

Principio:
- Evidencia progresiva: primero suficiente para avanzar, luego suficiente para decidir.

---

## 9. CTA Journey

| Etapa | CTA                               | Friccion permitida | Datos solicitados                                           |
| ----- | --------------------------------- | ------------------ | ----------------------------------------------------------- |
| 1     | "Iniciar diagnostico"             | Muy baja           | Ninguno                                                     |
| 2     | "Ver resultado de riesgo"         | Baja               | Ninguno                                                     |
| 3     | "Comparar rutas"                  | Baja               | Email opcional para guardar                                 |
| 4     | "Generar caso financiero"         | Media              | Email requerido                                             |
| 5     | "Ver caso comparable completo"    | Media              | Nombre + empresa                                            |
| 6     | "Validar readiness de decision"   | Media-alta         | Telefono opcional                                           |
| 7     | "Solicitar reunion de evaluacion" | Alta (intencional) | Nombre, cargo, empresa, email, telefono, ventana de reunion |
| 8     | "Iniciar briefing de propuesta"   | Alta               | Confirmacion de sponsor/alcance                             |

Reglas:
1. No pedir telefono antes de haber entregado valor claro.
2. No pedir reunion antes de generar output de decision.
3. Si no hay readiness, CTA debe ser "cerrar gaps" y no "agendar".

---

## 10. Metricas (centradas en decision)

| Metrica                | Definicion                                                     | Formula operativa                          | Etapa |
| ---------------------- | -------------------------------------------------------------- | ------------------------------------------ | ----- |
| Decision Coverage      | % de decisiones criticas cubiertas por outputs de experiencia  | decisiones_cubiertas / decisiones_objetivo | 2-6   |
| Decision Velocity      | Tiempo de trigger a solicitud de reunion                       | t(reunion) - t(entrada)                    | 1-7   |
| Trust Gain             | Incremento de confianza declarada entre etapa 2 y 6            | trust_score_6 - trust_score_2              | 2-6   |
| Evidence Consumption   | % de evidencias consumidas por usuario vs evidencias mostradas | evidencias_vistas / evidencias_disponibles | 3-6   |
| Advance Rate           | % de usuarios que pasan a siguiente etapa                      | users_stage_n+1 / users_stage_n            | Todas |
| Meeting Conversion     | % de journeys iniciados que terminan en reunion                | reuniones / entradas                       | 1-7   |
| Shortlist Rate         | % de reuniones que pasan a shortlist/propuesta                 | shortlist / reuniones                      | 7-8   |
| Decision Quality Proxy | % de reuniones con dossier completo (riesgo+finanzas+gobierno) | reuniones_con_dossier / reuniones_totales  | 7     |

Metas Alpha (90 dias):
1. Meeting Conversion >= 8% en trafico calificado.
2. Advance Rate etapa 2->4 >= 40%.
3. Decision Velocity mediana <= 10 dias.
4. Reuniones con dossier completo >= 60%.

---

## 11. Riesgos, vacios e hipotesis abiertas

### Riesgos de ruptura
1. Insuficiente evidencia comparable por vertical.
2. Calculadora financiera sin supuestos aceptados por CFO.
3. CTA de reunion prematura sin readiness real.
4. Sobrecarga de pasos para usuarios de baja urgencia.

### Informacion faltante critica
1. Baselines reales por ICP para Decision Velocity.
2. Umbral de readiness minimo para pasar a reunion.
3. Nivel de detalle de caso comparable permitido por permisos.

### Hipotesis a validar
1. Un score de riesgo claro aumenta avance a etapa financiera.
2. Un business case breve reduce objecion de "no hay presupuesto".
3. Un checklist de vetos previo aumenta tasa de reunion productiva.

---

## 12. MVP de produccion (minimo testeable)

### Alcance MVP
1. Entrada por una sola landing de trigger (riesgo operativo).
2. RiskDiag con 7 preguntas semilla aprobadas.
3. FinJustify con 3 calculos base (delay cost, payback, sensibilidad simple).
4. Caso comparable unico por vertical prioritaria.
5. Documento ejecutivo 1 pagina auto-generado.
6. Pre-evaluacion corta y CTA a reunion.

### Fuera de alcance MVP
1. Personalizacion avanzada por multiples verticales.
2. Automatizacion completa de propuesta.
3. Version multi-idioma completa.

### Criterio de exito MVP
El MVP se considera exitoso si demuestra que la experiencia mueve decisiones, medido por:
1. Reuniones solicitadas con contexto suficiente.
2. Menor tiempo de maduracion de decision.
3. Mayor calidad de reunion (menos discovery repetitivo).

---

## Decisiones de implementacion inmediatas

1. Priorizar ICP H02 con co-ruta H01.
2. Implementar journey secuencial RiskDiag -> FinJustify -> DecisionGov-lite.
3. Activar CTA progresivo con captura de datos por valor entregado.
4. Instrumentar metricas de decision desde dia 1 (no solo analytics de trafico).

## No-negociables de este sprint

1. No crear nuevos mapas ni frameworks.
2. No ampliar BCE ni preguntas.
3. No convertir la experiencia en un PDF estatico.
4. No pedir reunion sin readiness minimo.

## Resultado esperado de sprint

Un buyer puede completar un recorrido coherente desde trigger inicial hasta solicitud de reunion con:
1. Diagnostico de riesgo.
2. Justificacion economica.
3. Preparacion de decision defendible.

Si eso ocurre de forma medible, el sprint es exitoso.
