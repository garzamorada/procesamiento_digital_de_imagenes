# Contenido de la Carpeta: Detección de Caracteres y Palabras con TensorFlow y Keras

Esta carpeta contiene una serie de cuadernos de Jupyter (o Colab) que exploran la **detección de objetos** en el contexto de texto, específicamente la identificación de caracteres individuales y palabras en imágenes, utilizando el framework TensorFlow y Keras. Además, incluye un cuaderno para probar y demostrar estas capacidades de detección.

## Índice de Contenidos

* [13.2.1_deteccion_tensorflow_keras_letras](13.2.1_deteccion_tensorflow_keras_letras.ipynb)
* [13.2.2_deteccion_tensorflow_keras_palabras](13.2.2_deteccion_tensorflow_keras_palabras.ipynb)
* [13.2.3_test_deteccion_tensorflow_keras](13.2.3_test_deteccion_tensorflow_keras.ipynb)

---

### 13.2.1_deteccion_tensorflow_keras_letras.ipynb

**Descripción:**
Este cuaderno se enfoca en la **detección de caracteres individuales** en imágenes utilizando TensorFlow y Keras. Aborda los pasos fundamentales para preparar un conjunto de datos (importación, funciones auxiliares, carga del dataset, aumento de datos) y construir o entrenar un modelo capaz de identificar y localizar letras. Es probable que demuestre la generación de cuadros delimitadores (bounding boxes) alrededor de cada carácter detectado y que incluya una interfaz Gradio para una interacción sencilla.

**Puntos Clave:**
* Detección de caracteres individuales.
* Preparación y aumento de datos para modelos de detección.
* Uso de TensorFlow y Keras para la implementación.
* Posible integración con Gradio para demostraciones interactivas.

---

### 13.2.2_deteccion_tensorflow_keras_palabras.ipynb

**Descripción:**
Similar al cuaderno anterior, este notebook se centra en la **detección de palabras completas** en imágenes, también con TensorFlow y Keras. Sigue un flujo de trabajo de Machine Learning que incluye la importación de librerías, definición de funciones auxiliares, carga del dataset y técnicas de aumento de datos. La distinción clave reside en que el modelo está configurado para detectar grupos de caracteres que forman palabras, generando sus respectivos cuadros delimitadores. También presenta una interfaz Gradio para facilitar la interacción con el modelo de detección de palabras.

**Puntos Clave:**
* Detección de palabras en imágenes.
* Preparación y aumento de datos adaptados a la detección de palabras.
* Implementación con TensorFlow y Keras.
* Interfaz Gradio para visualizar las detecciones de palabras.

---

### 13.2.3_test_deteccion_tensorflow_keras.ipynb

**Descripción:**
Este cuaderno está diseñado para **probar y demostrar un modelo de detección** (probablemente de caracteres o palabras) previamente entrenado utilizando TensorFlow y Keras. El cuaderno carga un modelo existente y define una función clave `detectar_caracteres` que toma una imagen, procesa la predicción del modelo (interpretando la "objectness" y las coordenadas relativas), y dibuja cuadros delimitadores sobre los objetos detectados. La funcionalidad se encapsula en una **interfaz Gradio** que permite a los usuarios subir imágenes y visualizar en tiempo real los resultados de la detección, actuando como una herramienta de demostración interactiva.

**Puntos Clave:**
* Carga y prueba de modelos de detección preentrenados.
* Función para interpretar las predicciones del modelo y dibujar cuadros delimitadores.
* Utilización de Gradio para una interfaz de demostración interactiva.
* Visualización en tiempo real de la detección de objetos en imágenes.

---