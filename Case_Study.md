# Where is the profit going? Enterprise Sales, Profitability & Revenue Leakage Analysis

**Role:** Data analyst | **Tools:** Excel, Power Query, Power Pivot, DAX, PivotTables, Forecast Sheet, What-If analysis
**Period analysed:** Jan-Oct 2026 compared with Jan-Oct 2024 (like-for-like)

## 1. The problem
A multinational retail group (13 stores, 11 countries, 6 regions) was growing fast, but profit was not following. Revenue rose 39% ($2.36M to $3.27M) while net profit fell 9% ($280K to $256K). Profit per $1 of sales dropped from 11.9c to 7.8c. Management needed to know where the money was going.

## 2. The data
Sales, returns, product cost history, regional targets, expenses, products and stores: 37,743 clean sales lines across 2024 to Oct 2026. The data was synthetic and generated with deliberate problems (such as invalid quantities and unassigned regions) to practise real-world cleaning. 12 invalid rows were excluded and kept in a separate sheet for transparency.

## 3. What I did
- **Data engineering:** used Power Query to import, clean and merge the tables, with refresh-ready steps.
- **Sales analysis:** regions, top and weak products, monthly and quarterly seasonality, actual vs target.
- **Profitability:** built gross profit, net profit and margin measures with DAX in the Data Model.
- **Leakage analysis:** examined margin by discount band, by category and by product; measured refunds and cost increases.
- **Forecast and scenarios:** six-month forecast with confidence bounds, plus four what-if scenarios.
- **Dashboard:** interactive dark executive dashboard with Year and Region filters.

## 4. What I found
| Finding | Evidence (Jan-Oct, 2026 vs 2024) |
|---|---|
| Gross margin fell | 25.8% to 20.9% |
| Discounts grew sharply | Average discount rate 6.7% to 8.8%; discount value $169K to $316K (+87%) |
| Heavy discounting destroyed profit | Sales above 10% discount were 26% of 2026 revenue but earned only $17K of $684K gross profit; 830 sales lines lost money |
| Electronics was the weak spot | 37% of revenue, 6% of gross profit; margin 13.7% at 0% discount but -4.2% at 11-20%, -18.3% at 21-30% and -33.0% at 31-40% |
| Low-margin devices | Laptop, smartphone and smart TV margins were about 0% or below in 2026 |
| Costs and refunds rose | Average unit cost up about 8% (2024 to 2026); refunds up 96% ($33.5K to $65.8K) |

## 5. Forecast and scenarios
The six-month forecast is about $2.45M in revenue. Net profit over that period under four scenarios:

| Scenario | Net profit | Net margin |
|---|---|---|
| Cost shock | $93K | 3.8% |
| Trend continues | $191K | 7.8% |
| Discount discipline (revenue -5.1%) | $258K | 11.1% |
| Back to 2024 margin | $291K | 11.9% |

## 6. Recommendations
1. Cap discounts at 10% on electronics.
2. Reprice or review laptops, smartphones and smart TVs.
3. Pass cost increases into prices and review supplier terms.
4. Reduce refunds by fixing the most-returned products (the UltraBook laptop has the highest refund total).
5. Track margin monthly, not only revenue.

## 7. Limitations
- The dataset is synthetic, so the findings illustrate the method rather than a real company.
- Scenarios are simple assumptions, not predictions.
- 2026 contains January to October only, so all comparisons use the same ten months of 2024.

## 8. What I learned
How to build an automated cleaning pipeline in Power Query, write DAX measures, tell a profit story with a dashboard, and turn findings into clear business recommendations.
