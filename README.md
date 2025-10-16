# 💳 Credit Card Default Prediction: A Risk Modeling Case Study

## 🟣 Project Motivation

In an aggressive push to expand market share, a card-issuing bank over-distributed credit and cash cards — even to applicants with questionable repayment capacity. This led to widespread overuse, mounting debt, and a crisis of consumer finance confidence.

From a risk control perspective, **estimating the probability of default** is more meaningful than simply labeling customers as “risky” or “non-risky.” This project aims to build a predictive model that helps banks identify potential defaulters early and intervene proactively.

## 📊 Dataset Overview

The dataset contains **30,000 customer records** with 23 explanatory variables and one binary target:

- **Target Variable**:  
  `default payment next month` (1 = Yes, 0 = No)

- **Key Features**:
  - `LIMIT_BAL`: Credit limit (NT dollars)
  - `SEX`, `EDUCATION`, `MARRIAGE`, `AGE`: Demographics
  - `PAY_0` to `PAY_5`: Past payment status (April–September 2005)
  - `BILL_AMT1` to `BILL_AMT6`: Monthly bill statements
  - `PAY_AMT1` to `PAY_AMT6`: Monthly payments

## 🔍 Analytics Objectives

1. **Trend Analysis**: Explore outstanding amounts across months
2. **Relationship Mapping**: Link outstanding trends to age, education, marriage, and credit limit
3. **Behavioral Impact**: Assess how outstanding trends influence default behavior
4. **Data Cleaning**: Identify and correct errors or inconsistencies
5. **Statistical Profiling**: Apply EDA to understand distributions and correlations
6. **Modeling**: Build and compare ML models using:
   - Logistic Regression
   - Decision Tree Classifier
7. **Preprocessing**:
   - Feature Engineering (`TOTAL_BILL_AMT`)
   - Feature Selection
   - Label Encoding
   - Feature Scaling
   - SMOTE for class balancing

## ⚙️ Modeling Workflow

Two datasets were created for comparison:

- **`d2`**: Raw data with outliers
- **`d3`**: Cleaned data with outliers removed

Each dataset was processed through the following pipeline:

```text
Feature Engineering → Scaling → SMOTE → Train-Test Split → Modeling → Evaluation

<img width="912" height="396" alt="image" src="https://github.com/user-attachments/assets/38e7db7c-9069-4f62-8c16-33f72889ed2b" />

Recommendation
Logistic Regression on d2 with SMOTE is the most effective setup.
It balances interpretability with high recall, making it ideal for early defaulter detection in credit risk scenarios.

📁 Repository Structure
├── data/
│   ├── d2.csv
│   └── d3.csv
├── notebooks/
│   ├── smote_modeling_d2.ipynb
│   └── smote_modeling_d3.ipynb
├── results/
│   └── classification_reports/
├── README.md

🙌 Gratitude
This project reflects my passion for data logic, model fairness, and stakeholder-ready storytelling. Special thanks to mentors and peers who’ve supported this journey.
