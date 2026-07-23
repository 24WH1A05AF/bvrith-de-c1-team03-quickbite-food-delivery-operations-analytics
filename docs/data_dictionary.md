# Data Dictionary

**Week:** 2  
**Purpose:** Define raw, reference, Silver, and streaming fields for the QuickBite project.

---

## 1. Source File Catalog

| File Name | Grain | Purpose | Approx. Rows | Notes |
|---|---|---|---:|---|
| `orders.csv` | One row per order | Stores customer order details | 10,000 | Primary transaction dataset |
| `customers.csv` | One row per customer | Stores customer information | 5,000 | Customer master data |
| `restaurants.csv` | One row per restaurant | Stores restaurant details | 500 | Reference dataset |
| `delivery_events.json` | One row per event | Streaming delivery status updates | 15,000 | JSON event files |

---

## 2. Raw File Schema: `orders.csv`

| Field Name | Data Type | Required? | Example | Description |
|---|---|---|---|---|
| `order_id` | string | Yes | `ORD-1001` | Unique order ID |
| `customer_id` | string | Yes | `CUS-2001` | Customer identifier |
| `restaurant_id` | string | Yes | `RES-301` | Restaurant identifier |
| `order_date` | date | Yes | `2026-07-20` | Order date |
| `order_amount` | decimal | Yes | `450.75` | Total order amount |
| `payment_method` | string | Yes | `UPI` | Payment mode |

---

## 3. Raw File Schema: `customers.csv`

| Field Name | Data Type | Required? | Example | Description |
|---|---|---|---|---|
| `customer_id` | string | Yes | `CUS-2001` | Unique customer ID |
| `customer_name` | string | Yes | `Rahul Sharma` | Customer name |
| `city` | string | Yes | `Hyderabad` | Customer location |
| `phone_number` | string | No | `9876543210` | Contact number |

---

## 4. Reference File Schema

| Field Name | Data Type | Required? | Example | Description |
|---|---|---|---|---|
| `restaurant_id` | string | Yes | `RES-301` | Restaurant ID |
| `restaurant_name` | string | Yes | `Spicy Bites` | Restaurant name |
| `category` | string | Yes | `South Indian` | Food category |
| `location` | string | Yes | `Madhapur` | Restaurant location |

---

## 5. Canonical Silver Table Design

Final Silver table name:

```text
silver_food_orders
```

| Silver Field | Data Type | Source Mapping | Business Meaning |
|---|---|---|---|
| `order_id` | string | orders.order_id | Unique order identifier |
| `customer_id` | string | orders.customer_id | Customer identifier |
| `restaurant_id` | string | orders.restaurant_id | Restaurant identifier |
| `order_date` | date | orders.order_date | Order date for analytics |
| `order_amount` | decimal | orders.order_amount | Revenue generated |
| `payment_method` | string | orders.payment_method | Payment type |

---

## 6. Streaming Event Schema

| Field Name | Data Type | Required? | Example | Description |
|---|---|---|---|---|
| `event_id` | string | Yes | `EVT-1001` | Unique event ID |
| `event_timestamp` | timestamp | Yes | `2026-07-20T10:30:00+05:30` | Event time |
| `event_type` | string | Yes | `Order Delivered` | Delivery event type |
| `order_id` | string | Yes | `ORD-1001` | Related order ID |
| `delivery_status` | string | Yes | `Delivered` | Current delivery status |
