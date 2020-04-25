# Udacity_Capstone_Project

Contents
Project Overview
Components
Libraries Required
Files Required
Analysis and Results


### Project Overview
In this project, I used machine learning to analyze data provided by mail order sales company of Germany and compared it to the demographic information of the general population.
I used unsupervised learning techniques to perform customer segmentation, identifying the parts of the population that best describe the core customer base of the company. Then, I applied the learning on a third dataset with demographics information for targets of a marketing campaign for the company, and used a xgboost classifier model to predict which customers who are most likely to convert into becoming customers for the company. The data I used for this project was provided by Udacity and Bertelsmann Arvato Analytics.

### Components
The project has 3 major parts:
Customer Segmentation Report: Here, I used unsupervised learning techniques to describe the relationship between the demographics of the company's existing customers and the general population of Germany. By end of this this part, I was able to describe parts of the general population that are more likely to be part of the mail-order company's main customer base, and which parts of the general population are less so.
Supervised Learning Model: In this part of the project I built and tested a prediction model that predicts whether or not an individual would respond to a mail out campaign. Here attributes of a third dataset ‘mailout’ from mail campaign were used to test the model. 
Kaggle Competition: Once best performing model was identified, it was used to make predictions on the campaign data as part of a Kaggle Competition. The probability of individuals were ranked by how likely they are to convert to being a customer. Based on these results of our modeling skills, we are tested against our peers.

### Libraries Required
The code was written in python 3 
It requires the following packages: numpy, pandas, matplotlib, seaborn, pickle, time, sklearn

### Files Required
There are four data files associated with this project. However due to copyright, these cannot be shared. 

Udacity_AZDIAS_052018.csv: Demographics data for the general population of Germany; 891 211 persons (rows) x 366 features (columns).
Udacity_CUSTOMERS_052018.csv: Demographics data for customers of a mail-order company; 191 652 persons (rows) x 369 features (columns).
Udacity_MAILOUT_052018_TRAIN.csv: Demographics data for individuals who were targets of a marketing campaign; 42 982 persons (rows) x 367 (columns).
Udacity_MAILOUT_052018_TEST.csv: Demographics data for individuals who were targets of a marketing campaign; 42 833 persons (rows) x 366 (columns).
Each row of the demographics files represents a single person, but also includes information outside of individuals, including information about their household, building, and neighborhood
The "CUSTOMERS" file contains three extra columns ('CUSTOMER_GROUP', 'ONLINE_PURCHASE', and 'PRODUCT_GROUP'), which provide broad information about the customers depicted in the file. The original "MAILOUT" file included one additional column, "RESPONSE", which indicated whether or not each recipient became a customer of the company. For the "TRAIN" subset, this column has been retained, but in the "TEST" subset it has been removed; it is against that withheld column that your final predictions will be assessed in the Kaggle competition.
 For more information about the columns depicted in the files, you can refer to two Excel spreadsheets. DIAS Information Levels - Attributes 2017.xlsx is a top-level list of attributes and descriptions, organized by informational category.
DIAS Attributes - Values 2017.xlsx is a detailed mapping of data values for each feature in alphabetical order.

### Analysis and Results
Part 1 : The majority of analysis including Exploratory Data Analysis, Data Cleaning and Feature transformation were performed in this part of the project. Here, I used dimensionality reduction techniques of unsupervised learning such as PCA and Clustering with KMeans, to distinguish individuals from general population that could best describe the core customer base of the client. 
Part 2 : In this part, a prediction model was built using supervised learning techniques. Multiple classification models were tried and compared on basis of roc auc metric. XGBoost Classifier was ultimately selected due to its performance. It was then fitted to the training data and used to make predictions on the test datasets to identify which individuals of a marketing campaign are most likely to convert into becoming customers.
Part 3  In this part I submitted my file to Kaggle as part of the class competition where I got a score of 0.70.

Blog Post: https://medium.com/@kasakobe/who-is-your-customer-a-machine-learning-approach-7bcf9ebdc9d4	
