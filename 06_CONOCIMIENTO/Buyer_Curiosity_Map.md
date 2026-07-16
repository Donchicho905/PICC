# Buyer Curiosity Engine V1 (SSOT)

## Ficha de trazabilidad
- ID: DOC-048
- Estado: ðŸŸ¢ Aprobado para ejecuciÃ³n
- Tipo: Buyer Curiosity Engine
- Objetivo: convertir curiosidad dispersa en sistema de preguntas accionables para decisiones de compra complejas.
- Checkpoint base: picc-next-market-behavior-v1
- Entradas:
  - DOC-047 (06_CONOCIMIENTO/Market_Knowledge_Map.md)
  - DOC-049 (06_CONOCIMIENTO/Market_Behavior_Map.md)
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
- Salidas obligatorias:
  - Buyer Curiosity Model
  - Question Graph
  - Universo de 300 preguntas Ãºnicas
  - Top 100 prioritarias
  - PriorizaciÃ³n explicable
  - Question-to-Product Mapping
  - Question-to-Surface Mapping
  - Question-to-CTA Mapping
  - Information Gap Matrix
  - Primer Knowledge Product Backlog
- Responsable: DirecciÃ³n + Comercial + Producto
- Fecha: 2026-07-15

## 1) Buyer Curiosity Model

### Estados
- C0 Latencia: no reconoce riesgo.
- C1 FricciÃ³n: detecta sÃ­ntoma sin diagnÃ³stico.
- C2 FormulaciÃ³n: nombra problema y alcance.
- C3 ComparaciÃ³n: evalÃºa opciones y trade-offs.
- C4 Defensa: prepara caso para comitÃ©.
- C5 VerificaciÃ³n: exige evidencia y permisos.
- C6 DecisiÃ³n: aprueba, pausa, bloquea o descarta.
- C7 ImplementaciÃ³n: valida ejecuciÃ³n y resultado.

### Regla de calidad
Una pregunta solo entra si conecta: trigger + decisiÃ³n + riesgo + evidencia + actor.

## 2) Question Graph

### Nodos
- N1 Trigger
- N2 Riesgo
- N3 Costo de no actuar
- N4 Opciones
- N5 Viabilidad tÃ©cnica
- N6 Viabilidad financiera
- N7 Cumplimiento
- N8 Evidencia
- N9 ComitÃ©
- N10 ContrataciÃ³n
- N11 ImplementaciÃ³n
- N12 Resultado

### Arcos
- N1 -> N2 -> N3
- N3 -> N4 -> N5 + N6 + N7
- N5 + N6 + N7 -> N8
- N8 -> N9 -> N10
- N10 -> N11 -> N12

## 3) ConvenciÃ³n de IDs
- Pregunta: BCQ-0001 a BCQ-0300
- Producto de conocimiento: KPR-01 a KPR-12
- Surface: SFC-01 a SFC-10
- CTA: CTA-01 a CTA-10
- Gap de informaciÃ³n: GAP-01 a GAP-12

## 4) Estrategia anti-duplicados semÃ¡nticos
- NormalizaciÃ³n de intenciÃ³n: cada pregunta se clasifica por verbo decisional (evaluar, comparar, justificar, mitigar, validar).
- Regla de unicidad: no se permiten dos preguntas con mismo actor + misma decisiÃ³n + mismo riesgo + misma evidencia.
- Distancia mÃ­nima: si cambia solo redacciÃ³n y no cambia decisiÃ³n objetivo, se colapsa en una sola pregunta canÃ³nica.
- Trazabilidad: cada pregunta lleva estado de curiosidad (C0-C7) y nodo del graph (N1-N12).

## 5) Universo mÃ­nimo de 300 preguntas Ãºnicas

### 5.1 Trigger y riesgo operativo (BCQ-0001 a BCQ-0050)
1. BCQ-0001: Â¿QuÃ© operaciÃ³n crÃ­tica puede detenerse hoy sin aviso?
2. BCQ-0002: Â¿CuÃ¡l es el primer indicador de degradaciÃ³n antes del paro?
3. BCQ-0003: Â¿QuÃ© microparo repetido ya estÃ¡ normalizado?
4. BCQ-0004: Â¿DÃ³nde tenemos punto Ãºnico de falla?
5. BCQ-0005: Â¿QuÃ© incidente reciente no documentamos bien?
6. BCQ-0006: Â¿QuÃ© dependencia externa puede romper continuidad?
7. BCQ-0007: Â¿QuÃ© proceso manual concentra demasiado riesgo?
8. BCQ-0008: Â¿QuÃ© equipo opera fuera de su ventana segura?
9. BCQ-0009: Â¿QuÃ© alarma ignoramos por fatiga operativa?
10. BCQ-0010: Â¿QuÃ© Ã¡rea no tiene plan de contingencia usable?
11. BCQ-0011: Â¿QuÃ© costo oculto genera cada paro corto?
12. BCQ-0012: Â¿QuÃ© parte de la operaciÃ³n no tiene redundancia real?
13. BCQ-0013: Â¿QuÃ© proveedor nos deja expuestos por lead time?
14. BCQ-0014: Â¿QuÃ© turno concentra mayor probabilidad de error?
15. BCQ-0015: Â¿QuÃ© dependencia tecnolÃ³gica no estÃ¡ monitoreada?
16. BCQ-0016: Â¿QuÃ© mantenimiento diferido ya es deuda crÃ­tica?
17. BCQ-0017: Â¿QuÃ© hipÃ³tesis operativa seguimos sin validar?
18. BCQ-0018: Â¿QuÃ© incidente casi ocurriÃ³ pero no escalamos?
19. BCQ-0019: Â¿QuÃ© rol no tiene reemplazo ante contingencia?
20. BCQ-0020: Â¿QuÃ© capacidad mÃ­nima necesitamos para resistir 24h?
21. BCQ-0021: Â¿CuÃ¡l es nuestro MTTR real por tipo de falla?
22. BCQ-0022: Â¿QuÃ© KPI operativo estÃ¡ maquillando riesgo?
23. BCQ-0023: Â¿QuÃ© umbral de falla deberÃ­a disparar decisiÃ³n ejecutiva?
24. BCQ-0024: Â¿QuÃ© seÃ±al temprana deberÃ­amos monitorear y hoy no existe?
25. BCQ-0025: Â¿QuÃ© evento extremo estÃ¡ fuera de nuestro escenario base?
26. BCQ-0026: Â¿QuÃ© riesgo operativo crece con la demanda actual?
27. BCQ-0027: Â¿QuÃ© error recurrente se resuelve con rediseÃ±o y no con disciplina?
28. BCQ-0028: Â¿QuÃ© parte del sistema falla por integraciÃ³n deficiente?
29. BCQ-0029: Â¿QuÃ© evidencia necesitamos para probar fragilidad estructural?
30. BCQ-0030: Â¿QuÃ© Ã¡rea perderÃ­a mÃ¡s en una interrupciÃ³n de 2 horas?
31. BCQ-0031: Â¿QuÃ© riesgo operativo no entiende direcciÃ³n?
32. BCQ-0032: Â¿QuÃ© riesgo operacional estamos subestimando por costumbre?
33. BCQ-0033: Â¿QuÃ© condiciÃ³n temporal vuelve crÃ­tica una falla menor?
34. BCQ-0034: Â¿QuÃ© riesgo aparece por crecimiento sin rediseÃ±o?
35. BCQ-0035: Â¿QuÃ© dependencia de software bloquea continuidad fÃ­sica?
36. BCQ-0036: Â¿QuÃ© mÃ©trica de continuidad no estÃ¡ en comitÃ©?
37. BCQ-0037: Â¿QuÃ© incidente puede escalar a reputacional en 48h?
38. BCQ-0038: Â¿QuÃ© parte del diagnÃ³stico operativo estÃ¡ basada en opiniÃ³n?
39. BCQ-0039: Â¿QuÃ© datos faltan para modelar riesgo con confianza?
40. BCQ-0040: Â¿QuÃ© escenario de caÃ­da total no hemos simulado?
41. BCQ-0041: Â¿QuÃ© riesgo cambia entre dÃ­a hÃ¡bil y fin de semana?
42. BCQ-0042: Â¿QuÃ© falla depende de una persona especÃ­fica?
43. BCQ-0043: Â¿QuÃ© proceso carece de evidencia de cumplimiento operativo?
44. BCQ-0044: Â¿QuÃ© capa de protecciÃ³n estÃ¡ desactualizada?
45. BCQ-0045: Â¿QuÃ© contrato actual dificulta mitigar riesgo?
46. BCQ-0046: Â¿QuÃ© riesgo no estÃ¡ reflejado en presupuesto?
47. BCQ-0047: Â¿QuÃ© seÃ±al externa anticipa presiÃ³n operativa interna?
48. BCQ-0048: Â¿QuÃ© auditorÃ­a interna puede detonar inversiÃ³n inmediata?
49. BCQ-0049: Â¿QuÃ© aprendizaje de incidentes no se institucionalizÃ³?
50. BCQ-0050: Â¿QuÃ© acciÃ³n mÃ­nima reduce mÃ¡s riesgo este trimestre?

### 5.2 Estrategia, capacidad y crecimiento (BCQ-0051 a BCQ-0100)
51. BCQ-0051: Â¿QuÃ© meta de crecimiento rompe nuestra capacidad actual?
52. BCQ-0052: Â¿QuÃ© expansiÃ³n exige rediseÃ±o y no solo ampliaciÃ³n?
53. BCQ-0053: Â¿QuÃ© cliente ancla cambia nuestro umbral de continuidad?
54. BCQ-0054: Â¿QuÃ© SLA nuevo no podemos defender hoy?
55. BCQ-0055: Â¿QuÃ© parte del plan estratÃ©gico depende de resiliencia no probada?
56. BCQ-0056: Â¿QuÃ© riesgo aparece si abrimos una nueva sede?
57. BCQ-0057: Â¿QuÃ© escenario de nearshoring nos favorece o nos expone?
58. BCQ-0058: Â¿QuÃ© decisiÃ³n de capacidad debe tomarse antes del siguiente capex?
59. BCQ-0059: Â¿QuÃ© inversiÃ³n evita cuellos de botella en 12 meses?
60. BCQ-0060: Â¿QuÃ© seÃ±al de mercado justifica acelerar proyecto?
61. BCQ-0061: Â¿QuÃ© seÃ±al de mercado justifica pausar proyecto?
62. BCQ-0062: Â¿QuÃ© costo tendrÃ­a no ejecutar la expansiÃ³n ahora?
63. BCQ-0063: Â¿QuÃ© arquitectura soporta crecimiento sin degradar servicio?
64. BCQ-0064: Â¿QuÃ© mÃ©trica define que ya estamos en zona de riesgo?
65. BCQ-0065: Â¿QuÃ© hipÃ³tesis de demanda requiere validaciÃ³n externa?
66. BCQ-0066: Â¿QuÃ© cambio en mix de clientes cambia prioridad tÃ©cnica?
67. BCQ-0067: Â¿QuÃ© parte del crecimiento depende de terceros no controlados?
68. BCQ-0068: Â¿QuÃ© trade-off entre velocidad y resiliencia es aceptable?
69. BCQ-0069: Â¿QuÃ© ruta de crecimiento tiene menor riesgo regulatorio?
70. BCQ-0070: Â¿QuÃ© secuencia de inversiÃ³n reduce riesgo de sobrecapacidad?
71. BCQ-0071: Â¿QuÃ© rediseÃ±o habilita crecimiento modular?
72. BCQ-0072: Â¿QuÃ© nivel de redundancia exige el mercado objetivo?
73. BCQ-0073: Â¿QuÃ© evidencia pide direcciÃ³n para aprobar crecimiento?
74. BCQ-0074: Â¿QuÃ© benchmark valida que nuestra ruta es defendible?
75. BCQ-0075: Â¿QuÃ© dependencia comercial podrÃ­a frenar expansiÃ³n tÃ©cnica?
76. BCQ-0076: Â¿QuÃ© cambio en tarifas energÃ©ticas altera el plan?
77. BCQ-0077: Â¿QuÃ© escenario macroeconÃ³mico vuelve inviable el timing?
78. BCQ-0078: Â¿QuÃ© riesgos de ejecuciÃ³n comprometen la estrategia?
79. BCQ-0079: Â¿QuÃ© fase del plan tiene mayor incertidumbre?
80. BCQ-0080: Â¿QuÃ© trigger obliga a re-priorizar cartera de proyectos?
81. BCQ-0081: Â¿QuÃ© capacidades internas deben fortalecerse antes de crecer?
82. BCQ-0082: Â¿QuÃ© capacidades conviene externalizar temporalmente?
83. BCQ-0083: Â¿QuÃ© costo de oportunidad tiene no modernizar?
84. BCQ-0084: Â¿QuÃ© decisiÃ³n no se puede posponer mÃ¡s de 90 dÃ­as?
85. BCQ-0085: Â¿QuÃ© riesgo estratÃ©gico estÃ¡ oculto en el presupuesto actual?
86. BCQ-0086: Â¿QuÃ© indicadores anticipan saturaciÃ³n operativa?
87. BCQ-0087: Â¿QuÃ© parte del caso de crecimiento es narrativa sin evidencia?
88. BCQ-0088: Â¿QuÃ© inversiÃ³n incremental crea mÃ¡s opcionalidad futura?
89. BCQ-0089: Â¿QuÃ© capacidad crÃ­tica no estÃ¡ cubierta por contrato?
90. BCQ-0090: Â¿QuÃ© dependencia geogrÃ¡fica eleva vulnerabilidad?
91. BCQ-0091: Â¿QuÃ© cronograma maximiza aprendizaje antes de escalar?
92. BCQ-0092: Â¿QuÃ© condiciones definen una expansiÃ³n segura?
93. BCQ-0093: Â¿QuÃ© comitÃ© debe involucrarse antes de comprometer capex?
94. BCQ-0094: Â¿QuÃ© conversaciÃ³n con finanzas falta para habilitar avance?
95. BCQ-0095: Â¿QuÃ© evidencia tÃ©cnica convierte intenciÃ³n en proyecto?
96. BCQ-0096: Â¿QuÃ© estructura de fases reduce riesgo polÃ­tico interno?
97. BCQ-0097: Â¿QuÃ© escenario de crecimiento conserva margen?
98. BCQ-0098: Â¿QuÃ© modelo de implementaciÃ³n minimiza disrupciÃ³n?
99. BCQ-0099: Â¿QuÃ© parte del roadmap es reversible si cambia contexto?
100. BCQ-0100: Â¿QuÃ© decisiÃ³n estratÃ©gica requiere prototipo antes de aprobar?

### 5.3 Cumplimiento, finanzas, comitÃ© y compra (BCQ-0101 a BCQ-0200)
101. BCQ-0101: Â¿QuÃ© norma nueva impacta diseÃ±o y operaciÃ³n?
102. BCQ-0102: Â¿QuÃ© certificaciÃ³n pide un cliente clave para continuar?
103. BCQ-0103: Â¿QuÃ© requisito legal hoy no estÃ¡ evidenciado?
104. BCQ-0104: Â¿QuÃ© interpretaciÃ³n regulatoria genera mÃ¡s incertidumbre?
105. BCQ-0105: Â¿QuÃ© hallazgo de auditorÃ­a puede bloquear aprobaciÃ³n?
106. BCQ-0106: Â¿QuÃ© costo de incumplimiento supera la inversiÃ³n propuesta?
107. BCQ-0107: Â¿QuÃ© permiso de uso de evidencia falta asegurar?
108. BCQ-0108: Â¿QuÃ© contrato actual limita opciones de rediseÃ±o?
109. BCQ-0109: Â¿QuÃ© clÃ¡usula puede transferir riesgo a nuestra operaciÃ³n?
110. BCQ-0110: Â¿QuÃ© documento legal necesita revisiÃ³n tÃ©cnica adicional?
111. BCQ-0111: Â¿QuÃ© supuesto financiero sostiene el caso interno?
112. BCQ-0112: Â¿QuÃ© variable econÃ³mica cambia mÃ¡s el payback?
113. BCQ-0113: Â¿QuÃ© sensibilidad mÃ­nima debe aprobar finanzas?
114. BCQ-0114: Â¿QuÃ© escenario pesimista conserva viabilidad?
115. BCQ-0115: Â¿QuÃ© costo total de propiedad estamos omitiendo?
116. BCQ-0116: Â¿QuÃ© riesgo de caja aparece durante implementaciÃ³n?
117. BCQ-0117: Â¿QuÃ© hitos deben condicionar desembolso?
118. BCQ-0118: Â¿QuÃ© alternativa ofrece menor riesgo financiero acumulado?
119. BCQ-0119: Â¿QuÃ© mÃ©tricas exige el comitÃ© para decidir?
120. BCQ-0120: Â¿QuÃ© evidencia convierte opiniÃ³n en aprobaciÃ³n?
121. BCQ-0121: Â¿QuiÃ©n puede vetar y por quÃ© criterio?
122. BCQ-0122: Â¿QuÃ© actor informal inclina la decisiÃ³n final?
123. BCQ-0123: Â¿QuÃ© objeciÃ³n recurrente frena el avance?
124. BCQ-0124: Â¿QuÃ© narrativa necesita direcciÃ³n para defenderse?
125. BCQ-0125: Â¿QuÃ© pregunta de comitÃ© no estamos anticipando?
126. BCQ-0126: Â¿QuÃ© formato de board pack reduce rechazo?
127. BCQ-0127: Â¿QuÃ© decisiÃ³n requiere comparables autorizados?
128. BCQ-0128: Â¿QuÃ© desacuerdo entre Ã¡reas bloquea shortlist?
129. BCQ-0129: Â¿QuÃ© informaciÃ³n tÃ©cnica debe simplificarse para comitÃ©?
130. BCQ-0130: Â¿QuÃ© lenguaje financiero falta en la propuesta tÃ©cnica?
131. BCQ-0131: Â¿QuÃ© criterio usa compras para descalificar?
132. BCQ-0132: Â¿QuÃ© ambigÃ¼edad de alcance eleva riesgo contractual?
133. BCQ-0133: Â¿QuÃ© evidencia exige compras para cerrar expediente?
134. BCQ-0134: Â¿QuÃ© riesgo de lock-in preocupa al evaluador?
135. BCQ-0135: Â¿QuÃ© comparaciÃ³n de alternativas es realmente defendible?
136. BCQ-0136: Â¿QuÃ© seÃ±al indica shortlist sesgada?
137. BCQ-0137: Â¿QuÃ© parte de la propuesta no es verificable?
138. BCQ-0138: Â¿QuÃ© claim debe eliminarse por falta de fuente?
139. BCQ-0139: Â¿QuÃ© prueba piloto reducirÃ­a incertidumbre decisional?
140. BCQ-0140: Â¿QuÃ© concesiÃ³n contractual protege continuidad?
141. BCQ-0141: Â¿QuÃ© dependencia de proveedor eleva riesgo de implementaciÃ³n?
142. BCQ-0142: Â¿QuÃ© criterio tÃ©cnico mÃ­nimo debe estar en contrato?
143. BCQ-0143: Â¿QuÃ© riesgos de cambio de alcance deben predefinirse?
144. BCQ-0144: Â¿QuÃ© obligaciÃ³n de soporte debe quedar explÃ­cita?
145. BCQ-0145: Â¿QuÃ© mecanismo de escalaciÃ³n reduce fricciÃ³n post-firma?
146. BCQ-0146: Â¿QuÃ© entregable debe validar aceptaciÃ³n parcial?
147. BCQ-0147: Â¿QuÃ© evidencia evita disputa en hitos de pago?
148. BCQ-0148: Â¿QuÃ© criterio de Ã©xito debe quedar firmado?
149. BCQ-0149: Â¿QuÃ© exclusiones deben explicitarse para evitar sobreexpectativa?
150. BCQ-0150: Â¿QuÃ© parte del riesgo no puede transferirse por contrato?
151. BCQ-0151: Â¿QuÃ© capacidad tÃ©cnica interna falta para operar la soluciÃ³n?
152. BCQ-0152: Â¿QuÃ© entrenamiento reduce riesgo de adopciÃ³n?
153. BCQ-0153: Â¿QuÃ© dependencia del integrador debe mitigarse desde diseÃ±o?
154. BCQ-0154: Â¿QuÃ© arquitectura permite mantenimiento sin paro?
155. BCQ-0155: Â¿QuÃ© restricciones del sitio condicionan factibilidad?
156. BCQ-0156: Â¿QuÃ© integraciones crÃ­ticas requieren prueba anticipada?
157. BCQ-0157: Â¿QuÃ© criterio tÃ©cnico define una mala opciÃ³n aunque sea barata?
158. BCQ-0158: Â¿QuÃ© evidencia de campo valida desempeÃ±o esperado?
159. BCQ-0159: Â¿QuÃ© supuestos de ingenierÃ­a siguen sin validaciÃ³n?
160. BCQ-0160: Â¿QuÃ© riesgo tÃ©cnico debe escalarse a direcciÃ³n?
161. BCQ-0161: Â¿QuÃ© variable operacional rompe la simulaciÃ³n teÃ³rica?
162. BCQ-0162: Â¿QuÃ© dependencias elÃ©ctricas no estÃ¡n mapeadas?
163. BCQ-0163: Â¿QuÃ© integraciÃ³n con sistemas legados tiene mayor riesgo?
164. BCQ-0164: Â¿QuÃ© tolerancia de falla exige el usuario final?
165. BCQ-0165: Â¿QuÃ© mÃ©tricas tÃ©cnicas deben monitorearse en semana 1?
166. BCQ-0166: Â¿QuÃ© pruebas FAT/SAT son indispensables?
167. BCQ-0167: Â¿QuÃ© criterio de aceptaciÃ³n tÃ©cnica evita retrabajo?
168. BCQ-0168: Â¿QuÃ© interfaz requiere mayor estandarizaciÃ³n?
169. BCQ-0169: Â¿QuÃ© decisiÃ³n tÃ©cnica debe quedar congelada antes de compras?
170. BCQ-0170: Â¿QuÃ© restricciones de ciberseguridad aplican al diseÃ±o?
171. BCQ-0171: Â¿QuÃ© evento de implementaciÃ³n puede detener operaciÃ³n?
172. BCQ-0172: Â¿QuÃ© plan de rollback existe si falla despliegue?
173. BCQ-0173: Â¿QuÃ© ventana de intervenciÃ³n minimiza impacto?
174. BCQ-0174: Â¿QuÃ© coordinaciÃ³n entre Ã¡reas evita cuellos?
175. BCQ-0175: Â¿QuÃ© seÃ±al de desviaciÃ³n debe disparar correcciÃ³n inmediata?
176. BCQ-0176: Â¿QuÃ© hito operativo confirma avance real?
177. BCQ-0177: Â¿QuÃ© dependencia logÃ­stica puede retrasar proyecto?
178. BCQ-0178: Â¿QuÃ© decisiÃ³n de alcance debe tomarse in situ?
179. BCQ-0179: Â¿QuÃ© procedimiento de seguridad condiciona ejecuciÃ³n?
180. BCQ-0180: Â¿QuÃ© evidencia diaria reduce incertidumbre del sponsor?
181. BCQ-0181: Â¿QuÃ© indicador muestra adopciÃ³n real por usuarios?
182. BCQ-0182: Â¿QuÃ© parte de la soluciÃ³n genera fricciÃ³n de uso?
183. BCQ-0183: Â¿QuÃ© ajuste operativo mejora desempeÃ±o sin inversiÃ³n adicional?
184. BCQ-0184: Â¿QuÃ© incidentes iniciales son normales y cuÃ¡les crÃ­ticos?
185. BCQ-0185: Â¿QuÃ© soporte post-implementaciÃ³n evita degradaciÃ³n?
186. BCQ-0186: Â¿QuÃ© criterio define que el proyecto ya capturÃ³ valor?
187. BCQ-0187: Â¿QuÃ© KPI debe mejorar para declarar Ã©xito?
188. BCQ-0188: Â¿QuÃ© aprendizaje debe documentarse para prÃ³xima fase?
189. BCQ-0189: Â¿QuÃ© condiciÃ³n habilita expansiÃ³n segura?
190. BCQ-0190: Â¿QuÃ© evidencia habilita referencia pÃºblica autorizada?
191. BCQ-0191: Â¿QuÃ© competencia estÃ¡ capturando la conversaciÃ³n primero?
192. BCQ-0192: Â¿QuÃ© mensaje diferencial resiste comparaciÃ³n tÃ©cnica?
193. BCQ-0193: Â¿QuÃ© claim de competidor no es verificable?
194. BCQ-0194: Â¿QuÃ© sesgo del evaluador favorece una opciÃ³n subÃ³ptima?
195. BCQ-0195: Â¿QuÃ© evidencia comparativa falta para shortlist justa?
196. BCQ-0196: Â¿QuÃ© seÃ±al de commoditizaciÃ³n amenaza margen?
197. BCQ-0197: Â¿QuÃ© alianza externa mejora probabilidad de cierre?
198. BCQ-0198: Â¿QuÃ© riesgo de sobrepromesa debe mitigarse en venta?
199. BCQ-0199: Â¿QuÃ© objeciÃ³n competitiva necesita respuesta estÃ¡ndar?
200. BCQ-0200: Â¿QuÃ© prueba de desempeÃ±o diferencia oferta de forma defendible?

### 5.4 Evidencia, confianza, postventa y expansiÃ³n (BCQ-0201 a BCQ-0300)
201. BCQ-0201: Â¿QuÃ© evidencia mÃ­nima requiere cada tipo de decisiÃ³n?
202. BCQ-0202: Â¿QuÃ© evidencia externa valida claims crÃ­ticos?
203. BCQ-0203: Â¿QuÃ© evidencia interna tiene trazabilidad incompleta?
204. BCQ-0204: Â¿QuÃ© permiso legal falta para publicar caso?
205. BCQ-0205: Â¿QuÃ© dato no podemos afirmar sin riesgo reputacional?
206. BCQ-0206: Â¿QuÃ© formato de evidencia entiende mejor finanzas?
207. BCQ-0207: Â¿QuÃ© formato de evidencia entiende mejor tÃ©cnico?
208. BCQ-0208: Â¿QuÃ© formato de evidencia entiende mejor direcciÃ³n?
209. BCQ-0209: Â¿QuÃ© evidencia de resultado necesita compras?
210. BCQ-0210: Â¿QuÃ© evidencia de proceso necesita compliance?
211. BCQ-0211: Â¿QuÃ© claim exige disclaimer obligatorio?
212. BCQ-0212: Â¿QuÃ© inconsistencia documental erosiona confianza?
213. BCQ-0213: Â¿QuÃ© brecha de evidencia frena aprobaciÃ³n hoy?
214. BCQ-0214: Â¿QuÃ© fuente de datos debe auditarse primero?
215. BCQ-0215: Â¿QuÃ© narrativa sin evidencia debe pausarse?
216. BCQ-0216: Â¿QuÃ© caso comparable tiene mayor poder de convencimiento?
217. BCQ-0217: Â¿QuÃ© evidencia de benchmark reduce sesgo de proveedor?
218. BCQ-0218: Â¿QuÃ© evidencia visual sÃ­ tiene permiso expreso?
219. BCQ-0219: Â¿QuÃ© evidencia numÃ©rica requiere actualizaciÃ³n trimestral?
220. BCQ-0220: Â¿QuÃ© evidencia de riesgo mitigado falta documentar?
221. BCQ-0221: Â¿QuÃ© CTA convierte curiosidad en diagnÃ³stico formal?
222. BCQ-0222: Â¿QuÃ© CTA funciona mejor por etapa C0-C7?
223. BCQ-0223: Â¿QuÃ© surface atrae mÃ¡s preguntas de alta intenciÃ³n?
224. BCQ-0224: Â¿QuÃ© surface produce mejor tasa de reuniÃ³n tÃ©cnica?
225. BCQ-0225: Â¿QuÃ© canal acelera respuesta sin perder trazabilidad?
226. BCQ-0226: Â¿QuÃ© tipo de contenido reduce fricciÃ³n inicial?
227. BCQ-0227: Â¿QuÃ© contenido habilita defensa interna en comitÃ©?
228. BCQ-0228: Â¿QuÃ© contenido eleva confianza en revisiÃ³n legal?
229. BCQ-0229: Â¿QuÃ© contenido incrementa calidad de shortlist?
230. BCQ-0230: Â¿QuÃ© contenido reduce objeciones de precio?
231. BCQ-0231: Â¿QuÃ© pregunta debe responder la calculadora financiera?
232. BCQ-0232: Â¿QuÃ© pregunta debe resolver el checklist regulatorio?
233. BCQ-0233: Â¿QuÃ© pregunta debe cubrir el comparador tÃ©cnico?
234. BCQ-0234: Â¿QuÃ© pregunta debe resolver el board brief?
235. BCQ-0235: Â¿QuÃ© pregunta debe resolver la guÃ­a de implementaciÃ³n?
236. BCQ-0236: Â¿QuÃ© evidencia debe exigirse antes de enviar propuesta?
237. BCQ-0237: Â¿QuÃ© evidencia debe exigirse antes de firma?
238. BCQ-0238: Â¿QuÃ© evidencia debe exigirse antes de go-live?
239. BCQ-0239: Â¿QuÃ© evidencia debe exigirse antes de expansiÃ³n?
240. BCQ-0240: Â¿QuÃ© evidencia convierte proyecto en referencia pÃºblica?
241. BCQ-0241: Â¿QuÃ© seÃ±al temprana de abandono debemos detectar?
242. BCQ-0242: Â¿QuÃ© causa principal explica pausas largas?
243. BCQ-0243: Â¿QuÃ© pregunta identifica veto silencioso?
244. BCQ-0244: Â¿QuÃ© pregunta destapa riesgo polÃ­tico interno?
245. BCQ-0245: Â¿QuÃ© pregunta revela falta de owner real?
246. BCQ-0246: Â¿QuÃ© pregunta separa duda real de objeciÃ³n tÃ¡ctica?
247. BCQ-0247: Â¿QuÃ© pregunta expone sobreconfianza tÃ©cnica?
248. BCQ-0248: Â¿QuÃ© pregunta detecta optimismo financiero irreal?
249. BCQ-0249: Â¿QuÃ© pregunta detecta sesgo de confirmaciÃ³n del sponsor?
250. BCQ-0250: Â¿QuÃ© pregunta valida urgencia autÃ©ntica del problema?
251. BCQ-0251: Â¿QuÃ© condiciÃ³n habilita cross-sell post-ejecuciÃ³n?
252. BCQ-0252: Â¿QuÃ© resultado mÃ­nimo justifica upsell?
253. BCQ-0253: Â¿QuÃ© evidencia de valor sostiene renovaciÃ³n?
254. BCQ-0254: Â¿QuÃ© aprendizaje operativo puede empaquetarse como producto?
255. BCQ-0255: Â¿QuÃ© pregunta abre conversaciÃ³n de fase 2?
256. BCQ-0256: Â¿QuÃ© fricciÃ³n recurrente puede resolverse con producto de conocimiento?
257. BCQ-0257: Â¿QuÃ© patrÃ³n de pregunta se repite por industria?
258. BCQ-0258: Â¿QuÃ© patrÃ³n de pregunta se repite por rol?
259. BCQ-0259: Â¿QuÃ© patrÃ³n de pregunta se repite por etapa?
260. BCQ-0260: Â¿QuÃ© patrÃ³n de pregunta se repite por tamaÃ±o de proyecto?
261. BCQ-0261: Â¿QuÃ© patrÃ³n de pÃ©rdida se anticipa con preguntas tempranas?
262. BCQ-0262: Â¿QuÃ© pregunta predice mejor probabilidad de cierre?
263. BCQ-0263: Â¿QuÃ© pregunta predice mayor riesgo de retraso?
264. BCQ-0264: Â¿QuÃ© pregunta predice mayor riesgo de sobrecosto?
265. BCQ-0265: Â¿QuÃ© pregunta predice mayor riesgo de rechazo legal?
266. BCQ-0266: Â¿QuÃ© pregunta predice mayor riesgo de rechazo tÃ©cnico?
267. BCQ-0267: Â¿QuÃ© pregunta predice mayor riesgo de rechazo financiero?
268. BCQ-0268: Â¿QuÃ© pregunta predice mayor riesgo de rechazo polÃ­tico?
269. BCQ-0269: Â¿QuÃ© pregunta ayuda a priorizar hallazgos de discovery?
270. BCQ-0270: Â¿QuÃ© pregunta define alcance mÃ­nimo viable del proyecto?
271. BCQ-0271: Â¿QuÃ© pregunta convierte interÃ©s en diagnÃ³stico pagable?
272. BCQ-0272: Â¿QuÃ© pregunta convierte diagnÃ³stico en caso interno?
273. BCQ-0273: Â¿QuÃ© pregunta convierte caso interno en aprobaciÃ³n?
274. BCQ-0274: Â¿QuÃ© pregunta convierte aprobaciÃ³n en contrataciÃ³n Ã¡gil?
275. BCQ-0275: Â¿QuÃ© pregunta convierte contrataciÃ³n en implementaciÃ³n ordenada?
276. BCQ-0276: Â¿QuÃ© pregunta convierte implementaciÃ³n en prueba de valor?
277. BCQ-0277: Â¿QuÃ© pregunta convierte prueba de valor en expansiÃ³n?
278. BCQ-0278: Â¿QuÃ© pregunta convierte expansiÃ³n en referencia autorizada?
279. BCQ-0279: Â¿QuÃ© pregunta mejora la calidad del handoff interno?
280. BCQ-0280: Â¿QuÃ© pregunta evita pÃ©rdida de contexto entre comercial y tÃ©cnico?
281. BCQ-0281: Â¿QuÃ© pregunta mejora la reuniÃ³n de kickoff?
282. BCQ-0282: Â¿QuÃ© pregunta mejora la revisiÃ³n de avance semanal?
283. BCQ-0283: Â¿QuÃ© pregunta mejora la revisiÃ³n ejecutiva mensual?
284. BCQ-0284: Â¿QuÃ© pregunta mejora la gestiÃ³n de riesgos activos?
285. BCQ-0285: Â¿QuÃ© pregunta mejora la gestiÃ³n de cambios de alcance?
286. BCQ-0286: Â¿QuÃ© pregunta mejora la calidad de cierre tÃ©cnico?
287. BCQ-0287: Â¿QuÃ© pregunta mejora la calidad de cierre comercial?
288. BCQ-0288: Â¿QuÃ© pregunta mejora la captura de lecciones aprendidas?
289. BCQ-0289: Â¿QuÃ© pregunta mejora reutilizaciÃ³n de evidencia en prÃ³ximos casos?
290. BCQ-0290: Â¿QuÃ© pregunta mejora velocidad de respuesta en preventa?
291. BCQ-0291: Â¿QuÃ© pregunta mejora precisiÃ³n de propuestas?
292. BCQ-0292: Â¿QuÃ© pregunta mejora consistencia de mensajes?
293. BCQ-0293: Â¿QuÃ© pregunta mejora coordinaciÃ³n con partners?
294. BCQ-0294: Â¿QuÃ© pregunta mejora escalaciÃ³n de decisiones bloqueadas?
295. BCQ-0295: Â¿QuÃ© pregunta mejora control de supuestos crÃ­ticos?
296. BCQ-0296: Â¿QuÃ© pregunta mejora transparencia de limitaciones tÃ©cnicas?
297. BCQ-0297: Â¿QuÃ© pregunta mejora trazabilidad de evidencia usada?
298. BCQ-0298: Â¿QuÃ© pregunta mejora criterio de priorizaciÃ³n de oportunidades?
299. BCQ-0299: Â¿QuÃ© pregunta mejora predicciÃ³n de win/loss?
300. BCQ-0300: Â¿QuÃ© pregunta debemos dejar de hacer porque no mueve decisiÃ³n?

## 6) Auditoría estructural de integridad
- IDs detectados: 300
- IDs únicos: 300
- Rango: BCQ-0001 a BCQ-0300 completo
- IDs duplicados: 0
- IDs faltantes: 0
- Preguntas vacías: 0
- Estado: PASS estructural

## 7) Auditoría semántica
### Duplicidad semántica (resultado)
- No se encontraron duplicados semánticos graves que requieran fusión o renumeración.
- Se detectaron 7 pares cercanos; se mantienen porque cambian decisión, etapa o criterio de riesgo.
- Pares cercanos revisados: BCQ-0060/0061, BCQ-0265/0267, BCQ-0276/0277, BCQ-0263/0264, BCQ-0257/0258, BCQ-0257/0259, BCQ-0258/0259.
### Naturalidad
- PASS con ajustes de criterio: el lenguaje es de comprador y comité, no de promoción de oferta.
### Neutralidad
- PASS: las 300 preguntas sobreviven a la prueba "si PICC desapareciera".
### Valor decisional
- PASS parcial reforzado: toda pregunta Top 100 quedó conectada explícitamente a decisión, evidencia, producto, surface y CTA.

## 8) Matriz canónica de metadatos (obligatoria)
| Rango BCQ | ICP | Trigger | Stakeholder | Decision | Riesgo | Producto | Surface | CTA | Estado epistemologico |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| BCQ-0001-BCQ-0025 | H01,H02 | TRG-001..004 | STK-002/003/004 | reconocer/diagnosticar | operativo | KPR-01 | SFC-01 | CTA-01 | INFERENCE |
| BCQ-0026-BCQ-0050 | H01,H02 | TRG-001..004 | STK-002/003/004 | reconocer/diagnosticar | operativo | KPR-02 | SFC-02 | CTA-01 | INFERENCE |
| BCQ-0051-BCQ-0075 | H01,H02 | TRG-005..008 | STK-004/009/013 | priorizar/invertir | estrategico | KPR-03 | SFC-02 | CTA-02 | INFERENCE |
| BCQ-0076-BCQ-0100 | H01,H02 | TRG-005..008 | STK-004/009/013 | priorizar/invertir | estrategico | KPR-04 | SFC-03 | CTA-02 | INFERENCE |
| BCQ-0101-BCQ-0125 | H01,H02 | TRG-009..012 | STK-008/009/010/013 | comparar/justificar/aprobar | financiero/regulatorio/contractual | KPR-05 | SFC-03 | CTA-03 | PARTIAL |
| BCQ-0126-BCQ-0150 | H01,H02 | TRG-009..012 | STK-008/009/010/013 | comparar/justificar/aprobar | financiero/regulatorio/contractual | KPR-06 | SFC-04 | CTA-03 | PARTIAL |
| BCQ-0151-BCQ-0175 | H01,H02 | TRG-013..016 | STK-003/012/018 | diseñar/ejecutar/controlar | tecnico/ejecucion | KPR-07 | SFC-05 | CTA-04 | PARTIAL |
| BCQ-0176-BCQ-0200 | H01,H02 | TRG-013..016 | STK-003/012/018 | diseñar/ejecutar/controlar | tecnico/ejecucion | KPR-08 | SFC-05 | CTA-04 | PARTIAL |
| BCQ-0201-BCQ-0225 | H01,H02,H04 | TRG-010/013/014 | STK-004/008/011/013 | validar evidencia/activar siguiente paso | confianza/comercial | KPR-09 | SFC-06 | CTA-05 | HYPOTHESIS |
| BCQ-0226-BCQ-0250 | H01,H02,H04 | TRG-010/013/014 | STK-004/008/011/013 | validar evidencia/activar siguiente paso | confianza/comercial | KPR-10 | SFC-06 | CTA-06 | HYPOTHESIS |
| BCQ-0251-BCQ-0275 | H01,H02,H04,H05 | TRG-005/013/015 | STK-004/005/018 | medir/escalar/aprender | adopcion/expansion | KPR-11 | SFC-07 | CTA-07 | HYPOTHESIS |
| BCQ-0276-BCQ-0300 | H01,H02,H04,H05 | TRG-005/013/015 | STK-004/005/018 | medir/escalar/aprender | adopcion/expansion | KPR-12 | SFC-08 | CTA-08 | HYPOTHESIS |
Regla: cada BCQ hereda metadatos por rango; no se permiten campos nulos.

## 9) Auditoría de cobertura estratégica
| Dimensión | 300 preguntas | Top 100 | Hallazgo |
| --- | --- | --- | --- |
| Dominio | Estrategico: 50; Expansion-Learning: 50; Operativo: 50; Regulatorio-Financiero: 50; Tecnico-Ejecucion: 50; Trust-GoToMarket: 50 | Estrategico: 19; Expansion-Learning: 5; Operativo: 22; Regulatorio-Financiero: 21; Tecnico-Ejecucion: 19; Trust-GoToMarket: 14 | Balance estratégico aceptable; no concentración extrema en un solo dominio. |
| Buyer Journey | Awareness: 50; Consideration: 70; Evaluation/Decision: 80; Execution/Expansion: 100 | Awareness: 22; Consideration: 30; Evaluation/Decision: 29; Execution/Expansion: 19 | Top 100 cubre desde awareness hasta ejecución; se evita sesgo solo temprano. |
| Tipo de decisión | comparar/justificar/aprobar: 50; diseñar/ejecutar/controlar: 50; medir/escalar/aprender: 50; priorizar/invertir: 50; reconocer/diagnosticar: 50; validar evidencia/activar siguiente paso: 50 | comparar/justificar/aprobar: 21; diseñar/ejecutar/controlar: 19; medir/escalar/aprender: 5; priorizar/invertir: 19; reconocer/diagnosticar: 22; validar evidencia/activar siguiente paso: 14 | Se preserva continuidad diagnóstica, defensiva y de ejecución. |
| Familia de producto (Top100) | n/a | KPR-01: 10; KPR-02: 12; KPR-03: 11; KPR-04: 8; KPR-05: 12; KPR-06: 9; KPR-07: 10; KPR-08: 9; KPR-09: 6; KPR-10: 8; KPR-11: 3; KPR-12: 2 | Evita backlog dominado por artículos; prioriza trust, financial y diagnostic. |
| Surface/CTA (Top100) | n/a | Surfaces: SFC-01: 13, SFC-02: 18, SFC-03: 21, SFC-04: 14, SFC-05: 15, SFC-06: 10, SFC-07: 6, SFC-08: 3 / CTA: CTA-01: 22, CTA-02: 19, CTA-03: 21, CTA-04: 19, CTA-05: 6, CTA-06: 8, CTA-07: 3, CTA-08: 2 | Conexión comercial explícita en toda la priorización. |
Hallazgos críticos:
- Sobrerrepresentación inicial operativa corregida en Top 100 con inclusión de decisión financiera/comité/trust.
- Dependencia H01/H02 se mantiene por foco estratégico, con extensión H04/H05 en bloques de trust y expansión.
- Riesgo de preguntas tempranas sin conexión comercial mitigado vía CTA y producto por cada pregunta prioritaria.

## 10) Top 100 final y justificable
Clasificación aprobada: P0 (20), P1 (30), P2 (50).

| Tier | ID | Priority Score | Factores (I/U/G/M/A) | Confianza | Decision | ICP | Evidencia requerida | Producto | Surface | CTA | Razón de inclusión |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P0 | BCQ-0001 | 4.6 | 5/5/4/4/4 | media-alta | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0004 | 4.6 | 5/5/4/4/4 | media-alta | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0011 | 4.6 | 5/5/4/4/4 | media-alta | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0012 | 4.6 | 5/5/4/4/4 | media-alta | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0023 | 4.6 | 5/5/4/4/4 | media-alta | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0029 | 4.6 | 5/5/4/4/4 | media-alta | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-01 | CTA-01 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0048 | 4.6 | 5/5/4/4/4 | media-alta | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0050 | 4.6 | 5/5/4/4/4 | media-alta | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0053 | 4.6 | 5/5/4/4/4 | media-alta | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0058 | 4.6 | 5/5/4/4/4 | media-alta | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0062 | 4.6 | 5/5/4/4/4 | media-alta | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0073 | 4.6 | 5/5/4/4/4 | media-alta | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-03 | CTA-02 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0101 | 4.7 | 5/5/4/5/4 | media-alta | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0106 | 4.7 | 5/5/4/5/4 | media-alta | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0112 | 4.7 | 5/5/4/5/4 | media-alta | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0120 | 4.7 | 5/5/4/5/4 | media-alta | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0135 | 4.7 | 5/5/4/5/4 | media-alta | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0154 | 4.7 | 5/5/4/5/4 | media-alta | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-04 | CTA-04 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0213 | 4.8 | 5/5/5/4/4 | media | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-09 | SFC-06 | CTA-05 | fundacional para mover decisión con alta urgencia y alto impacto |
| P0 | BCQ-0243 | 4.8 | 5/5/5/4/4 | media | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-10 | SFC-07 | CTA-06 | fundacional para mover decisión con alta urgencia y alto impacto |
| P1 | BCQ-0003 | 3.7 | 4/4/3/4/3 | media | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0009 | 3.7 | 4/4/3/4/3 | media | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0016 | 3.7 | 4/4/3/4/3 | media | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0021 | 3.7 | 4/4/3/4/3 | media | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0024 | 3.7 | 4/4/3/4/3 | media | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-01 | SFC-01 | CTA-01 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0034 | 3.7 | 4/4/3/4/3 | media | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0037 | 3.7 | 4/4/3/4/3 | media | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0046 | 3.7 | 4/4/3/4/3 | media | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0059 | 3.7 | 4/4/3/4/3 | media | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0068 | 3.7 | 4/4/3/4/3 | media | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0070 | 3.7 | 4/4/3/4/3 | media | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0076 | 3.7 | 4/4/3/4/3 | media | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-04 | SFC-03 | CTA-02 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0084 | 3.7 | 4/4/3/4/3 | media | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-04 | SFC-03 | CTA-02 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0095 | 3.7 | 4/4/3/4/3 | media | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-04 | SFC-03 | CTA-02 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0105 | 3.8 | 4/4/3/5/3 | media | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0115 | 3.8 | 4/4/3/5/3 | media | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0118 | 3.8 | 4/4/3/5/3 | media | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0126 | 3.8 | 4/4/3/5/3 | media | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0131 | 3.8 | 4/4/3/5/3 | media | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0139 | 3.8 | 4/4/3/5/3 | media | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0147 | 3.8 | 4/4/3/5/3 | media | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0157 | 3.8 | 4/4/3/5/3 | media | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-04 | CTA-04 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0166 | 3.8 | 4/4/3/5/3 | media | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-05 | CTA-04 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0172 | 3.7 | 4/4/3/4/3 | media | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-05 | CTA-04 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0175 | 3.7 | 4/4/3/4/3 | media | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-05 | CTA-04 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0180 | 3.7 | 4/4/3/4/3 | media | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0195 | 3.7 | 4/4/3/4/3 | media | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0200 | 3.9 | 4/4/4/4/3 | media | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0231 | 3.9 | 4/4/4/4/3 | media | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-10 | SFC-06 | CTA-06 | alta oportunidad con buena defendibilidad y reutilización |
| P1 | BCQ-0249 | 3.9 | 4/4/4/4/3 | media | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-10 | SFC-07 | CTA-06 | alta oportunidad con buena defendibilidad y reutilización |
| P2 | BCQ-0027 | 3 | 3/3/3/3/3 | media-baja | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-01 | CTA-01 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0030 | 3 | 3/3/3/3/3 | media-baja | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-01 | CTA-01 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0039 | 3 | 3/3/3/3/3 | media-baja | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0041 | 3 | 3/3/3/3/3 | media-baja | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0044 | 3 | 3/3/3/3/3 | media-baja | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0049 | 3 | 3/3/3/3/3 | media-baja | reconocer/diagnosticar | H01,H02 | logs, incidentes, MTTR | KPR-02 | SFC-02 | CTA-01 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0056 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0063 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0065 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-02 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0071 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-03 | SFC-03 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0078 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-04 | SFC-03 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0081 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-04 | SFC-03 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0087 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-04 | SFC-03 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0091 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-04 | SFC-03 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0097 | 3 | 3/3/3/3/3 | media-baja | priorizar/invertir | H01,H02 | forecast, capacidad, benchmark | KPR-04 | SFC-03 | CTA-02 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0103 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0108 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0114 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0117 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-03 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0123 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-05 | SFC-04 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0129 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0134 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0142 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0149 | 3.1 | 3/3/3/4/3 | media-baja | comparar/justificar/aprobar | H01,H02 | ROI/TCO, contrato, compliance | KPR-06 | SFC-04 | CTA-03 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0152 | 3.1 | 3/3/3/4/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-04 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0159 | 3.1 | 3/3/3/4/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-04 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0163 | 3.1 | 3/3/3/4/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0169 | 3.1 | 3/3/3/4/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0171 | 3 | 3/3/3/3/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-07 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0178 | 3 | 3/3/3/3/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0183 | 3 | 3/3/3/3/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0187 | 3 | 3/3/3/3/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0190 | 3 | 3/3/3/3/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0193 | 3 | 3/3/3/3/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0197 | 3 | 3/3/3/3/3 | media-baja | diseñar/ejecutar/controlar | H01,H02 | planos, pruebas FAT/SAT, hitos | KPR-08 | SFC-05 | CTA-04 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0204 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-09 | SFC-06 | CTA-05 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0210 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-09 | SFC-06 | CTA-05 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0216 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-09 | SFC-06 | CTA-05 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0222 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-09 | SFC-06 | CTA-05 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0224 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-09 | SFC-06 | CTA-05 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0229 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-10 | SFC-06 | CTA-06 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0233 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-10 | SFC-06 | CTA-06 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0238 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-10 | SFC-06 | CTA-06 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0241 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-10 | SFC-07 | CTA-06 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0250 | 3.2 | 3/3/4/3/3 | media-baja | validar evidencia/activar siguiente paso | H01,H02,H04 | evidence pack, permisos, comparables | KPR-10 | SFC-07 | CTA-06 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0262 | 3.2 | 3/3/4/3/3 | media-baja | medir/escalar/aprender | H01,H02,H04,H05 | KPI post, lecciones, NPS | KPR-11 | SFC-07 | CTA-07 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0269 | 3.2 | 3/3/4/3/3 | media-baja | medir/escalar/aprender | H01,H02,H04,H05 | KPI post, lecciones, NPS | KPR-11 | SFC-07 | CTA-07 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0273 | 3.2 | 3/3/4/3/3 | media-baja | medir/escalar/aprender | H01,H02,H04,H05 | KPI post, lecciones, NPS | KPR-11 | SFC-08 | CTA-07 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0284 | 3.2 | 3/3/4/3/3 | media-baja | medir/escalar/aprender | H01,H02,H04,H05 | KPI post, lecciones, NPS | KPR-12 | SFC-08 | CTA-08 | expansión validada con valor compuesto y menor urgencia relativa |
| P2 | BCQ-0298 | 3.2 | 3/3/4/3/3 | media-baja | medir/escalar/aprender | H01,H02,H04,H05 | KPI post, lecciones, NPS | KPR-12 | SFC-08 | CTA-08 | expansión validada con valor compuesto y menor urgencia relativa |

### Sensibilidad del Top 100
- Si la frecuencia estimada cae en bloques operativos (BCQ-0001..0050), subirían preguntas financieras/comité (BCQ-0111..0140).
- Preguntas dependientes de evidencia no disponible: BCQ-0127, BCQ-0216, BCQ-0240; quedan con bandera de validación externa.
- Alto valor con baja defendibilidad: BCQ-0192, BCQ-0230, BCQ-0298; requieren evidencia comparativa adicional.
- Potencial tráfico sin pipeline: BCQ-0226, BCQ-0290, BCQ-0292; amarradas a CTA-01/03/10 para evitar fuga.
- Alto potencial multi-producto/surface: BCQ-0011, BCQ-0112, BCQ-0120, BCQ-0213, BCQ-0231, BCQ-0243, BCQ-0269.

## 11) Preguntas semilla para Knowledge Product Alpha (5-7)
| ID | Pregunta semilla | Motivo de selección | Activo Alpha principal |
| --- | --- | --- | --- |
| BCQ-0001 | Â¿QuÃ© operaciÃ³n crÃ­tica puede detenerse hoy sin aviso? | alta frecuencia y rápida activación comercial | Activo 1 Diagnóstico |
| BCQ-0011 | Â¿QuÃ© costo oculto genera cada paro corto? | alta frecuencia y rápida activación comercial | Activo 1 Diagnóstico |
| BCQ-0058 | Â¿QuÃ© decisiÃ³n de capacidad debe tomarse antes del siguiente capex? | decisión de capacidad con urgencia presupuestal | Activo 1 Diagnóstico |
| BCQ-0112 | Â¿QuÃ© variable econÃ³mica cambia mÃ¡s el payback? | traduce riesgo en impacto económico defendible | Activo 2 Financiero |
| BCQ-0120 | Â¿QuÃ© evidencia convierte opiniÃ³n en aprobaciÃ³n? | convierte opinión en aprobación de comité | Activo 3 Ejecutivo/Trust |
| BCQ-0213 | Â¿QuÃ© brecha de evidencia frena aprobaciÃ³n hoy? | detecta brecha de evidencia bloqueante | Activo 3 Ejecutivo/Trust |
| BCQ-0243 | Â¿QuÃ© pregunta identifica veto silencioso? | detecta veto silencioso antes de pérdida | Activo 3 Ejecutivo/Trust |

## 12) Validación del Knowledge Product Backlog (KPR-01..KPR-12)
| KPR | Preguntas que agrupa | Decisión que facilita | ICP | Stakeholder | Evidencia mínima | Formato recomendado | Surface | CTA | Métrica | Esfuerzo | Riesgo | Owner | Dependencias | Criterio de aceptación |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
Orden de prioridad recomendado aplicado: Trust -> Financial -> Diagnostic -> Decision -> Risk -> Executive -> Intelligence -> AI (AI diferido).

## 13) Knowledge Product Alpha recomendado (3 activos + derivados)
### Activo Alpha 1 - Diagnóstico: Risk and Readiness Scorecard
- Preguntas núcleo: BCQ-0001, BCQ-0011, BCQ-0058
- Derivados: checklist express, benchmark breve, script de discovery.
- Reutilización: KPR-01 + KPR-02 + CTA-01 en SFC-01/SFC-02.
### Activo Alpha 2 - Financiero: TCO and Downtime Impact Model
- Preguntas núcleo: BCQ-0112, BCQ-0115, BCQ-0118
- Derivados: plantilla de sensibilidad, anexo ROI para propuesta.
- Reutilización: KPR-04 + CTA-02/CTA-03 en SFC-09/SFC-05.
### Activo Alpha 3 - Ejecutivo/Trust: Committee Decision Memo
- Preguntas núcleo: BCQ-0120, BCQ-0213, BCQ-0243
- Derivados: checklist de aprobación, matriz de objeciones, one-page de riesgo.
- Reutilización: KPR-06 + KPR-09 + CTA-03/CTA-05 en SFC-05/SFC-06.
Selección final: 6 preguntas semilla activan 3 activos con valor compuesto y esfuerzo ejecutable.

## 14) Regla operativa sobre las 100 preguntas
Una misma pregunta puede originar múltiples formatos sin duplicar gobierno: respuesta breve, artículo, checklist, calculadora, diagnóstico, video, caso, benchmark, FAQ, respuesta IA, sección de propuesta y conversación comercial.
La unidad de gobierno es pregunta + decisión, no formato.

## 15) Gaps y validaciones pendientes para cierre total
- Validar frecuencia real de preguntas con CRM/Search Console antes de ajustar pesos de prioridad.
- Completar permisos de evidencia para BCQ vinculadas a comparables públicos (GAP-07).
- Confirmar sensibilidad financiera con datos reales de proyectos (GAP-04).
- Verificar que CTA-10 no se use como CTA principal en etapas tempranas sin diagnóstico.

## 16) Criterio de cierre BCE V1
- 300 preguntas canónicas válidas: cumplido.
- Top 100 justificable y no secuencial: cumplido.
- P0/P1/P2 definidos (20/30/50): cumplido.
- Preguntas semilla Alpha seleccionadas: cumplido.
- Conexión pregunta -> decisión -> producto -> surface -> CTA: cumplido para Top 100.
- Estado BCE: listo para congelar como fuente y pasar a producción de Knowledge Products.

