# EVA6 Session 7 #

Session 7 assignment submission for EVA6

## Team ##

* S R Prathaban
* Divyanshu Raj
* Siddharth Vij
* Santosh Chaganti

## Solution ##
* **Network architecture**
```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 64, 16, 16]           1,792
       BatchNorm2d-2           [-1, 64, 16, 16]             128
           Dropout-3           [-1, 64, 16, 16]               0
            Conv2d-4            [-1, 112, 8, 8]          64,624
       BatchNorm2d-5            [-1, 112, 8, 8]             224
           Dropout-6            [-1, 112, 8, 8]               0
            Conv2d-7            [-1, 112, 8, 8]           1,120
            Conv2d-8            [-1, 112, 8, 8]           1,120
            Conv2d-9             [-1, 84, 8, 8]           9,492
           Conv2d-10             [-1, 84, 8, 8]           9,492
      BatchNorm2d-11             [-1, 84, 8, 8]             168
          Dropout-12             [-1, 84, 8, 8]               0
           Conv2d-13            [-1, 128, 4, 4]          96,896
      BatchNorm2d-14            [-1, 128, 4, 4]             256
          Dropout-15            [-1, 128, 4, 4]               0
        AvgPool2d-16            [-1, 128, 1, 1]               0
           Linear-17                   [-1, 10]           1,290
================================================================
Total params: 186,602
Trainable params: 186,602
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.01
Forward/backward pass size (MB): 0.86
Params size (MB): 0.71
Estimated Total Size (MB): 1.58
----------------------------------------------------------------
```

## Data Augmentation ##
```
A.Compose([
    A.HorizontalFlip(p=0.4),
    A.ShiftScaleRotate(shift_limit=0.05, scale_limit=0.05, rotate_limit=15, p=0.5),
    A.CoarseDropout(max_holes = 1, max_height=4, max_width=4, min_holes = 1, 
                    min_height=1, min_width=1, fill_value=[0.49139968, 0.48215841, 0.44653091]),
    A.Normalize(mean=(0.49139968, 0.48215841, 0.44653091), std=(0.24703223, 0.24348513, 0.26158784)),
    ToTensorV2(),
])
```

* **Training**
1. Trained for 20 epochs
2. SGD optimizer with a learning rate of 0.02
3. StepLR

* **Results**
1. Test set: Accuracy: 83.59%
