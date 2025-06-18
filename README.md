# Pair Trading Using VECM & Kalman Filter

This project implements a pair trading strategy using two econometric techniques: **Vector Error Correction Model (VECM)** and **Kalman Filter**, applied to the historical price data of **Coca-Cola (COKE)** and **Pepsi (PEP)**.

## 📈 Overview

Pair trading is a market-neutral strategy that involves identifying two historically correlated securities, monitoring their price spread, and trading when the spread diverges from its mean. This notebook demonstrates:

- **Data preprocessing** for COKE and PEP stock prices
- **Stationarity tests** (ADF test)
- **Cointegration analysis** using Johansen test
- **VECM modeling** to identify long-run relationships
- **Kalman Filter estimation** for dynamic hedge ratios
- **Trading signal generation** and PnL visualization

## 🛠️ Technologies & Libraries

- Python 3
- pandas, numpy
- statsmodels
- matplotlib
- Google Colab (for notebook execution)

## 📂 Data

The dataset used is `YahooFinance_COKE_PEPSI_AdjClose_1990-2018.csv`, containing adjusted closing prices for COKE and PEP.

## 🔍 Methodology

1. **Visual Inspection** – Plotting COKE and PEP to confirm co-movement.
2. **Log Transformation** – Prices are log-transformed and differenced.
3. **Stationarity Testing** – ADF test checks for unit roots.
4. **Cointegration Analysis** – Johansen procedure to verify a long-run relationship.
5. **VECM** – Model the cointegrated system and generate spread.
6. **Kalman Filter** – Estimate dynamic hedge ratios in a state-space framework.
7. **Strategy Simulation** – Entry and exit signals based on spread z-scores.

## 📊 Results

The notebook includes visual plots for:

- Price series
- Residual spread from VECM
- Kalman Filter estimated hedge ratio
- Entry/exit points and cumulative PnL

## 🚀 Getting Started

### Requirements

Run the notebook in [Google Colab](https://colab.research.google.com/) or a local Jupyter environment.

### Setup

Mount Google Drive and ensure the data CSV is accessible at:
```
/content/drive/My Drive/230E/YahooFinance_COKE_PEPSI_AdjClose_1990-2018.csv
```

### Run

1. Open the notebook.
2. Run each cell sequentially.
3. Analyze plots and output.
