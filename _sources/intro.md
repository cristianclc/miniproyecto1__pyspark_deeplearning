# **Predicción de Clics en Anuncios Móviles mediante Redes Neuronales Multicapa**

### **Autores:**

- Johan David Diaz Lopez
- David Ricardo Marquez Luna
- Cristian Camilo Linero Cantillo
- Luis David Peñaranda Perez

**Universidad:** Universidad del Norte

**Programa:** Ciencia de Datos

**Profesor:** Dr. Lihki Rubio

**Año:** 2026

---

### **Abstract**

La predicción de clics en anuncios móviles —conocida como *Click-Through Rate (CTR) prediction*— es uno de los problemas más estudiados en la intersección entre el aprendizaje automático y la publicidad digital. Anticipar si un usuario hará clic en un anuncio tiene implicaciones económicas directas para plataformas y anunciantes, y representa un desafío técnico considerable: los datos son masivos, altamente desbalanceados y compuestos en su mayoría por variables categóricas anonimizadas que exigen estrategias de preprocesamiento cuidadosas.

En este trabajo se desarrolla un sistema de clasificación supervisada basado en **Redes Neuronales Multicapa (MLP)** para predecir la variable binaria `click` sobre el dataset **Avazu CTR Prediction**, un benchmark ampliamente utilizado en la comunidad que contiene aproximadamente 40 millones de registros de impresiones publicitarias móviles. El proyecto abarca desde un análisis exploratorio detallado —que incluye la transformación de la variable temporal `hour`, el estudio del desbalance de clases (83% no click / 17% click), el análisis de cardinalidad y la construcción de una matriz de correlación sobre variables anónimas— hasta el entrenamiento y comparación de modelos en dos entornos computacionales distintos.

En **scikit-learn**, se trabajó sobre una muestra representativa de un millón de registros, aplicando *Target Encoding* con suavizado para el manejo de variables categóricas de alta cardinalidad y optimización de hiperparámetros mediante `GridSearchCV`. En **PySpark**, se operó sobre 10 millones de registros balanceados mediante *undersampling* (50% / 50%), utilizando `StringIndexer`, `OneHotEncoder` y `VectorAssembler` dentro de un pipeline distribuido. Ambos entornos fueron evaluados con métricas como **AUC, F1-score, Precisión y Recall**, y se midió el costo computacional de cada uno.

Adicionalmente, se incorpora un análisis de interpretabilidad mediante **LIME** (*Local Interpretable Model-agnostic Explanations*) en ambos entornos, con el objetivo de identificar las variables más influyentes en predicciones individuales, particularmente en casos de clasificación errónea. Los resultados evidencian que el tratamiento del desbalance de clases y la estrategia de codificación tienen un impacto determinante sobre la capacidad del modelo para detectar clics, y que cada entorno presenta ventajas y limitaciones claras según el volumen de datos y la flexibilidad requerida.

---

**Keywords:**
Click-Through Rate Prediction, MLP, Neural Networks, PySpark, scikit-learn, LIME, Interpretability, Mobile Advertising, Class Imbalance

```{tableofcontents}
```