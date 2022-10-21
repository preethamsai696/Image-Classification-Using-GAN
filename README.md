
# Diabetic Retinopathy Detection

This a deep learning project which involves classsification of eye images.


## Aim
The main goal of this project is to develop a deep learning model to classify the images based on the level of diabetic retinopathy present in it.
## Data Set
Kaggle data set provided by EyePacs was used in this project. All the images were labelled by the clinicians on a scale of 0-4 based on the level of diabetic retinopathy. Out of 13,000 images, 10,000 were used for training and 3,000 were used for testing the developed model.

The data set distribution is as follows,


| Diabetic Retinopathy Class | Train Dataset Label Distribution | Test Dataset Label Distribution |
|:--------------------------:|:--------------------------------:|:-------------------------------:|
|              0             |               7257               |               2252              |
|              1             |                731               |               219               |
|              2             |               1585               |               418               |
|              3             |                240               |                56               |
|              4             |                187               |                55               |

## Process
The model developement involved the following methodology,
      
      1. Data PreProcessing 
      2. Building a Convolutional Neural Network model
      3. Data Augmentation
      4. Transfer Learning
## Results
The project resulted in generating two different types of result.
    1. Results obtained from CNN model
    2. Results obtained from Transfer Learning


| Class | Precision | Recall | f1-score | support |
|:-----:|:---------:|:------:|:--------:|:-------:|
|   0   |    0.76   |  0.64  |   0.70   |   2252  |
|   1   |    0.12   |  0.05  |   0.08   |   219   |
|   2   |    0.15   |  0.08  |   0.10   |   418   |
|   3   |    0.07   |  0.02  |   0.03   |    56   |
|   4   |    0.09   |  0.02  |   0.03   |    55   |


##### Transfer Learning(Without Class Weights):

| S.No | Model Architecture |  Loss  | Accuracy(%) |
|:----:|:------------------:|:------:|:-----------:|
|  1.  |      Xception      | 0.7782 |    74.43    |
|  2.  |     DenseNet169    | 0.8527 |    72.00    |
|  3.  |     DenseNet201    | 0.8594 |    71.53    |
|  4.  |     ResNet50V2     | 1.0802 |    67.67    |
|  5.  |       VGG-16       | 1.7917 |    66.43    |
|  6.  |       VGG-19       | 1.8839 |    66.40    |
|  7.  |     ResNet152V2    | 1.1017 |    66.07    |


##### Transfer Learning(With Class Weights):

| S.No | Model Architecture |  Loss  | Accuracy(%) |
|:----:|:------------------:|:------:|:-----------:|
|  1.  |     ResNet50V2     | 1.0826 |    68.67    |
|  2.  |       VGG-19       | 1.8839 |    66.23    |
|  3.  |       VGG-16       | 1.7458 |    64.07    |
|  4.  |      Xception      | 0.9598 |    63.47    |
|  5.  |     DenseNet169    | 0.9947 |    61.10    |
|  6.  |     DenseNet201    | 1.0831 |    53.80    |
|  7.  |     ResNet152V2    | 1.5105 |    42.90    |



