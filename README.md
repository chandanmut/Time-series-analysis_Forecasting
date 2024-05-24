# Time-series-analysis_Forecasting
This TSA forecasting model employs advanced machine learning techniques, including ARIMA, SARIMAX, and Exponential Smoothing, to predict future trends in monthly champagne sales. The model leverages statistical tests, differencing methods, and in-sample and out-of-sample evaluations to ensure robust and accurate forecasting.

I began by performing initial exploratory data analysis (EDA) to understand the dataset's structure and key statistical properties. This involved visualizing the sales trend over time, identifying seasonality patterns, and checking for missing values.

To ensure stationarity—a crucial requirement for time series modeling—I conducted the Augmented Dickey-Fuller (ADF) test. The initial series was non-stationary, with an ADF test statistic of -1.8336 and a p-value of 0.3639. After applying first-order differencing, the series became stationary, confirmed by an ADF test statistic of -7.1899 and a p-value of 2.5196e-10.

I employed Autoregressive Integrated Moving Average (ARIMA) models, experimenting with various lag values to identify the optimal model configuration. The ARIMA(1,1,1) model emerged as a good fit based on model diagnostics and AIC/BIC criteria. To better capture the periodic fluctuations in sales data, I incorporated seasonal components using Seasonal ARIMA (SARIMAX).

Additionally, I utilized Exponential Smoothing models to account for both trend and seasonality in a more flexible manner. I evaluated model performance using in-sample and out-of-sample predictions. The in-sample evaluation yielded a Mean Absolute Error (MAE) of 638.6494, Mean Squared Error (MSE) of 988527.2381, and Root Mean Squared Error (RMSE) of 994.2471. The out-of-sample evaluation produced an MAE of 1024.0798, an MSE of 1410610.1102, and an RMSE of 1187.6911, quantifying the model's predictive accuracy.

Finally, I forecasted future sales by extending the SARIMAX model, demonstrating the model’s robustness and applicability in real-world forecasting scenarios.
