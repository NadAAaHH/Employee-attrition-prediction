# `Employee Attrition Prediction`: Identify Early Warning Signs of Employee Turnover 

<img src="https://i.giphy.com/media/kf8bMrmElVACLbFCDg/giphy.webp" alt="drawing" width="200"/>

➽ Predict Employee Attrition with Supervised Machine Learning Models.  

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/dwyl/imgup/ci.yml?label=build&style=flat-square&branch=main)
[![codecov.io](https://img.shields.io/codecov/c/github/dwyl/imgup/main.svg?style=flat-square)](https://codecov.io/github/dwyl/imgup?branch=main)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat-square)](https://github.com/dwyl/imgup/issues)
[![contributions welcome](https://img.shields.io/badge/feedback-welcome-brightgreen.svg?style=flat-square)](https://github.com/dwyl/app-mvp/issues)

&nbsp;
### Table of Contents
1. [Problem Definition & Objectives](#header-1)
2. [Data Statistics & Exploratory Data Analysis (EDA)](#data)
3. [Model Development](#model-development)
4. [Cluster Analysis](#cluster-analysis)

&nbsp;
# <a id="header-1"></a> Problem Definition & Objectives
### What's the Problem & Why it's Important?
Employee attrition is a normal part of any business, but it can have a negative impact on the activities of other employees and the company's recruitment process. By understanding the reasons why employees leave, companies can take steps to address these issues and create a more positive and engaging work environment. This can lead to improved employee retention, which can save businesses money and help them achieve their goals.


&nbsp;
### What's the Goal of This Project?
This project aims to develop a predictive model that can determine which employees are most likely to leave based on various information about their personal and professional history.

&nbsp;
# Dataset Analysis
#### Data Statistics
* **Source:** [IBM HR Analytics Employee Attrition & Performance Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
* **Dataset Structure:** 1470 samples (rows), 35 features (variables)
* **Data Type:** categorical and numerical
* **Label:** The dataset uses the binary label <code>Attrition</code> to indicate employee turnover ('Yes') or retention ('No').

 
&nbsp;
### Exploratory Data Analysis (EDA)
Based on the above findings, the following factors were found to have the most impact on employee attrition:
1. Newly recruited employees 
2. At late 20's and early 30's 
3. Living far from work 

&nbsp;
# Model Development
Since this is a **supervised classification problem** with binary label, the following classification models were picked for training:
* Random Forest
* Logistic Regression
* Neural Network
  
&nbsp;
### Evaluation
To evaluate the models performance, the following measurements were used:
* Confusion matrix
* Precision
* Recall
* Accuracy

&nbsp;
### Performance

| Model | Accuracy    | Precision    | Recall    |
| :---:   | :---: | :---: | :---: |
| Neural Network | 87.96 %   | --   | --   |
| Random Forest | 86.68 %   | --   | --   |
| Logistic Regression | 75.54 %   | --   | --   |

&nbsp;
# Conclusion
After conducting the results of the models, we can conclude the top Reasons why employees leave the organization:
* No Overtime: This was a surpirse, employees who don't have overtime are most likely to leave the organization. This could be that employees would like to have a higher amount of income or employees could feel that they are underused.
* Monthly Income: As expected, Income is a huge factor as why employees leave the organization in search for a better salary.
* Age: This could also be expected, since people who are aiming to retire will leave the organization.
  
Knowing the most likely reasons why employees leave the organization, can help the organization take action and reduce the level of Attrition inside the organization.


