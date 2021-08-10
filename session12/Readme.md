# EVA6 Session 12 #

Session 12 Spatial Transformer Network assignment submission for EVA6

## Team ##

* S R Prathaban

## Solution ##

* **Spatial Transformer Networks**
* Spatial Transformer Networks allow a neural network to learn to generate augmentations for images in order to enhance the spatial invariance of the model. e.g., it can crop a region of interest, scale and correct the orientation of an image. Since CNNs are not invariant to spatial transformations, this can help improve the accuracy of the model.
* The model trains a set of 6 theta parameters which are applied to the input image using the affine_grid and grid_sample functions to generate the augmentation.   
![STN Transformations](https://github.com/prathaban-sr/eva6/blob/main/session12/dataset.png)

* **File Links**
1. [Colab File](https://colab.research.google.com/drive/1WPXThSaKefkHcp3iNLJSOa8wLdYPQjL1?usp=sharing)
2. [Github Link](https://github.com/prathaban-sr/eva6/blob/main/session12/EVA_Spatial_Transformer_CIFR.ipynb)

* **Visual Transformer Code Explained**
1. [Code Explained](https://github.com/prathaban-sr/eva6/blob/main/session12/Vit_explained.md)
