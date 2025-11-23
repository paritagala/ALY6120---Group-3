Northeastern University

ALY6120: Leadership in Analytics

Module 3 Assignment (Group 3)

CRISP-DM Cycle: Data Preparation

Student Names: Parita Gala, Josephine Agbedoawu, Jiansheng Shentu, Godfred Akoto

Professor: Abeba N. Turi

Date: November 23, 2025

Data Preparation and Quality Assessment

In this assignment, before the data would be passed on for further modelling, we would employ several preparation steps to ensure that there is data quality, reliability, and suitability for the predictive modelling, considering that the focus for the analysis here is attrition.

First, missing data would be identified and quantified across all variables. Although there might be a few Nas in the dataset, any gaps in fields such as education, job role, or income would require attention. Missing values in numerical variables may be imputed using simple approaches like mean or median, or flagged for review, while missing categorical values may need mode imputation or a dedicated unknown category. Rows with excessive missingness might be removed after several deliberations from the group.

Next, the data would be checked for incorrect values, for example negative ages, unrealistic total working years, duplicated employee IDs, or inconsistent combinations such as “Years at Company” greater than “Total Working Years.” Categorical variables would also require validation to ensure labels are properly formatted and standardized.
Outlier detection is essential for numerical fields such as monthly income, years of experience, distance from home, or daily rate. The outliers that would be identified may indicate data entry errors or genuinely extreme cases which would be evaluated and either corrected or removed depending on context.

The final step would be to ensure correct data types and documenting all cleaning decisions be to ensure transparency for the modelling team.
