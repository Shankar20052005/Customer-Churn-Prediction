# Project Results

## Dataset Summary

| Metric | Value |
|--------|------:|
| Dataset | IBM Telco Customer Churn |
| Total Customers | 7,043 |
| Features (Original) | 33 |
| Features (After Cleaning) | 25 |
| Churned Customers | 1,869 (26.5%) |
| Retained Customers | 5,174 (73.5%) |
| Train/Test Split | 80% / 20% |

---

# Exploratory Data Analysis (EDA)

## Key Findings

During the exploratory data analysis, several interesting patterns were observed:

- Around **26.5%** of customers had churned, while **73.5%** stayed with the company.
- Customers with **Month-to-Month contracts** were much more likely to churn than those with longer contracts.
- Customers with **lower tenure** tended to leave the company more often.
- Customers paying **higher monthly charges** showed a higher likelihood of churning.
- Customers using **Fiber Optic** internet services had a higher churn rate than DSL users.
- **Electronic Check** was the payment method most commonly associated with churn.
- Customers without **Online Security** or **Tech Support** services were more likely to discontinue their subscriptions.

These observations helped identify the factors that were most likely to influence customer churn and supported the machine learning analysis.

---

# Model Performance

Three machine learning models were trained and evaluated using the same train-test split.

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|-------|----------:|----------:|--------:|----------:|---------:|
| Logistic Regression | 79.13% | 61.98% | **55.35%** | **58.47%** | 84.03% |
| **Random Forest** | **79.56%** | **65.14%** | 49.47% | 56.23% | **84.15%** |
| XGBoost | 79.21% | 62.54% | 54.01% | 57.96% | 83.43% |

---

# Best Performing Model

Among the three models, **Random Forest** achieved the best overall performance.

### Performance

- Accuracy: **79.56%**
- Precision: **65.14%**
- Recall: **49.47%**
- F1 Score: **56.23%**
- ROC-AUC: **84.15%**

Although Logistic Regression achieved slightly better Recall and F1 Score, Random Forest produced the highest overall Accuracy, Precision, and ROC-AUC. Based on these results, Random Forest was selected as the final model for this project.

---

# Important Features

The feature importance analysis showed that the following variables had the greatest impact on predicting customer churn:

1. Tenure Months
2. Total Charges
3. Monthly Charges
4. CLTV
5. Contract Type (Month-to-Month)
6. Electronic Check Payment Method
7. Online Security
8. Fiber Optic Internet Service
9. Tech Support
10. Dependents

Most of these features were also identified during the exploratory data analysis, which indicates that the machine learning model is learning patterns that are consistent with the observed data.

---

# Business Recommendations

Based on the findings from this project, the following recommendations can help reduce customer churn:

- Encourage customers to move from **Month-to-Month** contracts to longer-term plans by offering discounts or loyalty benefits.
- Pay special attention to customers during their **first year**, as they are more likely to churn.
- Promote **Online Security** and **Tech Support** services, since customers without these services had higher churn rates.
- Review pricing strategies for customers with higher monthly charges.
- Improve the customer experience for **Fiber Optic** users.
- Use the trained machine learning model to identify customers who are at high risk of churning and target them with personalized retention campaigns.

---

# Project Deliverables

This project includes:

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Logistic Regression model
- Random Forest model
- XGBoost model
- Model evaluation and comparison
- Feature importance analysis
- Business recommendations
- Saved machine learning model (`models/churn_prediction_model.pkl`)

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Joblib
- Jupyter Notebook