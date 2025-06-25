# Herramientas y utilidades
Esta carpeta contiene notebooks con utilidades
* [Generador de imagenes de palabras sinteticas](generador_dataset_palabras.ipynb)
* [Generador de imagenes de letras sinteticas](generador_dataset_letras.ipynb)
* [Herramienta para obtener de fuentes de Google Fonts](google_fonts_downloader.ipynb)

## Datasets y Metadatos para Detección de Caracteres y Análisis Tipográfico
Metadatos y enlaces a los datasets utilizados  

## Datasets

Los datasets completos están disponibles públicamente en [Kaggle](https://www.kaggle.com/datasets/zimmer2014/google-fonts-latin-set-datos-entrenamiento).

## Contenido del Repositorio

* `metadata_fonts_dataset.json`: Metadatos detallados del dataset de fuentes.
* `metadata_ocr_font_labels_dataset.json`: Metadatos detallados del dataset de etiquetas (labels) para el entrenamiento OCR.
* `metadata_ocr_font_images_dataset.json`: Metadatos detallados del dataset de imágenes (con bounding boxes) para el entrenamiento OCR.
* `google_fonts_downloader.ipynb`: Script de Google Colab utilizado para la descarga de fuentes de Google Fonts.

## Instrucciones:
* Para la ejecucion de google_fonts_downloader.ipynb se requiere generar y cargar en el cuaderno de Colab la GOOGLE_FONTS_API_KEY
