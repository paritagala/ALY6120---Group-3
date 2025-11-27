### Northeastern University, Vancouver

### Course: ALY6120 - Leadership in Analytics 

### Module 4 Assignment (Group 3)

### CRISP-DM Cycle: Data Preparation

### Title: Employee Attrition Prediction Analysis

### Student Names: Parita Gala, Josephine Agbedoawu, Jiansheng Shentu, Godfred Akoto

### Professor: Abeba N. Turi

### Date: November 23, 2025


### Identify Your Data Sources

For this project, the primary dataset is the IBM HR Analytics Employee Attrition & Performance dataset. This dataset includes:
Employee Demographics: Age, gender, marital status, education, education field.

Job & Organizational Variables: Job role, department, job level, job satisfaction, environment satisfaction, work-life balance.
Compensation & Benefits: Monthly income, hourly rate, stock option level, percent salary hike.
Performance & Engagement: Performance rating, relationship satisfaction, training times last year.
Workplace Behavior: Distance from home, overtime status, total working years, job involvement.
Attrition Labels: Whether the employee left the company (Yes/No).

### Determine Whether They Can Be Acquired Internally or Externally

Internal Acquisition:
In a real corporate setting, HR departments would acquire this type of data internally from HRIS, payroll, performance management systems, and employee engagement systems. All the variables present in the IBM dataset map directly to internal company systems.

External Acquisition:
For academic or training purposes, the IBM HR Analytics Attrition dataset is publicly available externally (e.g., via Kaggle).
Therefore, while the dataset represents internal HR data, it is accessed externally for this project.

### How The Data Will Be Acquired 
We will obtain the IBM HR Analytics Employee Attrition & Performance dataset from Kaggle, a reliable source for publicly accessible datasets utilized in both academic and professional analytics.

Acquisition and Validity : We will go to Kaggle's official IBM HR Analytics repository, obtain the CSV file, and confirm that it includes the necessary variables (Age, Attrition, Job Satisfaction, Monthly Income, Years at Company, Work-Life Balance, etc.) without any corruption or missing information.

Protected Storage : The dataset would be stored in a well-organized project directory with distinct naming rules (e.g., IBM_HR_Analytics_Raw_2025-11-22.csv), keeping the original file distinct from its processed copies to guarantee reproducibility.
Load into Tools: We would bring the data into Python using pandas (pd.read_csv()) for analysis and cleaning, or into Power BI through the "Get Data" connector for visualization. Depending on the modelling needs, we may also use R or Jupyter notebooks.

Document Source: We would maintain a README file documenting the source (Kaggle), download date, original creators (IBM Watson Analytics), and any preprocessing steps applied.
Since this is a synthetic dataset created for educational purposes, it contains no real employee information, eliminating privacy concerns while providing a realistic HR analytics practice.

### Team Members We Will Collaborate With 
An HR Business partner or HR Analyst will provide domain expertise on workforce metrics and organizational practices. They would validate my interpretation of variables like Job Satisfaction and Work Life Balance, explain what constitutes concerning attrition rates, and help translate analytical findings into actionable retention strategies HR leadership can implement.

A Data Scientist or Analytics Manager oversees methodology and technical approach. They would review our feature selection for the attrition prediction model, recommend appropriate algorithms (logistic regression, decision trees, random forest), validate model performance interpretation, and ensure we follow best practices while avoiding pitfalls like overfitting.

IT/Database Professional (for real organizational data) manages data access, quality, and security. While unnecessary for this public Kaggle dataset, they become critical when working with actual employee information systems, providing data extraction, explaining table relationships, and ensuring proper security protocols.

HR Leadership (Stakeholders) represents the end users of our analysis. We shall work together with them to grasp their particular retention inquiries, specify what choices they must make, and deliver results in understandable formats that encourage action instead of merely generating technical documents.

Data Governance or Privacy Officer (in practical applications) guarantees adherence to regulations such as PIPEDA, FIPPA, or GDPR. Although this synthetic dataset doesn't need supervision, real HR data necessitates their authorization and direction regarding de-identification and privacy measures.

Within an academic environment, we would partner with our instructor for methodological advice and engage with classmates for peer evaluations and different analytical strategies. This cooperative method guarantees that the analysis is technically robust, relevant to the domain, and applicable for decision-making within the organization.

### Data Preparation and Quality Assessment

In this assignment, before the data would be passed on for further modelling, we would employ several preparation steps to ensure that there is data quality, reliability, and suitability for the predictive modelling, considering that the focus for the analysis here is attrition.

First, missing data would be identified and quantified across all variables. Although there might be a few Nas in the dataset, any gaps in fields such as education, job role, or income would require attention. Missing values in numerical variables may be imputed using simple approaches like mean or median, or flagged for review, while missing categorical values may need mode imputation or a dedicated unknown category. Rows with excessive missingness might be removed after several deliberations from the group.

Next, the data would be checked for incorrect values, for example negative ages, unrealistic total working years, duplicated employee IDs, or inconsistent combinations such as “Years at Company” greater than “Total Working Years.” Categorical variables would also require validation to ensure labels are properly formatted and standardized.
Outlier detection is essential for numerical fields such as monthly income, years of experience, distance from home, or daily rate. The outliers that would be identified may indicate data entry errors or genuinely extreme cases which would be evaluated and either corrected or removed depending on context.

The final step would be to ensure correct data types and documenting all cleaning decisions be to ensure transparency for the modelling team.

**Models to Employ and Rationale**

To uncover meaningful patterns in employee attrition, I would use a combination of descriptive, predictive, and exploratory models. Each model offers unique advantages that support both discovery and decision-making in an HR analytics context.

1. Logistic Regression (Primary Predictive Model)

Why this model: Logistic regression is the foundational predictive model for a binary classification problem such as attrition (Yes/No). It provides high interpretability, making it ideal for HR stakeholders who require transparent and ethically defensible insights.

What it contributes:

Interpretability: Coefficients directly show whether a variable increases or decreases attrition risk, helping HR teams translate findings into action.

Transparency: Supports fairness, compliance, and explainability—critical in HR-related decisions.

Baseline standard: Serves as a benchmark for evaluating more complex models.

Logistic regression is especially useful in identifying key drivers of attrition such as overtime status, job satisfaction, or distance from home, making it the preferred first step before building more complex models.

2. Decision Trees

Why this model: Decision trees mimic human decision-making and are easy to communicate. They reveal how combinations of variables form meaningful patterns that influence employee turnover.

What it contributes:

Clear segmentation: Shows how specific groups behave (e.g., low satisfaction + long commute → high attrition).

Captures non-linearity: Identifies relationships logistic regression may miss.

Practical insights: Produces simple rules that HR leaders can directly apply in retention strategies.

Decision trees are ideal when the goal is to understand which profiles of employees face the highest attrition risk and why.

3. Random Forest (Ensemble Model for Enhanced Accuracy)

Why this model: Random Forest reduces the instability of individual decision trees by aggregating many of them, resulting in better accuracy and generalizability.

What it contributes:

High predictive power: Handles complex interactions in HR data.

Feature importance rankings: Shows which variables matter most across thousands of trees.

Reduced overfitting: Ensemble structure ensures more reliable predictions.

This model is especially beneficial when working with multiple interacting variables such as income, job level, environment satisfaction, and years at company.

4. Gradient Boosting Models (e.g., XGBoost)

Why this model: XGBoost builds trees sequentially, allowing each tree to correct the errors of the previous one. It is often the highest-performing model on structured tabular data like HR datasets.

What it contributes:

Optimized accuracy: Excellent for maximizing predictive performance when stakes are high.

Handles imbalance: Attrition datasets often have far more “No” than “Yes” cases; boosting models manage this better.

Captures subtle interactions: Learns complex patterns logistic regression and simple trees cannot detect.

Because these models are less interpretable, they are best used after ensuring fairness and applying explainability techniques (e.g., SHAP values) if used in real HR contexts.

5. Cluster Analysis (Exploratory Model)

Why this model: Before prediction, clustering helps uncover natural groupings of employees that may not be immediately visible.

What it contributes:

Hidden patterns: Reveals employee segments that face similar workplace conditions or risks.

Better feature engineering: Insights can guide variable transformations or groupings for predictive models.

Targeted interventions: HR can design differentiated retention strategies for specific clusters (e.g., early-career employees with heavy workloads).

Cluster analysis enhances understanding at a population level and strengthens later predictive modelling.
<img width="468" height="612" alt="image" src="https://github.com/user-attachments/assets/d5393153-a8c7-47b1-82e0-f86edde41b42" />

