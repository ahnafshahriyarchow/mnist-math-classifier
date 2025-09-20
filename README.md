# MNIST Math Classifier

This project implements and compares **three machine learning classifiers** — **Support Vector Machine (SVM)**, **Random Forest**, and **K-Nearest Neighbors (KNN)** — for recognizing handwritten digits from the **MNIST dataset**.  
It demonstrates a full ML workflow: data loading, preprocessing, training, evaluation, and prediction visualization.


## Overview
The goal of this project is to build and compare machine learning models to classify handwritten digits (0–9) from the MNIST dataset.  
It evaluates model performance on **accuracy**, **precision**, **recall**, and **F1-score**, allowing a clear comparison of algorithms.

---

## Features
- **Data Preprocessing**:
  - Image reshaping and normalization (pixel values scaled to 0–1)
  - Standard scaling for improved model convergence
- **Multiple Classifier Implementation**:
  - Support Vector Machine (SVM)
  - Random Forest
  - K-Nearest Neighbors (KNN)
- **Model Evaluation**:
  - Accuracy, precision, recall, F1-score
  - Training vs validation accuracy
  - Classification reports
- **Prediction Visualization**:
  - Displays predicted labels on test samples

---

## Dataset
- **MNIST Dataset** (built-in from `tensorflow.keras.datasets`):
  - 60,000 training images
  - 10,000 test images
  - Each image is a 28×28 grayscale handwritten digit
- Automatically downloaded by the script (no manual setup required).

---

## Preprocessing
1. **Reshaping** images into 1D vectors of 784 pixels.  
2. **Normalization** of pixel values to the range [0,1].  
3. **Splitting** training data into training and validation sets (80/20).  
4. **Standardization** with `StandardScaler` for improved model performance.

---

## Models Implemented
| Model            | Key Parameters                     |
|-----------------|------------------------------------|
| **SVM**          | `C=0.1`, `kernel='rbf'`            |
| **Random Forest**| `n_estimators=50`, `max_depth=10`  |
| **KNN**          | `n_neighbors=7`                   |

---

## Results
Validation accuracy achieved by each model:

| Model          | Accuracy | Precision | Recall | F1-Score |
|----------------|----------|-----------|--------|----------|
| **SVM**        | ~0.929   | ~0.932    | ~0.929 | ~0.930   |
| **Random Forest**| ~0.943 | ~0.943    | ~0.943 | ~0.943   |
| **KNN**        | ~0.943   | ~0.943    | ~0.943 | ~0.943   |

- **Training Accuracy vs Validation Accuracy**:
  - SVM: 0.936 / 0.929  
  - Random Forest: 0.966 / 0.944  
  - KNN: 0.957 / 0.943  

 **Random Forest and KNN performed slightly better than SVM** on validation data.

---


