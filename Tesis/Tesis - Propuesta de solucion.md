2024-12-02
---
# Tesis - Propuesta de solucion

## Data collection
Primary and/or secondary sources -> Image compilation

### Primary sources
Copernicus data browser image downloads.

Advantages:
- Can select a region of interest and download cropped images
- Can select image and geolocation data formats
- Can select bands to download, including preprocessed layers like NDVI, false color and scene classification

### Secondary sources
Paleochannel maps to compare results and prepare training data.

## Data preparation
### Noise reduction
Small but irrelevant details resulting from various phenomena may affect the accuracy of the model. Artifacts may also
appear as a result of how the data was captured or processed.

Test and compare models trained on the normal and noise-reduced images. As satellite imagery is not as high-resolution
as a photo from up close, this may end up not being an issue

### Radiometric correction
Radiometric correction implies the correction of errors stemming from the fact that different objects are illuminated
differently.

### Georeferencing
Images without georeferencing information will need it applied, which means assigning a coordinate to every pixel in an
image.

### Splicing images, rearranging bands, creating mosaics
The creation of mosaics, cropping parts of the image that are not of interest and only using select bands can keep
the total data smaller and more focused on the area of interest for the study.

> [!Note] Use same source as Fabrizio's tesis here

## Data augmentation
These are methods meant to enhance certain aspects of an image, or increase its usefulness in some sense.

### Contrast manipulation
There are various techniques for manipulating contrast, which in effect amplifies the differences between light and
dark areas of the image, or amplifies differences in some chosen band to make transitions in the image more dramatic.
Contrast manipulation can make segmentation and contour maps easier to produce.

### Spatial feature manipulation
There are several ways of manipulating spatial features: spatial filters, convolution filters and edge enhancement.

Spatial filters allow for removing or heightening details in an image, for example image sharpening or applying a low
pass filter. Convolution filters are typically used for various features with smaller output sizes compared to the
original image, but with some detail enhanced, for example edge detection filters. Edge enhancement aims to increase the
apparent sharpness of an image by increasing the contrast of edges in the image.

> [!Note] Source
> https://astrogeology.usgs.gov/docs/concepts/image-processing/the-power-of-spatial-filters/

### Multiple image manipulation
Creating composite images representing relationships between datapoints in different bands can be useful to lift out
details otherwise not visible. For example, the relationship between the reflection of red and near infrared in plants
can be used to determine how healthy the plants are, and the use of indices like NDVI, SAVI or NDSI can help find
various relationships between bands in the images.

## Classification
This is the main objective of image classification. It consists of replacing visual interpretation with quantitative
techniques to automate the identification of characteristics in a scene. For satellite imaging, this implies the
analysis of multiple bands in the image, which are effectively additional dimensions of an image. The ultimate goal is
to assign labels to every pixel in an image according to a list of possibilities.

The implementation of the classification model will be done in Python, as there are a multitude of ready-made libraries
to support fast prototyping and development of classifier models.

## Training and validation


