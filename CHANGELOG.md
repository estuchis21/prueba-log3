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
- Conversión a escala de grises en `port_log/data/interim/imgs/03_01_gray`.
- Ecualización de histograma en `port_log/data/interim/imgs/03_02_equalized`.
- Suavizado gaussiano en `port_log/data/interim/imgs/03_03_blur`.
- Detección de bordes Canny en `port_log/data/interim/imgs/03_04_canny`.
- Inspección visual mediante `mostrar_muestra` en cada etapa.

[Ejercicio 02]
- Listado y cálculo de pesos en KB de imágenes.
- Separación en subgrupos 'plates' y 'completes'.
- Generación del archivo `port_log/data/interim/group_images.json`.
- Cálculo de métricas promedio de resolución, área y peso.
- Implementación y prueba de la función `mostrar_muestra`.

[Ejercicio 01]
- Creación y checkout de rama `Sprint_2` a partir de `Sprint_1`.
- Descarga y descompresión de imágenes en `port_log/data/raw/imgs`.
- Verificación de accesibilidad de archivos base del Sprint 1.
- Actualización de README.md con contexto y objetivos de Sprint 2.
