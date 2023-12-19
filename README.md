# `Employee Attrition Prediction`: Identify Early Signs of Employee Turnover 

<img src="https://i.giphy.com/media/kf8bMrmElVACLbFCDg/giphy.webp" alt="drawing" width="200"/>

➽ Predict Employee Attrition with Supervised Machine Learning Models.  

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/dwyl/imgup/ci.yml?label=build&style=flat-square&branch=main)
[![codecov.io](https://img.shields.io/codecov/c/github/dwyl/imgup/main.svg?style=flat-square)](https://codecov.io/github/dwyl/imgup?branch=main)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat-square)](https://github.com/dwyl/imgup/issues)
[![contributions welcome](https://img.shields.io/badge/feedback-welcome-brightgreen.svg?style=flat-square)](https://github.com/dwyl/app-mvp/issues)

&nbsp;
### Table of Contents
1. [Problem Definition & Objectives](#header-1)
2. [Dataset Analysis](#dataset-analysis)
3. [Model Development](#model-development)

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
* **Data Types:** 9 categorical, 26 numeric
* **Missing cells:** 0
* **Missing cells (%):**	0.0%
* **Total size in memory:**	1.1 MiB
* **Average record size in memory:** 796.8 B
* **Label:** The dataset uses the binary label <code>Attrition</code> to indicate employee turnover ('Yes') or retention ('No').
  &nbsp;
<img src="Screenshots/Attrition Imbalance.png" width="300" height="250"/>
The data indicates a significant class imbalance, with 84% of employees falling into the ('No') category and only 16% in the ('Yes') category.

 
&nbsp;
### Exploratory Data Analysis (EDA)  

#### Bivariate Analysis  

➤ Job Level vs Monthly Income  

<img src="Screenshots/JobLevel vs MonthlyIncome.png"/>

The line chart shows a nearly straight positive slope, indicating a strong correlation between `JobLevel` and `MonthlyIncome` . This means that on average, employees with higher job levels earn higher income each month.

&nbsp;
➤ Performance Rating vs Percent SalaryHike  

<img src="Screenshots/PerformanceRating vs PercentSalaryHike.png"/>  

The line chart shows a straight positive slope, indicating a strong correlation between `PerformanceRating` and `PercentSalaryHike` . Indicating that employees with higher performance ratings tend to receive higher salary hikes.  

&nbsp;
➤ Total Working Years vs Monthly Income  

<img src="Screenshots/TotalWorkingYears vs MonthlyIncome.png"/>  

The line on the graph shows a general trend of increasing `MonthlyIncome` with increasing `TotalWorkingYears` . However, there is a dramatic increase at `TotalWorkingYears` of 20. Suggesting that employees with 20+ years of experience receive approximately twice the income compared to those with less than 20 years of experience. The error band is also growing with the rising trend of the line.  

&nbsp;
➤ Age vs Monthly Income  

<img src="Screenshots/Age vs MonthlyIncome.png" width="600" height="450"/>  

The line slopes upwards, indicating a positive correlation between `Age` and `MonthlyIncome` . This means that on average, employees earn higher income as they get older. Additionally, the growing error band as the line it goes to the right indicates an increased in the uncertainty or variability of the data.  

&nbsp;
#### Target Variable Analysis

image grid

Based on the above findings, the following factors were found to have the most impact on employee attrition:
1. Late 20's - late 40's.
2. Live closer to work.
3. Low income.
4. Newly hired.
5. No prior experience.
6. Entry-Level.
7. Single.
8. Working in Research & Development department.
9. Either Laboratory Technician, Sales Executive or Research Scientist.

&nbsp;
# Model Development  
Since this is a **supervised binary classification problem** , several the classification models were trained and tested. The four best-performing models based on AUC-ROC score were:
1. Logistic Regression
2. Random Forest
3. Gaussian Naive Bayes
4. Decision Tree
  
&nbsp;
### Evaluation and Performance
To evaluate the models performance, the following metrics were measured:
* Confusion matrix
* AUC-ROC: given the imbalance in the dataset, focusing solely on Accuracy could be misleading. A model could simply predict the majority class to achieve high accuracy, but miss important insights into identifying the minority class. Therefore, we opted for AUC-ROC as a more robust performance metric.
* Precision
* Recall


The below numbers represent the models performance in predicting the Attrition ('Yes') class:
| Model | ROC-AUC    | Precision    | Recall    | Confusion matrix    |
| :---:   | :---: | :---: | :---: | :---: |
| Logistic Regression | 77.7 %   | 27%   | 65%   | [Click to View](Screenshots/LR_CM.png)   |
| Random Forest | 75.7%   | 27%   | 50%   | [Click to View](Screenshots/RF_CM.png)   |
| Gaussian Naive Bayes | 71.8 %   | 24%   | 71%   | [Click to View](Screenshots/GN_CM.png)   |
| Decision Tree | 63.4%    | 21%   | 54%   | [Click to View](Screenshots/DT_CM.png)   |  

&nbsp;
#### &nbsp;&nbsp;&nbsp; ▶️ For more details, please check the notebook file [here](Human_Resources_Department.ipynb). 
 
&nbsp;

### ░░░░░  Thank you for your interest in this project! I hope you find it helpful😄 ░░░░░ 
