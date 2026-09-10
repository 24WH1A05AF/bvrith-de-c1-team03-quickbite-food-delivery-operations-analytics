# Gold Metrics Definition

## KPI: Daily Order Count by Restaurant

### Business Question
How many orders does each restaurant receive each day?

### Formula
COUNT(*) of eligible orders.

### Grain
One row per restaurant per day.

Grain key:
- restaurant_id
- order_date

### Eligible Rows
Orders with a valid order_placed_ts.

### Outside Scope
Orders with a null order_placed_ts.

### Input
trusted_silver_orders

### Enrichment
trusted_silver_restaurants

### Join Type
LEFT JOIN

### Output Measure
daily_order_count

### Gold Table
gold_daily_restaurant_orders

## Validation Results

- Trusted Silver orders: 150,000
- Gold order count: 150,000
- Difference: 0
- Gold rows: 46,526
- Duplicate restaurant-date rows: 0
- Invalid/non-positive measures: 0
- Unmatched restaurant lookup rows: 250

## Controlled Rerun

The Gold table was recreated using the same transformation logic.

After rerun:
- Gold rows: 46,526
- Total orders: 150,000

The business results remained consistent.
