# 📊 Sales Performance Dashboard — Excel

An interactive business intelligence dashboard built in Microsoft Excel, analyzing **9,994 transactional records** across 4 years (2014–2017) to surface revenue trends, customer profitability, regional performance, and product-level insights.

---

## 📌 Project Overview

This dashboard was designed to give a comprehensive view of sales performance across multiple dimensions — time, geography, product category, and customer segments. It enables dynamic filtering and real-time KPI monitoring through Excel's native visualization and data modeling capabilities.

---

## 🖼️ Dashboard Preview

![Sales Dashboard](https://raw.githubusercontent.com/sarth-1411/SuperStore-Sales-Analytics/main/Sales%20Dashboard.png)

---

## 📂 Dataset

| Property | Details |
|---|---|
| **Source** | Sample Superstore Dataset |
| **File** | `Sample_-_Superstore.csv` |
| **Records** | 9,994 rows |
| **Time Period** | 2014 – 2017 |
| **Fields** | 21 columns including Order Date, Sales, Profit, Category, Sub-Category, State, Customer Name |

---

## 📈 Key Metrics & KPIs Tracked

- **Revenue Trends** — Profit over time by Category (Furniture, Office Supplies, Technology)
- **Regional Sales** — Geographic sales distribution across US states
- **Sales by Sub-Category** — 17 product sub-categories ranked by total sales
- **Top 5 Customers by Profit** — Customer-level profitability breakdown
- **Monthly Sales** — Seasonal patterns across all years
- **Customer Count** — Unique customer growth year-over-year

---

## 🛠️ Tech Stack

- **Microsoft Excel** — Primary tool
  - PivotTables & PivotCharts
  - Slicers (Year, Category)
  - Conditional Formatting
  - Data Validation
  - Named Ranges
  - Filled Map Chart
  - Dynamic filtering across all visuals

---

## 🔢 Excel Formulas & Methods Used

### Data Aggregation
| Formula | Purpose |
|---|---|
| `SUMIF` / `SUMIFS` | Aggregating Sales & Profit by Year, Category, Sub-Category |
| `COUNTIF` / `COUNTIFS` | Counting unique customers per year |
| `LARGE()` | Pulling Top 5 customer profit values |

### Lookup & Reference
| Formula | Purpose |
|---|---|
| `VLOOKUP` / `INDEX-MATCH` | Mapping customer names to profit values |
| `UNIQUE` + `SORT` | Dynamic top customer rankings (Excel 365) |

### Date & Time
| Formula | Purpose |
|---|---|
| `YEAR()` | Extracting year from Order Date for time-series analysis |
| `MONTH()` | Extracting month for monthly sales trend chart |

### Dashboard Logic
| Formula | Purpose |
|---|---|
| `IFERROR()` | Handling blank slicer states gracefully |
| `IF()` | Conditional display logic for KPI labels |

---

## 📊 Visualizations

| Chart | Type | Insight |
|---|---|---|
| Profit Gained Over Time | Line Chart | Year-over-year profit trend by Category |
| Sales by States | Filled Map Chart | Geographic revenue distribution |
| Sales by Sub-Category | Horizontal Bar Chart | Product-level sales ranking |
| Top 5 Customers by Profit | Pie Chart | Customer profitability breakdown |
| Monthly Sales | Area/Bar Chart | Seasonal sales patterns |
| Customer Count | Horizontal Bar Chart | YoY customer growth |

---

## 🔍 Data Validation & Findings

As part of this project, the source CSV was cross-validated against the Excel dashboard outputs:

- ✅ **Customer counts matched perfectly** across all 4 years
- ✅ **16 out of 17 sub-categories** matched (minor floating-point rounding only)
- ⚠️ **Chairs sub-category** showed a discrepancy of **~$281** (Dashboard: $328,167.76 vs CSV: $328,449.10) — likely due to a few transactions being miscategorized in the workbook

---

## 📁 File Structure

```
📦 Sales-Dashboard-Excel
 ┣ 📊 Sales_Dashboard.xlsx        # Main Excel dashboard file
 ┣ 📄 Sample_-_Superstore.csv     # Raw source data
 ┣ 🖼️ Sales_Dashboard_-_Excel.png # Dashboard screenshot
 ┗ 📝 README.md                   # Project documentation
```

---

## 🚀 How to Use

1. Open `Sales_Dashboard.xlsx` in Microsoft Excel (2016 or later recommended)
2. Navigate to the **Dashboard** sheet
3. Use the **Year** slicer to filter by 2014, 2015, 2016, or 2017
4. Use the **Category** slicer to filter by Furniture, Office Supplies, or Technology
5. All charts update dynamically based on slicer selections
