# Market Knowledge Map V1

## Ficha de Trazabilidad
- ID: DOC-047
- Estado: 🟢 Aprobado
- Tipo: Market Knowledge Map
- Objetivo: Mapear el conocimiento del mercado de infraestructura crítica desde primeros principios, centrado en consecuencias del fallo, decisiones del comprador, riesgos y oportunidades.
- Entradas:
  - DOC-012 (03_MODELO_COMERCIAL/Decision_Architecture.md)
  - DOC-017 (04_TRUST/Trust_Architecture.md)
  - DOC-025 (06_CONOCIMIENTO/Knowledge_Program.md)
  - DOC-026 (06_CONOCIMIENTO/Taxonomia.md)
- Salidas:
  - Dominios del mercado
  - Buyer Curiosity Graph inicial
  - Decision Graph inicial
  - Opportunity Graph inicial
  - Knowledge Flywheel inicial
- Dependencias:
  - DOC-006 (02_VERDAD_COMERCIAL/000_PREGUNTAS_ABIERTAS.md)
  - DOC-045 (99_META/SYSTEM_MAP.md)
- Documentos consumidos:
  - evidencia publica de `picc.com.mx`
  - hipótesis estratégicas aprobadas en conversación
- Documentos generados:
  - base para Market Behavior Map V1
- Responsable: Dirección + Producto + Comercial
- Fecha: 2026-07-15
- Criterios de aceptación:
  - El mapa expresa el mercado en lenguaje neutral
  - Cada nodo está vinculado a problemas, decisiones, riesgos y evidencias
  - No depende del nombre PICC para existir

## Tesis central
El mercado de infraestructura crítica se organiza por consecuencias del fallo, no por catálogo de servicios.

## Dominios de mercado
- Infraestructura de cómputo y datos.
- Operación industrial continua.
- Infraestructura logística de alta continuidad.
- Infraestructura sanitaria crítica.
- Infraestructura financiera/transaccional.
- Infraestructura de telecom y conectividad.
- Energía y utilidades críticas.
- Infraestructura pública esencial.
- Infraestructura corporativa de misión crítica.

## Problemas, decisiones y riesgos
- Cada dominio debe descomponerse en problemas visibles, invisibles, emergentes y no reconocidos.
- Cada comprador debe tomar decisiones sobre criticidad, resiliencia, inversión, riesgo y proveedor.
- Cada decisión se conecta a riesgo de continuidad, reputación, carrera, cumplimiento, tiempo y costo.

## Knowledge Graph mínimo
Problema -> Pregunta -> Decisión -> Riesgo -> Evidencia -> Producto de conocimiento -> Servicio PICC

## Reglas
- Ningún nodo entra si no puede expresarse en lenguaje neutral de mercado.
- No se modela desde la oferta de PICC, sino desde el comportamiento del mercado.
- Este artefacto alimenta el siguiente sprint: Market Behavior Map V1.
