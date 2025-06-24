# Repositorio de Notebooks de Colab para Procesamiento de Imágenes - IFTS24

Este repositorio contiene una colección de notebooks de Google Colaboratory utilizados para la práctica de la Materia Procesamiento de Imágenes en la Tecnicatura en Ciencia de Datos e Inteligencia Artificial del IFTS24 (ifts24.edu.ar).

## Contenido

Aquí puedes encontrar una lista de las carpetas con los notebooks incluidos en este repositorio y una breve descripción de cada uno:

* 00 [Repaso de Python](00_repaso_de_python): Breve repaso de los fundamentos del lenguaje **python** con ejemplos prácticos.
* 01 [Introduccion al procesamiento digital de imagenes](01_introduccion): Conceptos básicos sobre OpenCV y skimage
* 02 [Analisis de Color](02_color): Analisis y trabajo sobre los canales de color de las imagenes por medio de openCV.
* 03 [Muestreo y Cuantización](03_muestreo_y_cuantizacion): Analisis y trabajo sobre los pixeles y la cantidad de tonos de las imagenes por medio de openCV.
* 04 [Segmentacion Simple](04_segmentacion_simple): Utilizamos las tecnicas de los cuadernos anteriores para seleccionar un objeto por su color.
* 05 [Ejercicio Integrador](05_ejercicio_integrador): Aplicamos las tecnicas de separacion de colores, muestreo, cuantizacion y segmentación simple a una imagen.
* 06 *Extra* [Uso de skimage y pil-pillow](06_uso_skimage_y_pil-pillow): Funcionamiento básico y comparacion de librerias.
* 07 [Landmarks y Operaciones Morfológicas](07_lankmarks): Conceptos clave del procesamiento digital de imágenes, incluyendo operaciones morfológicas y la detección y uso de landmarks faciales.
* 08 [Clasificación y Redes Neuronales](08_clasificacion_rn): Exploración de conceptos fundamentales en el aprendizaje automático, específicamente la clasificación y la implementación de redes neuronales básicas.
* 09 [Redes Neuronales Convolucionales (CNNs)](09_cnns): Estudio y aplicación de las Redes Neuronales Convolucionales (CNNs) en el procesamiento de imágenes, así como una introducción a la comprensión espacial con Gemini 2.0.
* 10 [Modelos Preentrenados y Transferencia de Aprendizaje](10_transfer_learning): Aplicación de la Transferencia de Aprendizaje con modelos preentrenados como VGG16, ResNet18 y MobileNetV2 para clasificación de imágenes.
* 11 [Modelos de Difusión y Aplicaciones con IA Generativa](11_diffusion_models): Introducción a los Modelos de Difusión, con un enfoque en Stable Diffusion, y ejercicios prácticos de aplicaciones con IA generativa.
* 12 [Interfaces Interactivas con Gradio y Aplicaciones de IA Generativa](12_gradio_apps): Creación de interfaces de usuario interactivas con Gradio, aplicadas al procesamiento digital de imágenes y a modelos de IA generativa (descripción de imágenes, Stable Diffusion XL).
* 13 [Trabajo Práctico Integrador](13_trabajo_practico_integrador): Repositorio central del Trabajo Práctico Integrador, conteniendo subproyectos de detección y reconocimiento de texto y objetos con diversas arquitecturas (TensorFlow/Keras, YOLO, TensorFlow OD API).


## Cómo utilizar los Notebooks de Colab

Para utilizar estos notebooks, sigue estos sencillos pasos:

1.  **Accede al Notebook:** Haz clic en el enlace del notebook que te interese. Esto te dirigirá a la página del notebook en GitHub.
2.  **Abrir en Colab:** En la página del notebook en GitHub, busca el botón que dice "Open in Colab" (a menudo con el logo de Colab). Haz clic en este botón. Esto abrirá el notebook directamente en el entorno de Google Colaboratory en tu navegador.
3.  **Ejecutar las Celdas:** Una vez que el notebook esté abierto en Colab, puedes ejecutar las celdas de código individualmente (haciendo clic en el botón de "play" junto a la celda o usando `Shift + Enter`) o ejecutar todas las celdas secuencialmente (menú `Runtime` -> `Run all`).
4.  **Interactuar y Modificar:** Los notebooks de Colab te permiten interactuar con el código, modificarlo y experimentar con diferentes parámetros y datos. ¡Siéntete libre de explorar y adaptar los notebooks a tus necesidades!
5.  **Guardar tus Cambios (Opcional):** Si deseas guardar las modificaciones que realices, puedes hacerlo en tu propia cuenta de Google Drive (menú `File` -> `Save a copy in Drive`).

## Requisitos y Dependencias (Opcional)

Si tus notebooks requieren alguna biblioteca o configuración específica, menciónalas aquí. Por ejemplo:

* Este notebook requiere las siguientes bibliotecas de Python: `pandas`, `numpy`, `matplotlib`, `opencv-python`. Puedes instalarlas ejecutando `pip install pandas numpy matplotlib opencv-python` en una celda de Colab.
* Algunos notebooks pueden requerir la descarga de conjuntos de datos específicos. Las instrucciones para hacerlo se encuentran dentro del notebook correspondiente.

## Datos de Contacto

Si tienes alguna pregunta, sugerencia o encuentras algún problema con estos notebooks, no dudes en contactarme a través de los siguientes medios:

* **Nombre:** Andres Allievi
* **Email:** garzamorada@gmail.com
* **GitHub:** [garzamorada](https://github.com/garzamorada)
* **LinkedIn:** [andres-allievi](https://www.linkedin.com/in/andres-allievi)

## Contribuciones (Opcional)

Si deseas contribuir a este repositorio añadiendo nuevos notebooks, corrigiendo errores o realizando mejoras, ¡tus contribuciones son bienvenidas! Por favor, sigue estas pautas:

1.  Realiza un "fork" del repositorio.
2.  Crea una nueva rama con tu contribución (`git checkout -b feature/nueva-funcionalidad`).
3.  Realiza tus cambios y commitealos (`git commit -am 'Añade una nueva funcionalidad'`).
4.  Sube tus cambios a tu fork (`git push origin feature/nueva-funcionalidad`).
5.  Crea un "pull request" desde tu rama a la rama principal de este repositorio.

## Licencia

Este proyecto está bajo la licencia MIT - consulta el archivo [LICENSE](LICENSE) para más detalles.

---

¡Espero que estos notebooks sean de utilidad para la práctica de Procesamiento de Imágenes!
