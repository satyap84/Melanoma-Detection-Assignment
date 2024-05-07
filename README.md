# Melanoma Detection Assignment
> This project is to build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
- The CNN model is built using a dataset which consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
- The data set contains the following diseases:
    - Actinic keratosis
    - Basal cell carcinoma
    - Dermatofibroma
    - Melanoma
    - Nevus
    - Pigmented benign keratosis
    - Seborrheic keratosis
    - Squamous cell carcinoma
    - Vascular lesion
- However the class data was imbalanced. Augmentor was used to generate 500 images of each class so that some balance is achieved.
- Transfer Learning is not used for this project and a custom CNN model is created.


## Conclusions
- Without the use of regularazation and dropout layer, the model tend to overfit. There is huge difference betweeh the training accuracy and validation accuracy. The validation loss is also high.
- With the inclusion of dropout layer, the problem of overfitting got somewhat solved, however the overall accuracy is not that high.
- After checking the distribution of classes in training dataset it is found that some classes have very low volume and some has very high volume.
- Augmentor was used to generate 500 images of each class so that some balance is achieved. 
- After which Final model is created by doing following changes:
    - Batch normalization is added to the conv2D layers.
    - 3rd Conv2 layer block is added to capture more details
    - Dropout percentage is adjusted to counter overfitting.
- Final model gave very good accuracy and does not show any sign of overfitting or underfitting. Training and validation losses are also small.


## Technologies Used
- Python 3.11.4


## Contact
Created by [@satyap84] - feel free to contact me!