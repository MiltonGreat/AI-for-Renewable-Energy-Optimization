# Solar Energy Generation Prediction and Optimization

## Overview

This project predicts solar energy generation using meteorological and atmospheric data. It leverages machine learning techniques to analyze the relationship between weather conditions and solar power output, optimize solar panel placement, and forecast future energy generation. The project also explores how extreme weather conditions impact solar power generation.

### Project Overview

This project focuses on predicting solar energy generation (measured in megawatts) based on meteorological factors such as Direct Normal Irradiance (DNI), Global Horizontal Irradiance (GHI), wind speed, humidity, pressure, and ozone levels. The aim is to use machine learning to:

- Understand how weather conditions influence solar power output.
- Forecast future solar power generation.
- Optimize solar panel placement using location-specific meteorological data.
- Detect extreme weather events that affect solar power production.

### Data

The dataset used in this project is sourced from usaWithWeather.csv, which contains weather and solar energy data for different locations across the United States. 

The data includes:

- DNI (Direct Normal Irradiance)
- GHI (Global Horizontal Irradiance)
- Surface Albedo
- Pressure
- Wind Speed
- Precipitable Water (Humidity)
- Ozone
- Latitude and Longitude (for geospatial analysis)
- Solar Power (in MW)

### Approach

1. Data Preprocessing
- Datetime Parsing: The LocalTime column is converted into a datetime format and set as the index for easier time-based analysis.
- Feature Selection: Key meteorological features (e.g., DNI, GHI, Pressure, etc.) are selected to predict solar power generation.

2. Modeling and Prediction
- Random Forest Regressor: A Random Forest model is trained using the selected features to predict solar power generation.
- Evaluation: The model's performance is evaluated using R², MAE (Mean Absolute Error), and RMSE (Root Mean Squared Error).

3. Time Series and Seasonal Analysis
- Hourly Trends: The power generation is analyzed by hour of the day to identify daily patterns.
- Seasonal Trends: Boxplots are used to visualize solar energy generation across different months, identifying seasonal variations.

4. Geospatial Analysis
- Location-Based Optimization: A heatmap is created using Folium to visualize solar energy generation efficiency based on latitude, longitude, and elevation.
- Optimal Placement: This helps identify locations that would benefit from solar panel installation based on meteorological data.

5. Feature Impact Analysis
- Correlation Analysis: A correlation matrix is generated to study the relationship between various meteorological factors and solar power output.

6. Forecasting Solar Energy
- Prophet Model: A time series forecasting model (Prophet) is used to predict solar power generation for the next 30 days based on historical data.

7. Anomaly Detection
- Isolation Forest: Anomaly detection is used to identify extreme weather conditions that may cause a drop in solar power generation (e.g., low DNI or high wind speeds).
- Visualization: Anomalies are visualized using scatter plots and marked in the dataset for further analysis.

### Evaluation Metrics

- R² Score: Measures the proportion of variance explained by the model.
- MAE (Mean Absolute Error): Measures the average magnitude of errors in the predictions.
- RMSE (Root Mean Squared Error): Penalizes larger errors more heavily than MAE, providing an overall measure of prediction error.
- MAPE (Mean Absolute Percentage Error): Used for forecasting accuracy in future models.

### Future Work

- Deep Learning Models: Explore deep learning techniques such as LSTM (Long Short-Term Memory) or CNNs (Convolutional Neural Networks) for improved time series forecasting accuracy.
- Satellite Data Integration: Incorporate satellite-based weather data to enhance the model’s robustness and prediction accuracy.
- SHAP Analysis: Implement SHAP to explain the impact of individual features on the model's predictions.

https://www.kaggle.com/datasets/lambda21525702290303/solar-energy-prediction
