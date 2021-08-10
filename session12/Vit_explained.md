# EVA6 Session 12 #

Session 12 Vit Code explained
* [Code] (https://github.com/jeonsworld/ViT-pytorch/blob/main/models/modeling.py)

## Block ##

The Block class represents one block of the Transformer Encoder which consists of
1. Layer Normalization of the input
2. Multi-head attention
3. Addition of the Residual connection from the input to the output of the attention layer
4. Layer normalization of above
5. MLP layer
6. Addition of the Residual connection from (3) to the output of the MLP layer 

## Embeddings ##

The Embeddings class is responsible for
1. Generate the patch embeddings  
2. Initialize the position embeddings and CLS token
3. Add the patch and position embeddings



* **Vit **
* Spatial Transformer Networks allow a neural network to learn to generate augmentations for images in order to enhance the spatial invariance of the model. e.g., it can crop a region of interest, scale and correct the orientation of an image. Since CNNs are not invariant to spatial transformations, this can help improve the accuracy of the model.
* The model trains a set of 6 theta parameters which are applied to the input image using the affine_grid and grid_sample functions to generate the augmentation.   
![STN Transformations](https://github.com/prathaban-sr/eva6/blob/main/session12/dataset.png)

* **File Links**
* [Colab File](https://colab.research.google.com/drive/1WPXThSaKefkHcp3iNLJSOa8wLdYPQjL1?usp=sharing)
* [Github Link](https://github.com/prathaban-sr/eva6/blob/main/session12/EVA_Spatial_Transformer_CIFR.ipynb)
