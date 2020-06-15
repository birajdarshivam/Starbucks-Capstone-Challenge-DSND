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

[MEDIUM Blog](https://medium.com/@birajdarshivam11/predict-effective-offers-for-starbucks-app-users-74c68649fac7?sk=3293a9e18a06a41a220ac58b53caf862)

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
This is the part of Udacity Data Science capstone project. In this project I am trying to find out some answers to my questions :
  1. What are the main drivers of an effective offer on the Starbucks app?
  2. Could the data provided, namely offer characteristics and user demographics, predict whether a user would take up an offer?
And the objective of this project is trying to find how Starbucks customers use the app, and how well is the current offers system. more importantly, to find patterns and show when and where to give the specific offer to a specific customer.
