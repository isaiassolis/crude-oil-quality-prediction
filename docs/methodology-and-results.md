# Metodología y resultados

## Objetivo

En esta investigación exploramos el uso de **Machine Learning** para pronosticar parámetros de calidad del crudo pesado durante los procesos de deshidratación y desalado en la **Terminal Marítima Dos Bocas**.

El objetivo fue comparar modelos de regresión utilizando datos históricos y estudiar su capacidad para anticipar variables relevantes para el acondicionamiento del crudo.

## Datos y preparación

Trabajamos con **12 meses de registros históricos**. Entre las variables utilizadas se encontraban grados API, agua libre, emulsión y sal de las líneas de proceso 1 y 2, junto con información sobre volúmenes de Ku-Maloob-Zaap e inyección de crudo ligero.

Organizamos el trabajo en cinco actividades:

1. Definir variables de entrada y salida.
2. Limpiar y preparar registros.
3. Seleccionar los modelos de regresión.
4. Entrenar los modelos y generar pronósticos.
5. Comparar errores y analizar resultados.

## Modelos evaluados

Comparamos **Decision Tree, Random Forest, Gradient Boosted Trees, Ordinary Least Squares (OLS) y Ridge Regression**.

El trabajo presentado en el **Congreso Mexicano del Petróleo 2019** utilizó una partición **80 % para entrenamiento y 20 % para prueba**, y evaluó los pronósticos mediante el **error absoluto medio (MAE)**.

## Resultados

| Modelo | MAE presentado en la figura 7 |
| :--- | ---: |
| **Gradient Boosted Trees** | **20.417** |
| **Random Forest** | **21.553** |
| Ordinary Least Squares | 23.231 |
| Decision Tree | 23.573 |
| Ridge Regression | 23.770 |

Los ensambles de árboles obtuvieron los menores errores en la comparación publicada. Los valores corresponden a la figura 7 del artículo **CMP2019_207**; no especifican por sí solos el error de una variable de calidad con unidades individuales.

También estudiamos gráficamente los pronósticos y observaciones de **grados API, porcentaje de agua y sal**. Esta última variable presentó diferencias más marcadas, útiles para identificar posibles mejoras del enfoque.

## Resultado de la investigación

La prueba de concepto permitió comparar cinco enfoques predictivos y estudiar su comportamiento sobre los datos analizados.

Fue un **trabajo de investigación aplicada**. Convertir estos modelos en herramientas operativas habría requerido nuevas validaciones y su integración con los procesos industriales correspondientes.

## Referencia

**CMP2019_207** — *Simulador de los procesos de deshidratación y desalado del crudo pesado para cumplir con las especificaciones comprometidas en la fase de comercialización de hidrocarburos y derivados*. Congreso Mexicano del Petróleo, junio de 2019.
