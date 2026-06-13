# FinSight Risk Engine

## AI-Powered Corporate Bankruptcy Prediction and Financial Risk Assessment

FinSight Risk Engine is an end-to-end machine learning platform designed to identify financially distressed companies before bankruptcy occurs. The system analyzes financial statements and key accounting ratios to estimate bankruptcy probability, generate risk scores, and provide explainable insights into the factors driving financial risk.

Built using ensemble learning techniques, class imbalance handling, and Explainable AI (XAI), the platform helps transform complex financial indicators into actionable risk intelligence.

---

## Project Overview

Corporate bankruptcy prediction is a critical problem in finance, lending, investment management, and risk assessment. Traditional analysis often relies on manual review of financial statements, making large-scale risk evaluation challenging.

FinSight Risk Engine leverages machine learning models trained on real-world company financial data to:

* Predict bankruptcy probability
* Classify companies into risk categories
* Identify financial distress indicators
* Explain model decisions using SHAP
* Support data-driven financial risk assessment

---

## Dataset

**Source:** Company Bankruptcy Prediction Dataset (Taiwan Economic Journal)

### Dataset Statistics

* 6,819 Companies
* 95 Financial Indicators
* Binary Classification Problem
* Target Variable: Bankrupt / Non-Bankrupt

### Examples of Financial Indicators

* Return on Assets (ROA)
* Quick Ratio
* Debt Ratio
* Borrowing Dependency
* Net Income to Total Assets
* Retained Earnings to Total Assets
* Current Ratio
* Interest-Bearing Debt Metrics

---

## Technology Stack

### Machine Learning

* Scikit-Learn
* Random Forest Classifier
* XGBoost
* SMOTE (Synthetic Minority Oversampling)

### Data Analysis

* Pandas
* NumPy
* Matplotlib

### Explainable AI

* SHAP (SHapley Additive exPlanations)

### Model Persistence

* Joblib

---

## Project Architecture

```text
Financial Dataset
        │
        ▼
Data Cleaning & EDA
        │
        ▼
Feature Analysis
        │
        ▼
Train/Test Split
        │
        ▼
SMOTE Oversampling
        │
        ▼
Random Forest & XGBoost
        │
        ▼
Model Evaluation
        │
        ▼
SHAP Explainability
        │
        ▼
Risk Scoring Engine
        │
        ▼
Bankruptcy Risk Prediction
```

## Exploratory Data Analysis

The dataset exhibited significant class imbalance, with bankrupt companies representing only a small fraction of observations.

Key analyses performed:

* Class distribution analysis
* Correlation analysis
* Feature importance analysis
* Financial ratio exploration
* Bankruptcy trend visualization

---

## Models Evaluated

### Logistic Regression

Baseline classification model used for comparison.

### Random Forest Classifier

Ensemble tree-based model capable of handling nonlinear financial relationships.

### XGBoost Classifier

Gradient boosting framework evaluated for performance optimization and feature interactions.

---

## Handling Class Imbalance

Bankruptcy prediction datasets are naturally imbalanced because financially healthy companies significantly outnumber bankrupt firms.

To improve minority-class detection, SMOTE was implemented:

* Synthetic Minority Oversampling Technique (SMOTE)
* Balanced training dataset
* Improved recall for bankrupt companies

### Performance Improvement

| Metric               | Before SMOTE | After SMOTE                 |
| -------------------- | ------------ | --------------------------- |
| Bankruptcy Recall    | 57%          | 77%                         |
| Bankruptcy Precision | 41%          | 33%                         |
| ROC-AUC              | 0.944        | Maintained High Performance |

The improvement in recall enabled the model to identify substantially more financially distressed companies.

---

## Model Performance

### Random Forest

| Metric              | Score |
| ------------------- | ----- |
| ROC-AUC             | 0.944 |
| Accuracy            | 96%   |
| Bankruptcy Recall   | 57%   |
| Bankruptcy F1 Score | 0.48  |

### Random Forest + SMOTE

| Metric              | Score |
| ------------------- | ----- |
| Accuracy            | 94%   |
| Bankruptcy Recall   | 77%   |
| Bankruptcy F1 Score | 0.46  |

---

## Explainable AI (SHAP)

SHAP was used to understand how individual financial indicators influence bankruptcy predictions.

### Key Risk Drivers Identified

* Quick Ratio
* Total Debt / Total Net Worth
* Borrowing Dependency
* Interest-Bearing Debt Rate
* Persistent EPS
* Retained Earnings to Total Assets

This allows the model to provide interpretable and transparent financial risk assessments.

---

## Risk Scoring Engine

The prediction system generates both bankruptcy probability and risk category.

### Risk Categories

| Probability | Risk Level  |
| ----------- | ----------- |
| < 30%       | Low Risk    |
| 30–60%      | Medium Risk |
| > 60%       | High Risk   |

Example Output:

```python
{
    "Probability (%)": 78.4,
    "Risk Level": "High Risk"
}
```

---

## Business Impact

FinSight Risk Engine can support:

* Credit Risk Assessment
* Corporate Financial Analysis
* Lending Decisions
* Investment Screening
* Early Warning Systems
* Financial Due Diligence

---

## Future Improvements

* Streamlit Dashboard Deployment
* Real-Time Financial Data Integration
* Advanced Hyperparameter Optimization
* Ensemble Stacking Models
* Time-Series Financial Forecasting
* Cloud Deployment using AWS/GCP

---

## Results Summary

* Analyzed 6,819 companies using 95 financial indicators
* Achieved 0.94 ROC-AUC using ensemble learning
* Improved bankruptcy detection recall from 57% to 77%
* Implemented SHAP-based explainability
* Developed an interpretable risk scoring framework
* Built a complete end-to-end financial risk intelligence pipeline

---

## Author

Chinmay Kashyap

Machine Learning Engineer | Cloud Infrastructure | LLM & AI Applications

Focused on Applied Machine Learning, Financial AI, Explainable AI, and Scalable Intelligent Systems.
