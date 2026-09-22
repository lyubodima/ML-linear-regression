# ML-linear-regression
Price prediction for houses

1. Objective and data exploration

The objective of this analysis is to develop a linear regression model to predict house prices in different areas of London using the provided dataset. The dataset includes monthly variables related to housing in London, spanning several years. The key columns are:
date: The date of the record.
area: The area in London.
average_price: The average house price in that area for the given month.
code: The area code.
houses_sold: The number of houses sold in that area for the given month.
no_of_crimes: The number of crimes reported in that area for the given month.
borough_flag: A flag indicating whether the area is a borough.

2. Data Preprocessing

The no_of_crimes column had a lot of missing values, so it was not used. But it showed bad result, so later it was incorporated with feature engineering
The houses_sold column also had missing values, which were filled with the mean of the column at first but later used in feature engineering.
The categorical variables area and code were converted to numerical values using one-hot encoding.




3. Model Training
The data was split into training and testing sets with an 80-20 split:
A linear regression model was trained using the training set.
First model was giving only 37% RMSE. Number of crimes was not used because of ~50% of missing values. But after this poor result we decided to use it and it improved the model significantly.
4. Model Evaluation
The model made predictions on the test set. The performance of the model was evaluated using the Root Mean Squared Error, MAE,  R-squared and MSE. It showed good result.
RMSE: On average, the model’s predictions are off by 0.17 which is small
MAE: The average absolute error in the model’s predictions is 0.14 which is small
R-squared: The model explains 0.93% of variance in the target variable
MSE of 0.03 is small. There are small prediction errors


Summary:
Goal of the project: Predict house prices. Data set was inspected with plots and inspection and correlation functions. Model was trained but it required feature engineering to improve the model. Dataset is more than 10000 points. The linear regression model was successfully trained and evaluated on the housing dataset. RMSE value, MAE, R squared and MSE show good accuracy. Additionally a scatter plot was used to find the dependencies.
