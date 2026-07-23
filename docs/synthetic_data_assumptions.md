# Synthetic Data Assumptions

**Week:** 2  
**Purpose:** Document how educational synthetic data is created for the QuickBite project.

---

## 1. Synthetic Data Boundary

This project uses only synthetic data created for educational purposes. The datasets do not represent any real food delivery company, restaurant, customer, delivery partner, or business transactions. The data is generated only for learning, analysis, and project implementation.

---

## 2. Domain Assumptions

| Area | Assumption |
|---|---|
| Geography / Scope | Hyderabad and nearby regions |
| Time Period | July 2026 – September 2026 |
| Source Systems | Customer Orders, Restaurant Management, Delivery Tracking, Payment System |
| Event Types | Order Placement, Order Confirmation, Food Preparation, Pickup, Delivery, Payment |
| Reference Data | Restaurants, Customers, Delivery Partners, Menu Items, Payment Methods |

---

## 3. Data Volume Assumptions

| File | Approximate Rows | Reason |
|---|---:|---|
| `orders.csv` | 10,000 | Represents customer food orders |
| `restaurants.csv` | 500 | Restaurant information |
| `customers.csv` | 5,000 | Customer details |
| `delivery_events.json` | 15,000 | Delivery status and tracking events |

---

## 4. Controlled Data Quality Issues

| Issue Type | Approx. Share | Why Include It |
|---|---:|---|
| Duplicate Order IDs | 0.2%–0.5% | Tests uniqueness constraints |
| Missing Customer Details | 1%–3% | Tests completeness |
| Invalid Restaurant IDs | 0.5%–1% | Tests referential integrity |
| Negative Delivery Time | 0.1%–0.5% | Tests validation rules |
| Timestamp Inconsistencies | 0.1%–0.3% | Tests chronological order |

---

## 5. Manual Verification

Before using the generated data, the team verified that:

- Row counts are realistic and appropriate.
- All key fields are present.
- Dates, prices, and delivery times appear reasonable.
- Controlled data quality issues exist but do not dominate the dataset.
- Different source files require proper cleaning and standardization before analysis.
