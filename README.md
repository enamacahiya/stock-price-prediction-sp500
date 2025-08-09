# AI4ALL Project: Stock Market Analysis & Prediction for S&P 500 Companies
> **Team Members: Jasur Abdusattarov, Nourelhouda Belkadi, Ena Macahiya, Mateo Yepes**

---

## Project Overview
This project investigates the **challenges and limitations of using AI models to forecast stock prices**, with a focus on **overfitting** in time-series prediction for S&P 500 companies.
Our main objective was to **predict the next-day closing price** of stocks using historical price data and to test techniques that improve model generalization.

**Research Question:**  
> What are the limitations of AI models in forecasting stock prices, and how can we address overfitting?

**Impact:**

Accurate forecasting can help:
- Investors develop data-driven strategies.
- Policymakers gauge economic health.
- Financial tools become more accessible and transparent.

---

## Dataset
- **Source**: [Kaggle – S&P 500 Stock Data](https://www.kaggle.com/datasets/camnugent/sandp500/data)
- **Period**: 2013–2018 | **Size**: 600,000+ entries
- **Features**: `Open`, `High`, `Low`, `Close`, `Volume`

---

## Approach
1. Preprocessing: Cleaned nulls, one-hot encoded tickers, scaled features, added lag and rolling stats. Created separate dataset for one stock ticker.
2. Models Tested:
     - Linear Regression
     - Random Forest
     - XGBoost
     - CNN-LSTM
3. Evaluation: Mean Squared Error (MSE) on single-stock vs all-stock datasets.

---

## Key Findings
- Single-stock models outperformed all stock models without normalization
- **Best single stock MSE:** Random Forest (2.98), XGBoost (4.01)
- **Best all stock MSE:** XGBoost (208.06)
- Overfitting occurred regularly when models faced volatile and unseen test data.
- Stock prices are influences by unpredictable factors

---

## Next Steps
- Live data pipeline for daily predictions
- Financial metrics like Sharpe Ratio and Cumulative Return
- Interactive web dashboard
- Incorporate alternative data (e.g., headlines, news sentiment) for additional market context.

---

## Structure
```
data/         # raw and processed datasets
models/       # trained models and results
notebooks/    # EDA and experiments
src/          # scripts for cleaning, training and evaluation
```
---

### License

This project is part of the **AI4ALL Ignite Summer Program** and intended for educational purposes only.

### Full Details and Visualizations
See our [final presentation here](https://docs.google.com/presentation/d/1ekT43nMTO6OIa6uWwqUmpoDYaNCpEZW2FasLTjs9ATk/edit?usp=sharing).
