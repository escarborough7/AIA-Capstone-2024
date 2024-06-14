# AIA-Capstone-2024 Group 8
Hello and welcome to the Capstone project for AI Academy bootcamp by Group 8. Our goal with this project was to create a predictive model that can be accurately used by credit servicers to detect if a credit card transaction is fraudulent or not using a Kaggle dataset. We tested various analytical techniques including Principle Component Analysis(PCA). Linear Regression, and a couple different Decision Tree Regression models. We settled on a Decision tree Regression model optimized using SMOTE to handle our imbalanced dataseHello and welcome to the Capstone project for AI Academy bootcamp by Group 8. Our goal with this project was to create a predictive model that can be accurately used by credit servicers to detect if a credit card transaction is fraudulent or not using a Kaggle dataset. We tested various analytical techniques including Principle Component Analysis(PCA). Linear Regression, and a couple different Decision Tree Regression models. We settled on a Decision tree Regression model optimized using SMOTE to handle our imbalanced datase

# Project Objective
	
-Build a predictive model to detect the likelihood of a transaction being fraudulent
-Experiment with various machine learning techniques to classify fraudulent and nonfraudulent transactions
-Test different ways to handle the imbalanced dataset

### Project Approach
1.**Find a dataset**: We used Kaggle to find a dataset that fit the problem we wanted to solve.
2.**Exploratory Data Analysis**: Combed through the dataset to get an understanding of the data we were working with and how to best go about creating a model.
3.**Data Preparation**:
-Clean the data
-Normalize and Standardize the dataset
-Add a unique ID in the form of transaction numbers to each of the records
1.**Model Selection**: Various machine learning models are defined including:
-Logistic Regression	
-Decision Trees
-Principal Component Analysis (PCA)
2.**Handling Imbalance using Oversampling Techniques**: Used SMOTE to handle class imbalance within our dataset
3.**Model Training**: The models were trained using cross-validation both with and without SMOTE
3.**Prediction**: The models were introduced to testing data which were transactions different from the ones they were tested on.
4.**Model Tuning**: After we analyzed the predictions given by each model we tuned the model to better fit our objective. for the decision tree we pruned the leaves of the tree in an attempt to give us a more accurate result. 

# Choosing the Data
The project will review the data: https://www.kaggle.com/datasets/dhanushnarayananr/credit-card-fraud
This data was chosen for its size, recentness, and variable interpretability. 
The columns/variables are labeled in a manner that would be understood as to what it represented. There were many other data sets but they unfortunately did not have labeled columns and thus would have made it difficult to interpret and present as a solution to a hypothetical problem. 

# Notebook
Unfortunately, due to an error in creating the GitHub, all files used are located in the main branch. The important file with code that we would like to present is labeled as "Group 8 Final Code". 

In this code, you see that a basic EDA was ran to get initial thoughts on the data. 

Afterwards, it is clear that there is a clear class imbalance so SMOTE is the first step. 

The idea of using the PCA is that with 6 variables, two new variables "PC1" and "PC2" could be created to be used in future models. Unfortunately due to an error in interpretation and time, PCA was found to be useful but not used to run logistical regression and the decision tree. 

The next step was to run a logistical regression which did indeed produce nice metrics (accuracy, precision, recall, and F1), but the decision tree was decided given that recall was prioritized. 

Our reason for prioritizing recall was because given the nature of the probelem (finding positive cases), our model needed to be able to find true positives out of the true positives. It would be better to have the model mark a non-fraudulent case as fraudelent, rather than not flagging a fraudulent case as non- fraudulent. 
