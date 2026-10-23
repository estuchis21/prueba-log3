# Changelog - Port Log - Grupo 07

[Ejercicio 07]
- Conclusión en `reports/conclusion.md` generada a partir de los resultados: calidad del dataset, patrones de infracción, impacto de migrar sin limpieza y propuestas de mejora.

[Ejercicio 06]
- Análisis de cobertura visual sobre las infracciones detectadas.
- Comparación de desempeño de OCR entre subgrupos plates y completes.
- Evaluación de impacto de condiciones de captura y sesgos de lectura.
- Propuesta de mejoras técnicas de captura, preprocesamiento y matching.
- Guardado de informe final en `port_log/reports/conclusion_sprint2.md`.

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
- Imágenes originales: port_log/data/raw/imgs
- Gráficos intermedios: port_log/data/interim/plots
- Dataset procesado final: port_log/data/processed/port_movements_image.csv

[Ejercicio 01]
- Creación o selección de la rama `Sprint_3` desde `Sprint_2`.
- Verificación de los cuatro datasets heredados y registro de sus cantidades y fechas de modificación.
