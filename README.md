# Trabajo-final---Deep-Learning
# Clasificación de Imágenes – Intel Dataset (Machine Learning 2)

## Descripción del proyecto

Este proyecto tiene como objetivo desarrollar y comparar diferentes modelos de **Deep Learning** para la clasificación de imágenes en distintas categorías de paisajes naturales y urbanos.

Se implementaron múltiples arquitecturas de redes neuronales convolucionales (CNN), incluyendo enfoques tradicionales y técnicas avanzadas como **Transfer Learning** y **conexiones residuales**, con el fin de evaluar su desempeño y capacidad de generalización.

---

## Problema de Machine Learning

El problema abordado corresponde a una tarea de **clasificación multiclase de imágenes**, donde cada imagen debe ser asignada a una de las siguientes categorías:

* 🌆 buildings
* 🌲 forest
* 🏔 mountain
* 🌊 sea
* 🧊 glacier
* 🛣 street

Se trata de un problema supervisado, donde el modelo aprende a partir de imágenes etiquetadas.

---

## Dataset

Se utilizó el **Intel Image Classification Dataset**, que contiene imágenes organizadas en carpetas por clase.

* 📁 Total imágenes entrenamiento: ~14,000
* 📁 Clases: 6
* 📏 Tamaño de imagen: redimensionadas a 128x128

El dataset se descarga automáticamente desde Google Drive dentro del notebook.

---

## Tecnologías utilizadas

* Python 
* TensorFlow / Keras
* NumPy, Pandas
* Matplotlib, Seaborn
* Google Colab

---

## Modelos implementados

Se desarrollaron y compararon los siguientes modelos:

### Modelo 1 – CNN Básica

* Arquitectura simple con capas convolucionales y pooling
* Sirve como línea base

---

### Modelo 2 – CNN Mejorada

* Incluye:

  * Batch Normalization
  * Dropout
* Mejora la estabilidad y reduce overfitting

---

### Modelo 3 – CNN con Conexiones Residuales

* Inspirado en arquitecturas tipo ResNet
* Implementa conexiones residuales mediante suma de capas
* Mejora el flujo de información en la red

---

### Modelo 4 – Transfer Learning

* Basado en **MobileNetV2**
* Capas preentrenadas congeladas
* Mejor desempeño general

---

## Resultados

| Modelo            | Accuracy     |
| ----------------- | ------------ |
| CNN Básica        | ~0.80        |
| CNN Mejorada      | ~0.60 – 0.62 |
| CNN Residual      | ~0.70 – 0.73 |
| Transfer Learning | ~0.88 – 0.90 |

---

## Conclusiones

* El **Transfer Learning** obtuvo el mejor desempeño.
* Aumentar la complejidad del modelo no garantiza mejores resultados.
* Las **conexiones residuales** ayudan a estabilizar el entrenamiento.
* El uso de **Early Stopping** permitió evitar sobreajuste y reducir tiempos de entrenamiento.

---

## Cómo ejecutar el proyecto

### Opción recomendada: Google Colab

1. Abrir el notebook en Google Colab
2. Activar GPU:

```
Entorno de ejecución → Cambiar tipo de entorno → GPU (T4 recomendado)
```

---

## Recomendaciones IMPORTANTES

### Uso de GPU

* Se recomienda usar **GPU T4**
* Reduce significativamente el tiempo de entrenamiento

---

### Tiempo de ejecución

* Cada modelo puede tardar aproximadamente:

  *  **8 – 10 minutos**
* El proyecto completo puede tardar:

  *  **30 – 40 minutos**

 Tener paciencia durante el entrenamiento

---

###  Early Stopping

* Algunos modelos pueden detenerse antes de completar todas las épocas
* Esto es normal y evita sobreentrenamiento

---

### Resultados variables

* Los resultados pueden cambiar ligeramente en cada ejecución
* Esto se debe a:

  * Inicialización aleatoria
  * Data augmentation
  * Dropout

---

## Funcionalidades adicionales

* Visualización de imágenes del dataset
* Predicción de imágenes individuales
* Matriz de confusión
* Reportes de clasificación (precision, recall, F1-score)

---

## Notas finales

Este proyecto demuestra la aplicación de técnicas modernas de Deep Learning para problemas de visión por computador, destacando la importancia del diseño experimental y la comparación entre modelos.

---
