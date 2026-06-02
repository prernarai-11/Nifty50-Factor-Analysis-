# Nifty 50 Multi-Factor Investing Strategy Analysis (2019–2024)

## Project Overview

Built a systematic multi-factor investing strategy to evaluate whether factor-based stock selection can outperform the Nifty 50 benchmark.

Using six years of historical data, I created a monthly rebalanced portfolio using three factors — Momentum, Low Volatility, and Mean Reversion — and backtested performance against the Nifty 50 index.

This project combines:

* Financial data analysis
* Factor engineering
* Portfolio construction
* Backtesting & performance evaluation
* Cloud data engineering using Databricks & Delta Lake

---

## Business Question

**Can a systematic factor-based strategy outperform the Nifty 50 while improving risk-adjusted returns?**

---

## Key Results

* **207% total return** vs **97% benchmark return**
* **10.8% annualized alpha**
* **Sharpe Ratio:** 1.35 vs 0.83 benchmark
* **Maximum Drawdown:** -17.8% vs -23.2%
* Lower downside during the COVID crash
* Consistent monthly outperformance across the backtest period

---

## Project Pipeline

```text
Yahoo Finance Data
        ↓
Data Cleaning & Validation
        ↓
Exploratory Data Analysis
        ↓
Factor Engineering
        ↓
Stock Ranking Model
        ↓
Portfolio Construction
        ↓
Backtesting
        ↓
Performance Evaluation
```

---

## Architecture

```text
Yahoo Finance
      ↓
Databricks
      ↓
Delta Lake Storage
      ↓
Apache Spark Processing
      ↓
Jupyter Analysis Layer
      ↓
Factor Model & Backtesting
```

---

## Factors Built

### 1. Momentum

Measures past 12-month performance while excluding the most recent month.

Purpose:

* Capture trend persistence
* Identify strong performers

---

### 2. Low Volatility

Uses rolling volatility over six months.

Purpose:

* Reduce downside risk
* Reward stable stocks

---

### 3. Mean Reversion

Measures recent short-term underperformance.

Purpose:

* Capture short-term reversals
* Identify potential recovery candidates

---

## Dataset

| Metric            | Value           |
| ----------------- | --------------- |
| Universe          | Nifty 50 Stocks |
| Final Stocks Used | 49              |
| Historical Period | 2019–2024       |
| Trading Days      | 1480            |
| Benchmark         | Nifty 50 Index  |

---

## Notebook Structure

The project is organized inside a single notebook with clearly separated sections:

```text
1. Problem Statement & Objective

2. Data Collection

3. Data Cleaning & Validation

4. Exploratory Data Analysis

5. Factor Construction
   - Momentum
   - Low Volatility
   - Mean Reversion

6. Factor Combination & Ranking

7. Portfolio Construction

8. Backtesting

9. Performance Evaluation

10. Databricks & Delta Lake Integration

11. Limitations

12. Conclusion
```

---

## Visualizations Included

* Growth of ₹100 invested across stocks
* Sector performance analysis
* Correlation heatmap
* Volatility analysis
* Factor ranking chart
* Strategy vs Benchmark cumulative returns

---

## How to Run

Clone repository:

```bash
git clone <repository_url>
cd nifty50-factor-analysis
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run:

```text
Open:
nifty50_factor_analysis.ipynb

Run notebook from top to bottom.
```

---

## Tech Stack

### Languages & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* yFinance

### Cloud & Big Data

* Databricks
* Apache Spark
* Delta Lake

---

## Limitations

Results should be interpreted with caution due to:

* Survivorship bias (current Nifty constituents used)
* Transaction costs not included
* Monthly rebalancing costs ignored

Estimated realistic alpha after costs:

**~7–9% annually**

---

## Conclusion

The factor-based strategy significantly outperformed the benchmark while delivering stronger risk-adjusted returns and lower downside risk.

This project demonstrates practical applications of:

* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* Financial Analytics
* Backtesting
* Cloud Data Engineering
* Systematic Investing
