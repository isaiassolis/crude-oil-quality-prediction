<p align="center"><img src="assets/banner.svg" width="100%" alt="Crude Oil Quality Prediction — Industrial Machine Learning" /></p>
<p align="center">
<img src="https://img.shields.io/badge/Project-Industrial%20AI-087F8C?style=for-the-badge" alt="Industrial AI" />
<img src="https://img.shields.io/badge/Machine%20Learning-Supervised-12395D?style=for-the-badge" alt="Supervised learning" />
<img src="https://img.shields.io/badge/Role-Technical%20Manager-0B91A1?style=for-the-badge" alt="Technical Manager" />
<img src="https://img.shields.io/badge/CMP-2019-12395D?style=for-the-badge" alt="CMP 2019" />
</p>

# Pronóstico de calidad de crudo pesado mediante Machine Learning

### Prueba de concepto orientada a apoyar decisiones operativas durante la deshidratación y el desalado de crudo en la Terminal Marítima Dos Bocas.

**Plenumsoft Energy & Sustainability · Congreso Mexicano del Petróleo 2019 · Trabajo CMP2019_207**

En 2019 participé, como **Gerente Técnico de Plenumsoft Energy & Sustainability**, en un proyecto de inteligencia artificial aplicada a la industria energética: pronosticar características del crudo pesado durante su acondicionamiento para apoyar el cumplimiento de las especificaciones comprometidas en su comercialización.

El trabajo fue una colaboración entre personal de **PEMEX Exploración y Producción** y **Plenumsoft**. Fui **coautor del artículo técnico** presentado en el Congreso Mexicano del Petróleo. En este repositorio comparto el enfoque y los resultados publicados de la prueba de concepto, sin incluir datos operativos, modelos entrenados ni código propietario.

## 🎯 El problema

Para comercializar crudo pesado es necesario cumplir parámetros de calidad, entre ellos los **grados API, la concentración de agua y el contenido de sal**. El comportamiento de estas variables depende de las condiciones del proceso y su incumplimiento puede tener consecuencias contractuales.

Nuestro reto consistía en **utilizar registros históricos para anticipar estas variables** y ofrecer información útil a quienes toman decisiones operativas.

## 🧠 Nuestra prueba de concepto

Trabajamos con **12 meses de datos históricos** y seguimos un proceso de selección de variables, limpieza y acondicionamiento de datos, entrenamiento de modelos y comparación de pronósticos.

**Entradas estudiadas:** grados API, agua libre, emulsión y sal de dos líneas de proceso, además de datos de volumen e inyección de crudo considerados en el artículo.

**Evaluación reportada:** **80 % de los registros para entrenamiento** y **20 % para prueba**, utilizando **error absoluto medio (MAE)** como medida de comparación.

| Modelo evaluado | Enfoque |
| :--- | :--- |
| Decision Tree | Árbol de regresión |
| **Random Forest** | Ensamble de árboles |
| **Gradient Boosted Trees** | Ensamble secuencial |
| Ordinary Least Squares (OLS) | Modelo lineal de referencia |
| Ridge Regression | Modelo lineal regularizado |

## 📊 Resultados presentados en el congreso

![Comparación de MAE de cinco modelos](assets/model-comparison.svg)

Los valores proceden de la **figura 7 del artículo CMP2019_207**. No se indica con suficiente detalle cómo se agregaron las distintas variables objetivo; por eso se presentan como resultados publicados y no como métricas reproducidas en este repositorio.

**Gradient Boosted Trees y Random Forest** registraron los menores errores entre los cinco enfoques. El trabajo compara además las curvas pronosticadas y observadas para **grados API, porcentaje de agua y sal**, con diferencias apreciables especialmente en la variable sal.

> **Alcance:** el estudio documentó resultados de una **prueba de concepto**. No afirmo que estos modelos se hayan desplegado en producción ni que se hayan evitado penalizaciones reales mediante su utilización.

## 🔄 Metodología

```mermaid
flowchart LR
  A[Datos históricos] --> B[Limpieza y preparación]
  B --> C[Cinco modelos supervisados]
  C --> D[Entrenamiento 80%]
  D --> E[Prueba 20%]
  E --> F[Evaluación con MAE]
  F --> G[Comparación de pronósticos]
```

## 👤 Mi participación

Participé desde la **Gerencia Técnica de Plenumsoft Energy & Sustainability** y como **coautor del trabajo**. El proyecto reunió conocimientos del proceso industrial, manejo de datos históricos y aprendizaje automático, junto con especialistas de PEMEX y Plenumsoft.

El artículo acredita como **autor a Bruno Pecero García** (PEMEX Exploración y Producción), y como **coautores a Felipe Pacheco Rosado, Minerva Rojas Solís, Yahvé Isaías Solís Aranda, Raúl López Altamirano y Gabriel Azuela Barajas** (Plenumsoft).

El carácter colectivo del trabajo es importante: no atribuyo exclusivamente a mi persona el desarrollo de cada algoritmo.

## 📚 Documentación

- [Metodología y resultados](docs/methodology-and-results.md)
- [Mi participación, autoría y alcance público](docs/scope-and-attribution.md)

**Fuente principal:** *CMP2019_207 — Simulador de los procesos de deshidratación y desalado del crudo pesado para cumplir con las especificaciones comprometidas en la fase de comercialización de hidrocarburos y derivados*. Congreso Mexicano del Petróleo, junio de 2019.

---
<p align="center"><strong>Aplicar el análisis predictivo a decisiones operativas reales.</strong></p>
<p align="center">Caso de estudio profesional de <a href="https://github.com/isaiassolis">Isaías Solís</a></p>