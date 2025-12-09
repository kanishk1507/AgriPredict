# Crop Yield Prediction and Agricultural Advisory System

## Project Overview

This project implements an Agricultural Prediction System using Flask, machine learning models, and rule-based systems to provide valuable insights for farmers. It offers functionalities for crop yield prediction, disease risk assessment, fertilizer recommendation, and weather pattern analysis. The system is designed to aid in informed decision-making to optimize agricultural practices and improve productivity.

## Features

- **Crop Yield Prediction**: Predicts crop yield based on environmental factors like rainfall, pesticide usage, and temperature using a Random Forest Regressor.
- **Disease Risk Assessment**: Assesses the risk of crop diseases based on environmental conditions (rainfall, temperature, pesticide usage) using a Random Forest Classifier.
- **Fertilizer Recommendation**: Provides rule-based recommendations for NPK (Nitrogen, Phosphorus, Potassium) fertilizers tailored to specific crops, rainfall, soil types, and growth stages.
- **Weather Pattern Analysis**: Analyzes historical weather data and provides future rainfall predictions using a Linear Regression model, along with general weather advice.
- **Interactive Web Interface**: A user-friendly web application built with Flask for easy interaction with the prediction models.

## Project Structure

```
Crop Yield Prediction/
├── app.py                      # Main Flask application file
├── dataset/                    # Stores raw and processed agricultural data
│   ├── pesticides.csv
│   ├── rainfall.csv
│   ├── temp.csv
│   ├── yield_df.csv
│   └── yield.csv
├── models/                     # Contains trained machine learning models and scalers
│   ├── disease_encoder.pkl
│   ├── disease_prediction_model.pkl
│   ├── disease_scaler.pkl
│   ├── fertilizer_recommender.pkl # This file is expected by app.py but not explicitly saved in training.ipynb. The system uses a rule-based fallback if not found.
│   ├── __init__.py
│   ├── prediction_models.py    # Class to load and use prediction models
│   ├── weather_model.pkl
│   ├── yield_prediction_model.pkl
│   └── yield_scaler.pkl
├── requirements.txt            # Python dependencies
├── static/                     # Static files (CSS, JS, images)
│   ├── css/
│   │   └── style.css
│   └── js/
│       ├── charts.js
│       └── main.js
├── templates/                  # HTML templates for the web application
│   ├── about.html
│   ├── base.html
│   ├── disease_prediction.html
│   ├── fertilizer_recommendation.html
│   ├── index.html
│   ├── weather_prediction.html
│   └── yield_prediction.html
└── training.ipynb              # Jupyter notebook for data analysis, model training, and evaluation
```
