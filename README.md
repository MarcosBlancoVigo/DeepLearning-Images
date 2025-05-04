# 🚢 Ship Detection from Aerial Images

Este proyecto tiene como objetivo aplicar técnicas de **Análisis Exploratorio de Datos (EDA)**, **Machine Learning clásico**, y **Deep Learning** para resolver el problema de la **detección de barcos en imágenes aéreas**. Utilizamos un dataset proveniente de Kaggle que contiene imágenes aéreas del mar con barcos visibles, con el fin de:

- Clasificar imágenes según presencia de barcos  
- Detectar la ubicación de los barcos en las imágenes  
- Explorar técnicas de generación y procesamiento de imágenes  

---

## 📦 Requisitos

Crea un entorno con Python 3.12.

Instala las dependencias necesarias con:

```
pip install -r requirements.txt
```

O si usas Anaconda:

```
conda env create --file requirements.txt
```

Además, deberás instalar la librería pytorch y torchvision según tu sistema operativo y GPU. Puedes encontrar las instrucciones en la [página oficial de PyTorch](https://pytorch.org/get-started/locally/).

---

## 📁 Estructura del Proyecto

```
ship-detection-project/
│
├── data/                         
│   ├── raw/                      # Imágenes originales del dataset
│   └── processed/                # Imágenes redimensionadas / aumentadas
│
├── notebooks/                   
│   ├── 01_EDA.ipynb                      # Análisis exploratorio
│   ├── 02_ML_Baseline.ipynb             # Machine Learning clásico
│   ├── 03_DL_Classification.ipynb       # Deep Learning - Clasificación
│   ├── 04_DL_ObjectDetection.ipynb      # Deep Learning - Detección de objetos
│   └── 05_ImageToImage.ipynb            # Image-to-Image translation
│
├── models/                              # Modelos entrenados guardados
│   ├── cnn_model.h5
│   └── yolov5_best.pt
│
├── utils/                               
│   ├── preprocessing.py                 # Funciones para limpiar y procesar datos
│   └── visualizations.py                # Funciones de graficado y visualización
│
├── outputs/                             # Métricas, gráficos, predicciones
│   ├── classification_reports/
│   └── detection_results/
│
├── requirements.txt                     # Librerías necesarias
├── README.md                            # Documentación principal
└── LICENSE                              # Licencia (MIT u otra)
```

---

## 📊 Análisis Exploratorio de Datos (EDA)

Se realizó un análisis detallado de las imágenes del dataset:

- **Distribución de tamaños** de imágenes (ancho, alto)  
- **Distribución de clases** (presencia o ausencia de barcos)  
- **Histogramas de color** para entender los valores predominantes  
- Visualización de la **intensidad de píxeles**  
- Análisis de relaciones espaciales y patrones recurrentes  

> 📌 Este paso permite definir las transformaciones necesarias para los modelos y comprender posibles problemas como el desbalanceo de clases o tamaños dispares.

---

## 🤖 Machine Learning Clásico

Como baseline, se probaron modelos de clasificación simples con extracción de características tradicionales:

- **Extracción de features** con Histogramas, HOG, y ResNet (feature extractor)  
- Modelos evaluados:  
  - Support Vector Machines (SVM)  
  - Random Forest  
  - Logistic Regression  

> 🔍 Estos modelos sirven como línea base para comparar el desempeño de los modelos de Deep Learning posteriores.

---

## 🧠 Deep Learning - Clasificación de Imágenes

Entrenamos modelos de redes neuronales convolucionales (CNN) para clasificar imágenes:

### Modelos

- **CNN desde cero** con Keras/TensorFlow  
- **Transfer Learning** usando:  
  - ResNet50  
  - MobileNetV2  
  - EfficientNet  

### Evaluación

- Curvas de **accuracy y loss**  
- Evaluación de **overfitting** y regularización  
- Métricas: precisión, recall, F1-score  

> 📈 Los modelos preentrenados mostraron mejor generalización y desempeño más robusto.

---

## 🕵️‍♀️ Deep Learning - Detección de Objetos

Implementamos detección de barcos en imágenes usando modelos de object detection:

- **YOLOv5** con PyTorch  
- **TensorFlow Object Detection API**  
- Evaluación con mAP (mean Average Precision)

---
