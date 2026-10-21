# Google Advanced Data Analytics Capstone

### Business Problem Context
The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They collected data from employees, but now they don’t know what to do with it. They refer to you as a data analytics professional and ask you to provide data-driven suggestions based on your understanding of the data. They have the following question: what’s likely to make the employee leave the company?

### Problem Statement
It is time-consuming and expensive to find, interview, and hire new employees. Increasing employee retention will be beneficial to the company.

### Goals
Analyze the data collected by the HR department and to build a model that predicts whether or not an employee will leave the company. 

### Modeling
The dataset has through preprocessing stage: one-hot encoding and scaling. During modeling process, several based learners and ensemble models have been compared. Resampling has been tried as the data was imbalanced, but the metrics do not show any improvement. Bagging Classifier (with Decision Tree based) give better result with F-1 score 95% (balanced of Precision and Recall) score. Further hyperparameter tuning also give the same F-1 score, even with adjusting threshold value doesn’t improve model accuracy rate significantly.

### Model Interpretation
Several methods such as Feature Importance, SHAP value, and LIME are used to understand how the model works.

<img width="940" height="389" alt="image" src="https://github.com/user-attachments/assets/5cd45b0d-e11e-41d3-91d6-211345ffdf2d" />

`Satisfaction_level` plays a huge role, 45% in determining whether employee will left or not. This is followed by `Number_project` and `Last_evaluation` around 15%, `time_spend_company` and `average_monthly_hours` contribute 10% of the model prediction. This is also supported by the SHAP plot as below:

<img width="566" height="667" alt="SHAP Values" src="https://github.com/user-attachments/assets/5dd336b6-faf8-4b8d-a83b-3ea138c36bce" />

### Recommendation:
To increase employee retainment rate, HR team should focus on employee who gave low satisfaction level, to understand the root cause. Based on the dataset, it is known that low satisfaction level indicates the employee worked a high number of projects thus longer working hours. HR should address these issues to each deparment head or managers, to balance the workload. 
