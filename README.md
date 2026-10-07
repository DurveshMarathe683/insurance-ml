# Insurance ML

A machine learning project focused on understanding the factors that drive medical insurance costs and building predictive models capable of estimating individual insurance charges.

---

## Why This Project?

Medical insurance costs vary significantly from person to person. Factors such as age, lifestyle, smoking habits, family size, and overall health can dramatically impact the amount an individual pays.

This project explores how these variables influence insurance charges and aims to answer a simple question:

> Given a person's demographic and health information, can we accurately predict their medical insurance expenses?

Rather than jumping directly into model building, this project follows a structured machine learning workflow beginning with data exploration, feature engineering, and statistical analysis to ensure that the model is built on a solid foundation.

---

## Dataset Overview

The dataset contains information about insurance beneficiaries along with their corresponding medical charges.

### Features

- **Age** — Age of the policyholder
- **Sex** — Gender of the individual
- **BMI** — Body Mass Index
- **Children** — Number of dependents covered by insurance
- **Smoker** — Smoking status
- **Region** — Residential region within the United States
- **Charges** — Medical insurance costs *(Target Variable)*

---

## What Has Been Done So Far?

### Exploratory Data Analysis (EDA)

The project started with an in-depth exploration of the dataset to understand:

- Data distributions
- Feature relationships
- Outliers
- Duplicate records
- Correlation between variables

Visualizations used include:

- Histograms
- KDE Plots
- Boxplots
- Correlation Heatmaps
- Countplots

---

### Data Cleaning

To ensure data quality:

- Duplicate records were identified and removed
- Data types were verified
- Dataset consistency was validated

---

### Feature Engineering

To improve the predictive power of the dataset, additional features were created.

#### BMI Categories

Instead of using only raw BMI values, BMI was categorized into medically meaningful groups:

| Category | BMI Range |
|-----------|------------|
| Underweight | < 18.5 |
| Normal | 18.5 – 24.9 |
| Overweight | 25 – 29.9 |
| Obese | ≥ 30 |

These categories were later encoded into machine-learning-friendly features.

---

### Categorical Encoding

Several categorical variables were transformed into numerical representations.

Examples:

```python
male   -> 0
female -> 1

non-smoker -> 0
smoker     -> 1
```

One-hot encoding was applied where appropriate to avoid introducing artificial ordering among categories.

---

### Feature Scaling

Numerical features were standardized using:

```python
StandardScaler()
```

Features scaled:

- Age
- BMI
- Number of Children

This helps machine learning algorithms learn more effectively by ensuring all features operate on a comparable scale.

---

### Feature Selection & Statistical Analysis

Feature importance is currently being explored using:

- Pearson Correlation Analysis
- Chi-Square Tests
- Domain Knowledge

The goal is to identify which variables have the strongest influence on insurance charges before model training begins.

---

## Current Project Status

### Completed

- [x] Data Exploration
- [x] Data Cleaning
- [x] Feature Engineering
- [x] Feature Encoding
- [x] Feature Scaling
- [x] Correlation Analysis
- [x] Statistical Feature Evaluation

### Next Steps

- [ ] Train/Test Split
- [ ] Baseline Regression Models
- [ ] Model Comparison
- [ ] Hyperparameter Tuning
- [ ] Performance Evaluation
- [ ] Model Deployment

---

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-Learn
- Jupyter Notebook
- UV

---

## Project Structure

```text
insurance-ml/
│
├── data/
│   └── insurance.csv
│
├── notebooks/
│   └── insurance_analysis.ipynb
│
├── pyproject.toml
├── uv.lock
├── .gitignore
└── README.md
```

---

## What Comes Next?

The next phase of this project focuses on transforming the cleaned and engineered dataset into a production-ready machine learning pipeline.

Multiple regression models will be evaluated and compared to determine which approach provides the most accurate insurance charge predictions while maintaining interpretability.

The long-term goal is to expose the trained model through an API and build an end-to-end prediction system.

---

## Author

**Durvesh Marathe**

Building machine learning projects from the ground up — focusing not only on model training but also on data understanding, feature engineering, and production-ready workflows.
