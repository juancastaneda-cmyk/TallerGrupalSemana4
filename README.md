Segmentación de Clientes con Aprendizaje No Supervisado
Dataset: Online Retail (Kaggle)
Descripción del Proyecto

Este proyecto implementa técnicas de Aprendizaje Automático No Supervisado para segmentar clientes utilizando el dataset Online Retail de Kaggle.

El objetivo principal es identificar grupos de clientes con comportamientos de compra similares mediante técnicas de clustering, con el fin de apoyar estrategias de marketing, retención y análisis comercial.

Modelos aplicados:

K-Means

DBSCAN

PCA (Reducción de dimensionalidad)

t-SNE (Visualización avanzada)

El análisis se basa en la metodología RFM (Recency, Frequency, Monetary).

Dataset Utilizado

Nombre: Online Retail Dataset
Fuente: Kaggle
Link oficial:
https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset

Nota importante

El archivo original del dataset es pesado.
Para poder subirlo a GitHub sin superar el límite permitido, fue comprimido en formato:

OnlineRetail.zip

Para ejecutar el proyecto:

Descargue el archivo OnlineRetail.zip del repositorio.

Descomprímalo.

Coloque el archivo OnlineRetail.csv en la carpeta raíz del proyecto.

Metodología Aplicada
1. Limpieza de Datos

Eliminación de registros sin CustomerID

Eliminación de valores negativos en Quantity y UnitPrice

Conversión de InvoiceDate usando dayfirst=True

Creación de la variable TotalAmount

2. Ingeniería de Características – RFM

Se construyeron las siguientes variables:

Recency: Días desde la última compra

Frequency: Número total de facturas por cliente

Monetary: Total gastado por cliente

Estas métricas permiten evaluar el valor y comportamiento de los clientes.

3. Análisis Exploratorio (EDA)

Se generaron:

Histogramas de distribución

Matriz de correlación

Estadísticos descriptivos

Todos los gráficos se almacenan automáticamente en la carpeta:

../figures

4. Preprocesamiento

Estandarización con StandardScaler

Preparación de datos para clustering

5. Clustering

K-Means

Método del Codo

Silhouette Score

Selección del k óptimo

DBSCAN

Identificación de clusters por densidad

Detección de clientes atípicos (ruido)

6. Reducción de Dimensionalidad

PCA (2 componentes)

t-SNE

Permite visualizar los clusters en 2D.

7. Perfilamiento de Clusters

Se generaron archivos CSV con el promedio de:

Recency

Frequency

Monetary

Esto facilita la interpretación estratégica de cada segmento.

Estructura del Proyecto

Proyecto
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

Requisitos Técnicos

Python 3.9+

Instalar dependencias:

pip install pandas numpy matplotlib seaborn scikit-learn

Cómo Ejecutar

Descargar el repositorio

Descomprimir OnlineRetail.zip

Colocar OnlineRetail.csv en la carpeta raíz

Verificar que exista la carpeta ../figures

Ejecutar el notebook completo

Resultados Esperados

Segmentación clara de clientes

Identificación de clientes de alto valor

Detección de clientes inactivos

Identificación de clientes atípicos

Visualización clara de clusters

Aplicaciones Empresariales

Estrategias de fidelización

Campañas segmentadas

Identificación de clientes VIP

Prevención de abandono

Optimización de recursos comerciales
