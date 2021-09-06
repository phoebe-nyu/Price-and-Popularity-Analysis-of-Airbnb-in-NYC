# Price-and-Popularity-Analysis-of-Airbnb-in-NYC
This is a final project of Applied Data Science course in NYU 

## Group Members
* Letao Hou (lh3163)
* Anbo Guo (ag6738)
* Yuetong Zhou (yz6729)
* Yanchen Liu (yl4265)

## Dataset

we used two dataset, one is NYC airbnb daily open data from October 2017 to October 2018 obtained from Airbnb Open Data for price analysis.   
  Another is the NYC Airbnb listings data obtained from Inside Airbnb, which contains detailed data on Airbnb property listings.
  https://www.kaggle.com/peterzhou/airbnb-open-data-in-nyc
  http://insideairbnb.com/get-the-data.html

## Methods
1. We established ARIMA and SARIMA models to perform time series analysis and forecast price.
 
2. For popularity analysis, we defined popularity metrics by applying booking rate, we first calculated median booking rate. If booking rate of the unit is lower than median booking rate, it is unpopular, otherwise, it is popular. Then we labeled popular/unpopular to each unit. 
There are 80+ features in original dataset, such as host_location, host_response_rate, host_acceptance_race, neighborhood, room type, number of reviews, etc, so we implemented correlation analysis to obtain top 25 features that are most related to booking rate. 

3. Considering plenty of categorical variables, we used ordinal encoder and one hot encoding. We developed PCA to reduce dimensions. By utilizing logistic regression, random forest and xgboost model, we finally got 0.78 accuracy with XGBoost model to forecast popularity. 

