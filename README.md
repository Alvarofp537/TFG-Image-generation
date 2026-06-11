# TFG-Image-generation
Trabajo de Fin de Grado de entrenamiento y comparación de resultados de métodos generativos de imágenes con recursos computacionales reducidos. Se siguen 2 líneas de estudio, una de generación aleatoria y otra de generación condicionada por texto. 


## Generación aleatoria

En la carpeta `random generation` se encuentra el código y los modelos empleados para el estudio de técnicas de generación de imágenes sobre el **Anime Face Dataset**.

El objetivo es comparar distintos enfoques generativos (VAE, GAN y DDPM) en un escenario de generación no condicionada, evaluando su comportamiento sobre un conjunto de imágenes de rostros de estilo anime con resolución **64×64**.

### Descarga y preparación de datos

El dataset utilizado está disponible públicamente en Kaggle:

https://www.kaggle.com/datasets/splcher/animefacedataset

Para reproducir los experimentos:

1. Subir el cuadernillo que se desea ejecutar a Kaggle (`.ipynb`).

2. Añadir el dataset anterior como **Input** del proyecto desde el menú lateral de Kaggle.

3. Ejecutar las celdas del cuadernillo. El código detectará automáticamente el dataset añadido como entrada y realizará el preprocesamiento necesario antes del entrenamiento.

### Uso del dataset Anime Faces

Este proyecto utiliza el Anime Face Dataset exclusivamente con fines académicos y no comerciales. Este repositorio no distribuye ninguna imagen perteneciente al dataset original. Los usuarios deben usar los datos directamente desde Kaggle utilizando el enlace proporcionado anteriormente.

Las texturas generadas como resultado de los modelos entrenados pueden considerarse obras derivadas, de modo que su uso también queda sujeto a la licencia Anime Faces incluida en la carpeta `extras/`.

## Generación condicionada por texto

En la carpeta `text-guided generation` se encuentra el código y modelos empleados para el estudio de técnicas de generación de imágenes aplicadas a texturas de objetos de **Minecraft**, concretamente utilizando el pack **Faithful 32x32**, versión **1.21.1**.

El objetivo es comparar distintos enfoques generativos (CVAE, CGAN y DDPM) para evaluar su rendimiento en entornos con datos limitados y resolución reducida.


###  Descarga y preparación de datos

Los datos utilizados en este estudio pertenecen al proyecto **Faithful**, disponibles públicamente en:

**https://faithfulpack.net/downloads**

Para reproducir los experimentos:

1. Descargar la versión:
   - **Faithful 32x32 Java 1.21.1**

2. Dentro del archivo `.zip`, navegar hasta: `/assets/minecraft/textures/`

3. Copiar la carpeta `item` de esa carpeta en: `text-guided generation/datos/`

4. Ejecutar todas las celdas del cuadernillo `utils/preproceso_datos.ipynb`

Este código crea el archivo `.parquet` que contiene el dataset que usarán los modelos para entrenarse.

### Uso adecuado del pack Faithful

Este proyecto utiliza texturas del pack Faithful exclusivamente con fines académicos y no comerciales. Este repositorio no distribuye ningún archivo del pack Faithful. Los usuarios deben descargar los recursos directamente desde su web oficial: https://faithfulpack.net/

Las texturas generadas como resultado de los modelos entrenados pueden considerarse obras derivadas, de modo que su uso también queda sujeto a la licencia Faithful incluida en la carpeta `extras/`.


## Licencia del repositorio

El código fuente de este repositorio está disponible bajo una licencia de uso académico y no comercial (MIT License).




