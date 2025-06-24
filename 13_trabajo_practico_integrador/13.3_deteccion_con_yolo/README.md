# Contenido de la Carpeta: Detección de Texto con YOLOv8 para OCR

Esta carpeta contiene una serie de cuadernos de Jupyter (o Colab) que exploran la **detección de texto** en imágenes utilizando el modelo **YOLOv8** para aplicaciones de Reconocimiento Óptico de Caracteres (OCR). Los cuadernos cubren desde la preparación de datos y el entrenamiento de modelos para la detección de letras y palabras, hasta la prueba y demostración de las capacidades de un modelo YOLO entrenado.

## Índice de Contenidos

* [13.3.1_deteccion_con_yolo_v1](13.3.1_deteccion_con_yolo_v1.ipynb)
* [13.3.2_deteccion_yolo_por_letras](13.3.2_deteccion_yolo_por_letras.ipynb)
* [13.3.3_deteccioon_yolo_por_palabras_v2_mejorado](13.3.3_deteccioon_yolo_por_palabras_v2_mejorado.ipynb)
* [13.3.4_test_deteccion_yolo](13.3.4_test_deteccion_yolo.ipynb)

---

### 13.3.1_deteccion_con_yolo_v1.ipynb

**Descripción:**
Este cuaderno introduce un **detector de texto para OCR** basado en la arquitectura **YOLOv8**. El objetivo es identificar la presencia de texto en una imagen y, potencialmente, extraer líneas de texto y las cajas delimitadoras de los caracteres que las componen. El cuaderno detalla los pasos para la preparación del dataset, incluyendo el reescalado de imágenes y cajas delimitadoras, la conversión al formato esperado por YOLO, y la configuración necesaria para el entrenamiento de un modelo YOLOv8.

**Puntos Clave:**
* Introducción a la detección de texto con YOLOv8.
* Preparación de datos y conversión al formato YOLO.
* Configuración del entorno y entrenamiento del modelo.
* Orientado a la detección de la presencia general de texto.

---

### 13.3.2_deteccion_yolo_por_letras.ipynb

**Descripción:**
Este cuaderno profundiza en la **detección de texto por caracteres individuales** utilizando un modelo basado en **YOLOv8** para OCR. Aborda la importación de librerías, la preparación específica de datos para la detección de letras y el entrenamiento del modelo YOLO para esta tarea. Incluye la visualización de métricas de entrenamiento, como las curvas de mAP (mean Average Precision) y de pérdida, para evaluar el rendimiento del modelo en la detección a nivel de carácter.

**Puntos Clave:**
* Detección de caracteres individuales con YOLOv8.
* Preparación específica de datasets para detección de letras.
* Entrenamiento de modelos YOLO para reconocimiento de caracteres.
* Visualización y análisis de métricas de entrenamiento (mAP, curvas de pérdida).

---

### 13.3.3_deteccioon_yolo_por_palabras_v2_mejorado.ipynb

**Descripción:**
Este cuaderno presenta una versión mejorada (v2) del **detector de texto por palabras** basado en **YOLOv8**. El objetivo es detectar la presencia de texto y, en particular, identificar y delimitar palabras completas en una imagen para fines de OCR. Se enfoca en la preparación avanzada de datos y el entrenamiento de un modelo YOLOv8 optimizado para esta tarea, buscando mejorar la precisión en la localización de palabras y, posiblemente, en la extracción de las cajas de caracteres dentro de ellas.

**Puntos Clave:**
* Detección de palabras utilizando YOLOv8 (versión mejorada).
* Preparación de datos para la detección de palabras.
* Entrenamiento y optimización del modelo YOLOv8.
* Orientado a la detección de unidades de texto a nivel de palabra.

---

### 13.3.4_test_deteccion_yolo.ipynb

**Descripción:**
Este cuaderno está diseñado para **probar y demostrar las capacidades de un modelo de detección YOLOv8** previamente entrenado. Permite cargar un modelo (`.pt`), realizar inferencias en imágenes de ejemplo y visualizar los resultados, incluyendo los cuadros delimitadores (bounding boxes) detectados y sus puntuaciones de confianza. Es una herramienta práctica para evaluar el rendimiento del modelo en escenarios reales y observar cómo identifica texto o palabras en nuevas imágenes.

**Puntos Clave:**
* Carga de modelos YOLOv8 preentrenados.
* Realización de inferencias en nuevas imágenes.
* Visualización de cuadros delimitadores y confianza de detección.
* Demostración práctica de las capacidades del modelo YOLO.

---