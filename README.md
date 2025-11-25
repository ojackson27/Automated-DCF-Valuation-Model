# 📈 Automated DCF Valuation Model (Python)

##  Project Overview
This project is an automated financial modeling tool built in Python. It performs a **Discounted Cash Flow (DCF)** analysis to determine the intrinsic value of public companies.

Unlike static Excel models, this script connects directly to live market data APIs to fetch up-to-date financial statements, automates the calculation of Free Cash Flow (FCF) and revenue growth, and projects future value using a rigorous 2-stage growth model.

##  Key Features
* **Live Data Integration:** Leverages the `yfinance` library to scrape real-time Balance Sheet, Income Statement, and Cash Flow data.
* **Dynamic Forecasting:** Automatically calculates historical growth rates to project FCF for the next 5 years.
* **Valuation Engine:** Implements a standard WACC-based discounting mechanism and Terminal Value calculation (Gordon Growth Method).
* **Investment Verdict:** Compares the calculated "Fair Value" against the live market price to generate a "Buy/Sell" recommendation with specific upside/downside percentages.

##  Technologies Used
* **Python 3.x**
* **yfinance** (Data ingestion)
* **Pandas** (Data manipulation and financial statement parsing)

##  Example Output
*Running the model on Apple Inc. (AAPL) [Nov 2025]:*

```text
--- ANALYST DASHBOARD ---
Ticker: AAPL
Latest FCF:       $98,767,000,000
Revenue Growth:   6.42%

--- VALUATION SUMMARY ---
Estimated Fair Value:  $111.95
Current Market Price:  $278.95
Upside/Downside:      -59.87%
Recommendation:        SELL (Overvalued)
