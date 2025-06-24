# Clasificación de Imágenes con Redes Neuronales Preentrenadas
# Autor: Martin Nicolas Serafini
* [GitHub del Autor](https://github.com/MNSerafini/)
* [GhitHub de la Materia](https://github.com/MNSerafini/Tecnicas-de-Procesamiento-Digital-de-Imagenes/)

## Comparativa y Explicación de Modelos

Este cuaderno de Google Colab, desarrollado por Martin Nicolas Serafini en Mayo de 2025, se centra en la **clasificación de imágenes utilizando redes neuronales convolucionales (CNNs) preentrenadas**. El objetivo principal es explorar y comparar el rendimiento de diferentes arquitecturas de modelos preentrenados en una tarea de clasificación de imágenes.

## Descripción

El proyecto aborda la clasificación de imágenes aprovechando el poder de los modelos preentrenados. Estos modelos, que han sido entrenados en grandes conjuntos de datos como ImageNet, son excelentes puntos de partida para tareas de visión por computadora debido a su capacidad para extraer características relevantes de las imágenes. El cuaderno guía a través del proceso de cargar un conjunto de datos, aplicar transformaciones a las imágenes, definir y cargar modelos preentrenados, entrenarlos o ajustarlos (fine-tuning) en un conjunto de datos específico y evaluar su rendimiento.

## Funciones y Acciones

El cuaderno realiza las siguientes acciones principales:

* **Instalación e Importación de Librerías:** Configura el entorno instalando bibliotecas esenciales como `torch`, `torchvision`, `pandas`, `matplotlib`, `seaborn`, `tqdm`, `scikit-learn` y `torchinfo`.
* **Preparación de Datos:**
    * Descarga y carga un conjunto de datos (por ejemplo, el conjunto de datos de perros y gatos para clasificación binaria o un conjunto de datos con múltiples clases).
    * Define transformaciones de imágenes para el conjunto de entrenamiento y validación (redimensionamiento, normalización, aumento de datos para entrenamiento).
    * Crea `DataLoader`s para facilitar la carga por lotes de las imágenes durante el entrenamiento y la evaluación.
* **Carga de Modelos Preentrenados:**
    * Define una lista de arquitecturas de modelos preentrenados a comparar (e.g., `ResNet18`, `ResNet34`, `ResNet50`, `VGG16`, `AlexNet`, `GoogleNet`, `InceptionV3`, `DenseNet121`, `MobileNetV2`, `EfficientNetB0`).
    * Modifica las capas finales de estos modelos para adaptarlas al número de clases específicas del problema de clasificación.
* **Definición de Funciones de Entrenamiento y Evaluación:**
    * `train_model`: Implementa el bucle de entrenamiento, incluyendo el forward pass, el cálculo de la pérdida, el backward pass y la optimización de los pesos del modelo.
    * `evaluate_model`: Calcula la precisión del modelo en el conjunto de validación.
* **Bucle Principal de Entrenamiento y Evaluación:**
    * Itera sobre cada modelo preentrenado seleccionado.
    * Congela las capas convolucionales (extracción de características) y entrena solo la capa clasificadora lineal (transfer learning).
    * Opcionalmente, realiza un *fine-tuning* descongelando algunas capas convolucionales y entrenándolas con una tasa de aprendizaje más baja.
    * Registra métricas como la pérdida y la precisión en cada época.
* **Análisis y Visualización de Resultados:**
    * Almacena los resultados de rendimiento de cada modelo.
    * Genera gráficos para comparar la precisión de los diferentes modelos.
    * Muestra ejemplos de predicciones del modelo en imágenes de prueba, incluyendo la imagen original, la predicción del modelo y la clase verdadera.

## Requisitos

Para ejecutar este cuaderno, necesitará un entorno con las siguientes bibliotecas de Python instaladas. Es altamente recomendable ejecutarlo en Google Colab, ya que proporciona un entorno preconfigurado con acceso a GPU.

* `torch`
* `torchvision`
* `pandas`
* `matplotlib`
* `seaborn`
* `tqdm`
* `scikit-learn`
* `torchinfo`
* `Pillow` (generalmente incluido con `torchvision` o entornos de Python)

## Instrucciones de Uso

Siga estos pasos para ejecutar el cuaderno en Google Colab:

1.  **Abrir en Colab:** Haga clic en el botón "Open in Colab" (o equivalente) si este `README.md` se visualiza en GitHub, o simplemente cargue el archivo `.ipynb` directamente en Google Colab.
2.  **Configurar el Entorno de Ejecución:**
    * Vaya a `Entorno de ejecución` (Runtime) en el menú superior.
    * Seleccione `Cambiar tipo de entorno de ejecución` (Change runtime type).
    * Asegúrese de que el `Acelerador de hardware` (Hardware accelerator) esté configurado en `GPU` para un rendimiento óptimo.
3.  **Ejecutar Todas las Celdas:**
    * Puede ejecutar cada celda individualmente haciendo clic en el botón de reproducción (`▶`) en la esquina superior izquierda de cada celda de código.
    * Alternativamente, para ejecutar todo el cuaderno, vaya a `Entorno de ejecución` (Runtime) en el menú y seleccione `Ejecutar todo` (Run all).
4.  **Seguir el Flujo:** El cuaderno está diseñado para ser ejecutado secuencialmente. Las salidas (gráficos, métricas, etc.) se generarán a medida que se ejecuten las celdas.

Asegúrese de que su conexión a Internet sea estable para la descarga de los conjuntos de datos y los pesos de los modelos preentrenados.
