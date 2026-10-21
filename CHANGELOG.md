# Changelog - Port Log - Grupo 07

[Ejercicio 07]
- Conclusión en `reports/conclusion.md` generada a partir de los resultados: calidad del dataset, patrones de infracción, impacto de migrar sin limpieza y propuestas de mejora.

[Ejercicio 06]
- Porcentaje de infracciones con fecha inválida y con hora inválida.
- Tipo de carga más frecuente entre las infracciones.
- Origen más frecuente entre los buques infractores.
- Duración promedio de estadía de los buques infractores.

[Ejercicio 05]
- Top 10 de matrículas reincidentes (barras verticales).
- Infracciones por turno del día (torta).
- Infracciones por mes (barras horizontales).
- Histograma del exceso de velocidad real con KDE.
- Exceso promedio por muelle (barras horizontales).
- Infracciones con fecha válida vs inválida (barras).

[Ejercicio 04]
- Clase `PortAnalyzer` que encapsula una copia privada de las infracciones y valida las columnas requeridas.
- Métodos `top_infractores`, `infracciones_por_turno`, `exceso_promedio`, `exceso_promedio_tolerancia`, `infracciones_por_muelle` e `infractores_por_tipo_carga`.
- Métodos auxiliares para los gráficos y las preguntas de negocio.

[Ejercicio 03]
- Fechas en formato YYYY-MM-DD; las inválidas se completan con 1900-01-01.
- Horas en formato de 24 hs; las inválidas se completan con 00:00 y se marcan en columnas `*_valida`.
- Columna `duracion_horas` (pd.NA si una fecha es inválida o el egreso es anterior al ingreso).
- Matrículas y muelles sin caracteres especiales y en mayúsculas.
- Eliminación de nulos en columnas críticas y de outliers por IQR.
- Columnas `exceso_velocidad_real` y `exceso_velocidad` (tolerancia del 5%) y eliminación de filas sin infracción.
- Dataset limpio en `data/interim` y resumen en `reports/summary_sprint1.csv`.

[Ejercicio 02]
- Descarga del dataset crudo en `port_log/data/raw/port_movements.csv`.
- Visualización de las primeras y últimas filas.
- Comparación de tipos inferidos contra el esquema esperado.
- Conteo de valores nulos ordenado de mayor a menor.
- Completitud por columna validando formato además de nulos.

[Ejercicio 01]
- Configuración de git sobre la rama `Sprint_1`.
- Creación de la estructura de directorios `port_log` con `.gitkeep`.
- README.md con el sprint, objetivo, introducción y contexto.
- CHANGELOG.md ordenado del último cambio al primero.
