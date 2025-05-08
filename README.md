# Blaine’s AI Projects

Welcome to my AI portfolio. I’m building applied machine learning and deep learning models focused on commodity trading use cases.

## Projects

---

### **Brent Price Predictor — Week 2 (Baseline Linear Regression)**

**Goal:** Build a simple linear regression model to predict daily Brent prices based on previous prices.

**Tools:** Python, pandas, scikit-learn, matplotlib

**Results:** 
* Model trained and tested on historical Brent price data.
* Mean Absolute Error (MAE): $1.22

**Next Steps:** Explore adding more features like moving averages, volume, or news sentiment.

---

### **Brent Price Predictor — Week 3 (Feature Engineering)**

**Goal:** Improve the baseline linear regression model by adding engineered features:
* Previous day's price
* Percentage change from the previous day
* 5-day moving average of price

**Tools:** Python, pandas, scikit-learn, matplotlib

**Model:** Multiple linear regression using three input features.

**Results:** 
* Model trained and tested on historical Brent price data.
* Mean Absolute Error (MAE): $0.62

**Key Insights:**
* Moving averages help smooth out noise and random daily price shocks.
* Percentage change captures relative price movements and momentum effects.
* Multivariate regression allows the model to weight multiple predictors and adjust for confounding relationships.

**Next Steps:** Explore additional features such as volatility measures or rolling volume. Consider testing more advanced models (Random Forest, Gradient Boosting) for comparison.

[View the notebook here](Brent_Price_Predictor_Week3.ipynb)

---

### **Brent Price Predictor — Week 4 (Decision Tree Model)**

**Goal:** Replace linear regression with a non-linear model (Decision Tree) to capture complex patterns in Brent price data.

**Tools:** Python, pandas, scikit-learn, matplotlib

**Model:** Decision Tree Regressor with price_previous, pct_change, and ma_5 as input features.

**Results:** 
* Model trained and tested on historical Brent price data.
* Mean Absolute Error (MAE): $1.64

**Key Insights:**
* Decision trees automatically handle non-linear relationships and feature interactions.
* Feature importances revealed which engineered features contributed most to predictions.
* This is the first step toward building models that can eventually inform trading signals, not just predictions.

**Next Steps:** Implement ensemble models (Random Forest, XGBoost) and begin evaluating whether model outputs can translate into tradeable signals with backtesting.

[View the notebook here](Brent_Price_Predictor_Week4.ipynb)

---

### **Brent-WTI Spread Predictor — Week 5 (Random Forest Model)**

**Goal:** Model the monthly Brent-WTI spread using Random Forests to capture nonlinear relationships and feature interactions.

**Tools:** Python, pandas, scikit-learn, matplotlib

**Features Used:**
* Spread Lag 1 (previous month’s spread)
* Percentage change in spread
* 5-month moving average of the spread

**Model:** Random Forest Regressor (100 trees, max depth 5)

**Results:**  
* Mean Absolute Error (MAE): $1.39
* Feature Importance:
  * Spread_Lag1: 0.854
  * Spread_Pct_Change: 0.042
  * Spread_MA5: 0.103

**Key Insights:**
* Lagged spread was the dominant predictor, consistent with the mean-reverting nature of Brent-WTI spreads.
* Random Forest successfully captured nonlinear patterns but remained interpretable.
* Data cleaning and proper date parsing were critical — a silent index formatting issue was detected and resolved, which had previously compromised model accuracy.
* The final model accurately tracked historical spread dynamics and provided a solid baseline for future model comparisons.

**Next Steps:**  
Proceed to Week 6 (XGBoost) using the same engineered features for direct model comparison. Future weeks will focus on improving prediction accuracy, expanding feature sets, and evaluating potential trading signals based on forecast outputs.

[View the notebook here](Brent_WTI_Spread_Predictor_Week5.ipynb)

---

### **Oil News Sentiment Analyzer (Coming Month 3)**
* NLP model classifying sentiment in oil market headlines.

---

## About Me

Senior marketer in refinery supply, training to bridge physical commodity trading and machine learning.

## Contact

* LinkedIn: https://www.linkedin.com/in/blainehodder/
* Hugging Face: https://huggingface.co/blainehodder
