# 📊 Retail Sales Forecasting Project

## 📌 Overview

This project focuses on forecasting sales for a global retail business using time series analysis. It involves data preprocessing, feature engineering, segment selection, and applying multiple forecasting techniques to identify the best-performing model.

---

## 🎯 Objectives

* Forecast future sales accurately
* Identify the most stable and profitable market segment
* Compare multiple time series models
* Select the best model using evaluation metrics

---

## 📂 Dataset

* Total Records: **51,290**
* Features:

  * Order Date
  * Segment
  * Market
  * Sales
  * Profit

---

## 🔄 Project Workflow

```
Raw Data → Data Cleaning → Feature Engineering → Aggregation
→ Segment Selection → Time Series Creation → Train-Test Split
→ Model Building → Evaluation → Best Model Selection
```

---

## 🛠️ Data Preparation

### 1. Feature Engineering

* Created `Market_Segment` by combining Market and Segment
* Helps in granular analysis

### 2. Date Transformation

* Converted Order Date to **monthly format**
* Reduces noise and captures trend & seasonality

### 3. Aggregation

* Used pivot table to aggregate profit by:

  * Month
  * Market Segment

---

## 📊 Segment Selection (CoV Analysis)

* Used **Coefficient of Variation (CoV)**:

```
CoV = Standard Deviation / Mean
```

### Insight:

* **APAC_Consumer** had the lowest CoV
* Indicates high stability and predictability

---

## 📈 Time Series Creation

* Filtered APAC_Consumer segment
* Aggregated monthly sales
* Created univariate time series

---

## ✂️ Train-Test Split

* Train Data: First 42 months
* Test Data: Last 6 months

---

## 🔍 Time Series Decomposition

* Additive Model
* Multiplicative Model

### Purpose:

* Identify trend
* Detect seasonality
* Understand residual patterns

---

## 🤖 Models Implemented

### 🔹 Baseline Models

* Naive Method
* Simple Average
* Moving Average

### 🔹 Exponential Smoothing

* Simple Exponential Smoothing (SES)
* Holt’s Linear Trend Model
* Holt-Winters Additive
* Holt-Winters Multiplicative

### 🔹 ARIMA Family Models

* AR (Auto Regression)
* MA (Moving Average)
* ARMA
* ARIMA
* SARIMA

---

## 📉 Evaluation Metrics

### RMSE (Root Mean Squared Error)

* Penalizes large errors

### MAPE (Mean Absolute Percentage Error)

* Provides percentage-based error

---

## 📊 Model Performance Summary

| Model                       | RMSE     | MAPE      |
| --------------------------- | -------- | --------- |
| Naive                       | 12355    | 17.47%    |
| Simple Average              | 24146    | 34.34%    |
| Moving Average              | 14756    | 15.82%    |
| SES                         | 14765    | 15.83%    |
| Holt’s Method               | 18976    | 34.57%    |
| **Holt-Winters Additive**   | **8942** | **8.84%** |
| Holt-Winters Multiplicative | 9976     | 10.12%    |
| AR                          | 10985    | 13.56%    |
| MA                          | 23360    | 33.93%    |
| ARMA                        | 22654    | 32.40%    |
| ARIMA                       | 22654    | 32.40%    |
| SARIMA                      | 9617     | 12.88%    |

---

## 🏆 Key Results

* **Best Model (Overall):** Holt-Winters Additive
* **Best ARIMA-based Model:** SARIMA
* **Most Stable Segment:** APAC_Consumer

---

## 💡 Key Insights

* Sales exhibit both trend and seasonality
* Stable segments improve forecasting accuracy
* Advanced models outperform baseline methods

---

## 🚀 Business Impact

* Improved demand forecasting
* Better inventory planning
* Data-driven decision making
* Revenue optimization

---

## 🧠 Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Statsmodels
* Scikit-learn


---


## 🙌 Conclusion

This project demonstrates how time series forecasting can be applied to real-world retail data to generate actionable business insights and improve decision-making.

