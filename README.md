## Overview of the Analysis

The purpose of the analysis in this repository was to build and critique a machine learning model that could predict the credit risk of certain loan applicants. This analysis is aimed at helping financial entities identifying whether a loan is likely to be "healthy" (labeled as 0) or "high-risk" (labeled as 1).

The dataset used in this analysis contained financial data on borrowers, including features such as income, loan amounts, and other key indicators. The target variable for the machine learning model was loan_status, which classified loans as either "healthy" or "high-risk".

**Stages in this machine learning process:**

1. Data Loading and Preparation: The data was first read from a CSV file and split into its features (X) and the target label (y). 
1. Data Splitting: The dataset was divided into training and testing datasets using the train_test_split function. The feature data (X) was also scaled using Standard Scaler to help solve a convergance warning that would appear without its use.
1. Model Selection and Training: A logistic regression model (LogisticRegression) was used and trained.
1. Model Evaluation: The model was lastly tested using the test dataset (X_test), and its performance was evaluated using a confusion matrix and classification report to provide metrics such as accuracy, precision, and recall.

## Results

**Logistic Regression Model:**
- Accuracy: 99%
- Precision:
    - 0 (healthy loans): 1.00
    - 1 (high-risk loans): 0.84
- Recall:
    - 0 (healthy loans): 0.99
    - 1 (high-risk loans): 0.99

## Summary

The logistic regression model achieved an overall accuracy of 99%. It performed exceptionally well and optimally in predicting healthy loans due to its perfect precision (1.00) and near-perfect recall (0.99). For high-risk loans, the model is showed good recall (0.99), identifying nearly all high-risk loans. However, its precision for high-risk loans (0.84) indicates some false positives, making it a little less appealing overall yet very serviceable

Based on the results found, this model is recommended for use by the company, especially if the priority is to minimize missed high-risk loans. However, if reducing false positives for high-risk loans is crucial, additional fine-tuning or alternative models may be necessary depending on how strict the company is.
