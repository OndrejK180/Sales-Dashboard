# Sales & Profitability Dashboard

A 4-page Power BI dashboard analyzing sales, profit, discounting, and product-level performance across categories, subcategories, and regions.

## 📊 Overview

This dashboard was built to answer core business questions:
- Which categories and subcategories actually drive profit — not just sales volume?
- Where is discounting hurting rather than helping margins?
- Which products or regions are underperforming and why?

## 🖼️ Preview

### Page 1 — Sales & Profit Overview
![Overview](screenshots/01_overview.png)
KPI summary, quarterly sales & profit trend, category and regional breakdowns.

### Page 2 — Product & Profitability Analysis
![Product Analysis](screenshots/02_product_profitability.png)
Profit margin by category, subcategory-level sales/profit comparison, and top/bottom 10 products by profit.

### Page 3 — Discount & Profitability Deep Dive
![Discount Deep Dive](screenshots/03_discount_deep_dive.png)
Profit-vs-discount relationship by category (bubble chart), and subcategory profit margins with loss-making subcategories highlighted.

### Page 4 — Business Insights
![Business Insights](screenshots/04_business_insights.png)
Key takeaways from the analysis, summarized for quick, non-technical consumption.

## 🔑 Key Insights

1. **Technology and Office Supplies are similarly efficient; Furniture lags.** Both post ~17% margins, while Furniture manages just 2.5% despite solid sales volume.
2. **Tables quietly lose money.** Despite ranking 4th in sales, Tables post a -8.6% margin (-18k profit) — volume isn't translating to profit here.
3. **Copiers punch above their weight.** They rank behind Phones and Chairs in sales but deliver a stronger 37.2% margin — an underleveraged opportunity.
4. **Heavy discounts aren't paying off.** Binders and Machines get the deepest discounts, yet several heavily-discounted subcategories (Supplies, Bookcases, Tables) run negative margins.
5. **Q4 is a consistent seasonal peak.** Sales and profit spike in Q4 every year from 2014-2017, pointing to reliable holiday-driven demand.
6. **West leads in both sales and profit.** It outperforms East, Central, and South on both metrics — worth studying what's driving it.
7. **A handful of products drive outsized losses.** The bottom 10 products lose 2-9k each; reviewing or discontinuing these SKUs could lift overall profit without touching sales.

## 🛠️ Built With

- **Power BI Desktop**
- DAX measures for Total Sales, Total Profit, Profit Margin, and Average Discount
- Custom date hierarchy (Year → Quarter → Month) for drill-down analysis
- Conditional formatting to flag loss-making products/subcategories

## 📁 Repository Structure

```
sales-profitability-dashboard/
├── README.md
├── .gitignore
├── pbix/
│   └── Sales_Profitability_Dashboard.pbix
├── data/
│   └── sample_data.csv
├── screenshots/
│   ├── 01_overview.png
│   ├── 02_product_profitability.png
│   ├── 03_discount_deep_dive.png
│   └── 04_business_insights.png
└── docs/
    └── data_dictionary.md
```

## 🚀 How to Use

1. Clone this repository.
2. Open `pbix/Sales_Profitability_Dashboard.pbix` in **Power BI Desktop** (free download from Microsoft).
3. If prompted, point the data source to your own copy of the dataset (see `data/` folder, if included).
4. Explore the report — use the Year/Category/Sub-Category filters on the right-hand filter pane, and click into the line chart to drill down from Year → Quarter → Month.

## 📄 Data Source

*(Fill in: e.g., "Sample Superstore dataset" or your actual data source, and note any licensing/usage restrictions.)*

## 📌 Notes

- Report pages are designed to be read in order: **Overview → Product Analysis → Discount Deep Dive → Business Insights**.
- Color coding is consistent throughout: light blue = Technology/Sales, navy = Furniture/Profit, orange = Office Supplies, red = loss-making items.
