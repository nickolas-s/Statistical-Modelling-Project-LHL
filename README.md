# Final-Project-Statistical-Modelling-with-Python

## Project/Goals

The objective of this project is to apply all the Python and Statistics Modelling knowledge acquired throughout Course 2 of the Data Analytics Bootcamp.
The goal is to build a statistical Model using Python that demonstrates a relationship between the number of bikes in a particular location and the characteristics of the POIs in that location.

## Process

- Connect to the Citybikes API and retrieve all available bike stations in a chosen city. Create a dataset from the result.
- Connect to Foursquare API and Yelp API to retrieve the points of interest for each bike station in a 1000-meter radius. Create two datasets from the results.
- Analyze the results from both APIs to identify which one provides more detailed information.
- Join the data from Citybikes with the data from Foursquare or YLP to create a new dataframe.
- Use data visualization to explore the data.
- Create a SQLite database to store the data collected from the APIs.
- Build a Multivariate Linear Regression that demonstrates a relationship between the number of bikes in a particular location and the characteristics of the points of interest in that location.
- Interpret results and derive insights from your model.

## Results

When comparing the quality of Foursquare API and Yelp API coverage for Hamilton Ontario, the latter API provided better details such as review count, rating, and price from a single API call based on latitude and longitude. If we wanted to retrieve similar information from Foursquare, we would need to first make an API call based on latitude and longitude to get all the POI and then make another API call for every single POI for further details. For this reason, the Yelp API was chosen to proceed with the analysis since it offers more detailed results with fewer steps.

The results from the Multivariate Linear Regression Model were not very insightful. Due to the nature of the dataset, it seems like all the numerical variables are not correlated with one another.

![](https://res.cloudinary.com/dnfecsurp/image/upload/v1701968731/python-project-lhl/OLS_Regression_Results_g6ikgr.png)

We can see below a few highlights from the model output:

- **Adj. R-squared**: This multivariate model explains only 0.6% of the variations in the data. This model doesn't seem to be a good fit.

- **Prob (F-statistic)**: The P-value for the hypothesis test is greater than 0, so we fail to reject the null hypothesis. The independent variables do not affect the dependent variable.
    
- **coef**: We can tell from the output that the average POI price has the strongest positive impact on the number of bikes per station, whereas review_count has the largest negative impact on on the number of bikes per station.

- **P>|t|**: A p-value of less than 0.05 is considered to be statistically significant. This regression output shows that all p-values are >0.05. In other words,review_count, rating, and price attributes of a point of interest do not impact the number of bikes in a bike station.

## Challenges 

Interpreting and deriving insights from the model was rather challenging since the data was not quite interconnected.

## Future Goals

If more time was available, it would probably be to explore further the Foursquare API.
