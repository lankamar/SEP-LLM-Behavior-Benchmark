# SEP-LLM-Behavior-Benchmark 🛡️

Reproducible framework for evaluating and documenting Large Language Model (LLM) behavior under the **Systematic Excellence Protocol (SEP)**.

## 🚀 Case Study: Systematic Excellence Protocol (SEP)

> [!IMPORTANT]
> **Misión**: Validar un protocolo operativo (SEP) que permita trabajar con LLMs de forma estructurada, segura y reproducible en dominios críticos.

Este repositorio no es solo una colección de archivos; es un **objeto científico** diseñado para evaluar si un flujo de 4 fases (Análisis, Plan, Ejecución, Feedback) puede imponer un patrón estable y seguro en la respuesta de las IAs.

### 🎯 Objetivos Estratégicos
- **H1 — Estabilidad**: Verificar si la estructura mejora la calidad de respuesta.
- **H2 — Transferibilidad**: Aplicar el mismo patrón en salud, código y teoría.
- **H3 — Seguridad**: Sinergia entre SEP y los guardrails del modelo.

### 📖 [Leer Caso de Estudio Completo](docs/case_study_sep.md)

---

## 📂 Estructura del Repositorio
- **/context/**: Evidencia histórica (Preprints) y casos de estudio detallados.
- **/protocol/**: Guías maestras del SEP y rúbricas de evaluación.
- **/prompts/**: Casos de prueba estandarizados (Clínico, Programación, Educación, Teoría).
- **/sessions/**: Registro de interacciones individuales y logs de benchmark.
- **/docs/**: Metodología, resultados y guías de reproducibilidad.


## 🚀 Getting Started
### 1. Cloning the Repository
```bash
git clone https://github.com/lankamar/SEP-LLM-Behavior-Benchmark.git
cd SEP-LLM-Behavior-Benchmark
```

### 2. Environment Setup
Install the necessary tools for analysis:
```bash
pip install -r environment/requirements.txt
```

### 3. Execution Order
1.  **Read the Protocol**: Start with `protocol/sep_master_protocol.md` to understand the 4-phase execution (Analysis -> Plan -> Execution -> Feedback).
2.  **Select a Prompt**: Choose a test case from `/prompts/`.
3.  **Run the Session**: Use `sessions/session_template.md` to record the interaction.
4.  **Evaluate**: Apply the `protocol/evaluation_rubric.md` to score the response.
5.  **Log Results**: Archive raw data in `artifacts/raw_responses/` and update `docs/results_summary.md`.

## 🔄 Replicating Tests
To replicate a test on another machine:
1. Ensure the model version and parameters are recorded in the session log.
2. Follow the exact prompt provided in `/prompts/`.
3. Document any deviations in the environment (e.g., system prompt changes).

## 📝 Registering New Tests
- Create a new entry in `sessions/` following the `session_template.md`.
- Link the raw output file located in `artifacts/raw_responses/`.
- Update the `protocol/version_log.md` if any changes were made to the protocol methodology.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
