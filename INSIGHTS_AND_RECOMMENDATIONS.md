# E-commerce Insights and Recommendations

## Executive summary

The preparation workbook reports **$10.83 million in sales**, **125,226 orders**, and **100,000 users**. Search is the largest reported sales source, while the inventory summary shows substantially more unsold than sold items. The reported return rate is about **10%**. Several dashboard measures need definition checks before they are treated as decision-grade metrics, especially the unusually high average session duration.

## Key insights

### 1. Sales and order growth

- Reported total sales: **$10,827,119**.
- Reported total orders: **125,226**.
- Orders rise from **2,538 in 2019** to **59,041 in 2023**. The workbook shows **9,130 orders in 2024**; the year may be partial, so it should not be compared with full years without checking the coverage dates.
- Sales by gender are relatively balanced: approximately **$5.09M for F** and **$5.74M for M**.

**Recommendation:** Track monthly sales and orders with year-over-year comparisons, and label incomplete periods. Segment merchandising and campaigns by gender only after checking whether the difference is meaningful after accounting for order volume and product mix.

### 2. Returns and order status

- The overview reports a **10.01% return rate**.
- The order-item status summary contains **18,232 Returned** items out of **181,759** total items (about **10.03%**), **27,090 Cancelled**, **45,609 Complete**, **36,388 Processing**, and **54,440 Shipped**.
- The near match between the overview return rate and the item-level share is encouraging, but one is labeled as an order metric while the other is an item count. They may use different denominators.

**Recommendation:** Define return rate explicitly (returned orders divided by eligible delivered orders, or returned items divided by sold items). Report cancellations separately from returns, and investigate return reasons and rates by product category, item value, and delivery time.

### 3. Marketing contribution

The workbook's sales summary attributes approximately:

| Sales source | Sales | Share of reported sales |
|---|---:|---:|
| Search | $7.60M | 70.2% |
| Organic | $1.64M | 15.1% |
| Facebook | $0.63M | 5.8% |
| Email | $0.53M | 4.9% |
| Display | $0.44M | 4.0% |

Email has the largest reported session volume (**306,313**), followed by Adwords (**205,010**), YouTube (**68,202**), Facebook (**67,933**), and Organic (**34,301**). The sales and session summaries use different channel labels and likely different attribution fields, so they should not be directly compared as if they were the same source dimension.

**Recommendation:** Confirm channel definitions and attribution windows, then compare channels using consistent measures: spend, attributed revenue, conversion rate, and customer acquisition cost. Search is a clear candidate for deeper analysis, but do not increase budget based on sales totals alone without spend and margin data. Test email audience segmentation and campaign timing given its high session volume.

### 4. Shopping journey

- The workbook lists **845,607 product events**, **595,994 cart events**, and **181,759 purchase events**.
- The dashboard labels the product-to-cart rate as **70.5%** and cart-to-purchase rate as **30.5%**. These are event-count ratios, not necessarily user- or session-level conversion rates.
- Approximately **2.43M total events** and **681,759 sessions** are reported.

**Recommendation:** Recalculate the funnel using distinct sessions or users that progress through product view → cart → purchase. Break down drop-off by device, traffic source, product category, and new versus returning users. Review cart and checkout friction before treating event ratios as conversion rates.

### 5. Inventory exposure

- The workbook lists **490,705 inventory items**, with **181,759 sold** and **308,946 unsold**.
- This implies a sell-through share of about **37.0%** and an unsold share of about **63.0%**.
- Total inventory cost is reported as **$14.06M**. Jeans (**$1.81M**) and Outerwear & Coats (**$1.56M**) are the largest category cost lines in the summary, followed by Sweaters (**$1.10M**).
- These category amounts are total inventory cost, not confirmed unsold-stock value.

**Recommendation:** Prioritize an aging and sell-through review by category, product, and inventory age. Estimate the cost tied up specifically in unsold stock before proposing markdowns. Use targeted promotions for slow-moving items and review replenishment levels for fast-selling products.

## Data checks before publishing results

1. **Session duration:** The overview reports an average of **1,044.3 minutes**. Confirm the source unit and whether session durations were summed or averaged at the correct session grain; exclude or cap sessions with anomalous durations only under a documented rule.
2. **Metric grain:** The workbook mixes order-level KPIs, order-item status counts, event counts, and session counts. Preserve the grain and denominator in every chart and metric definition.
3. **Date coverage:** Confirm the dataset's latest date. The lower 2024 order and session totals may reflect partial-year coverage.
4. **Attribution:** Reconcile marketing source names across sales and session summaries before channel comparisons.
5. **Sensitive fields:** Avoid publishing raw user records, email addresses, street addresses, or precise location data.

## Source and scope

These findings were transcribed and calculated from the summary tables in the supplied `ee.xlsx` workbook. They are descriptive observations, not causal claims. The underlying source data was not reprocessed for this report, and the workbook's metric definitions may differ across dashboard sections.
