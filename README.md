# Predicting Taxi Ride Fares in New York City
A Multiple Linear Regression (MLR) project was used to predict ride fares to optimize revenue growth.

# Overview
This is a project on the New York City Taxi and Limousine Commission data. The goal was to predict ride fares using existing data that was collected over the course of a year. A Multiple Linear Regression model was used to find the biggest predictor of fare amounts per ride, successfully resulting in an R-squared of 0.868. This result suggests that 87% of the variance is explained by the model. The feature **mean distance** produced a mean of 7.10, suggesting that, when translated from standard deviation, for every 3.56 miles traveled the fare increases by $7.10.

# Business Understanding
The company wants to optimize revenue growth and create an app that allows drivers to see the estimated fare before the trip initiates. This app would not only help the company optimize revenue by introducing a stable price predictor but also help upscale drivers' salaries to a livable wage.

# Data Understanding
The NYC Taxi and Limousine Commission data came from https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page. The data was sampled into a dataset of 22699 rows and 18 columns. The features included information on trip duration and pickup and dropoff date/time, passenger count, fare amount, and payment type. The box plot below shows the distribution of trip distance that exists in the data set. 

![MLR_Boxplot_Trip](https://github.com/Nero103/Multiple-Linear-Regression-of-Taxi-and-Limousine-Services/assets/92405860/5741c54b-15cb-4962-af92-989f09be7c01)

# Model and Evaluation

The **mean distance** shows a high correlation with the target variable **fare amount** at 0.91.

![Correlation_Heatmap_TLC](https://github.com/Nero103/Multiple-Linear-Regression-of-Taxi-and-Limousine-Services/assets/92405860/7a7dd1df-1ea9-41c3-832e-c19b931aff8b)

An MLR model comprising of 5 predictor variables was then used to determine which feature had the most weight in the model's prediction. The below table shows that **mean distance**, **mean_duration**, and **trips during rush hour** were the top 3 weights in predicting fares before a ride starts. The overall model performed with an R-squared of .87% and a 14.32 mean squared error. 

VendorID  passenger_count  mean_distance  mean_duration  rush_hour
-0.054376         0.030755       7.102335       2.806779   0.110278

# Conclusion

This model can benefit Taxi Drivers in knowing what the fare will be before the ride starts. However, running a model to determine how much each variable will influence the actual fare with correlated predictors may widen the confidence interval. In the future, isolating the correlated predictors or removing one of them may also be beneficial in helping the model address the weights of other predictors, giving an even more precise prediction. 
