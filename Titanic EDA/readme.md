# Titanic EDA — Exploratory Data Analysis

A complete exploratory data analysis of the Titanic dataset. 
The goal of this project was to practice EDA skills — asking 
meaningful questions about data, cleaning it, and answering 
those questions with visualizations.

---

## Project Overview

This project explores the Titanic passenger dataset to uncover
patterns and insights about who survived and why. No ML model
is used — this is purely data exploration and visualization.

---

## Dataset

**Titanic Dataset** — 891 passengers with 12 features.

Download: [kaggle.com/datasets/yasserh/titanic-dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)

### Column Descriptions:

| Column | Description |
|--------|-------------|
| PassengerId | Unique ID for each passenger |
| Survived | 0 = Died, 1 = Survived (target variable) |
| Pclass | Passenger class — 1st, 2nd, or 3rd |
| Name | Full name of passenger |
| Sex | Gender of passenger |
| Age | Age of passenger |
| SibSp | Number of siblings/spouses aboard |
| Parch | Number of parents/children aboard |
| Ticket | Ticket number |
| Fare | Amount paid for ticket |
| Cabin | Cabin number (mostly missing) |
| Embarked | Port of embarkation — S=Southampton, C=Cherbourg, Q=Queenstown |

---

## Data Cleaning

- **Age** — 177 missing values filled with median age grouped by Pclass
- **Cabin** — 687 missing values (77% empty) — column dropped entirely
- **Embarked** — 2 missing values filled with mode (Southampton)

---

## Questions Explored

### 1. How does fare vary by passenger class?
- 1st class paid ~84 on average
- 2nd class paid ~21 on average
- 3rd class paid ~14 on average
- 1st class paid 6x more than 3rd class

### 2. Did passenger class affect survival?
- 1st class — 63% survival rate
- 2nd class — 47% survival rate
- 3rd class — 25% survival rate
- Higher class = significantly better chance of survival

### 3. Did gender affect survival?
- Female — 74% survival rate
- Male — 19% survival rate
- Women were 4x more likely to survive than men
- Confirms the "women and children first" policy

### 4. Did age affect survival?
- Children aged 0-10 had higher survival rates
- Passengers aged 20-30 had the highest death count
- Older passengers had lower survival rates overall

---

## Visualizations

- Average Fare by Passenger Class
- Survival Rate by Passenger Class
- Survival Rate by Gender
- Age Distribution — Survived vs Died

---

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib

---

## Key Findings

1. **Class mattered** — 1st class passengers were 2.5x more likely to survive than 3rd class
2. **Gender mattered most** — women had a 74% survival rate vs 19% for men
3. **Children were prioritized** — passengers under 10 had noticeably higher survival
4. **Wealth = survival** — higher fare directly correlated with higher survival rate

---

## Author

**Zaryab Zahid** — ML Engineer in progress

- GitHub: [github.com/Zaryab-Zahid](https://github.com/Zaryab-Zahid)
- Portfolio: [zaryab-zahid.github.io](https://zaryab-zahid.github.io)