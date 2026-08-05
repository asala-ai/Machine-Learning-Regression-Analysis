# Machine Learning Final Project

## Implementation and Performance Analysis of Linear Regression and Logistic Regression Models

This repository contains the implementation of a complete Machine Learning pipeline using:

- Linear Regression
- Logistic Regression

The models were implemented from scratch and compared with Scikit-learn implementations.

---

## Project Overview

This project applies Machine Learning techniques on hotel booking data to:

- Predict the **Average Daily Rate (ADR)** using Linear Regression.
- Predict **booking cancellation** using Logistic Regression.

---

## Pipeline

### 1. Data Preprocessing

The following preprocessing techniques were applied:

- Handling missing values
- Encoding categorical features
- Outlier detection and removal
- Feature normalization
- PCA dimensionality reduction

---

### 2. Model Implementation

Implemented models:

- Linear Regression using Gradient Descent
- Logistic Regression using mathematical optimization

---

### 3. Model Evaluation

#### Regression Metrics:

- RMSE
- MAE
- R² Score

#### Classification Metrics:

- Accuracy
- Precision
- Recall
- F1 Score

---

## Experiments

Three preprocessing scenarios were evaluated:

1. Baseline (Raw Data)
2. Normalization
3. Normalization + PCA

---

## Main Results

- Normalization significantly improved Logistic Regression performance.
- PCA reduced the number of features while preserving most variance, but slightly reduced performance.
- Custom implementations achieved results close to Scikit-learn models.

---

## Repository Structure

```
Repository Structure
Machine_Learning_Project/
│
├── README.md
├── Machine_Learning_Project.ipynb
│
└── Results/
    ├── ADR_before_outlier_removal.png
    ├── ADR_after_outlier_removal.png
    ├── regression_plot.png
    ├── linear_regression_results.png
    ├── logistic_regression_results.png
    ├── PCA_plot.png
    └── confusion_matrix.png
```


---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## Future Work

Possible improvements:

- Hyperparameter optimization
- Advanced models such as Random Forest and XGBoost
- Feature selection techniques
- Cross-validation
