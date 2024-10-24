# Air-Passengers

Summary of the analysis and model:
Data Collection and Exploration:
1.	Started by importing necessary libraries such as Pandas, NumPy, Seaborn, and Matplotlib.
2.	Then loaded the 'AirPassengers.csv' dataset into a Pandas DataFrame called 'air'.
3.	Explored the dataset using functions like shape, info, isna, isnull, describe, columns, and dtypes.
4.	Converted the 'Month' column to datetime objects and set it as the index.
5.	Visualized the data using pair plots, box plots, and KDE plots to understand the distribution and relationships between variables.
6.	Checked for normality of the '#Passengers' column using the Shapiro-Wilk test.
7.	Plotted the time series data to observe trends and seasonality.
8.	Decomposed the time series into trend, seasonal, and residual components using seasonal_decompose.
9.	Performed an Augmented Dickey-Fuller (ADF) test to check for stationarity.
10.	Applied differencing to make the time series stationary.
    
Model Building and Evaluation:
1.	Split the data into training and testing sets.
2.	Established a baseline MSE using the mean of the training data.
3.	Used auto_arima to find optimal parameters for a SARIMA model.
4.	Fit the SARIMA model using the identified parameters.
5.	Plotted residuals to check model assumptions.
6.	Performed rolling validation (walk-forward validation) to evaluate the model's performance on the test set.
7.	Compared the model's MSE to the baseline MSE.
   
Communication of Results:
1.	Created visualizations to compare the predicted values with the actual values.
2.	Saved the trained model using joblib.dump.
3.	Loaded the saved model using joblib.load.
4.	Created a predictor function Air_Passenger_Predictor to generate predictions for future dates.
5.	Tested the predictor function.
The analysis involved exploring the AirPassengers dataset, transforming it to ensure stationarity, fitting a SARIMA model to capture trends and seasonality, and evaluating its predictive performance. You also implemented functionalities for saving, loading, and using the model for future predictions.

  # Summary of Output

  Comparison:

The Test MSE (1013.48) is significantly lower than the Baseline MSE (2629.12). This indicates that SARIMA model performs much better than simply predicting the average.

Interpretation:

A lower MSE suggests better predictive accuracy. In this case, the substantial reduction in MSE from baseline to the SARIMA model implies that the model effectively captures the underlying patterns in the data and generates more accurate predictions.

Conclusion:

Based on the comparison of MSE values and visualizations,  SARIMA model demonstrates a good level of performance in predicting the number of passengers. It effectively captures the trends and seasonality present in the data, resulting in improved accuracy compared to the baseline approach. 


##The model fit the data reasonably well.

