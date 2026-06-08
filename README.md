# -internSpark-Intership-project-2-
loan approval prediction
# Loan Approval Prediction

## Overview

This project focuses on building a machine learning model to predict whether a loan application will be approved based on applicant financial and demographic information. The objective is to assist financial institutions in making faster, more consistent, and data-driven lending decisions.

The project covers the complete data science workflow, including data exploration, preprocessing, handling class imbalance, model training, evaluation, and business interpretation of results.

---

## Dataset

**Dataset Name:** Loan Approval Prediction Case Study

**Source:** Kaggle

Dataset Link: https://www.kaggle.com/datasets/bhanupratapbiswas/loan-approval-prediction-case-study

### Dataset Description

The dataset contains information about loan applicants, including:

* Annual Income
* Loan Amount
* Loan Term
* CIBIL Score
* Residential Assets Value
* Commercial Assets Value
* Luxury Assets Value
* Bank Asset Value
* Education Status
* Employment Status
* Loan Approval Status (Target Variable)

The target variable indicates whether a loan application was approved or rejected.

---

## Project Objectives

* Perform Exploratory Data Analysis (EDA) to understand the dataset.
* Clean and preprocess the data.
* Handle missing values and categorical variables.
* Address class imbalance using resampling techniques.
* Build and compare multiple machine learning models.
* Evaluate model performance using industry-standard metrics.
* Interpret model outputs from a business perspective.
* Recommend a deployment threshold for loan approval decisions.

---

## Technologies Used

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn (SMOTE)
* Jupyter Notebook / Google Colab

---

## Exploratory Data Analysis

The following analyses were performed:

### Data Quality Checks

* Missing value analysis
* Data type inspection
* Summary statistics
* Duplicate record detection

### Visualizations

1. Loan Approval Distribution
2. Annual Income vs Loan Status
3. CIBIL Score Distribution
4. Correlation Heatmap

### Initial Observations

* Loan approval is strongly influenced by financial indicators.
* Applicants with higher CIBIL scores generally have higher approval rates.
* Income and asset ownership show positive relationships with approval likelihood.
* Some imbalance exists in the target classes, requiring special handling during model training.

---

## Data Preprocessing

### Missing Value Treatment

* Numerical features filled using median values.
* Categorical features filled using mode values.

### Encoding

Categorical variables were converted into numerical representations using:

* Label Encoding
* One-Hot Encoding (where applicable)

### Feature Scaling

Numerical features were standardized using StandardScaler to improve model performance.

---

## Handling Class Imbalance

To improve prediction performance on minority classes, imbalance handling techniques were explored:

* SMOTE (Synthetic Minority Oversampling Technique)
* Class Weights
* Random Undersampling

SMOTE was selected as the primary approach for balancing the training data.

---

## Machine Learning Models

The following models were trained and compared:

### Logistic Regression

A baseline linear model that provides high interpretability and fast training.

### Decision Tree

A rule-based model capable of capturing non-linear relationships.

### Random Forest

An ensemble learning method that combines multiple decision trees to improve accuracy and reduce overfitting.

---

## Evaluation Metrics

Models were evaluated using:

* Precision
* Recall
* F1-Score
* Confusion Matrix
* ROC-AUC Score

### Model Comparison

               Model  Precision  Recall  F1-Score  ROC-AUC
0  Logistic Regression      0.845   0.835     0.840    0.841
1        Decision Tree      0.838   0.729     0.780    0.707
2        Random Forest      0.852   0.882     0.867    0.811



---

## Feature Importance Analysis

Feature importance was analyzed to identify the most influential factors affecting loan approval decisions.

Typical high-impact features include:

* CIBIL Score
* Annual Income
* Loan Amount
* Residential Asset Value
* Commercial Asset Value

Understanding these factors helps stakeholders make informed lending decisions.

---

## Business Insights

Key findings from the analysis include:

* Higher credit scores significantly increase approval probability.
* Applicants with stronger financial backgrounds are more likely to receive loan approval.
* Large loan requests relative to income may increase rejection risk.
* Asset ownership provides additional confidence in applicant creditworthiness.

The model can serve as a decision-support tool for loan officers by identifying high-risk and low-risk applicants efficiently.

---

## Deployment Recommendation

A probability threshold must be selected based on business objectives.

* Threshold = 0.50 → Balanced Precision and Recall
* Threshold = 0.60–0.70 → Conservative lending strategy with lower risk
* Threshold = 0.40 → Aggressive lending strategy with higher approval rates

For most banking scenarios, a threshold between 0.60 and 0.70 is recommended to minimize risky loan approvals.

---

## Project Structure

```text
Loan-Approval-Prediction/
│
├── data/
│   └── loan_approval_dataset.csv
│
├── notebooks/
│   └── loan_approval_prediction.ipynb
│
├── images/
│   └── visualizations/
│
├── reports/
│   └── project_report.pdf
│
├── README.md
│
└── requirements.txt
```

---

## Conclusion

This project demonstrates an end-to-end machine learning pipeline for loan approval prediction. Through data preprocessing, exploratory analysis, imbalance handling, model training, and evaluation, the project provides valuable insights into lending decisions and showcases practical data science skills applicable to real-world financial applications.

