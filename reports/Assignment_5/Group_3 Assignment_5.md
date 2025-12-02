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
The real challenge organizations face is not just knowing turnover happens; it's knowing who might leave and being able to do something about it before they have already decided. That is exactly what these models solve.
Finding people at risk early, by examining factors such as monthly earnings, tenure at the company, and overtime trends, we can identify employees exhibiting worrying patterns before they begin searching for new jobs. HR can then engage in crucial check-in discussions while there is still an opportunity to resolve issues, instead of performing exit interviews once someone has already left.
Understanding What Matters: These models do not just predict, they tell us why. If we discover that work-life balance is the biggest driver in a particular department, that is actionable. 
We are confident about offering better pay or flexible hours; we know which option will genuinely have an impact. This is especially important when retention budgets are limited and need to be used wisely.
Customizing Our Reply: Not everyone departs for identical reasons. A top achiever may feel dissatisfied due to limited growth prospects, whereas another person might simply be exhausted from continual extra hours. The models assist us in recognizing these various scenarios so we can react suitably: career discussions for some, workload modifications for others
Making the Business Case: When we can forecast that certain roles or departments will likely see higher turnover and quantify the cost (typically 50-200% of someone's salary when you factor in recruitment, training, and lost productivity), it becomes much easier to justify investing in retention programs. We are showing clear ROI rather than just saying retention is important.
Changing How HR Operates: This shifts the entire approach from reactive to strategic. Instead of wondering why someone left after they are gone, we are identifying risks and addressing them proactively. It is the kind of analytics-enabled decision-making we have been discussing throughout this course, using data to drive real organizational change.
What makes this work is that we are not just building models for the sake of having predictions. We are developing a system that truly assists organizations in retaining valuable employees, minimizes the ongoing cycle of recruitment and training, and fosters more stable teams. The main goal of utilizing analytics in HR is to enhance workplaces by making informed decisions.

