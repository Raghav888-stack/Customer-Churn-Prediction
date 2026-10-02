# Customer-Churn-Prediction
Machine learning project for predicting telecom customer churn using data preprocessing, exploratory analysis, Logistic Regression, and Random Forest.


## 1. Project Overview

Customer churn is a major business problem for subscription-based companies because losing existing customers can directly affect recurring revenue.

This project uses historical telecom customer data to identify customers who are likely to churn. The objective is to build a classification model that can distinguish between customers who are likely to leave and those who are likely to remain, while also analyzing the customer characteristics associated with churn.

---

## 2. Problem Statement

The objective is to predict whether a telecom customer will churn based on demographic, account, and service-related attributes.

The project focuses on two aspects:

1. Building machine learning models for churn classification.
2. Identifying customer-level patterns associated with higher churn risk.

---

## 3. Dataset

The project uses the **Telco Customer Churn Dataset** from Kaggle.

The dataset contains information related to:

- Customer demographics
- Account information
- Service usage
- Contract characteristics
- Monthly and total charges
- Customer churn status

The target variable is `Churn`, which indicates whether a customer has left the service.

---

## 4. Data Preprocessing

The following preprocessing steps were performed:

- Converted `TotalCharges` to a numeric format.
- Handled missing values.
- Removed `customerID`, as it is an identifier rather than a predictive feature.
- Encoded categorical variables for machine learning.
- Applied feature scaling using `StandardScaler`.

---

## 5. Exploratory Data Analysis

Exploratory analysis was performed to understand the relationship between customer characteristics and churn.

The analysis included:

- Distribution of churn across customers.
- Relationship between `MonthlyCharges` and churn.
- Relationship between customer `tenure` and churn.
- Analysis of customer contract characteristics.
- Visualization of relevant feature distributions.

The analysis indicated that customers with shorter tenure and higher monthly charges showed greater churn tendency, while contract type was also associated with customer retention.

---

## 6. Machine Learning Approach

Two classification models were implemented:

### Logistic Regression

Logistic Regression was used as a baseline classification model for predicting the probability of customer churn.

### Random Forest Classifier

A Random Forest classifier was used as a tree-based model to capture potentially non-linear relationships between customer characteristics and churn.

---

## 7. Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Because churn prediction involves identifying customers who are actually going to leave, recall for the churn class is particularly relevant.

### Results

| Model | Accuracy |
|---|---:|
| Logistic Regression | 81.5% |
| Random Forest | 79.4% |

The churn-class recall was approximately **48%**, indicating that although the models achieved reasonable overall accuracy, a substantial proportion of actual churn cases were not identified.

---

## 8. Key Findings

The analysis produced the following observations:

- Customers with higher monthly charges showed greater churn tendency.
- Customers with lower tenure showed greater churn tendency.
- Contract type had a significant relationship with customer retention.
- The models achieved reasonable overall classification accuracy.
- Churn-class recall remained comparatively lower, indicating scope for improving identification of at-risk customers.

---

## 9. Limitations

The current implementation has limitations:

- Churn-class recall is relatively low.
- The models were evaluated using a limited set of baseline algorithms.
- Class imbalance was not specifically addressed in the current implementation.
- Hyperparameter optimization was not extensively explored.

Therefore, the current models should be considered a baseline rather than a production-ready churn prediction system.

---

## 10. Possible Improvements

Future iterations could explore:

- SMOTE or other class-balancing techniques.
- Hyperparameter tuning.
- Gradient Boosting or XGBoost-based models.
- Feature selection and additional feature engineering.
- Threshold optimization to improve churn recall.
- Deployment as an interactive application.

---

## 11. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 12. Project Structure

```text
Customer-Churn-Prediction/
│
├── churn_analysis.ipynb
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
└── README.md
