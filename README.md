# Credit Risk Analysis Report

  

## Overview

My goal is to create a *machine learning model* for the bank stakeholders, to accurately predict if a loan application is high risk.

Using data of applicants as features to determine the label of high-risk, a linear regression model was used.

The **Supervised Machine Learning** method was used since we are able to note the features and determine an outcome.

## Variables Used

 - Loan size
 - Interest rate
 - Borrower income
 - Debt to income
 - Number of accounts
 - Derogatory marks
 - Total debt
 - Loan status

  

## Process

  

1️⃣Split the data into training and testing sets

* Read the `lending_data.csv` data from the `Resources` folder into a Pandas DataFrame.

* Create the labels set (`y`) from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.

* Check the balance of the labels variable (`y`) by using the `value_counts` function.

* Split the data into training and testing datasets by using `train_test_split`.

2️⃣Create a Logistic Regression Model with the Original Data

* Fit a logistic regression model by using the training data (`X_train` and `y_train`).

* Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.

3️⃣ Evaluate the model’s performance by doing the following:

  

* Calculate the accuracy score of the model.

* Generate a confusion matrix.

* Print the classification report.

4️⃣Predict a Logistic Regression Model with resampled training data.

* Use the `RandomOverSampler` module from the imbalanced-learn library to resample the data. Be sure to confirm that the labels have an equal number of data points.

* Use the `LogisticRegression` classifier and the resampled data to fit the model and make predictions.

5️⃣Evaluate the model’s performance by doing the following:

  

* Calculate the accuracy score of the model.

  

* Generate a confusion matrix.

  

* Print the classification report.

  

## Results from the Machine Learning Model

  

Below is a description of the accuracy scores and the precision and recall scores of all machine learning models.

  

### Linear Regression Model:

  

**Healthy Loan Scores**

  

 - Precision: 1.00
 - Recall: 0.99
 - F1-score: 1.00
 - Support: 18765

  

**Risky Loan Scores**

 - Precision: 0.85
 - Recall: 0.91
 - F1-score: 0.88
 - Support: 619

  

### Oversampled Model:

  

**Healthy Loan Scores**

  

 - Precision: 1.00
 - Recall: 0.99
 - F1-score: 1.00
 - Support: 18765

  

**Risky Loan**

 - Precision: 0.84
 - Recall: 0.99
 - F1-score: 0.91
 - Support: 619

  

# Summary

  

- Both models perform very strongly when predicting healthy loans. 
- Using the resampled data on the second model, the accuracy and recall greatly improved to nearly perfect scores. 
- Precision remains an issue with both models, staying at 85%.
- Since both models correctly predict healthy loans, it is convenient to have a model that correctly classifies more high-risk loans. 
- This is why I would recommend to use Model 2.

# References

Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
