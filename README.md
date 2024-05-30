# Caso Práctico: Clasificación de Imágenes

Este caso práctico ilustra un enfoque de aprendizaje profundo de extremo a extremo (end-to-end learning) aplicado a la clasificación de imágenes utilizando la biblioteca Keras y el conjunto de datos Fashion MNIST.

## 1. Conjunto de Datos

El conjunto de datos utilizado es Fashion MNIST, que contiene imágenes de 28x28 píxeles de diferentes artículos de moda. Este conjunto de datos incluye un subconjunto de entrenamiento y un subconjunto de pruebas.

## 2. Visualización del Conjunto de Datos

Se muestra una visualización de algunas imágenes del conjunto de datos de entrenamiento para tener una idea de su contenido. Estas imágenes se presentan en una figura con múltiples subgráficas, cada una mostrando una imagen diferente en escala de grises. Además, se imprimen las longitudes de los subconjuntos de entrenamiento y de pruebas.

## 3. Transformación del Conjunto de Datos

Las imágenes del conjunto de datos se transforman en vectores unidimensionales para facilitar su uso en modelos de aprendizaje automático. Luego, los datos se normalizan para tener valores en un rango más manejable y las etiquetas se convierten a una representación categórica para el uso en clasificación.

## 4. Construcción del Modelo

Se construye una red neuronal secuencial con tres capas densas. La primera capa tiene 300 neuronas con función de activación ReLU, la segunda capa tiene 100 neuronas también con ReLU y la última capa tiene 10 neuronas con función de activación softmax para la clasificación en 10 categorías. El modelo se compila utilizando la función de pérdida de entropía cruzada categórica, el optimizador Adam y se evalúan las métricas de precisión y exactitud.

El modelo se entrena en el conjunto de datos de entrenamiento durante 15 épocas, con un tamaño de lote de 32, y se valida utilizando el conjunto de datos de prueba. Al finalizar cada época, se registran la pérdida y la precisión tanto en el conjunto de entrenamiento como en el de validación.

## Resultados del Entrenamiento

Durante el entrenamiento del modelo, se observa una mejora continua en la precisión y una reducción en la pérdida. Los resultados al final de las 15 épocas muestran una alta precisión en ambos conjuntos de datos, indicando que el modelo es capaz de clasificar correctamente los artículos de moda en la mayoría de los casos.

## Aprendizaje de Extremo a Extremo (End-to-End Learning)

Este caso práctico ejemplifica el enfoque de aprendizaje profundo de extremo a extremo, donde el modelo se alimenta directamente con las imágenes en bruto (después de una mínima preprocesamiento) y aprende a mapearlas a sus respectivas categorías a través de la red neuronal. El flujo de trabajo de extremo a extremo elimina la necesidad de características hechas a mano o de múltiples etapas de procesamiento, permitiendo que el modelo aprenda directamente a partir de los datos y optimice el proceso de clasificación en una única pasada del modelo.
