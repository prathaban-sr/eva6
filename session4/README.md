# EVA6 Session 4 #

Session 4 assignment submission for EVA6

## Team ##

* S R Prathaban
* Divyanshu Raj
* Siddharth Vij
* Santosh Chaganti

### Session 4 Assignment ###
## PART I
* **Back Propogation**

## Training model on Excel
![Test PDF 1](https://github.com/prathaban-sr/eva6/blob/main/session4/back_prop.png)

## Graphs for varying learning rates
![Test Image 1](https://github.com/prathaban-sr/eva6/blob/main/session4/Learning%20Rate%20Variation.png)

## PART II
* **Main file** EVA_Session_4.ipynb
* **Contents** 
MNIST classification using CNN. 
* **Requirements** 
1. Use less than 20K parameters
1. Train for less than 20 epochs
1. Accuracy >= 99.4% 

* **Solution**
* **Network architecture**
```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1            [-1, 8, 26, 26]              80
       BatchNorm2d-2            [-1, 8, 26, 26]              16
            Conv2d-3           [-1, 16, 24, 24]           1,168
       BatchNorm2d-4           [-1, 16, 24, 24]              32
            Conv2d-5           [-1, 16, 22, 22]           2,320
       BatchNorm2d-6           [-1, 16, 22, 22]              32
         MaxPool2d-7           [-1, 16, 11, 11]               0
           Dropout-8           [-1, 16, 11, 11]               0
            Conv2d-9             [-1, 24, 9, 9]           3,480
      BatchNorm2d-10             [-1, 24, 9, 9]              48
          Dropout-11             [-1, 24, 9, 9]               0
           Conv2d-12             [-1, 24, 7, 7]           5,208
      BatchNorm2d-13             [-1, 24, 7, 7]              48
          Dropout-14             [-1, 24, 7, 7]               0
           Conv2d-15             [-1, 32, 5, 5]           6,944
      BatchNorm2d-16             [-1, 32, 5, 5]              64
        AvgPool2d-17             [-1, 32, 1, 1]               0
           Linear-18                   [-1, 10]             330
================================================================
Total params: 19,770
Trainable params: 19,770
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.45
Params size (MB): 0.08
Estimated Total Size (MB): 0.53
----------------------------------------------------------------
```

* **Training**
1. Trained for 19 epochs
1. SGD optimizer with a learning rate of 0.1

* **Results**
1. Train set: Accuracy: 59796/60000 (99.66%)
2. Test set: Accuracy: 9951/10000 (99.51%)
