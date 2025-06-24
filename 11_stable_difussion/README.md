# Contenido de la Carpeta: Modelos de Difusión y Aplicaciones con IA Generativa

Esta carpeta contiene cuadernos de Jupyter (o Colab) que introducen los **Modelos de Difusión**, con un enfoque particular en **Stable Diffusion**, y proponen una serie de ejercicios prácticos para explorar diversas aplicaciones de la IA generativa en el procesamiento de imágenes.

## Índice de Contenidos

* [11.1_intro_stable_diffusion_spa_oficial](11.1_intro_stable_diffusion_spa_oficial.ipynb)
* [11.2_stable_diffusion](11.2_stable_diffusion.ipynb)
* [11.3_ejercicios](11.3_ejercicios.ipynb)

---

### 11.1_intro_stable_diffusion_SPA_oficial.ipynb

**Descripción:**
Este cuaderno introduce **Stable Diffusion**, un modelo de difusión latente de texto a imagen. Proporciona una visión general de su origen (CompVis, Stability AI, LAION), su entrenamiento en el dataset LAION-5B, y su arquitectura, incluyendo el codificador de texto CLIP ViT-L/14. El foco principal está en la **aplicación práctica** del modelo utilizando la biblioteca `🧨 Diffusers` de Hugging Face, permitiendo a los usuarios empezar a generar imágenes a partir de texto de forma rápida.

**Puntos Clave:**
* Introducción a Stable Diffusion como modelo de texto a imagen.
* Uso práctico de Stable Diffusion con la librería `Diffusers`.
* Explicación de sus componentes principales y cómo está entrenado.
* Ejemplos iniciales para la generación de imágenes.

---

### 11.2_stable_diffusion.ipynb

**Descripción:**
Este cuaderno profundiza en la teoría y el funcionamiento de los **Modelos de Difusión** en general, antes de centrarse en Stable Diffusion. Explica que son modelos generativos que aprenden a "deshacer" un proceso de ruido gradual para crear imágenes de alta calidad. Cubre sus diversas aplicaciones (texto-a-imagen, imagen-a-imagen, super-resolución, edición). Se explican las bases teóricas, incluyendo los Denoising Diffusion Probabilistic Models (DDPMs) y los Latent Diffusion Models (LDMs), y se describen los componentes clave como el Autoencoder, U-Net y el codificador de texto.

**Puntos Clave:**
* Definición y funcionamiento de los Modelos de Difusión.
* Aplicaciones principales de los modelos de difusión en visión por computadora.
* Explicación teórica de DDPMs y Latent Diffusion Models (LDMs).
* Componentes arquitectónicos de un LDM como Stable Diffusion.

---

### 11.3_ejercicios.ipynb

**Descripción:**
Este cuaderno es un set de **desafíos y ejercicios prácticos** diseñados para que el usuario explore y desarrolle sus propias aplicaciones utilizando las herramientas y conocimientos adquiridos sobre IA generativa y visión por computadora. Propone diversas ideas, divididas en "Aplicaciones de Análisis Visual" (como un detector de emociones en rostros o un comparador de imágenes) y "Aplicaciones Creativas" (como la transferencia de estilo o la creación de interfaces con Gradio), fomentando la experimentación y la creación personal.

**Puntos Clave:**
* Propuesta de ejercicios prácticos para aplicar conocimientos de IA.
* Ideas para desarrollar detectores de emociones, comparadores de imágenes, etc.
* Ejemplos de aplicaciones creativas como la transferencia de estilo.
* Fomenta la exploración y el desarrollo de proyectos propios.

---