PROBLEM STATEMENT:
Cars4U is a fast-growing tech startup exploring the pre-owned car market in India. With increasing demand for used vehicles and a slowdown in new car sales, an effective pricing model is critical. This project builds a machine learning regression model to predict used car prices based on various features such as brand, model, year, kilometers driven, fuel type, and more.

The goal is to develop a model that can assist the business in setting optimal prices, avoiding underpricing, and making profitable decisions using data-driven strategies.



PROCESS FOLLOWED TO ACHIEVE THE RESULT:

Data Collection & Exploration:
Loaded used_cars_data.csv (7,252 rows × 14 columns).
Checked datatypes, missing values, and duplicates.
Performed statistical summaries (df.describe()), histograms, and boxplots to understand distributions.


Data Cleaning & Preprocessing:
Extracted numeric values from Mileage, Engine, Power, and New_Price.
Handled missing values (mean/median/mode imputation).
Removed outliers using the IQR method.
Dropped duplicate rows.
Encoded categorical variables (one-hot encoding).


Exploratory Data Analysis (EDA):
Visualized distributions of numerical features.
Plotted relationships: Fuel_Type vs Price, Model counts, Mileage/Engine/Power vs Price, and correlation heatmap.
Observed right-skewed prices, outliers, and key brand/model insights.


Model Building:

SIMPLE LINEAR REGRESSION
Seats → New_Price (R² ≈ 0.0003, very poor fit).
Seats → Power (R² ≈ 0.011, also poor fit).

Multiple Linear Regression:
Features: Year, Kilometers_Driven, mileage_num, engine_num, power_num, New_Price (+ encoded categorical vars).
Achieved R² ≈ 0.78 with MSE ≈ 28 → strong predictive power.
Synthetic Example Regression
Tested regression on dummy sales data (Product_Price, Discount, Advertising).

Model Evaluation:
Used metrics: R², MSE, RMSE, MAE.
Multiple regression significantly outperformed simple regression.
Best-fit regression equation derived for car price prediction.
