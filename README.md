# Syria-terrorism-forecasting
📌 Project Overview

This project presents an end-to-end data science pipeline for forecasting terrorism trends in Syria using historical data from the Global Terrorism Database (GTD). The analysis focuses on monthly attack counts between 1970 and 2017 and explicitly accounts for the structural break introduced by the Syrian Civil War in 2011.

Two complementary modeling approaches are implemented and evaluated:

SARIMAX — a classical statistical time-series model used as an interpretable baseline

LSTM (Long Short-Term Memory) — a deep learning model designed to capture non-linear escalation and momentum patterns

The objective of this project is not to predict individual attacks, but to understand temporal dynamics, volatility behavior, and early-warning signals in high-risk environments.

🎯 Key Objectives

Build a reproducible time-series forecasting pipeline

Identify and model regime shifts in conflict-driven data

Compare linear statistical models with deep learning approaches

Analyze strengths, limitations, and failure modes of each model

Generate insights relevant to risk forecasting and anomaly detection

📊 Dataset

Source: Global Terrorism Database (GTD)

Geography: Syria

Time period: 1970 – 2017

Granularity: Monthly aggregation

Data preprocessing includes:

Filtering Syria-specific incidents

Aggregating attacks at monthly frequency

Handling missing values

Creating intervention variables for structural break analysis

Note: Only aggregated, non-sensitive data is included in this repository.

🔍 Methodology
1. Exploratory Data Analysis

Time-series visualization of monthly attacks

Rolling averages to examine long-term trends

Identification of regime shift around 2011

2. Structural Break Modeling

Introduction of a binary intervention variable capturing post-2011 dynamics

Validation of regime-dependent behavior

3. Baseline Statistical Modeling (SARIMAX)

ARIMA(1,1,1) with seasonal components

Incorporation of exogenous intervention variable

Residual diagnostics and forecast evaluation

4. Deep Learning Model (LSTM)

12-month lookback window

Single hidden layer (50 neurons)

Dropout regularization

Train–test split preserving temporal order

5. Model Comparison

Trend tracking vs escalation sensitivity

Stability vs adaptability trade-offs

Evaluation using RMSE and visual diagnostics

📈 Key Findings

Terrorism activity in Syria exhibits a clear structural break in 2011, after which mean and variance increase permanently

SARIMAX effectively captures long-term baseline trends and seasonality but underestimates extreme spikes

LSTM successfully learns non-linear escalation patterns but tends to over-predict during de-escalation phases

No single model performs optimally across all regimes

Conclusion:
A hybrid ensemble approach, combining interpretable statistical baselines with deep learning–based escalation detection, provides the most robust framework for forecasting in conflict-driven systems.
