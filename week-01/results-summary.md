# Week 1 Results Summary: Data Foundation

## Goal
Profile, clean, integrate and document the 12-table heavy supplier dataset.

## Data received
12 CSV files: branches, customers, inventory_master, invoices, payments, products,
purchase_orders_header, purchase_orders_lines, sales_orders_header, sales_orders_lines,
stock_ledger and suppliers.

## Problems found
- [e.g. missing values in some columns]
- [e.g. duplicate rows in some tables]
- [e.g. dates stored as text]
- [e.g. keys that did not match between tables]

## Fixes applied
- Standardised column names and text, and fixed data types
- Removed duplicates and handled missing values
- Checked impossible values such as negative quantities
- [add any other fix you made]

## Outputs
Integrated and feature-engineered datasets:

| Dataset | Rows | Columns | Missing cells |
|---|---|---|---|
| sales_features | 130,402 | 26 | 0 |
| purchase_features | 155,495 | 24 | 30,836 |
| inventory_features | 180 | 12 | 0 |
| finance_features | 21,480 | 16 | 9,010 |
| customer_features | 500 | 5 | 0 |
| stock_ledger_clean | 237,230 | 9 | 0 |

Engineered features: line_revenue, order_month, delivery_delay_days, is_late,
stock_value, days_since_last_movement, payment_delay_days, is_overdue,
and customer-level aggregates (first order, last order, order count, total spend).

## Validation
Checks were run for negative quantities, missing keys, duplicate product-branch rows
and invalid dates. Results and decisions are in docs/validation_log.csv.

## Next steps
ABC classification, slow and dead stock, inventory turnover, overstock and understock detection.
