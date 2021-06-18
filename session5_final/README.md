# EVA6 Repository #

Repository for all assignment submissions for EVA6

## Team ##

* S R Prathaban
* Divyanshu Raj
* Siddharth Vij
* Santosh Chaganti

### Session 5 Assignment ###

### Iteration 1
* **Main file** EVA_Session_5_experiment3_1 
### Target
Light network with <8K parameters

### Result

*   Parameters : 7,702
*   Best Train Accuracy : 98.9
* Best Test Accuracy : 98.9

### Analysis

*   Test Accuracy between 98.5 and 98.9 over last few epochs

### Iteration 2
* **Main file** EVA_Session_5_experiment3_2 
### Target
Add batch normalization and dropout regularisation

### Result

*   Parameters : 7,854
*   Best Train Accuracy : 99.5
* Best Test Accuracy : 99.31

### Analysis

*   Test Accuracy at 99.3 for last 2 epochs.
*   Test and train accuracy are tracking very closely
* Seeing the wrong image set, we can rotate images to improve prediction.

### Iteration 3
* **Main file** EVA_Session_5_experiment3_3 
### Target
Add image augmentation by introducing random rotation

### Result

*   Parameters : 7,854
*   Best Train Accuracy : 99.4
* Best Test Accuracy : 99.32

### Analysis

*   Test Accuracy varying between 99.15 and 99.32 over last 5 epochs..
*   Test and train accuracy are tracking very closely
* Seeing the wrong image set, we can conclude that it is difficult even for a human to predict those images correctly.

### Iteration 4
* **Main file** EVA_Session_5_experiment3_4 
### Target
Control the Learning Rate as an inverse factor of test accuracy

### Result

*   Parameters : 7,854
*   Best Train Accuracy : 99.43
* Best Test Accuracy : 99.43

### Analysis

*   Test Accuracy 99.4 consistent over last 10 epochs.
*   Test and train accuracy are tracking very closely
* Seeing the wrong image set, we can conclude that it is difficult even for a human to predict those images correctly.
