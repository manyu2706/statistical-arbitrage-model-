# statistical-arbitrage-model-
# Statistical Arbitrage (Pairs Trading) on NIFTY 50

This project implements a fully automated **statistical arbitrage (pairs trading)** strategy using NIFTY 50 equities, exploiting mean-reversion in cointegrated asset pairs.

---

## 📌 Strategy Overview
- Universe: NIFTY 50 stocks (Yahoo Finance)
- Time Period: Apr 2015 – Mar 2024
- Market Benchmark: NIFTY 50 Index (^NSEI)

---

## 🔍 Methodology
1. **Data Cleaning**
   - Forward & backward filling
   - Assets with excessive missing data removed

2. **Pair Selection**
   - Engle-Granger cointegration test (p < 0.05)
   - Correlation ranking using daily log returns

3. **Trading Logic**
   - Spread constructed via OLS hedge ratio
   - Z-score based signals:
     - Enter trade at |Z| > 2
     - Exit at Z ≈ 0
   - Market-neutral long-short positions

4. **Automation**
   - Strategy iterates through ranked pairs
   - Stops when a profitable pair is identified

---

## 📈 Results (Sample Profitable Pair)
**HDFCBANK vs KOTAKBANK**
- Annualized Return: **25.29%**
- Annualized Volatility: **22.58%**
- Sharpe Ratio: **1.12**
- Portfolio Beta vs NIFTY 50: **0.06**
- Annualized Alpha: **21.79%**

---

## 🧮 Risk Metrics
- Individual stock beta & alpha vs NIFTY 50
- Portfolio-level alpha & beta
- Volatility-adjusted performance (Sharpe)

---

## 🛠 Tools & Libraries
- Python
- pandas, numpy
- statsmodels
- yfinance
- matplotlib, seaborn

---

## ⚠️ Notes & Limitations
- No transaction costs included
- Assumes continuous rebalancing
- Survivorship bias possible due to current NIFTY constituents

---

## ▶️ Run the Notebook
You can run this project directly on Google Colab:  
🔗 **[Colab Link](https://colab.research.google.com/drive/1R3JnG9FnAcu2bg-TRrt1H33BW80FEuKk?usp=sharing#scrollTo=LoHS4fIfYrBd)**

---

## 📄 Author
Abhimanyu Goel

