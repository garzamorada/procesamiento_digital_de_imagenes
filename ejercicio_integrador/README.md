# Ejercicio Integrador: Color, Muestreo, Cuantización y Segmentación

Este notebook de Colab integra varios conceptos fundamentales del procesamiento de imágenes, incluyendo espacios de color, muestreo, cuantización y segmentación.

## Descripción

El notebook presenta una serie de ejercicios que combinan diferentes técnicas de procesamiento de imágenes. Los ejercicios guían al usuario a través de la manipulación de espacios de color, la aplicación de muestreo y cuantización, y la realización de segmentación de imágenes.

## Contenido

El notebook se divide en los siguientes ejercicios:

**Ejercicio 1: Espacios de Color**

* **a) Cargar y mostrar canales BGR:** Carga una imagen con OpenCV y muestra los canales Azul, Verde y Rojo por separado.
* **b) Identificar canal con mayor información:** Calcula el valor promedio de cada canal BGR y determina cuál canal tiene la mayor cantidad de información.
* **c) Conversión BGR a RGB:** Convierte la imagen de BGR a RGB y explica la diferencia en la visualización de los colores.

**Ejercicio 2: Muestreo y Cuantización**

* **a) Aplicar muestreo espacial:** Reduce la resolución de una imagen aplicando muestreo espacial con factores de 2, 4 y 8.
* **b) Calcular tamaño y reducción de datos:** Para cada factor de muestreo, calcula el nuevo tamaño de la imagen y el porcentaje de reducción de datos.
* **c) Aplicar cuantización:** Reduce la cantidad de colores en una imagen utilizando cuantización con 8, 4 y 2 bits.
* **d) Calcular porcentaje de reducción de datos:** Para cada nivel de cuantización, calcula el porcentaje de reducción de datos.

**Ejercicio 3: Segmentación**

* **a) Segmentación por color:** Segmenta una imagen utilizando el espacio de color RGB para aislar objetos dentro de un rango de color específico.

## Cómo utilizar

1.  **Abrir en Colab:** Abre este notebook en Google Colaboratory.
2.  **Ejecutar las celdas:** Ejecuta las celdas en orden secuencial para seguir el flujo de los ejercicios.
3.  **Completar los ejercicios:** Sigue las instrucciones y completa las tareas en cada sección del notebook.
4.  **Experimentar:** Modifica los parámetros y el código para explorar diferentes resultados y profundizar en tu comprensión de los conceptos.

## Dependencias

* `cv2` (OpenCV)
* `numpy`
* `matplotlib.pyplot`
* `google.colab.patches` (para `cv2_imshow` en Colab)

Estas librerías generalmente están preinstaladas en Google Colab, excepto `opencv-python` que puede requerir instalación.

## Notas adicionales

* Este notebook está diseñado como un ejercicio integrador, combinando varios temas importantes del procesamiento de imágenes.
* Presta atención a las explicaciones y comentarios en el código para comprender el razonamiento detrás de cada paso.
* ¡No dudes en experimentar y modificar el código para explorar más a fondo los conceptos!
