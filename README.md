# Machine Learning Final Project

## Implementation and Performance Analysis of Linear Regression and Logistic Regression Models

### Course
Machine Learning (ML)

### Instructor
Dr. Thaer Sahmoud

### Student
Asala AbuGharara

---

## Project Overview

This project focuses on implementing and analyzing two fundamental Machine Learning algorithms:

- Linear Regression for continuous value prediction.
- Logistic Regression for binary classification.

Both models were implemented from scratch using NumPy and compared with Scikit-learn implementations to validate correctness and evaluate performance.

The project also studies the impact of different preprocessing techniques and dimensionality reduction using PCA on model performance.

---

# Dataset

The project uses the **Hotel Booking Dataset**.

Dataset Information:

- Number of records: 119,390
- Original features: 32 attributes
- Regression target:
  - `ADR` (Average Daily Rate)

- Classification target:
  - `is_canceled` (Booking cancellation status)

---

# Project Workflow

The complete Machine Learning pipeline includes:

1. Data Exploration
2. Data Preprocessing
3. Feature Engineering
4. Model Implementation
5. Model Evaluation
6. Comparison with Scikit-learn
7. Performance Analysis

---

# Data Preprocessing

The following preprocessing techniques were applied:

## Missing Data Handling

- Removed unsuitable columns with excessive missing values.
- Filled missing numerical values using statistical methods.
- Filled categorical missing values using the most frequent value.

## Data Leakage Removal

Columns containing information available only after booking completion were removed to prevent unrealistic model performance.

Removed features:

- `reservation_status`
- `reservation_status_date`

## Outlier Detection

The IQR method was used to detect and remove extreme values in the ADR target variable.

## Categorical Encoding

Categorical features were converted into numerical representations using:

- One-Hot Encoding

## Feature Scaling

Standardization was applied using:

- StandardScaler

## Dimensionality Reduction

Principal Component Analysis (PCA) was applied while preserving:

- 95% of the original variance

---

# Linear Regression

## Implementation

Linear Regression was implemented from scratch using NumPy.

The model estimates:

\[
\hat{y}=Xw+b
\]

where:

- X represents input features.
- w represents learned weights.
- b represents bias.

## Experiments

Three models were evaluated:

### Model A
Baseline Linear Regression

- No normalization
- No PCA

### Model B
Linear Regression with Normalization

- StandardScaler applied

### Model C
Linear Regression with Normalization + PCA

- StandardScaler
- PCA with 95% variance retention

---

# Logistic Regression

## Implementation

Logistic Regression was implemented from scratch using NumPy.

The model uses the sigmoid function:

\[
\sigma(z)=\frac{1}{1+e^{-z}}
\]

for binary classification.

## Experiments

Three models were evaluated:

### Model A

Baseline Logistic Regression

- No preprocessing

### Model B

Logistic Regression with Normalization

- StandardScaler applied

### Model C

Logistic Regression with Normalization + PCA

- StandardScaler
- PCA dimensionality reduction

---

# Evaluation Metrics

## Regression Metrics

The Linear Regression models were evaluated using:

- RMSE
- MAE
- R² Score


## Classification Metrics

The Logistic Regression models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score

---

# Results Summary

## Linear Regression Results

| Model | RMSE | R² Score |
|------|------|----------|
| Baseline | 26.0852 | 0.5906 |
| Normalization | 26.0852 | 0.5906 |
| Normalization + PCA | 30.7825 | 0.4299 |

Observation:

Normalization had little effect on Linear Regression, while PCA reduced performance because some useful information was removed.

---

## Logistic Regression Results

| Model | Accuracy | F1 Score |
|------|----------|----------|
| Baseline | 0.4086 | 0.5588 |
| Normalization | 0.8054 | 0.7041 |
| Normalization + PCA | 0.7908 | 0.6747 |

Observation:

Normalization significantly improved Logistic Regression performance, while PCA caused a small decrease due to information loss.

---

# Custom Model vs Scikit-learn

The implemented models were compared with Scikit-learn versions using the same preprocessing pipeline.

Results showed that:

- Custom Linear Regression achieved comparable results.
- Custom Logistic Regression produced similar performance trends.

This validates the correctness of the mathematical implementation.

---

# Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab
- Jupyter Notebook

---

# Project Structure
