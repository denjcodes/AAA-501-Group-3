# Forecasting in the U.S. Domestic Airline Industry

## Introduction

This project applies AI-driven forecasting to the U.S. domestic airline industry, where volatility in fuel prices, seasonal demand, and competition challenge profitability—especially for startups. By combining machine learning regressors and statistical time series models, we aim to improve route planning and fare optimization.

### Project Topic Statement

Using the U.S. Airline Flight Routes and Fares 1993–2024 dataset, we explore how route attributes (carrier, distance, timing) affect fares and revenue. Models are evaluated not only for prediction accuracy but also for their ability to correctly anticipate trend directions, enabling better strategic decisions.

---

## Data Cleaning/Preparation

The dataset spans over 30 years of U.S. domestic airline fare and route data (1993–2024). Key steps include:

- Dropped columns with >50% missingness and rows missing required fields.
- Removed duplicates, standardized data types, and mapped cities to major airports.
- Engineered features: revenue, fare_per_mile, passengers_per_mile, fare_per_passenger, year_quarter, and airport–airline mappings.
- Applied IQR filtering on selected numeric fields to reduce extreme outliers while preserving meaningful changes.

---

## Exploratory Data Analysis

The exploratory analysis focuses on understanding key trends and correlations, including:

- Analyzed fare distributions, geographic trends, and seasonal effects.
- Correlation analysis revealed strong links between passengers and revenue, and between distance and fare_per_mile.
- Visualized trends, clusters, and route popularity (e.g., LAX ↔ LAS, ATL ↔ JFK).
- Identified distinct route segments (short-haul business, seasonal leisure, long-haul premium) informing feature selection.

---

## Model Selection

*Problem Definition*: Forecast quarterly route revenue with high accuracy and correct directional trend prediction.

### Models Tested

- *Regression*: Random Forest Regression, XGBoost Regression.
- *Statistical*: ARIMA, SARIMA
- Evaluation Metrics: RMSE, MAE, R², MAPE, and Directional Accuracy (DA).
- 222 configurations tested; feature sets included lag, rolling mean, and percentage change metrics.
- Top model: XGBoost Regression with MAPE 1.3%, R² 0.612, DA 90%.

## Model Analysis

XGBoost with temporal and seasonal features (lag_1, lag_4, rolling_mean_4, pct_change_1) delivered the best trade-off between low error and high trend prediction accuracy. Directional accuracy was emphasized for its strategic value—guiding which routes and carriers to prioritize each quarter.

## Conclusion

Machine learning models, particularly XGBoost, can accurately forecast both revenue magnitude and trend direction in the airline industry. This hybrid approach blends predictive power with actionable insights, helping startup airlines compete in a volatile market.

### Recommendations

- *Enhance Feature Engineering* – Incorporate seasonal peaks, holiday periods, weather impacts, and geographic classifications.
- *Integrate External Data* – Add macroeconomic indicators (fuel prices, consumer spending, employment rates) to improve model stability during market shocks.
