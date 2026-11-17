# Matriz Teleológica «Con Propósito» — SEP-LLM-Behavior-Benchmark

- **Proyecto:** `lankamar/SEP-LLM-Behavior-Benchmark`
- **Autor:** Lic. Marcelo Omar Lancry Kamycki (`ORCID: 0009-0008-8196-6291`)
- **Filiación:** Hospital de Clínicas «José de San Martín», Universidad de Buenos Aires (UBA) · Centro de Innovación en Tecnología y Pedagogía (CITEP–UBA)
- **DOI Zenodo:** `10.5281/zenodo.24269181` (Todas las versiones) · `10.5281/zenodo.24269182` (Versión 2.0.0)

---

## 1. Dolores que cubre (Planteamiento del Problema)
1. **Alucinaciones no advertidas en dominios críticos:** Los LLMs producen respuestas fluidas pero factualmente erróneas sin señales de advertencia (Ji et al., 2023; Maynez et al., 2020).
2. **Ausencia de trazabilidad experimental reproducible:** El prompting artesanal no registra parámetros, semillas ni rúbricas comparables entre modelos y sesiones (Open Science Collaboration, 2015).
3. **Falta de evaluación bajo estrés y escenarios adversariales:** Pocos protocolos evalúan conjuntamente triaje clínico, refactorización de código, docencia sanitaria y resistencia ante solicitudes maliciosas.

## 2. Justificación, Propósito, Misión y Visión
- **Justificación:** En salud y educación superior se exigen procesos auditables, seguros y reproducibles bajo estándares de ciencia abierta y Ciencia del Diseño (Peffers et al., 2007).
- **Propósito:** Convertir la interacción cotidiana con LLMs en un objeto científico medible, criticable y replicable.
- **Misión:** Proveer un protocolo de cuatro fases (Análisis, Planificación, Ejecución y Telemetría/Feedback) inspirado en Deming (1986) y la Ingeniería del Caos (Basiri et al., 2016), acompañado de prompts multidominio y rúbricas de evaluación.
- **Visión:** Consolidar un banco de pruebas abierto de referencia para comparar la estabilidad y seguridad de distintos LLMs en español e inglés.

## 3. Alcance, Objetivos y Metas
- **Alcance:** Incluye especificaciones en `protocol/`, 4 casos de prueba en `prompts/`, trazas históricas en `context/`, plantillas en `sessions/` y monografía APA 7 en `paper/`. Excluye datos clínicos reales (Ley N.° 25.326).
- **Objetivo General:** Evaluar la estabilidad, transferibilidad y sinergia con guardrails del protocolo SEP en escenarios multidominio.
- **Metas:** Replicabilidad completa de los 4 casos, trazabilidad bajo APA 7.ª edición e indexación en Zenodo, ORCID y Google Scholar.
