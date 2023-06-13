# credit-risk-classification
UPenn Data Bootcamp Module 20 Assignment

* Split the Data into Training and Testing Sets
  * Read the lending_data.csv data into a Pandas DataFrame.
  * Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
  * Split the data into training and testing datasets by using train_test_split.

* Create a Logistic Regression Model with the Original Data
  * Fit a logistic regression model by using the training data (X_train and y_train).
  * Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
  * Evaluate the model’s performance by doing the following:
    * Calculate the accuracy score of the model.
    * Generate a confusion matrix.
    * Print the classification report.
  * Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

* Write a Credit Risk Report

# Credit Report
* ## Overview
This analysis is to determine the creditworthiness of borrowers based off of data from previous lending activity of a peer-to-peer loan company. From the company we are given data on loan amount, interest rate, borrower income, etc. This dataframe also included a column on 'loan_staus' which is indicated with a 0 or a 1, based on if the loan was healthy or was at risk of defaulting, respectively. From this, we are asked to predict whether or not the borrower is a high risk borrower, indicated with a '1', or a creditworthy borrower, indicated with a '0'. 
Firstly, we separated the label column of 'loan_status', which will be our y variable, from the rest of the dataframe which will serve as our X variable. From this, we split the data into testing and training datasets. We can now instantiate a logistic regressor, using LogisticRegression from the SciKit Learn Python package, where we will fit it to our training data and then create predictions based on the testing data. We can then evaluate the results based on accuracy, the resulting confusion matrix, and the classification report. 
After we have found this, we decided to resample the data, using RandomOverSampler from the Imbalanced-Learn library. We then perform logistic regression on the resampled data, and make predictions, as similar to before. Then we calculated the reports as well. 

* ## Results
Machine Learning Model 1:
* Balanced Accuracy Score: 95% 
* Precision [0]: 100%
* Precision [1]: 85%
* Recall Score [0]: 0.99
* Recall Score [1] : 0.91 

Machine Learning Model 2:
* Balanced Accuracy Score: 99% 
* Precision [0]: 100%
* Precision [1]: 84%
* Recall Score [0]: 0.99
* Recall Score [1]: 0.99

* ## Summary
From this analysis, I would recommend the second machine learning model. I would recommend this model over the first model because of the increased balanced accuracy score. While both are good, relative to each other the second model is better. I would also pick the second model due to the high recall scores for both outputs, putting it at a significant advantage over the first model, which would ensure less false positives, specifically looking at the high risk borrowers. Since the company is especially concerned about predicting trustworthy people incorrectly, it is important that false positives are minimal. Since the recall score for both models are the same, which will not affect that concern, then choosing the higher balance accuracy and better recall scores for both would be the better choice. 
