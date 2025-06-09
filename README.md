# StockPrizeForecasting  
# Asian Paints Stock Price Forecasting

This project aims to forecast the stock prices of Asian Paints using various data analysis and machine learning techniques. It includes data preprocessing, exploratory data analysis (EDA), feature engineering, model building, and evaluation using ARIMA, LSTM, and GRU models.

---

## Introduction

Stock price forecasting is an essential task in financial analysis, helping investors make informed decisions about buying or selling stocks. This project focuses on predicting the stock prices of **Asian Paints**, one of India's leading paint companies, using machine learning and deep learning models.

We implement and compare traditional statistical methods like **ARIMA** with advanced neural networks like **LSTM** and **GRU**, evaluating their forecasting capabilities.

---

## Dataset

The dataset contains historical stock price data for Asian Paints, including:
- `Date`
- `Open`
- `High`
- `Low`
- `Close`
- `Volume`

📅 Time Period: **2000 to 2021**

---

## Project Structure

```bash
StockPrizeForecasting/
│
├── data/
│   └── ASIANPAINT.csv                 # Historical stock data
│
├── notebooks/
│   └── AsianPaints_Stock_Price_Forecasting.ipynb  # Main notebook
│
├── src/
│   ├── preprocessing.py               # Data cleaning & scaling
│   ├── eda.py                         # Visualizations and trend analysis
│   ├── feature_engineering.py         # Time series formatting
│   ├── model_building.py              # Model training and prediction
│   └── evaluation.py                  # Evaluation metrics
│
├── requirements.txt
└── README.md

```

## Data Preprocessing

* Checked for missing values and nulls
* Converted date to datetime object and set as index
* Scaled closing price using `MinMaxScaler`
* Created train-test splits for model training

---

## Exploratory Data Analysis (EDA)

* Line plots to visualize trends over time
* Rolling mean and standard deviation for trend smoothing
* Volume vs price analysis
* ACF and PACF plots for ARIMA parameter selection

---

## Feature Engineering

* Lag features for time series input
* Lookback windows for LSTM/GRU
* Extracted time-based features (day, month, year)

---

## Model Building

### ARIMA

* Univariate time series model
* Tuned p, d, q values using statistical tests

### LSTM

* Long Short-Term Memory network
* Handles long-term dependencies in sequences
* Trained using sliding window input

### GRU

* Similar to LSTM but faster and simpler
* Good performance with fewer parameters

---

## Evaluation Metrics

* **Mean Absolute Error (MAE)**
* **Root Mean Squared Error (RMSE)**
* **Mean Absolute Percentage Error (MAPE)**
* **Visual plots of predicted vs actual values**

---

## Results

| Model | Accuracy |
| ----- | -------- |
| ARIMA | \~80%    |
| LSTM  | \~91%    |
| GRU   | \~89%    |

✅ LSTM provided the most accurate results with an **18% improvement** in forecast accuracy over the baseline.

---

## Conclusion

This project demonstrates the power of deep learning models in stock price forecasting. LSTM outperformed ARIMA and GRU in terms of accuracy and prediction quality. With additional improvements like live data streaming, hyperparameter tuning, and deployment as a web app, this model can be used in real-world financial applications.
