---
title: Parking Space Analysis
publishDate: 2019-12-01 00:00:00
img: /assets/parking.png
img_alt: A bright pink sheet of paper used to wrap flowers curves in front of rich blue background
description: |
  A system able to analyze an image to determine whether a parking space is occupied.


tags:
  - Python
  - Machine Learning
---

The project aims to classify images of parking spaces as either “occupied” or “free” using machine learning techniques. It utilizes image processing and feature extraction methods, specifically Local Binary Patterns (LBP) and Histogram of Oriented Gradients (HOG), combined with a Random Forest classifier to achieve this goal. The core of the project lies in extracting both texture and shape-based features from images to build an accurate classification model.

Source code: https://github.com/YassineIdiri/Parking-Space-Analysis

### 📄 Report

![park1](https://github.com/user-attachments/assets/77d61ccd-86ed-48c0-9e79-d9807ca450a0)

### ⚙️ Technologies Used

Python: The programming language used for implementing the entire project.
OpenCV: A computer vision library for image processing tasks such as reading, resizing, and converting images to grayscale.
scikit-image: A library that provides efficient implementations for image processing functions like Local Binary Patterns (LBP) and Histogram of Oriented Gradients (HOG).
NumPy: A fundamental package for numerical operations and handling arrays.
scikit-learn: A machine learning library used for classification, hyperparameter tuning (GridSearchCV), normalization, and evaluation metrics.
Pandas (if used for data handling): For organizing and managing labeled datasets.

### 🔎 Approach

Image Feature Extraction:

Local Binary Patterns (LBP): Extracts texture information by identifying local patterns in grayscale images. An LBP histogram is computed to represent texture-based features.
Histogram of Oriented Gradients (HOG): Extracts shape-based features by analyzing the gradients in different directions within an image.
Data Normalization: The features extracted using LBP and HOG are normalized using MinMaxScaler to bring all values within the range [0, 1].

Classification:

A Random Forest Classifier is used to classify the features into "occupied" or "free". The classifier’s hyperparameters are optimized using GridSearchCV to find the best settings for n_estimators, max_depth, and min_samples_split.
Model Evaluation:

The model is evaluated on test images using accuracy, precision, recall, F1-score, and a confusion matrix.

### 📈 Outcome 

The project successfully uses a combination of texture (LBP) and shape (HOG) features to classify parking spaces, achieving an accuracy of around 85% with an optimized Random Forest model. This approach is effective for scenarios where differentiating between occupied and free parking spaces is required based on image data.