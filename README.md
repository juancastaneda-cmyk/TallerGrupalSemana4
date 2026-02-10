# Segmentación de Usuarios con Aprendizaje No Supervisado  
*K-means · DBSCAN · PCA · t-SNE*

## 📌 Descripción del proyecto

Este proyecto implementa y analiza modelos de **aprendizaje no supervisado** para segmentar perfiles de usuarios/clientes en un entorno tecnológico.  
Se aplican técnicas de **clustering** y **reducción de dimensionalidad** con el objetivo de identificar patrones de comportamiento y generar **insights accionables para marketing y negocio**.

El caso simula una **plataforma digital de servicios personalizados** que desea comprender mejor a sus usuarios a partir de datos de comportamiento y consumo.

---

## 🎯 Objetivos

- Aplicar técnicas de clustering no supervisado (**K-means y DBSCAN**).
- Determinar el número óptimo de clusters mediante **Elbow Method** y **Silhouette Score**.
- Reducir dimensionalidad y visualizar patrones con **PCA** y **t-SNE**.
- Comparar resultados entre modelos.
- Interpretar los clusters y traducirlos en **perfiles de cliente** e **insights de marketing**.
- Comunicar resultados de forma técnica y visual.

---

## 📂 Dataset

**Origen:** Kaggle  
**Dataset:** *Mall Customer Segmentation Data*

El dataset contiene información anonimizada de clientes de un centro comercial, incluyendo:

- `Age`: Edad del cliente  
- `Annual Income (k$)`: Ingreso anual  
- `Spending Score (1–100)`: Puntaje de gasto  

📌 **Justificación del uso**  
El dataset fue seleccionado por ser público, realista y adecuado para la aplicación de técnicas de aprendizaje no supervisado en segmentación de clientes.

---

## 🧪 Metodología

### 1️⃣ Preparación del entorno
- Python 3.x
- Librerías científicas y de visualización
- Control de versiones con GitHub

### 2️⃣ Análisis exploratorio (EDA)
- Estadísticos descriptivos
- Distribución de variables
- Análisis de correlaciones
- Escalado de variables numéricas

### 3️⃣ Modelos implementados

#### 🔹 K-means
- Selección del número óptimo de clusters con:
  - Elbow Method
  - Silhouette Score
- Análisis de centroides

#### 🔹 DBSCAN
- Ajuste de hiperparámetros (`eps`, `min_samples`)
- Identificación y exclusión de ruido (outliers)

#### 🔹 PCA
- Reducción lineal de dimensionalidad
- Visualización bidimensional de clusters

#### 🔹 t-SNE
- Visualización no lineal para detección de agrupamientos complejos

---

## 📊 Visualización y exportación de resultados

Todos los resultados generados por el notebook se **exportan automáticamente en la carpeta `figures/`**, incluyendo:

- Gráficos de Elbow Method y Silhouette Score
- Visualizaciones 2D de PCA y t-SNE
- Comparaciones gráficas entre K-means y DBSCAN
- Tablas de perfiles promedio por cluster en formato **CSV**
- Resultados de DBSCAN excluyendo observaciones consideradas como ruido

Los archivos se generan utilizando `matplotlib.pyplot.savefig()` y `pandas.DataFrame.to_csv()`.

---

## 📈 Resultados y análisis

- Identificación de perfiles diferenciados de clientes según edad, ingreso y nivel de gasto.
- **K-means** generó clusters bien definidos y fácilmente interpretables.
- **DBSCAN** permitió identificar clientes atípicos que no pertenecen a ningún grupo denso.
- PCA y t-SNE facilitaron la interpretación visual de los patrones encontrados.

---

## 🧠 Insights de marketing

A partir de los clusters obtenidos se identificaron perfiles como:

- Clientes de alto ingreso y alto gasto → estrategias premium y programas de fidelización.
- Clientes jóvenes con gasto impulsivo → promociones personalizadas.
- Clientes de bajo gasto → campañas de activación y retención.

Estos perfiles permiten adaptar estrategias de marketing basadas en datos.

---

## ⚠️ Limitaciones

- Sensibilidad de K-means al número de clusters.
- Dependencia de DBSCAN en la elección de hiperparámetros.
- Número limitado de variables.
- Ausencia de datos temporales o categóricos.

**Posibles mejoras:**
- Incorporar más variables de comportamiento.
- Evaluar otros algoritmos de clustering.
- Integrar información temporal.

---

## 📁 Estructura del repositorio

```bash
├── data/
│   └── mall_customers.csv
├── notebooks/
│   └── clustering_kaggle.ipynb
├── figures/
│   ├── *.png
│   └── *.csv
├── requirements.txt
└── README.md
