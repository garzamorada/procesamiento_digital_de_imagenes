# Contenido de la Carpeta: 13_trabajo_practico_integrador

Esta carpeta sirve como el repositorio central para el **Trabajo Práctico Integrador** del curso de Procesamiento Digital de Imágenes. Contiene varios subproyectos dedicados a diferentes aspectos de la detección y reconocimiento de texto y objetos, utilizando diversas arquitecturas y frameworks de Deep Learning.

## Índice de Contenidos por Subcarpeta

* [13.1_Reconocimiento_con_TensorFlow_y_Keras](https://github.com/garzamorada/procesamiento_digital_de_imagenes/tree/main/13_trabajo_practico_integrador/13.1_reconocimiento_con_tensorflow_y_keras)
* [13.2_Detector_TensorFlow_y_Keras](https://github.com/garzamorada/procesamiento_digital_de_imagenes/tree/main/13_trabajo_practico_integrador/13.2_deteccion_con_tensorflow_y_keras)
* [13.3_Detector_YOLO](https://github.com/garzamorada/procesamiento_digital_de_imagenes/tree/main/13_trabajo_practico_integrador/13.3_deteccion_con_yolo)
* [13.4_Detector_TensorFlow_Object_Detection_API](https://github.com/garzamorada/procesamiento_digital_de_imagenes/tree/main/13_trabajo_practico_integrador/13.4_tensorflow_object_detection_api)

---

### Contenido de las Subcarpetas

#### **13.1_OCR_Clasificador**

Esta subcarpeta contiene el cuaderno principal del **Proyecto de OCR (Reconocimiento Óptico de Caracteres)**. Se enfoca en la implementación completa de un sistema de reconocimiento de texto a partir de imágenes, abarcando desde la importación de librerías y la gestión de datasets hasta la aplicación de modelos de Deep Learning para el reconocimiento de texto. También se incluye la creación de una interfaz interactiva con Gradio para facilitar la interacción con el modelo.

**Cuadernos principales:**
* `13.1.1_proyecto_ocr_reconocimiento.ipynb`: Desarrollo de un sistema de OCR con Gradio.

#### **13.2_Detector_TF_Keras**

Esta subcarpeta explora la **detección de caracteres y palabras** en imágenes utilizando el framework **TensorFlow y Keras**. Incluye cuadernos dedicados a la detección de caracteres individuales, la detección de palabras completas y una herramienta para probar los modelos entrenados, con integración de interfaces Gradio para visualización.

**Cuadernos principales:**
* `13.2.1_deteccion_tensorflow_keras_letras.ipynb`: Detección de caracteres individuales con TF y Keras.
* `13.2.2_deteccion_tensorflow_keras_palabras.ipynb`: Detección de palabras con TF y Keras.
* `13.2.3_test_deteccion_tensorflow_keras.ipynb`: Cuaderno para probar y demostrar modelos de detección con TF y Keras.

#### **13.3_Detector_YOLO**

Esta subcarpeta se centra en la **detección de texto para OCR** utilizando la arquitectura de modelos **YOLOv8**. Los cuadernos cubren la preparación de datos y el entrenamiento de modelos para la detección de letras y palabras, así como un cuaderno para probar y demostrar la efectividad de un modelo YOLO entrenado en la localización de texto en imágenes.

**Cuadernos principales:**
* `13.3.1_deteccion_con_yolo_v1.ipynb`: Detector de texto basado en YOLOv8 (versión inicial).
* `13.3.2_deteccion_yolo_por_letras.ipynb`: Detección de caracteres individuales con YOLOv8.
* `13.3.3_deteccioon_yolo_por_palabras_v2_mejorado.ipynb`: Detección de palabras mejorada con YOLOv8.
* `13.3.4_test_deteccion_yolo.ipynb`: Cuaderno para probar y demostrar modelos de detección YOLOv8.

#### **13.4_Detector_TensorFlow_OD_API**

Esta subcarpeta contiene cuadernos que guían en el uso de la **TensorFlow Object Detection API** para la detección de objetos. Abarca desde la crucial generación de datos en formato `TF Records` hasta el entrenamiento, exportación y prueba de modelos personalizados de detección. También se incluyen los archivos de configuración esenciales para definir la arquitectura y los parámetros de entrenamiento de los modelos.

**Cuadernos principales:**
* `13.4.1_entrenamiento_tf_od_api.ipynb`: Entrenamiento de modelos con TensorFlow Object Detection API.
* `13.4.2_generador_tf_records.ipynb`: Generación de TF Records para entrenamiento de modelos.
* `13.4.3_generador_tf_records_v2.ipynb`: Generación mejorada de TF Records.
* `13.4.4_test_model_tensorflow_od_api.ipynb`: Cuaderno para probar modelos de detección entrenados con TensorFlow Object Detection API.

---

## Archivos de Configuración

Estos archivos de configuración son fundamentales para definir la arquitectura, los parámetros de entrenamiento y las etiquetas de clase utilizadas por la TensorFlow Object Detection API. Son piezas clave para entrenar y adaptar modelos de detección de objetos a tareas específicas dentro del ecosistema de TensorFlow.

* **`label_map.txt`**
    * **Descripción:** Este archivo define el mapeo entre las etiquetas de clase (nombres de objetos) y sus respectivos IDs numéricos. Es esencial para que el modelo sepa qué representa cada clase detectada y para interpretar los resultados de la inferencia. Suele estar en formato `.pbtxt` y lista cada ítem con su `id` y `name`.

* **`pipeline_ ssd_mobilenet_v2_fpnlite_320x320.config`**
    * **Descripción:** Un archivo de configuración de *pipeline* para un modelo **SSD (Single Shot Detector)** que utiliza un *backbone* **MobileNetV2 FPNLite** y espera imágenes de entrada de **320x320 píxeles**. Define la estructura del modelo, los hiperparámetros del optimizador (ej., tasa de aprendizaje, número total de pasos), las opciones de aumento de datos, y las rutas a *checkpoints* preentrenados para la inicialización (Transfer Learning). Configura `num_classes` y detalles del codificador de cajas.

* **`pipeline_efficientdet_d0.config`**
    * **Descripción:** Este archivo de configuración de *pipeline* es para un modelo de la familia **EfficientDet**, específicamente la versión **D0**. EfficientDet es conocido por su eficiencia y precisión en la detección de objetos. El archivo detalla el extractor de características (`ssd_efficientnet-b0_bifpn_keras`), el redimensionamiento de la imagen (a 320x320 con *padding*), los parámetros de entrenamiento y el uso de `bfloat16`.

* **`pipeline_Faster_R-CNN_Resnet-50_640x640_.config`**
    * **Descripción:** Archivo de configuración para un modelo **Faster R-CNN** con un *backbone* **ResNet-50**, diseñado para imágenes de entrada de **640x640 píxeles**. Faster R-CNN es un detector de dos etapas reconocido por su alta precisión. Este archivo configura el generador de anclas (`anchor_generator`), los umbrales de supresión no máxima (NMS), el optimizador, y las opciones de aumento de datos (`data_augmentation_options`), además de las rutas a `label_map.pbtxt`.

* **`pipeline_ssd_mobilenet_v2_640x640.config`**
    * **Descripción:** Otro archivo de configuración para un modelo **SSD (Single Shot Detector)** con *backbone* **MobileNetV2**, esta vez configurado para imágenes de entrada de **640x640 píxeles**. Define parámetros similares a la versión de 320x320, incluyendo detalles del extractor de características, hiperparámetros para las capas convolucionales y de normalización por lotes, la red de características *Feature Pyramid Network* (FPN), y los parámetros del codificador de cajas y del optimizador de entrenamiento.

---
