Required Capstone Project 24.1: Final Report

California Houses’ Pricing Prediction Final Report
1.	Define the Problem Statement: Provide a well-defined problem statement that clearly articulates the goals, challenges, and potential benefits of your machine learning solution.
Response: The goal of this project is to predict housing prices in California based on socio-economic and geographic factors. The challenge lies in dealing with varied feature types, missing values, and potential non-linear relationships across independent variables. Accurate price prediction has practical value for buyers, investors, builders, and policy makers.

2.	Model Outcomes or Predictions: Identify the type of learning (classification or regression) and specify the expected output of your selected model. Determine whether supervised or unsupervised learning algorithms will be used.
Response: This is a regression problem using supervised learning. The expected output is a continuous variable representing the median house value in the state of Califionia .

3.	Data Acquisition: The deliverable at this step is to identify what data you plan to acquire and use with your model. For the best results, data should come from multiple sources and your analysis for including specific data should be clear. Please provide a clear visualization to assess the data’s potential to solve the problem as well.
Response: The dataset used (https://www.kaggle.com/datasets/camnugent/california-housing-prices/discussion/57595) is a public California housing dataset consisting of 20,640 rows and 10 columns. It includes features such as median income, housing median age, and geographic coordinates. A visual EDA was performed using scatter plots and correlation matrices to assess feature relationships.

4.	Data Preprocessing/Preparation: For this deliverable, you are tasked with detailing how you cleaned the data for your notebook. 
a.	What techniques did you use to ensure your data was free of missing values, and inconsistencies? 
Response: Data cleaning involved removing 207 rows with missing values in 'total_bedrooms'. Duplicate rows were also removed. Outliers were identified using IQR and scatter plots, reducing the dataset to 17,434 rows.

b.	How did you split the data into training and test sets?
Response: Data was split into 80% training and 20% testing sets.

c.	Please include any necessary analysis and encoding steps you took as well.
Response: Feature engineering included creating 'rooms_per_household', 'population_per_household', and 'bedrooms_per_room'. The 'ocean_proximity' categorical variable was one-hot encoded.


5.	Modeling: For this deliverable, please document your selection of machine learning algorithms that you selected for your problem statement from the first deliverable.
Response: Several regression models were implemented using scikit-learn pipelines: Linear Regression, Ridge Regression, Random Forest Regressor, Gradient Boosting Regressor, SVR, and an ensemble Voting Regressor. The best model among all these , based on  the Evaluation metrics (R-squared and RMSE), was trained and evaluated using GridSearchCV for hyperparameter tuning to get the final result.


6.	Model Evaluation: Share your model evaluation here. What types of models did you consider for your problem (classification, regression, unsupervised)?  Articulate the evaluation metrics you used and how you determined which model was most optimal for your problem.
​​Response: 
The models were evaluated using Mean Squared Error (MSE) , Root Mean-Squared Error (RMSE), and R-squared (R²).
Random Forest model was the top performer, achieving the highest R-squared of 0.787 and the lowest Root Mean Squared Error (RMSE) of approximately $43,048. 
The result after GridSearch gave low R-Squared and higher RMSE , hence hyper parameter tuning didn’t help in this case.
Important features across models included median_income, latitude, longitude, proximity to Ocean, and population


# Module24
