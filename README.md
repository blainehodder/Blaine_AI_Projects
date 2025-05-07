# Blaine’s AI Projects

Welcome to my AI portfolio. I’m building applied machine learning and deep learning models focused on finance and commodity trading use cases.

## Projects

### 1. Brent Price Predictor — Week 2 (Baseline Linear Regression)

**Goal:** Build a simple linear regression model to predict daily Brent prices based on previous prices.

**Tools:** Python, pandas, scikit-learn, matplotlib

**Results:** 
- Model trained and tested on historical Brent price data.
- Mean Absolute Error (MAE): $1.22

**Next Steps:** Explore adding more features like moving averages, volume, or news sentiment.

---

### 2. Brent Price Predictor — Week 3 (Feature Engineering)

**Goal:** Improve the baseline linear regression model by adding engineered features:
- Previous day's price
- Percentage change from the previous day
- 5-day moving average of price

**Tools:** Python, pandas, scikit-learn, matplotlib

**Model:** Multiple linear regression using three input features.

**Results:** 
- Model trained and tested on historical Brent price data.
- Mean Absolute Error (MAE): $0.62

**Key Insights:**
- Moving averages help smooth out noise and random daily price shocks.
- Percentage change captures relative price movements and momentum effects.
- Multivariate regression allows the model to weight multiple predictors and adjust for confounding relationships.

**Next Steps:** Explore additional features such as volatility measures or rolling volume. Consider testing more advanced models (Random Forest, Gradient Boosting) for comparison.

[View the notebook here](Brent_Price_Predictor_Week3.ipynb)

---

### 3. Oil News Sentiment Analyzer (Coming Month 3)
- NLP model classifying sentiment in oil market headlines.

## About Me

Senior marketer in refinery supply, training to bridge physical commodity trading and machine learning.

## Contact

- LinkedIn: https://www.linkedin.com/in/blainehodder/
- Hugging Face: https://huggingface.co/blainehodder
