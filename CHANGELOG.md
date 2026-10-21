# Changelog - Port Log - Grupo 07

[Ejercicio 07]
- Conclusión en `reports/conclusion.md` generada a partir de los resultados: calidad del dataset, patrones de infracción, impacto de migrar sin limpieza y propuestas de mejora.

[Ejercicio 06]
- Porcentaje de infracciones con fecha inválida y con hora inválida.
- Tipo de carga más frecuente entre las infracciones.
- Origen más frecuente entre los buques infractores.
- Duración promedio de estadía de los buques infractores.

[Ejercicio 05]
- Conteo de infracciones con y sin imagen asociada.
- Conteo de imágenes sin match aceptado en el dataset.
- Cálculo del ratio promedio del dataset final.
- Comparación de tasas de match entre plates y completes.
- Conteo de infracciones PENDIENTES sin evidencia visual.
- Tratamiento de ausencia de matches y empates entre grupos.

[Ejercicio 04]
- Extracción de texto de imágenes con EasyOCR.
- Actualización de matricula_imagen en group_images.json.
- Normalización de matrículas y comparación por posición.
- Aplicación de un umbral de coincidencia del 75%.
- Detección de empates entre matrículas diferentes.
- Selección de la imagen con mayor ratio por movimiento.
- Generación de port_movements_image.csv.
- Verificación de columnas, cantidad de registros y ratios.

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
