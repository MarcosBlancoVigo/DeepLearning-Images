# 🚢 Ship Detection from Aerial Images

Este proyecto tiene como objetivo aplicar técnicas de **Análisis Exploratorio de Datos (EDA)**, **Machine Learning clásico**, y **Deep Learning** para resolver el problema de la **detección de barcos en imágenes aéreas**. Utilizamos un dataset proveniente de Kaggle que contiene imágenes aéreas del mar con barcos visibles, con el fin de:

- Clasificar imágenes según presencia de barcos
- Detectar la ubicación de los barcos en las imágenes
- Explorar técnicas de generación y procesamiento de imágenes

---

## 📁 Estructura del Proyecto
hip-detection-project/ │ ├── data/ # Dataset original y procesado │ ├── raw/ # Imágenes originales del dataset │ └── processed/ # Imágenes redimensionadas / augmentadas │ ├── notebooks/ # Notebooks principales del proyecto │ ├── 01_EDA.ipynb # Exploración de datos │ ├── 02_ML_Baseline.ipynb # Pruebas con ML clásico │ ├── 03_DL_Classification.ipynb # Modelos de clasificación con DL │ ├── 04_DL_ObjectDetection.ipynb # Modelos de detección de objetos │ └── 05_ImageToImage.ipynb # Generación de imágenes │ ├── models/ # Modelos entrenados guardados │ ├── utils/ # Funciones auxiliares │ ├── preprocessing.py # Funciones de preprocesamiento │ └── visualizations.py # Funciones de visualización │ ├── requirements.txt # Librerías necesarias └── README.md # Este archivo
