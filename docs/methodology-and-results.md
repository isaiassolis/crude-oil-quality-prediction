# Metodología y resultados

## Objetivo

Estudiar la viabilidad de pronosticar parámetros de calidad del crudo pesado durante los procesos de deshidratación y desalado en la **Terminal Marítima Dos Bocas** a partir de información histórica.

## Datos

La prueba de concepto utilizó **12 meses de datos históricos**. Las variables de entrada incluían grados API, agua libre, emulsión y sal de las líneas 1 y 2, junto con volúmenes procedentes de Ku-Maloob-Zaap e inyección de crudo ligero.

No publico los registros originales ni construyo un dataset sintético que pueda confundirse con datos reales de la terminal.

## Proceso

1. Definición de variables de entrada y variables objetivo.
2. Limpieza y acondicionamiento de registros.
3. Selección de modelos para comparar.
4. Entrenamiento y generación de pronósticos.
5. Cálculo de errores y comparación de resultados.

## Métodos

Se compararon **Decision Trees, Random Forest, Gradient Boosted Trees, Ordinary Least Squares (OLS) y Ridge Regression**.

La memoria técnica indica una partición **80/20** para entrenamiento y prueba, y usa **MAE** como métrica de comparación.

## Resultados publicados

| Modelo | MAE mostrado en la figura 7 |
| :--- | ---: |
| Gradient Boosted Trees | 20.417 |
| Random Forest | 21.553 |
| Ordinary Least Squares | 23.231 |
| Decision Trees | 23.573 |
| Ridge Regression | 23.770 |

**Estos números son los publicados en la figura 7 del artículo de 2019.** El documento no especifica completamente cómo se agregaron los errores de distintas variables de salida, por lo que no deben reinterpretarse como error de una única variable con unidades homogéneas.

El artículo muestra comparaciones visuales para grados API, porcentaje de agua y libras de sal por millar de barriles. Los ensambles de árboles ofrecieron el menor error reportado, aunque el pronóstico de sal presentó mayores discrepancias respecto de los valores observados.

## Límites

- Se trató de una **prueba de concepto**, no de un sistema con desempeño productivo verificado.
- No se documentan validaciones prospectivas ni seguimiento de modelos después del congreso.
- No se conservan aquí configuraciones, particiones exactas, código fuente o datos para una reproducción independiente.
- No se atribuyen ahorros económicos ni reducciones de penalizaciones que no hayan sido medidas.

## Referencia

**CMP2019_207**, Congreso Mexicano del Petróleo 2019, especialmente páginas 1, 7–8 y 12–17.