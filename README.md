# Blaine’s AI Projects

Welcome to my applied machine learning portfolio with a focus on commodity trading and market prediction.

This portfolio documents my learning and development process, emphasizing:

- Transparent performance reporting  
- Practical models relevant to physical and financial commodity markets  
- Deep understanding of model mechanics, not just code execution  

---

## Projects

### Brent Price Predictor — Week 2 (Baseline Linear Regression)

**Goal:** Build a simple linear regression model to predict daily Brent prices.

**Tools:** Python, pandas, scikit-learn, matplotlib  
**Results:** MAE: $1.22  

**Next steps:** Add features such as moving averages, volume, or news sentiment.

---

### Brent Price Predictor — Week 3 (Feature Engineering)

**Goal:** Improve the baseline model by adding:
- Previous day's price
- Percentage change
- 5-day moving average

**Results:** MAE: $0.62  
**Key insights:**  
Multivariate regression significantly improved accuracy. Engineered features captured momentum and smoothed volatility.

[View notebook](Brent_Price_Predictor_Week3.ipynb)

---

### Brent Price Predictor — Week 4 (Decision Tree Model)

**Goal:** Replace linear regression with a non-linear model to capture complex patterns.  
**Model:** Decision Tree Regressor  
**Features:** Lagged price, percentage change, moving average  
**Results:** MAE: $1.64  

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

**Results:** MAE: $0.82  
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
**Results:** MAE: $0.87

**Key learnings:**
- Deep understanding of XGBoost mechanics:
  - Gradient/Hessian-based split optimization
  - Gain calculation at split points
  - Regularization via learning rate, depth, subsampling
- Manually validated Gain calculations using dummy data
- Developed intuition for residual error reduction across boosting rounds

**Next steps:**  
Tune hyperparameters. Add time series CV. Expand feature set.

[View notebook](Brent_WTI_Spread_Predictor_Week6_XGBoost.ipynb)

---

### Brent-WTI Regime-Sliced Signal — Week 7 (Classification with Sentiment Overlay)

**Goal:** Improve directional prediction of Brent-WTI spread moves by conditioning on market structure and layering in headline sentiment.

**Additions:**
- Trader-style regime flags: curve structure (contango/backwardation), volatility buckets
- Lagged VADER sentiment score (from oil-related headlines)
- Proxy inventory "surprise" based on 4-week rolling mean
- Shift from regression to XGBoost 3-class classification (up / flat / down)

**Key outputs:**
- Classification performance by market regime
- Sentiment overlay analysis (filtering/fading signals)
- Exploratory SHAP visualization for signal attribution (optional)

**Next steps:**  
Polish model and migrate to `Trading_Signal_Research` once performance is scoped and documented.

[View notebook](week-07-brent-wti-regime-signal/brent_wti_regime_signal.ipynb)

---

## Upcoming Work

- Week 8: Composite feature signal table and conditional classifiers  
- Week 9+: Regime-aware signal stacking, SHAP-based feature filtering  
- Long-term: Backtesting framework, tear sheets, LSTM exploration, VaR & stress testing

---

## Summary of Progress

- Built and tested linear and tree-based models on price and spread data
- Engineered financial features (lags, % changes, moving averages)
- Built interpretable ensemble models (Random Forest, XGBoost)
- Learned and manually validated model mechanics (split math, boosting logic)
- Incorporated trader logic and NLP sentiment into early directional signal prototypes

---

## About Me

I work in refinery supply and physical oil marketing and logistics.  
My goal is to integrate machine learning into trading signals, portfolio structure, and risk metrics for real-world commodity market application.

---

## Contact

**LinkedIn**: [blainehodder](https://www.linkedin.com/in/blainehodder/)  
**Hugging Face**: [blainehodder](https://huggingface.co/blainehodder)
