# Customer Churn Prediction

## Overview

Customer churn is a major challenge for subscription-based businesses. This project builds machine learning models to predict whether a telecommunications customer is likely to churn.

The analysis includes data preprocessing, model training, evaluation, and feature importance analysis to understand the key factors influencing churn.

---

## Dataset

Dataset Source: HuggingFace
`aai510-group1/telco-customer-churn`

The dataset contains customer demographic information, account details, and service usage metrics.

Examples of variables include:

* Contract Type
* Internet Type
* Payment Method
* Monthly Charges
* Tenure
* Customer Lifetime Value (CLTV)

Target variable:

**Churn**

* `0` = Customer stays
* `1` = Customer churns

---

## Data Preprocessing

The following preprocessing steps were applied:

1. Removed variables not useful for modeling

   * Customer ID
   * Geographic information
   * Churn explanation fields

2. Converted categorical variables using **one-hot encoding**

3. Split the dataset into **training and testing sets (80/20)**

---

## Machine Learning Models

Three classification algorithms were evaluated:

### Random Forest

An ensemble model that combines multiple decision trees to improve prediction accuracy.

### Logistic Regression

A statistical classification model commonly used for binary prediction problems.

### Bernoulli Naive Bayes

A probabilistic classifier based on Bayes’ theorem.

---

## Model Evaluation

Models were evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC Curve
* Area Under the Curve (AUC)

### ROC Curve

The ROC curve measures how well the model distinguishes between churn and non-churn customers.

### Confusion Matrix

The confusion matrix shows how many churn predictions were correct vs incorrect.

---

## Feature Importance

Feature importance analysis was performed using the Random Forest model.

The most important predictors of churn include:

* Contract Type
* Monthly Charges
* Tenure
* Internet Type
* Payment Method

These variables provide insight into customer behavior and churn risk.

---

## Model Deployment

The trained Random Forest model is saved using **Joblib**:

```python
joblib.dump(rf_clf, "churn_model.joblib")
```

This allows the model to be loaded later and used to generate churn predictions on new data.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* HuggingFace Datasets
* Joblib
* Jupyter Notebook

---

## Project Structure

```
customer-churn-prediction/
│
├── README.md
├── Customer Churn Prediction Report.pdf
│
├── notebooks/
│   ├── 01_model_training.ipynb
│   └── 02_predict_churn.ipynb
│
├── models/
│   └── churn_model.joblib
│
├── data/
│   └── churn.csv
│
└── images/
    ├── comparison.png
    ├── roc_curve.png
    ├── confusion_matrix.png
    └── feature_importance.png
```

---

## Author

Jared Pino
Master of Science – Data Science

GitHub
https://github.com/japio7
