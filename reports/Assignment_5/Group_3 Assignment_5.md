### Northeastern University, Vancouver

### Course: ALY6120 - Leadership in Analytics 

### Module 5 Assignment (Group 3)

### CRISP-DM Cycle: Modeling

### Title: Employee Attrition Prediction Analysis

### Student Names: Parita Gala, Josephine Agbedoawu, Jiansheng Shentu, Godfred Akoto

### Professor: Abeba N. Turi

### Date: December 01, 2025




### 1. Identify Your Model or Models
For our employee attrition project, we are using three classification models that build on each other:
#### Logistic Regression
This is our starting point because it is straightforward and tells us exactly how factors like job satisfaction or overtime affect someone's likelihood of leaving. When we present findings to HR leadership at any organization, they need to understand not just the prediction but also why, and logistic regression gives us those clear answers.
#### Decision Tree
This model helps us see the real-world patterns that are not always linear. For instance, working overtime might not be a problem by itself, but when you combine it with poor work-life balance, that is when people start looking elsewhere. The tree structure makes these combinations visible and gives managers practical decision points.
#### Random Forest
This is where we get our best predictions. It handles all the messiness in our IBM dataset (the mix of numbers and categories), the fact that most people stay while fewer leave, and still finds the patterns that matter most. This typically becomes our main prediction tool once we have understood the insights from the simpler models.
Together, these models let us start simple and interpretable, then build up to the accuracy we need for real retention decisions.

### 2. Describe How the Model(s) Will Address the Business Problem
Our models will help the company move from reacting to turnover to preventing it. By analyzing factors like income, tenure, overtime, and job satisfaction, they will show who is most at risk and the reasons behind it. This allows HR to intervene early with targeted actions—improving work-life balance, offering growth opportunities, or adjusting workloads. The models also quantify the cost of turnover and highlight high-risk roles, making retention efforts easier to justify. Overall, they give HR a clear, data-driven way to address problems before employees decide to leave.

### 3. Attrition Model Summary
The models were chosen for a strategic balance. Logistic Regression is prized for its high interpretability through directional coefficients, but it fails to capture complexity. Decision Trees identify actionable, non-linear interaction rules but risk overfitting. The Random Forest offers the highest accuracy for prediction but is a "black box," requiring reliance on Feature Importance rather than direct causal explanation (Hastie et al., 2009; Shmueli et al., 2017).

### 4. Project Team Collaboration
We would collaborate with a team of three main groups:
Data & Analytics: Data Scientists build the models, and Data Engineers maintain the data pipelines.
HR & Business: HR Business Partners use the predictions for employee interventions, and Business Leaders implement organizational changes based on insights.
Ethics & Legal: Legal Counsel and Compliance Officers ensure the model operates fairly, without bias, and adheres to privacy laws.

### 5. Highlight any potential data quality issues with your model(s)
When building predictive models, data quality can make or break your results. Missing values create blind spots, outliers skew your coefficients, and inconsistent categories muddy the waters. Duplicate records artificially inflate certain patterns while unbalanced classes push predictions toward the majority. Even something as basic as incorrect data types can violate core model assumptions. Taking time to clean and validate your data upfront saves countless headaches down the road—it's the unglamorous work that makes everything else possible.

### 6. Key Patterns to identify in the models
Our goal is to find out the real stories behind why our employees leave. Our models will help us to see when certain factors come together—like low job satisfaction, long commutes, and constant overtime—to quietly push employees toward resignation. Logistic regression will show which issues matter most, while decision trees will show how they interact in everyday situations. Random Forest will confirm the top drivers across the organization. By turning these findings into plain insights, the HR can focus on the real-life challenges that employees face and take action before they decide to go.

### Reference
Hastie, T., Tibshirani, R., & Friedman, J. (2009). The elements of statistical learning: Data mining, inference, and prediction (2nd ed.). Springer Science+Business Media.
Shmueli, G., Patel, N. R., & Bruce, P. C. (2017). Data mining for business analytics: Concepts, techniques, and applications in R. Wiley.
