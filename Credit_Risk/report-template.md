# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
- the purpose I assume is to predict the loan facilites that are likely to default in our sample data and ones that aren't at risk, using borrower information.

* Explain what financial information the data was on, and what you needed to predict.
- The data provided was the size of the loan and its corresponding interest rate. 
- The borrowers' income and the reported number of accounts each have.
- It also shows how may times the borrowers has had deragotory marks, which could be failure to make a payment.
- total debt for the borrower is also given. Which must likely be split among the other number of accounts.
- Loan status is 0 for good standing, 1 that is at default or the client is well behind on its payments.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
- I tried to predict the loan status using all the other information in the given columns.

* Describe the stages of the machine learning process you went through as part of this analysis.
- first assigned y to the loan status and then removed it from the testing/training data.
- then split the test data from the training data.
- then created a regression model by fitting training data in it.
- finally made predictions using the regression model on the testing data.
- I then used a confusion matrix and a classification report to draw an analysis and conclusions.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
- refer to my above answer to the previous bullet point, last three line items to be specific.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
-     precision    recall  f1-score   support

  0       1.00      0.99      1.00     18765
  1       0.85      0.91      0.88       619

  accuracy                           0.99     19384
  macro avg       0.92      0.95      0.94     19384
 weighted avg       0.99      0.99      0.99     19384 



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
-     precision    recall  f1-score   support
   0       1.00      1.00      1.00     56271
   1       0.86      0.90      0.88      1881

  accuracy                           0.99     58152
  macro avg       0.93      0.95      0.94     58152
  weighted avg       0.99      0.99      0.99     58152 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
- Model 2 (training) performs better than Model 1 (testing) for predicting accounts at no risk of default "0".
- both models do a similar job predicting the probability that an account will default.
- Presision was better in the first model and recall was relatively the same for both.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
- Predicting which borrowers are likely to default on their obligations is the far more important varible to predict here '1'.
- This is because anyone that is owed money would like to know who is likely to not pay you back, in simple words.
- these models predicted that ~90% of the time.

If you do not recommend any of the models, please justify your reasoning.
- I recommend both. Borrowers marked by the models as a '1' should be taken seriously.
