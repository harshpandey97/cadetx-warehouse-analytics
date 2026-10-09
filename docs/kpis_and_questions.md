# KPIs and Analysis Questions

## Proposed KPIs
| KPI | Formula | Source table |
|---|---|---|
| Inventory turnover | Units sold / average stock on hand | sales_features, inventory_features |
| Dead stock % | Stock value with no movement 180+ days / total stock value | inventory_features |
| Stock value by branch | On-hand quantity x unit cost | inventory_features |
| Supplier on-time delivery % | On-time purchase orders / total purchase orders | purchase_features |
| Average delivery delay (days) | Mean of received date - expected date | purchase_features |
| Revenue per customer | Total revenue / active customers | sales_features, customer_features |
| Average payment delay (days) | Mean of payment date - due date | finance_features |
| Overdue invoice % | Overdue invoices / total invoices | finance_features |

## Analysis questions
1. Which 20% of products generate about 80% of revenue (ABC classification)?
2. Which products and branches hold the most slow or dead stock?
3. Which products have the highest and lowest inventory turnover?
4. Which branches are overstocked or understocked relative to demand?
5. Which suppliers deliver late most often, and by how many days?
6. Which customers drive the most revenue, and which have stopped ordering?
7. How does monthly demand vary over time?
8. Which customers pay late, and how much revenue is overdue?
