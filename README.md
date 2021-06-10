# Bank-Customer-Churn-Prediction

## Project Overview 
 Customer Churning is a major concern for any industry or sector., no company wants that their user stops using their services. In this project, I focused on Bank Customers, and I used machine learning algorithms to predict either the customers exit the bank or continue to use their services. The project will help the bank by identifying the potential customers who may leave the bank. The bank can provide attractive offers to them or ask them for feedback. And If they are facing some difficulty with bank services, it can be resolved early, and we can retain the customers.

## Data
The dataset is taken from Kaggle(https://www.kaggle.com/adammaus/predicting-churn-for-bank-customers). The dataset has 10,000 records total, and it is a binary classification dataset (either customer will exit from the bank or not). There are 7963 records for customers who do no exit from the bank and 2037 records for the customer who exit from the bank. The features of the dataset are as follows:

![Feature Description Image](https://github.com/Pranjal-Soni/Bank-Customer-Churn-Prediction/blob/main/images/features_desc.JPG)

## Exploratory Data Analysis
Box plots for continous variables on the basis of target attribute :

![Feature Description Image](https://github.com/Pranjal-Soni/Bank-Customer-Churn-Prediction/blob/main/images/feature_target_relation.jpg)

The distribution of categories for various categorical features :

![Feature Description Image](https://github.com/Pranjal-Soni/Bank-Customer-Churn-Prediction/blob/main/images/categorical_feat_dist.jpg)

The heatmap to visulaise the correlation between numerical vaiables :

![Feature Description Image](https://github.com/Pranjal-Soni/Bank-Customer-Churn-Prediction/blob/main/images/corr.jpg)


## Feature Engineering 

There are too many categorical features like Gender, Geography, HasCard, IsActiveMember, etc. So to analyse their effect on the target variable, I performed the chi-square test, and I found that expect HasCard feature, all other features have a significant impact on the target variable. So I drop the HasCard feature from the dataset and perform one-hot encoding for all the nominal features. The numerical features like Age, CreditScore, etc., are not normally distributed, so I take the help of a power transformer to make them normally distributed. To perform all these operations and avoid data leakage, I help sklearn pipelines perform all the feature engineering and training models.

## Model Selection And Perfomarmance Matric:

I applied various ML algorithms like Logistic Regression, Support Vector Machine, Random Forest, Adaboost Classifier, XGBoost, Catboost and Balanced Random Forest. To mejor the performance of the machine learning model I choose RECALL score for the customers who Exit from the Bank. The reason behind is that if a model have higher recall, it is able to identify that much churn customers correctly.

## Results of Machine Learning models:

The recall value for class 1 is as follows for vaious machine learning algorithms:
* Logistic Regression : 0.22
* Support Vector Classifier : 0.40
* Random Forest Classifer : 0.44
* XGBClassifier : 0.50
* AdaBoost Classifier : 0.48
* Balanced Random Forest Classifier : 0.75

