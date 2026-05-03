# Customer Churn Prediction

A machine learning project that predicts whether a telecom customer 
will churn (leave) or stay, using the IBM Telco Customer Churn dataset.

---

## Project Overview

Customer churn is when a customer stops using a service. This project
builds a Random Forest classifier to identify at-risk customers before
they leave, helping businesses take proactive action.

---

## Dataset

**IBM Telco Customer Churn Dataset** — 7,043 customers with 21 features.

Download: [kaggle.com/datasets/blastchar/telco-customer-churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

### Column Descriptions:

| Column | Description |
|--------|-------------|
| customerID | Unique customer ID (dropped) |
| gender | Male or Female |
| SeniorCitizen | 1 if senior citizen, 0 if not |
| Partner | Whether customer has a partner |
| Dependents | Whether customer has dependents |
| tenure | Months with the company |
| PhoneService | Whether customer has phone service |
| MultipleLines | Whether customer has multiple lines |
| InternetService | DSL, Fiber optic, or No |
| OnlineSecurity | Whether customer has online security |
| OnlineBackup | Whether customer has online backup |
| DeviceProtection | Whether customer has device protection |
| TechSupport | Whether customer has tech support |
| StreamingTV | Whether customer streams TV |
| StreamingMovies | Whether customer streams movies |
| Contract | Month-to-month, One year, Two year |
| PaperlessBilling | Whether customer uses paperless billing |
| PaymentMethod | How customer pays |
| MonthlyCharges | Monthly amount charged |
| TotalCharges | Total amount charged |
| Churn | Target — Yes = churned, No = stayed |

---

## Data Cleaning

- **TotalCharges** — stored as string, converted to float
- **TotalCharges** — 11 missing values filled with `tenure × MonthlyCharges`
- **customerID** — dropped (irrelevant)

---

## Feature Engineering

- Binary columns encoded with Label Encoder (Yes/No → 1/0)
- Multi-value columns encoded with One Hot Encoding
- Prediction threshold lowered from 0.5 to 0.3 to improve churn detection

---

## Model

**Random Forest Classifier**
- 100 decision trees voting together
- Trained on 80% of data (5,634 rows)
- Tested on 20% of data (1,409 rows)

---

## 📊 Results

| Metric | Class 0 (Stay) | Class 1 (Churn) |
|--------|---------------|-----------------|
| Precision | 0.90 | 0.54 |
| Recall | 0.77 | 0.75 |
| F1 Score | 0.83 | 0.63 |
| Accuracy | 0.77 | — |

Churn recall improved from **47% to 75%** by lowering prediction threshold.

---

## Key Findings

1. **TotalCharges, tenure and MonthlyCharges** are the top 3 most important features
2. Dataset is imbalanced — 73% stayed, 27% churned
3. Lowering threshold from 0.5 → 0.3 significantly improved churn detection
4. Customers on month-to-month contracts are more likely to churn

---

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

## How to Run

1. Clone the repository
2. Download dataset from Kaggle and place CSV in project folder
3. Open `customer_churn.ipynb` in VS Code or Jupyter
4. Run all cells top to bottom

---

## Author

**Zaryab Zahid** — ML Engineer in progress

- GitHub: [github.com/Zaryab-Zahid](https://github.com/Zaryab-Zahid)
- Portfolio: [zaryab-zahid.github.io](https://zaryab-zahid.github.io)