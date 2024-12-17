# Brain Tumor MRI Segmentation Using U-Net  

## Table of Contents  
- [Overview](#overview)  
- [Problem Statement](#problem-statement)  
- [Objectives](#objectives)  
- [Datasets Used](#datasets-used)  
- [Methodology](#methodology)  
  - [U-Net Architecture](#u-net-architecture)  
  - [Preprocessing and Data Augmentation](#preprocessing-and-data-augmentation)  
  - [Evaluation Metrics](#evaluation-metrics)  
- [Execution Environment](#execution-environment)
- [Results and Discussion](#results-and-discussion)  
- [Future Scope](#future-scope)  

---

## Overview  
Brain tumors are critical health conditions requiring accurate and timely diagnosis to ensure effective treatment. This project aims to develop an automated approach for brain tumor segmentation using MRI scans, leveraging the U-Net architecture to achieve precise segmentation of tumor regions. By automating the segmentation process, the project provides a reliable and efficient method to assist medical professionals in diagnosis and treatment planning.  

---

## Problem Statement  
Develop a method to improve the accuracy of brain tumor segmentation in MRI scans using a U-Net-based architecture to provide precise and reproducible results, reducing human error and saving time.  

---

## Objectives  
- Develop a U-Net-based brain tumor segmentation model to achieve high accuracy and precision in MRI-based tumor delineation.  
- Provide a reliable, automated tool to assist radiologists and medical professionals in identifying tumor boundaries.  

---

## Datasets Used  
The following publicly available datasets were used for training and validation:  
1. [Brain Tumor Segmentation Dataset](https://www.kaggle.com/datasets/atikaakter11/brain-tumor-segmentation-dataset)  
   - Contains labeled MRI images for tumor segmentation tasks.  
2. [Brain Tumor Classification MRI Dataset](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri)  
   - Offers MRI images of glioma, meningioma, pituitary tumors, and non-tumor cases.  

---

## Methodology  

### U-Net Architecture  
The U-Net architecture was chosen for its proven ability to perform image segmentation tasks effectively. Key features include:  
- **Encoder-Decoder Design:** Extracts features in the encoding path and reconstructs the segmented image in the decoding path.  
- **Skip Connections:** Preserves spatial hierarchies, ensuring accurate segmentation even for small tumor regions.  

### Preprocessing and Data Augmentation  
To improve model performance and generalizability:  
- **Preprocessing:** MRI images were normalized to ensure uniform intensity distribution.  
- **Data Augmentation:** Included flipping, rotation, zooming, and contrast adjustments to increase dataset variability and reduce overfitting.  

### Evaluation Metrics  
The model was evaluated using standard segmentation metrics:  
- **Dice Coefficient:** Measures overlap between predicted and ground-truth masks.  
- **Intersection over Union (IoU):** Evaluates the accuracy of the segmented region.  

---

## Execution Environment  
The project was implemented and executed on Kaggle Notebooks. The code available in this repository is the direct export of the completed Kaggle notebook.  

**Programming Language:** Python  
**Frameworks and Libraries Used:**  
- TensorFlow/Keras for deep learning model implementation.  
- OpenCV and NumPy for image preprocessing and manipulation.  
- Matplotlib and Seaborn for visualization of metrics and results.  

---
## Results and Discussion

### Quantitative Evaluation  
- **Accuracy:**  
  - Training: 99.51%  
  - Validation: 99.47%  

- **Dice Coefficient:**  
  - Training: 0.9054  
  - Validation: 0.8807  

- **Intersection over Union (IoU):**  
  - Training: 0.8275  
  - Validation: 0.7877  

### Qualitative Evaluation  
- Predicted segmentation masks closely matched ground-truth masks, demonstrating high boundary precision.  
- The model performed well across various tumor types (glioma, meningioma, pituitary) and non-tumor cases, as shown in visualizations.

---

## Future Scope  
- **Expand Dataset:** Train the model on larger and more diverse datasets to improve robustness.  
- **Multi-Class Segmentation:** Extend the model to simultaneously classify and segment tumor types.  
- **Post-Processing:** Apply morphological operations to refine boundaries for higher precision.  
- **Deployment:** Develop a web-based tool or application for real-time segmentation in clinical settings.  
