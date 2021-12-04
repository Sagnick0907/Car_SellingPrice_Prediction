# Car-Price-Prediction
# Car Selling Price Prediction:
## Table of Content
  * [Demo](#demo)
  * [Overview](#overview)
  * [Goal](#goal)
  * [Technical Aspect](#technical-aspect)
  * [Technologies Used](#technologies-used)

## Demo
Link : https://carsellingpricepredictor0907.herokuapp.com/ 
## Overview
This is a simple Car Selling Price Flask app trained with Random Forest Regressor. The trained model takes various parameters (years of service, kilometres driven, no. of previous owners, etc.) as an input from user and predicts the approximate Selling Price for that car.
## Motivation and Goal
Imagine a situation where you have an old car and want to sell it. You may of course approach an agent for this and find the market price, but later may have to pay pocket money for his service in selling your car. But what if you can know your car selling price without the intervention of an agent. Or if you are an agent, this will definitely make your work easier as this system has already learned about previous selling prices over years of various cars.  
Any kind of modifications can also be later be built in this application. So, in this way, this kind of app becomes handy for many people.  
## Technical Aspect
Dataset: https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho?select=car+data.csv

Given below are the steps taken to build the app:
1. Started with creating new environment for our project. 
2. For the ML implementation code – 
	- Imported necessary Python libraries (Pandas, Numpy, seaborn, etc.)
	- Imported the Dataset and performed Data Analysis on the dataset to derive insights on the features, number of features, their correlation, etc., so that we will be able to distinguish which features are important for prediction & how we would perform feature engineering on it effectively.
	- In Feature Engineering Section, we found no NULL values in the dataset. We used One Hot Encoding for Categorical Variables. Created a new column for the attribute “Years of Service” .
	- Splitting Datasets using train_test_split from sklearn.model_selection.
	- We used Randomized Search CV for Hyperparameter Tuning to help us find the best parameters.
	- Created a base RandomForestRegressor() model along with various parameters and “random_grid” as param_distributions (Randomized Search CV).
	- Training & Testing was done.
	- From sklearn we imported metrics to calculate how good our model was which is as follows:  
   		- Accuracy using Multiple Linear Regression :  
   		r2 score is: 0.8517983059778264  
   		MAE: 1.2426713915033707  
   		MSE: 4.432128265667618  
   		RMSE: 2.105262042043132  
   		- Accuracy using random forest regressor using randomizedCV :  
   		r2 score is: 0.8670971735039767  
   		MAE: 0.8876565934065918  
   		MSE: 3.9745994658604404  
   		RMSE: 1.993639753280527  

3. Created a pickle file.
4. Created the requirements.txt file.
5. Created the Flask app on Spyder IDE.
6. Finally, deployed the app on Heroku Platform where anyone can access & use my web app for Car Selling Price Prediction.

## Technologies Used
- Jupyter Notebook
- Flask Framework
- Spyder IDE
- Heroku
- ML model : Random Forest Regressor + hyperparameters tuning(Randomized CV) ( Selected )
- Multiple Linear Regression
-	SVM(To be Done)
- Libraries: pandas, numpy, seaborn, matplotlib, sk-learn, metrics, etc.

