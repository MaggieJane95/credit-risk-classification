# credit-risk-classification

# Overview of the Analysis
In this project, the task was to develop a supervised learning model to assess the creditworthiness of loan applicants using logistic regression. The dataset included various financial attributes of borrowers and their loan status, indicating whether a loan is healthy (0) or high-risk (1).

## Purpose of the Analysis
The purpose of this analysis is to predict the creditworthiness of borrowers based on historical lending data. This model helps the peer-to-peer lending services company in identifying the risk of defaulting on loans, which is crucial for making informed lending decisions and mitigating financial risks.


## Variables:
loan_status (labels, y): 0 indicates a healthy loan, and 1 indicates a high-risk loan.

Features (X): All other columns in the dataset except loan_status.

## Machine Learning Process:
Data Loading and Preprocessing: The lending_data.csv file was read into a Pandas DataFrame, with the loan_status column separated as the label (y) and the remaining columns as features (X).

Data Splitting: The data was split into training and testing sets using train_test_split with a random state of 1.

Model Training: A logistic regression model was instantiated and trained using the training data (X_train and y_train).

Model Evaluation: The model's performance was evaluated using a confusion matrix and a classification report on the testing data.

## Methods Used:
Logistic Regression (LogisticRegression from sklearn.linear_model)

## Results
## Logistic Regression Model:
## Confusion Matrix:

[[18663   102]
 [   56   563]]

## Classification Report:

              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
    macro avg       0.92      0.95      0.94     19384
    weighted avg       0.99      0.99      0.99     19384
    Accuracy: 0.99

# Precision:
Class 0: 1.00
Class 1: 0.85

# Recall:
Class 0: 0.99
Class 1: 0.91

## Summary

### Best Performing Model
The logistic regression model demonstrated outstanding performance with an overall accuracy of 99%. The model achieved a precision score of 1.00 for healthy loans and 0.85 for high-risk loans. It also had a recall score of 0.99 for healthy loans and 0.91 for high-risk loans. These metrics indicate a strong ability to correctly identify both healthy and high-risk loans.

### Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

**Healthy Loans**: The model excels in predicting healthy loans with 100% precision and 99% recall, making it highly reliable. 

**High-Risk Loans**: While the precision for high-risk loans is slightly lower at 85%, the recall is strong at 91%, indicating that the model effectively identifies most high-risk loans.


## Recommendation:
The logistic regression model is recommended for use by the company due to its high accuracy and balanced performance in predicting both healthy and high-risk loans.
This model is particularly useful in minimizing the risk of loan defaults, which is crucial for financial decision-making in lending services.
