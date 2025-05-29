2025-05-29
---
# Tesis - Dev Planning

## Goals
- Classification of images with/without paleochannels
- Segmentation of paleochannels in images

## Brainstorming
Great place to look for tooling: https://www.osgeo.org/projects/
 
Use Pytorch, in particular something like TorchGeo looks interesting (even if it is from M$).
- https://torchgeo.readthedocs.io/en/latest/

Pytorch also supports CUDA and ROCm from Nvidia and AMD respectively: https://pytorch.org/get-started/locally/

https://github.com/Bengal1/Simple-CNN-Guide/tree/main can be used as a test to see if the installation is using the GPU.

For fetching data we can use the OGC API which Copernicus supports: https://dataspace.copernicus.eu/ogc-api.
There is also a python package to use it: https://github.com/geopython/pygeoapi

Take a look at https://github.com/giswater, made to analyze the water cycle in GIS applications like QGIS. Could be useful

Take a look at https://www.osgeo.org/projects/open-data-cube/ for indexing large amounts of data, maybe it simplifies getting or organizing the data to be used
