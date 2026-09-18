# 🚗 Automobile Sales & Dealer Performance Analytics (Power BI)

An enterprise-level Power BI analytics solution designed to track **automotive revenue, dealer profit margins, vehicle fuel trends (EV vs. Hybrid vs. Gas), and inventory performance** across regional dealerships.

---

## 📌 Open Source Dataset & Data Wrangling

The pipeline uses the **Kaggle Automotive Sales Dataset** cleaned using Python and Power Query:
* **Missing Value Imputation:** Fixed null pricing entries using regional average cost models.
* **Type Conversion & Date Normalization:** Formatted standard ANSI `YYYY-MM-DD` timestamps for Star-Schema Date dimensions.
* **Calculated Columns:** Derived `Final_Price_USD` and `Profit_USD` after discounting.

---

## 📐 Data Model & Relationships (Star Schema)

* **Fact Table:** `automobile_sales_cleaned`
* **Lookup Tables:** `Dim_Dealership`, `Dim_Date`, `Dim_Vehicle`

---

## 🚀 How to Build in Power BI Desktop

1. Open **Power BI Desktop**.
2. Click **Get Data** -> **Text/CSV** and select `automobile_sales_cleaned.csv`.
3. Click **Transform Data** (Power Query), verify columns, then click **Close & Apply**.
4. Create a **New Table** for DAX measures and copy formulas from `DAX_Measures.dax`.
5. Save as `Automobile_Sales_Dashboard.pbix`.
