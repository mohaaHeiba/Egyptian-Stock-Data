# Egyptian Stock Market Intraday Dataset

## Dataset Overview
This repository hosts a high-fidelity, pre-processed intraday dataset for **Fawry (FWRY)**, a leading stock in the Egyptian Exchange (EGX30).

The dataset is engineered specifically for **Deep Learning (LSTM) training**, bridging the gap in available high-frequency financial data for the Egyptian market. It contains **20,000+ records** with a **1-minute time interval**, processed to include technical indicators and predictive targets.

## Data Specifications
* **Stock Symbol:** `FWRY.CA`
* **Timeframe:** 1-Minute Interval (Intraday)
* **Total Records:** +20,000 Rows
* **Format:** CSV (Comma Separated Values)
* **Processing Status:** Cleaned, Sorted, and Feature Engineered.

## Features Dictionary (Columns)
The dataset includes raw market data combined with calculated technical indicators:

| Column Name | Description |
| :--- | :--- |
| `datetime` | Timestamp in `YYYY-MM-DD HH:MM:SS` format. |
| `open` | Opening price of the candle. |
| `high` | Highest price reached in the minute. |
| `low` | Lowest price reached in the minute. |
| `close` | Closing price (Primary feature for prediction). |
| `volume` | Number of shares traded. |
| `RSI` | **Relative Strength Index (14):** Momentum indicator to detect overbought/oversold conditions. |
| `SMA_20` | **Simple Moving Average (20):** Short-term trend indicator. |
| `Momentum` | Price change momentum over the last 10 minutes. |
| `Target_Change` | **Predictive Target:** The percentage change in price **5 minutes into the future**. |

## Usage with Python
You can load this dataset directly into Pandas for model training:
