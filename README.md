# Deutsche-Bank-Stock-Price-Prediction-Linear-Regression-vs-LSTM
An end-to-end machine learning project that predicts the next-day closing price of Deutsche Bank stock using historical market data. The pipeline includes data preprocessing, feature engineering (lag features and moving averages), and model comparison between Linear Regression and LSTM to analyze performance and forecasting behavior
# 📌 Problem Statement

Financial time-series data are noisy, dynamic, and non-linear, making accurate stock price forecasting challenging.
The objective of this project is to:

Predict the next-day closing price of Deutsche Bank stock

Evaluate and compare the performance of Linear Regression and Long Short-Term Memory (LSTM) networks

Analyze how feature engineering and temporal modeling influence forecasting accuracy

# 🎯 Objectives

Build a reproducible data processing and modeling pipeline

Engineer time-dependent features to capture historical trends

Train and evaluate multiple predictive models

Identify strengths and limitations of classical ML vs deep learning

Propose a hybrid modeling direction

# 📊 Dataset

Source: Yahoo Finance

Timeframe: Nov 2023 – Nov 2024

Observations: 256 rows

Features:

Date (temporal)

Open, High, Low, Close, Adj Close, Volume

Target Variable: Close price

# 🔍 Exploratory Data Analysis 

Descriptive statistics for numerical features

Distribution visualization using boxplots

Outlier detection using Interquartile Range (IQR)

Finding: No significant outliers were detected in the closing price.

# Feature Engineering 
To incorporate temporal dependencies:

Lag Features: Previous day closing prices

Moving Average (window=5): Trend smoothing

Train-test split preserving chronological order

Feature scaling prior to model training

# Model Implemented 

## Linear Regression (Baseline)

Fast convergence

Works effectively with engineered static features

Provides strong interpretability

## LSTM (Recurrent Neural Network)
Designed for sequential and temporal data

Captures long-term dependencies and non-linear patterns

# Result 
Linear Regression outperformed LSTM on this dataset due to:

Limited dataset size

Noisy auxiliary features

Strong engineered linear signals
