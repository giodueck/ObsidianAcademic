2024-08-03
---
# Tesis - CNN

## Definition and Concepts

Una Red Neuronal Convolucional (o CNN por sus siglas en inglés) es un tipo de red neuronal artificial en la cual las
neuronas procesan datos de entrada por medio de filtros de convolución. Esto implica el procesamiento de un grupo de
datos cercanos, lo que permite interpretar el contexto de un dato, en contraste con redes neuronales típicas. Esta
propiedad hace que las CNN sean el método preferido para el procesamiento de imágenes por medio de redes neuronales. (1)(2)

Este método de procesamiento permite procesar una gran cantidad de entradas con una cantidad reducida de neuronas,
comparado con una red neuronal típica con la misma capacidad.

Por ejemplo, considerando una red neuronal con una capa de entrada y una capa siguiente con la misma cantidad de neuronas $N$ en ambas, una
red neuronal densa, es decir donde cada neurona de una capa está conectada a cada neurona de la siguiente capa, contiene
$N \times N$ conexiones. En contraste, una red neuronal convolucional equivalente estaría compuesta de tan solo $N$ neuronas,
mientras que al mismo tiempo captura un grupo de píxeles en cada neurona en lugar de uno solo.

Para el procesamiento se utilizan los filtros de convolución, matrices de dimensiones reducidas comparadas con la imagen,
cuyas celdas contienen coeficientes. Este filtro se superpone sobre una sección de la imagen, y los valores de los píxeles
se multiplican con los de la celda superpuesta del filtro, y la suma de los productos es el resultado de la convolución
del grupo de píxeles. Con una representación adecuada de los datos de cada píxel, estos filtros, también llamados *kernels*,
pueden usarse en la detección de bordes en cualquier orientación, reducción de ruido, aumentación de intensidad de píxeles
de cierto color o brillo, entre otros. (1)

## References
1. Géron, Aurélien (2019). Hands-on Machine Learning with Scikit-Learn, Keras, and TensorFlow. Sebastopol, CA: O'Reilly Media. ISBN 978-1-492-03264-9., pp. 448
2. Ciresan, Dan; Ueli Meier; Jonathan Masci; Luca M. Gambardella; Jurgen Schmidhuber https://web.archive.org/web/20220405190128/https://people.idsia.ch/~juergen/ijcai2011.pdf
