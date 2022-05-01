# Customer-Churn-Machine-Learning

## Scope

- Predictive analytics
- Machine learning
- Logisrtic Regression
- Receiver Operating Characteristic curve

## About the dataset
    Dataset: https://www.kaggle.com/blastchar/telco-customer-churn\n
    
From kaggle, Telco customer churn dataset is one in which each row represents a customer, each column contains customer’s attributes.
The data set includes information about:

Customers who left within the last month – the column is called Churn.

Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies.

Customer account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges
Demographic info about customers – gender, age range, and if they have partners and dependents.

## Methodology

In this [project](https://github.com/gregoryoffodum/Customer-Churn-Machine-Learning/blob/main/Customer%20Churn.ipynb), the Logistic Regression model was trained, validated and tested with 60%, 20% and 20% of the dataset respectively. Thew following were explored extensively:

- Exploratory data preparation and cleaning
- Feature importance analysis
  - Churn rate, risk ratio, correlation, one hot encoding using DictVectorizer
- Logistic regression model
- Accuracy metrics
  - Precision and recall
  - True positive and negative rates
  - Confusion matrix
  - ROC curve
  - AUC
  - K-Fold Validation

## Results

- AUC score for the final model was *0.86*. It is worth noting that a dummy model predicts at 74% accuracy due to a classification imbalance in target values. 
- A good strategy would be to send emails for promotional discounts to customers predicted to churn (leave). The confusion matrix shows we predict more than 80% of customer behaviour correctly, however, we spend money to give promotional discounts to 112 (false positive) customers we shouldn't have, and not give 167 (false negative) customers we should have (and will probably lose them).

## Deployment

- The model was [saved](https://github.com/gregoryoffodum/Customer-Churn-Machine-Learning/blob/main/model_C%3D1.0.bin), [tested](https://github.com/gregoryoffodum/Customer-Churn-Machine-Learning/blob/main/predict_test.py) and served using [Flask](https://github.com/gregoryoffodum/Customer-Churn-Machine-Learning/blob/main/predict.py); and a python virtual environment, Pipenv; which therefater can be managed in docker and deployed to a cloud environemnt.




