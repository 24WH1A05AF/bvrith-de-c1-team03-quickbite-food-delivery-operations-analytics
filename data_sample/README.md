# QuickBite — Streaming Data Pipeline

## From Event Ingestion to Live Operational KPIs

QuickBite extends its batch analytics platform with a streaming pipeline
for incremental delivery-status events.

The streaming layer transforms incoming operational events into
standardized records, maintains the latest order status, and produces
live operational KPIs in Databricks.

---

## 1. Streaming Architecture

```text
JSON DELIVERY EVENTS
        │
        ▼
   AUTO LOADER
        │
        ▼
STREAMING BRONZE
        │
        ▼
STREAMING SILVER
        │
        ├──────────────────────┐
        ▼                      ▼
LIVE ORDER STATUS          LIVE KPIs
        │                      │
        └──────────┬───────────┘
                   ▼
          OPERATIONAL VIEW
