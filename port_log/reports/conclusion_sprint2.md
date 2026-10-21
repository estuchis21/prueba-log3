# Conclusión - Sprint 2

## Relación entre los datos y las imágenes

De las **474 infracciones** provenientes del Sprint 1, **456** recibieron una imagen asociada por matrícula: **96.20%**. Los 93 matches de imágenes aceptados tuvieron un ratio promedio de **94.32%**.

Este porcentaje mide asociación por matrícula, no una validación definitiva del momento de la infracción. Una misma imagen se asigna a todos los movimientos con esa matrícula; sin fecha, hora o identificador de captura no puede asegurarse que corresponda al evento registrado.

## Grupo más útil para OCR

`plates` alcanzó **95.00%** de matches y `completes`, **90.00%**. Por lo tanto, `plates` resultó más útil: el recorte hace que la matrícula ocupe una mayor proporción de la imagen y reduce el fondo que puede confundir al OCR.

## Condiciones que afectaron el matching

Quedaron **7 imágenes sin match**: 3 de `plates` y 4 de `completes`. La tasa de fallo de las imágenes completas fue del 10%, el doble del 5% observado en los recortes. La inspección de los casos fallidos muestra que la distancia —que vuelve muy pequeña la matrícula—, combinada con baja iluminación, poco contraste o desenfoque, fue la situación más perjudicial. En los recortes también aparecieron confusiones entre caracteres de forma similar, como `A/4`, `G/6`, `I/1` y `P/0`.

Como las imágenes no incluyen etiquetas formales de condición (`nocturna`, `lejana` o `borrosa`), esta comparación es una conclusión de la inspección visual y no una medición causal aislada.

## Mejoras propuestas

1. Exigir un tamaño mínimo de matrícula en píxeles y controlar automáticamente foco, exposición e iluminación al capturar.
2. Detectar y recortar primero la región de la matrícula; conservar también la imagen completa para auditoría.
3. Ejecutar el OCR sobre variantes original, ecualizada y suavizada, y elegir el resultado con mayor confianza.
4. Incorporar una comparación tolerante a confusiones frecuentes y enviar a revisión manual los casos cercanos al umbral o ambiguos.
5. Guardar en cada captura fecha, hora, radar e identificador del movimiento para vincular evidencia e infracción de manera unívoca.
