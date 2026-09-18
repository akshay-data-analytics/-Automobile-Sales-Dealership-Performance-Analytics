# 🚗 Automobile Sales & Dealership Performance Analytics

A Power BI data analytics project evaluating automobile dealership revenue, profit margins, brand performance, and electric vehicle (EV) market transition using a structured data model and dynamic DAX metrics.

---

## 📌 Executive Summary
This project provides an interactive dashboard designed for dealership executives and regional operations managers to track sales performance and profit margins across dealerships and car makes, as well as analyze vehicle electrification trends across fuel types (Gasoline, Electric, Hybrid).

---

## 📊 Key Insights & Metrics
- **Total Revenue**: $321.18K across evaluated transactions
- **Total Profit**: $36.68K generated across dealerships
- **Profit Margin**: ~11.4% overall dealership margin
- **Units Sold**: 8 transaction units cataloged
- **Brand Revenue Leaders**: Top performers led by **BMW** ($104.4K) and **Tesla** ($88.1K)
- **EV Adoption**: Significant market revenue driven by Electric Vehicles ($123.3K) alongside Gasoline ($143.2K)

---

## 🛠️ Data Architecture & DAX Measures
The project model processes dealership transaction data (`automobile_sales_cleaned.csv`) and utilizes custom DAX calculations:

```dax
// Total Revenue
Total Revenue = SUM('Automobile-Sales-Analytics-PowerBI_automobile_sales_cleaned'[Final_Price_USD])

// Total Profit
Total Profit = SUM('Automobile-Sales-Analytics-PowerBI_automobile_sales_cleaned'[Profit_USD])

// Profit Margin Percentage
Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)

// Total Units Sold
Units Sold = COUNT('Automobile-Sales-Analytics-PowerBI_automobile_sales_cleaned'[Sale_ID])

// Average Sale Price
Average Sale Price = AVERAGE('Automobile-Sales-Analytics-PowerBI_automobile_sales_cleaned'[Final_Price_USD])

// EV Segment Revenue
EV Revenue = CALCULATE([Total Revenue], 'Automobile-Sales-Analytics-PowerBI_automobile_sales_cleaned'[Fuel_Type] = "Electric")