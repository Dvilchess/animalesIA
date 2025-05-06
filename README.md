# Modelo de reconocimiento de imágenes (Animales)
El presente modelo busca realizar una clasificación de Imágenes respecto a un dataset ya existente. El dataset corresponde a Animales y se poseen 10 tipos de animales, con una cantidad de 28K de datos.

# Objetivos
Se desea Implementar un clasificador de Imágenes en Python utilizando la plataforma de Google Colab, para ello se busca lo siguiente:

Mejora de precisión: Incrementar la precisión del modelo en la clasificación de animales, reduciendo la tasa de errores.
Generalización: Asegurar que el modelo pueda generalizar bien en datos no vistos, evitando el sobreajuste a los datos de entrenamiento.
Eficiencia computacional: Optimizar el rendimiento del modelo para que pueda procesar imágenes de forma más rápida y eficiente, especialmente en entornos con recursos limitados.
Alcances
Optimización de hiperparámetros: Realizar una búsqueda sistemática de los hiperparámetros del modelo, como la tasa de aprendizaje, el tamaño del lote y la regularización, para encontrar la configuración óptima que maximice el rendimiento del modelo en términos de precisión y generalización.
Regularización: Implementar técnicas de regularización, como la disminución de la tasa de aprendizaje, la regularización L1/L2 y la deserción (dropout), para evitar el sobreajuste y mejorar la capacidad del modelo para generalizar en datos nuevos.
Optimización del rendimiento: Implementar técnicas de optimización del rendimiento, como la paralelización del cómputo y el uso de aceleradores de hardware (por ejemplo, GPU), para mejorar la eficiencia computacional del modelo y reducir los tiempos de entrenamiento e inferencia.

#Mejoras a Implementar
Para mejorar la exactitud del modelo al trabajar con los datos (Imagenes), se implementarán las siguientes mejoras:

Ajuste de Hiperparametros
Learning Rate: No se realizó un ajuste explícito del learning rate en este código. Sin embargo, se utilizó el optimizador RMSprop con una tasa de aprendizaje predeterminada de 0.001.
Cantidad de Capas (CNN) Se definió una arquitectura de red con dos capas convolucionales seguidas de max pooling y dos capas densas para la clasificación.
Función de Activación Se utilizó la función de activación ReLU en las capas convolucionales y densas, ya que es comúnmente utilizada en arquitecturas de redes neuronales convolucionales debido a su capacidad para manejar el problema de desvanecimiento del gradiente y acelerar el entrenamiento.

#Preprocesamiento
Normalización Se normalizaron los datos dividiendo los valores de píxeles de las imágenes por 255.0, lo que escala los valores de los píxeles al rango [0, 1]. Esto ayuda a estandarizar los datos y acelerar el entrenamiento del modelo.
*Cargar Incremental * Para manejar grandes conjuntos de datos de manera eficiente, se implementó la carga incremental dividiendo los datos en lotes más pequeños durante el entrenamiento del modelo. Esto se logró al cargar y mezclar los datos por lotes en lugar de cargar todo el conjunto de datos en la memoria al mismo tiempo.
Regularización y Reducción de Overfitting
Dropout Se aplicó Dropout con una tasa de 0.5 en la capa densa para reducir el sobreajuste. Dropout apaga aleatoriamente un porcentaje de unidades durante el entrenamiento, lo que ayuda a prevenir que la red se vuelva demasiado dependiente de ciertas características y mejora su capacidad de generalización.
Batch Normalization Se añadieron capas de BatchNormalization para normalizar las activaciones de cada capa en la red. Esto ayuda a estabilizar y acelerar el entrenamiento de la red al reducir la covariable interna entre las capas, y puede actuar como una forma de regularización para prevenir el sobreajuste.
