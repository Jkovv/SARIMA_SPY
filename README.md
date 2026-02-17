# SARIMA Forecasting (SPY)

Time series forecasting of the **SPDR S&P 500 ETF (SPY)** using a Seasonal AutoRegressive Integrated Moving Average (SARIMA) model.  
This project demonstrates financial market forecasting with classical statistical modeling in Python.

---

## Project Overview

The notebook builds and evaluates a SARIMA model to analyze and forecast SPY price movements. It covers:

- Historical data retrieval
- Time series preprocessing
- Stationarity testing
- Parameter selection
- Model training
- Forecast generation
- Visualization of predictions vs. actual values

The goal is to explore how seasonal ARIMA models perform on equity market data.

---

## Data Source

Market data for SPY is obtained via financial data APIs (e.g., Yahoo Finance through `yfinance`).

Typical fields used:

- Date
- Open
- High
- Low
- Close
- Adjusted Close
- Volume

---

## Tech Stack

- **Python**
- **Jupyter Notebook**
- **pandas** - data manipulation  
- **numpy** - numerical computing  
- **matplotlib / seaborn** - visualization  
- **statsmodels** - SARIMA modeling  
- **yfinance** - financial data retrieval  

---

## Methodology

### 1. Data Collection
- Download historical SPY price data.
- Set date as index for time series structure.

### 2. Data Preprocessing
- Handle missing values.
- Convert to appropriate frequency.
- Plot raw time series.

### 3. Stationarity Check
- Augmented Dickey–Fuller (ADF) test.
- Differencing applied if needed.

### 4. Parameter Selection

SARIMA parameters:

- **p** - autoregressive order  
- **d** - differencing order  
- **q** - moving average order  
- **P, D, Q, s** - seasonal components  

ACF/PACF plots guide parameter tuning.

### 5. Model Training
- Fit SARIMA using `statsmodels`.
- Evaluate AIC/BIC for model quality.

### 6. Forecasting
- Generate out-of-sample predictions.
- Produce confidence intervals.

### 7. Visualization
- Forecast vs. historical data.
- Residual diagnostics.

---

## How to Run

```bash
# Clone repo
git clone https://github.com/Jkovv/SARIMA_SPY.git
cd SARIMA_SPY

# Install dependencies
pip install pandas numpy matplotlib seaborn statsmodels yfinance notebook

# Launch notebook
jupyter notebook SARIMA_SPY.ipynb
