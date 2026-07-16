# PICC NEXT Boot

## Propósito
Este documento permite que una IA nueva entienda PICC NEXT en menos de 10 minutos y continúe trabajo sin romper principios, contexto ni gobernanza.

---

## 1. Qué es PICC NEXT

PICC NEXT es el sistema comercial y de conocimiento de PICC para reducir incertidumbre de compra en infraestructura crítica. Su función no es publicar más, sino ayudar a compradores complejos a decidir mejor, con evidencia verificable, aprendizaje compuesto y activos reutilizables.

---

## 2. Qué problema resuelve

Convierte señales dispersas del mercado en:
1. Hipótesis útiles.
2. Evidencia estructurada.
3. Expedientes de decisión.
4. Propuestas defendibles.
5. Proyectos ejecutables.
6. Casos reutilizables para fortalecer conversion futura.

---

## 3. Estado actual

- SHDLS V1.0 congelado.
- Growth System V1 congelado.
- Buyer System V1 congelado.
- Buyer Curiosity Engine V1 congelado.
- Market Behavior Map V1 congelado.
- Growth MVP V1 aprobado.
- Buyer Curiosity Engine V1 completado y congelado.
- Decision Experience Alpha analizado, pero no implementado.
- Repositorio en fase de consolidación y transferencia operativa.

---

## 4. Componentes congelados

- SHDLS V1.0
- Growth System V1
- Buyer System V1
- Discovery Intelligence System V1
- Demand Engine V1
- Buyer Curiosity Engine V1
- Market Behavior Map V1
- Buyer Curiosity Map V1
- Knowledge Product Portfolio V1 conceptual

---

## 5. Qué leer primero

Orden recomendado de lectura:
1. `00_IMPLEMENTATION_REPORT.md`
2. `99_META/SYSTEM_MAP.md`
3. `99_META/DECISION_HISTORY.md`
4. `99_META/REPOSITORY_RULES.md`
5. `99_META/ARTIFACT_REGISTRY.md`
6. `99_META/CHANGELOG.md`
7. `INDEX.md`
8. `06_CONOCIMIENTO/Buyer_Curiosity_Map.md`
9. `06_CONOCIMIENTO/Market_Behavior_Map.md`
10. `06_CONOCIMIENTO/Knowledge_Product_Alpha.md`
11. `08_IMPLEMENTACION/DECISION_EXPERIENCE_ALPHA.md`
12. `08_IMPLEMENTACION/MVP.md`

---

## 6. Documentos críticos

- `00_IMPLEMENTATION_REPORT.md` — handoff principal y estado actual.
- `99_META/SYSTEM_MAP.md` — mapa sistémico de alto nivel.
- `99_META/REPOSITORY_RULES.md` — reglas permanentes del repositorio.
- `99_META/DECISION_HISTORY.md` — decisiones institucionalizadas.
- `06_CONOCIMIENTO/Buyer_Curiosity_Map.md` — SSOT del universo de preguntas.
- `06_CONOCIMIENTO/Market_Behavior_Map.md` — modelo de comportamiento de mercado.
- `06_CONOCIMIENTO/Knowledge_Product_Alpha.md` — alpha candidates de producto.
- `08_IMPLEMENTACION/MVP.md` — experiencia comercial mínima ejecutable.

---

## 7. Documentos de referencia

- `06_CONOCIMIENTO/BCE_V1_AUDIT_REPORT.md`
- `06_CONOCIMIENTO/BCE_V1_TOP100.md`
- `06_CONOCIMIENTO/Knowledge_Product_Alpha.md`
- `08_IMPLEMENTACION/DECISION_EXPERIENCE_ALPHA.md`
- `04_TRUST/Trust_Architecture.md`
- `04_TRUST/Sistema_de_Evidencia.md`
- `04_TRUST/Biblioteca_de_Evidencia.md`
- `05_PRODUCTO/Capability_Backlog.md`
- `05_PRODUCTO/Product_Roadmap.md`

---

## 8. Sprint actual

Sprint actual de consolidación:
- Convertir el repositorio en autoejecutable para una IA nueva.
- Transferir reglas, límites, estado y handoff sin tocar arquitectura.
- Preparar ejecución autónoma con mínima ambigüedad.

---

## 9. Siguiente objetivo autorizado

Siguiente objetivo conceptual autorizado:
- Continuar desde la consolidación hacia ejecución autónoma de sprints operativos sin reabrir la arquitectura congelada.

Si la IA no está segura del siguiente sprint, debe leer `00_IMPLEMENTATION_REPORT.md` y `99_META/DECISION_HISTORY.md` antes de actuar.

---

## 10. Comandos Git iniciales

Usar siempre la raíz PICC:
```bash
git -C c:\Development\DataManager\agents\projects\PICC status --short
git -C c:\Development\DataManager\agents\projects\PICC branch --show-current
git -C c:\Development\DataManager\agents\projects\PICC rev-parse --show-toplevel
git -C c:\Development\DataManager\agents\projects\PICC rev-parse --short HEAD
git -C c:\Development\DataManager\agents\projects\PICC rev-parse --short origin/feature/picc-next-growth-system
```

Reglas de uso:
- No usar Git del repositorio padre para staging, commit, restore, stash o reset.
- No usar `git add .` ni `git add -A`.
- No usar `git commit -a`.
- Agregar solo rutas explícitas dentro de PICC.

---

## 11. Checklist de pre-flight

1. Confirmar raíz del repositorio PICC.
2. Confirmar rama actual.
3. Confirmar HEAD local y remoto.
4. Revisar `git status --short`.
5. Verificar que no existan archivos inesperados dentro de PICC.
6. Leer `00_IMPLEMENTATION_REPORT.md`.
7. Leer `99_META/SYSTEM_MAP.md`.
8. Leer `99_META/DECISION_HISTORY.md`.
9. Leer `99_META/REPOSITORY_RULES.md`.
10. Confirmar el sprint autorizado antes de ejecutar.

---

## 12. Qué no hacer

- No reabrir SHDLS.
- No redefinir Buyer System.
- No ampliar BCE.
- No inventar nuevas preguntas.
- No crear nuevos frameworks.
- No modificar arquitectura congelada.
- No mezclar trabajo externo con PICC.
- No asumir contexto que no esté documentado.

---

## 13. Cómo pensar el repositorio

PICC NEXT no es un conjunto de páginas. Es un sistema que convierte señales de mercado en decisiones, proyectos, evidencia y ventaja acumulativa.

Si una tarea no mejora esa cadena, probablemente no es prioritaria.
