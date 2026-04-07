# Imbalance Classification Methods & Mammography Detection

This repository explores various techniques for handling **imbalanced
datasets in machine learning**, specifically applied to **medical
imaging (Mammography)** and **classification performance evaluation**.

## 📂 Project Structure

### 1) Detect Mammography Microcalcifications.ipynb

A complete **end-to-end mammography classification notebook** for
detecting microcalcifications.

**Outputs included:** - Dataset shape and class distribution summaries -
Histograms of input variables - Pairwise scatter plots / feature
relationships - Mean ROC AUC evaluation - Multi-model comparison
results: - Logistic Regression - SVM - Bagging - Random Forest -
Gradient Boosting - Cost-sensitive model comparison - Prediction
examples for cancer vs non-cancer cases

------------------------------------------------------------------------

### 2) PR-CURVE and ROC-CURVE.ipynb

Focused on **classifier evaluation metrics for imbalanced medical
datasets**.

**Outputs included:** - ROC Curve plots - Precision-Recall Curve plots -
ROC AUC values - PR AUC values - No-skill vs Logistic Regression
comparisons - Predicted probability distribution plots -
Threshold-related numeric outputs

------------------------------------------------------------------------

### 3) Resampling(over_under_combine).ipynb

Comparison of **oversampling, undersampling, and combined resampling
methods**.

**Outputs included:** - Original class distribution - Random
oversampling results - Random undersampling results - Combined over +
under sampling results - F1-score comparison for each method

------------------------------------------------------------------------

### 4) SMOTE.ipynb

Detailed notebook covering **SMOTE and advanced synthetic sampling
techniques**.

**Outputs included:** - Original imbalanced class distribution - Scatter
plots before SMOTE - Scatter plots after SMOTE - SMOTE + undersampling
outputs - ROC AUC comparison before and after resampling - Grid search
over SMOTE `k` values - Borderline-SMOTE results - SVM-SMOTE results -
ADASYN results

------------------------------------------------------------------------

### 5) Threshold-Moving for Imbalanced Classification.ipynb

Notebook for **decision threshold optimization**.

**Outputs included:** - ROC curve plots - Precision-Recall curve plots -
Best ROC threshold - Best PR threshold - G-Mean optimization - F-score
optimization - Threshold search outputs

------------------------------------------------------------------------

### 6) Undersampling methods.ipynb

A notebook dedicated to **multiple undersampling strategies**.

**Outputs included:** - Original class distribution - NearMiss-1
results + scatter plots - NearMiss-2 results + scatter plots -
NearMiss-3 results + scatter plots - Condensed Nearest Neighbor
results + scatter plots

------------------------------------------------------------------------

## 🚀 Key Features & Methods

### Handling Imbalanced Data

-   **SMOTE**
-   **ADASYN**
-   **Oversampling**
-   **Undersampling**
-   **Threshold Moving**
-   **Combined Sampling**
-   **NearMiss methods**

### Performance Evaluation

-   ROC Curves
-   Precision-Recall Curves
-   Confusion Matrix analysis
-   ROC AUC / PR AUC
-   F1-score
-   Threshold optimization
-   Cost-sensitive learning

------------------------------------------------------------------------

## 📊 Sample Outputs

The notebooks include: - Class distribution visualization before and
after resampling - ROC / PR performance curves - Threshold comparison
plots - Mammography classification workflow outputs - Scatter plots for
resampling strategies - Prediction examples

------------------------------------------------------------------------

## 🛠️ Requirements

-   Python 3.x
-   Scikit-learn
-   imbalanced-learn (`imblearn`)
-   Pandas
-   Matplotlib
-   NumPy
-   Jupyter Notebook

------------------------------------------------------------------------

## 🎯 Application Domain

This project is especially useful for: - **Medical AI** - **Cancer
detection research** - **Imbalanced classification learning** -
**Machine learning education** - **Model evaluation for rare-event
datasets**
