# Stock Analysis Pipeline

## Overview
This repository contains a Jupyter Notebook (`Pipline.ipynb`) designed to build a data pipeline for analyzing and forecasting a stock portfolio consisting of four blue-chip stocks listed on the Ho Chi Minh Stock Exchange (HOSE): **HPG (Hoa Phat Group)**, **VCI (Viet Capital Securities)**, **TCB (Techcombank)**, and **FPT (FPT Corporation)**. The pipeline integrates market context data from the **VNINDEX** (Vietnam Stock Index) to enhance the accuracy of financial analysis and predictions.

The project is aimed at financial analysts, fintech developers, and data scientists interested in automating stock data processing, applying machine learning (ML) techniques, and visualizing performance metrics.

## Features
- **Data Extraction**: Fetches historical price data (OHLCV: Open, High, Low, Close, Volume) for the portfolio stocks and VNINDEX using the `vnstock` library, covering the period from June 16, 2022, to June 16, 2025 (with the potential to update to the current date: October 11, 2025).
- **Data Transformation**: Computes portfolio-level metrics (e.g., weighted average close price), technical indicators (e.g., SMA20, SMA50, RSI), and targets for regression (returns) and classification (price direction: up/down).
- **Machine Learning**:
  - Regression models (Linear Regression, Decision Tree Regressor) to predict stock returns or prices.
  - Classification models (Logistic Regression, Decision Tree Classifier) to predict price movement (increase/decrease).
- **Evaluation**: Measures model performance using RMSE, MAE, Confusion Matrix, and AUC (Area Under Curve), with visualization via ROC Curve.
- **Automation**: Designed as a reusable pipeline that can be scheduled for daily updates.

## Requirements
- **Python**: Version 3.13.5 or later.
- **Dependencies**:
  - `vnstock` (for data retrieval)
  - `pandas` (data manipulation)
  - `numpy` (numerical computations)
  - `scikit-learn` (machine learning models and metrics)
  - `talib` (technical indicators, optional)
  - `matplotlib` (visualization)
- **Installation**:
  ```bash
  pip install vnstock pandas numpy scikit-learn matplotlib TA-Lib
