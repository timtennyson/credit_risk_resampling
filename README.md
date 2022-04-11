# Credit Risk Resampling

This application uses a Logistic Regression training/test model to analyze sample data for loans issued in order to predict future outcomes for future loan applications. The application then backtests results for both the original sample data and for a random oversampling to figure out which will produce the highest level of accuracy for the lender when assessing credit risk.

## Technologies
[Python3.7](https://www.python.org/)

[Jupyter Lab](https://jupyter.org/)

[Pandas](https://pandas.pydata.org)

[Pathlib](https://docs.python.org/3/library/pathlib.html) 

[sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)

[imblearn](https://imbalanced-learn.org/stable/)



## Installation guide
Install the required libraries above in Terminal and open the application files in Jupyter Lab

## Part 1)-- 

### Step 1: Split the Data into Training and Testing Sets

First we convert the csv file in the /Resources folder into a pandas dataframe using the pd.read_csv function and split the data into training and testing sets. The training set is used to create the prediction model and the testing set is used to backtest the accuracy of the model created.

### Step 2: Create a Logistic Regression Model with the Original Data

Our application then creates a logistic regression model using the training data (X_train, y_train).

### Step 3: Predict a Logistic Regression Model with Resampled Training Data

Next, we take a random oversampling of the data to see how well the model performs with a larger sample size and compare it to the original results.

## Overview of the Analysis

* The purpose of this analysis is to review loan applications for credit risk.
* Parameters for each application are as follows: loan size, interest rate, borrower income, debt-to-income-ratio, number of accounts, total debt, derogatory marks, and loan status
* The variable the model intends to predict is value_count for 'loan status'. If the variable has an assigned value of '1', it is a high-risk loan. If it has an assigned value of '0', it is a low-risk loan.
* A logistic regression model was created using training data and test data to analyze a sample of applications with known results in order to predict the outcome of future applications with the highest degree of accuracy possible.
* Results are provided for both the original sample and for a random oversampling of the data.

# Reported Results:

* Machine Learning Model 1:
  * Model 1 uses only the sampled data. It scores as follows: Balanced Accuracy= 95.2% Avg Precision= 99% and Avg Recall= 99%
  * This model correctly identifies low-risk loan applications (loan status=0) 100% of the time, and high risk loan applications (loan status=1) 91% of the time.



* Machine Learning Model 2:
  * Model 2 uses the sampled data with a random oversampling. It scores as follows: Balanced Accuracy= 99.3% Avg Precision= 99% and Avg Recall= 99%
  * This model also correctly identifies low_risk loan applications 100% of the time, but the percentage of accurate predictions for high-risk loans goes up to 99%



### Summary

While both models provide fairly reliable analysis, the second model with the random oversampling provides an 8% higher degree of accuracy for prediction of high-risk loans, which over a high volume of loan applications adds up to a significant amount of savings if the model is utilized. The results are backtested using the test data.

It is more important for this application to identify the higher risk applications ('1s') as they are much more likely to default on a loan.


Tim Tennyson 
<ttennyson.xyz@gmail.com>

License: Open source, free distribution/reproduction
