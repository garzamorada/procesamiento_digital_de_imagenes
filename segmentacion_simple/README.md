# Segmentación Simple por Color

Este notebook de Colab proporciona un ejemplo introductorio de segmentación de imágenes basado en el color.

## Descripción

La segmentación de imágenes es el proceso de particionar una imagen digital en múltiples segmentos (conjuntos de píxeles). La segmentación por color utiliza la información del color de los píxeles para agruparlos en regiones. Este notebook demuestra un método simple para segmentar una imagen identificando píxeles dentro de un rango de color específico.

## Contenido

El notebook incluye las siguientes secciones:

1.  **Bibliotecas necesarias:** Importa las librerías `numpy`, `cv2` (OpenCV), `matplotlib.pyplot` y `cv2_imshow` (para mostrar imágenes en Colab).
2.  **Función `info_img(img)`:**
    * **Descripción:** Imprime información sobre las dimensiones y los valores máximo y mínimo de la imagen.
    * **Parámetros:**
        * `img`: La imagen de entrada (array de NumPy).
    * **Funcionamiento:** Utiliza `img.shape` para obtener las dimensiones, `img.max()` para el valor máximo y `img.min()` para el valor mínimo.
3.  **Carga de la imagen:** Carga una imagen utilizando `cv2.imread()`.
4.  **Conversión de espacio de color:** Convierte la imagen del espacio de color BGR (predeterminado en OpenCV) al espacio de color HSV (Matiz, Saturación, Valor). El espacio HSV es a menudo más intuitivo para la segmentación basada en el color.
5.  **Definición de rangos de color:** Define los rangos de color (en HSV) que se utilizarán para la segmentación. Se definen los límites inferior y superior para el color deseado.
6.  **Creación de una máscara:** Utiliza `cv2.inRange()` para crear una máscara binaria. Los píxeles que caen dentro del rango de color definido se marcan como blancos (255), y los píxeles fuera del rango se marcan como negros (0).
7.  **Aplicación de la máscara:**
    * Utiliza `cv2.bitwise_and()` para extraer la región de la imagen original que corresponde a la máscara (los píxeles dentro del rango de color).
    * Crea una imagen de fondo negro y copia la región segmentada en ella.
8.  **Mostrar resultados:** Muestra la imagen original, la máscara y la imagen segmentada.

## Cómo utilizar

1.  **Abrir en Colab:** Abre este notebook en Google Colaboratory.
2.  **Ejecutar las celdas:** Ejecuta las celdas en orden secuencial.
    * La primera celda importa las librerías.
    * Las celdas siguientes definen la función `info_img`, cargan la imagen, convierten el espacio de color, definen los rangos de color, crean la máscara, aplican la máscara y muestran los resultados.
3.  **Experimentar:**
    * **Modificar los rangos de color:** Cambia los valores de `lower_bound` y `upper_bound` para segmentar diferentes colores en la imagen. Recuerda que estos valores están en el espacio de color HSV.
    * **Cargar diferentes imágenes:** Cambia la ruta del archivo para cargar y segmentar diferentes imágenes.

## Dependencias

* `numpy`
* `cv2` (OpenCV)
* `matplotlib.pyplot`
* `google.colab.patches` (para `cv2_imshow` en Colab)

Estas librerías generalmente están preinstaladas en Google Colab.

## Notas adicionales

* La segmentación por color es una técnica simple pero efectiva para aislar objetos en imágenes con fondos de color contrastante.
* En los ejemplos del gato y el auto utilicé blur y reduccion de tonos para mejorar la segmentacion.
* Ajustar los rangos de color es crucial para obtener buenos resultados de segmentación.
