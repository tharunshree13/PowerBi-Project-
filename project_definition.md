# 📋 Project Definition — Zepto Sales Dashboard

## Project Title
**Zepto Quick-Commerce Sales Analytics Dashboard using Power BI**

---

## Project Background

Zepto is one of India's fastest-growing quick-commerce platforms, delivering groceries and daily essentials within 10 minutes. In the quick-commerce industry, real-time sales analytics is essential for managing inventory, optimizing delivery operations, and understanding customer purchasing behavior across cities and product categories.

This project simulates a business intelligence solution for Zepto's sales team using a structured flat dataset and an interactive Power BI dashboard.

---

## Problem Statement

The sales operations team at Zepto needs a centralized, visual reporting tool to:

1. Monitor overall sales performance on a monthly basis
2. Identify which cities generate the highest revenue
3. Understand which product categories drive the most sales and profit
4. Track average order value and units sold to evaluate basket size
5. Enable quick filtering and drill-down by month, city, and product category

---

## Objectives

- Build a single-page interactive Power BI dashboard covering key sales KPIs
- Visualize sales trends across time (monthly), geography (city-wise), and product (category-wise)
- Enable business users to filter the dashboard by Month, Category, and City using slicers
- Calculate DAX measures for Total Sales, Total Orders, Total Units, and AOV

---

## Scope

**In Scope:**
- Sales data for Q1 2025 (January, February, March)
- 4 cities: Hyderabad, Bangalore, Mumbai, Delhi
- 5 product categories: Dairy, Snacks, Vegetables, Beverages, Fruits
- 1,000 order records with 42 fields per record

**Out of Scope:**
- Real-time data refresh / live database connection
- Customer segmentation or predictive analytics
- Multi-year comparison

---

## Dataset Description

| Attribute | Details |
|---|---|
| Source | Simulated / Synthetic dataset |
| File | zepto_sales_flat_dataset.xlsx |
| Rows | 1,000 orders |
| Columns | 42 fields |
| Period | January 2025 – March 2025 |
| Format | Flat (denormalized) Excel table |

---

## Dashboard Design

**Layout:** Single-page dashboard with black background and gold/beige color theme

**KPI Cards (Top Row):**
- Total Orders: 1,000
- Total Sales: ₹1.09M
- Total Units Sold: 3,038
- Average Order Value (AOV): ₹1.09K

**Charts:**
| Visual | Type | X-Axis | Y-Axis |
|---|---|---|---|
| Total Sales by Month | Area Chart | Month | Total Sales |
| Total Sales by City | Bar Chart | City | Total Sales |
| Sales & Profit by Category | Grouped Bar Chart | Category | Sales + Profit |
| Total Sales by Category | Donut Chart | Category | Total Sales |

**Slicers:** Month, Category, City

---

## DAX Measures Used

```dax
Total Sales = SUM(zepto_sales_flat_dataset[Selling_Price])

Total Orders = COUNTROWS(zepto_sales_flat_dataset)

Total Units = SUM(zepto_sales_flat_dataset[Quantity])

AOV = DIVIDE([Total Sales], [Total Orders], 0)

Total Profit = SUM(zepto_sales_flat_dataset[Profit])
```

---

## Key Findings

1. **Hyderabad** leads in total sales among all four cities
2. **January** was the highest-revenue month; sales declined through March
3. **Dairy** and **Snacks** are the top two categories by total sales value
4. **AOV of ₹1,090** suggests customers order mid-range value baskets
5. **Fruits** generated the lowest sales, indicating lower demand or fewer SKUs

---

## Tools & Technologies

| Tool | Version | Purpose |
|---|---|---|
| Power BI Desktop | Latest | Dashboard design and visualization |
| Microsoft Excel | .xlsx | Source data storage |
| Power Query | Built-in | Data ingestion and transformation |
| DAX | Built-in | Calculated measures and KPIs |

---

## Project Timeline

| Phase | Activity | Status |
|---|---|---|
| Phase 1 | Dataset preparation and review | ✅ Done |
| Phase 2 | Data loading and Power Query transformations | ✅ Done |
| Phase 3 | DAX measure creation | ✅ Done |
| Phase 4 | Dashboard design and visual layout | ✅ Done |
| Phase 5 | Testing and slicer validation | ✅ Done |
| Phase 6 | GitHub documentation and publishing | ✅ Done |

---

## Author

**Tharun S**
B.E. Artificial Intelligence & Data Science
Vinayaka Mission's Kirupananda Variyar Engineering College (VMKV), Salem — 2026
GitHub: [github.com/tharunshree13](https://github.com/tharunshree13)
