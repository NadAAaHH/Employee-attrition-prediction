<img src="https://i.giphy.com/media/kf8bMrmElVACLbFCDg/giphy.webp" alt="drawing" width="200"/>

# Employee Attrition Prediction: Why Do Employees Leave Their Organization?

### What's the Problem & Why it's Important?
Employee attrition is a normal part of any business, but it can have a negative impact on the activities of other employees and the company's recruitment process. By understanding the reasons why employees leave, companies can take steps to address these issues and create a more positive and engaging work environment. This can lead to improved employee retention, which can save businesses money and help them achieve their goals.

### What's the Goal of This Project?
This project aims to develop a predictive model that can determine which employees are most likely to leave based on various information about the employees.


# Data
* **Source:** [IBM HR Analytics Employee Attrition & Performance Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset).
* **Dataset Structure:** 1470 samples (rows), 35 features (variables)
* **Data Type:** categorical and numerical
* **Label:** <code>'Attrition'</code> is the label in this dataset, with 'Yes' indicate leaving and 'No' indicate staying. Therefore, the label is binary.


# Analysis
Based on the above findings, the following factors were found to have the most impact on employee attrition:
1. Newly recruited employees 
2. At late 20's and early 30's 
3. Living far from work 


# Model Development
Since this is a supervised classification problem, the following classification models were picked for training:
* Random Forest
* Logistic Regression
* Neural Network

### Evaluation
To evaluate the models performance, the following measurements were used:
* Confusion matrix
* Precision
* Recall
* Accuracy

### Performance

| Model | Accuracy    | Precision    | Recall    |
| :---:   | :---: | :---: | :---: |
| Neural Network | 87.96 %   | --   | --   |
| Random Forest | 86.68 %   | --   | --   |
| Logistic Regression | 75.54 %   | --   | --   |

# Conclusion
After conducting the results of the models, we can conclude the top Reasons why employees leave the organization:
* No Overtime: This was a surpirse, employees who don't have overtime are most likely to leave the organization. This could be that employees would like to have a higher amount of income or employees could feel that they are underused.
* Monthly Income: As expected, Income is a huge factor as why employees leave the organization in search for a better salary.
* Age: This could also be expected, since people who are aiming to retire will leave the organization.
  
Knowing the most likely reasons why employees leave the organization, can help the organization take action and reduce the level of Attrition inside the organization.


