# Issue Summary
X Education, an online education company, has 30% low conversion of leads. They have word-of-mouth, search, and website leads but are unable to convert them into revenue-generating customers. The most important thing is to identify high-value leads for the salespeople to follow up. The organization will raise lead conversion through a logistic regression-based scoring. The goal will be to boost the conversion rate to 80%.
Information

The data set contains 9,240 rows and 37 features, both numeric and categorical. The most important preparation steps are feature engineering, missing value management, and data cleaning.
Case Study Objectives

### Develop a logistic regression model that gives a 0-100 lead score to every lead.
The model would identify high-scoring leads, allowing salespeople to focus on them for better conversion chances.
Goal: Increase the 80% lead conversion rate.
Data Preparation and Analysis

### Missing Values Handling
Characteristics with over 45% missing values.
Kept 'Select' values of categorical variables as missing and excluded them.
Filled imputed missing categorical values with mode values.
Feature Engineering:
no
Dummy-coding was applied to categorical variables.
Total visits and website time were normalized.
Categorical variables were binned into wider bins to reduce noise.

### EDA
Univariate Analysis:
Distribution of verified numerical attributes through histograms and box plots.
Conversion rates for lead source and activity were analyzed.
Bivariate Analysis:
There was strong positive correlation between lead conversion and website time.
Leads generated through SMS or email performed better.
Multivariate Analysis:
A heatmap was produced to determine correlation between numeric variables.
PageViewsPerVisit and TotalVisits were negatively and weakly correlated with conversion rate, but total time spent had a greater impact.

### Model Building and Engineering Specifications
Model: Logistic regression because it has an explainable probability score.
Feature Selection: 15 important features were chosen using Recursive Feature Elimination (RFE) to improve model performance.
Training Model: Applied LogisticRegression(class_weight='balanced') to address class imbalance.
Model Performance & Threshold Tuning
Train Set Results:
Accuracy: 89.87%
Remember: 85.4%
Test Set Results:
Accuracy: 87.12%
Recall: 83.2%
Specificity: 92.67%
Threshold Optimization:
The initial threshold value for the definition of leads was 0.5. Different thresholds were experimented with, and the optimal one was selected to achieve an 80% recall.

### Business Ideas
Top Variables for Lead Conversion:
Total Time on Site: The greatest conversion predictor.
Last Activity – SMS Sent: Leads who receive SMS notifications convert more.
Lead Quality – Not Sure: Not sure leads are less likely to convert.
Top Categorical Variables:
Lead Source – Welingak Website: This lead source has an extremely high conversion rate.
Lead Source – Lead Add Form: Manually added leads convert at a high rate.
Tags – Revert After Email: Prospects requiring follow-ups. •	Business Scenarios: Intern Recruits: Reduce the bar to more than 0.4 and aim for active users (e.g., those who spent more time on the site or engaged through SMS/email). Quarterly Targets: Raise the cut-off higher than 0.7 for high-value calls, and mail/SMS automatically for lower leads. Conclusion & Impact The lead scoring model predicts conversion probabilities, allowing X Education to engage with best-potential leads and optimize sales processes. The main benefits are: 
1.Improved sales effectiveness resulting from high-potential leads prioritization.
2.Less operational expense by avoiding unnecessary follow-ups. 
3.Anticipated increase in conversion rates to 80% conversion level as the CEO's objective.
