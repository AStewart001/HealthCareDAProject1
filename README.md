# HealthCareDAProject1
Automated Stock Portfolio Tracker

*A Python + MySQL + Tableau end-to-end data analytics project*

 Overview

This project tracks the performance of a personal stock portfolio using live market data.
It automates data collection, stores it in a relational database, and visualizes portfolio value and profit/loss trends in Tableau.

---

## Tech Stack

* **Python** → data extraction & ETL (`yfinance`, `mysql-connector-python`)
* **MySQL** → structured storage of transactions, prices, and P&L snapshots
* **Tableau Desktop** → interactive dashboards for weekly/monthly performance
* **Pandas / SQL** → data cleaning & aggregation

---

## Database Schema

**Tables**

1. `transactions` – buy/sell history (ticker, date, quantity, price)
2. `daily_prices` – closing price per ticker per day
3. `portfolio_pnl` – calculated daily portfolio value & unrealized P&L

---

## Workflow

1. **Record trades** manually or via CSV into `transactions`.
2. **Run Python script**

   * Fetches latest prices from Yahoo Finance
   * Updates `daily_prices` and `portfolio_pnl`
3. **Open Tableau** → refresh MySQL connection → view updated dashboards.

---

## Tableau Dashboards

* **Portfolio Value Over Time** – daily market value trend
* **Ticker-Level P&L** – current winners vs. losers
* **Weekly / Monthly Change** – ROI comparisons across time frames

Future Enhancements

* Add forecasting (Prophet / ARIMA)
* Automate daily runs via scheduler
* Email alerts for major portfolio changes
