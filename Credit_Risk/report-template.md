

## Overview of the Analysis


* The purpose of the analysis is to use various techniques to train and evaluate a model based on loan risk to identify the creditworthiness of borrowers.

* Financial information the data was on, and what you needed to predict.
The following features (independent variables) and the target variable (dependent variable) were used for analysis:

Features (X):
loan_size
interest_rate
borrower_income
debt_to_income
num_of_accounts
derogatory_marks
total_debt

Target variable (y):
loan_status
0 (healthy loan) and 1 (high-risk loan) labels

* The stages of the machine learning process you went through as part of this analysis.
The stages of the machine learning process are as follows:

- Data preprocessing. The data was split into features (X) and the target variable (y), which is the loan_status column representing the labels. The balance of the target labels was checked to assess any class imbalance. y.value_counts() 0 - 75036, 1 - 2500
- Model building. Two logistic regression models were created using different training datasets:
  Model 1: Logistic regression model trained with the original data.
  Model 2: Logistic regression model trained with resampled data using the RandomOverSampler. 
  The balance of the resampled labels data y_resample.value_counts() 1 - 56271, - 56271


## Results

The balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  Balanced Accuracy Score: 0.9520
  Precision and Recall Scores:
    Precision for label 0: 1.00
    Precision for label 1: 0.85
    Recall for label 0: 0.99
    Recall for label 1: 0.91


* Machine Learning Model 2:
 Balanced Accuracy Score: 0.9937
  Precision and Recall Scores:
    Precision for label 0: 1.00
    Precision for label 1: 0.84
    Recall for label 0: 0.99
    Recall for label 1: 0.99

## Summary

Based on the results, both models performed well in predicting the loan status. However, the logistic regression model, trained with oversampled data - Model 2, has a higher balanced accuracy score (0.9937 vs. 0.9520) and improved recall for label 1 (high-risk loans). The resampled model shows better performance in correctly identifying high-risk loans, it reduces the risk of approving potentially risky loans.


