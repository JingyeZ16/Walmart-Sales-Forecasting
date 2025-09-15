# Walmart-Sales-Forecasting

# 📖 Background & Problem

Walmart, as one of the largest retailers in the world, faces strong seasonal fluctuations in sales. Peaks around Thanksgiving, Black Friday, and Christmas are followed by sharp declines in January.

If these seasonal patterns are not properly anticipated, Walmart risks:

Overstocking or stockouts during peak seasons

Missed revenue targets, negatively impacting stock prices and investor confidence

Inefficient inventory management and supply chain disruptions

Accurate forecasting of weekly sales is therefore critical to:

Plan stock levels and reduce waste

Align promotional campaigns with demand

Forecast revenue and guide investment decisions

Maintain investor trust by meeting projections.

# 🎯 Aim

The goal of this project is to predict weekly sales at the store–department level using a combination of time series forecasting and machine learning models.

With accurate predictions, Walmart can:

Identify seasonal demand patterns

Protect against revenue loss

Improve inventory and promotional planning

Support long-term strategic investments


# 📊 Project Overview
This project implements both univariate and multivariate time series forecasting pipelines to predict weekly sales at the store-department level for Walmart, incorporating:

✅ Lag features and rolling statistics

✅ External regressors (holidays, promotions, temperature, fuel price, unemployment)

✅ Machine learning models including XGBoost, Random Forest, and Prophet

The objective is to provide actionable insights to enhance inventory management, reduce stockouts, and improve promotional timing.


# 🚀 Highlights

✅ Multivariate time series forecasting with external regressors (holidays, promotions, CPI, fuel price, weather)

✅ 10+ lag features, rolling statistics, and holiday decomposition to capture seasonal effects

✅ Model portfolio: XGBoost, Random Forest, Prophet, Linear Regression, ARIMA

✅ Hyperparameter tuning with GridSearchCV and SHAP value analysis for interpretability

✅ Delivered actionable insights to optimize stock levels, reduce stockouts, and align promotional timing

# 📦 Data Sources

Kaggle: Walmart Sales Forecast Dataset

File	Description	Rows x Columns
features.csv	Economic indicators, promotions, holidays	8,190 x 12

stores.csv	Store metadata (type, size)	45 x 3

train.csv	Historical weekly sales	421,570 x 5

test.csv	Evaluation dataset	115,064 x 4

# ⚙️ Methodology

# 📐 Feature Engineering

Lag features, rolling means, rolling std, min/max windows

Holiday and week-of-year decomposition

Encoded categorical variables (store type, department)

Incorporated markdowns, CPI, unemployment, fuel price, temperature

# 🤖 Models Applied

| Model             | R²    | RMSE     | MAE      |
| ----------------- | ----- | -------- | -------- |
| Linear Regression | 0.902 | 7,142.25 | 2,798.20 |
| Random Forest     | 0.949 | 5,161.36 | 2,210.34 |
| XGBoost           | 0.961 | 4,316.12 | 1,825.57 |


Hyperparameter tuning with GridSearchCV

Residual diagnostics and SHAP-based feature interpretation.

Residual diagnostics confirmed non-stationary behavior; handled via differencing & log transforms.

Exponential Smoothing also performed well on certain departments.

GridSearchCV tuning improved Random Forest and XGBoost performance.

# 📊 Key Findings

Store size & type: Larger stores (Type A) consistently drive higher sales.

Holiday peaks: Thanksgiving, Black Friday, and Christmas dominate weekly sales.

Seasonality: Back-to-school (week 22) is a strong but overlooked driver.

Post-season dips: January consistently shows reduced sales after holiday peaks.

Economic indicators: Fuel price, CPI, and unemployment have weaker short-term influence.

# 🎯 Business Impact

✔ More accurate demand forecasting

✔ Optimized inventory management

✔ Reduced stockouts & overstocks

✔ Improved promotional alignment with seasonal peaks

✔ Supports investor confidence by reducing forecasting uncertainty



