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
