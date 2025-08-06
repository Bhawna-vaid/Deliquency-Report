# Deliquency-Report
📊 Exploratory Data Analysis (EDA) Summary Report
1. Introduction
The purpose of this report is to explore and analyze customer financial behavior and identify risk indicators for delinquent accounts. The goal is to prepare clean, meaningful data for predictive modeling and business insights using EDA techniques.

2. Dataset Overview
This dataset consists of customer-level data including credit behavior, income, account tenure, and delinquency status.

Number of records: Approx. 1000 entries (as per your shared data)

Key variables:

Income: Annual income of the customer

Credit_Score: Creditworthiness score (300–850)

Loan_Balance: Total loan balance

Debt_to_Income_Ratio: Monthly debt to income ratio

Employment_Status: Employment category

Delinquent_Account: Target variable (1 = delinquent, 0 = not)

Data types:

Numerical: Income, Credit_Score, Loan_Balance, Debt_to_Income_Ratio, Age, Missed_Payments, Credit_Utilization, Account_Tenure

Categorical: Employment_Status, Credit_Card_Type, Location

Notes:

Some values in Employment_Status were inconsistent (EMP, employed, Employed) and were standardized.

No duplicate records or formatting errors were observed after cleaning.

3. Missing Data Analysis
Columns with missing values:

Income – 39 missing

Credit_Score – 2 missing

Loan_Balance – 29 missing

Treatment:

Income: Imputed using the median (robust against outliers)

Credit_Score: Imputed using the median

Loan_Balance: Imputed using the median

Justification:
Median imputation is industry standard when the data is skewed or contains outliers. It ensures stability without altering overall distribution.

4. Key Findings and Risk Indicators
Correlation Analysis:

Most variables showed very weak correlation with Delinquent_Account. All correlations were close to zero.

Example: Income (0.04), Credit_Score (0.03), Debt_to_Income_Ratio (0.03)

Categorical Insights:

Unemployed customers had the highest delinquency rate (19.4%)

Retired customers had the lowest delinquency rate (11.5%)

Boxplots showed slightly lower credit scores and income among delinquent customers

Anomalies:

Minor inconsistency in text casing (e.g., EMP, Employed, employed)

Some zero or very low income entries flagged as potential outliers

5. AI & GenAI Usage
Generative AI was used to:

Guide imputation strategy

Explain statistical charts like heatmaps, boxplots, and histograms

Summarize category-wise delinquency rates

Format report-ready text and visualization insights

Example AI prompts used:

“Suggest an imputation strategy for missing income values based on industry best practices.”

“Explain the boxplot showing Income vs. Delinquent_Account.”

“Summarize correlation heatmap results.”

6. Conclusion & Next Steps
The dataset is now cleaned and free of missing values

Most individual features don’t show strong correlation with delinquency, suggesting multi-feature interactions or non-linear relationships

Next steps:

Perform feature engineering (e.g., binning credit scores, combining features)

Train and evaluate classification models (Logistic Regression, Random Forest)

Evaluate feature importance from modeling

