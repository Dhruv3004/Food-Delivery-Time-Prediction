![logo](https://github.com/Dhruv3004/Food-Delivery-Time-Prediction/blob/main/thumbnail.png?raw=true)

# Food Delivery Time Prediction

This project aims to predict the delivery time of food orders using various features like the delivery person's age, ratings, weather conditions, and more. The goal is to enhance the accuracy of delivery time estimates, which can improve customer satisfaction and operational efficiency for food delivery services.

## Table of Contents
- Introduction
- Dataset
- Data Preprocessing
- Feature Engineering
- Modeling
- Evaluation

## Introduction

This project focuses on predicting the time taken for food deliveries based on several factors such as the delivery person's age, weather conditions, and road traffic density. Accurate predictions can help improve the efficiency of food delivery services by providing better time estimates.

## Dataset

The dataset contains the following features:

- `Delivery_person_Age`: Age of the delivery person.
- `Delivery_person_Ratings`: Ratings received by the delivery person.
- `Weather_conditions`: Weather during the delivery.
- `Road_traffic_density`: Road traffic density during the delivery.
- `Vehicle_condition`: Condition of the vehicle used for delivery.
- `Type_of_order`: Type of food order.
- `Type_of_vehicle`: Vehicle type used for delivery.
- `multiple_deliveries`: Indicates if multiple deliveries were made.
- `Festival`: Whether the delivery occurred during a festival.
- `City`: City where the delivery took place.
- `City_code`: Unique code representing the city.
- `day`, `month`, `quarter`, `year`: Temporal features indicating the delivery date.
- `day_of_week`: Day of the week when the delivery was made.
- `is_month_start`, `is_month_end`, `is_quarter_start`, `is_quarter_end`, `is_year_start`, `is_year_end`: Boolean features indicating specific time periods.
- `is_weekend`: Whether the delivery was made on a weekend.
- `order_prepare_time`: Time taken to prepare the order.
- `Distance_km`: Distance between the restaurant and the delivery location.
- `Time_taken(min)`: Target variable representing the delivery time in minutes.

## Data Preprocessing

Steps involved in data preprocessing:

1. **Handling Missing Values**: Imputed missing values using the mean, median, or mode, depending on the column type.
2. **Data Type Conversion**: Converted date and time columns to appropriate formats.
3. **Feature Extraction**: Extracted additional information from existing columns (e.g., city codes from delivery person ID).
4. **Label Encoding**: Converted categorical variables into numerical values using Label Encoding.

## Feature Engineering

Feature engineering involved:

- **Time Extraction**: Extracted time-related features like order preparation time.
- **Label Encoding**: Converted categorical variables into numerical values for modeling.

## Modeling

The following models were used to predict delivery time:

- `LinearRegression()`
- `DecisionTreeRegressor()`
- `RandomForestRegressor()`
- `xgb.XGBRegressor()`

Each model was tuned using Grid Search CV to find the best hyperparameters and achieve optimal performance.

## Evaluation

Models were evaluated based on their R-squared scores and Mean Absolute Error (MAE). The best-performing model was selected for the final predictions.

## Conclusion

The project successfully demonstrated the use of machine learning models to predict food delivery times. These predictions can help businesses improve service efficiency and customer satisfaction.

