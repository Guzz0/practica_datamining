# Airbnb Madrid Data Mining Project

This project is a practical application of data mining techniques on Airbnb data for Madrid, Spain. The main objective is to predict the square meterage of apartments based on various features. The project involves several stages including data cleaning, feature engineering, model building, and prediction.

## Data Cleaning

The first step in the data mining process was to clean the data. The dataset initially contained missing and zero values in the `Square.Meters` column. These were replaced with `NA` values for more accurate analysis. Additionally, apartments with less than 20 square meters were considered outliers and were replaced with `NA`.

## Feature Engineering

The neighborhood appears to be a significant factor for the square meters of an apartment. Therefore, neighborhoods were grouped based on their similarity in terms of square meters. The similarity was calculated using Tukey's HSD (Honestly Significant Difference) test. This resulted in a new feature `neighb_id` in the dataframe, representing the cluster to which each neighborhood belongs.

## Model Building

The cleaned and processed dataset was split into a training set and a test set. A linear regression model was built to predict the square meters of an apartment based on the following features: 

- Accommodates
- Bathrooms
- Bedrooms
- Beds
- Price
- Guests.Included
- Extra.People
- Review.Scores.Rating
- Latitude
- Longitude
- neighb_id

The model showed a good fit with the training data, indicating that it could be a useful tool for predicting apartment sizes.

## Prediction

The final step in the data mining process was to use the model to predict the square meters of apartments in the test set. The predictions were compared with the actual values to evaluate the model's performance. The model showed a reasonable performance, indicating that it could be used to make accurate predictions.

## Conclusion

This data mining project provides valuable insights into the factors that influence the size of apartments in Madrid. The model built in this project can be used to predict the size of an apartment based on various features. This can be particularly useful for Airbnb hosts and guests, as well as for real estate professionals in Madrid.
