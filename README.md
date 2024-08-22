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