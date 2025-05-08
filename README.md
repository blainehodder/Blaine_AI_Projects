# Blaine’s AI Projects

Welcome to my applied machine learning portfolio with a focus on commodity trading and market prediction.

This portfolio documents my learning and development process, emphasizing:
- Transparent performance reporting.
- Practical models relevant to physical and financial commodity markets.
- Deep understanding of model mechanics, not just code execution.

## Projects

### Brent Price Predictor — Week 2 (Baseline Linear Regression)

**Goal:** Build a simple linear regression model to predict daily Brent prices.

**Tools:** Python, pandas, scikit-learn, matplotlib

**Results:**  
MAE: $1.22

**Next steps:** Add features such as moving averages, volume, or news sentiment.

---

### Brent Price Predictor — Week 3 (Feature Engineering)

**Goal:** Improve the baseline model by adding:
- Previous day's price
- Percentage change
- 5-day moving average

**Results:**  
MAE: $0.62

**Key insights:**  
Multivariate regression significantly improved accuracy. Engineered features captured momentum and smoothed volatility.

[View notebook](Brent_Price_Predictor_Week3.ipynb)

---

### Brent Price Predictor — Week 4 (Decision Tree Model)

**Goal:** Replace linear regression with a non-linear model to capture complex patterns.

**Model:** Decision Tree Regressor  
**Features:** Lagged price, percentage change, moving average

**Results:**  
MAE: $1.64

**Key insights:**  
Tree models handled non-linearities but showed a tendency to overfit without regularization.

[View notebook](Brent_Price_Predictor_Week4.ipynb)

---

### Brent-WTI Spread Predictor — Week 5 (Random Forest Model)

**Goal:** Model the monthly Brent-WTI spread using ensemble methods.

**Model:** Random Forest (100 trees, max depth 5)  
**Features:**  
- Spread_Lag1  
- Spread_Pct_Change  
- Spread_MA5

**Results:**  
MAE: $0.82

**Feature importance:**  
- Spread_Lag1: 0.854 (dominant predictor, confirming mean-reversion tendencies)

**Key insights:**  
Random Forest captured non-linear relationships and provided a robust baseline. Careful data cleaning and proper date parsing were critical, as early index formatting issues impacted model accuracy.

[View notebook](Brent_WTI_Spread_Predictor_Week5.ipynb)

---

### Brent-WTI Spread Predictor — Week 6 (XGBoost Model)

**Goal:** Apply XGBoost to improve upon the Week 5 Random Forest benchmark.

**Model:** XGBoost Regressor  
**Features:** Same as Week 5

**Results:**  
MAE: $0.87 (slightly higher than the Random Forest baseline, potentially due to conservative hyperparameters and limited tree count)

**Key learnings:**  
- Deep understanding of XGBoost mechanics:
    - How trees minimize error using gradients and Hessians.
    - Gain calculation at split points.
    - Role of learning rate as a regularization mechanism.
- Manually validated Gain calculations for all candidate splits in Tree 1 using dummy data.
- Developed an intuitive understanding of how successive trees iteratively reduce residual errors.

**Next steps:**  
Tune learning rate, tree depth, and subsampling. Introduce time series cross-validation. Expand feature set.

[View notebook](Brent_WTI_Spread_Predictor_Week6_XGBoost.ipynb)

---

## Upcoming Work

- Week 7+: Time series cross-validation, ARIMA/SARIMA exploration, and testing whether model outputs can provide actionable trading signals.
- Longer term: Deep learning models (LSTM), backtesting frameworks, and developing tear sheets.

---

## Summary of Progress

- Built and tested baseline linear and tree-based models.
- Engineered financial features including lags, percentage changes, and moving averages. Obviously simple metrics which can be easily tweaked in the future and optimized for trading.
- Implemented Random Forest and XGBoost with a deep understanding of split mechanics, Gain calculation, and regularization.
- Learned to calculate and validate boosting decisions manually.

---

## About Me

I work in refinery supply and physical oil marketing and supply.  
My goal is to integrate machine learning into trading signals, risk metrics, and portfolio construction strategies used in commodity markets.

---

## Contact

LinkedIn: [blainehodder](https://www.linkedin.com/in/blainehodder/)  
Hugging Face: [blainehodder](https://huggingface.co/blainehodder)

