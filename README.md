# Telecom Churn Prediction Model

## Project Overview
The goal of this project is to develop a machine learning model that predicts customer churn for Interconnect, a telecommunications company, using various machine learning algorithms.

## Data
We were provided with four CSV files containing:

- `contract.csv` -> Contract Information: Details about customer contracts.
- `personal.csv` -> Personal Information: Demographic data of customers.
- `internet.csv` -> Internet Services: Information on internet services per contract.
- `phone.csv` -> Phone Services: Information on phone services per contract.

## Steps Taken
### Data Loading and Cleaning:

- Loaded the CSV files.
- Cleaned the data and handled null values.
- Joined the datasets to create a comprehensive dataset.
- Feature Engineering:

- Created a new column "churn" to represent our target variable.
- Scaled continuous variables.
- One-hot encoded categorical features.

### Data Preparation:

- Split the data into training and validation datasets.
- Applied SMOTE to address class imbalance.
  
### Modeling:

- Applied various algorithms: XGBoost, RandomForestClassifier, LogisticRegression.
- Use of CVGridSearch to get the best hyperparameters for model tuning.
- Evaluated models using ROC-AUC curves and F1 metrics.
  
## Results
The best model was XGBoost with an F1 score of 0.84 and ROC-AUC of 0.92. LogisticRegressor and RandomForestClassifier came close with F1 0.82 and 0.84 and ROC-AUC 0.90 and 0.92 respectively. RFC performed a little worse on class 0 F1, scoring 0.83.

## Conclusion
This project demonstrates the application of data cleaning, feature engineering, and machine learning techniques to predict customer churn in the telecommunications industry. The XGBoost model provided the best performance, indicating its suitability for this type of predictive analysis. XGBoost turned out to be the superior model, requiring less time to setup compared to hyperparameter tuning of RFC.
