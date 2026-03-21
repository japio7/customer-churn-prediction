# 📉 Customer Churn Prediction
Predicting customer attrition to drive retention and revenue growth

___


## 🔍 Overview

Customer churn is a major challenge for subscription-based businesses. This project builds machine learning models to predict whether a telecommunications customer is likely to churn.

The analysis includes data preprocessing, model training, evaluation, and feature importance analysis to understand the key factors influencing churn.

## 🎯 What This Project Demonstrates

- End-to-end machine learning workflow  
- Business-driven model evaluation  
- Translation of model outputs into actionable strategy

---

## 📌 Key Results

🧠 Best Model: Random Forest 

| Metric     | Value |
|------------|------:|
| Accuracy   | 0.968 |
| Precision  | 0.976 |
| Recall     | 0.902 |
| F1 Score   | 0.937 |
| ROC-AUC    | 0.992 |

> **Why Recall Matters:** Missing a churned customer is more costly than a false positive, making recall a critical metric in this problem.

The model effectively identifies high-risk customers before churn occurs.

___

## 💰 Business Impact

This model enables:

- Targeted retention campaigns for high-risk customers  
- Reduction in churn-related revenue loss  
- More efficient marketing spend  
- Increased customer lifetime value (CLV)

Example:
In a base of 10,000 customers, identifying the top 10% highest-risk customers could enable targeted interventions that significantly reduce churn-related revenue loss.

## 🔮 Example Prediction

**Customer Profile:**
- Tenure: 2 months  
- Contract: Month-to-month  
- Monthly Charges: $90  

**Model Output:**
- Churn Probability: 78%

**Business Action:**
- Offer retention incentive  
- Promote contract upgrade  
- Trigger customer success outreach


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

These results show that customers with short-term commitments and higher costs are significantly more likely to churn, highlighting clear opportunities for targeted retention strategies.

---

## Model Deployment

The trained Random Forest model is saved using **Joblib**:

```python
joblib.dump(rf_clf, "churn_model.joblib")
```

This allows the model to be loaded later and used to generate churn predictions on new data.

This model can be integrated into a production system to score customers in real-time and trigger automated retention workflows.

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
