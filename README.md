# 🧠 Segmentación de Clientes con Aprendizaje No Supervisado  
## Dataset: Online Retail (Kaggle)

---

## 📌 Descripción del Proyecto

Este proyecto implementa técnicas de **Aprendizaje Automático No Supervisado** para segmentar clientes utilizando el dataset **Online Retail** de Kaggle.

## 🎯 Objetivo del Proyecto

El objetivo principal del proyecto es identificar y caracterizar segmentos de clientes con comportamientos de compra similares mediante técnicas de clustering no supervisado, con el fin de generar información útil para la toma de decisiones comerciales.

### 🔍 Modelos aplicados

- K-Means  
- DBSCAN  
- PCA (Reducción de dimensionalidad)  
- t-SNE (Visualización avanzada)  

El análisis se basa en la metodología **RFM (Recency, Frequency, Monetary)**.

---

## 📂 Dataset Utilizado

- **Nombre:** Online Retail Dataset  
- **Fuente:** Kaggle  
- **Link oficial:**  
  https://www.kaggle.com/datasets/ulrikthygepedersen/online-retail-dataset
  
**Online Retail** Es un dataset de ventas de una tienda minorista online del Reino Unido (2010-2011). Cada registro es un artículo vendido en una transacción, con datos como factura, producto, cantidad, fecha, precio, cliente y país.

---

## ⚠️ Nota Importante sobre el Dataset

El archivo original del dataset es pesado.  
Para poder subirlo a GitHub sin superar el límite permitido, fue comprimido en formato:


### ▶ Cómo utilizarlo:

1. Descargue el archivo `OnlineRetail.zip` del repositorio.
2. Descomprímalo.
3. Coloque el archivo `OnlineRetail.csv` en la carpeta raíz del proyecto.
4. Ejecute el notebook.

---

## 🧹 Metodología Aplicada

### 1️⃣ Limpieza de Datos

- Eliminación de registros sin `CustomerID`
- Eliminación de valores negativos en `Quantity` y `UnitPrice`
- Conversión de `InvoiceDate` usando `dayfirst=True`
- Creación de la variable `TotalAmount`

---

### 2️⃣ Ingeniería de Características – RFM

Se construyeron las siguientes variables:

- **Recency:** Días desde la última compra  
- **Frequency:** Número total de facturas por cliente  
- **Monetary:** Total gastado por cliente  

Estas métricas permiten evaluar el valor y comportamiento de los clientes.

---

### 3️⃣ Análisis Exploratorio (EDA)

Se generaron:

- Histogramas de distribución  
- Matriz de correlación  
- Estadísticos descriptivos  

Todos los gráficos se almacenan automáticamente en la carpeta:



---

### 4️⃣ Preprocesamiento

- Estandarización con `StandardScaler`
- Preparación de datos para clustering

---

### 5️⃣ Clustering

#### 🔹 K-Means
- Método del Codo
- Silhouette Score
- Selección del k óptimo

#### 🔹 DBSCAN
- Identificación de clusters por densidad
- Detección de clientes atípicos (ruido)

---

### 6️⃣ Reducción de Dimensionalidad

- PCA (2 componentes)
- t-SNE

Permite visualizar los clusters en 2D.

---

### 7️⃣ Perfilamiento de Clusters

Se generaron archivos CSV con el promedio de:

- Recency  
- Frequency  
- Monetary  

Esto facilita la interpretación estratégica de cada segmento.

## 📊 Principales Hallazgos

- K-means permitió identificar cuatro perfiles de clientes con comportamientos claramente diferenciados en términos de recencia, frecuencia y gasto.
- DBSCAN identificó un único grupo denso y un conjunto de clientes atípicos, siendo más útil para la detección de outliers que para una segmentación fina.
- Las visualizaciones mediante PCA y t-SNE confirmaron la separación de los clusters obtenidos con K-means.
- Los clientes de alto valor representan un grupo reducido, pero con un impacto significativo en el valor monetario total.

---

## 📁 Estructura del Proyecto

Proyecto/
│
├── OnlineRetail.zip
├── segmentacion_clientes.ipynb
└── figures/
├── distribucion_rfm.png
├── matriz_correlacion_rfm.png
├── elbow_kmeans.png
├── silhouette_kmeans.png
├── pca_kmeans.png
├── pca_dbscan.png
├── tsne_kmeans.png
├── tsne_dbscan.png
├── perfiles_cluster_kmeans.csv
└── perfiles_cluster_dbscan.csv

---

## 🛠 Requisitos Técnicos

- Python 3.9+

Instalar dependencias:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn


