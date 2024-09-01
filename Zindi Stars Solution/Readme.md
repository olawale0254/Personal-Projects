# Uber Traffic Incident Prediction (ZINDI 3rd Place Solution)

This project aims to predict traffic incidents on road segments in Cape Town, South Africa using machine learning models.

## Overview

The main components are:

- Data preprocessing and feature engineering
- Training LightGBM and CatBoost models 
- Ensembling predictions from both models

## Data

The data includes:

- Historical traffic incident records
- Road segment information 
- Weather data
- Geospatial features

Key preprocessing steps:

- Aggregating incidents to hourly level per road segment
- Extracting time-based features
- Merging road and w