# Power-BI---Supply-Chain-Analysis
# 📦 Power BI - Supply Chain Management Dashboard

## I. Introduction

### Project Overview

This project was developed to analyze supply chain performance. Through data cleaning, DAX measure development, and interactive dashboard design, the project provides a comprehensive view of supplier performance, logistics operations, and business performance at the SKU level.

The report was built to help the supply chain management team identify potential issues, analyze product performance, and optimize shipping and inventory operations.

---

## II. Project Objectives

The project was designed to answer the following key business questions:

- Which suppliers deliver the best balance of cost and quality?
- Which carriers and routes offer the most optimal cost and delivery times?
- Which SKUs are at critical stock risk and require urgent action?
- Which product categories contribute the most revenue and profit?
- Which regions show unusually high defect rates that need investigation?
- Where should the business allocate resources to improve overall supply chain performance?

---

## III. Data Description

### Onyx Data DataDNA Supply Chain Dataset

The dataset consists of 100 rows and 26 columns, describing the full product lifecycle from supplier to end customer.

| Column Name | Description |
|---|---|
| SKU | Product identifier |
| Product Type | Product category (Skincare, Haircare, Cosmetics) |
| Price | Product selling price |
| Supplier Name | Name of the supplier |
| Order Quantities | Quantity ordered |
| Lead Time | Order lead time (days) |
| Manufacturing Cost | Cost of manufacturing |
| Defect Rate | Defect rate percentage |
| Shipping Carrier | Shipping carrier used |
| Route | Shipping route |
| Transportation Mode | Mode of transport (Road, Rail, Air, Sea) |
| Shipping Cost | Cost of shipping |
| Shipping Times | Shipping duration |
| Stock Levels | Inventory stock level |
| Location | Region (Bangalore, Chennai, Delhi, Kolkata, Mumbai) |
| Customer Demographics | Customer demographic data |
| Revenue Generated | Revenue generated |

---

## IV. Project Methodology

### 1. Data Cleaning & Preparation

- Checked for missing values and data format inconsistencies
- Standardized supplier names, carriers, and locations
- Reviewed anomalies in Defect Rate and Lead Time

### 2. Data Modeling & DAX Measures

- Built DAX measures for Unit Cost, %Cost/Revenue, and Avail%
- Designed a dynamic SVG-based calculated column (progress ring) to visualize stock availability per SKU
- Applied Conditional Formatting to highlight anomalies (high defect rate, high cost)

### 3. Dashboard Development

The report consists of 4 interactive pages, connected through cross-chart filtering:

- **Suppliers** - evaluates supplier performance by volume, cost, and quality
- **Inventory & Logistics** - monitors stock levels, carriers, routes, and transportation modes
- **SKU Performance** - analyzes cost and revenue at the SKU level
- **Insights** - summarizes key findings in natural language


---

## V. Dashboard

### Overview Dashboard

<img width="1509" height="716" alt="image" src="https://github.com/user-attachments/assets/44f858d9-4660-491a-85e8-9f481502b35e" />
<img width="1362" height="715" alt="image" src="https://github.com/user-attachments/assets/b95c2a9e-af32-4484-95b1-851cecac74da" />
<img width="1351" height="686" alt="image" src="https://github.com/user-attachments/assets/eb73d51f-63f9-4d20-a579-6036cb0ee024" />

---

## VI. Key Insights

### 1. Suppliers – Trade-off Between Volume, Cost, and Quality

**Supplier 1** leads in order volume (1,458 orders) and revenue (158K), but is not the cheapest supplier.

**Supplier 2** has the lowest unit cost (0.06) yet the highest defect rate (0.52%), clearly illustrating the trade-off between price and quality when selecting a supplier.

This suggests the business should consider a multi-sourcing strategy rather than relying on a single cost or volume criterion.

### 2. Inventory & Logistics – Shipping Efficiency and Stock Risk

**Carrier B** handles the largest shipping volume (45.31%) and offers the fastest delivery time (5.30 days).

**Road** is the fastest transportation mode (4.72 days); **Sea** is the slowest (7.12 days) but the cheapest (0.010/unit) — highlighting a clear trade-off between speed and shipping cost.

**Carrier B combined with Route A** delivers the most optimal outcome for both cost and delivery time, making it the preferred choice for orders requiring balance between the two.

**SKU10** is at a critical stock level (Avail 11%), requiring urgent replenishment to avoid supply disruption.

In terms of manufacturing lead time, Mumbai should generally be avoided; specifically, **Supplier 5 should avoid Delhi** due to notably high lead times in that region.

**Chennai and Delhi** have failure rates exceeding 50%, with Delhi showing manufacturing costs 38% above average. Chennai also recorded a higher defect rate at 2.6 — both regions require priority review of their quality control processes.

### 3. SKU Performance – High Revenue Does Not Always Mean High Margin

**Skincare** generates the highest revenue (0.24M, 42% of total revenue) but has the lowest average unit price (11.66), resulting in the thinnest per-unit profit margin among the three categories.

Customer demographic analysis reveals: **women rarely purchase Haircare** (only 2% share), while **men rarely purchase Cosmetics** (only 4% share). This provides a data-driven basis for developing targeted product and marketing strategies by customer segment and category.

---

## VII. Conclusion & Recommendations

### Conclusion

The supply chain generated total revenue of 577,605, total cost of 52,925. However, performance varies significantly across suppliers, regions, and carriers - particularly the trade-off between low cost and quality at the supplier level, and between speed and cost at the shipping level.

The Skincare category leads in revenue but carries the thinnest per-unit margin, indicating that sales volume growth does not necessarily translate into proportional profit growth. Meanwhile, certain regions (Chennai, Delhi) show defect rates above safe thresholds and require priority attention.

### Recommendations

- Adopt a multi-sourcing strategy to balance cost and quality, avoiding over-reliance on a single supplier.
- Prioritize Carrier B and Route A for orders requiring simultaneous optimization of cost and delivery time.
- Urgently replenish stock for SKUs at critical levels (Avail% below 15%).
- Investigate and improve quality control processes in Chennai and Delhi.
- Reassess pricing strategy for the Skincare category to improve per-unit profit margin.
- Develop segment-specific marketing strategies based on identified gender and category purchasing differences.
- Establish %Cost/Revenue (currently at 9.16%) as a benchmark KPI to track cost efficiency across periods.

---

## VIII. Tools & Technologies

- **Microsoft Power BI**
  - DAX Measures & Calculated Columns
  - Custom SVG Visualization (Progress Ring)
  - ZoomCharts Drill Down Visuals
  - Cross-Chart Filtering
  - Conditional Formatting
  - Bookmarks & Interactive Navigation

---

## 🔗 Links

- LinkedIn: [Dương Minh Nhật](https://www.linkedin.com/in/duong-minh-nhat-4084091b8/)
- GitHub: [duon97](https://github.com/duon97)
