# 🧹 Data Cleaning

**Oasis Infobyte SIP — Data Analytics Track — Level 1, Task 3**

**Author:** Sanika Deepak Shinde

---

## 📌 Objective
Take a messy real-world dataset and systematically transform it into a clean, analysis-ready dataset, documenting the reasoning behind every cleaning decision.

## 🗂️ Dataset
`HRDataset_v14.csv` — 311 employee records, 36 columns (HR Analytics dataset: demographics, salary, performance, engagement, and employment history).

## 🛠️ Tech Stack
Python · pandas · numpy · Jupyter Notebook

## ✅ Checklist Coverage
- [x] Data quality report — nulls per column, duplicate check, dtype issues, value range anomalies
- [x] Missing data handling — strategy and justification per column
- [x] Duplicate removal — identified and documented (0 found)
- [x] Standardisation — inconsistent text formatting normalised
- [x] Outlier detection — IQR method on Salary, decision documented
- [x] Data type correction — IDs as string, dates as datetime, Zip zero-padded, Salary as float
- [x] Before vs. after summary table
- [x] Cleaned dataset saved to a new CSV

## 🔍 Key Data Quality Issues Found
| Issue | Column(s) | Fix |
|---|---|---|
| Legitimate nulls (not missing data) | `DateofTermination`, `ManagerID` | Left as null, documented as meaningful (still employed / no manager); added `IsActive` flag |
| Inconsistent text casing/whitespace | `Sex`, `HispanicLatino`, `Department`, `MaritalDesc` | Stripped and standardised casing |
| 2-digit year date ambiguity | `DOB` | Parsed and corrected century (some birth years were parsing to the 2060s) |
| Dates stored as text | `DateofHire`, `DateofTermination`, `LastPerformanceReview_Date`, `DOB` | Converted to `datetime64` |
| Leading zeros dropped | `Zip` | Cast to string, zero-padded to 5 digits |
| Salary outliers | `Salary` | 29 outliers found via IQR — all senior roles, retained (not capped) |

## 📁 Repository Structure
```
DataAnalytics-L1-CleaningData/
├── Data_Cleaning_HR.ipynb          
├── HRDataset_v14.csv               # Original raw dataset
├── HRDataset_v14_cleaned.csv       # Cleaned output
└── README.md
```

## ▶️ How to Run
```bash
pip install pandas numpy jupyter
jupyter notebook Data_Cleaning_HR.ipynb
```

---
*Submitted as part of the Oasis Infobyte Summer Internship Program (SIP) — Data Analytics track.*
