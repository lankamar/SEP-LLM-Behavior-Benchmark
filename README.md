# SEP-LLM-Behavior-Benchmark 🛡️

Reproducible framework for evaluating and documenting Large Language Model (LLM) behavior under the **Systematic Excellence Protocol (SEP)**.

## 🎯 Project Objective
This repository serves as a standardized base for testing, documenting, and comparing LLM responses across different sessions and models. It ensures that evaluations are traceable, reproducible, and structured according to professional engineering standards.

## 📂 Repository Structure
- `/protocol/`: Master SEP guidelines and evaluation rubrics.
- `/prompts/`: Standardized test cases (Clinical, Programming, Education, Theory).
- `/sessions/`: Templates for logging individual model interactions.
- `/artifacts/`: Storage for raw responses, generated reports, and figures.
- `/docs/`: Methodology, results summary, and reproducibility guides.
- `/environment/`: Requirements and technical configuration notes.

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
