# credit-risk-classification

## Overview of the Analysis

The main goal of this analysis is to predict whether a loan is deemed high-risk or healthy using a supervised machine learning approach, specifically a Logistic Regression model. The dataset consists of 77,536 records in a CSV file, each containing information related to the loan, such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and loan status.

The dependent variable (loan_status) is utilized as the target variable (y), with 75,036 instances labelled as 0 (healthy) and 2,500 labelled as 1 (high risk). The independent variables (X values) include the remaining columns mentioned above.

After defining the y and X variables, the data is split into training and testing sets using the train_test_split function from sci-kit-learn. A Logistic Regression model is then fitted to the training set with a random state of 1.

Subsequently, predictions are made on the testing set, and the results are stored in a Pandas data frame. To evaluate the model's performance, a confusion matrix and a classification report are generated, providing insights into the accuracy of predictions.

## Results

Upon reviewing the overall model performance, it demonstrates a 99% accuracy in predicting both 0 and 1 labels. However, a deeper analysis reveals variations when examining each label individually.

The F1 score for the 0 labels is 100%, indicating perfect precision and recall scores. In contrast, the F1 score for the 1 label is 88%, with precision at 87% and recall at 89%. This discrepancy is likely influenced by the significantly lower number of records for the 1 label (2,500) compared to the 0 label (75,036).

## Summary

The Logistic Regression model proves to be a robust tool for accurately predicting whether a loan is healthy or high risk for borrowers. However, the existing data imbalance between healthy and high-risk loans may impact the model's effectiveness, particularly for high-risk predictions. To enhance the model's performance, the dataset would benefit from an increase in high-risk loan data points.

Additionally, it's important to note that the model provides a binary response, lacking the ability to distinguish between different levels of high risk. Further refinements could be explored to capture nuances within the high-risk category for a more detailed assessment.
