#  Linear Regression vs LSTM for Next-Day Closing Price Forecasting

An end-to-end time-series forecasting pipeline that predicts the next-day closing price of Deutsche Bank stock using historical OHLCV data. The study benchmarks a classical regression baseline against a deep sequential model (LSTM) to analyze the impact of feature engineering versus temporal representation learning.
# 📌 Problem Statement

Financial markets exhibit:

Non-stationarity

High noise

Temporal dependencies

Regime shifts

This project investigates whether explicitly engineered temporal features (lag & moving averages) with Linear Regression can outperform end-to-end sequence learning via LSTM when data is limited.

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

# Observation:
No statistically significant outliers in Close price → suitable for regression modeling without aggressive winsorization.

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
