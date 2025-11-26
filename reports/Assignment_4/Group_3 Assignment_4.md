Northeastern University, Vancouver

Course: Leadership in Analytics (ALY6120)

Module 3 Assignment (Group 3)

CRISP-DM Cycle: Data Preparation

Student Names: Parita Gala, Josephine Agbedoawu, Jiansheng Shentu, Godfred Akoto

Professor: Abeba N. Turi

Date: November 23, 2025

Title: Employee Attrition Prediction Analysis

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
