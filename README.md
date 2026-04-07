# Imbalance Classification Methods & Mammography Detection

This repository explores various techniques for handling imbalanced datasets in machine learning, specifically applied to medical imaging data (Mammography) and classification performance metrics.

## 📂 Project Structure

* **Detect Mammography Microcalcifications.ipynb**: A complete end-to-end notebook for detecting microcalcifications using classification models.
* **PR-CURVE and ROC-CURVE.ipynb**: Evaluation of model performance using Precision-Recall and Receiver Operating Characteristic curves.
* **mammography.csv**: The dataset used for training and testing the models.
* **Powerpoints_Explanations/**: Detailed educational slides on:
    * Confusion Matrices
    * SMOTE (Synthetic Minority Over-sampling Technique)
    * Oversampling & Undersampling methods.

## 🚀 Key Features & Methods

### 1. Handling Imbalanced Data
The project demonstrates how to deal with datasets where the "Positive" class (e.g., cancer detection) is much rarer than the "Negative" class.
* **SMOTE**: Generating synthetic samples for the minority class.
* **Sampling**: Comparing random oversampling vs. undersampling.

### 2. Performance Evaluation
Since accuracy is misleading for imbalanced data, this project focuses on:
* **ROC Curves**: Plotting True Positive Rate vs. False Positive Rate.
* **Precision-Recall Curves**: More effective for highly imbalanced medical datasets.
* **Confusion Matrix**: Visualizing Type I and Type II errors.

## 📊 Sample Outputs
The notebooks include visualizations of:
* Class distribution before and after resampling.
* Comparison plots of model thresholds.
* Step-by-step logic for mammography feature extraction.

## 🛠️ Requirements
* Python 3.x
* Scikit-learn
* Imbalanced-learn (imblearn)
* Pandas / Matplotlib / Seaborn
