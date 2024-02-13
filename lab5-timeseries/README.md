# Week 5 - Time series forecasting

This week we will explore ways to visualise and analyse time series data.

## Data

* Download the data for this lab from [https://github.com/Mcompetitions/M4-methods/blob/master/Dataset/Train/Hourly-train.csv](https://github.com/Mcompetitions/M4-methods/blob/master/Dataset/Train/Hourly-train.csv)
* This is a spreadsheet that contains many different time series (one per **row**).
* The data are collected hourly for each of them.
* Note that the time series are independent of each other and have no relationships between them; this is just a convenient way to store them.

## Lab Exercises
    
* You have been given a notebook that already loads the data called _timeseries_lab.ipynb_.
		
* In this notebook:

- [ ] We're going to work with the time series from column 'H414'.
- [ ] Extract the time series from the main data frame. If it has any missing values, drop them after making your copy (so the original data is not overwritten).
- [ ] Plot the time series, making sure you add proper labels to the axes.
- [ ] Plot the autocorrelation and partial autocorrelation functions.
- [ ] Use the STL method to decompose the time series.
- [ ] Use the ADF test to check if the data is stationary.
- [ ] Split the data:
    * Training set: first 30 days
    * Validation set: next 6 days
    * Test set: whatever number of days left after the validation set.
    * Create a plot in which the three sets are clearly distinguishable.
- [ ] Let's model the data. Start by creating a baseline model -- it's up to you which type: what does your knowledge of the data tell you?
    * Calculate the RMSE, R2, and MAE on your validation set using the baseline/naive method
- [ ] Select a range of suitable values for $p$ and $q$ and use the AIC criterion to select the best value to train an ARMA model on the time series.
    * Train the model with the best values and look at the residuals. Is it a valid model for forecasting the data?
- [ ] Now go to Moodle and complete the Quiz to get your marks for the lab.
