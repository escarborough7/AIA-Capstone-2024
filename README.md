# AIA-Capstone-2024 Group 8
Hello and welcome to the Capstone project for AI Academy bootcamp by Group 8. Our goal with this project was to create a predictive model that can be accurately used by credit servicers to detect if a credit card transaction is fraudulent or not using a Kaggle dataset. We tested various analytical techniques including Principle Component Analysis(PCA). Linear Regression, and a couple different Decision Tree Regression models. We settled on a Decision tree Regression model optimized using SMOTE to handle our imbalanced dataset.

# Project Objective
	
-Build a predictive model to detect the likelihood of a transaction being fraudulent

-Experiment with various machine learning techniques to classify fraudulent and nonfraudulent transactions

-Test different ways to handle the imbalanced dataset

### Project Approach
1.**Find a dataset**: We used Kaggle to find a dataset that fit the problem we wanted to solve. 
The project will review the data: https://www.kaggle.com/datasets/dhanushnarayananr/credit-card-fraud

This data was chosen for its size, recentness, and variable interpretability. 

The columns/variables are labeled in a manner that would be understood as to what it represented. There were many other datasets but they unfortunately did not have labeled columns and thus would have made it difficult to interpret and present as a solution to a hypothetical problem.

2.**Exploratory Data Analysis**: Combed through the dataset and did basic EDA to get an understanding of the data we were working with and how to best go about creating a model.


3.**Data Preparation**:

-Clean the data

-Normalize and Standardize the dataset

-Add a unique ID in the form of transaction numbers to each of the records


1.**Model Selection**: Data transformation methods are defined including:

-Logistic Regression	

-Decision Trees

-Principal Component Analysis (PCA) __*while not a model, was used as a dimensionality reduction method_


2.**Handling Class Imbalance using Oversampling Techniques**: Used SMOTE to handle class imbalance within our dataset


3.**Model Training**: The models were trained using cross-validation both with and without SMOTE


3.**Prediction**: The models were introduced to testing data which were transactions different from the ones they were trained on.


4.**Model Tuning**: After we analyzed the predictions given by each model we tuned the model to better fit our objective. for the decision tree we pruned the leaves of the tree in an attempt to give us a more accurate result.


# Project Considerations
-For all code history please refer to the folder labelled **Working-Codes** 

-Here you will find the files used which acts as a history of the models we tried and the dataset both balanced and unbalanced. Included in the file is the dataset we used in the form of a python file. We included a file of our original decision tree using entropy and pruning. We also included a file containing the both balanced and unbalanced data.

-For our final code please refer to **Group 8 Final Code**. 

-The idea of using the PCA is that with 6 variables, two new variables "PC1" and "PC2" could be created to be used in future models. Previously, our PCA ran and was unable to account for more than 30% of variance making it unuseful at the time, but after running SMOTE and rerunning the PCA, it was able to account for almost 100% of the variance. Unfortunately, at this point we were unable to include it in the further models due to timing. 

-Our reason for prioritizing recall was because given the nature of the probelem (finding positive cases), our model needed to be able to find true positives out of the true positives. It would be better to have the model mark a non-fraudulent case as fraudelent, rather than not flagging a fraudulent case as non - fraudulent. 

For our presentation please refer to this link: https://amedeloitte-my.sharepoint.com/personal/pdriscoll_deloitte_com/Documents/Fraud%20Fighters%20Capstone%20Presentation.pptx?web=1
