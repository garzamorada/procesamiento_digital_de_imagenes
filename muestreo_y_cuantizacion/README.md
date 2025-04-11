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
