# AAVE-price-prediction-using-ARIMA

The purpose of this project is to create an ARIMA (AutoRegressive Integrated Moving Average) model to predict the future prices of AAVE.

## Data Collection:

The historical data of AAVE is collected from Investing.com [Link to the dataset](https://www.investing.com/crypto/aave/historical-data)

## Data description:

The data contains the historical prices of AAVE from Nov 05, 2020 to Feb 13, 2022.

[Image]

## Baseline model - Persistence model:

A baseline model is built, so that it is easy to compare the results of our optimum model with it. We got a RMSE value of 15.816 using the baseline model. So, our other models must be definitely better than this.

## Checking whether the data is stationary or not:

ADF (Augmented Dicky Fuller) test is performed. ADF (Augmented Dicky Fuller) statistic is -8.79 which is less than 1% critical value. So, we can reject the null hypothesis and accept the alternate hypothesis (which is the data is stationary, by performing 1 differencing).

## Hyper parameter tuning to find the best (p,d,q) values for the ARIMA model:

ARIMA(1,0,0) gives us the better RMSE value, which is Autoregression of "1" will be the optimum model for this dataset.

## Transforming the dataset using boxcox transform:

Best lambda value for the boxcox transform is 1.0169. The data is transformed and again trained using ARIMA (1,0,0).

## Prediction:

[Image]

## Performance of the model:

RMSE (Root Mean Sqaured Error) value for the validation data is 8.940




