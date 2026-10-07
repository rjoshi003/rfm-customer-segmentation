# RFM Customer Segmentation — Online Retail Dataset

Segmented customers of a UK-based online gift retailer by purchase behavior using RFM (Recency, Frequency, Monetary) analysis, to identify who drives the business and who's at risk of churning.

**Dataset:** [UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail) — ~540K transaction line items, Dec 2010–Dec 2011.

**Tools:** Python, pandas, matplotlib, seaborn

## Method

1. Cleaned the raw transaction data: removed duplicates, rows with no real `CustomerID`, and bad/zero-price entries (~26% of rows dropped overall)
2. Computed Recency, Frequency, and Monetary value per customer
3. Scored each metric into quartiles (1-4) and combined into an RFM score (3-12)
4. Bucketed customers into 5 segments: **Champions, Loyal Customers, Potential Loyalists, At Risk, Hibernating/Lost**
5. Visualized segment distribution, revenue contribution, and recency/frequency/monetary patterns

## Key Findings

- **Champions are ~29% of customers but generate ~77% of total revenue** — a small core of highly engaged customers drives the overwhelming majority of the business.
- **Median customer has only 2 orders and ~£669 lifetime spend** — most customers sit well below "Champion" status, leaving a large addressable middle segment.
- **"At Risk" customers (991, the 2nd-largest segment) contribute only 3.5% of revenue** — a win-back opportunity with a clear behavioral trigger (recency) and lower cost than new acquisition.
- **Hibernating/Lost customers (~7%) contribute under 1% of revenue** — low priority for retention spend.

## Files

- `RFM_Customer_Segmentation.ipynb` — full analysis notebook (code + narrative + charts), run end-to-end with real outputs
- `rfm_customer_segments.csv` — final customer-level RFM scores and segment labels
- `rfm_charts.png` — summary visualizations
- `online_retail.zip` — cleaned source data, zipped (unzip to get `online_retail.csv`); [original source](https://archive.ics.uci.edu/dataset/352/online+retail)
