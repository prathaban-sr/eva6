# EVA6 Session 12 #

Session 12 Vit Code explained
* [Code] (https://github.com/jeonsworld/ViT-pytorch/blob/main/models/modeling.py)

## Block ##

The Block class represents one block of the Transformer Encoder which is responsible for

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

## MLP ##

The MLP class is responsible for
1. Applying a FC layer to the output of the transformer encoder  
2. It then applies the GELU activation function 
3. Finally, applies a second FC layer to generate the output

## Attention ##

The Attention class is responsible for implementing the multi-head attention using the below

1. Attention(Q, K, V ) = softmax(QKt√dk)V #Kt - Keys transposed. 
2. This is then passed through a Linear layer

## Encoder ##

The Encoder class is resposible for 

1. Implementing all the layers of the Transformer Encoder
2. The output of each layer is sent to the subsequent layer
3. Layer normalization to generate the output

