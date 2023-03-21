# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to use different supervised machine learning models to predict whether or not a loan is healthy or at-risk based on several input variables such as:

* Loan size
* Interest rate
* Borrower income
* Debt to income ratio
* Number of accounts
* Derogatory marks
* Total debt

'0' is used to indicate a healthy loan while '1' is used to indicate an at-risk loan.  The dataset is considered 'inbalanced' because the number of healthy loans (75,000) far exceeds the number of at-risk loans (2,500).  I first ran a logistic regression analysis on the data, then used an oversampling model to attempt to correct for the imbalanced actual results.

## Results

The accuracy, precision and recall of each model is outlined below.

* Machine Learning Model 1(Logistic Regression):
  * Accuracy: .95
  * Precision:
      * 0 (healthy loan): 1.00
      * 1 (high-risk loan): .85
  * Recall
      * 0 (healthy loan): .99
      * 1 (high-risk loan):  .91

* Machine Learning Model 2 (Random Oversampling):
  * Accuracy: .99
  * Precision:
      * 0 (healthy loan): 1.00
      * 1 (high-risk loan): .84
  * Recall
      * 0 (healthy loan): .99
      * 1 (high-risk loan):  .99

## Summary

Balancing the dataset (using random oversampling) increased our recall by 8 basis points while only decreasing precision by only 1 basis point for the high-risk loan category.  Meanwhile precision and recall for the '0' (healthy loan) category stayed the same while the accuracy score increased from .95 to .99.  Therefore, we made a small sacrifice in precision for a greater increase in recall, limiting the number of False Negative outcomes.  This is important because we don't want to classify a loan as high risk if it is healthy.  Therefore, the second Machine Learning Model we used is the one I would recommend.

