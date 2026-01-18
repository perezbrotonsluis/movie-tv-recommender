# 🎬 Movie & TV Show Recommender System

Proyecto final del curso **Big Data y Business Intelligence**.

---

## 📌 Descripción general

Este proyecto consiste en el desarrollo de un **sistema de recomendación de películas y series basado en contenido**, utilizando información textual y semántica de los títulos. El sistema es capaz de recomendar contenidos similares a uno dado, sin necesidad de datos de usuarios, basándose únicamente en las características propias de cada película o serie.

El recomendador se ha construido a partir de un catálogo unificado de contenidos procedentes de distintas plataformas de streaming, permitiendo trabajar con un conjunto amplio y diverso de títulos.

---

## 🎯 Objetivo

Diseñar e implementar un **recomendador basado en contenido** que:

* Analice películas y series a partir de su descripción, géneros y reparto.
* Represente cada título mediante técnicas de vectorización de texto.
* Genere recomendaciones coherentes utilizando medidas de similitud.
* Permita evaluar la calidad de las recomendaciones de forma cualitativa y cuantitativa.

---

## 📊 Dataset

Los datos utilizados provienen de **Kaggle** y corresponden a catálogos de:

* Netflix
* HBO
* Amazon Prime Video
* Disney Plus

Se han utilizado dos tipos de datasets:

* **Títulos**: información general (título, descripción, géneros, año, etc.).
* **Créditos**: actores y directores asociados a cada título.

Durante el proyecto, los datasets han sido **analizados, limpiados y unificados** para construir un catálogo común sobre el que aplicar el modelo de recomendación.

---

## 🧠 Metodología

El sistema se basa en un enfoque de **recomendación por contenido**, siguiendo los siguientes pasos:

1. **Análisis exploratorio (EDA)**

   * Inspección de estructura, valores nulos y duplicados.
   * Estudio de las variables más relevantes para el recomendador.

2. **Preprocesamiento de datos**

   * Limpieza de valores nulos críticos.
   * Normalización de texto.
   * Procesamiento de nombres de actores y directores como tokens únicos.
   * Agregación de créditos por título.
   * Construcción de una columna `metadata` que combina descripción, géneros y reparto.

3. **Modelado**

   * Vectorización del contenido mediante **TF-IDF**.
   * Cálculo de similitud entre títulos usando **cosine similarity**.
   * Generación de recomendaciones a partir de títulos de referencia.

4. **Evaluación**

   * Evaluación cualitativa de recomendaciones para títulos conocidos.
   * Evaluación automática mediante métricas como *Precision@K*, utilizando los géneros como criterio de validación.

---

## 📁 Estructura del repositorio

```
├── data/
│   ├── raw/                # Datasets originales
│   └── processed/          # Datasets preprocesados
│
├── notebooks/
│   ├── 01_eda_inicial.ipynb
│   ├── 02_preprocesamiento.ipynb
│   ├── 03_modelo_recomendador.ipynb
│   └── 04_evaluacion_y_conclusiones.ipynb
│
├── README.md
└── requirements.txt
```

---

## 📈 Resultados

El sistema es capaz de generar recomendaciones coherentes desde el punto de vista temático y semántico, identificando similitudes entre títulos en función de su contenido textual y del reparto.
Las evaluaciones muestran que una proporción significativa de las recomendaciones comparte géneros con el título original, validando el enfoque utilizado.

---

## 🚀 Posibles mejoras futuras

* Ajuste automático de hiperparámetros del modelo TF-IDF.
* Inclusión de variables numéricas (año, duración, puntuaciones) mediante enfoques híbridos.
* Uso de embeddings más avanzados (Word2Vec, Sentence-BERT).
* Incorporación de información de usuarios para evolucionar hacia un recomendador híbrido.

---

## 🛠️ Tecnologías utilizadas

* Python
* Pandas, NumPy
* Scikit-learn
* Jupyter Notebook

---

## 👤 Autor

**Luis Pérez-Brotons**

Proyecto académico – Big Data y Business Intelligence
