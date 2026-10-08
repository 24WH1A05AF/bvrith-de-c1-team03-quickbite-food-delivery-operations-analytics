# Dashboard Insights

## Purpose

This document explains what the QuickBite Power BI dashboard shows and
how the dashboard supports operational analysis.

---

## 1. Dashboard Pages

| Page | Purpose | Main Visuals |
|---|---|---|
| Page 1: Executive Overview | High-level operational summary | KPI cards, order trends, city-level analysis |
| Page 2: Restaurant & Delivery Performance | Analyse restaurant and delivery operations | Restaurant performance, cuisine analysis, delivery metrics, filters |

The streaming component is implemented as a separate Databricks streaming
workflow and is documented through the streaming outputs and lineage
evidence.

---

## 2. Key Insights

1. The dashboard contains approximately **150K orders** across the
   displayed operational period.

2. The displayed **delivery rate is 86.10%**, providing a high-level view
   of delivery performance.

3. The displayed **cancellation rate is 13.97%**, making cancellations an
   important operational metric to monitor.

4. The displayed **total revenue is ₹55.83M**.

5. The displayed **average delivery time is 23.98 minutes**.

6. The dashboard compares order volume across cities, allowing operational
   teams to identify differences in demand across locations.

7. Restaurant performance is analysed using multiple measures including
   order volume, preparation time, cancellation rate, delivery rate and
   average order value.

8. Zone-level delivery-time analysis provides a way to identify areas
   requiring closer operational investigation.

---

## 3. How the Dashboard Uses Gold Outputs

The Power BI dashboard represents the business-consumption layer of the
QuickBite data engineering pipeline.

```text
Source
   ↓
Bronze
   ↓
Silver
   ↓
Data Quality
   ↓
Trusted
   ↓
Gold
   ↓
Power BI
