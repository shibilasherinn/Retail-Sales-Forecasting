# Retail Sales Forecasting — Time Series Analysis

An end-to-end time series forecasting project that predicts weekly retail sales using Python, combining exploratory data analysis with a feature-engineered Linear Regression model.

## Project Overview

- **Dataset:** Synthetic 3-year daily sales data (2022-2024) across 3 retail stores, engineered to reflect realistic patterns — upward trend, weekly and monthly seasonality, festive spikes, and missing values.
- **Goal:** Forecast weekly retail sales and evaluate how much forecast accuracy improves when moving from a simple trend-based model to one using lag features and rolling averages.
- **Tech stack:** Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly, Scikit-learn

## Workflow

1. **Data Generation** — Synthetic daily sales data created for 3 stores with trend, seasonality, festive spikes, and missing values.
2. **Data Cleaning** — Missing values handled via time-based interpolation.
3. **Exploratory Data Analysis** — Visualized overall trend, store-wise monthly patterns, weekday distribution, and monthly seasonality.
4. **Train-Test Split** — Chronological split, holding out the last 12 weeks for testing.
5. **Modeling** — Linear Regression using lag features (previous weeks' sales) and a rolling mean, instead of relying on trend alone.
6. **Evaluation** — Compared model performance using MAE, RMSE, and MAPE.

## Key Visualizations

**Total Daily Sales Trend**
![Total Daily Sales](Total%20daily%20sales.png)

**Monthly Sales Trend by Store**
![Monthly Sales by Store](Monthly%20sales%20by%20store.png)

**Sales Distribution by Day of Week**
![Weekday Boxplot](Weekday%20boxplot.png)

**Average Sales by Month (Seasonality Check)**
![Monthly Seasonality](Monthly%20seasonality.png)

**Forecast vs Actual (Linear Regression)**
![Forecast vs Actual](Forecast%20vs%20actual.png)

> Note: the sharp dip in the final data point of the forecast chart reflects a partial week at the end of the dataset (2024-12-31 cutoff), not an actual sales crash.

## Key Insights

- Sales show a steady upward trend over the 3-year period
- Weekend sales are consistently higher than weekdays
- Sales peak around June-July, with additional short-term spikes during the festive season (Oct-Nov)
- Adding lag features and a rolling mean significantly improved forecast accuracy — **MAPE dropped from ~40% (trend-only baseline) to 13.39%**
- Recent sales history is a much stronger predictor than long-term trend alone for short-term forecasting

## Model Performance

| Metric | Value |
|--------|-------|
| MAE    | 13,782.63 |
| RMSE   | 22,340.34 |
| MAPE   | 13.39% |

## Business Takeaway

Stock up and staff up ahead of the June-July peak season and around weekends. Use recent sales momentum — not just long-term trend — for short-term demand planning.

## Repository Structure

```
├── sales_forecasting.ipynb        # Main analysis notebook
├── retail_sales_synthetic.csv     # Synthetic dataset
├── Total daily sales.png          # Chart exports used in this README
├── Monthly sales by store.png
├── Weekday boxplot.png
├── Monthly seasonality.png
├── Forecast vs actual.png
└── README.md
```

---

## Author
**Shibila Sherin M**
Data Science | Data Analysis | Power BI | Python | Statistics | Machine Learning | NLP | Deep Learning | SQL

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/shibilasherinn)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat&logo=github)](https://github.com/shibilasherinn/E-Commerce-Sales-Dashboard)
