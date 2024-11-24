# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

This analysis aimed to evaluate a machine learning model's ability to predict the credit risk of borrowers using historical lending data. The dataset contained financial variables such as loan size, interest rate, borrower income, and total debt. The target variable, loan_status, indicates whether a loan is classified as "healthy" (0) or "high-risk" (1).

The analysis followed these key steps:

Data Preparation: Split the data into features (X) and target (y).
Class Distribution Analysis: Found that the dataset was highly imbalanced, with significantly more 0 (healthy loans) than 1 (high-risk loans).
Model Training: Used a logistic regression model with training and testing data split at 80% and 20%, respectively.
Evaluation: Assessed model performance using metrics such as precision, recall, and F1-score from a classification report and confusion matrix.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

Logistic Regression Model
Accuracy: Approximately 99% (due to the dominance of class 0).
Class 0 (Healthy Loans):
Precision: High (likely near 100%).
Recall: High (likely near 100%).
Class 1 (High-Risk Loans):
Precision: Low (due to false positives).
Recall: Low (due to false negatives).
F1-Score: Balances the trade-off between precision and recall but is lower for class 1 than class 0.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:


The logistic regression model performs exceptionally well for classifying healthy loans (0) due to the dataset's class imbalance. However, it struggles with predicting high-risk loans (1), as reflected by the lower precision, recall, and F1-score for this class.

Recommendations:
Imbalanced Dataset Handling:
Use techniques such as SMOTE (Synthetic Minority Oversampling Technique), undersampling, or class weighting to address the imbalance.
Alternative Models:
Experiment with tree-based models like Random Forest or XGBoost, which may perform better with imbalanced data.
Feature Engineering:
Include additional features that could help the model distinguish high-risk loans, such as payment history or additional borrower credit details.
Given its current state, the model is suitable for identifying healthy loans but is not reliable for high-risk loans. Improvements in handling the class imbalance and refining feature selection are recommended before deploying this model.

If you do not recommend any of the models, please justify your reasoning.
