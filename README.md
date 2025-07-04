# Airfare Prediction and Route Segmentation Across U.S. Routes (1993–2024)

## Introduction

### Project Topic Statement

This project investigates how historical airline fare and route data can be used to predict airfare prices and identify customer behavior trends in air travel across the United States from 1993 to 2024. The system employs both regression algorithms for fare prediction and clustering algorithms for identifying route or customer-type groupings. These insights aim to assist airline carriers and travel platforms in fare optimization and market segmentation strategies.

---

## Data Cleaning/Preparation

The dataset spans over 30 years of U.S. domestic airline fare and route data (1993–2024). Key steps include:

- Handling missing or inconsistent historical fare records.
- Normalizing features such as route distance, carrier codes, and seasonal indicators.
- Engineering features from raw data (e.g., converting dates to seasonality, categorizing carriers, calculating route distances).
- Removing duplicate entries and outliers (e.g., fares far outside reasonable ranges).
- Encoding categorical features and scaling continuous variables.

---

## Exploratory Data Analysis

The exploratory analysis focuses on understanding key trends and correlations, including:

- Fare distributions over years and across regions.
- Price variability by carrier, route distance, and seasonality.
- Correlation analysis to understand the influence of features on fare pricing.
- Visualization of route clusters and seasonal demand patterns.
- Preliminary inspection to detect potential segmentations (e.g., premium long-haul vs. budget short-haul).

---

## Model Selection

### Problem Definition

- *How do route characteristics (e.g., distance, carrier, region, seasonality) influence airfare?*
- *Can we group U.S. routes or travelers into meaningful clusters to inform pricing and planning?*
- *What patterns can be learned from over 30 years of data to assist airline revenue management?*

### Algorithms

- *Regression*: Linear Regression, Random Forest Regressor, XGBoost — for fare prediction.
- *Clustering*: K-Means, DBSCAN — for traveler or route segmentation.

### System Overview

- Data ingestion and preprocessing pipeline.
- Clustering module to identify route or seasonal clusters.
- Regression module to predict fare prices.
- Evaluation framework using metrics such as RMSE, MAE, and silhouette scores.

---

## Model Analysis

### Regression Analysis

- Evaluate prediction accuracy using RMSE and MAE across Linear Regression, Random Forest, and XGBoost models.
- Feature importance analysis to determine the most influential factors on fare predictions.

### Clustering Analysis

- Identify optimal number of clusters using elbow method and silhouette score.
- Interpret resulting clusters (e.g., "high-volume short-haul," "premium transcontinental") for strategic pricing.
- Validate clusters against external indicators like demand volume and revenue potential.

### Example System Behaviors

- Given a new route (e.g., LAX → ORD on Delta in March), the system predicts expected fare.
- Clusters of routes emerge, revealing key segments to support targeted marketing or fleet planning.
- The system flags underpriced routes or suggests competitive adjustments.

---

## Conclusion and Recommendations

The analysis demonstrates that route characteristics such as carrier, distance, and seasonality significantly affect airfare pricing. Regression models (especially Random Forest and XGBoost) provide strong predictive performance, while clustering helps identify strategic segments for market differentiation.

*Recommendations:*

- Airlines should focus on dynamic pricing strategies for clusters identified as price-sensitive.
- Further refinement of seasonal and regional features can improve predictive accuracy.
- Integration with external factors (e.g., macroeconomic data, fuel prices) may provide additional improvements.

---

## Appendix
