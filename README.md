# 📘 README — Credit Risk Analysis using Application Data

## 🔍 Overview

This project focuses on analyzing credit risk by exploring, cleaning, and visualizing customer application data. I used the datasets `application_data.csv` and `previous_application.csv` to identify patterns between customer profiles and their ability to repay loans (TARGET = 0) or default (TARGET = 1).

The goal was to understand the characteristics of reliable vs. risky clients and derive actionable insights for better credit policy.

---

## 📁 Files Used

- `application_data.csv`: Contains client-level data (demographics, credit info, etc.)
- `previous_application.csv`: Includes details of past loan applications for each client

---

## ⚙️ Step-by-Step Workflow

### 1. **Data Loading and Initial Exploration**
- Loaded both datasets using pandas
- Explored structure, shape, data types, and initial stats
- Checked for null values and calculated missing data percentage

### 2. **Data Cleaning**
- Dropped columns with over 30% missing values
- Dropped redundant or low-informative columns
- Handled null rows if necessary
- Replaced inconsistent categorical entries (e.g., `CODE_GENDER`)

### 3. **Feature Engineering**
- Created custom binned columns:
  - `AMT_INCOME_RANGE`
  - `AMT_CREDIT_RANGE`
  - `AGE_GROUP`
- Created new features:
  - `LOAN_TO_INCOME_RATIO`
  - `YEARS_EMPLOYED`
  - `EMPLOYMENT_BIN`
- Merged previous application data for extended context

### 4. **Univariate & Bivariate Analysis**
- Built a custom function `uniplot()` for plotting with seaborn
- Visualized distribution of key variables across both targets (0 & 1)
- Used boxplots to analyze bivariate relationships (e.g. income vs credit, age vs credit)

### 5. **Correlation Analysis**
- Used Spearman correlation to understand relationships between financial indicators and repayment behavior
- Created heatmaps for target-specific correlations

---

## 📌 Key Findings

1. **Client Profile with Better Repayment**:
   - Students, Pensioners, and Businessmen showed better repayment behavior.
   - Married and Female clients were more likely to repay loans.

2. **Riskier Segments**:
   - "Working" class had higher default rates despite being the majority.
   - Higher loan-to-income ratio correlates with increased risk.

3. **Organization Type**:
   - Distribution of organizations showed significant variance across targets.

---

## 🧠 Next Steps (Planned / Optional)
- Build predictive models (logistic regression, random forest)
- Handle class imbalance (SMOTE, balanced class weights)
- Feature selection and hyperparameter tuning
- Create an interactive dashboard for stakeholders

---

## 📦 Requirements

- Python (>=3.7)
- pandas, numpy
- matplotlib, seaborn
- jupyter notebook (optional)

