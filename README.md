# Starbucks-Capstone-Challenge-DSND


## 1. Libraries :
This project was written in Python, using Jupyter Notebook on Anaconda. The relevant Python packages for this project are as follows:

pandas

numpy

math

json

sklearn.model_selection (train_test_split module)

sklearn.preprocessing (StandardScaler, PolynomialFeatures)

from sklearn.tree (DecisionTreeClassifier,DecisionTreeRegressor)

sklearn.ensemble (RandomForestClassifier)

sklearn.metrics (mean_squared_error,classification_report)

sklearn.linear_model (Ridge)

time

sklearn.model_selection (GridSearchCV)

matplotlib

[MEDIUM Blog](https://medium.com/@birajdarshivam11/starbucks-capstone-challenge-dsnd-96d6902c9e61?sk=75a8a38db696e23ac93f9c41840b8350)

![](Starbucks1.png)

## 2. JSON Files :
  1. portfolio.json
  2. profile.json
  3. transcript.json
  
  The data is contained in three files:

portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
profile.json - demographic data for each customer
transcript.json - records for transactions, offers received, offers viewed, and offers completed
Here is the schema and explanation of each variable in the files:

### portfolio.json

  id (string) - offer id
  offer_type (string) - type of offer ie BOGO, discount, informational
  difficulty (int) - minimum required spend to complete an offer
  reward (int) - reward given for completing an offer
  duration (int) - time for offer to be open, in days
  channels (list of strings)
  
### profile.json

  age (int) - age of the customer
  became_member_on (int) - date when customer created an app account
  gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
  id (str) - customer id
  income (float) - customer's income
  
### transcript.json

  event (str) - record description (ie transaction, offer received, offer viewed, etc.)
  person (str) - customer id
  time (int) - time in hours since start of test. The data begins at time t=0
  value - (dict of strings) - either an offer id or transaction amount depending on the record
  
## 3. Project Motivation :
The goal of this project is to best determine which kind of offers to send to each customer demographics based on their response to the previously sent offers so that different machine learning models can be built to predict whether a customer will respond to an offer.
The following steps will be taken to build our model.
1. Clean and transform the data as needed for modeling
2. Train a classifier which will predict customers response

The objective of this project is trying to find how Starbucks customers use the app, and by using this data we want to give an offer for specific customers of their buying habits. How well is the current offers system? more importantly, to find patterns and show when and where to give the specific offer to a specific customer. For example, A user could receive a discount offer on buy 10 dollars get 2 off on Monday. The offer is valid for 10 days from receipt. If the customer accumulates at least 10 dollars in purchases during the validity period, the customer completes the offer.
