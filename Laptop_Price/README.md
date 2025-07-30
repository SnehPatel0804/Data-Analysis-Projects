
# 💻 Laptop Price Analysis 

This project explores a dataset containing laptop specifications and their corresponding prices. The main objective is to understand the factors affecting laptop prices and to build predictive models using regression techniques.

## 📦 Dataset Overview

- The dataset contains **22 features** and **975 rows**.
- Target column: `Price_euros` (Laptop Price in Euros)

### Key Features:
- Company
- Product
- TypeName (Notebook, Ultrabook, Gaming, etc.)
- Ram, Inches, Weight
- OS (Operating System)
- Screen details (Full HD, Touchscreen, Retina Display)
- CPU & GPU details
- Storage (Primary & Secondary)

---

## 📊 Exploratory Data Analysis (EDA)

- **Top 3 companies** by count: HP, Dell, Lenovo
- **Most common OS**: Windows 10
- **Most common screen type**: Full HD
- **Most used CPU**: Intel Core i7
- **Most used storage type**: SSD
- **Outliers handled** using IQR technique for features like Price, Ram, Inches, Weight, etc.

### Visualizations:

- Histograms for categorical columns using Plotly
- Boxplots and Scatterplots for numeric features
- Heatmap showing correlation matrix
- Pivot plots for Screen types across laptop types

---

## ⚙️ Feature Engineering

- Label Encoding used on categorical columns
- Handled missing values using `SimpleImputer`
- Feature scaling using `StandardScaler`

---

## 🧠 Model Building

### 🔹 Linear Regression
- **R² Score**: ~0.699
- **RMSE**: Moderate

### 🔹 Random Forest Regressor
- **R² Score**: ~0.85
- **RMSE**: Low
- **Top Important Features**:
  - `Ram` (Highest importance)
  - `Weight`
  - `CPU_freq`
  - `Inches`
  - `PrimaryStorage`

---

## 📝 Insights

- RAM has the **highest influence** on laptop price.
- Weight, CPU frequency, and Screen dimensions also contribute significantly.
- Retina Display has the **least impact** on pricing.
- Random Forest outperforms Linear Regression in prediction accuracy.

---

## 📁 Project Files

- `laptop_prices.csv` – Dataset used
- `laptop_price_analysis.ipynb` – Jupyter Notebook (main code)
- `README.md` – Project overview and documentation




