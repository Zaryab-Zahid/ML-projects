# Heart Disease Prediction

A machine learning project that predicts whether a patient has heart disease.
Compares 5 different ML models, selects the best one, and tunes it using 
GridSearchCV for optimal performance.

---

## Project Overview

This project builds a complete ML pipeline for heart disease prediction:
- Tests 5 different models and compares their accuracy
- Selects the best performing model
- Tunes hyperparameters using GridSearchCV
- Evaluates using Cross Validation for reliable results

---

## Dataset

**Heart Disease UCI Dataset** — 920 patients with 16 features.

Download: [kaggle.com](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data)

### Column Descriptions:

| Column | Description |
|--------|-------------|
| age | Patient age in years |
| sex | Male or Female |
| cp | Chest pain type (4 types) |
| trestbps | Resting blood pressure (mm Hg) |
| chol | Serum cholesterol (mg/dl) |
| fbs | Fasting blood sugar > 120 mg/dl |
| restecg | Resting ECG results |
| thalch | Maximum heart rate achieved |
| exang | Exercise induced chest pain |
| oldpeak | ST depression during exercise |
| num | Target — 0 = no disease, 1 = has disease |

---

## Data Cleaning

- Dropped `id` and `dataset` — irrelevant columns
- Dropped `slope`, `ca`, `thal` — over 50% missing values
- Filled numerical columns with median: `trestbps`, `chol`, `thalch`, `oldpeak`
- Filled categorical columns with mode: `fbs`, `restecg`, `exang`
- Converted `num` from 0-4 scale to binary (0 = no disease, 1 = disease)

---

## Feature Engineering

- Label Encoding for binary columns: `sex`
- One Hot Encoding for multi-value columns: `cp`, `restecg`
- Bool columns converted to int: `fbs`, `exang`

---

## Model Comparison

| Model | Accuracy |
|-------|----------|
| Random Forest | **82.06%** |
| XGBoost | 81.52% |
| Logistic Regression | 80.97% |
| SVM | 71.19% |
| KNN | 69.02% |

---

## Hyperparameter Tuning

Used **GridSearchCV** with 5-fold cross validation to find optimal parameters:

| Parameter | Values Tried | Best Value |
|-----------|-------------|------------|
| n_estimators | 100, 200, 300 | 200 |
| max_depth | 3, 5, 10, None | 10 |
| min_samples_split | 2, 5, 10 | 10 |

- **Before tuning:** 82.06%
- **After tuning:** 82.60%

---

## 📊 Final Results

| Metric | Class 0 (No Disease) | Class 1 (Disease) |
|--------|---------------------|-------------------|
| Precision | 0.77 | 0.87 |
| Recall | 0.81 | 0.83 |
| F1 Score | 0.79 | 0.85 |
| Accuracy | 0.83 | — |

**Cross Validation Mean Accuracy: 76.6%**

---

## Key Findings

1. **Random Forest** outperformed all other models
2. Dataset is balanced — 55% disease, 45% no disease
3. GridSearchCV improved accuracy by 0.54%
4. High CV standard deviation (0.085) suggests more data needed for stability

---

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost

---

## How to Run

1. Clone the repository
2. Download dataset from Kaggle and place in project folder
3. Open `heart_disease.ipynb` in VS Code or Jupyter
4. Run all cells top to bottom

---

## Author

**Zaryab Zahid** — ML Engineer in progress

- 🌐 Portfolio: [zaryab-zahid.github.io](https://zaryab-zahid.github.io)
- 💻 GitHub: [github.com/Zaryab-Zahid](https://github.com/Zaryab-Zahid)
- 📧 Email: zaryabchess900@gmail.com