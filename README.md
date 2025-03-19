# Melanoma-Detection

This project utilizes a CNN-based approach to accurately identify melanoma—a dangerous type of skin cancer that can be fatal if not caught early. Since melanoma is responsible for 75% of skin cancer-related deaths, a tool that analyzes images and alerts dermatologists can significantly reduce manual diagnostic efforts.

## Table of Contents
- [Problem Overview](#problem-overview)
- [Project Workflow](#project-workflow)
- [Technologies and Tools](#technologies-and-tools)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

<!-- Feel free to add any additional sections as needed -->

## Problem Overview

### Understanding the Challenge

The dataset comprises 2,357 images representing both malignant and benign skin conditions, collected by the International Skin Imaging Collaboration (ISIC). These images have been categorized according to ISIC classifications, with a slightly higher number of images for melanomas and moles.

The collection includes the following conditions:
- Actinic Keratosis
- Basal Cell Carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented Benign Keratosis
- Seborrheic Keratosis
- Squamous Cell Carcinoma
- Vascular Lesion

### Project Objective

Develop a multi-class classification model using a custom convolutional neural network (CNN) built with TensorFlow.

### Risk Considerations

- Incorrectly predicting the type of skin cancer, which could lead to misdiagnosis

## Project Workflow

- **Data Preparation & Exploration:** Establish paths for both training and testing image directories.
- **Dataset Creation:** Generate training and validation datasets from the available images, using a batch size of 32 and resizing images to 180x180.
- **Visualization:** Develop a script to display a representative sample from each of the nine classes.
- **Initial Model Building & Training:**
  - Construct a CNN model capable of differentiating the nine classes, with image pixel values normalized between 0 and 1.
  - Select a fitting optimizer and loss function.
  - Train the model for roughly 20 epochs and assess for overfitting or underfitting.
- **Data Augmentation:** Implement a robust augmentation strategy to mitigate overfitting/underfitting issues.
- **Enhanced Model Training on Augmented Data:**
  - Rebuild the CNN model (with normalization) using the augmented dataset.
  - Continue with the previously chosen optimizer and loss function.
  - Train for another 20 epochs and verify if the earlier issues have been resolved.
- **Class Distribution Analysis:**
  - Identify the class with the fewest samples.
  - Determine which classes are over-represented.
- **Addressing Class Imbalance:** Apply the Augmentor library to correct any imbalances in the training data.
- **Final Model Training on Balanced Data:**
  - Re-develop the CNN model with normalization.
  - Use an appropriate optimizer and loss function.
  - Train for about 30 epochs.

## Technologies and Tools

- **TensorFlow:** Version 2.18.0
- **Keras:** Version 3.9.0
- **Matplotlib:** Version 3.10.0
- **NumPy:** Version 1.26.4
- **Pandas:** Version 2.2.2
- **PIL:** Version 10.3.0
- **Augmentor:** Version 0.2.12

<!-- It is recommended to include version details as libraries are frequently updated -->

## Acknowledgements

<!-- Add any acknowledgements or credits here -->

## Contact

**Author:** Sanjay Barnwal
