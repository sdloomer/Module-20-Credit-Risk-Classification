# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge.

* Explain the purpose of the analysis.
  * The purpose of this analysis is to determine whether using different resampling techniques has any effect on logistic regression models for the same set of data. In the real world, it is good practice to split the data in different ways to make sure results aren't skewed. 

* Explain what financial information the data was on, and what you needed to predict.
  * The financial information used notes lending data of various customers; columns include the size of the loan, total amount of debt, and the loan status of a customer. This model will be used to predict whether a customer will default on a loan or not, depending on the different features provided.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
  * The target values, or "loan status" that we are trying to predict were checked using the value_counts() method; these numbers show how many customers have defaulted (denoted by "1") or not ("0").

* Describe the stages of the machine learning process you went through as part of this analysis.
  * To begin, we first needed to read in the data and separate in into labels and features (X and y, where y is the loan_status column). Then, using the train_test_split method on the separated data, we further separated it into training and testing bins. From here, we can now fit a logistic regression model on the training data and use this to make predictions on the testing data. By using an accuracy score and confusion matrix, we are able to determine whether the model is sufficient. The same steps were used with a different resampling method (RandomOverSampler) to bin the y data evenly.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Accuracy: 0.95
  * Precision: 
    * 0: 1.00
    * 1: 0.85
  * Recall: 
    * 0: 0.99
    * 1: 0.91



* Machine Learning Model 2:
  * Accuracy: 0.99
  * Precision: 
    * 0: 1.00
    * 1: 0.84
  * Recall: 
    * 0: 0.99
    * 1: 0.99

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
  * The second model using an even count of y (loan_status) data seems to perform the best, as its overall accuracy jumped 4% from the original model, and its recall for defaults also jumped about 8%. Precision for defaults seemed to have dropped about 1% from the original model, however.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  * For many companies, it is decidedly more important to predict those customers who will default ("1") on their loans, as they are a greater risk, so perhaps the second model might not be sufficient to make those predictions, based on its lower precision for that category. However, overall accuracy might be more defining to a model, and with a 99% accuracy, model 2 seems to be the better choice.