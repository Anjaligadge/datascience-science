# Trader Performance vs Market Sentiment Analysis

##  Overview
This project analyzes the relationship between **Bitcoin market sentiment (Fear/Greed Index)** and **trader performance** using historical trading data from Hyperliquid.

The objective is to uncover behavioral patterns and performance trends that can help design **data-driven trading strategies** and improve decision-making.

---

## Datasets Used

### 1. Bitcoin Market Sentiment Dataset
- Columns:
  - `Date`
  - `Classification` (Fear / Greed)

### 2. Historical Trader Data (Hyperliquid)
- Columns include:
  - `account`
  - `symbol`
  - `execution price`
  - `size`
  - `side` (Buy/Sell)
  - `time`
  - `closedPnL`
  - (other trading-related fields)

---

##  Methodology

###  Data Preparation
- Loaded datasets using **Pandas**
- Converted timestamps to datetime format
- Extracted date for alignment
- Merged datasets on **date level**
- Handled missing values and removed inconsistencies

---

###  Feature Engineering
Created additional features for analysis:
- `profit` → whether trade resulted in profit
- `loss` → whether trade resulted in loss
- `absPnL` → magnitude of profit/loss
- Trade counts per day
- Buy/Sell distribution

---

###  Exploratory Data Analysis

####  Performance vs Sentiment
- Compared **average PnL** across Fear and Greed periods
- Evaluated **win/loss behavior**

####  Trader Behavior Analysis
- Trade frequency by sentiment
- Buy vs Sell patterns
- Position sizing trends

####  Trader Segmentation
- High activity vs low activity traders
- Profitable vs loss-making traders

---

##  Key Insights

1. **Higher losses observed during Fear periods**, likely due to increased uncertainty and panic-driven trading.

2. **Trading activity increases during Greed periods**, but this is accompanied by higher volatility and risk.

3. **Frequent traders adapt better to sentiment changes**, showing more consistent performance compared to infrequent traders.

---

##  Strategy Recommendations

1. Reduce position sizes and avoid aggressive trading during **Fear periods**.

2. Increase trading activity cautiously during **Greed periods**, while maintaining strict risk management.

3. Frequent traders should dynamically adjust strategies based on sentiment signals.

4. Avoid overtrading during high volatility conditions.

5. Focus on **risk management and consistency** rather than maximizing short-term gains.

---

##  Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

---

##  How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Trader_Sentiment_Analysis.git
