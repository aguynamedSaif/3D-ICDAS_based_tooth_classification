# 3D-ICDAS_based_tooth_classification
This repo features code for an experiment on 56 restorative cavities on simulated molars using four ICDAS classifications. 3D CNN assessed cavity size, and operator proficiency, and predicted ICDAS class.


This repository contains the following:

1. **Deep Learning Workflows**: 
   - A workflow to classify work performed by two operators, along with their corresponding saliency maps.
   ![Workflow for 2 Operators](https://github.com/aguynamedSaif/3D-ICDAS_based_tooth_classification/raw/main/utils/workflow_2operator.jpg)

   - A workflow to classify ICDAS cavity classes, with saliency maps to explain the model's decisions.
   <img src="" alt="Diagram of Workflow" width="500">

2. **Data Processing Script**: 
   - A script to convert .stl files into 2D slices, and then accumulate these slices into .npy files, ready for 3D convolution in neural networks.

This setup facilitates the analysis and classification of dental cavities and operator proficiency using deep learning techniques.