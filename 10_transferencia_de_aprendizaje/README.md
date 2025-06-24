# Contenido de la Carpeta: Modelos Preentrenados y Transferencia de Aprendizaje

Esta carpeta contiene cuadernos de Jupyter (o Colab) dedicados a la **Transferencia de Aprendizaje (Transfer Learning)**, una técnica esencial en Deep Learning que aprovecha el conocimiento de modelos preentrenados en grandes datasets para aplicarlo a problemas específicos de clasificación de imágenes.

## Índice de Contenidos

* [10.1_vgg16_modelo_preentrenado](10.1_vgg16_modelo_preentrenado.ipynb)
* [10.2_resnet18](10.2_resnet18.ipynb)
* [10.3_transferencia_de_aprendizaje](10.3_transferencia_de_aprendizaje.ipynb)
* [10.4_integracion_trasfer_learning](10.4_integracion_trasfer_learning.ipynb)
* [10.4a_dataset_imagenes_perros](https://drive.google.com/file/d/17UXvPn_fOZ5FxNzbfOuUv5yoMVO84uOx/view?usp=drive_link)
* [10.4b_dataset_imagenes_gatos](https://drive.google.com/file/d/1T9bzAeT1SbuEf74OCI947ENXHbt0_Ilb/view?usp=drive_link)

---

### 10.1_vgg16_modelo_preentrenado.ipynb

**Descripción:**
Este cuaderno se enfoca en el uso del modelo **VGG16 preentrenado** para la tarea de clasificación de imágenes. Explica cómo cargar este modelo (entrenado en ImageNet) sin sus capas superiores, congelar sus capas base y añadir nuevas capas para adaptar el modelo a una tarea específica, como la clasificación de imágenes de gatos y perros. Cubre el preprocesamiento de imágenes, la definición y entrenamiento del modelo, y la realización de predicciones.

**Puntos Clave:**
* Introducción al modelo VGG16 y su uso en clasificación.
* Concepto de Transferencia de Aprendizaje con VGG16.
* Congelación de capas base y adición de nuevas capas de clasificación.
* Preprocesamiento de imágenes para VGG16.
* Entrenamiento y evaluación del modelo adaptado.

---

### 10.2_resnet18.ipynb

**Descripción:**
Este cuaderno explora la **clasificación de imágenes reales utilizando modelos preentrenados**, específicamente **ResNet18**. Demuestra cómo cargar ResNet18 (preentrenado en el vasto dataset ImageNet) con `torchvision` y aplicarlo directamente para clasificar imágenes sin necesidad de entrenamiento adicional extenso. Se detalla el preprocesamiento de imágenes para adaptarlas a los requisitos del modelo y se realiza una actividad práctica para que el usuario pruebe el modelo con sus propias imágenes.

**Puntos Clave:**
* Uso de modelos preentrenados como ResNet18 para clasificación.
* Carga de modelos con `torchvision`.
* Preprocesamiento de imágenes según los requisitos del modelo.
* Realización de predicciones con un modelo preentrenado.
* Actividad práctica para aplicar el modelo en nuevas imágenes.

---

### 10.3_transferencia_de_aprendizaje.ipynb

**Descripción:**
Este cuaderno introduce la **Transferencia de Aprendizaje** como una técnica fundamental en Deep Learning. Destaca sus ventajas, como el ahorro de tiempo y recursos computacionales, y el mejor rendimiento en conjuntos de datos pequeños. El ejemplo práctico consiste en clasificar imágenes de babuinos y jirafas utilizando **MobileNetV2**, un modelo preentrenado en el dataset ImageNet, y demuestra cómo ajustar (fine-tune) las últimas capas del modelo para la nueva tarea.

**Puntos Clave:**
* Fundamentos y ventajas de la Transferencia de Aprendizaje.
* Reutilización de modelos preentrenados (MobileNetV2).
* Aplicación a problemas de clasificación con datasets específicos.
* Proceso de ajuste (fine-tuning) de las capas finales del modelo.

---

### 10.4_integracion_trasfer_learning.ipynb

**Descripción:**
Este cuaderno es una extensión o integración de los conceptos de **Transferencia de Aprendizaje** aplicados con el modelo **VGG16 preentrenado** para la clasificación de imágenes. Al igual que el `10.1`, se enfoca en la clasificación de gatos y perros, pero posiblemente profundiza en la integración de todos los pasos: desde el montaje de Google Drive, la carga y preparación de datos, la configuración de callbacks, hasta el ajuste fino (fine-tuning) del modelo y la realización de predicciones. Es un ejemplo completo de cómo aplicar el transfer learning en un escenario práctico.

**Puntos Clave:**
* Aplicación integral de Transferencia de Aprendizaje con VGG16.
* Clasificación de imágenes (ej. gatos y perros).
* Procesos de carga y preparación de datos.
* Configuración de callbacks y ajuste fino del modelo.
* Evaluación y predicción con el modelo entrenado.

---