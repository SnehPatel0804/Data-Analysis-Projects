# Fake Instagram Account Detection

A complete end-to-end machine-learning pipeline for detecting **fake Instagram accounts**.  
The project covers data cleaning, exploratory data analysis (EDA), feature engineering, model training, evaluation, and model persistence.

---

## 📂 Dataset

| File        | Purpose                  |
|-------------|--------------------------|
| `train.csv` | Model training / EDA     |
| `test.csv`  | Final evaluation set     |

**Key columns**

- `#followers`, `#follows`, `#posts`
- `nums/length username`, `nums/length fullname`
- `description length`
- `fake` &nbsp;*(target: 0 = genuine, 1 = fake)*

---

## 🔧 Workflow Summary

| Step | Action |
|------|--------|
| **1** | Remove duplicates and IQR-based outliers |
| **2** | Visual EDA: count plots, histograms + KDEs, box plots, scatter & pair plots, correlation heatmaps |
| **3** | Log‐transform skewed features → standardize with `StandardScaler` |
| **4** | Rank feature importance with Random Forest + Mutual Information |
| **5** | Train three classifiers (Logistic Regression, Random Forest, SVM) with 5-fold Stratified CV |
| **6** | Select best model by **F1-Score** and save to `best_model.pkl` |

---

## 📊 Model Performance

| Model                | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|----------------------|---------:|----------:|-------:|---------:|--------:|
| **Logistic Regression** | **0.933** | **0.889** | **1.000** | **0.941** | **0.993** |
| Random Forest<sup>†</sup> | 0.921 | 0.875 | 0.942 | 0.907 | 0.965 |
| SVM<sup>†</sup>            | 0.910 | 0.861 | 0.948 | 0.903 | 0.960 |

<sup>† Metric values shown for context; Logistic Regression achieved the top F1-Score and was therefore saved.</sup>

---

## 🏆 Best Model – Logistic Regression

Logistic Regression achieved the highest **F1-Score (0.941)**, perfectly recalling all fake accounts while maintaining strong precision. In an imbalanced-class setting, F1-Score is preferred because it balances precision and recall.

`best_model.pkl` contains the trained Logistic Regression instance, ready for deployment or further analysis.

---

## 🔑 Key Insights

- **Followers, follows, and description length** are the most influential predictors (via both RF importance & Mutual Information).
- Log-transforming heavy-tailed count variables dramatically reduced skew, improving model stability.
- Although ensemble models offered high accuracy, Logistic Regression provided the best precision-recall trade-off and superior interpretability.



