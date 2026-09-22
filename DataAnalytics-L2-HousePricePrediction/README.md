# 🏠 Predicting House Prices with Linear Regression

**Oasis Infobyte SIP — Data Analytics Track — Level 2, Task 1**

**Author:** Sanika Deepak Shinde

---

## 📌 Objective
Build and evaluate a linear regression model that predicts house prices based on features such as area, location, number of rooms, and age — developing end-to-end skills from data cleaning through to model interpretation.

## 🗂️ Dataset
`train.csv` — House Prices: Advanced Regression Techniques (Ames Housing Dataset, Kaggle) — residential property records with area, location/neighborhood, room counts, age, and sale price.

## 🛠️ Tech Stack
Python · pandas · scikit-learn · matplotlib · seaborn · Jupyter Notebook

## ✅ Checklist Coverage
- [x] EDA — null check, descriptive statistics, distribution of target variable (`Price`)
- [x] Feature selection discussion — reasoning documented in markdown
- [x] Missing value handling — median imputation (numeric), mode imputation (categorical)
- [x] Categorical encoding — One-Hot Encoding applied
- [x] Correlation heatmap — features most correlated with price identified
- [x] Train/test split — 80/20
- [x] Linear Regression model trained (scikit-learn)
- [x] Model evaluation — MSE, RMSE, R² score
- [x] Actual vs. predicted scatter plot
- [x] Residual plot — checked for systematic patterns
- [x] Coefficient analysis — top positive/negative price drivers identified
- [x] Bonus — Ridge and Lasso regularized models compared against baseline

## 🔍 Key Findings
| Step | Detail | Outcome |
|---|---|---|
| Missing values | Numeric columns | Imputed with median (robust to skew/outliers) |
| Missing values | Categorical columns | Imputed with mode, then one-hot encoded |
| Sparse columns | Any column >50% missing | Dropped rather than imputed |
| Correlation | Area/square footage | Strongest positive correlation with price |
| Correlation | Age of property | Negative correlation with price, as expected |
| Model performance | Linear Regression | RMSE and R² reported in notebook output (Section 9) |
| Residuals | Actual − Predicted | Checked for random scatter vs. systematic pattern (Section 11) |
| Coefficients | Top drivers | Area, location dummies, and bathrooms ranked among strongest positive contributors; age among strongest negative |
| Bonus comparison | Ridge vs. Lasso vs. Linear | R² compared across all three; Lasso zeroes out weaker features |

## 📁 Repository Structure
```
DataAnalytics-L2-HousePricePrediction/
├── house_price_prediction.ipynb    
├── train.csv                       # Original raw dataset (add manually from Kaggle)
└── README.md
```

## ▶️ How to Run
```bash
jupyter notebook house_price_prediction.ipynb
```

---
*Submitted as part of the Oasis Infobyte Summer Internship Program (SIP) — Data Analytics track.*
