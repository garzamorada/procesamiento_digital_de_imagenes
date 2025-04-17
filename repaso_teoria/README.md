# Repositorio de Cuadernos de Colab sobre Procesamiento de Imágenes

Este repositorio contiene cuadernos de Colab diseñados para explorar y aprender diferentes aspectos del procesamiento de imágenes utilizando Python y bibliotecas populares como PIL (Pillow), scikit-image y scipy.

## Índice de Cuadernos

1.  [Introduccion a Pil/Pillow](introduccion_pil-pillow.ipynb)
2.  [Ejemplos de usoa de scikit-image y scipy](ejemplos_de_uso_scikit-image_scupy.ipynb)
3.  [Ejemplos de uso de Pil/Pillow](ejemplos_de_uso_de_pil-pillow.ipynb)

## Descripción de los Cuadernos

### 1. [Lectura, Guardado y Visualización de Imágenes con PIL/Pillow](#lectura-guardado-y-visualización-de-imágenes-con-pilpillow)

   **Descripción:**
   Este cuaderno introduce los fundamentos de la manipulación de imágenes utilizando la biblioteca PIL (Pillow). Aprenderás a cargar, guardar y visualizar imágenes en diferentes formatos. Se cubren las operaciones básicas como mostrar imágenes en Colab y entender los diferentes modos de apertura de imágenes.

   **Instrucciones de Uso:**
   1.  Asegúrate de tener la biblioteca PIL (Pillow) instalada.  En Colab, esto generalmente está preinstalado.
   2.  Ejecuta las celdas de código en orden para cargar y mostrar las imágenes.
   3.  Experimenta con diferentes rutas de archivos para cargar tus propias imágenes.
   4.  Presta atención a las diferencias entre los modos de apertura de imágenes (e.g., 'r', 'w', 'rb', 'wb').
   5.  Utiliza las funciones de `matplotlib.pyplot` para visualizar las imágenes y entender cómo interactúan con PIL.

### 2. [Procesamiento de Imágenes con scikit-image y scipy](#procesamiento-de-imágenes-con-scikit-image-y-scipy)

   **Descripción:**
   Este cuaderno se enfoca en el procesamiento de imágenes usando las bibliotecas scikit-image y scipy.  Aprenderás a realizar conversiones entre diferentes espacios de color, manejar formatos de imágenes y trabajar con estructuras de datos específicas para imágenes. Se exploran temas como la conversión de imágenes entre PIL y NumPy.

   **Instrucciones de Uso:**
   1.  Instala las bibliotecas scikit-image y scipy ejecutando la celda de instalación (`!pip install scikit-image scipy`).
   2.  Sigue las celdas en orden para entender cómo se manipulan las imágenes con estas bibliotecas.
   3.  Presta especial atención a las conversiones entre espacios de color (RGB, HSV, etc.) y cómo afectan la representación de la imagen.
   4.  Observa cómo se convierten las imágenes entre objetos PIL y arrays de NumPy.
   5.  Utiliza el resumen de funciones clave al final del cuaderno como referencia rápida.

### 3. [Visualización de Múltiples Imágenes y Ajuste de Interpolación](#visualización-de-múltiples-imágenes-y-ajuste-de-interpolación)

   **Descripción:**
   Este cuaderno se centra en la visualización de múltiples imágenes en una misma figura y en el ajuste de la interpolación al mostrar imágenes. Aprenderás a usar `matplotlib` para crear subplots y a controlar la apariencia de las imágenes mediante diferentes métodos de interpolación.

   **Instrucciones de Uso:**
   1.  Ejecuta las celdas para generar y visualizar las imágenes.
   2.  Experimenta con los diferentes métodos de interpolación (`'none'`, `'nearest'`, `'bilinear'`, etc.) para ver cómo afectan la calidad de la imagen mostrada.
   3.  Modifica el código para mostrar diferentes conjuntos de imágenes o ajustar los parámetros de los subplots.
   4.  Presta atención a las notas clave sobre el contexto de la interpolación y su impacto en la visualización.

---

¡Espero que estos cuadernos te sean de gran utilidad! Si tienes alguna pregunta o sugerencia, no dudes en abrir un issue en este repositorio.
