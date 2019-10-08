# Prediction_Models_of_Energy_Use_of_Appliances

## Dataset
The data set records the energy consumption of appliances in a house along with the corresponding environment, weather and time statistics in a time span of 137 days. There are a total of 19735 pieces of data and 32 variables in the data set.

![dataset](https://github.com/jingan0514/Prediction_Models_of_Energy_Use_of_Appliances/blob/master/images/Data%20variables%20and%20description.png)

## Features Filtering
Considering the weather data is not exactly metered in the house and there are several variables in the data set, we want to choose the most relevant variables to do data training. The Boruta package is used to evaluate the variable importance.
Although the Boruta package provides us with the sense of the variable importance, we still want to know how many variables are suitable to make the prediction. The recursive feature elimination (RFE) is used to choose an appropriate number of variables to perform the prediction. The random forest method is used with 10-fold cross validation.

![filter](https://github.com/jingan0514/Prediction_Models_of_Energy_Use_of_Appliances/blob/master/images/Importance.png)

![RFE](https://github.com/jingan0514/Prediction_Models_of_Energy_Use_of_Appliances/blob/master/images/kOgQtp28dYWN6PxU-PwD8LRBMbmagDfW_IIewR0p3LYllDjxWuW72qBLQ7ld4g3r_XQriq4HLwr8QT89-eq5Zi94w1953vD1BUolDFIgF82SjtIU_8QaaDnWmIWZSotxKwCO4LDP.png)

## Multiple Linear Regression
|     LR    | RMSE | R^2 | MAE | MAPE(%) |
| ----------| -----| -----| -----| -----|
| Training  | 93.21  | 0.18 | 53.13 | 61.32 |
| Testing   | 93.18  | 0.16 | 51.97 | 59.93 |

## Support Vector Machine
|     SVM    | RMSE | R^2 | MAE | MAPE(%) |
| ----------| -----| -----| -----| -----|
| Training  | 48.98  | 0.76 | 17.85 | 16.45 |
| Testing   | 82.82  | 0.36 | 37.92 | 35.82 |

## Random Forest
|     Rf    | RMSE | R^2 | MAE | MAPE(%) |
| ----------| -----| -----| -----| -----|
| Training  | 32.83 | 0.92 | 16.06 | 16.36 |
| Testing   | 81.52  | 0.38 | 40.3 | 40.00 |
