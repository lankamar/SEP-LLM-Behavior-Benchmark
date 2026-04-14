# Guía de Reproducibilidad (Reproducibility Guide)

Garantizar que un test sea reproducible es el pilar de este repositorio. Sigue estas instrucciones para repetir o validar pruebas en otra máquina.

## 📋 Variables a Documentar
Para que una sesión sea válida, DEBEN registrarse las siguientes variables:
1.  **Modelo y Proveedor**: Ej. OpenAI GPT-4o, Anthropic Claude 3.5 Sonnet.
2.  **Parámetros de Inferencia**: Temperature, Top-P, Max Tokens.
3.  **System Prompt**: Documentar si se utilizó el SEP Pre-Prompt u otro específico.
4.  **Latencia**: Tiempo de respuesta medido.
5.  **Entorno**: Versiones de librerías instaladas (referenciar `environment/requirements.txt`).

## 💾 Gestión de Outputs
- Los outputs crudos (sin procesar) deben guardarse en `artifacts/raw_responses/` con un nombre descriptivo: `AAAA-MM-DD-MODELO-CASO.txt`.
- No editar el texto generado por la IA en estos archivos; cualquier observación debe ir en el log de la sesión.

## 🔄 Procedimiento de Repetición
1. Clonar el repositorio.
2. Configurar el entorno exacto.
3. Introducir el prompt del archivo `prompts/caseX.md`.
4. Comparar el nuevo resultado con los históricos usando la matriz de evaluación.
5. Documentar cualquier desviación significativa en el razonamiento del modelo.
