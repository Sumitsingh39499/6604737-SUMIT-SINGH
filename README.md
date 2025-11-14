# 📊 *Crypto Market Data Cleaning & Analysis Project Report*

## *1. Introduction*

Cryptocurrency markets are highly volatile and data-driven. For investors and analysts, understanding daily price movements, returns, and trend patterns is essential. This project focuses on *downloading, cleaning, and preparing Bitcoin (BTC) and Ethereum (ETH) market data, followed by visual analysis using **Power BI*.

This report explains the complete workflow, including data collection, cleaning, preprocessing, and visualization steps.

---

## *2. Project Objectives*

The main objectives of this project are:

* To collect historical cryptocurrency prices (BTC & ETH).
* To clean and structure the raw data.
* To generate useful metrics such as daily returns and moving averages.
* To build Power BI dashboards for trend analysis.

---

## *3. Tools & Technologies Used*

### *Programming Language:*

* Python 3.11

### *Libraries:*

* yfinance — For downloading crypto data
* pandas — For cleaning and preprocessing data

### *Visualization Tool:*

* Microsoft Power BI Desktop

---

## *4. Data Collection*

We used the yfinance library to download daily price data for:

* *Bitcoin (BTC-USD)*
* *Ethereum (ETH-USD)*

Date range used: *From 1st January 2020 to Present*

### *4.1 Python Script Used for Downloading Data*

python
import yfinance as yf
import pandas as pd

# Download Bitcoin Data
btc = yf.download("BTC-USD", start="2020-01-01")

# Download Ethereum Data
eath = yf.download("ETH-USD", start="2020-01-01")

# Save inside data folder
btc.to_csv("data/BTC-USD.csv")
eath.to_csv("data/ETH-USD.csv")

print("Dataset downloaded")


### *4.2 Output Files Generated*

After running the script, two CSV files are created:

* BTC-USD.csv
* ETH-USD.csv

Each file contains:

* Date
* Open
* High
* Low
* Close
* Adj Close
* Volume

---

## *5. Data Cleaning & Preprocessing*

Cleaning steps performed:

### *5.1 Handling Missing Values*

* Checked for null values.
* Forward-filled missing prices.

### *5.2 Formatting the Date Column*

* Converted to proper datetime format for Power BI.

### *5.3 Calculating Daily Return*

Formula:


Daily Return = (Today's Close - Yesterday's Close) / Yesterday's Close


### *5.4 Adding Moving Averages*

* 7-day Moving Average
* 30-day Moving Average

These help visualize trends in Power BI.

---

## *6. Data Analysis in Power BI*

After importing the cleaned data, the following dashboards/visuals were created:

### *6.1 Line Chart: BTC vs ETH Closing Prices*

Shows the price trend since 2020.

### *6.2 Daily Return Chart*

Highlights market volatility.

### *6.3 Candlestick Chart*

Shows open, high, low, close for both cryptocurrencies.

### *6.4 Moving Average Trendline*

Shows smoothed trends over time.

### *6.5 Volume Analysis*

Displays trading activity.

---

## *7. Key Insights*

### *Bitcoin (BTC):*

* Highly volatile during 2020–2021 bull run.
* Shows higher market dominance.

### *Ethereum (ETH):*

* Lower price compared to BTC but higher percentage movement.
* Strong uptrend during DeFi & NFT boom.

### *Overall Market Behavior:*

* Cryptocurrencies follow similar macro trends.
* Moving averages reveal long-term stability patterns.

---

## *8. Conclusion*

This project demonstrates the complete workflow of:

* Fetching real-world financial data
* Cleaning and enriching the dataset
* Building visually interactive dashboards in Power BI

The final outcome is a clear and data-driven understanding of cryptocurrency price behavior over the last few years.

This project can be extended with:

* More cryptocurrencies
* Machine learning forecasting models
* Correlation studies with stock markets or macroeconomic indicators

---

## *9. Future Scope*

* Predict future prices using LSTM/ARIMA models.
* Create live Power BI dashboards with API integration.
* Study sentiment-driven market behavior using Twitter or Google Trends.

---

## *10. References*

* Yahoo Finance API
* Python yfinance documentation
* Power BI official documentation
