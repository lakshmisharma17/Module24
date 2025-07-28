
# 🏡 California Housing Price Prediction

This project is part of the Capstone Project 24.1 and aims to predict housing prices in California based on socio-economic and geographic features. It explores data preparation, modeling, and evaluation techniques in a supervised machine learning pipeline.

## 📌 Problem Statement
The goal is to predict California housing prices using socio-economic and geographic data. Key challenges include handling missing values, non-linear feature relationships, and feature engineering. Accurate predictions can benefit buyers, investors, and policymakers.

## 🎯 Model Outcome
- **Type**: Supervised Learning
- **Prediction Task**: Regression
- **Target**: Median house value

## 📊 Data Source
Dataset: [California Housing Prices](https://www.kaggle.com/datasets/camnugent/california-housing-prices)  
- 20,640 rows, 10 features  
- Includes `median_income`, `housing_median_age`, `latitude`, `longitude`, and `ocean_proximity`

## 🧹 Data Preprocessing
- Removed 207 rows with missing `total_bedrooms` values.
- Dropped duplicates.
- Handled outliers using IQR and scatter plots (final dataset: 17,434 rows).
- Engineered features: `rooms_per_household`, `population_per_household`, `bedrooms_per_room`.
- One-hot encoded `ocean_proximity`.
- Train-test split: 80% training / 20% test.

## 🤖 Models Used
- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor (SVR)
- Voting Regressor (Ensemble)

## 🧪 Model Evaluation
- **Metrics**: MSE, RMSE, R²
- **Top Performer**: Random Forest Regressor
  - R²: **0.787**
  - RMSE: **~$43,048**
- GridSearchCV tuning did not improve results further.

## 🔍 Key Features Identified
- `median_income`
- `latitude`, `longitude`
- `population`
- `ocean_proximity`

## 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Scikit-learn, Matplotlib, Seaborn

## 📁 Project Structure
- `notebooks/` – Jupyter Notebooks for EDA and modeling
- `data/` – Cleaned dataset
- `README.md` – Project overview
- `report/` – Final report (PDF/docx)

## 📌 Conclusion
Random Forest yielded the best predictive performance. The consistent appearance of socio-economic and geographic features across models demonstrates their importance in determining housing prices in California.
