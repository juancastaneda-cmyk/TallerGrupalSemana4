# Segmentación de Usuarios con Aprendizaje No Supervisado

## 📌 Descripción General

Este proyecto tiene como objetivo implementar y analizar **modelos de aprendizaje no supervisado** para segmentar usuarios de una plataforma digital de servicios personalizados. A partir de datos de navegación, transacciones y comportamiento, se buscan **perfiles representativos de usuarios** que permitan apoyar decisiones de marketing, personalización de servicios y estrategia de negocio.

Se aplican y comparan los siguientes métodos:

* **K-means**
* **DBSCAN**
* **PCA (Principal Component Analysis)**
* **t-SNE (t-distributed Stochastic Neighbor Embedding)**

El enfoque combina análisis estadístico, visualización avanzada y reflexión crítica sobre los resultados obtenidos.

---

## 🎯 Objetivos del Proyecto

### Objetivo General

Implementar y analizar modelos de clustering no supervisado para segmentar perfiles de usuario en un entorno tecnológico.

### Objetivos Específicos

* Explorar y preparar un dataset de comportamiento de usuarios.
* Determinar el número óptimo de clusters mediante métricas adecuadas.
* Comparar el desempeño y resultados de K-means y DBSCAN.
* Utilizar PCA y t-SNE para visualización y reducción de dimensionalidad.
* Interpretar y comunicar los perfiles identificados de forma técnica y visual.

---

## 🧠 Contexto del Caso

Una plataforma digital de servicios personalizados busca comprender mejor el comportamiento de sus usuarios con el fin de:

* Personalizar campañas de marketing.
* Mejorar la experiencia del usuario.
* Incrementar la retención y el valor del cliente.

El equipo de analítica aplica técnicas de aprendizaje no supervisado para descubrir patrones ocultos y segmentar la base de usuarios sin etiquetas previas.

---

## 📂 Estructura del Repositorio

```
Proyecto-Clustering-No-Supervisado/
│── data/               # Dataset utilizado o link de referencia
│── notebooks/          # Jupyter Notebooks con el desarrollo del proyecto
│── src/                # Scripts auxiliares (si aplica)
│── figures/            # Visualizaciones exportadas (PNG/PDF)
│── README.md           # Documentación del proyecto
│── requirements.txt    # Dependencias del entorno
```

---

## ⚙️ Entorno de Trabajo

* **Lenguaje:** Python 3.10+
* **Herramientas:** Jupyter Notebook, VS Code, Git
* **Librerías principales:**

  * numpy
  * pandas
  * matplotlib
  * seaborn
  * scikit-learn

Para instalar las dependencias:

```bash
pip install -r requirements.txt
```

---

## 📊 Dataset

* Dataset validado por el docente.
* Contiene variables numéricas relacionadas con:

  * Frecuencia de uso
  * Tiempo de sesión
  * Transacciones
  * Monto promedio
  * Interacciones con la plataforma

**Nota:** Si el dataset no se incluye directamente en el repositorio, se proporciona el enlace de origen en la carpeta `/data`.

---

## 🔍 Análisis Exploratorio de Datos (EDA)

Se realizó:

* Análisis estadístico descriptivo.
* Visualización de distribuciones (histogramas, boxplots).
* Análisis de correlación mediante heatmaps.
* Limpieza de datos y eliminación de variables irrelevantes.
* Escalado de variables para garantizar un desempeño adecuado de los modelos.

---

## 🤖 Modelos Implementados

### K-means

* Aplicación de escalado previo.
* Selección del número óptimo de clusters mediante:

  * Método del codo (Elbow Method).
  * Silhouette Score.
* Asignación de etiquetas y análisis de centroides.

### DBSCAN

* Ajuste de hiperparámetros `eps` y `min_samples`.
* Identificación de ruido (outliers).
* Comparación directa con K-means.

### PCA

* Reducción de dimensionalidad.
* Análisis de varianza explicada.
* Proyección de los datos a 2 dimensiones para visualización.

### t-SNE

* Reducción no lineal para detección de estructuras complejas.
* Visualización de clusters latentes.
* Comparación visual con PCA.

---

## 📈 Visualización de Resultados

* Comparación gráfica entre clusters generados por K-means y DBSCAN.
* Visualizaciones 2D utilizando PCA y t-SNE coloreadas por cluster.
* Tabla resumen con estadísticas promedio por cluster.

Las visualizaciones exportadas se encuentran en la carpeta `/figures`.

---

## 🧩 Resultados y Análisis

* Se identificaron distintos perfiles de usuario con comportamientos diferenciados.
* K-means mostró clusters más compactos y fáciles de interpretar.
* DBSCAN permitió identificar ruido y usuarios atípicos.
* PCA facilitó la interpretación global, mientras que t-SNE reveló estructuras más complejas.

---

## ⚠️ Limitaciones

* Sensibilidad de los modelos al escalado y a los hiperparámetros.
* Interpretabilidad limitada en métodos no lineales como t-SNE.
* Dependencia de la calidad y representatividad del dataset.

---

## 🚀 Propuestas de Mejora

* Aplicar clustering jerárquico.
* Realizar ingeniería de características más avanzada.
* Integrar validación con expertos de negocio.
* Probar técnicas de clustering basadas en densidad adicionales.

---

## 📦 Entregables

* Repositorio colaborativo en GitHub/GitLab.
* Código fuente (.ipynb / .py).
* Dataset o enlace de referencia.
* Documentación completa (README.md).
* Visualizaciones exportadas.
* Presentación técnica (5–10 minutos).

---

## 📚 Recursos

* Documentación oficial de Scikit-learn – Clustering
* Guías de PCA y t-SNE

---

## ✍️ Autores

Proyecto desarrollado con fines académicos como parte del curso de **Machine Learning / Inteligencia Artificial**.
