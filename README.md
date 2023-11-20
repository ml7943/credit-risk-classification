# credit-risk-classification —— Module 12 Report

## Overview of the Analysis

The purpose of this analysis is to evaluate credit risk using a dataset containing information about loans. 
The dataset comprises 75,036 healthy loans (label 0) and 2,500 high-risk loans (label 1). 
The analysis involved using logistic regression and oversampling to handle the imbalanced dataset.

### Purpose of the Analysis
The primary objective of this analysis is to conduct a credit risk assessment using machine learning techniques on a dataset containing financial information related to loans. 
The aim is to develop a predictive model capable of evaluating loan statuses and identifying potential high-risk loans.

### Financial Information in the Data
The dataset contains various financial attributes associated with loans, such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and the crucial target variable loan status. 
The goal is to predict the loan status, where a value of 0 indicated a healthy loan, while a value of 1 indicated a high-risk loan susceptible to default.

### Variables Being Predicted
The target variable, loan status, was the focal point of prediction. 
The dataset comprised 75,036 healthy loans labeled as 0 and 2,500 high-risk loans labeled as 1. 
The analysis aims to develop a model capable of accurately distinguishing between these two classes to effectively predict loan statuses.

### Stages of the Machine Learning Process
The analysis followed a structured approach:
1. **Data Loading and Preprocessing:** The lending_data.csv file was loaded into a Pandas DataFrame, and the data was preprocessed to separate features (X) and the target variable (y).
2. **Data Splitting:** The dataset was divided into training and testing sets using the `train_test_split` method from `sklearn.model_selection`.
3. **Model Building and Evaluation:** Logistic Regression was employed as the primary predictive model.
   The model was trained using the training data and then evaluated for performance using various evaluation metrics such as accuracy, precision, recall, F1-score, and confusion matrix.

### Machine Learning Methods Used
The primary machine learning method employed was Logistic Regression. 
Additionally, to handle the imbalance in the dataset, a RandomOverSampler from the imbalanced-learn library was used. 
This technique artificially balanced the classes in the training data by oversampling the minority class, thereby improving the model's ability to predict both healthy and high-risk loans accurately.

## Results
### Logistic Regression Model
- **Balanced Accuracy:** The logistic regression model achieved a balanced accuracy of 0.952, indicating good overall predictive performance.
- **Label 0 (Healthy Loans):** Precision, recall, and F1-score were all high at 1.00, indicating perfect performance in identifying healthy loans.
- **Label 1 (High-Risk Loans):** Precision was slightly lower at 0.86, with recall and F1-score at 0.91 and 0.88 respectively. Overall, it exhibited good performance in identifying high-risk loans.

### Logistic Regression Model with Resampled Data
- **Balanced Accuracy:** The resampled logistic regression model achieved a significantly higher balanced accuracy of 0.994, demonstrating outstanding performance in predicting both healthy and high-risk loans.
- **Label 0:** Showed excellent metrics, with precision, recall, and F1-score all high (1.00, 0.99, and 1.00 respectively), indicating precise identification of healthy loans.
- **Label 1:** While precision was slightly lower at 0.85, recall and F1-score were high at 0.99 and 0.92 respectively, showcasing strong performance in identifying high-risk loans.

## Summary
The logistic regression model, especially when utilized with resampled data, showed remarkable accuracy in predicting both healthy and high-risk loans. 
It accurately identified healthy loans with minimal misclassifications and demonstrated a high ability to recognize high-risk loans, albeit with a few false positives. 
Overall, the model exhibited exceptional accuracy and a robust capacity to handle imbalanced classes.

These results highlight the model's effectiveness in credit risk assessment. 
The detailed analysis and performance metrics suggest that the model, particularly with oversampling, is highly recommendable for the company's credit risk evaluation, 
considering its remarkable accuracy and capability to handle imbalanced datasets.

## Author and Date
- **Author:** `Mu Li`
- **Date:** `11/19/2023`
