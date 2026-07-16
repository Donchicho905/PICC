# AI Execution Contract

## Ficha de trazabilidad
- ID: DOC-052
- Estado: Aprobado para uso operativo
- Tipo: Contrato de ejecución IA
- Objetivo: Definir las reglas inmutables y operativas para que cualquier IA competente continúe PICC NEXT sin romper principios, contexto ni gobernanza.
- Alcance: Todo el repositorio PICC.
- Responsable: Dirección + PMO + Arquitectura de conocimiento
- Fecha: 2026-07-15

---

## 1. Misión del repositorio

PICC NEXT existe para convertir incertidumbre comercial en decisiones defendibles, proyectos ejecutables, entregables verificables y aprendizaje acumulativo que incremente ventaja competitiva en infraestructura crítica.

La misión operativa de cualquier IA en este repositorio es:
1. Reducir incertidumbre de compra.
2. Mejorar la calidad de decisión del comprador.
3. Aumentar la conversión a reunión, propuesta y proyecto.
4. Preservar y reutilizar evidencia verificable.
5. No romper principios ya aprobados.

---

## 2. Principios inmutables

1. No reabrir arquitecturas congeladas.
2. No crear nuevos modelos conceptuales sin aprobación humana explícita.
3. No inventar datos, claims o evidencia.
4. No confundir documentación con producto.
5. No optimizar CTR si no mejora una decisión real.
6. No sacrificar trazabilidad por velocidad.
7. No mezclar trabajo externo con el alcance del sprint actual.
8. No modificar archivos fuera del alcance autorizado.
9. No introducir complejidad que no aumente valor.
10. No crear artefactos sin propósito único y verificable.

---

## 3. Arquitectura congelada

La IA debe tratar como congelado lo siguiente:
- SHDLS V1.0
- Growth System V1
- Buyer System V1
- Discovery Intelligence System V1
- Demand Engine V1
- Buyer Curiosity Engine V1
- Market Behavior Map V1
- Buyer Curiosity Map V1
- Knowledge Product Portfolio V1 conceptual
- Decision Operating System (DOS) como hipotesis estrategica prometedora, no doctrina transversal ni arquitectura validada de OLYMPUS

La IA puede leerlos, usar sus salidas y construir sobre ellos. No puede redefinirlos por preferencia.

---

## 4. Qué puede evolucionar

Puede evolucionar, con disciplina y trazabilidad:
1. Implementaciones concretas.
2. Activos de evidencia.
3. Knowledge Products derivados.
4. Surfaces de experiencia.
5. Flujos de captura y calificación.
6. Módulos operativos que no alteren principios congelados.
7. Métricas y telemetría operacional.
8. Documentación de handoff y boot para nuevas IAs.

---

## 5. Qué requiere aprobación humana

1. Cualquier cambio de arquitectura congelada.
2. Cualquier nuevo modelo conceptual.
3. Cualquier cambio de alcance que afecte estrategia.
4. Cualquier claim público no sustentado por evidencia aprobada.
5. Cualquier cambio de prioridad entre sprints mayores.
6. Cualquier modificación de reglas de Git fuera de este contrato.
7. Cualquier publicación externa con riesgo reputacional o legal.

---

## 6. Reglas de evidencia

1. Cada afirmación relevante debe tener fuente, trazabilidad o estado epistemológico explícito.
2. Si la evidencia es parcial, debe decirse.
3. Si una cifra no está verificada, no se presenta como hecho.
4. Las referencias deben apuntar a documentos del repositorio o a evidencia verificada.
5. La evidencia no se reescribe para que encaje con una conclusión.
6. Los assets de evidencia deben distinguir entre hecho, inferencia e hipótesis.

---

## 7. Reglas de investigación

1. Investigar solo cuando la pregunta esté ligada a una decisión real.
2. Formular hipótesis antes de expandir trabajo.
3. No abrir líneas de investigación sin salida operativa.
4. Documentar vacíos de contexto en lugar de rellenarlos con suposiciones.
5. Si un hallazgo no cambia decisión, no es prioridad.
6. Toda investigación debe terminar en una de tres salidas: evidencia, descarte o hipótesis abierta.

---

## 8. Reglas de Git

1. Usar siempre el repositorio PICC como raíz operativa.
2. No usar Git del repositorio padre para staging, commit, restore, stash o reset.
3. No usar `git add .` ni `git add -A`.
4. No usar `git commit -a`.
5. No usar `git stash`.
6. No usar `git reset --hard`.
7. No usar `git clean`.
8. Agregar al staging solo rutas explícitas dentro de PICC.
9. Si aparecen archivos inesperados dentro de PICC, detener y reportar.
10. No declarar limpio el repositorio padre; solo reportar el estado de PICC.

---

## 9. Reglas de commits

1. Un commit debe tener intención única.
2. Un commit no debe mezclar infraestructura, handoff y contenido no relacionado.
3. Los mensajes deben ser descriptivos y accionables.
4. Los commits deben poder auditarse por archivo y propósito.
5. No hacer commits por conveniencia si el trabajo no está validado.
6. Si un cambio necesita revisión crítica antes de commit, detener.

---

## 10. Reglas de handoff

1. Todo sprint debe dejar claro qué leer primero.
2. El handoff debe indicar qué está congelado, qué está activo y cuál es el siguiente paso autorizado.
3. El handoff debe distinguir entre contexto estable y trabajo en curso.
4. El siguiente agente debe poder continuar sin depender de memoria externa.
5. El handoff debe decir qué NO tocar.

---

## 11. Reglas de documentación

1. Cada documento debe tener un propósito único.
2. No duplicar contenido entre artefactos sin razón de gobierno.
3. No crear documentos “por completitud” si no cambian la ejecución.
4. Mantener una sola versión canónica por dominio.
5. La documentación debe ser operacional, no ornamental.
6. Si un documento existe, debe poder usarse para decidir o ejecutar.

---

## 12. Definition of Ready

Una tarea está lista cuando:
1. Tiene objetivo explícito.
2. Tiene alcance delimitado.
3. Tiene restricciones claras.
4. Tiene documentos fuente identificados.
5. Tiene criterio de éxito verificable.
6. Tiene repositorio y ruta de trabajo definidos.
7. No depende de supuestos no documentados sin marcar.

---

## 13. Definition of Done

Una tarea está terminada cuando:
1. El artefacto queda creado o actualizado.
2. La intención queda trazable.
3. La validación de calidad pasa.
4. El estado de Git es correcto.
5. El handoff queda inequívoco.
6. Los riesgos y vacíos quedan visibles.
7. El siguiente paso está explícito.

---

## 14. Criterios para detener la ejecución y pedir intervención humana

Detener inmediatamente si ocurre cualquiera de estos casos:
1. Se detecta cambio de arquitectura congelada.
2. Aparece un archivo inesperado dentro del alcance PICC.
3. Hay ambigüedad sobre el repositorio raíz o scope real.
4. Un dato crítico no puede verificarse.
5. El trabajo requiere una decisión estratégica no documentada.
6. Un cambio puede afectar legal, reputación o claims públicos.
7. La evidencia disponible contradice la hipótesis central.
8. Una tarea depende de memoria conversacional no institucionalizada.

---

## 15. Errores que nunca debe cometer una IA

1. Inventar evidencia.
2. Reabrir principios congelados.
3. Cambiar arquitectura por estilo.
4. Crear capas nuevas para resolver un problema operativo.
5. Mezclar repositorios o scopes.
6. Hacer commits no auditables.
7. Usar claims sin permiso o sin respaldo.
8. Confundir output documental con valor comercial.
9. Ocultar incertidumbre.
10. Continuar cuando un hallazgo exige pausa humana.

---

## 16. Jerarquía de decisión

Orden de prioridad para cualquier IA:
1. Seguridad del repositorio y del scope.
2. Fidelidad a principios congelados.
3. Veracidad de la evidencia.
4. Trazabilidad de cambios.
5. Utilidad comercial del output.
6. Velocidad de entrega.

---

## 17. Cláusula operativa final

Si una instrucción conversa con una decisión ya documentada, prevalece el documento aprobado.
Si una instrucción nueva contradice una arquitectura congelada, la IA debe detenerse y solicitar intervención humana.
Si el repositorio no permite resolver el problema sin romper principios, no se improvisa una nueva arquitectura.
