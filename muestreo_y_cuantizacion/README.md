# Muestreo y Cuantización en Procesamiento de Imágenes

Este notebook de Colab explora los conceptos fundamentales de muestreo y cuantización, dos operaciones esenciales en el procesamiento digital de imágenes.

## Descripción

El procesamiento digital de imágenes se basa en la conversión de una imagen continua en una forma digital. Esto se logra mediante dos pasos principales:

* **Muestreo espacial:** Convierte una imagen continua en una matriz discreta de píxeles.
* **Cuantización:** Asigna valores discretos a la intensidad de cada píxel.

Este notebook demuestra estos procesos y sus efectos en una imagen.

## Contenido

El notebook incluye las siguientes secciones:

1.  **Preparación del entorno:** Importa las librerías necesarias como `numpy` y `cv2` (OpenCV).
2.  **Muestreo espacial (Reducción de la resolución):**
    * Carga una imagen.
    * Define una función `reducir_resolucion(imagen, factor)` que reduce la resolución de la imagen tomando un píxel de cada `factor` x `factor` bloque.
        * **Descripción:** Reduce el tamaño de la imagen muestreando un píxel de cada bloque de `factor` x `factor`.
        * **Parámetros:**
            * `imagen`: La imagen de entrada (array de NumPy).
            * `factor`: El factor de reducción de la resolución.
        * **Funcionamiento:** Crea una nueva imagen tomando un píxel de cada bloque de tamaño `factor` x `factor` de la imagen original.
    * Muestra la imagen original y las versiones con resolución reducida para diferentes factores.
3.  **Cuantización (Reducción de la profundidad de bits):**
    * Define una función `cuantizar(imagen, niveles)` que reduce la cantidad de niveles de intensidad en la imagen.
        * **Descripción:** Reduce el número de niveles de intensidad en la imagen.
        * **Parámetros:**
            * `imagen`: La imagen de entrada (array de NumPy).
            * `niveles`: El número deseado de niveles de intensidad.
        * **Funcionamiento:** Divide el rango de valores de píxeles (0-255) en `niveles` intervalos iguales y asigna a cada píxel el valor central del intervalo al que pertenece.
    * Muestra la imagen original y las versiones cuantizadas con diferentes números de niveles.

## Cómo utilizar

1.  **Abrir en Colab:** Abre este notebook en Google Colaboratory.
2.  **Ejecutar las celdas:** Ejecuta las celdas en orden secuencial.
    * La primera celda importa las librerías necesarias.
    * Las siguientes celdas cargan la imagen y definen las funciones para reducir la resolución y cuantizar.
    * Las últimas celdas muestran los resultados de la reducción de resolución y la cuantización.
3.  **Experimentar:**
    * Puedes modificar el `factor` en la sección de muestreo para explorar diferentes niveles de reducción de resolución.
    * Puedes modificar los `niveles` en la sección de cuantización para observar el efecto de diferentes niveles de cuantización.
    * Puedes cambiar la imagen cargada modificando la ruta del archivo.

## Dependencias

* `numpy`
* `cv2` (OpenCV)

Estas librerías generalmente están preinstaladas en Google Colab.

## Notas adicionales

* Este notebook proporciona una demostración práctica de los conceptos teóricos de muestreo y cuantización.
* Observa cómo la reducción de la resolución produce un efecto de "bloqueo" en la imagen.
* Observa cómo la cuantización produce un efecto de "contorno falso" a medida que se reducen los niveles de intensidad.

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
