# Breast Tumor Classification Using Convolutional Neural Networks

## Problem statement

Breast cancer is a major health problem, and medical imaging plays an important role in the assessment of breast abnormalities. Breast ultrasound provides images that can contain characteristics associated with benign and malignant tumors, but interpretation of these images requires specialized expertise and can be challenging.

Deep-learning methods, particularly convolutional neural networks (CNNs), can automatically learn visual patterns from medical images and may therefore be useful for computer-assisted breast-tumor classification.

However, simply developing a CNN is not enough; its performance needs to be systematically evaluated, and its predictions should be interpretable to determine whether it is focusing on relevant regions of the ultrasound images.

Therefore, this study will develop and evaluate a CNN-based model for classifying breast ultrasound images and investigate the image regions contributing to its predictions using explainable-AI techniques.

## General aim

To develop and evaluate a convolutional neural network for classifying breast ultrasound images into normal, benign, and malignant categories.

### Specific objectives

- To preprocess and prepare breast ultrasound images for CNN-based classification.

- To develop a CNN model for classifying breast ultrasound images into normal, benign, and malignant categories.

- To evaluate the performance of the CNN using appropriate classification metrics.

- To compare the performance of a custom CNN with a transfer-learning model such as ResNet50 or EfficientNet.

- To investigate the regions of ultrasound images contributing to model predictions using Grad-CAM.

## Research questions

### Main research question

Can convolutional neural networks accurately classify breast ultrasound images into normal, benign, and malignant categories?

### Specific research questions

1. How effectively can a CNN classify breast ultrasound images into normal, benign, and malignant categories?

2. How does a transfer-learning model compare with a CNN developed from scratch for breast-tumor classification?

3. Which evaluation metrics best characterize the performance of the models across the three classes?

3. Which regions of breast ultrasound images contribute most strongly to the CNN's predictions?

4. How does image augmentation affect CNN classification performance?

## Methodology

### Study design

Quantitative experimental machine-learning study using publicly available breast ultrasound images.

#### Step 1 — Data acquisition

- Obtain the BUSI dataset.

#### Step 2 — Data preprocessing

- Organize images by class

- Resize images to a consistent size

- Normalize pixel values

- Check image quality

- Remove inappropriate/duplicate images where necessary

#### Step 3 — Data splitting

Divide the data into:

Training set

Validation set

Test set

Important: because multiple images can originate from the same patient, the split should ideally be performed at the patient level, so images from the same patient don't appear in both training and testing. This prevents data leakage.

#### Step 4 — Data augmentation

Apply appropriate transformations to training images

#### Step 5 — CNN development

Develop a CNN using TensorFlow/Keras.

#### Step 6 — Transfer learning

Train a pretrained architecture 

#### Step 7 — Model evaluation

Evaluate using:

Accuracy

Precision

Recall/sensitivity

Specificity

F1-score

Confusion matrix

ROC-AUC where appropriate

Because this is a medical classification problem, recall/sensitivity and false negatives deserve particular attention, rather than relying on accuracy alone.

#### Step 8 — Explainability

Use Grad-CAM to generate heatmaps showing which image regions contributed to the CNN's predictions.

## Data source

Breast Ultrasound Images (BUSI)

The original BUSI dataset was developed by Al-Dhabyani and colleagues and contains 780 ultrasound images from 600 women aged 25–75, divided into:

Normal

Benign

Malignant

Link:

[Diabetes](https://archive.ics.uci.edu/dataset/296/diabetes?)


