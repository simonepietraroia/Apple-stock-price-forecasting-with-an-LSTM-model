# Stock Price Forcasting With an LSTM Model

## Overview

This project explores the relationship between financial market data and predictive modelling, with a focus on forecasting Apple (`AAPL`) stock behaviour using historical price data and deep learning techniques.

The repository follows an end-to-end workflow that includes:

- Collecting stock market data  
- Cleaning and preprocessing the dataset  
- Training a predictive model  
- Evaluating model performance  
- Generating future value predictions  

Although the project title refers to *financial news sentiment analysis*, the current implementation focuses primarily on **time-series stock prediction using historical Apple stock data and an LSTM model**.

---

## Project Aim

The aim of this project is to investigate whether market movement can be modelled using machine learning and deep learning techniques, and to build a workflow that predicts future stock values from historical trading data.

---

## Repository Structure

```bash
Financial-News-Sentiment-Analysis-for-Market-Impact/
│
├── AAPL_raw.csv                  # Raw Apple stock dataset
├── collect_data.ipynb           # Data collection notebook
├── cleaning&processing.ipynb    # Data cleaning and preprocessing
├── modeling.ipynb               # Model training
├── model_evaluation.ipynb       # Model evaluation
├── predicting_value.ipynb       # Future prediction workflow
├── X_train.npy                  # Training features
├── X_test.npy                   # Test features
├── y_train.npy                  # Training labels
├── y_test.npy                   # Test labels
├── scaler.pkl                   # Saved scaler used for normalization
├── stock_lstm_model.h5          # Trained LSTM model
└── README.Rmd                   # Project documentation
```
---

## Dataset

The project uses historical stock market data for **Apple Inc. (`AAPL`)**.

The dataset contains common financial market variables including:

- Open price
- High price
- Low price
- Close price
- Volume

These values are used to construct a **time-series dataset** for predictive modelling.

---

## Methods Used

### 1. Data Collection

Historical stock data is collected programmatically using the Python library:

- `yfinance`

This allows automated downloading of financial market data directly from Yahoo Finance.

---

### 2. Data Cleaning and Preprocessing

The preprocessing stage prepares the raw financial data for modelling. This includes:

- selecting relevant columns
- handling missing values
- scaling numerical data
- transforming the dataset into sequential time-series inputs
- splitting the data into training and testing sets

A `MinMaxScaler` is used to normalize the values before feeding them into the neural network.

---

### 3. Predictive Modelling

The project uses a **Long Short-Term Memory (LSTM)** neural network.

LSTM models are well suited for:

- sequential data
- time-series prediction
- learning long-term dependencies in financial data

The trained model is saved as: stock_lstm_model.h5


---

### 4. Model Evaluation

Model performance is evaluated using regression metrics including:

- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R-squared (R²)

These metrics help determine how accurately the model predicts stock prices.

---

### 5. Forecasting

After training and evaluation, the model is used to generate **future price predictions** based on the most recent stock market data.

---

## Technologies Used

The project was built using the following technologies:

- Python
- Jupyter Notebook
- pandas
- numpy
- scikit-learn
- tensorflow / keras
- matplotlib
- yfinance

---

## Project Workflow

1. Collect historical AAPL stock data

2. Clean and preprocess the dataset

3. Split the data into training and testing sets

4. Scale the data for neural network training

5. Train the LSTM model

6. Evaluate model performance

7. Predict future stock values


---

## Example Research Questions

This project explores questions such as:

- Can historical stock data be used to forecast future price movements?
- How effective is an LSTM model for financial time-series prediction?
- What limitations exist when applying deep learning models to financial markets?

---

## Model Performance

Evaluation results from the trained model include:

| Metric | Value |
|------|------|
| RMSE | 23.19 |
| MAE | 21.70 |
| R² Score | 0.0287 |

These results indicate that the model learns some structure from the data, but financial markets remain highly complex and difficult to predict.

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/simonepietraroia/Financial-News-Sentiment-Analysis-for-Market-Impact.git
cd Financial-News-Sentiment-Analysis-for-Market-Impact

### 2. Install dependencies

```bash
pip install pandas numpy scikit-learn tensorflow matplotlib yfinance
