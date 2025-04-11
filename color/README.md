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

----------------------------------------------------------------------------------------------------------------------

# Cuantización por Canales de Color

Este notebook de Colab explora el efecto de la cuantización en imágenes digitales, específicamente cómo afecta a los diferentes canales de color (Azul, Verde y Rojo - BGR).

## Descripción

El objetivo principal es visualizar y comprender cómo la reducción del número de tonos disponibles (cuantización) impacta la apariencia de una imagen y cómo este impacto varía entre los canales de color. El notebook carga una imagen, la procesa para separar sus canales de color, y luego aplica la cuantización con diferentes niveles de tonos. Finalmente, muestra las imágenes resultantes y sus histogramas.

## Contenido

El notebook incluye las siguientes secciones:

1.  **Importación de Librerías:** Importa las librerías necesarias como `numpy`, `cv2` (OpenCV) y `matplotlib.pyplot`.
2.  **Obtención de Imagen:** Descarga y carga una imagen desde una URL utilizando `wget` y `cv2.imread`. La imagen cargada se muestra usando `matplotlib.pyplot`.
3.  **Funciones:**
    * `reduceCanales(imagen_original, tonos)`:  Reduce la cantidad de tonos en cada canal de color de la imagen.
    * `MuestraCanales(imagen_procesada, tonos)`:  Muestra la imagen procesada, los canales individuales (BGR) en escala de grises y con sus respectivos mapas de color, y los histogramas de cada canal.
4.  **Pruebas con distintos valores de tonos:** Itera sobre una lista de valores de tonos (`[256, 128, 64, 32, 16, 8, 4, 2]`) y muestra la imagen cuantizada para cada valor, permitiendo la comparación visual del efecto de la cuantización.

## Cómo utilizar

1.  **Abrir en Colab:** Abre este notebook en Google Colaboratory.
2.  **Ejecutar las celdas:** Ejecuta las celdas en orden secuencial.
    * La primera celda instala las librerías necesarias.
    * La segunda celda descarga y carga la imagen.
    * Las celdas siguientes definen las funciones y realizan las pruebas de cuantización.
3.  **Experimentar:** Puedes modificar la lista `lista_tonos` para probar diferentes niveles de cuantización. También puedes cambiar la imagen de entrada modificando la URL en la celda correspondiente.

## Dependencias

* `numpy`
* `cv2` (OpenCV)
* `matplotlib.pyplot`

Estas librerías generalmente están preinstaladas en Google Colab. Si no lo están, puedes instalarlas usando `pip install numpy opencv-python matplotlib`.

## Notas adicionales

* Este notebook es útil para entender visualmente cómo la cuantización afecta la información de color en las imágenes.
* Observa cómo los histogramas cambian a medida que se reduce el número de tonos.
