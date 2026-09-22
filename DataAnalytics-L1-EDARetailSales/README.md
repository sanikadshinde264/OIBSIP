# 📊 EDA on Retail Sales Data

**Oasis Infobyte SIP — Data Analytics Track — Level 1, Task 1**

**Author:** Sanika Deepak Shinde

---

## 📌 Objective
Perform exploratory data analysis on an e-commerce sales dataset to uncover patterns in customer behaviour, product performance, and time-based sales trends, and translate the findings into actionable business recommendations.

## 🗂️ Dataset
`realistic_e_commerce_sales_data.csv` — 1,000 orders across 12 columns:

| Column | Description |
|---|---|
| Customer ID | Unique customer identifier |
| Gender | Customer gender |
| Region | North / South / East / West |
| Age | Customer age |
| Product Name | Item purchased |
| Category | Electronics / Accessories / Wearables |
| Unit Price | Price per unit ($) |
| Quantity | Units ordered |
| Total Price | Order value ($) |
| Shipping Fee | Shipping cost ($) |
| Shipping Status | Delivered / In Transit / Returned |
| Order Date | Date of order |

## 🛠️ Tech Stack
Python · pandas · numpy · matplotlib · seaborn · Jupyter Notebook

## ✅ Checklist Coverage
- [x] Initial inspection — shape, dtypes, null check
- [x] Descriptive statistics — mean, median, mode, std for all numeric columns
- [x] Time series analysis — monthly and quarterly sales trend line charts
- [x] Customer demographics — age distribution and gender breakdown
- [x] Product analysis — revenue by product and by category (bar charts)
- [x] Correlation heatmap across numeric variables
- [x] Additional visualisation — shipping status by region
- [x] Markdown observations after every chart
- [x] Conclusion with actionable business recommendations

> Note: the dataset contains only 7 distinct products, so the "top 10 best-selling products" requirement is satisfied by ranking all 7 rather than 10.

## 💡 Key Insights
- Laptops and smartphones drive the large majority of revenue despite being 2 of 7 SKUs.
- Accessories (mouse, keyboard, headphones) generate high order volume but low revenue per order.
- Returns and shipping status vary somewhat by region, worth further investigation.
- Monthly sales fluctuate with order-driven spikes rather than a steady seasonal trend.

## 📈 Business Recommendations
1. Prioritise laptop and smartphone inventory and marketing spend.
2. Bundle low-revenue accessories with high-revenue electronics to lift average order value.
3. Investigate the region(s) with elevated return rates to reduce reverse-logistics costs.
4. Run off-peak promotions to smooth monthly demand and improve inventory planning.

## 📁 Repository Structure
```
DataAnalytics-L1-EDARetailSales/
├── EDA_Retail_Sales.ipynb          
├── realistic_e_commerce_sales_data.csv
├── README.md
└── charts/
    ├── Monthly Sales Trend (line chart).png
    ├── Revenue by Product — all 7 SKUs (bar chart).png
```

## 🖼️ Charts
| Chart | File |
|---|---|
| Monthly sales trend | `charts/Monthly Sales Trend (line chart).png` |
| Quarterly sales trend | `charts/Quarterly Sales Trend (line chart).png` |
| Customer age distribution | `charts/Customer Age Distribution (histogram).png` |
| Gender breakdown | `charts/Gender Breakdown (bar chart).png` |
| Revenue by product (all 7 SKUs) | `charts/Revenue by Product — all 7 SKUs (bar chart).png` |
| Revenue by category | `charts/Revenue by Product Category (bar chart).png` |
| Correlation heatmap | `charts/Correlation Heatmap (numeric variables).png` |
| Shipping status by region | `charts/Shipping Status by Region (stacked bar chart).png` |

## ▶️ How to Run
```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook EDA_Retail_Sales.ipynb
```

---
*Submitted as part of the Oasis Infobyte Summer Internship Program (SIP) — Data Analytics track.*
