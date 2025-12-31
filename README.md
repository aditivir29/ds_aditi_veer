## Web3 Trading Behavior vs Market Sentiment
## Objective

Analyze how trader behavior on Hyperliquid (profitability, returns, trade direction) aligns or diverges from Bitcoin market sentiment (Fear vs Greed), and identify patterns that can inform smarter trading strategies in a Web3 environment.

## Repository Structure

This repository strictly follows the required standardized format:

ds_aditi_veer/
├── notebook_1.ipynb
├── csv_files/
│   ├── hyperliquid_cleaned.csv
│   ├── sentiment_cleaned.csv
│   └── merged_data.csv
├── outputs/
│   ├── pnl_distribution_sentiment.png
│   ├── avg_return_sentiment.png
│   ├── win_rate_sentiment.png
│   └── pnl_heatmap_sentiment_direction.png
├── ds_report.pdf
└── README.md

## Google Colab Notebook

All analysis was performed in Google Colab.

Notebook: notebook_1.ipynb

## Colab Link:
https://colab.research.google.com/drive/1JIxQELPuxc5dD_qQIsbe4cLe1JPAJ0Dl?usp=sharing

Access: Anyone with the link → Viewer

## Datasets Used
## 1. Bitcoin Market Sentiment (Fear & Greed Index)

Columns:

timestamp

classification (Fear / Greed)

## 2. Hyperliquid Historical Trader Data

Columns include:

account, coin

execution_price

size_tokens, size_usd

direction (Long / Short)

closed_pnl

timestamp_ist

## Data Cleaning & Feature Engineering

Standardized column naming

Converted timestamps to datetime

Daily-level merge between sentiment and trades

Removed zero-notional trades

## Engineered features:

notional = execution_price × size_tokens

return_pct = closed_pnl / notional

profit_flag for win-rate calculation

Cleaned datasets are stored in the csv_files/ directory.

Analysis Performed

Profitability comparison across sentiment regimes

Average return analysis (Fear vs Greed)

Directional bias (Long vs Short)

Win-rate analysis by sentiment

Heatmap analysis of PnL vs sentiment and trade direction

## Key Insights

Market sentiment significantly impacts trader performance

Greed phases show higher average returns with higher volatility

Fear phases reflect more conservative trading behavior

Directional bias shifts across sentiment regimes

Sentiment acts as a contextual risk signal, not a standalone predictor

Detailed findings are documented in ds_report.pdf.

## Visual Outputs

All charts and visualizations generated during EDA are saved in the outputs/ directory.

## Tools & Technologies

Python

Google Colab

pandas, numpy

matplotlib, seaborn

## Notes

Folder and file naming strictly comply with assignment instructions

GitHub repository mirrors the Google Colab project structure exactly

All outputs and intermediate data files are reproducible

## Author

Aditi Veer
Data Science | Web3 Analytics
Savitribai Phule Pune University
