# ☕ Coffee Sales Data Analysis Project

## 📁 Project Overview

This project involves end-to-end data analysis on a coffee sales dataset. The dataset contains detailed records of coffee sales including timestamps, payment methods, product names, and amount spent.

---

## 📊 Dataset Features

| Column        | Description                          |
|---------------|--------------------------------------|
| `date`        | Transaction date                     |
| `datetime`    | Exact timestamp of transaction       |
| `cash_type`   | Payment method (e.g., cash, card)    |
| `card`        | Unique user identifier               |
| `money`       | Amount spent per transaction         |
| `coffee_name` | Type of coffee purchased             |

---

## ✅ Steps Performed

### 🧹 1. Data Cleaning & Preprocessing
- Checked for null/missing values
- Removed rows with 0 or negative money
- Converted date/datetime columns to datetime objects

### 📈 2. Exploratory Data Analysis (EDA)
- Sales trends over time
- Coffee-wise distribution of sales
- Payment method comparison (cash vs. card)
- Hour-wise and day-wise analysis

### 📊 3. Intermediate-Level Analysis
- Identified **top 5 spending customers**
- Created **heatmap of coffee preferences** by top customers
- Analyzed **repeat purchase behavior**
- Plotted **purchase distribution** (1-time vs frequent buyers)

### 🚀 4. Advanced-Level Analysis
- **RFM (Recency, Frequency, Monetary)** analysis for all customers
- **KMeans clustering** of customers into 4 segments
- **Time series forecasting** using 7-day moving average

---

## 🧠 Key Conclusions

1. **92% payments** were made via card – suggest digital loyalty systems
2. **Top 2 coffees**: Americano with Milk, and Latte
3. **Peak hours**: 10 AM – 12 PM | **Peak days**: Tuesday to Thursday
4. **Top 10% of customers** generate over 30% of revenue
5. **Sales forecasting** showed mid-week peaks, weekend dips

---

## 🛠 Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn (KMeans, StandardScaler)
- Google Colab

---


