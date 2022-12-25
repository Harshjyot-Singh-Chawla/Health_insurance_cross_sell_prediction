# HEALTH-INSURANCE-CROSS-SELL-PREDICTION
A model to predict whether a customer already owning a health insurance would be interested in Vehicle Insurance or not
# Project Summary :
### Problem Statement :
The task is to use existing Health and Vehicle Insurance Customer Data to predict whether the any new Customers are open to purchasing Vehicle Insurance from this company .

### About the Data :
We have the data of existing Health Insurance Customers , this Data includes 12 relevant data points such as age, gender, sales channel data, vehicle ownership data. And most importantly , the target variable : whether the customer has vehicle insurance or not . The Data is available for 390K existing customers .

### Approach taken :
The task was divided into 2 main parts : 1.Statistical Analysis over the dataset to discover relationships between each feature and the target variable . So that this relationship information can be used by the management in making better Business decisions 2.Creating a Machine Learning Pipeline , that can take in the data of any new customer and predict whether they will be interested in vehicle insurance . It was required to kepp this pipeline modular , such that it can be retrained often when new data is collected

### Technical Details for ML : We trained 5 Different Algorithms
( Logistic Regression , K-Nearest Neighbors , Random Forest , XGBoost and CatBoost ) We used GridSearchCV and BayesSearchCV for HyperParameter Tuning Comparing both F1 and AUC-ROC Score , we can see that Random Forrest and XGBoost model performs the best . Best AUC-ROC = 0.86 , Best F1=0.44

### Conclusions : Insights from exploring the Data :
* Customers of age between 30 and 70 are more likely to buy insurance. 
* Customers with Driving Licence have higher chance of buying Insurance. 
* Customers with Vehicle Damage are more likely to buy insurance. 
* Customers with Vehicle age between 1 and 2 years are more likely to interested. 
* Customer who are not insured previously are more likely to be interested.

## Python Libraries used
Datawrangling :

* Numpy
* Pandas
For Graphing :

* Matplotib
* Seaborn
Machine learning :

* Scikit-Learn
* SK-Opt
* XGBoost
* CatBoost
Miscellaneous :

* Google colab tools
# Getting Started
1. Clone this repo (for help see this tutorial).
2. Raw Data is being kept here within GDrive
3. Data processing/transformation scripts are being kept [here](Repo folder containing data processing scripts/notebooks)

# The Structure of the main IPYNB notebook :
* About this Project

* Problem Statement

*Buisness Goal

* Approach Taken in this Project

* Understanding the given Data
* Initial Code : Initliaing the Data and Modules

Installing and Importing Libraries

Import Dataset and Initial Data Checks
* Data Preparation and Cleaning

*Exploratory Data Analysis

Initial Macro-Level Data Analysis

Variable wise EDA
1. Target Variable (Response)
2. Age variable
3. Annual_Premium
4. Gender variable
5. Driving License
6. Previously Insured
7. Vehicle Age
8. Vechicle damage
9. Vintage
10. Region Code
11. Policy Sales Channel

Correlation Plot for Numeric Features

* Data Preprocessing and Feature Engineering

Outlier Treatment in feature : Annual_Premium
Label Encoding
Target Mean Encoding
Cleaned Data Exporting
Building Prediction Systems using ML Models

Import cleaned final data

Classifier Performance Reporting Function

* Overfitting Underfitting Debugging Notes
* Metrics to be used during HyperParameter
* Random Forrest Specific Cutom Defined Metrics
* Function Definations for Analytics report generation

Logistic Regression Classifier Algorithm:

* LR Classifier Generator Function:
* LR Hyper Parameter Tuning : GridSearch
* Final Logistic Regression Training run

K Nearest Neighbours Classifier Algorithm:

* Default Parameters : KNeighborsClassifier
* KNN Model Generator Funciton
* KNN Hyper Parameter Tuning : GridSearch
* Final KNN Training run

Random Forrests of Decsision Trees:

* Default Parameters : RandomForestClassifier
* Base Estimator Generator Function
* HyperParameter tuning using GridSearchCV
* Final Training Run
* Gradient Boosted Trees using XGBoost Library

XGBoost algorithn training and tuning notes:

* XGBoost Estimator Instance Generator Function
* HyperParameter tuning using BayesSearchCV
* Final Training Run for XGBoost
* Feature Importance

Categorical Gradient Boosted Trees using CatBoost Library:

* Cleaning Raw Data with Categorical Encoding
* CatBoost Estimator Instance Generator Function
* Model Evaluation
* Final Training Run for CatBoost
* Feature Importance
* Inferences and Conclusions

-What Worked? What Did Not Work?

-Future Work and More Ideas to Explore

