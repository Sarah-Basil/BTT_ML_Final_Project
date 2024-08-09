# Airbnb Price Prediction Project

## Overview

This project aims to predict the price of Airbnb listings based on various features such as property type, location, amenities, and more. The model leverages machine learning techniques to provide accurate price predictions, which can help hosts price their listings competitively and assist potential guests in understanding the cost dynamics of different listings.

## Table of Contents
- [Project Description](#project-description)
- [Data](#data)
- [Features](#features)
- [Modeling Approach](#modeling-approach)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)


## Project Description

The primary goal of this project is to build a regression model that can predict the price of an Airbnb listing. By analyzing various factors such as the number of rooms, location, amenities, and customer reviews, I aim to provide a reliable model that can be used for both pricing strategy and customer insight.

## Data

The dataset used in this project is sourced from Airbnb, which includes detailed information on listings. The data contains features like:

- Listing ID
- Location (Neighborhood, City)
- Property Type (Entire Home, Shared Room, etc.)
- Number of Bedrooms, Bathrooms, Beds
- Amenities (e.g., Wi-Fi, Kitchen, Washer)
- Customer Reviews (Scores for cleanliness, location, etc.)
- Availability and Booking Information

## Features

### Predictive Features
The following features were selected for training the model:

- `accommodates`: Number of people the property can accommodate
- `room_type_Entire home/apt`: Whether the listing is an entire home or apartment
- `bedrooms`: Number of bedrooms
- `bathrooms`: Number of bathrooms
- `beds`: Number of beds
- `neighbourhood_group_cleansed_Manhattan`: Whether the property is in Manhattan
- `amenities_sum`: Sum of amenities provided
- `review_scores_location`: Average location score from reviews
- **...more**

### Target Variable
- `price`: The target variable representing the listing price.

## Modeling Approach

### 1. **Data Preprocessing**
   - Handling missing values.
   - Encoding categorical features.
   - Feature selection based on correlation and importance.

### 2. **Modeling**
   - **Random Forest Regressor**: The primary model used for prediction.
   - **Hyperparameter Tuning**: Manual tuning of `n_estimators` and `max_depth` to optimize performance.

### 3. **Evaluation**
   - The model was evaluated using **Root Mean Squared Error (RMSE)** and **R-squared (R²)** metrics.

## Evaluation Metrics

The model performance was evaluated using the following metrics:

- **Root Mean Squared Error (RMSE)**: Measures the average magnitude of the errors between predicted and actual values.
- **R-squared (R²)**: Represents the proportion of the variance in the dependent variable that is predictable from the independent variables.

## Results

- **Best Model**: The best-performing model was achieved with `n_estimators = 500` and `max_depth = 32`.
- **Model Performance**:
  - RMSE: `0.1105`
  - R-squared: `0.7049`

These results indicate that the model performs well in predicting Airbnb prices, with a reasonable balance between bias and variance.
