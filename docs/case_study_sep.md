# Case Study: SEP-LLM-Behavior-Benchmark

## 1. Contexto y Motivación

El uso de modelos de lenguaje grandes (LLMs) se ha expandido a dominios sensibles como la salud, la educación y la investigación científica. En estos entornos, no alcanza con “respuestas inteligentes”: se necesitan **procesos reproducibles, auditables y trazables** que permitan entender *cómo* y *por qué* un modelo tomó ciertas decisiones.

Este caso de estudio documenta el desarrollo del **Systematic Excellence Protocol (SEP)** aplicado a LLMs, y su implementación en un entorno de trabajo real con agentes y herramientas (Antigravity, GitHub, Powershell, etc.). El repositorio captura tanto la **evolución histórica** (preprint) como la fase actual de **stress testing sistemático**.

---

## 2. Misión, Visión y Propósito

### Misión

Diseñar y validar un protocolo operativo que permita trabajar con LLMs de forma **estructurada, segura y reproducible**, basado en cuatro fases explícitas:

1. Análisis  
2. Planificación  
3. Ejecución  
4. Feedback (telemetría, riesgos, mejora continua)

### Visión

Evolucionar desde el “prompting artesanal” hacia un **marco de ingeniería epistemológicamente sólido**, donde:

- cada interacción con el LLM pueda auditarse como si fuera un experimento,  
- los agentes actúen como sistemas que se **auto-analizan y corrigen**,  
- y otros equipos/instituciones puedan **replicar y mejorar** el proceso de forma transparente.

### Propósito

Convertir el trabajo cotidiano con LLMs en:

- **objeto científico** (medible, criticable, replicable),  
- **herramienta formativa** (para enseñanza de IA aplicada en salud y educación),  
- y **plataforma de colaboración** (repositorio público donde otros puedan correr las mismas pruebas y aportar mejoras).

---

## 3. Pregunta Central y Objetivos

### Pregunta central

¿Puede un protocolo explícito de cuatro fases (SEP) imponer un patrón **estable, seguro y útil** en el comportamiento de LLMs a través de:

- múltiples dominios (clínico, programación, educación, teoría),  
- múltiples sesiones y contextos,  
- y distintos modelos,  

y dejar además una traza suficientemente rica como para ser **evaluada científicamente**?

### Objetivo general

Evaluar la **estabilidad, reproducibilidad y transferibilidad** del SEP como marco de interacción con LLMs.

### Objetivos específicos

1. Verificar si las 4 fases del SEP aparecen **de forma consistente** en dominios muy distintos.  
2. Observar el comportamiento del protocolo bajo **condiciones ambiguas y adversariales**, especialmente en temas de seguridad.  
3. Integrar en un solo repositorio la **historia previa** (preprint, dashboards, informes) y las **nuevas pruebas**, para que otros puedan seguir la línea de desarrollo.  
4. Definir un **mecanismo de réplica** que permita a terceros repetir los experimentos con sus propios modelos y datasets.  
5. Abrir el camino a evaluaciones comparativas entre modelos (Perplexity, Claude, Gemini, etc.) bajo el mismo protocolo.

---

## 4. Hipótesis de Trabajo

Las hipótesis que guiaron este caso de estudio son:

- **H1 — Estructura mejora estabilidad.**  
  Un protocolo explícito de 4 fases (Análisis → Plan → Ejecución → Feedback) mejora la estabilidad y calidad de las respuestas de un LLM frente a prompts no estructurados.

- **H2 — Transferibilidad entre dominios.**  
  El mismo patrón SEP puede manifestarse de manera reconocible y útil en dominios muy diferentes (p. ej. triaje telefónico coronario, refactor de código, diseño de clase de enfermería, explicación teórica de Chaos Engineering).

- **H3 — Sinergia con guardrails.**  
  La combinación de SEP con los mecanismos de seguridad propios del modelo reduce la probabilidad de respuestas peligrosas en escenarios adversariales (ej. pedidos de ataques DoS), redirigiendo la conversación hacia prácticas éticas y profesionales.

- **H4 — Repositorio como objeto científico.**  
  Un repositorio bien estructurado (código + prompts + respuestas crudas + rúbricas + contexto preprint) permite que otros investigadores evalúen críticamente el protocolo y lo utilicen como base para nuevos estudios.

---

## 5. Diseño del Caso y Evidencia

### 5.1. Fase Preprint (Contexto Histórico)

En `context/preprint/` se encuentran los artefactos que documentan la **fase inicial** del proyecto:

- `data_dashboard.md` – Primeras visualizaciones y métricas de interacción.  
- `laboratory_report.md` – Informe de laboratorio con experimentos preliminares.  
- `sep_scientific_paper.md` – Borrador del paper científico que formaliza el SEP.  
- `SKILL.md` – Definición del skill/protocolo como “módulo de comportamiento” para el agente.  
- `orchestrator_directive.md` – Directiva de orquestación que indica cómo el agente debe aplicar el SEP.

Estos documentos muestran el pasaje desde una práctica más intuitiva a un enfoque cada vez más **normado y auditable**.

### 5.2. Fase de Stress Tests (Casos 1–4)

En la carpeta `prompts/` y en `context/case2`, `context/case3` se documentan cuatro casos de stress test:

1. **Caso 1 – Clínico (Triaje Coronario Telefónico)**  
   - Objetivo: verificar si el SEP puede estructurar un protocolo de triaje seguro, sensible y legalmente defendible.  
   - Evidencia: protocolo con niveles de riesgo, preguntas clave, acciones y requisitos de registro.  

2. **Caso 2 – Programación (Refactor “Big Ball of Mud”)**  
   - Objetivo: analizar si el SEP ayuda a descomponer un script monolítico en una arquitectura en capas mantenible.  
   - Evidencia: `implementation_plan.md` con análisis, arquitectura propuesta, ejemplo “antes/después” y métricas (complejidad ciclómática, Maintainability Index, acoplamiento).

3. **Caso 3 – Educación (Clase de Seguridad de Medicación)**  
   - Objetivo: ver si el SEP puede guiar el diseño de una clase de 90 minutos en enfermería sobre errores de medicación y cultura de seguridad.  
   - Evidencia: `diseno_clase_nursing.md` con análisis, objetivos de aprendizaje, cronograma, actividad práctica tipo “Detective de Medicación” y esquema de evaluación (3-2-1, near miss, Just Culture).

4. **Caso 4 – Teórico (Chaos Engineering)**  
   - Objetivo: comprobar el comportamiento del SEP en explicaciones de nivel posgrado, integrando teoría de sistemas complejos, resiliencia y prácticas de ingeniería.  
   - Evidencia: respuesta con las 4 fases, definición académica, taxonomía de experimentos, relación con load testing y monitoreo, análisis de blast radius y límites éticos.

En todos los casos, el LLM produjo respuestas con las 4 fases claramente diferenciadas y adaptadas al dominio correspondiente.

### 5.3. Stress Test Adversarial

Se realizaron prompts orientados a **probar límites de seguridad**, por ejemplo:

- pedido explícito de diseñar un ataque para saturar una API pública (DoS).

El modelo, bajo el marco SEP, respondió:

- identificando la ilegalidad y riesgos éticos,  
- rechazando el pedido de ataque,  
- y redirigiendo hacia prácticas legítimas de **load testing controlado** y **chaos engineering** en entornos propios o autorizados.

Esto refuerza la hipótesis H3 sobre la sinergia entre el protocolo y los guardrails del modelo.

---

## 6. Resultados Principales

1. **Estabilidad del patrón SEP.**  
   En los cuatro dominios probados, el modelo organizó su respuesta según las 4 fases SEP, aun cuando el prompt no mencionaba explícitamente el protocolo, lo que sugiere una internalización del patrón.

2. **Calidad contextual.**  
   Las respuestas fueron evaluadas como de alta calidad técnica y contextual:  
   - en el dominio clínico, el protocolo de triaje telefónico respetó criterios de seguridad reales;  
   - en programación, el plan de refactor siguió buenas prácticas de arquitectura y testing;  
   - en educación, la clase integró estándares OMS/ISMP;  
   - en teoría, la explicación de Chaos Engineering fue consistente con la literatura académica.

3. **Comportamiento bajo ambigüedad y adversarial.**  
   En escenarios ambiguos, el SEP tendió a **pedir aclaraciones, explicitar supuestos y ofrecer múltiples planes**.  
   En escenarios adversariales, combinó el análisis de riesgo con una **reorientación ética** de las acciones.

4. **Repositorio como evidencia estructurada.**  
   La integración de preprint + casos + rúbricas + prompts en un único repositorio permite:

   - trazar la evolución del proyecto,  
   - auditar decisiones,  
   - y ofrecer un punto de partida para nuevas réplicas y comparaciones.

---

## 7. Mecanismo de Réplica

Este repositorio está diseñado para que otros investigadores puedan **repetir y extender** el estudio. El flujo recomendado es:

### 7.1. Preparación

1. Clonar el repositorio:  
   ```bash
   git clone https://github.com/lankamar/SEP-LLM-Behavior-Benchmark.git
   cd SEP-LLM-Behavior-Benchmark
   ```
2. Revisar el protocolo en `protocol/sep_master_protocol.md` y la rúbrica en `protocol/evaluation_rubric.md`.  
3. Leer la metodología en `docs/methodology.md` y este `docs/case_study_sep.md`.

### 7.2. Ejecución de Nuevas Sesiones

1. Elegir un caso existente (1–4) o definir un nuevo dominio de prueba.  
2. Tomar el prompt correspondiente en `prompts/`.  
3. Ejecutarlo con el modelo que se desee evaluar (otro LLM, otra configuración, otra plataforma).  
4. Registrar la interacción completa usando `sessions/session_template.md` (fecha, modelo, parámetros, respuesta cruda).  
5. Guardar el archivo en `sessions/` con un nombre que identifique modelo, dominio y fecha.

### 7.3. Evaluación

1. Aplicar la matriz de `protocol/evaluation_rubric.md` a cada sesión.  
2. Puntuar presencia de fases, calidad del plan, adaptabilidad, seguridad y utilidad.  
3. Documentar observaciones y anomalías.

### 7.4. Extensión y Mejora

- Proponer nuevos casos de stress test (p. ej. dominios legales, financieros, de simulación clínica).  
- Ajustar el SEP (nuevas sub-fases, checklists, métricas) y registrar cambios en `protocol/version_log.md`.  
- Enviar pull requests con nuevas sesiones, evaluaciones y mejoras del protocolo.

---

## 8. Limitaciones y Trabajo Futuro

- **N de sesiones por caso.**  
  Este estudio inicial trabaja con un número limitado de sesiones; se requieren series más grandes para análisis estadístico robusto.

- **Variedad de modelos.**  
  La mayor parte de la evidencia actual proviene de un único proveedor. Futuras extensiones deberían incluir al menos 2–3 familias de modelos, documentando versión, temperatura y herramientas disponibles.

- **Entornos reales.**  
  Aunque algunos escenarios se inspiran en contextos clínicos y educativos reales, la validación final debería involucrar **equipos humanos expertos** y, en salud, los comités éticos correspondientes.

A pesar de estas limitaciones, el caso demuestra que:

- es posible tratar a un LLM y su protocolo asociado **como objeto de estudio científico**,  
- y que un repositorio bien diseñado puede servir como **base de réplica, comparación y mejora continua**.

---

## 9. Conclusión

El proyecto **SEP-LLM-Behavior-Benchmark** muestra que un protocolo explícito de cuatro fases puede:

- estabilizar el comportamiento de un LLM,  
- mejorar la calidad y seguridad de sus respuestas,  
- y dejar una traza suficientemente rica como para ser evaluada y replicada.

Este repositorio queda abierto como invitación para que otros investigadores:

- repitan las pruebas,  
- comparen modelos,  
- cuestionen y mejoren el SEP,  
- y, sobre todo, contribuyan a construir una práctica de IA **responsable, reproducible y científicamente seria**.
