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

## Key techniques and architectures

https://medium.com/@navarai/unveiling-the-diversity-a-comprehensive-guide-to-types-of-cnn-architectures-9d70da0b4521

First successful CNNs featured some convolution and max pooling layers, some fully connected layers and various traditional NN techniques like dropout. The first examples are LeNet (LeCun ~1990s) and AlexNet (Krizhevsky et al 2012).

New breakthroughs aim at specific kinds of optimizations. VGGNet provides a simpler structure with the same capacity as a more complex architecture. Google's GoogLeNet used different sized kernels to improve generalization, along with showcasing Inception as a performance booster through parallelism. ResNet showed techniques for training very deep networks using shortcuts between layers, which could entirely skip some layers to make backpropagation and gradient descent easier. Lastly, Google also introduced MobileNet, an architecture aimed at efficiency for use in mobile and edge devices.

Another milestone architecture is the U-Net, a fully convolutional neural network architecture designed for biomedical image segmentation. It was developed to require fewer training images and to yield more precise segmentation, which on a modern (2015) GPU takes less than a second for a 512x512 image. (5) It has also been used in diffusion models for iterative image denoising, and it underlies many generative image technologies, like DALL-E, Midjourney and Stable Diffusion. (4) The U-Net has also been successfully employed in segmentation of satellite imagery for detection of various features, like water resources, forests or urban areas. (3)

## References
1. Géron, Aurélien (2019). Hands-on Machine Learning with Scikit-Learn, Keras, and TensorFlow. Sebastopol, CA: O'Reilly Media. ISBN 978-1-492-03264-9., pp. 448
2. Ciresan, Dan; Ueli Meier; Jonathan Masci; Luca M. Gambardella; Jurgen Schmidhuber https://web.archive.org/web/20220405190128/https://people.idsia.ch/~juergen/ijcai2011.pdf
3. https://fruct.org/publications/volume-22/acm22/files/Khr.pdf
4. https://github.com/hojonathanho/diffusion?tab=readme-ov-file
5. https://arxiv.org/abs/1505.04597v1
