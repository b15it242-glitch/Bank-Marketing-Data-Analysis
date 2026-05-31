# Bank Marketing Data Analysis 🏦📊

## Project Overview
This repository contains an Exploratory Data Analysis (EDA) conducted on a bank marketing campaign dataset featuring **41,188 rows and 21 columns**. The objective of this project is to deeply inspect customer behavior patterns, evaluate campaign demographics, identify underlying data issues (like multicollinearity), and discover variables that drive term deposit subscriptions (`y`).

## Key Insights & Inspection Takeaways
Based on the data inspection and analysis pipelines executed within the notebook, here are the critical findings:

- **High-Quality Clean Data:** The dataset is exceptionally clean with **zero missing values** detected across all rows and attributes.
- **Target Class Imbalance:** There is a substantial class imbalance present in the target variable `y`. Approximately **88.7%** of targeted customers did not subscribe (`no`), which is an important factor to consider before building machine learning models.
- **Macro-Economic Interdependence:** Macro-economic features such as `euribor3m` (3-month Euribor interest rate), `emp.var.rate` (employment variation rate), and `nr.employed` (number of employees) exhibit extremely high correlations with one another. This indicates strong **multicollinearity** that must be addressed during feature selection.
- **The Call Duration Factor:** The feature `duration` (call duration in seconds) displays the strongest individual correlation with successful deposit outcomes. However, because this value is only known *after* a call ends, it represents a data leakage risk and should be excluded from predictive modeling workflows.
- **High-Conversion Demographics:** Looking into job categories, **retired individuals and students** show the highest percentage of subscription conversion rates compared to other professions.

## Tools & Libraries Used
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn

## Future Modeling Roadmap
The logical next steps outlined for this dataset include data preprocessing (one-hot encoding categorical features, re-mapping `pdays=999`), mitigating class imbalance, and training classification models such as **Logistic Regression, Random Forests, and XGBoost**.

> 📌 **Note on Dataset:** The dataset file `bankmarketing.csv` is excluded from this public directory to keep repository performance optimized. The full analytical exploration, data cleaning steps, and visualization configurations are entirely readable inside the attached Jupyter Notebook.
