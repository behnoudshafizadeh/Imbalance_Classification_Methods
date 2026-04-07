# Imbalance Classification Methods & Mammography Detection

This repository presents a **practical and research-oriented study of
imbalanced classification methods** applied to **medical mammography
data** for microcalcification detection.

The main objective is to demonstrate **why standard classifiers fail on
rare-event datasets** and how advanced resampling and thresholding
methods can significantly improve performance.

------------------------------------------------------------------------

## 🎯 Why this project matters

Medical datasets are usually **highly imbalanced**, where
cancer-positive samples are rare.

A naïve classifier may achieve high accuracy while still **missing most
positive cancer cases**.

This project focuses on: - improving minority-class detection -
increasing ROC AUC and F1-score - optimizing decision thresholds -
comparing oversampling vs undersampling strategies - explaining the
reasoning behind each algorithm

------------------------------------------------------------------------

## 📂 Notebook Breakdown with Reasoning & Numerical Results

### 1) Detect Mammography Microcalcifications.ipynb

**Goal:** Build a complete mammography classification pipeline.

### Reasoning

This notebook establishes the **baseline performance** before applying
imbalance-learning techniques.

It helps answer:

> *How poorly can a standard model behave when the data is extremely
> imbalanced?*

### Outputs

-   dataset shape and class distribution
-   histograms and scatter plots
-   multiple classifier comparisons
-   prediction examples
-   cost-sensitive learning comparison

### Verified baseline result

-   **Baseline ROC AUC = 0.497**

This shows near-random classification performance, proving the need for
imbalance-aware methods.

------------------------------------------------------------------------

### 2) PR-CURVE and ROC-CURVE.ipynb

**Goal:** Explain why ROC and Precision-Recall curves are critical for
imbalanced medical data.

### Reasoning

Accuracy is misleading for rare-event detection.

This notebook demonstrates: - why ROC AUC is useful - why PR curves are
even better for rare positives - how threshold changes affect
performance

### Outputs

-   ROC curves
-   PR curves
-   no-skill vs logistic comparison
-   predicted probability distributions
-   threshold-related arrays

### Verified result

-   **Logistic ROC AUC = 0.903**
-   **Logistic PR AUC = 0.898**

This notebook mainly explains **evaluation reasoning**, not data
balancing.

------------------------------------------------------------------------

### 3) Resampling(over_under_combine).ipynb

**Goal:** Compare different data balancing strategies.

### Reasoning

This notebook answers:

> *Which resampling strategy improves minority-class learning the most?*

### Verified F1-score results

-   **Random Oversampling = 0.990**
-   **Random Undersampling = 0.945**
-   **Combined Sampling = 0.973**

### Improvement insight

Random oversampling performs best because it preserves all minority
samples while increasing class balance.

**Best gain over undersampling = +0.045 F1**

------------------------------------------------------------------------

### 4) SMOTE.ipynb

**Goal:** Use synthetic sample generation to improve classifier
learning.

### Reasoning

SMOTE generates **new synthetic minority examples**, allowing the
classifier to learn better decision boundaries instead of simply
duplicating samples.

This notebook also explores: - Borderline-SMOTE - SVM-SMOTE - ADASYN -
parameter tuning over `k`

### Verified ROC AUC improvement

-   **Original data = 0.759**
-   **After SMOTE = 0.830**
-   **SMOTE + undersampling = 0.840**

### Improvement

-   **SMOTE improvement = +0.071**
-   **Best total improvement = +0.081**

This notebook demonstrates the **strongest measurable improvement in the
repository**.

------------------------------------------------------------------------

### 5) Threshold-Moving for Imbalanced Classification.ipynb

**Goal:** Improve classification decisions without changing the data.

### Reasoning

Instead of balancing the dataset, this notebook changes the **decision
threshold** to maximize: - G-Mean - F-score - recall/precision trade-off

This is critical in medical AI where **false negatives are costly**.

### Verified threshold optimization

-   **Best ROC threshold = 0.016153**
-   **Best PR threshold = 0.256036**
-   **Best F-score = 0.756**

This notebook explains the reasoning behind **decision-level
optimization**.

------------------------------------------------------------------------

### 6) Undersampling methods.ipynb

**Goal:** Compare multiple undersampling algorithms.

### Reasoning

This notebook studies how removing majority-class examples changes the
decision boundary.

Algorithms compared: - NearMiss-1 - NearMiss-2 - NearMiss-3 - Condensed
Nearest Neighbor

### Outputs

-   class distributions
-   scatter plots for each method
-   geometric decision boundary intuition

This notebook is useful for understanding **how sample selection affects
model behavior**.

------------------------------------------------------------------------

## 📊 Key Verified Improvements

### Best measurable gains from the project

-   **ROC AUC:** `0.759 → 0.840` using SMOTE + undersampling
-   **F1-score:** up to `0.990` using random oversampling
-   **Threshold optimization:** best **F-score = 0.756**

------------------------------------------------------------------------

## 🛠️ Technologies

-   Python
-   Scikit-learn
-   imbalanced-learn
-   Pandas
-   NumPy
-   Matplotlib
-   Jupyter Notebook

