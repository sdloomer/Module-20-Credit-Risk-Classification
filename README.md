# Module-20-Credit-Risk-Classification

To begin, we need to split the data into training and testing sets, using train_test_split. Then we can fit and predict a logistic regression model using the X and y training data sets, and then generate an accuracy score, confusion matrix, and classification report. This initial model seems to be able to predict both healthy and high-risk loans fairly well, with an overall accuracy score of 99%.

However, the data sets are not balanced and this may skew predictions; using RandomOverSampler, we are able to resample the training data so that both X and y have an equal number of data points to use. Using the same method as above with Logistic Regression, we can generate another model using the resampled data and generate another accuracy score, confusion matrix, and classification report. This model has a slightly better accuracy for predicting high-risk loans (from 88% to 91%), and its overall accuracy is still at 99%.

In conclusion, resampling the data may increase precision and accuracy, and should be suggested for use in all models.