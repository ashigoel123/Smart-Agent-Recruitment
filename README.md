                              SMART AGENT RECRUITMENT

Problem Statement
FinMan is a Financial Distribution company. Over the last 10 years, they have created an offline distribution channel across India. They sell financial products to consumers by hiring agents in their network. These agents are freelancers and get commission when they make a product sale.
The Managers at FinMan are primarily responsible for recruiting agents. Once a manager has identified a potential applicant, they would explain the business opportunity to the agent. Once the agent provides the consent, an application is made to FinMan to become an agent. This date is known as application_receipt_date.
In the next 3 months, this potential agent has to undergo a 7 day training at the FinMan branch (about Sales processes and various products) and clear a subsequent examination in order to become a FinMan agent.

There is a significant investment which FinMan makes in identifying, training and recruiting these agents. However, there are a set of agents who do not bring in the expected resultant business. 

Objective
•	Based on the above problem statement task was to create a prediction model that will help the FinMan to evaluate that on what candidates they should be more focus in future to save their cost and time screening non-relevant candidates and what kind of managers should be appointed for the screening process.





Approach:
To create a Prediction Model that will help FinMan to target right candidates, I have used the following approach:
•	Identify the problem statement: Thoroughly understood the data and the problem statement to use the required ML algorithm for prediction.
•	Based on the problem statement and objective the ML algorithm best identified for the prediction of the credit card leads is supervised (Logistic Regression) Machine Learning Algorithm, because the target variable that we are targeting is categorical.


Data Preprocessing:
For Data Preprocessing I have followed the following approach:
•	The dataset was given as train and test dataset. Both the datasets are imported, visualized, cleaned accordingly.
•	Anatomy of each column of both the datasets is identified that whether the columns are Quantitative, Categorical or Qualitative.
•	The columns which were qualitative were dropped from the datasets as they would create high dimensionality. 
•	Exploratory Data Analysis of both the datasets was done which helped to evaluate the outliers present in the datasets.
•	Quantitative variables were identified using histogram
•	Categorical Variables were identified using Bar Graph.
•	Treatment of outliers was done on both the datasets based on the values which were very far away from the average value.
•	Outliers treatment was not required in the Quantitative variables but it was done in the Categorical Variables, Values that very less in number were replaced by the another lowest category in the column to balance the data
•	 Missing Value Treatment was done in both the datasets, in which the missing values which were less than the 30% of the total number of rows were replaced by the average value of that column.
•	Bivariate analysis was done on the Train dataset with the Target Variable (Business_Sourced) to visualize that whether the predictors were correlated with the target variable or not.
•	To visualize the Categorical vs Quantitative predictors Box Plots were plotted.
•	To visualize the Categorical vs Categorical predictors Grouped Bar charts were plotted.
•	The bivariate analysis of the target variable and predictors was done on the basis of the average value, that how much the average value of one category is different from the other category’s average value.


Model Development:
•	To create a final prediction model, those predictors were required that were correlated with the target variable.
•	The correlation of the predictor variables with the target variables was statistically evaluated on the basis of the statistics tests.
•	For categorical vs quantitative predictors ANOVA TEST was performed.
•	For categorical vs categorical predictors CHISQ Test was performed.
•	On the basis of the p-value predictors were considered to be correlated with the target variable.
•	P-value was evaluated on the basis of the hypothesis test by accepting and rejecting the null hypothesis test, if the p-value was less than 5% than the null hypothesis was rejected and vice-versa.
•	After selecting the final predictors, dummies of the categorical variables were created.
•	The data was then splitted into70% train and 30% test datasets, in which the data was to be trained on the train dataset and the accuracy was to be calculated on the train dataset.
•	Then the train dataset values were passed through the Logistic Regression Model and the model was created to learn the train data that has been passed through it.
•	The predictons were made on the test dataset on the basis of the model has learned from the train dataset.
•	Models used : Logistic Regression, Random Forest, Decision Tree, XG Boost, LGBM
•	Final model selected giving the best roc_auc_score is LGBM

