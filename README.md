# Prediction_Models_of_Energy_Use_of_Appliances

## Dataset
The data set records the energy consumption of appliances in a house along with the corresponding environment, weather and time statistics in a time span of 137 days. There are a total of 19735 pieces of data and 32 variables in the data set.

![dataset]()

## Features Filtering
Considering the weather data is not exactly metered in the house and there are several variables in the data set, we want to choose the most relevant variables to do data training. The Boruta package is used to evaluate the variable importance.
Although the Boruta package provides us with the sense of the variable importance, we still want to know how many variables are suitable to make the prediction. The recursive feature elimination (RFE) is used to choose an appropriate number of variables to perform the prediction. The random forest method is used with 10-fold cross validation.

## Multiple Linear Regression
| LR  | RMSE | R^2 | MAE | MAPE(%) |
| ------------- | ------------- |
| Training  | 93.21  | 0.18 | 53.13 | 61.32 |
| Testing  | 93.18  | 0.16 | 51.97 | 59.93 |
