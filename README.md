# 3D-ICDAS_based_tooth_classification
This repo features code for an experiment on 56 restorative cavities on simulated molars using four ICDAS classifications. 3D CNN assessed cavity size, and operator proficiency, and predicted ICDAS class.



<div align="center">

  <a href="https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/blob/main/utils/flowchart.jpg">
    <img src="https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/raw/main/utils/flowchart.jpg" alt="Flowchart" width="600" />
  </a>

</div>




This repository contains the following:

1. **Deep Learning Workflows**: 
   - [A workflow to classify work performed by two operators, along with their corresponding saliency maps.](https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/tree/main/2_operators_classification/code)

   

<div align="center">

  <img src="https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/raw/main/utils/workflow_2operator.jpg" alt="Workflow for 2 Operators" width="600" />

  <img src="https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/raw/main/utils/ICDAS%202%20Operators%20Classification.svg" alt="ICDAS 2 Operators Classification" width="600" />

</div>



   - [A workflow to classify ICDAS cavity classes, with saliency maps to explain the model's decisions.](https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/tree/main/4_classes_classification)

<div align="center">

  <img src="https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/raw/main/utils/workflow_ICDAS.jpg" alt="Workflow for ICDAS Classification" width="600" />

  <img src="https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/raw/main/utils/ICDAS%20Classification.svg" alt="ICDAS Classification" width="600" />

</div>


2. **Data Processing Script**: 
   - [A script to convert .stl files into 2D slices, and then accumulate these slices into .npy files, ready for 3D convolution in neural networks.](https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/blob/main/preprocessing/preprocessing.ipynb)

This setup facilitates the analysis and classification of dental cavities and operator proficiency using deep learning techniques.

The 3D Convolutional Neural Network (3D-CNN) model architecture was then adopted for classifying 3D tooth images into four categories: ICDAS class 3, 4, 5, and 6. It consists of three convolutional layers followed by max-pooling operations to extract important features from the tooth images. 
The convolutional layers gradually increase in complexity, with the first layer having 16 channels, the second layer having 32 channels, and the third layer having 64 channels. Each layer uses a 3x3x3 filter to maintain spatial dimensions. Max-pooling layers then down sample the feature maps to extract key patterns. The model's output was processed through two fully connected layers for final classification, with a dropout layer included to prevent overfitting. 
The convolutional layers extracted complex features from the 3D tooth images using convolution operations and Rectified Linear Unit (ReLU) activation functions.18 These features were then further refined through max-pooling layers to identify dominant patterns within the cavity. The fully connected layers process these features for final classification. Additionally, dropout regularization helped enhance the model's generalization by randomly deactivating neurons during training.
The same model was applied to differentiate between corresponding ICDAS preparations made by two different operators. The classifier was modified to distinguish between Operator A and Operator B instead of ICDAS classes. 
The following are the hyperparameter details of the training part:

epochs = 500
batch_size = 2
learning_rate = 1e-3
weight_decay = 0.0000000001
momentum=0.9