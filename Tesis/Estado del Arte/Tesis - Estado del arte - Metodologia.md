2024-09-29
---
# Tesis - Metodologia

> [!Note] Everything here can be tweaked
> Nothing is final at this stage of the project. If these strategies give bad or not good enough results, they can be changed

## Estrategias de busqueda

Keywords       | Synonyms
---------------|------------------
Neural network | Convolutional neural network
               | Deep learning
Remote sensing | Satellite imagery
Classification |
Detection      |
Lack of data   | Small data

Search engines:
- Google Scholar
- Cicco
- ArXiv
- IEEE Xplore

## Criterios de seleccion

### Inclusion
1. Trabajos que se enfoquen en la clasificacion de imagenes satelitales por medio de redes neuronales en el rango de publicacion de 2014 a 2024
2. Trabajos que coincidan en su contenido con los terminos de busqueda
3. Trabajos cuyo contenido sea relevante para la investigacion

### Exclusion
1. Trabajos que no contengan las palabras claves o son irrelevantes para el campo de investigacion
2. Trabajos que se centran en un termino de busqueda pero no incluyen alguno de los demas
3. Trabajos con una cantidad mayoritaria de informacion irrelevante para el tema estudiado

## Preguntas de investigacion

El objetivo principal de este estudio es determinar cual es el estado del arte en técnicas utilizadas para clasificar y caracterizar o interpretar imágenes satelitales por medio
de redes neuronales convolucionales. Con este fin en mente, se plantean las siguientes preguntas de investigación:

1. ¿Qué proyectos se están llevando adelante para clasificar y caracterizar imágenes satelitales usando redes neuronales convolucionales?
2. ¿Cuáles son las ventajas y/o desventajas de la clasificación y caracterización de imágenes satelitales usando redes neuronales convolucionales en comparación con las alternativas?
3. ¿Qué soluciones existen para abordar la falta de datos de entrenamiento para las redes neuronales convolucionales?

## Findings
[[Tesis - Estado del arte - Planilla]]

### Google Scholar
- neural network remote sensing classification
    - 2017: A patch-based convolutional neural network for remote sensing image classification https://www.sciencedirect.com/science/article/abs/pii/S0893608017301806
    - 2017: Multisource Remote Sensing Data Classification Based on Convolutional Neural Network https://ieeexplore.ieee.org/abstract/document/8068943
    - 2016: Convolutional Neural Networks for Large-Scale Remote-Sensing Image Classification https://ieeexplore.ieee.org/abstract/document/7592858
    - 2015: Land Use Classification in Remote Sensing Images by Convolutional Neural Networks https://arxiv.org/abs/1508.00092
    - 2021: Convolutional Neural Networks for Multimodal Remote Sensing Data Classification https://ieeexplore.ieee.org/abstract/document/9598903
- convolutional neural network remote sensing classification
    - 2018: **interesting** Deep Convolutional Neural Network for Complex Wetland Classification Using Optical Remote Sensing Imagery https://ieeexplore.ieee.org/abstract/document/8401505
    - 2017: **interesting** Towards better exploiting convolutional neural networks for remote sensing scene classification https://www.sciencedirect.com/science/article/abs/pii/S0031320316301509
- convolutional neural network satellite imagery classification
    - 2016: **interesting** SatCNN: satellite image dataset classification using agile convolutional neural networks https://www.tandfonline.com/doi/abs/10.1080/2150704X.2016.1235299
    - 2016: Classification and Segmentation of Satellite Orthoimagery Using Convolutional Neural Networks https://www.mdpi.com/2072-4292/8/4/329
    - 2020: Multi-Classification of Satellite Imagery Using Fully Convolutional Neural Network https://ieeexplore.ieee.org/abstract/document/9111928
    - 2019: DeepSat V2: feature augmented convolutional neural nets for satellite image classification https://www.tandfonline.com/doi/abs/10.1080/2150704X.2019.1693071
    - 2016: Fully convolutional neural networks for remote sensing image classification https://ieeexplore.ieee.org/abstract/document/7730322
    - 2018: Satellite Image Classification with Deep Learning https://ieeexplore.ieee.org/abstract/document/8457969
    - 2017: Performance Enhancement of Satellite Image Classification Using a Convolutional Neural Network https://link.springer.com/chapter/10.1007/978-3-319-64861-3_63
- convolutional neural network satellite imagery detection
    - 2017: Satellite Imagery Feature Detection using Deep Convolutional Neural Network: A Kaggle Competition https://arxiv.org/abs/1706.06169
    - 2016: Convolutional Neural Network Based Automatic Object Detection on Aerial Images https://ieeexplore.ieee.org/abstract/document/7447728
    - 2015: Orientation robust object detection in aerial images using deep convolutional neural network https://ieeexplore.ieee.org/abstract/document/7351502
    - 2018: Optimization Of Convolutional Neural Network For Object Recognition On Satellite Images https://ieeexplore.ieee.org/abstract/document/8457056
    - 2023: A Deep Convolutional Neural Network for Detecting Volcanic Thermal Anomalies from Satellite Images https://www.mdpi.com/2072-4292/15/15/3718
- deep learning remote sensing small data
	- 2023: Ten deep learning techniques to address small data problems with
remote sensing https://www.sciencedirect.com/science/article/pii/S156984322300393X
### Tutor
- 2016: Identificación y Mapeo de Paleocauces utilizando Imágenes Satelitales de Alta Resolución en la Llanura Costera de la Bahía Samborombón, Este de la Provincia de Buenos Aires, Argentina. https://www.researchgate.net/publication/325827963_IDENTIFICACION_Y_MAPEO_DE_PALEOCAUCES_UTILIZANDO_IMAGENES_SATELITALES_DE_ALTA_RESOLUCION_EN_LA_LLANURA_COSTERA_DE_LA_BAHIA_SAMBOROMBON_ESTE_DE_LA_PROVINCIA_DE_BUENOS_AIRES_ARGENTINA

## Comments on findings

### Sharma 2017
- Patch-based CNN in contrast with:
    - pixel-based conventional NN
    - pixel-based CNN
    - patch-based conventional NN

### Xu 2017
- CNN approach on multisource data tested against:
    - SVM
    - ELM
    - state-of-the-art CNN, CNN-PPF

### Maggiori 2016-0
- 2 step training approach using large amounts of OSM data and a small amount of manuallt labeled reference.
- Produce fine-grained calssification maps, as CNNs tend to hamper fineness of output as consequence of taking in a large context.

### Castelluccio 2015
- Training from scratch with limited data not always a good idea
- Adapts pretrained CNN to target task, demonstrates results with new dataset

### Wu 2022
- Cross-channel reconstruction tested against conventional CNN for multimodal RS imagery
*

### Rezaee 2018
- Wetlands classification using CNN
- 16% improvement compared to RF

### Nogueira 2017
- Explore exploiting existing CNNs to circumvent low amount of training data
- Best results between full training, fine tuning and using as feature extractors was fine tuning

### Zhong 2016
- SatCNN as a model made for RS data as opposed to other CNNs made primarily for natural scene classification

### Langkvist 2016
- CNN built with relatively small output and filter count
- Stability achieved through 4 parallel CNNs with differing context sizes

### Tun 2020
- Generally shows effectiveness of CNNs for classifying RS images
- Multi-classification of images
*

### Liu 2019
- Augmentation of CNN with handcrafted features for better discrimitative power
*

### Maggiori 2016-1
- CNN with only convolution and deconvolution layers
- Lower execution time and enhanced learning process
*

### Pritt 2018
- Ensamble of CNNs that classifies objects and facilities in high resolution multispectral RS images
- Post-processing NN that combine predictions from CNNs with satellite metadata

### Laban 2017
- Two step training approach to select least image scale with high accuracy to improve performance
*

### Iglovikov 2017
- No relevant info in conclusions
*

### Sevo 2016
- 2 stage training approach which outperforms feature based approaches and other network solutions
- Automated object detection CNN
*

### Zhu 2015
- Combined deep CNN layers produce features which allow detection without rotation of objects
- Performance improvement from not needing to go through the rotate-and-detect pipeline
*

### Khryashchev 2018
- No relevant info in conclusions
*

### Amato 2023
- Tuning pre-trained SqueezeNet CNN with handpicked images
- High accuracy but succeptible to clouds and weather causing false positives

### Luengo 2016
- Use of CNN and high-resolution satellite imagery to detect paleochannels and abandoned meanders
*

### Safonova 2023
- Review of papers in RS and DL space and their approaches to the small data problem
- Additional techniques to those of the papers, including data augmentation and training approach solutions
