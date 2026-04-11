# 📊 SEO Underwriting Fee Analysis

## 🔍 Overview

This project analyzes the key drivers of underwriting fees for Seasoned Equity Offerings (SEOs) in the United States.

Using regression modelling, time series forecasting, and decision tree analysis, the project identifies the main factors influencing underwriting costs and estimates future fee levels.

Key Insight:
Larger firms and larger equity offerings consistently pay lower underwriting fees, highlighting strong economies of scale in capital markets.

## 🎯 Objective
- What factors influence SEO underwriting fees?
- Do larger firms and larger deals receive lower fees?
- What are the expected fee levels for 2026–2027?
- Which variables are most important in predicting fees?

## 📁 Data

The analysis uses a dataset of approximately 17,500 U.S. SEO transactions.

Key variables include:

- Underwriting fees (%)
- Issue size (principal amount)
- Post-offering market value
- Offer price
- Exchange
- Industry
- Year
  
## ⚙️ Methodology

a) Data Preparation
- Cleaned and standardised financial variables
- Removed missing and invalid observations
- Applied winsorisation to reduce outlier impact
- Created log-transformed variables for financial features
- Converted categorical variables (exchange, industry, year)

b) Exploratory Analysis
- Fee distribution is relatively stable, with most values between 3.9% and 6.0%
- Financial variables are highly skewed, reflecting variation between small and large firms
- Strong negative relationship between firm size and fees (r ≈ -0.67)

c) Regression Modelling
- OLS regression used to identify key drivers of underwriting fees
- Market value and issue size show strong negative relationships with fees
- Models explain a substantial portion of variation (R² ≈ 0.5)

👉 Interpretation:
Larger firms and larger offerings benefit from lower percentage issuance costs

d) Forecasting SEO Fees
- Time series model (AR(1)) applied to yearly average fees
- Model selected based on AIC comparison
- Forecasted average fees: ~4.8% (2026), ~5.0% (2027)

👉 Interpretation:
Underwriting fees are stable over time, with no major structural shifts expected

e) Variable Importance
- Decision tree model used to assess predictor importance
- Key result: Market value is the most important factor, followed by issue size and deal characteristics

👉 Confirms robustness of regression findings

## 📌 Key Findings
- Larger firms consistently pay lower underwriting fees
- Larger issue sizes are associated with lower percentage fees
- Firm size is the dominant driver of underwriting costs
- Fees remain relatively stable over time
- Forecasts suggest average fees around 4.8%–5.0% in the near term

## 💡 Implications
- Investment banks benefit from economies of scale when underwriting larger deals
- Smaller firms face higher relative issuance costs
- Stable fee structure suggests a mature and competitive underwriting market

## ⚠️ Limitations
- Based on historical U.S. SEO transactions
- Some drivers (e.g. firm risk, market conditions) are not fully captured
- Forecast assumes similar future market conditions
  
## 🛠️ Tools Used
- Python (pandas, numpy, statsmodels)
- Data visualization (matplotlib, seaborn)
- Time series modelling (ARIMA)
- Machine learning (decision tree)

This project was adapted from a university team assignment and rebuilt independently as a portfolio project. The GitHub version reflects a cleaned, individual presentation of the analysis.
