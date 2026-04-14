# Plan de Refactorización de Script Monolítico Python

Este documento detalla la estrategia para transformar un script de 300 líneas con responsabilidades mezcladas en una estructura mantenible y profesional.

## FASE 1 – ANÁLISIS
Identificación de los problemas actuales del diseño "Big Ball of Mud":
- **Acoplamiento Fuerte**: La lógica de negocio depende directamente de la estructura de la DB.
- **Baja Cohesión**: Una sola función gestiona I/O, reglas de negocio y presentación.
- **Imposibilidad de Pruebas Unitarias**: No se puede testear el cálculo sin instanciar una base de datos o capturar la consola.
- **Carga Cognitiva**: 300 líneas exceden el límite de comprensión rápida.

## FASE 2 – PLAN (Estructura Propuesta)
Se propone una **Arquitectura en Capas** simple:
1. **Capa de Datos (Infrastructure/Persistence)**: Clase `Repository` para queries SQL/NoSQL.
2. **Capa de Negocio (Domain/Service)**: Funciones puras que procesan datos sin saber de dónde vienen.
3. **Capa de Presentación (Entrypoint/Presenter)**: Script principal que coordina el flujo y formatea el output.

### Nueva Estructura de Archivos
- `database.py`: Gestión de conexión.
- `repository.py`: Consultas específicas.
- `services.py`: Lógica de negocio (ej. cálculos, validaciones).
- `models.py`: Clases (Dataclasses) para representar los datos.
- `main.py`: Punto de entrada y formateo.

## FASE 3 – EJECUCIÓN (Ejemplo de División)
Transformación de una función `procesar_reporte()` monolitica a una versión desacoplada:

**Antes (300 líneas):**
```python
def procesar_reporte():
    # 1. SQL Query hardcoded
    # 2. Iterar filas y aplicar lógica de impuestos
    # 3. Print de tablas formateadas
```

**Después (Desacoplado):**
- `get_raw_data()` -> `list[VentaDTO]` (Repo)
- `calcular_impuestos(ventas)` -> `list[VentaProcesada]` (Service)
- `render_table(datos)` -> String/Console (Presenter)

## FASE 4 – FEEDBACK (Métricas de Éxito)
Evaluación post-refactor mediante:
- **Complejidad Ciclomática (McCabe)**: Reducción drástica al dividir ramificaciones (if/else).
- **Maintainability Index**: Cálculo basado en líneas de código, complejidad y volumen Halstead.
- **Acoplamiento (Afferent/Efferent coupling)**: Medir cuántas dependencias tiene la lógica de negocio.
- **Facilidad de Mocking**: Tiempo requerido para escribir un test unitario de la lógica central.

## Evaluación de Riesgos
> [!WARNING]
> Un refactor sin tests previos ("Refactor a ciegas") es peligroso. Se recomienda escribir al menos un test de integración (Black-box) que valide que el output final no cambie antes de empezar a mover el código.
