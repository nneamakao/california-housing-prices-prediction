# california-housing-prices-prediction
Prediction of house values in California using Regression model

The dataset can be downloaded from (Kaggle)[https://www.kaggle.com/datasets/camnugent/california-housing-prices]. 
It consists of ten columns as follows:
1. longitude: A measure of how far west a house is; a higher value is farther west
2. latitude: A measure of how far north a house is; a higher value is farther north
3. housing_median_age: Median age of a house within a block; a lower number is a newer building
4. total_rooms: Total number of rooms within a block
5. total_bedrooms: Total number of bedrooms within a block
6. population: Total number of people residing within a block
7. households: Total number of households, a group of people residing within a home unit, for a block
8. median_income: Median income for households within a block of houses (measured in tens of thousands of US Dollars)
9. median_house_value: Median house value for households within a block (measured in US Dollars)
10. ocean_proximity: Location of the house w.r.t ocean/sea

In the exploratory and transformation phases, columns dropped were highly correlated features (total_rooms, total_bedrooms, households) as well as housing_median_age, which seemed not to have any impact on the value of a house. The ocean_proximity column, which was initially categorical, was encoded using one-hot encoding. The resulting numerical dataset was then clustered as I found that assigning clusters before the regression model took the $\r^2$ score from about 0.84 to 0.955.

I tried different regression models - Linear Regression, Decision Tree Regression, Ridge, Lasso, Gradient Boosting Regression, and K-nearest Neighbours Regression. The Gradient Boosting Regressor performed best in terms of mean absolute error and mean squared error with final values of 18524.859 and 612529906.242 respectively. 
