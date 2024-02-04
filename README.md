# Advanced Regression Assignment


## Table of Contents
* [General Info](#general-information)
* [Contents](#contents)
* [Technologies Used](#technologies-used)
* [Steps performed](#Steps-performed)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
- This repository contains the code for Advanced Regression modeling on housing dataset.
- Problem Statement
A US-based housing company named Surprise Housing has decided to enter the Australian market.
The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia.
The company is looking at prospective properties to buy to enter the market
Build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

The company wants to know:
Which variables are significant in predicting the price of a house
How well those variables describe the price of a house.
Determine the optimal value of lambda for ridge and lasso regression.

- Business Goal
Model the price of houses with the available independent variables.
This model will then be used by the management to understand how exactly the prices vary with the variables.
They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

- Dataset used: train.csv

## Contents
- Notebook: EPGPML58_AnishVA_AdvancedRegression.ipynb
- Document: Advanced_Regression_Subjective_Questions.pdf

## Steps Performed
Following steps were perfomed to create the model and do the prediction
- Reading and Understanding the Data
- Data cleaning (missing value, data duplicate check etc.)
- Dropping irrelavant feature columns based on initial data understanding
- Visualising the Data
- Data Preparation (Creating dummy varaibles for categorical columns)
- Splitting the Data into Training and Testing Sets
- Rescaling the Features (Using Standard scalar)
- Dividing tarining data into X and Y sets for the model building
- Removing features having high colliniarity and low variance
- Building the model (Model shall be built using Ridge and Lasso Regression function from SciKit Learn for its compatibility with RFE (which is a utility from sklearn))
- Making Predictions with test data (Applying the scaling on the test sets, Dividing into X_test and y_test, predict with x_test data)
- Model Evaluation (R2, RSS, RMSE)
- Choosing appropraite model based on metrics obtained


## Conclusions
Based on the model metrics, here are the inferences.
- Lasso and Ridge regression has almost same train and test accuracy (Observed from the above mertic table)
- Lasso regression model is slighly better than Ridge model (metric on test data determines the same).Lasso regression has omitted 61 features.
- Lasso regression shall be chosen as final model, from the above considerations
- From the above features and its coefficient, it can be determined that:
    - OverallQual (Overall Quality of the house) is a significant predictor, with higher quality (e.g., OverallQual_9 - Excellent, OverallQual_8 - very good) contributing positively to the house sale price. OverallQual (OverallQual_3, OverallQual_4) contributes negatively to the house sale price
    - OverallCond (Overall Condition of the house) is also a significant predictor, but negatively impacting the price. Lower overall condition (OverallCond_3) leads to lower prices.
    - Neighborhood features such as Crawfor, NridgHt, IDOTRR, MeadowV, and StoneBr are significant predictors. Certain neighborhoods ( Crawfor, NridgHt, StoneBr) positively affect the house price, while others (IDOTRR, MeadowV) have a negative impact.
    - Other features like MSSubClass_30, BsmtExposure_Gd, SaleCondition_Partial, Exterior1st_BrkFace, etc., also have significant but varying impacts on the house price.
    - Summary: Quality, condition, and neighborhood of the house are significant predictors of the house sale price.
    

For more details, refer to EPGPML58_AnishVA_AdvancedRegression.ipynb


## Technologies Used
- Seaborn version: 0.12.2
- Matplotlib version: 3.7.0
- Python version: 3.10.9
- scikit-learn version: 1.2.1



## Contact
Created by [@anishnairva] - feel free to contact me!
