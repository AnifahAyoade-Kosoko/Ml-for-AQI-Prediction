# Air Quality Index (AQI) Prediction Using Machine Learning

This is my MSc Data Science dissertation project at the University of Wolverhampton.

## Overview

This project compares machine learning and deep learning models for predicting the Air Quality Index (AQI) in Delhi, India. It also looks at which pollutants influence air quality the most, and uses Explainable AI methods (SHAP and LIME) to make the models' predictions easier to understand.

## Data

The project uses historical AQI and pollutant data for Delhi from 2020 to 2023, with 18,776 records in total. The dataset comes from [add the dataset link here].

## Methods

I prepared the data by filling missing values with the median, capping outliers using the interquartile range, scaling the features, encoding categories and creating time-based features. Class imbalance was handled with SMOTEENN. I then trained and compared four models: Random Forest, XGBoost, LSTM and Transformer, and tuned them with grid search and randomised search. The models were evaluated using MAE, RMSE and R². SHAP was used to show which pollutants mattered most overall, and LIME was used to explain individual predictions.

## Results

Random Forest gave the lowest error, with an MAE of 0.1155 and an RMSE of 2.6069. The Transformer was next with an MAE of 0.1231 and an RMSE of 2.8910, followed by XGBoost with 0.1295 and 2.9578, and LSTM with 0.1542 and 3.2245. The SHAP analysis showed that PM10 and PM2.5 had the biggest influence on AQI.

## Limitations and Future Work

AQI is calculated from pollutant concentrations, so the models partly relearn that calculation, which explains the very high scores. A useful next step would be forecasting future AQI using lagged values and weather data. The data covers only one city, so the results may not apply to other places.

## Files

EDA.ipynb contains the exploratory data analysis. Model development.ipynb contains the preprocessing, model training and evaluation.

## Tools

Python, Pandas, NumPy, Scikit-learn, XGBoost, TensorFlow and Keras, SHAP, LIME, Matplotlib, Seaborn, Plotly and Google Colab.
