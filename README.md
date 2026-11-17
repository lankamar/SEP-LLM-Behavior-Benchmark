# Systematic Excellence Protocol (SEP-LLM-Behavior-Benchmark)
### *Evaluación Multidominio, Ingeniería del Caos y Telemetría Reproducible en Grandes Modelos de Lenguaje*

[![Zenodo DOI (All Versions)](https://zenodo.org/badge/DOI/10.5281/zenodo.24269181.svg)](https://doi.org/10.5281/zenodo.24269181)
[![Zenodo DOI v2.0.0](https://zenodo.org/badge/DOI/10.5281/zenodo.24269182.svg)](https://doi.org/10.5281/zenodo.24269182)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0008--8196--6291-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0008-8196-6291)
[![Google Scholar](https://img.shields.io/badge/Google_Scholar-ERLQOWcAAAAJ-4285F4?logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?user=ERLQOWcAAAAJ&hl=es)
[![APA 7th Edition](https://img.shields.io/badge/Standard-APA_7th_Edition-blue.svg)](https://apastyle.apa.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

- **Autor:** Lic. Marcelo Omar Lancry Kamycki
- **Filiación Institucional:** Hospital de Clínicas «José de San Martín», Universidad de Buenos Aires (UBA) · Centro de Innovación en Tecnología y Pedagogía (CITEP–UBA)
- **Identificador Persistente de Investigador (ORCID):** [https://orcid.org/0009-0008-8196-6291](https://orcid.org/0009-0008-8196-6291)
- **Perfil en Google Académico:** [https://scholar.google.com/citations?user=ERLQOWcAAAAJ&hl=es](https://scholar.google.com/citations?user=ERLQOWcAAAAJ&hl=es)
- **Sitio Institucional / Portfolio:** [https://lankamar.github.io/](https://lankamar.github.io/)
- **DOI de Registro Científico en Zenodo (Todas las versiones):** [https://doi.org/10.5281/zenodo.24269181](https://doi.org/10.5281/zenodo.24269181)
- **DOI Versión 2.0.0 (APA 7.ª ed. Verificada):** [https://doi.org/10.5281/zenodo.24269182](https://doi.org/10.5281/zenodo.24269182)
- **Paper Completo en PDF (Norma APA 7.ª ed.):** [paper/Kamycki_2026_SEP_LLM_Behavior_Benchmark.pdf](paper/Kamycki_2026_SEP_LLM_Behavior_Benchmark.pdf)
- **Encuadre Metodológico:** Investigación en Ciencia del Diseño (*Design Science Research Methodology* — DSRM; Peffers et al., 2007).

---

## Resumen

El despliegue de grandes modelos de lenguaje (LLMs) en dominios de alta criticidad —como el triaje clínico, la ingeniería de software, la docencia en seguridad del paciente y el análisis teórico de sistemas resilientes— enfrenta la recurrencia de alucinaciones no advertidas (Ji et al., 2023; Maynez et al., 2020) y la ausencia de trazabilidad experimental reproducible (Open Science Collaboration, 2015). Enmarcado en la Metodología de Investigación en Ciencia del Diseño (Peffers et al., 2007), este repositorio documenta el diseño, la arquitectura de evaluación y las pruebas de estrés del **Systematic Excellence Protocol (SEP)** y su banco de pruebas abierto **SEP-LLM-Behavior-Benchmark**. Inspirado en el ciclo de mejora continua Planificar-Hacer-Verificar-Actuar (Deming, 1986), el aprendizaje por refuerzo (Sutton & Barto, 2018) y los principios de la Ingeniería del Caos (*Chaos Engineering*; Basiri et al., 2016), el protocolo impone una secuencia explícita de cuatro fases operativas: (1) *Análisis Profundo*, (2) *Planificación Algorítmica*, (3) *Ejecución Controlada* y (4) *Síntesis de Retroalimentación y Telemetría*.

**Palabras clave:** grandes modelos de lenguaje, protocolo de excelencia sistemática, ingeniería del caos, reproducibilidad científica, alucinaciones en inteligencia artificial, ciencia del diseño.

---

## Abstract

Deploying large language models (LLMs) across high-stakes domains—such as clinical triage, software refactoring, nursing safety education, and complex systems theory—faces persistent challenges from unflagged hallucinations (Ji et al., 2023; Maynez et al., 2020) and the lack of reproducible experimental telemetry (Open Science Collaboration, 2015). Grounded in Design Science Research Methodology (DSRM; Peffers et al., 2007), this repository presents the design, evaluation rubric, and multi-domain stress testing of the **Systematic Excellence Protocol (SEP)** and its open-source suite, **SEP-LLM-Behavior-Benchmark**. Drawing on the Plan-Do-Check-Act (PDCA) quality cycle (Deming, 1986), reinforcement learning feedback principles (Sutton & Barto, 2018), and Chaos Engineering (Basiri et al., 2016), SEP enforces a structured four-phase cognitive workflow: (1) Deep Analysis, (2) Algorithmic Planning, (3) Controlled Execution, and (4) Telemetry & Feedback Synthesis.

**Keywords:** large language models, systematic excellence protocol, chaos engineering, scientific reproducibility, AI hallucinations, design science research.

---

## 1. Matriz Teleológica «Con Propósito»

- **Dolores que cubre:** Alucinaciones no advertidas en dominios críticos (Ji et al., 2023; Maynez et al., 2020), ausencia de trazabilidad experimental reproducible (Open Science Collaboration, 2015) y carencia de pruebas multidominio con escenarios adversariales.
- **Justificación:** La aplicación responsable de LLMs en salud y educación superior exige protocolos auditables y reproducibles bajo Ciencia del Diseño (Peffers et al., 2007).
- **Propósito:** Convertir la interacción cotidiana con LLMs en un objeto científico medible, criticable y replicable.
- **Misión:** Evaluar la estabilidad, transferibilidad y sinergia con *guardrails* de un protocolo de cuatro fases (Análisis ⟶ Planificación ⟶ Ejecución ⟶ Feedback/Telemetría).
- **Visión:** Consolidar un banco de pruebas abierto de referencia para comparar el comportamiento de múltiples familias de modelos LLM.
- **Alcance:** Incluye especificaciones (`protocol/`), 4 casos de prueba (`prompts/`), contexto histórico (`context/`), plantillas (`sessions/`), documentación (`docs/`) y monografía APA 7 (`paper/`). Excluye datos clínicos reales (Ley N.° 25.326).
- **Caso de Estudio Completo:** Ver [docs/case_study_sep.md](docs/case_study_sep.md) y [docs/PROPOSITO.md](docs/PROPOSITO.md).

---

## 2. Estructura Académica del Repositorio

```text
SEP-LLM-Behavior-Benchmark/
├── README.md                                                 ← Monografía ejecutiva APA 7 + Matriz "Con Propósito"
├── CITATION.cff                                              ← Metadatos oficiales de citación en GitHub (APA 7 / BibTeX)
├── .zenodo.json                                              ← Metadatos de indexación para Zenodo, ORCID y OpenAIRE
├── docs/
│   ├── PROPOSITO.md                                          ← Matriz Teleológica "Con Propósito"
│   ├── PRD.md                                                ← Product Requirements Document
│   ├── CASOS_DE_USO.md                                       ← Narrativa de los 4 Casos Multidominio + Adversarial
│   ├── case_study_sep.md                                     ← Caso de estudio completo
│   ├── methodology.md                                        ← Diseño metodológico
│   ├── reproducibility.md                                    ← Guía de reproducibilidad
│   └── results_summary.md                                    ← Síntesis de resultados
├── paper/
│   └── Kamycki_2026_SEP_LLM_Behavior_Benchmark.pdf           ← Artículo completo en PDF (Norma APA 7.ª ed.)
├── protocol/                                                 ← Protocolo maestro SEP y rúbrica de evaluación
├── prompts/                                                  ← Casos estandarizados (Clínico, Código, Educación, Teoría)
├── sessions/                                                 ← Plantillas de registro experimental
└── context/                                                  ← Evidencia histórica (preprint) y trazas de casos
```

---

## 3. Cómo citar este trabajo (Norma APA 7.ª Edición)

> Lancry Kamycki, M. O. (2026). *Systematic Excellence Protocol (SEP-LLM-Behavior-Benchmark): Evaluación multidominio, ingeniería del caos y telemetría reproducible en grandes modelos de lenguaje* (Version 2.0.0). Zenodo. https://doi.org/10.5281/zenodo.24269181

---

## 4. Referencias Bibliográficas (Norma APA 7.ª Edición)

- Basiri, A., Behnam, N., de Rooij, R., Hochstein, L., Kosewski, L., Reynolds, J., & Rosenthal, C. (2016). Chaos engineering. *IEEE Software*, *33*(3), 35–41. https://doi.org/10.1109/MS.2016.60
- Deming, W. E. (1986). *Out of the crisis*. MIT Press.
- Ji, Z., Lee, N., Frieske, R., Yu, T., Su, D., Xu, Y., Ishii, E., Bang, Y. J., Madotto, A., & Fung, P. (2023). Survey of hallucination in natural language generation. *ACM Computing Surveys*, *55*(12), Article 248, 1–38. https://doi.org/10.1145/3571730
- Lancry Kamycki, M. O. (2026a). *Pragmatic alignment of large language models through intensity-weighted feedback markers: An empirical field study* (Version 2.0.0). Zenodo. https://doi.org/10.5281/zenodo.18904436
- Lancry Kamycki, M. O. (2026b). *Heutagogic Narration Protocol (HNP): Aprendizaje autodeterminado, interpretabilidad agéntica por diseño y prevención de inversión de roles en grandes modelos de lenguaje* (Version 2.0.0). Zenodo. https://doi.org/10.5281/zenodo.24269024
- Maynez, J., Narayan, S., Bohnet, B., & McDonald, R. (2020). On faithfulness and factuality in abstractive summarization. In *Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics* (pp. 1906–1919). Association for Computational Linguistics. https://doi.org/10.18653/v1/2020.acl-main.173
- Open Science Collaboration. (2015). Estimating the reproducibility of psychological science. *Science*, *349*(6251), Article aac4716. https://doi.org/10.1126/science.aac4716
- Peffers, K., Tuunanen, T., Rothenberger, M. A., & Chatterjee, S. (2007). A design science research methodology for information systems research. *Journal of Management Information Systems*, *24*(3), 45–77. https://doi.org/10.2753/MIS0742-1222240302
- Sutton, R. S., & Barto, A. G. (2018). *Reinforcement learning: An introduction* (2nd ed.). MIT Press.
