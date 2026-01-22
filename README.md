# Proyecto Final – Data Science III

## Clasificación y análisis del sesgo político en textos periodísticos mediante NLP

**Autor:** Miguel Torres Romero  
**Curso:** Data Science III  
**Herramientas:** Python · NLP · Machine Learning · Deep Learning  
**Entorno:** Jupyter Notebook / Google Colab  

---

## 📌 Descripción general

Este proyecto analiza el **sesgo político en textos periodísticos** a partir de técnicas de Procesamiento de Lenguaje Natural (NLP) y modelos de aprendizaje automático. El objetivo no se limita a la clasificación automática de textos, sino que busca **explorar e interpretar los patrones lingüísticos, semánticos y discursivos** a través de los cuales se construyen orientaciones ideológicas en los medios de comunicación.

El trabajo se inscribe en la intersección entre **ciencia de datos y análisis político**, combinando exploración empírica, visualización de resultados y reflexión sustantiva sobre el significado político de los hallazgos.

---

## 🎯 Objetivos

* Analizar el sesgo político a partir de **patrones lingüísticos y semánticos** en textos periodísticos.
* Construir un **pipeline reproducible de NLP** utilizando datos no tabulares.
* Entrenar y evaluar modelos supervisados para clasificar textos como **Left vs Right**.
* Complementar modelos lineales con un baseline de **Deep Learning (MLP)**.
* Interpretar los resultados desde una **perspectiva política y discursiva**.

---

## 📂 Dataset

**Fuente de los datos**

El dataset utilizado corresponde a **Political Bias**, disponible públicamente en Kaggle y elaborado por el usuario *mayobanexsantana*.  
Los datos pueden consultarse en el siguiente enlace: https://www.kaggle.com/datasets/mayobanexsantana/political-bias/data

El dataset está compuesto por artículos periodísticos en inglés, con las siguientes variables principales:

* `Title`: título del artículo
* `Text`: cuerpo del texto
* `Source`: medio de comunicación
* `Bias`: etiqueta ideológica original
* `bias_binary`: variable binaria (Left / Right)

El análisis se realiza sobre la concatenación **Title + Text**, previamente limpiada y normalizada.

---

## 🧠 Metodología

El proyecto se estructura en dos grandes etapas:

### 1️⃣ Análisis exploratorio y lingüístico (NLP)

* Limpieza y preprocesamiento de texto
* Análisis de longitud y distribución del corpus
* Palabras más frecuentes por clase
* N-gramas (bigramas y trigramas)
* Grafos de co-ocurrencia
* Análisis gramatical (POS tagging)
* Extracción de Entidades Nombradas (NER)
* Análisis de sentimiento (VADER)

Estas técnicas permiten explorar **cómo se organiza el discurso político**, más allá del contenido explícito.

---

### 2️⃣ Modelado supervisado

* **Machine Learning**

  * Bag of Words / TF-IDF
  * Regresión Logística
* **Deep Learning**

  * Red neuronal multicapa (MLP) con Keras/TensorFlow
  * Regularización mediante Dropout

La evaluación se realiza mediante métricas estándar y matrices de confusión, priorizando la **interpretabilidad** por sobre la optimización extrema del rendimiento.

---

## 📊 Principales resultados

* El sesgo político es **detectable empíricamente** a partir de regularidades lingüísticas y semánticas.
* Los modelos aprenden patrones asociados a:

  * vocabulario,
  * marcos semánticos (co-ocurrencias),
  * actores, instituciones y fuentes mediáticas.
* El análisis de sentimiento muestra que el sesgo **no se explica principalmente por el tono emocional**, sino por **estructuras de encuadre discursivo**.
* El modelo de Deep Learning funciona como complemento metodológico, sin superar de manera significativa a los modelos lineales.

---

## ⚠️ Limitaciones

* Desbalance de clases en el dataset.
* Corpus en inglés, centrado en el contexto mediático estadounidense.
* Posible sesgo temporal asociado a coyunturas políticas específicas.
* Captura parcial de señales de fuente además de ideología.

Los resultados deben interpretarse como **patrones situados**, no como propiedades universales del discurso político.

---

## 🔮 Perspectivas futuras

* Extender el análisis a otros idiomas y contextos nacionales.
* Incorporar embeddings contextuales (Word2Vec, GloVe, Transformers).
* Aplicar el pipeline al análisis de **discursos políticos y narrativas de fraude electoral**.
* Explorar modelos temporales para captar cambios discursivos en el tiempo.

---

## ▶️ Ejecución del proyecto

El notebook principal puede ejecutarse en **Google Colab** o en un entorno local con Jupyter.

### Requisitos principales

```bash
pandas
numpy
matplotlib
seaborn
nltk
spacy
scikit-learn
tensorflow
networkx
```

En Colab, basta con **subir el archivo CSV** cuando se solicite.

---

---

## 🧾 Licencia

Este proyecto se publica bajo la **licencia MIT**.

El dataset utilizado (**Political Bias – Kaggle**) pertenece a su autor original y se distribuye bajo los términos de uso establecidos por la plataforma Kaggle.  
Su utilización en este proyecto tiene fines **exclusivamente académicos y no comerciales**.

---

## 👤 Autor

**Miguel Torres Romero**  
Cientista político  
Mg. (c) en Investigación en Ciencias Sociales – Universidad de Buenos Aires (UBA)  

📧 hola@migueltorresromero.com  
🌐 https://www.migueltorresromero.com  

---

## ⭐ Créditos

Proyecto desarrollado en el marco del curso **Data Science III – Coderhouse (2025-2026)**.  
El trabajo articula herramientas de ciencia de datos y Procesamiento de Lenguaje Natural con una perspectiva de **análisis político y discursivo**, orientada al estudio empírico del sesgo ideológico en medios de comunicación.
