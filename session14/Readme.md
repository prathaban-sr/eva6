# EVA6 Session 14 #

Session 14 DETR

## Team ##

* S R Prathaban

## Solution ##

* **DETR**

DETR is a single pass architecture that uses standard CNN and transformer models along with bipartite loss to generate SOTA level results on multiple problems like object detection, panoptic segmentation etc.
The use of bipartite loss with an appropriate threshold value also helps to avoid the usage of post-processing tasks like NMS. 

The DETR architecture has the following main components
1. Backbone network
        DETR uses a ResNet50 architecture to generate rich embeddings
2. Transformer Encoder
        The embeddings from the backbone network are added to the positional encodings. This is then converted to a 1D sequence to feed to the transformer encoder. The transformer encoder is a set of layers each consisting of a multi-head self attention layer followed by a  FFN. 
3. Transformer Decoder
         The encoder output and N positional embeddings, called object queries, are fed to the Transformer decoder. Each layer of the Transformer decoder consists of a multi-head self attention, multi-head attention and a FFN layer.
4. FFN 
      The FFN layer outputs class label and bounding box predictions 

* **Encoder-Decoder**
1. Encoder
The transformer encoder architecture with its (self)attention mechanism allows the network to reason across the entire image (large receptive fields) in a performant way. The embeddings from the backbone network are added to the positional encodings. This is then converted to a 1D sequence to feed to the transformer encoder. The transformer encoder is a set of layers each consisting of a multi-head self attention layer followed by a  FFN. 

2. Decoder
The encoder output and N positional embeddings, called object queries, are fed to the Transformer decoder. Each layer of the Transformer decoder consists of a multi-head self attention, multi-head attention and a FFN layer. The N object queries are transformed into an output embedding by the decoder. The decoder also generates all the bounding boxes/labels at the same time. 

* **Bi-partite Loss**
Bipartite loss provides an elegant way of solving the object detection problem without requiring pre-knowlede of the problem, choosing anchor boxes and avoids post-processing like NMS. It is designed as a set based problem where loss is defined as the level of matching between N predicted labels/bounding boxes and the ground-truth. Both sets have the same number of elements (populated with Null class predictions if necessary). Since the loss looks for a 1-1 correspondence of the boxes, the best fitting bounding box is chosen while eliminating duplicate matches.

* **Object Queries**

Object Queries are N embeddings of size d that are transformed into an output embedding by the decoder in parallel. They are independently decoded into box coordinates and class labels by a feed forward network. 

* **Detection sample**
![Detection sample](https://github.com/prathaban-sr/eva6/blob/main/session14/download.png)

