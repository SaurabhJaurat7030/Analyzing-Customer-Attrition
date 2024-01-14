# Analyzing-Customer-Attrition
Integrated Analysis of Churn Dynamics in Telecom: Unveiling Patterns through Customer and Internet Data

# Description
In the ever-evolving telecom landscape, combating customer churn is a constant challenge. This project dives into the intricacies of churn analysis, utilizing three core datasets – churn data, customer data, and internet data.

The churn data set provides insights into termination decisions, forming the basis for a predictive model to anticipate and address potential churn events proactively.

Customer data offers a comprehensive profile, including demographics and usage patterns, enabling a nuanced understanding of individual preferences and behaviors.

Internet data explores the relationship between online activities and telecom churn, recognizing the increasing importance of internet services.

This project aims to synthesize these datasets, creating a robust machine learning model. Beyond predicting churn, the model uncovers valuable connections between customer demographics, behaviors, and internet usage. The outcome is a roadmap for telecom companies to enhance retention strategies in the face of dynamic industry challenges.

# Objective
Develop a predictive machine learning model by integrating churn, customer, and internet data in the telecom industry. The objective is to anticipate and understand customer churn events, revealing correlations between demographics, behaviors, and internet usage. The insights gained will guide the enhancement of targeted retention strategies for telecom companies.

# Dataset
[customer_data.csv](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/files/13931041/customer_data.csv)

[churn_data.csv](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/files/13931042/churn_data.csv)

[internet_data.csv](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/files/13931043/internet_data.csv)

## Language and Libraries
Language : Python

Libraries
- Numpy
- Pandas
- Matplotlib
- Seaborn
- statsmodel
- Sklearn

# Project Approach

## Data Understanding
   Whole dataset after merging all the data set, infromationa and description
   
![Merged_Data](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/29c7363a-ff3c-4bba-bafc-f283b2b042ae)

![Desc](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/ff4452fa-3748-4289-a1ce-20c0823af0d0)

![Info](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/b913b94e-1cfc-4873-a255-8218f474cba5)

## Data Prepartion
- We need to handle null values, create dummay variables by one-hot-encoding.
   ![dp_datafframe](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/8fc8f425-02d4-4589-b2d8-7d2badb69546)
   
![outlier_check](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/d1127066-58f8-4265-ab17-074835eeb6c6)

- checking for the correlation between featuers
![corr](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/7ca63c0c-e75d-4f2f-8f90-f66db62efe9b)

- Correaltion between features after removing highly correlated features
  ![corr_2](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/d99a2306-2f3e-484f-a1d6-2a060e96c6d1)

- Using Recusring Feature Elimination Method to get top 15 featueres
  ![RFE_top15](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/51ee7935-5b2c-45ea-9cb5-4bef2d1ba0d1)

## Model building
- building Logestic regression model with top 15 features and after removing fetaures with high P-value and VIF final trained model summnary looks like

    ![Final Model](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/1a955cb5-442c-4766-aafd-28df419e3a5e)
    ![Final_VIF](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/d8d7839b-6dcf-449d-be59-f1bfcd3368fe)
  
    

  - Finding Optimum Cutoff, with taking cutoffs upto 0.9 and by accuaray,sensitivy and specificacity Traidoff (Optimum cutoff is 0.3)
    
    ![Optimumcutoff_DF](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/883b8a4d-fcd6-426d-9f98-105b8d2a1dee)

    ![ASS_curve](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/9a0551cd-2830-40a8-9c6a-f95f1a4b813b)
  
    - ROC Curve
    
      ![ROC](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/a1ce4cea-cd02-4354-a7b7-29dc955d65cd)

    - Precision-Recall Traidoff
    
  ![precesion_recall](https://github.com/SaurabhJaurat7030/Analyzing-Customer-Attrition/assets/154229876/34442fe1-2ebd-44ff-b36f-fcce155006f0)

  ## Final Model Summary
 ### Train Dataset:
- Accuracy : 77.00%
- Sensitivity : 77.62%
- Specoficacity: 76.78%

### Test Dataset:
- Accuracy : 74.08%
- Sensitivity : 71.99%
- Specoficacity: 74.86%
  
   



