# QuickBite Data Dictionary

## Purpose

This document defines the structure, meaning, and role of the datasets used
throughout the QuickBite data engineering pipeline.

The data dictionary provides a common reference for source data, transformed
data, operational identifiers, and streaming events.

It supports:

- Data ingestion and transformation
- Data quality validation
- Gold-layer analytical modelling
- Power BI reporting
- Streaming operational analytics

---

## 1. Source Data Catalog

QuickBite uses operational datasets representing a food-delivery platform.

| Dataset | Grain | Purpose | Actual Scale |
|---|---|---|---:|
| `orders` | One row per order | Core order and delivery transaction data | 150K orders |
| `restaurants` | One row per restaurant | Restaurant master and operational information | 600 restaurants |
| `riders` | One row per rider | Rider and delivery-partner information | 2,500 riders |
| `refunds` | One row per refund record | Refund and exception information | 12K refunds |

The source layer represents operational data before transformation,
validation, and business modelling.

---

## 2. Core Business Entities

### Orders

The order entity represents the central business transaction in QuickBite.

Important identifiers include:

- `order_id` — unique identifier for an order
- `restaurant_id` — restaurant associated with the order
- `rider_id` — rider associated with delivery activity
- Order timestamp/date fields
- Order value / revenue fields
- Delivery and cancellation attributes

### Restaurants

The restaurant entity represents restaurants participating in the
food-delivery platform.

Important attributes include:

- `restaurant_id` — unique restaurant identifier
- Restaurant name
- Location / city / zone information
- Restaurant category or cuisine information
- Operational performance attributes

### Riders

The rider entity represents delivery partners responsible for order
fulfilment.

Important attributes include:

- `rider_id` — unique rider identifier
- Rider-related operational attributes
- Delivery activity
- Performance-related measures

### Refunds

The refund entity represents refund transactions and customer/order
exceptions.

Important identifiers include:

- Order reference
- Refund-related identifiers
- Refund amount
- Refund status / reason where available
- Refund timing information

---

## 3. Key Identifiers and Relationships

QuickBite uses business identifiers to connect operational entities.

```text
                    ┌──────────────┐
                    │ Restaurants  │
                    │ restaurant_id│
                    └──────┬───────┘
                           │
                           │
┌──────────────┐     ┌─────▼──────┐     ┌──────────────┐
│    Riders    │────►│   Orders   │◄────│   Refunds    │
│   rider_id   │     │  order_id  │     │   order_id   │
└──────────────┘     └────────────┘     └──────────────┘
