# Brain Tumor Detection Using HOG and SVM

## Overview

This project focuses on detecting brain tumors in MRI images using Histogram of Oriented Gradients (HOG) for feature extraction and Support Vector Machine (SVM) for classification. The pipeline involves preprocessing MRI images, extracting relevant features using HOG, training an SVM classifier, and evaluating its performance on labeled datasets.

![Block Diagram](./41008470-5c5e-4fbf-8eae-6c7c6965c86f.png)

## Models Used

### Feature Extraction: HOG (Histogram of Oriented Gradients)

HOG is utilized to capture gradient and edge information from MRI scans. This method is effective in distinguishing structural patterns present in tumor versus non-tumor regions.

- Implemented using `skimage.feature.hog`.
- Parameters like orientations, pixels per cell, and cells per block were fine-tuned to optimize detection accuracy.

![HOG Feature Extraction](./6f2fc955-7cea-438f-9452-26907402d87a.png)

### Classification: SVM (Support Vector Machine)

An SVM classifier is used to categorize MRI images as either tumor or non-tumor.

- Implemented using `sklearn.svm.SVC`.
- Kernel used: RBF (Radial Basis Function).
- Hyperparameters such as C and gamma were optimized via grid search.

## Dataset

The dataset consists of pre-labeled MRI brain images classified into tumor and non-tumor categories.

- Source: Brain MRI Images for Brain Tumor Detection.
- Preprocessing included resizing images, grayscale conversion, and normalization.

![Sample MRI Images](./33459f62-2074-4af8-938e-7f5cf7b91aba.png)

## Workflow

### Data Preprocessing:

- Image resizing to 128x128.
- Conversion to grayscale.
- Normalization.

### Feature Extraction:

- Extract HOG features from each preprocessed image.

### Model Training:

- Split dataset into training and testing sets.
- Train SVM classifier with extracted HOG features.

### Model Evaluation:

- Evaluate using metrics such as accuracy, precision, recall, F1 score.

## Results

The final model achieved the following metrics on the test set:

- **Accuracy**: 94.3%
- **Precision**: 93.8%
- **Recall**: 95.1%
- **F1 Score**: 94.4%

These results suggest the model is reliable for initial-level brain tumor detection tasks in MRI images.

## Dependencies

- Python 3.x
- scikit-learn
- scikit-image
- numpy
- matplotlib

