# 🚢 Ship Detection from Aerial Images

Este proyecto tiene como objetivo aplicar técnicas de **Análisis Exploratorio de Datos (EDA)**, **Machine Learning clásico**, y **Deep Learning** para resolver el problema de la **detección de barcos en imágenes aéreas**. Utilizamos un dataset proveniente de Kaggle que contiene imágenes aéreas del mar con barcos visibles, con el fin de:

- Clasificar imágenes según presencia de barcos  
- Detectar la ubicación de los barcos en las imágenes   

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
│   ├── MASATI/                      
│       ├── output
│           ├── test
│                ├── images              # Imágenes de test
│                └── labels              # Etiquetas de las fotos de test
│           ├── train
│                ├── images              # Imágenes de train
│                └── labels              # Etiquetas de las fotos de train
│           └── val             
│                ├── images              # Imágenes de validation
│                └── labels              # Etiquetas de las fotos de validation
│
├── code/                   
│   └── Code.ipynb                       # Código completo
│
├── requirements.txt                     # Librerías necesarias
├── data.yml                             # Estructura del dataset
└── README.md                            # Documentación principal
```

---

## 📊 Análisis Exploratorio de Datos (EDA)

Se realizó un análisis detallado de las imágenes del dataset:

- **Distribución de tamaños** de imágenes (ancho, alto)  
- **Distribución de clases** (presencia o ausencia de barcos)  
- **Histogramas de color** para entender los valores predominantes   

> 📌 Este paso permite definir las transformaciones necesarias para los modelos y comprender posibles problemas como el desbalanceo de clases o tamaños dispares.

---

## 🤖 Machine Learning Clásico

Como baseline, se probaron modelos de clasificación simples con extracción de características tradicionales:
  
- Modelos evaluados:  
  - Support Vector Machines (SVM)   

> 🔍 Este modelo sirve como línea base para comparar el desempeño de los modelos de Deep Learning posteriores.

---

## 🧠 Deep Learning - Clasificación de Imágenes

Entrenamos modelos de redes neuronales convolucionales (CNN) para clasificar imágenes:

### Modelos

- **CNN desde cero** con Keras/TensorFlow   

### Evaluación

- Curvas de **accuracy y loss**  
- Evaluación de **overfitting** y regularización  
- Métricas: precisión, recall, F1-score  

---

## 🕵️‍♀️ Deep Learning - Detección de Objetos

Implementamos detección de barcos en imágenes usando modelos de object detection:

- **YOLOv5** con PyTorch  
- **TensorFlow Object Detection API**  
- Evaluación con mAP (mean Average Precision)

---
