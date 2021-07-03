# EVA6 Session 8 #

Session 8 assignment submission for EVA6

## Team ##

* S R Prathaban
* Santosh Chaganti

## Solution ##
* Implemented Resnet18 in the desired structure. 
* Created a separate repo to hold the training template files
* Created a python wheel file for the above
* Tested on Google Colab using the wheel file with the followin conditions
** Train resnet18 for 20 epochs on the CIFAR10 dataset
** Show loss, accuracy curves for test and train datasets
** Show a gallery of 10 misclassified images
** Show gradcam output on 10 misclassified images. 

* **Training**
1. Trained for 20 epochs
2. SGD optimizer with a learning rate of 0.01
3. CosineAnnealingLR

* **Loss, Accuracy graphs**
![alt text](https://github.com/prathaban-sr/eva6/blob/main/session8/training_loss.png)



* **Results**
1. Test set: Accuracy: 83.59%
