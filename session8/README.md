# EVA6 Session 8 #

Session 8 assignment submission for EVA6

## Team ##

* S R Prathaban
* Santosh Chaganti

## Solution ##
* Implemented Resnet18 in the desired structure. 
* Created a separate repo to hold the training template files (https://github.com/prathaban-sr/soai_repo)
* Created a python wheel file for the above (https://github.com/prathaban-sr/soai_repo/blob/main/dist/soai-0.0.1-py3-none-any.whl)
* Tested on Google Colab using the wheel file with the following conditions (https://github.com/prathaban-sr/eva6/blob/main/session8/EVA_Session8.ipynb)
- Train resnet18 for 20 epochs on the CIFAR10 dataset
- Show loss, accuracy curves for test and train datasets
- Show a gallery of 10 misclassified images
- Show gradcam output on 10 misclassified images. 

* **Training**
1. Trained for 20 epochs
2. SGD optimizer with a learning rate of 0.01
3. CosineAnnealingLR

* **Loss, Accuracy graphs**
![Accuracy, Loss Graphs](https://github.com/prathaban-sr/eva6/blob/main/session8/training_loss.png)

* **Wrongly classified images**

![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_2.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_3.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_4.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_5.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_6.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_7.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_8.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_9.png)
![Wrongly classified images](https://github.com/prathaban-sr/eva6/blob/main/session8/wrong_classification_10.png)

* **Attention Maps**

![Original Images](https://github.com/prathaban-sr/eva6/blob/main/session8/original_imgs.png)

![Heatmap](https://github.com/prathaban-sr/eva6/blob/main/session8/attention_map.png)

* **Results**
* Train Loss:0.093,Acc:96.770(48385/50000)
* Test Loss:0.671,Acc:83.610(8361/10000)

