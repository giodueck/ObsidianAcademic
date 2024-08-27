2024-08-26
---
# Tesis - CNN Aplicaciones en analisis de imagenes satelitales

## Classification

%% yoink (1) %%
Classification is a fundamental task in remote sensing data analysis, where the goal is to assign a semantic label to each image, such as 'urban', 'forest', 'agricultural land', etc. The process of assigning labels to an image is known as image-level classification. However, in some cases, a single image might contain multiple different land cover types, such as a forest with a river running through it, or a city with both residential and commercial areas. In these cases, image-level classification becomes more complex and involves assigning multiple labels to a single image. This can be accomplished using a combination of feature extraction and machine learning algorithms to accurately identify the different land cover types. It is important to note that image-level classification should not be confused with pixel-level classification, also known as semantic segmentation. While image-level classification assigns a single label to an entire image, semantic segmentation assigns a label to each individual pixel in an image, resulting in a highly detailed and accurate representation of the land cover types in an image.

## Segmentation

%% yoink (1) %%
Image segmentation is a crucial step in image analysis and computer vision, with the goal of dividing an image into semantically meaningful segments or regions. The process of image segmentation assigns a class label to each pixel in an image, effectively transforming an image from a 2D grid of pixels into a 2D grid of pixels with assigned class labels. One common application of image segmentation is road or building segmentation, where the goal is to identify and separate roads and buildings from other features within an image. To accomplish this task, single class models are often trained to differentiate between roads and background, or buildings and background. These models are designed to recognize specific features, such as color, texture, and shape, that are characteristic of roads or buildings, and use this information to assign class labels to the pixels in an image. Another common application of image segmentation is land use or crop type classification, where the goal is to identify and map different land cover types within an image. In this case, multi-class models are typically used to recognize and differentiate between multiple classes within an image, such as forests, urban areas, and agricultural land. These models are capable of recognizing complex relationships between different land cover types, allowing for a more comprehensive understanding of the image content.

## Change detection

%% yoink (1) %%
Change detection is a vital component of remote sensing analysis, enabling the monitoring of landscape changes over time. This technique can be applied to identify a wide range of changes, including land use changes, urban development, coastal erosion, and deforestation. Change detection can be performed on a pair of images taken at different times, or by analyzing multiple images collected over a period of time. It is important to note that while change detection is primarily used to detect changes in the landscape, it can also be influenced by the presence of clouds and shadows. These dynamic elements can alter the appearance of the image, leading to false positives in change detection results. Therefore, it is essential to consider the impact of clouds and shadows on change detection analysis, and to employ appropriate methods to mitigate their influence.

## Time series

%% yoink (1) %%
The analysis of time series observations in remote sensing data has numerous applications, including enhancing the accuracy of classification models and forecasting future patterns and events.

## References
1. https://github.com/satellite-image-deep-learning/techniques

## Links
https://medium.com/@robmarkcole/a-brief-introduction-to-satellite-image-classification-with-neural-networks-3ce28be15683
https://medium.com/@robmarkcole/a-brief-introduction-to-satellite-image-segmentation-with-neural-networks-33ea732d5bce

