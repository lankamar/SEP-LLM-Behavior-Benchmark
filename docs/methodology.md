# Metodología de Evaluación de Comportamiento Funcional

Este proyecto se centra en el estudio del **comportamiento funcional del sistema** y su capacidad para adherirse a protocolos operativos rigurosos, independientemente de la "veracidad" externa de los datos generados (en contextos teóricos) o de la legitimidad de autoría de papers preexistentes.

## 🔬 Objeto de Estudio
El benchmark analiza la **capacidad de razonamiento, planificación y ejecución** de los modelos de lenguaje bajo carga técnica. No se evalúa el conocimiento estático del modelo, sino su **proceso dinámico** ante problemas que requieren:
1.  Análisis recursivo.
2.  Priorización de seguridad sobre conveniencia.
3.  Estructuración de planes multicapa.
4.  Síntesis de feedback autocrítico.

## 📊 Comparativa de Sesiones
Para garantizar la validez del benchmark, se comparan:
- **Modelos**: Distintas arquitecturas (Transformer, MoE) y proveedores.
- **Dominios**: Estresando al modelo en áreas donde la precisión es vital (Clínico) vs. donde la abstracción es clave (Teórico).
- **Consistencia Temporada**: Comparando respuestas ante el mismo prompt en diferentes sesiones para medir la deriva estocástica.

## ⚖️ Neutralidad y Ética
El benchmark mantiene una postura neutral. Los resultados no indican qué modelo es "mejor" de forma absoluta, sino qué modelo se adapta mejor al **Protocolo SEP** en condiciones de reproducibilidad.
