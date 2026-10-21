# Conclusión - Sprint 1

## Calidad del dataset heredado

- Se recibieron 1500 registros. Por problemas de calidad (nulos en columnas críticas y outliers) se descartaron 255 (17.00%); otros 772 se excluyeron por no constituir infracción, quedando 474 infracciones.
- Los errores más frecuentes por columna son:
  - `hora_egreso`: 171 valores incorrectos (11.40%)
  - `matricula`: 142 valores incorrectos (9.47%)
  - `hora_ingreso`: 97 valores incorrectos (6.47%)
- Entre las infracciones, 4.64% tiene una fecha inválida y 18.57% una hora inválida: son datos que el nuevo sistema no podría ubicar en el tiempo.

## Patrones de infracción

- Turno con más infracciones: **Madrugada** (134 casos). Las horas inválidas se completaron con 00:00, así que parte de ese turno puede ser un efecto de la limpieza y no un patrón real.
- Muelles con más infracciones: **MUELLE D** (87) y **MUELLE B** (82). El mayor exceso promedio se da en **MUELLE D** (3.28).
- Tipo de carga con más infracciones: **CONTENEDORES** (71 casos).
- Exceso promedio: 3.03 sin tolerancia y 2.47 con la tolerancia del 5%.

## Impacto de migrar sin limpieza

Cargar estos datos sin depurar llevaría al nuevo sistema velocidades y tonelajes imposibles que distorsionan cualquier promedio, estadías negativas o de siglos por fechas mal cargadas, y el mismo buque repartido en varias matrículas escritas de forma distinta. Las sanciones y los reportes de reincidencia quedarían mal atribuidos y las decisiones operativas se tomarían sobre indicadores falsos.

## Propuestas de mejora para la captura de datos

1. Validar en el punto de carga: fecha y hora con selector (ISO 8601 y 24 hs), rangos numéricos por muelle y tipo de carga, y campos obligatorios que no permitan guardar el registro vacío.
2. Tomar matrícula y muelle de catálogos maestros en lugar de texto libre, así un mismo buque no aparece con varias grafías.
3. Registrar la velocidad directamente desde el radar (`radar_id`) con marca de tiempo automática, eliminando la transcripción manual.
