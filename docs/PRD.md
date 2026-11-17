# Product Requirements Document (PRD) — SEP-LLM-Behavior-Benchmark

- **Proyecto:** `lankamar/SEP-LLM-Behavior-Benchmark`
- **Versión:** `2.0.0`
- **Autor:** Lic. Marcelo Omar Lancry Kamycki (`ORCID: 0009-0008-8196-6291`)

---

## Requerimientos Funcionales (RF)

| ID | Requerimiento Funcional | Criterio de Aceptación |
| :--- | :--- | :--- |
| **RF-01** | **Estructura Invariante en 4 Fases (SEP):** Toda respuesta evaluada debe descomponerse en Análisis, Planificación, Ejecución y Retroalimentación. | Verificable mediante la rúbrica en `protocol/evaluation_rubric.md`. |
| **RF-02** | **Suite de 4 Casos Multidominio + Adversarial:** Prompts estandarizados en `prompts/` cubriendo clínica, programación, educación y teoría/seguridad. | Archivos `case1_clinical.md` a `case4_theory.md` disponibles y ejecutables. |
| **RF-03** | **Registro Reproducible de Sesiones:** Toda corrida debe registrarse con modelo, fecha y salida cruda usando `sessions/session_template.md`. | Plantillas presentes y trazables con `docs/reproducibility.md`. |
| **RF-04** | **Transparencia Epistémica:** Separar explícitamente artefactos verificados in-silico de ensayos futuros con grupo control (`N > 100`). | Declarado en `context/preprint/sep_scientific_paper.md` y en el paper PDF v2.0.0. |
