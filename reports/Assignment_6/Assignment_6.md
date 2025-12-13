

# CRISP-DM: Business Understanding and Data Understanding
This phase establishes the project’s overall objectives and success criteria.


### Business Objectives

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


## 2. Data Understanding

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

