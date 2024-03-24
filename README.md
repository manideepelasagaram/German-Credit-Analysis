# German-Credit-Analysis
## Introduction
The "German Credit Project" data source available at https://www.dataminingbook.com/content/datasets-download-1st-edition provides comprehensive data on the credit risk of individuals. This data can be used to determine whether a person represents good or bad credit risk. Using this data source provides easier access to information that would otherwise have to be compiled manually from multiple sources and, in some cases, even locked behind a paywall. The data includes information on borrowers, including personal data, employment history, credit history, and other financial metrics. These can be used as predictor variables in a model to predict the credit risk of individuals and make informed decisions.
There are two types of risks associated with the bank’s decision:
• If the applicant is likely to repay the loan i.e., having a good credit risk, then not approving the loan to the person results in a loss of business to the bank.
• If the applicant is not likely to repay the loan i.e., having a bad credit risk, then approving the loan to the person results in a financial loss to the bank.

## Main Chapter
## 1. Develop Understanding
• Our project goal is to develop a credit risk assessment model that analyzes a set of attributes of an individual and accurately classifies them as either good or bad credit risk.
Final Project – German Credit
• The model will use a combination of statistical and machine learning techniques to identify the most important factors that influence credit risk and provide insights to help lenders make informed decisions about lending to potential borrowers.
• The outcome of the German Credit Project is to predict whether a person has a good or bad credit risk based on a set of attributes. Additionally, we aim to identify the most important attributes that contribute to good or bad credit risk and provide insights to financial institutions to make informed decisions.
• Our analysis of the German Credit Project can be an ongoing effort, with more real-time data available to collect from financial transactions and credit history. We believe that this will be able to improve our accuracy as more data is collected and analyzed over time. The goal is to create a model that can accurately predict whether an individual has good or bad credit risk based on a set of attributes, and to continue refining and updating the model as new data becomes available.

## 2. Explore, Clean, and Preprocess Data; Reduce Data Dimension
• Applicants with good credit have a great possibility to repay financial obligations. Applicants with bad credit have a high possibility of defaulting.
• The German Credit dataset contains information about 1000 customers. By using this data, and developing & assessing various models, the bank can decide on a prospective applicant, whether to go ahead with the loan approval or not.

## 3. Determine the Data Mining Task
Details about a few Fields from the given dataset,
• The OBS column has been dropped, it is Observation Number(it is like a serial no.)
• The Fields ‘NEW_CAR, USED_CAR, FURNITURE, RADIO/TV, EDUCATION, and
RETRAINING belong to the Purpose of taking a loan. In this dataset, we can see them
as dummies created to take a loan.
• The field of HISTORY has 4 levels, these are classified based on the past credit History
of a person.
• The field SA V_ACCT has 5 levels; these are classified based on the average balance in
a savings account.
• The field CHK_ACCT has 4 levels; these are classified based on the status of the
checking account.
• The field EMPLOYMENT has 5 levels, these are classified based on the number of
years of employment a person has.
• The field JOB has 4 levels, these are classified based on the nature of the JOB
• Our variable of interest is the RESPONSE field, which holds the credit rating of a
customer(person) (1-Good Credit Rating, 0-Bad Credit Rating)


## 4. Partition Data
To avoid an overfitting situation, we use partitions to develop our data by using train_test_split with a test size of 40%. While we will split the data into ‘Training’ and ‘Validation’, the Training partition contains 60% of the data to develop the model, while Validation contains 40% of the data to evaluate new data performance.

## 5. Techniques
We will be using logistic regression and classification tree methods to analyze the outcome variables, which are classifications and not numerical data. We will first convert the Good/bad classifications into binary variables to do this.

## 6. Algorithm and Measures
K-NN MODEL:
k-nearest-neighbors algorithm can be used for classification (of a categorical outcome) or prediction (of a numerical outcome).
The following shows the accuracy metrics of a regression model, including results from both the training and validation sets.

## 7. Algorithm and Measures K-NN MODEL:
k-nearest-neighbors algorithm can be used for classification (of a categorical outcome) or prediction (of a numerical outcome).
The following shows the accuracy metrics of a regression model, including results from both the training and validation sets.

## 8. Grid Search 
The improved parameters reported are {'max_depth': 5, 'min_impurity_decrease': 0, 'min_samples_split': 28}. These are likely the hyperparameters that were found to yield the best performance on the validation set during the grid search.

## 9. Logistic Regression – Good/Bad Prediction
Logistic Regression models for binary response variables allow us to estimate the probability of outcome-which is to classify whether s person has a good or bad credit risk based on a set of attributes.
For logistic regression, we can use maximum likelihood.
It does not assume a linear relationship between dependent and independent variables. However, it assumes a linear relationship between the link function and independent variables in the logit model.
For logistic regression: The predicted Y lies within the 0 and 1 range.
To interpret logistic regression results, we first transform the coefficients to odds ratios by raising e - or Euler’s constant - to the coefficients.
The intercept and regression coefficients obtained based on 13 predictors used to build Logistic Regression Model are as below.

## Conclusion
Comparing the predictive accuracy in your validation data for all the models developed above are given below.
K-NN MODEL:
The algorithm works by finding the k-nearest neighbors to a given data point in the training data and using their labels to predict the label of the new data point.
 
Final Project – German Credit
We have evaluated the algorithm's predictive accuracy on the German Credit dataset using two different values of k, i.e., k=3 and k=11. We have achieved an accuracy of 72.75% for k=3 and an accuracy of 76% for k=11.
This means that when k=11, the algorithm can correctly predict the class label of a new data point 76% of the time. The higher accuracy score suggests that the algorithm's performance improved when we increased the value of k from 3 to 11.
Classification TREE:
By implementing the Decision tree, we can conclude that our model has an accuracy of 74.25% in predicting a person's credit risk as either good or bad. This accuracy indicates that our model is capable of making relatively accurate predictions and can be used as a reliable tool to assess the creditworthiness of a person.
Grid search:
Our optimization of hyperparameters resulted in an enhanced accuracy of 75.75% for predicting credit risk using the Grid Search tree. This improvement indicates that our efforts have led to a more reliable model for assessing creditworthiness. With increased confidence in the predictions made by the model, financial institutions can use it to make informed decisions about granting loans and other credit products.
Logistic Regression:
Based on our analysis using the Logistic Regression model, we were able to achieve an overall predictive accuracy of 77% at a probability threshold of 0.5. This indicates that the model can
   
Final Project – German Credit
accurately classify individuals as either having good or bad credit risk based on their attributes. However, it's worth noting that the accuracy of the model varies depending on the probability threshold used. For instance, at a probability threshold of 0.3, we achieved an accuracy of 73.5%. We can continue to refine and optimize the model to improve its overall accuracy and ensure that it can effectively predict credit risk for individuals.
Comparing the predictive accuracy in your validation data for all the models developed above are given below:
• The Predictive Accuracy we got from k-NN,
• At K=3, we got an accuracy of 72.75%
• AT K=11, we have got the Accuracy of 76%
• The Predictive Accuracy we got from the default Decision tree is 74.25%
• The Predictive Accuracy we got from the Pruned tree is 75.75%
• The Predictive accuracy we have got from Logistic regression is 75.94%
The Logistic regression model has given the highest accuracy when compared to KNN and Trees.
Summary
The predictors we would use based on predictive accuracy and the analysis above:
We will identify significant predictor columns by considering those with low P-values (p<=0.05). Below are some examples of these columns.
• CHK_ACCT – Checking account status with the Bank.

Final Project – German Credit
• HISTORY – Credit History
• SAV_ACCT – Avg Balance in Savings Account
• INSTALL_RATE – Installment rate %
• OTHER_INSTALL – Other installments if any
• FOREIGN – Either Foreign worker or not
• TELEPHONE – Applicant has a phone number in this name.
We can consider these important attributes from this model, as these variables play an important role in classifying whether a person has a Bad Credit Rating or Good Credit Rating.
