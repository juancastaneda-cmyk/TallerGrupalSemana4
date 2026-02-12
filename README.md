📊 Segmentación de Clientes con Aprendizaje No Supervisado
Dataset: Online Retail (Kaggle)
📌 Descripción del Proyecto

Este proyecto implementa técnicas de Aprendizaje Automático No Supervisado para segmentar clientes utilizando el dataset Online Retail de Kaggle.

El objetivo principal es identificar grupos de clientes con comportamientos de compra similares mediante técnicas de clustering, con el fin de apoyar estrategias de marketing, retención y análisis comercial.

Se aplican los siguientes modelos:

✅ K-Means

✅ DBSCAN

✅ PCA (Reducción de dimensionalidad)

✅ t-SNE (Visualización avanzada)

El análisis se basa en la metodología RFM (Recency, Frequency, Monetary).

📂 Dataset Utilizado

Nombre: Online Retail Dataset
Fuente: Kaggle
Link oficial:
https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset

⚠ Nota Importante sobre el Dataset

El archivo original del dataset es relativamente pesado.
Para poder subirlo al repositorio de GitHub sin superar los límites de tamaño, fue comprimido en formato:

OnlineRetail.zip


Por lo tanto:

Descargue el archivo .zip del repositorio.

Descomprímalo.

Coloque el archivo OnlineRetail.csv en la carpeta raíz del proyecto antes de ejecutar el notebook.

🧠 Metodología Aplicada
1️⃣ Limpieza de Datos

Eliminación de registros sin CustomerID

Eliminación de valores negativos en Quantity y UnitPrice

Conversión de fecha (InvoiceDate) usando dayfirst=True

Creación de la variable TotalAmount

2️⃣ Ingeniería de Características – RFM

Se construyen las siguientes variables clave:

Recency: Días desde la última compra

Frequency: Número total de facturas por cliente

Monetary: Total gastado por cliente

Estas métricas permiten evaluar el valor y comportamiento de los clientes.

3️⃣ Análisis Exploratorio (EDA)

Se generan:

Histogramas de distribución

Matriz de correlación

Estadísticos descriptivos

Todos los gráficos se almacenan automáticamente en la carpeta:

../figures

4️⃣ Preprocesamiento

Estandarización con StandardScaler

Preparación de los datos para algoritmos de clustering

5️⃣ Clustering
🔹 K-Means

Selección del número óptimo de clusters mediante:

Método del Codo

Silhouette Score

Segmentación final con k óptimo

🔹 DBSCAN

Identificación de clusters basados en densidad

Detección de clientes atípicos (ruido)

6️⃣ Reducción de Dimensionalidad

Para visualización avanzada:

PCA (2 componentes)

t-SNE

Permite representar los clusters en 2D.

7️⃣ Perfilamiento de Clusters

Se generan archivos CSV con el promedio de:

Recency

Frequency

Monetary

Esto permite interpretar cada segmento de clientes y facilitar la toma de decisiones estratégicas.

📁 Estructura del Proyecto
Proyecto
│
├── OnlineRetail.zip
├── notebooks/
│   └── segmentacion_clientes.ipynb
│
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

🛠️ Requisitos Técnicos

Python 3.9+

Instalar dependencias:

pip install pandas numpy matplotlib seaborn scikit-learn

▶️ Cómo Ejecutar el Proyecto

Descargar el repositorio.

Descomprimir OnlineRetail.zip.

Colocar OnlineRetail.csv en la carpeta raíz.

Asegurarse de que exista la carpeta ../figures.

Ejecutar el notebook completo.

📊 Resultados Esperados

Segmentación clara de clientes.

Identificación de clientes de alto valor.

Detección de clientes inactivos.

Identificación de clientes atípicos.

Visualización clara de clusters en 2D.

📈 Aplicaciones Empresariales

El modelo puede utilizarse para:

Estrategias de fidelización

Campañas segmentadas de marketing

Identificación de clientes VIP

Detección de abandono

Optimización de recursos comerciales

🔍 Conclusiones

K-Means genera segmentos claros y fácilmente interpretables.

DBSCAN permite identificar comportamientos atípicos.

PCA y t-SNE mejoran la visualización.

La metodología RFM es altamente efectiva para análisis comercial.

Este proyecto demuestra la aplicación práctica del Aprendizaje No Supervisado en un caso real de negocio.
