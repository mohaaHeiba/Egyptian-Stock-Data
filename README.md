# Egyptian Stock Market Intraday Datasets

High-frequency 1-minute intraday dataset for EGX stocks , pre-processed and feature-engineered with RSI, SMA, and predictive targets for LSTM/Deep Learning models. 

## Overview
This repository hosts a collection of **high-fidelity, pre-processed intraday datasets** for top-performing companies in the **Egyptian Exchange (EGX30)**.

The datasets are engineered specifically for **Deep Learning (LSTM) training**, bridging the gap in available high-frequency financial data for the Egyptian market. Each dataset contains **20,000+ records** with a **1-minute time interval**, processed to include technical indicators and predictive targets.

> **Methodology:** Data was aggregated using manual exports from TradingView Pro and verified against Yahoo Finance to ensure accuracy and continuity.

## Available Stocks (Tickers)
The repository includes processed data for the following market leaders:

* **FWRY** (Fawry for Banking Technology)
* **COMI** (Commercial International Bank)
* **EAST** (Eastern Company)
* **HRHO** (EFG Hermes)
* **ETEL** (Telecom Egypt)
* **SWDY** (Elsewedy Electric)
* **TMGH** (Talaat Moustafa Group)
* **ABUK** (Abou Kir Fertilizers)
* **EFIH** (e-finance)
* **ORAS** (Orascom Construction)
* And others (EMFD, EXPA, IRON, etc.)

## Data Specifications
* **Timeframe:** 1-Minute Interval (Intraday).
* **Total Records:** +20,000 Rows per stock.
* **Format:** CSV (Comma Separated Values).
* **Processing Status:** Cleaned, Sorted, and Feature Engineered.

## 🛠 Features Dictionary (Columns)
Each dataset includes raw market data combined with calculated technical indicators:

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
You can load any stock dataset directly into Pandas for model training.



print(f"Loaded {len(df)} records for {url}")
print(df.head())
