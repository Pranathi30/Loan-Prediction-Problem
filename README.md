# Loan-Prediction-Problem
Link to the data set and Problem statement

https://datahack.analyticsvidhya.com/contest/practice-problem-loan-prediction-iii/

Steps to solve the problem:

Tried different models to check how the accuracy varies. I found that with logistic regression and XGBoost without any feature engineering the accuracy did not change and it was found to be 0.778. While it reduced with Random Forest.
The accuracy has increased when features like loan_income_ratio and income_per_dependent were introduced with XGBoost. It was found to be 0.801.Hence I took XGBoost with feature engineering as my main model

1) Basic preprocessing :
- filled missing values with -1 and 0 accordingly
- Done label encoding to change categorical variables to continous variables

2) Feature Engineering:
- Added features loan_income_ratio and income_per dependent
3) Defined customised accuracy metric
4) Used in built cross validation for XGBoost, where I performed 10-fold cross validation and found 4 rounds as the optimum value.
5) fitted the model using train and predicted on the test data set.
6) Plotting the F-score values showed that loan_income_ratio and income_per_dependent are important features.
