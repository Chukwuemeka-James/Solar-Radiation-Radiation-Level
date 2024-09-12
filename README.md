
# Solar Radiation Prediction using XGBoost

## Overview

This project aims to **predict solar radiation** levels based on historical meteorological data. Predicting solar radiation is essential for optimizing solar energy systems, which are becoming increasingly significant as the world shifts toward renewable energy sources. By accurately forecasting solar radiation, one can better plan and manage the usage of solar panels, ensuring maximum energy generation efficiency.

The project leverages machine learning techniques, particularly **XGBoost**, which is well-suited for structured tabular data, to build a predictive model. Through this project, we explore various feature engineering, data preprocessing techniques, and hyperparameter tuning using **Optuna** to optimize the performance of the model.

## Dataset

### Context

The dataset was sourced from the **Space Apps Moscow challenge**, which was organized by NASA. It contains meteorological data points measured over the past 4 months, including attributes such as:
- **Wind Direction**: Direction from which the wind originates.
- **Wind Speed**: Measured speed of the wind.
- **Humidity**: The percentage of moisture in the air.
- **Temperature**: Recorded temperature in degrees Celsius.
- **Solar Radiation** (Target): The amount of solar energy hitting a given area (in watts per square meter).

The goal is to predict **solar radiation** using the aforementioned meteorological features.

### Columns in the Dataset
- **Wind Direction**: Numeric value representing wind direction.
- **Wind Speed**: Numeric value representing wind speed.
- **Humidity**: Percentage of humidity in the air.
- **Temperature**: Measured temperature in degrees Celsius.
- **Time-based attributes**: Year, Month, Day, Hour, Minute, and Second.
- **Sunrise and Sunset times**: Represented as hours and minutes.
- **Solar Radiation**: Target variable to predict (measured in watts per square meter).

### Acknowledgements
The dataset was generously provided by **NASA** during the Space Apps Challenge. Special thanks to NASA for making the data available and supporting climate and space research initiatives.

## Problem Statement

Given the meteorological data, the objective of this project is to **predict the level of solar radiation** for future timestamps. Accurate prediction models will help in determining when it is feasible to rely on solar energy for power generation.

## Project Workflow

1. **Data Exploration**: Understanding relationships between features such as temperature, humidity, wind speed, and solar radiation.
2. **Feature Engineering**: Extracting time-based features (year, month, day, hour, minute, second) from raw timestamps and calculating sunrise/sunset attributes.
3. **Data Preprocessing**:
   - Removing unnecessary columns such as `Year` and `SunriseHour`, which do not contribute significantly to prediction.
   - Handling missing values in the dataset.
   - Scaling features using **StandardScaler** for better model performance.
4. **Model Selection**: Using **XGBoost** as the primary machine learning algorithm.
5. **Hyperparameter Tuning**: Optimizing the XGBoost model using **Optuna**.
6. **Evaluation**: Evaluating the model using metrics like **RMSE** and comparing predicted vs actual values for the test set.