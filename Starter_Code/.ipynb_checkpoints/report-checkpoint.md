# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The purpose of this analysis is to review historical lending activity and create a machine learning model that can identify whether a loan is healthy or risky. The financial data includes many features including loan size, interest rate, debt-to-income ratio, etc (7 features total). Using the value_counts() function we can see we have about 77500 examples to use in our ML model. The data is very imbalanced, there are 75000 healthy loans compared to only 2500 risky loans. Logistic Regression was chosen as the training algorithm for our supervised learning process because we are concerned with a binary outcome. Features are seperated from targets and data is split into training and testing sets. Next we model, fit, and predict. Another ML analysis is created but first the data is balanced using random over-sampling. Random instances of risky loans are duplicated from the training data. The training data now has equal amounts of healthy loans and risky loans (about 56000 of each in the training data). 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
        * Balanced Accuracy Score: 0.952
        * Precision for Healthy Loans: 1.00
        * Recall for Healthy Loans: 0.99
        * Precision for High-Risk Loans: 0.85
        * Recall for High-Risk Loans: 0.91

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
        * Balanced Accuracy Score: 0.994
        * Precision for Healthy Loans: 1.00
        * Recall for Healthy Loans: 0.99
        * Precision for High-Risk Loans: 0.84
        * Recall for High-Risk Loans: 0.99
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Machine Learning Model 2 performs the best overall. Healthy loan accuracy, precision, and recall are identical to ML Model 2. ML Model 2 has a higher balanced accuracy score. Risky loan precision is only 1% lower (0.84 instead of 0.85). However, recall for high-risk loans is much higher (0.99 instead of 0.91). In summary, high-risk loans incorrectly classified as healthy loans were decreased, while healthy loans incorrectly classified as high-risk loans barely increased. If NOT missing out on loans is more important than NOT taking risky loans you may choose Machine Learning Model 1. But probably not. ML Model 1 takes on 24 more healthy loans while taking on 52 more risky loans. 
