# Ejercicios sobre Color

Este notebook de Colab contiene ejercicios prácticos relacionados con el procesamiento y la manipulación de color en imágenes digitales.

## Descripción

El objetivo de este notebook es proporcionar una serie de ejercicios que demuestren cómo trabajar con imágenes a color, incluyendo la separación de canales, la visualización de histogramas y el análisis de la información de color.

## Contenido

El notebook incluye las siguientes secciones:

1.  **Importar librerías:** Importa las librerías necesarias como `cv2`, `matplotlib.pyplot` y `numpy`. También importa `cv2_imshow` de `google.colab.patches` para mostrar imágenes en Colab.
2.  **Cargar Imagen:** Descarga y carga una imagen desde una URL.
3.  **Funciones:**
    * `muestraCanales(imagen_rgb)`:  Esta función toma una imagen RGB y realiza las siguientes operaciones:
        * Muestra la imagen original RGB.
        * Separa la imagen en sus canales Azul, Verde y Rojo.
        * Muestra cada canal en escala de grises.
        * Muestra cada canal con su respectivo mapa de color (Azul, Verde, Rojo).
        * Calcula y muestra el histograma de cada canal.
4.  **Llamada a la función `muestraCanales`:** Se llama a la función `muestraCanales` para procesar la imagen cargada y mostrar los resultados.

## Cómo utilizar

1.  **Abrir en Colab:** Abre este notebook en Google Colaboratory.
2.  **Ejecutar las celdas:** Ejecuta las celdas en orden secuencial.
    * La primera celda instala las librerías necesarias.
    * La segunda celda descarga y carga la imagen.
    * La tercera celda define la función `muestraCanales`.
    * La última celda llama a la función para procesar la imagen.
3.  **Experimentar:** Puedes modificar la URL de la imagen para procesar diferentes imágenes. Puedes también modificar la función `muestraCanales` para realizar otras operaciones de procesamiento de color.

## Dependencias

* `cv2` (OpenCV)
* `matplotlib.pyplot`
* `numpy`
* `google.colab.patches` (para `cv2_imshow` en Colab)

Estas librerías generalmente están preinstaladas en Google Colab.

## Notas adicionales

* Este notebook es una buena introducción a la manipulación de canales de color en imágenes.
* Los histogramas proporcionan información valiosa sobre la distribución de los colores en la imagen.

--------------------------------------------------------------------------
# Trabajo con Canales de Color: HSV, HLS y YUV

Este notebook de Colab explora diferentes espacios de color más allá del tradicional RGB, específicamente HSV, HLS e YUV, y cómo trabajar con sus canales individuales.

## Descripción

Las imágenes digitales se representan comúnmente en el espacio de color RGB (Rojo, Verde, Azul). Sin embargo, otros espacios de color son útiles para ciertas tareas de procesamiento de imágenes. Este notebook demuestra cómo convertir imágenes entre RGB y otros espacios de color (HSV, HLS, YUV) y cómo visualizar y analizar los canales individuales de estos espacios.

## Contenido

El notebook incluye las siguientes secciones:

1.  **Instalación e Importación de Bibliotecas:** Instala e importa las librerías necesarias: `cv2` (OpenCV), `numpy`, `google.colab.patches` (para `cv2_imshow` en Colab) y `matplotlib.pyplot`.
2.  **Carga de la imagen:** Carga una imagen utilizando `cv2.imread()`.
3.  **Conversión a Espacios de Color:**
    * Convierte la imagen RGB a los espacios de color HSV, HLS e YUV utilizando `cv2.cvtColor()`.
4.  **Visualización de Canales:**
    * Para cada espacio de color (RGB, HSV, HLS, YUV), el notebook:
        * Separa la imagen en sus canales individuales utilizando `cv2.split()`.
        * Muestra la imagen original.
        * Muestra cada canal en escala de grises.
        * Muestra el histograma de cada canal utilizando `matplotlib.pyplot.hist()`.

## Cómo utilizar

1.  **Abrir en Colab:** Abre este notebook en Google Colaboratory.
2.  **Ejecutar las celdas:** Ejecuta las celdas en orden secuencial.
    * La primera celda instala e importa las librerías.
    * Las celdas siguientes cargan la imagen, la convierten a diferentes espacios de color y visualizan los canales.
3.  **Experimentar:**
    * **Cargar diferentes imágenes:** Modifica la ruta del archivo para cargar y procesar otras imágenes.
    * **Analizar los histogramas:** Observa cómo se distribuyen los valores de los píxeles en los diferentes canales y espacios de color. Esto puede proporcionar información sobre las características de la imagen (por ejemplo, brillo, saturación, etc.).

## Dependencias

* `opencv-python`
* `numpy`
* `google.colab.patches`
* `matplotlib.pyplot`

Estas librerías generalmente están preinstaladas en Google Colab, excepto `opencv-python` que se instala en la primera celda.

## Notas adicionales

* **HSV (Matiz, Saturación, Valor):** Es útil para la segmentación de color y el ajuste del color.
* **HLS (Matiz, Luminosidad, Saturación):** Similar a HSV, pero Luminosidad reemplaza a Valor.
* **YUV:** Se utiliza en la transmisión de video, ya que separa la información de luminancia (Y) de la información de crominancia (U, V).
* Los histogramas son representaciones gráficas de la distribución de la intensidad de los píxeles en una imagen.
