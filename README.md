![](https://res.cloudinary.com/dnfecsurp/image/upload/v1707366290/python-project-lhl/Screenshot_2024-02-07_at_11.24.19_PM_rcp2ow.png)

# Statistical Modelling with Python - Project LHL

## Project Objectives

The main objective of this project is to apply the Python and statistical modeling knowledge obtained during Course 2 of the Data Analytics Bootcamp. The goal is to construct a statistical model using Python that illustrates the relationship between the number of bikes in a specific location and the characteristics of the Points of Interest (POIs) in that location.

## Process Overview

[Part 01](https://github.com/nickolas-s/Statistical-Modelling-Project-LHL/blob/main/notebooks/city_bikes.ipynb)
- Utilize the Citybikes API to fetch all available bike stations in a chosen city and generate a dataset.

[Part 02](https://github.com/nickolas-s/Statistical-Modelling-Project-LHL/blob/main/notebooks/yelp_foursquare_EDA.ipynb)
- Utilize the Foursquare API and Yelp API to acquire points of interest for each bike station within a 1000-meter radius and create two datasets from the obtained results.
- Analyze the results from both APIs to determine which one provides more comprehensive information.

[Part 03](https://github.com/nickolas-s/Statistical-Modelling-Project-LHL/blob/main/notebooks/joining_data.ipynb)
- Merge the data from Citybikes with the data from either Foursquare or Yelp to create a new dataframe.
- Employ data visualization techniques to explore the dataset.
- Establish a SQLite database to store the data collected from the APIs.

[Part 04](https://github.com/nickolas-s/Statistical-Modelling-Project-LHL/blob/main/notebooks/model_building.ipynb)
- Develop a Multivariate Linear Regression model to showcase the relationship between the number of bikes in a particular location and the characteristics of the points of interest in that location.
- Interpret the model results and extract insights.

## Results Summary

After comparing the quality of data coverage between the Foursquare API and Yelp API for Hamilton, Ontario, it was found that the latter provided more detailed information, including review count, rating, and price, with just a single API call based on latitude and longitude. Given this advantage, the Yelp API was chosen for further analysis.

However, the results from the Multivariate Linear Regression Model were not particularly illuminating. Due to the dataset's nature, it appears that there is little correlation among the numerical variables.


![](https://res.cloudinary.com/dnfecsurp/image/upload/v1707367024/python-project-lhl/full_df_pairgrid_vlvuzh.png)

![](https://res.cloudinary.com/dnfecsurp/image/upload/v1701968731/python-project-lhl/OLS_Regression_Results_g6ikgr.png)

Some key points from the model output include:

- **Adj. R-squared**: The multivariate model explains only 0.6% of the variance in the data, suggesting it is not a good fit.

- **Prob (F-statistic)**: The p-value for the hypothesis test is greater than 0, indicating that the independent variables do not significantly impact the dependent variable.
    
- **coef**: The average POI price has the strongest positive impact on the number of bikes per station, while review_count has the largest negative impact.

- **P>|t|**: All p-values are >0.05, indicating that the review_count, rating, and price attributes of a point of interest do not significantly affect the number of bikes in a bike station.

## Challenges 

Interpreting and deriving insights from the model proved challenging due to the lack of interconnectedness within the data.

## Future Goals

Given more time, further exploration of the Foursquare API would be a potential avenue for future research.
