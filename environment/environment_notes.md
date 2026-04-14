# Notas sobre el Entorno de Ejecución

Este benchmark se ha desarrollado considerando los siguientes parámetros y restricciones tecnológicas.

## 🛠️ Configuración de Referencia
- **Sistema Operativo**: Windows 11 (Entorno de desarrollo original).
- **Python**: 3.10+ recomendado.
- **Protocolo Maestro**: Systematic Excellence Protocol (SEP) v1.0.

## 🤖 Versiones de Modelos Testeados
Se recomienda registrar la versión exacta (timestamp) de los modelos, ya que el comportamiento de las APIs de LLM puede variar sin previo aviso.

| Proveedor | Modelo | ID de Versión Crítica | Notas |
| :--- | :--- | :--- | :--- |
| Google | Gemini 1.5 Pro | `gemini-1.5-pro-latest` | Alta adherencia al SEP en razonamiento lógico. |
| OpenAI | GPT-4o | `gpt-4o-2024-05-13` | Excelente en dominios clínicos y educativos. |
| Anthropic | Claude 3.5 Sonnet | `claude-3-5-sonnet-20240620` | Sobresaliente en refactorización de código. |

## ⚠️ Advertencias Técnicas
- **Consumo de Tokens**: Los prompts de stress test en `protocol/prompts_master.md` pueden generar respuestas extensas (>2000 tokens).
- **Variabilidad**: Se han observado variaciones de hasta un 15% en la puntuación de la rúbrica ante el mismo prompt con `Temperature=0.7`. Se recomienda `Temperature=0` para benchmark de reproducibilidad pura.
