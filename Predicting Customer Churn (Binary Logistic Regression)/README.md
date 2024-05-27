#Solving a classification problem - "The customer will get churned or not?"

*Dataset* : ecommerce_transaction.xlsx (Attached to the repo)

This dataset provides insights into customer behavior, retention, engagement with email campaigns, purchasing patterns, and service preferences. It can be used to create a model which can predict whether a customer will be retained or not!! 

Classification problems are an important category of problems in analytics in which the outcome variable or response variable (Y) takes discrete values. Primary objective of a classification model is to predict the probability of an observation belonging to a class, known as class probability. 
Classification problems may have binary or multiple outcomes or classes. Binary outcomes are called binary classification and multiple outcomes are called multinomial classification. I am dealing with the binary classification here, and will try to predict whether the customer will be retained or not!! 

## Pre-processing and Modelling

Our target variable is "retained" column, which says the customer is retained or not! And we'll use this data to train our logit model. The data type of the "retained" column is categorical in nature, so I have converted the column in String data type, as KNIME understands String for building logit model.

![image](https://github.com/Subham-here/KNIME-Workflows/assets/170924246/9a5a5e69-8798-4e64-8024-d39b09dec69c)

After partitioning the dataset into Train-Test (70:30), the model has been created with the trained dataset and later the result has been matched with the results of the test dataset to check the performance of the model.

![image](https://github.com/Subham-here/KNIME-Workflows/assets/170924246/da0ade7d-d7f1-4b7a-95df-f6f34317ae84)

The target column is set to "retained" and the reference category is set to '0' for the same. I have Taken the variables 'esent', 'eclickrate', 'avgorder', 'ordfreq' and 'doorstep' into cosideration and checked the score of the model. Here I have considered the metric 'Precision' for the evaluation, because we want to measure greater number of True Positives in our case. 

![image](https://github.com/Subham-here/KNIME-Workflows/assets/170924246/2d27510d-dd99-4920-95df-099a72c0b39d)

P.S We can do trial and error with the variables taken into consideration to find the greater performance of the model.










