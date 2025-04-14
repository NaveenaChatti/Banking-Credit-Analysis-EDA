# 📘 Credit Risk Analysis – Project Summary

## 🔍 Overview

In this project, I analyzed customer loan application data to predict credit risk. The objective was to identify which applicants were more likely to repay their loans (TARGET = 0) and which ones might default (TARGET = 1). This analysis helps provide insights into improving lending strategies and credit scoring.

---

## 📊 Data Used

- **application_data.csv** (307511, 122): Contains information about applicants (income, employment status, family details, etc.)
  
---

## 🧪 Techniques & Analysis

1. **Data Cleaning:**  
   I handled missing values by dropping columns with too many missing entries (over 30%) and removing rows with critical missing data. Unnecessary features were removed to simplify the dataset.

2. **Feature Engineering:**  
   I created new features like `LOAN_TO_INCOME_RATIO`, `YEARS_EMPLOYED`, and binned continuous variables like income, age, and credit amount into categories. This step made it easier to visualize trends and relationships between the variables.

3. **Correlation Analysis:**  
   Spearman's correlation was used to explore non-linear relationships between variables. It’s particularly useful when the data is skewed or when we expect ranked relationships (e.g., higher income correlates with higher credit amounts).

4. **Data Visualization:**  
   I built custom plots to explore the distributions of key features like income, age, and family status. This included univariate and bivariate analysis (e.g., how family status impacts credit amount or how income ranges differ by target class).

5. **Identifying Trends & Patterns:**  
   By comparing the characteristics of applicants who repay loans vs. those who default, I identified key insights — like which segments are safer to lend to, and which ones might be riskier.

---

## 🔑 Key Insights

- **Safer Segments:**  
   Students, pensioners, and businessmen show better repayment behavior. Female and married applicants tend to repay loans more reliably.
  
- **Riskier Profiles:**  
   Applicants in the "Working" category had more defaults, even though they made up the majority of the dataset. Higher `loan-to-income` ratios were also more common among defaulters.

- **Previous Applications Matter:**  
   People with fewer past loan applications generally had better repayment behavior, suggesting that repeated loan applications might indicate financial distress.

---

## 🧰 Tools & Libraries Used

- **Programming Language:** Python (for data manipulation and analysis)
- **Data Handling:** pandas, numpy
- **Visualization:** matplotlib, seaborn
- **Environment:** Jupyter Notebook (for exploration and visualization)

---

