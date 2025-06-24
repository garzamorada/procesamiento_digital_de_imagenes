# Contenido de la Carpeta: Detección de Objetos con TensorFlow Object Detection API

Esta carpeta contiene cuadernos de Jupyter (o Colab) que abordan el proceso de **detección de objetos** utilizando la **TensorFlow Object Detection API**. Los cuadernos cubren desde la preparación de los datos en formatos específicos (`TF Records`) hasta el entrenamiento, exportación y prueba de modelos personalizados de detección.

## Índice de Contenidos

* [13.4.1_entrenamiento_tf_od_api](13.4.1_entrenamiento_tf_od_api.ipynb)
* [13.4.2_generador_tf_records](13.4.2_generador_tf_records.ipynb)
* [13.4.3_generador_tf_records_v2](13.4.3_generador_tf_records_v2.ipynb)
* [13.4.4_test_model_tensorflow_od_api](13.4.4_test_model_tensorflow_od_api.ipynb)

---

### 13.4.1_entrenamiento_tf_od_api.ipynb

**Descripción:**
Este cuaderno se enfoca en el **entrenamiento de modelos de detección de objetos** utilizando la **TensorFlow Object Detection API**. Probablemente muestra cómo configurar el entorno, definir la configuración del *pipeline* (incluyendo el modelo base y los hiperparámetros de entrenamiento) y ejecutar el proceso de entrenamiento. Podría incluir comandos para la exportación del modelo entrenado a un formato utilizable para inferencia. El snippet sugiere que está configurado para ejecutarse en un entorno con GPU y usa `model_main_tf2.py` para el entrenamiento.

**Puntos Clave:**
* Configuración del entorno para TensorFlow Object Detection API.
* Entrenamiento de modelos de detección de objetos personalizados.
* Uso del script `model_main_tf2.py` para el proceso de entrenamiento.
* Posiblemente, exportación del modelo entrenado.

---

### 13.4.2_generador_tf_records.ipynb

**Descripción:**
Este cuaderno está dedicado a la **generación de TF Records**, un formato de datos optimizado requerido por la TensorFlow Object Detection API para el entrenamiento. Muestra cómo tomar un dataset de imágenes y sus anotaciones (e.g., cajas delimitadoras y etiquetas) y transformarlo en archivos TFRecord. Es crucial para preparar los datos de entrada para el proceso de entrenamiento de modelos de detección personalizados, incluyendo la visualización de los datos generados con sus *bounding boxes*.

**Puntos Clave:**
* Preparación de datos para la TensorFlow Object Detection API.
* Generación de archivos TFRecord a partir de imágenes y anotaciones.
* Visualización de imágenes con cajas delimitadoras para verificación de datos.
* Funciones para manejar y procesar imágenes y anotaciones.

---

### 13.4.3_generador_tf_records_v2.ipynb

**Descripción:**
Similar al cuaderno anterior, este (`v2`) también se centra en la **generación de TF Records**, pero posiblemente incorpora mejoras o funcionalidades adicionales para la creación de imágenes compuestas y sus anotaciones. Su objetivo es generar un dataset sintético o modificado a partir de imágenes y anotaciones originales para ser usado en el entrenamiento de modelos de detección. El cuaderno detalla cómo componer imágenes grandes a partir de caracteres o elementos más pequeños y cómo generar las etiquetas correspondientes en formato TFRecord.

**Puntos Clave:**
* Generación mejorada de TF Records.
* Creación de imágenes compuestas con múltiples objetos.
* Adaptación de las anotaciones de objetos al nuevo formato compuesto.
* Utilidad para aumentar o adaptar datasets para detección.

---

### 13.4.4_test_model_tensorflow_od_api.ipynb

**Descripción:**
Este cuaderno está diseñado para **probar y demostrar un modelo de detección** entrenado con la TensorFlow Object Detection API. Carga un modelo exportado (probablemente en formato `SavedModel`) y proporciona una función para realizar inferencias en nuevas imágenes. Muestra cómo preprocesar una imagen, ejecutar la detección y visualizar los resultados, incluyendo los cuadros delimitadores y las etiquetas de las clases detectadas. Además, integra una **interfaz Gradio** para permitir a los usuarios subir imágenes y ver las detecciones en tiempo real.

**Puntos Clave:**
* Carga y prueba de modelos de detección de objetos exportados.
* Realización de inferencias en imágenes.
* Visualización de resultados de detección (cajas delimitadoras, etiquetas).
* Integración con Gradio para una demostración interactiva y amigable.

---

---

## Archivos de Configuración

Estos archivos de configuración son fundamentales para definir la arquitectura, los parámetros de entrenamiento y las etiquetas de clase utilizadas por la TensorFlow Object Detection API. Son piezas clave para entrenar y adaptar modelos de detección de objetos a tareas específicas.

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