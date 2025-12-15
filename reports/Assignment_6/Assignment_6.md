###Signature Assessment (Group 3)###

# CRISP-DM: Business Understanding and Data Understanding
This phase establishes the project’s overall objectives and success criteria.


### 1 Business Objectives

The overarching business problem is **employee turnover (attrition)**.  
The aim is to shift the organization from **reacting** to turnover toward **preventing** it through data-driven decision-making.

- **Goal:** Strengthen workforce retention strategies by identifying meaningful patterns in employee attrition.
- **Outcome:** Design targeted interventions and implement organizational improvements backed by analytics.
- **Value:** Quantify the cost of turnover and highlight high-risk roles, making retention initiatives easier to justify.


### Data Mining Goal

The Data Mining Goal is to identify the **key drivers of attrition** and **predict employees most likely to leave**.

- **Prediction:** Identify employees most at risk and determine contributing factors.
- **Discovery:** Uncover deeper insights such as:
  - Low job satisfaction + long commutes + frequent overtime → increased resignation likelihood.
  - Interaction of organizational factors that push employees toward turnover.


### Business Success Criteria

Success will be measured by the model’s ability to produce **actionable**, **practical**, and **impactful** insights.

- Models must guide HR to intervene **before** employees decide to leave.
- Findings must be **clear** and **interpretable**, transforming analytics into real managerial decision points.
- Success is defined by **measurable improvements** in retention metrics (e.g., reduced attrition rate).


### 2 Data Understanding

This phase focuses on **collecting**, **describing**, **exploring**, and **verifying** data quality.


### Collect Initial Data (Data Sources)

**Primary Dataset:**  
The *IBM HR Analytics Employee Attrition & Performance Dataset*.

- **Acquisition (for this project):**  
  Obtained from **Kaggle**, a reliable, publicly available data repository used for academic and professional studies.

- **Acquisition in a real corporate setting:**  
  Data would typically come from internal systems such as:
  - HRIS  
  - Payroll  
  - Employee performance systems  
  - Employee engagement or survey tools  


### Data Content

The dataset includes variables across key HR domains:

- **Employee Demographics**
  - Age, gender, marital status, education level

- **Job & Organizational Factors**
  - Job role, job satisfaction, work-life balance, job level

- **Compensation & Benefits**
  - Monthly income, hourly rate, stock option level

- **Workplace Behavior**
  - Overtime, distance from home, years at company, total working years

- **Target Variable**
  - **Attrition:** *Yes/No*  


### Verify Data Quality

Ensuring data quality, reliability, and suitability is critical before modeling.  
Potential issues include:

- Missing values (e.g., education fields, salary fields)
- Outliers (e.g., unusually high or low income)
- Incorrect categories or data types
- Duplicate records
- Class imbalance (far more employees stay than leave)
- Logical inconsistencies  
  - Example: *Years at Company* > *Total Working Years*


### Quality Assessment Steps

Steps taken to validate and prepare data:

1. **Identify & quantify missing data**
   - Impute numerical values (mean/median)
   - Impute categorical values (mode or "Unknown")

2. **Check correctness & consistency**
   - Fix incorrect values  
   - Remove or merge duplicate employee IDs  
   - Ensure logical consistency between fields  

3. **Detect & handle outliers**
   - Review numerical distributions  
   - Remove or correct anomalies where appropriate  

4. **Validate data types**
   - Ensure all fields use consistent and appropriate formats  

5. **Document all cleaning decisions**
   - Maintain transparency and reproducibility
  
##3. Data Preparation
The Data Preparation stage of the CRISP-DM framework is a critical step that transforms the raw IBM HR Analytics Employee Attrition & Performance dataset into a high-quality analytical asset suitable for modelling. Since this dataset reflects many of the variables found in real-world HRIS environments including demographic, organizational, behavioral, and compensation-related features, rigorous preparation is required to ensure that both the predictive models and subsequent interpretations are valid, reliable, and ethically defensible. This stage focuses on selecting relevant data, cleaning and correcting inconsistencies, engineering meaningful features, and preparing the final dataset for use in logistic regression, decision tree, and Random Forest models.

Data Selection
Although the dataset contains a wide range of variables, not all fields contribute meaningfully to attrition prediction or align with the business objectives. During this phase:
· Irrelevant or redundant variables (e.g., Employee Count, Standard Hours, Employee Number) were removed because they offer no predictive value.
· Features directly tied to the target variable (such as Attrition) were retained as-is.
· Predictor variables expected to influence attrition, job satisfaction, overtime, years at company, income, and work - life balance were prioritized for deeper cleaning and transformation.
This step ensures that only variables aligned with the business problem and data mining goals progress through the modelling pipeline.

Data Cleaning
Data cleaning addresses inaccuracies and prepares the dataset for consistent interpretation.

Handling Missing Data
Although the IBM dataset contains limited missing values due to its synthetic design, a robust workflow was implemented to mirror what would be required in a real corporate HR environment:
· Numerical variables were imputed using median or mean values.
· Categorical variables were imputed using mode or assigned an “Unknown” category.
· Documentation of cleaning decisions was maintained to preserve transparency.

Resolving Inconsistencies
Quality checks were conducted to identify:
· Inaccurate or impossible values (e.g., Years at Company > Total Working Years)
· Mismatched categorical entries
· Duplicate records
· Conflicting combinations such as high Job Satisfaction paired with Very Low Work-Life Balance when inconsistent with broader profile patterns
These inconsistencies were corrected or removed based on HR logic and dataset constraints.

Outlier Detection and Treatment
Outliers can distort model coefficients, especially for interpretable models such as logistic regression. Several numerical fields were assessed, including:
· Monthly Income
· Daily Rate
· Total Working Years
· Distance From Home
Boxplots and z-score analysis were used to detect extreme values. Outliers without plausible HR justification were removed or capped to preserve the predictive integrity of the dataset.

Data Transformation
To ensure compatibility with machine learning models, several transformations were applied Categorical Encoding, Feature Scaling and Feature Engineering. These ensured that the logistic
regression model could interpret categorical data numerically and that the Random Forest model could maximize pattern detection.

Addressing Class Imbalance
Employee attrition is naturally imbalanced, with far more employees staying than leaving. To prevent models from over-predicting the majority class:
· SMOTE oversampling was applied during model training
· Class weights were adjusted for logistic regression
· Random Forest was tuned using balanced subsampling parameters
These steps ensure the model can recognize high-risk employees without bias toward the dominant class.

Dataset Integration and Finalization
All cleaned, encoded, and engineered variables were consolidated into a finalized modelling dataset. This final prepared dataset provided the foundation for building a robust predictive model that accurately would detect attrition risk and support HR’s proactive retention strategies.


### 4 Modeling and EVALUATION
At this evaluation stage, we determine if the created models effectively meet the initial business goals. This project sought to accurately forecast attrition while making sure insights were understandable, actionable, equitable, and in line with Human Resource leadership requirements. This stage assesses model effectiveness from technical and business viewpoints

### Evaluation Criteria and Metrics
Given the binary nature of employee attrition and class imbalance in the dataset, multiple performance metrics were employed:

•	Accuracy provided overall correctness but was not exclusively relied upon due to class imbalance.

•	Precision measured the proportion of correctly predicted attrition cases, minimizing unnecessary HR interventions.

•	Recall (Sensitivity) was prioritized to avoid missing at-risk employees and resulting turnover costs.

•	F1-score balanced precision and recall.

•	ROC-AUC assessed the model's ability to distinguish between employees who leave and those who stay.

These metrics ensured evaluation reflected business risk rather than statistical performance alone.

### Model Performance Comparison
Logistic Regression provided us with stable, interpretable performance with clear insights into attrition drivers (overtime, job satisfaction, tenure), critical for HR communication and policy justification.

Decision Trees revealed non-linear interaction patterns, such as combined effects of poor work-life balance and frequent overtime. However, overfitting was observed, requiring pruning and validation.

Random Forest achieved the strongest predictive performance in recall and ROC-AUC, effectively handling feature interactions and class imbalance.

Feature importance consistently highlighted overtime, job satisfaction, monthly income, and tenure as dominant drivers.

A layered approach, prioritizing interpretability alongside accuracy, best served the business problem.

### Business Alignment and Success Criteria
The models were evaluated against three defined success criteria:

Early Risk Identification: Models showed high recall in spotting at-risk employees, aiding in proactive prevention instead of reactive turnover handling.

Actionability: Primary factors repeatedly appeared in various models, facilitating focused HR strategies such as workload modifications, engagement efforts, and career advancement assistance.

Managerial Interpretability: Logistic Regression and Decision Trees offered understandable outcomes for business executives, whereas Random Forest's feature significance enhanced simpler models, striking a balance between predictive performance and clarity.

Predictions were confirmed for their plausibility and consistency with recognized HR issues, connecting analytics with organizational confidence.

### Ethical and Risk Considerations
Given the sensitivity of HR analytics, several ethical safeguards were implemented:

•	No demographic attribute was treated as an isolated causal factor.

•	Model outputs were framed as risk indicators, not deterministic decisions.

•	Random Forest's black-box nature was mitigated through feature importance and simpler model explanations.

•	The synthetic dataset reduced privacy concerns, though bias audits and explainability tools (e.g., SHAP) would be necessary for real employee data deployment.


### Limitations
•	The synthetic dataset may not fully capture organizational culture or workforce dynamics.

•	Cross-sectional data limit causal inference regarding time-dependent attrition factors.

•	External factors such as labour market conditions were excluded.

•	Predictive accuracy does not guarantee intervention effectiveness without organizational follow-through.

***Conclusion***

The evaluation verifies that the models we used fulfilled project goals by delivering dependable forecasts, understandable clarifications and practical recommendations. 
The Logistic Regression offers clarity, Decision Tree yields clear guidelines, and Random Forest achieves robust predictive accuracy. United, they create a strong base for forward-thinking employee retention approaches. The project is ready to move into the Deployment phase with established direction on communication, governance, and monitoring in organizational practices.


### 5 Deployment
At the deployment phase, we will focus on translating the model outputs into routine HR actions, ensuring analytics creates value beyond evaluation results. Consistent with the CRISP-DM framework, deployment emphasizes embedding insights into organizational processes so that findings directly inform decisions rather than remain analytical artifacts (Chapman et al., 2000).

In practice, the evaluated attrition models would be operationalized through a regularly refreshed HR dashboard. Instead of presenting technical metrics, we will group employees into low-, medium-, and high-risk attrition categories. This design follows best practices in business analytics, where simplifying outputs improves managerial adoption and decision quality (Shmueli et al., 2017). HR teams can then prioritize attention without treating predictions as automatic decisions.

We also includes a clear action layer. For example, if the dashboard reveals persistent high-risk signals driven by frequent overtime, HR may initiate workload reviews or staffing adjustments. If elevated risk is associated with low job satisfaction, targeted manager check-ins or engagement initiatives can be introduced. These examples illustrate how analytics supports intervention planning rather than merely identifying risk, aligning with applied predictive modeling guidance that stresses actionability over accuracy alone (Hastie et al., 2009).

Post-deployment responsibilities will also be assigned clearly. HR business partners interpret results and coordinate interventions, while analytics teams monitor model stability and refresh predictions as new data become available. Leadership oversight ensures analytical insights remain aligned with organizational priorities and ethical expectations.
Finally, deployment success will be monitored over time. Trends in attrition rates and post-intervention outcomes are reviewed periodically to assess impact. Continuous feedback allows both the analytical process and HR practices to evolve, supporting sustainable retention strategies rather than one-time analytical insights.

###References ###

Chapman, P., Clinton, J., Kerber, R., Khabaza, T., Reinartz, T., Shearer, C., & Wirth, R. (2000). CRISP-DM 1.0: Step-by-step data mining guide.

Hastie, T., Tibshirani, R., & Friedman, J. (2009). The elements of statistical learning (2nd ed.). Springer.

Shmueli, G., Patel, N. R., & Bruce, P. C. (2017). Data mining for business analytics. Wiley.





