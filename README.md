# Hospital Charge Prediction Project

## Introduction
This project aims to build a machine learning model to predict hospital charges based on patient data. The goal is to gain insights into the key factors that drive healthcare costs and help healthcare providers and payers better understand and manage inpatient expenditures.

## Data
The dataset used in this project contains information on 1,338 hospital visits, including the patient's age, sex, BMI, smoking status, number of children, region, and the total hospital charges. After cleaning and preprocessing the data, we split it into training and testing sets to evaluate different regression models.

## Modeling
We trained and evaluated several regression models to find the best performer:

1. **Linear Regression**: This provided a baseline model, achieving an R-squared of 0.7511.

2. **Support Vector Regressor (SVR)**: The SVR model did not perform as well, with an R-squared of -0.0406.

3. **Random Forest Regressor (RFR) - Model 1**: The first RFR model, with optimized hyperparameters, achieved an impressive R-squared of 0.8419.

4. **Random Forest Regressor (RFR) - Model 2**: Tuning the RFR model further, we were able to increase the R-squared to 0.843.

5. **Adaptive Boost Regressor (AdaBoost)**: The AdaBoost model attained an R-squared of 0.8403.

6. **Gradient Boosting Regressor (GBR)**: The GBR model yielded an R-squared of 0.8457, making it one of the top performers.

7. **Historic Gradient Boosting Regressor (HistGBR)**: The HistGBR model had an R-squared of 0.8296.

8. **Categorical Boosting Regressor (CatBoost)**: The CatBoost model achieved the highest R-squared of 0.8537, making it the best performing model.

## Feature Importance
To understand the key drivers of hospital charges, we examined the feature importance of the best-performing Categorical Boosting Regressor model:

1. **Smoking Status**: This was by far the most influential factor, with a feature importance over 60. Smoking is a major determinant of healthcare costs.

2. **BMI**: A patient's body mass index had the second highest importance, around 20. Higher BMI is linked to increased medical complications and costs.

3. **Age**: The patient's age was the third most important factor, with an importance around 15. Older patients tend to have greater healthcare needs and utilization.

4. **Children**: Whether the patient had children had a relatively low importance, under 5. This suggests the presence of dependents does not substantially impact inpatient charges.

5. **Region**: The geographic region variable was not included in the feature importance, indicating it had minimal impact on the model's predictions.

6. **Sex**: Interestingly, a patient's sex had the lowest importance, under 2. Gender appears to be less of a factor than other personal characteristics.

## Conclusion
The Categorical Boosting Regressor model achieved the best performance, with an R-squared of 0.8537 on the test set. This model can be used to accurately predict hospital charges based on patient data.

<img width="1168" alt="Screenshot 2024-12-09 at 15 46 44" src="https://github.com/user-attachments/assets/204fb7e6-10af-4be8-9f09-72497ebb7c2e">

The feature importance analysis reveals that a patient's smoking status, BMI, and age are the key drivers of inpatient costs, while the presence of children, geographic region, and biological sex play a less significant role. These insights can help healthcare providers and payers better target interventions and allocate resources to address the primary cost factors.

Overall, this project demonstrates the power of machine learning in uncovering meaningful patterns in healthcare data and providing actionable intelligence to improve cost management and patient outcomes.
