# Bike_Shearing_Demand_Prediection

## Problem Statement
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern.
The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes
## Data Description:
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.

In this project, we train a model to predict the number of bike rentals at any hour of the year given the weather conditions. The data set was obtained from the Capital Bikeshare program in Washington, D.C. which contained the historical bike usage pattern with weather data spanning two years.
We first build several individual regression models such as Linear, Ridge, Random Forest, Gradient Boost and Adaboost. We then use 'Stacking' approach where the predictions from these level 1 individual models are used as meta-features to build a second level model (Linear Regressor, Random Forest and Gradient Boost) to further enhance the predicting capabilities.

The key takeaway from the EDA and Modeling are

Bike rental count is strongly correlated with the time of the day, with weaker dependence on the temperature and humidity
There are 2 rental patterns across the day in bike rentals count
First on a Working Day where the rental count high at peak office hours (8am and 5pm) and
Second on a Non-working day where rental count is more or less uniform across the day with a peak at around noon.
Below figure shows the bike rental behavior and our model predictions on the test set data for a Random Forest Model
#output
![pred_vs_actual_rf1](https://user-images.githubusercontent.com/48796009/226129683-064188cd-87b5-4319-a461-e3ff04e83d51.png)
# Attribute Information:

 
• Date : year-month-day

• Rented Bike count - Count of bikes rented at each  hour

• Hour - Hour of the day

• Temperature-Temperature in Celsius

• Humidity - %

• Windspeed - m/s

• Visibility - 10m

• Dew point temperature - Celsius

• Solar radiation - MJ/m2

• Rainfall - mm

• Snowfall - cm

• Seasons - Winter, Spring, Summer, Autumn

• Holiday - Holiday/No holiday

• Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)
# Data Pipeline:

● Exploratory Data Analysis (EDA): In this part we have done some EDA on the features to see the trend.

● Data Processing: In this part we went through each attributes and encoded the categorical features.

● Model Creation: Finally in this part we created the various models. These various models are being analysed and we tried to study various models so as to get the best performing model for our project.
# Observations:

● Observation 1: In the Model Evaluation Matrices table, Linear Regression, KNN is not giving great results.

● Observation 2: Random forest & GBR have performed equally good in terms of adjusted r2.

● Observation 3: We are getting the best results from lightGBM and CatBoost.
