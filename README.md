# Product Sales & Region Analysis
 
An end-to-end Excel data analysis project: cleaning a raw retail sales dataset, building pivot-table summaries, and drawing business insights across region, product, payment method, and customer behavior.
 
This is a **practice/portfolio project** built to demonstrate an Excel analysis workflow (data cleaning → structured analysis → pivot tables → written insights). It is not a real business report.

The Excel workbook itself contains 4 tabs and is the core deliverable:
 
| Tab | Purpose |
|---|---|
| `Sheet1` | Raw source data (1,500 orders, 19 columns) |
| `Data Cleaning` | Cleaned/validated copy of the raw data |
| `Data Analysis` | Calculated fields (Gross Sales, Discount Amount, Net Sales) and summary KPIs |
| `Pivot Analysis` | Pivot tables: regional, product, payment method, salesperson, and monthly performance |

## 📊 Data Source
 
Practice dataset from [excelx.com](https://excelx.com/practice-data/sales-retail/) — a synthetic retail sales dataset. Because the data is randomly generated for practice purposes, findings below describe *what the numbers show*, not real market behavior.
 
## 🧹 Data Cleaning
 
Starting from the raw 1,500-row, 19-column export, the cleaning pass:
- Verified there were no missing values in any core transactional field (Date, Region, Product, Quantity, UnitPrice, TotalPrice, etc.) — the only column with nulls is `Promotion`, which is legitimately blank for orders with no promo code applied (370 of 1,500 orders)
- Confirmed there were zero duplicate rows
- Standardized date fields (`Date`, `OrderDate`, `DeliveryDate`) to a consistent datetime format
- Added calculated fields: **Gross Sales**, **Discount Amount**, and **Net Sales**, each built with formulas rather than hardcoded values so the sheet recalculates if the source data changes
## 📈 Key Metrics
 
| Metric | Value |
|---|---|
| Total orders | 1,500 |
| Date range | Jan 1, 2023 – Jun 30, 2025 |
| Total Net Sales | $4,379,992.43 |
| Average Order Value | $2,919.99 |
| Average discount rate | 7.3% |
| Return rate | 24.8% (372 of 1,500 orders) |
| Average delivery time | 6.0 days (range: 2–10 days) |
 
## 🔍 Insights
 
**Regional performance is close, with North slightly ahead.** North generated the most net sales ($967,958), about 17% ahead of the lowest-performing region, South ($827,768). East, West, and Central are clustered tightly together ($847K–$884K), so region isn't a strong differentiator in this dataset — no single region dominates.

<img width="1325" height="805" alt="preview" src="https://github.com/user-attachments/assets/ecaa67e8-6b1a-4064-bc8c-40c577eb2180" />

**Laptops, Tablets, and Printers are the top revenue products — but Chairs have the worst return rate.** Laptops ($684,417), Tablets ($684,539), and Printers ($684,387) are essentially tied at the top, while Phones trail at $497,163 (partly because Phones also carry the lowest average discount amount and unit price). Looking at *returns* rather than revenue, Chairs stand out with a 28.2% return rate — well above the 24.8% overall average and the highest of any product.

<img width="1325" height="805" alt="product_net_sales" src="https://github.com/user-attachments/assets/be3e42af-3fa7-4b89-aef2-b13e7efdc533" />

**Online payment is the leading channel, but the five payment methods are fairly balanced.** Online transactions bring in the most net sales ($971,115 across 323 orders), narrowly ahead of Cash ($950,388). Debit Card is the smallest channel at $770,421. No payment method is negligible — all five sit within roughly 20% of each other.

<img width="1326" height="730" alt="payment_method" src="https://github.com/user-attachments/assets/8ba6aa6e-b382-4f8c-8b25-ade2291b272e" />

**Monthly sales are volatile with no clear trend.** Net sales swing widely month to month (from a low of ~$79K in October 2023 to a high of ~$208K in March 2023) with no consistent upward or downward trajectory across the 2.5-year window. This is consistent with the dataset being randomly generated rather than reflecting a real seasonal retail business.

<img width="1568" height="702" alt="preview (1)" src="https://github.com/user-attachments/assets/e409ed4c-5f72-4ece-b660-d9a7fc5bcda5" />
 
**Retail and Wholesale customers contribute almost identically.** Retail ($2,195,526) and Wholesale ($2,184,467) split total revenue nearly 50/50, so customer type isn't a meaningful lever for prioritization in this dataset.
 
**Promotions have little measurable effect on order value.** Average order value is nearly flat whether a customer used FREESHIP ($2,955), SAVE10 ($2,928), WINTER15 ($2,890), or no promotion at all ($2,903) — a ~2% spread. In a real dataset this would be worth flagging to a marketing team, since it suggests these promo codes aren't driving meaningfully larger baskets.
 
**Return rate (24.8%) is the most actionable number in the dataset.** Nearly 1 in 4 orders is returned. Chairs (28.2%) and Laptops (27.4%) run above average; Desks (21.7%) and Printers (22.3%) run below. If this were a live business, this would be the first place to investigate — e.g., quality issues, sizing/fit problems for furniture, or return-policy abuse — since a 3–5 point reduction in return rate would have a direct, quantifiable revenue impact.

<img width="1324" height="805" alt="returns_by_product" src="https://github.com/user-attachments/assets/c3b6c4bf-dd95-4599-a826-b80658f67bef" />

## 🛠️ Tool Used
 
- Microsoft Excel — data cleaning, formulas (SUMIFS, AVERAGEIFS), and PivotTables

## 🚀 About This Project
 
This is my first end-to-end data analysis project, built to practice structuring a messy dataset in Excel — cleaning it, building calculated fields, and summarizing it with PivotTables — and to practice communicating the results in writing. Dashboards/visual reporting (Excel dashboard or Power BI) are a planned next step.
 
**Author:** Jimrose Sugguiyao Gramaje
