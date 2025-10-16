# 💳 Credit Card Default Prediction: A Risk Modeling Case Study

🟣 Project Motivation

In an aggressive push to expand market share, a card-issuing bank over-distributed credit and cash cards — even to applicants with questionable repayment capacity. 
This led to widespread overuse, mounting debt, and a crisis of consumer finance confidence.
From a risk control perspective, estimating the probability of default is more meaningful than simply labeling customers as “risky” or “non-risky.”
This project aims to build a predictive model that helps banks identify potential defaulters early and intervene proactively.

📊 Dataset Overview

The dataset contains 30,000 customer records with 23 explanatory variables and one binary target:

Target Variable:
default payment next month (1 = Yes, 0 = No)
- Key Features:
- LIMIT_BAL: Credit limit (NT dollars)
- SEX, EDUCATION, MARRIAGE, AGE: Demographics
- PAY_0 to PAY_5: Past payment status (April–September 2005)
- BILL_AMT1 to BILL_AMT6: Monthly bill statements
- PAY_AMT1 to PAY_AMT6: Monthly payments

- Feature Scaling
- SMOTE for class balancing

⚙️ Modeling Workflow
Two datasets were created for comparison:
- d2: Raw data with outliers
- d3: Cleaned data with outliers removed
Each dataset was processed through the following pipeline:
Feature Engineering → Scaling → SMOTE → Train-Test Split → Modeling → Evaluation

🔍 Analytics Objectives
- Trend Analysis: Explore outstanding amounts across months
- Relationship Mapping: Link outstanding trends to age, education, marriage, and credit limit
- Behavioral Impact: Assess how outstanding trends influence default behavior
- Data Cleaning: Identify and correct errors or inconsistencies
- Statistical Profiling: Apply EDA to understand distributions and correlations
- Modeling: Build and compare ML models using:
- Logistic Regression
- Decision Tree Classifier
- Preprocessing:
- Feature Engineering (TOTAL_BILL_AMT)
- Feature Selection
- Label Encoding
- Feature Scaling
- SMOTE for class balancing

⚙️ Modeling Workflow
Two datasets were created for comparison:
- d2: Raw data with outliers
- d3: Cleaned data with outliers removed
Each dataset was processed through the following pipeline:
Feature Engineering → Scaling → SMOTE → Train-Test Split → Modeling → Evaluation

📊 Result Summary

This project compared the performance of Logistic Regression and Decision Tree classifiers on both datasets. SMOTE was applied to balance the classes, and models were evaluated based on their ability to detect defaulters (class 1) using recall, F1-score, and accuracy.
Model Performance:
- Logistic Regression on d2
- Recall: 0.85
- F1-score: 0.69
- Accuracy: 69%
- Decision Tree on d2
- Recall: 0.74
- F1-score: 0.68
- Accuracy: 69%
- Logistic Regression on d3
- Recall: 0.66
- F1-score: 0.61
- Accuracy: 58%
- Decision Tree on d3
- Recall: 0.77
- F1-score: 0.65
- Accuracy: 57%

🔑 Key Insights

- Logistic Regression on d2 with SMOTE achieved the highest recall and F1-score for defaulters.
- Removing outliers (d3) did not improve model performance — suggesting that some outliers may carry predictive signal.
- SMOTE significantly improved recall across all models, helping to address the imbalance between defaulters and non-defaulters.

✅ Recommendation

Proceed with Logistic Regression on d2 with SMOTE
This setup offers the best balance between interpretability and defaulter detection, making it suitable for stakeholder-facing credit risk modeling.


🙌 Gratitude

This project reflects my passion for data logic, model fairness, and stakeholder-ready storytelling.
Special thanks to mentors and peers who’ve supported this journey.
