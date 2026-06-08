# Hyperliquid Trader Performance Analysis Using Bitcoin Market Sentiment

## Overview

This project explores the relationship between trader performance and Bitcoin market sentiment by combining historical Hyperliquid trading data with the Bitcoin Fear & Greed Index.

The objective is to understand how market sentiment influences trader profitability, win rates, trading activity, asset performance, position sizing, and overall trading behavior.

---

## Problem Statement

Market sentiment is one of the most influential drivers of cryptocurrency markets. By integrating trader-level transaction data with sentiment indicators, we aim to uncover behavioral patterns and identify market conditions that lead to superior trading performance.

Key questions explored:

* Does trader profitability vary across market sentiment regimes?
* Which sentiment conditions produce the highest win rates?
* Which assets perform best under different sentiment environments?
* How concentrated is profitability among traders?
* Does larger position sizing lead to higher profitability?

---

## Dataset Information

### 1. Hyperliquid Historical Trader Data

Contains:

* Account
* Coin
* Execution Price
* Size Tokens
* Size USD
* Side
* Direction
* Closed PnL
* Fee
* Timestamp
* Transaction Details

Records Analyzed:

**211,224+ trades**

---

### 2. Bitcoin Fear & Greed Index

Contains:

* Date
* Sentiment Value
* Classification

Sentiment Categories:

* Extreme Fear
* Fear
* Neutral
* Greed
* Extreme Greed

Records Analyzed:

**2,644 sentiment observations**

---

## Methodology

### Data Preparation

* Cleaned trader and sentiment datasets
* Converted timestamps into comparable date formats
* Merged sentiment data with trade records using trade date
* Removed unmatched observations

### Realized Trade Filtering

Only realized trading actions were analyzed:

* Close Long
* Close Short
* Sell

Opening transactions and non-PnL events were excluded to prevent distortion of profitability metrics.

### Exploratory Data Analysis

Analyzed:

* Sentiment Distribution
* Profitability by Sentiment
* Win Rate by Sentiment
* Asset-Level Performance
* Trader-Level Performance
* Position Size Analysis
* Fee Analysis
* Correlation Analysis

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Key Findings

### Market Sentiment Significantly Influences Performance

| Sentiment     | Avg PnL |
| ------------- | ------- |
| Extreme Greed | 130.20  |
| Fear          | 111.81  |
| Greed         | 83.09   |
| Extreme Fear  | 72.18   |
| Neutral       | 71.05   |

Extreme Greed delivered the highest average profitability.

---

### Extreme Greed Produced the Highest Win Rate

| Sentiment     | Win Rate |
| ------------- | -------- |
| Extreme Greed | 89.12%   |
| Fear          | 87.10%   |
| Neutral       | 82.14%   |
| Greed         | 76.34%   |
| Extreme Fear  | 76.16%   |

Strong sentiment environments generated better outcomes than neutral conditions.

---

### Fear Markets Outperformed Normal Greed

One of the most interesting findings was that Fear markets generated higher profitability and win rates than standard Greed periods.

This suggests that volatility-driven opportunities may provide favorable conditions for skilled traders.

---

### Profitability Is Highly Concentrated

* Total Traders: 32
* Top 10 Traders Contribution: 84.14%

A small subset of traders captured the majority of profits, highlighting the importance of strategy quality and execution skill.

---

### Top Performing Assets

Highest profit-generating assets:

* @107
* HYPE
* SOL
* ETH
* BTC

SOL and ETH demonstrated particularly strong profitability across multiple sentiment regimes.

---

### Position Size Is Not the Main Driver of Profitability

Correlation between Position Size and Closed PnL:

0.1636

This weak positive relationship indicates that larger trades alone do not guarantee better performance.

---

## Strategic Recommendations

### 1. Utilize Sentiment-Aware Trading Strategies

Adjust trading approaches based on prevailing market sentiment conditions.

### 2. Capitalize on Extreme Greed Momentum

Extreme Greed environments historically delivered the highest profitability and win rates.

### 3. Exploit Volatility During Fear Markets

Fear conditions consistently generated strong trading opportunities despite negative sentiment.

### 4. Prioritize Strategy Quality Over Position Size

Results indicate that profitability is more dependent on execution quality than trade size.

### 5. Monitor High-Performing Traders

Given the concentration of profits among a small subset of accounts, behavioral analysis of successful traders may provide valuable insights.

---

## Repository Structure

```text
primetrade-market-sentiment-analysis/

├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── 01_data_inspection.ipynb
│
├── outputs/
│   ├── figures/
│   └── tables/
│
├── requirements.txt
└── README.md
```

---

## Conclusion

This analysis demonstrates that Bitcoin market sentiment has a measurable impact on trader behavior and performance. Extreme Greed and Fear regimes consistently produced the strongest results, while profitability was shown to be highly concentrated among a small number of traders.

The findings suggest that incorporating sentiment indicators into trading decision frameworks can improve market awareness, risk management, and overall strategy effectiveness.

---

**Author:** Pralisha Tripathy
**Project Type:** Data Science / Quantitative Trading Analytics
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook
