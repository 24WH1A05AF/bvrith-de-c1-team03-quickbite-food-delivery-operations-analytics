# Week 06 Log — Silver Candidate to Trusted Silver

**Week:** 6  
**Date range:** 10 August 2026 – 16 August 2026  
**Team:** Team 03  
**Project:** QuickBite – Food Delivery Operations Analytics

---

## 1. Sprint Goal

Create and validate Trusted Silver Delta tables from the Silver Candidate layer. Verify the required Silver Candidate datasets, ensure successful data transfer into Trusted Silver tables, and prepare trusted datasets for Gold-layer analytics.

---

## 2. Work Completed

| Task | Owner | Status | Evidence |
|---|---|---|---|
| Verified Silver Candidate tables (`silver_orders_candidate`, `silver_refunds_candidate`, `silver_restaurants_candidate`, `silver_riders_candidate`) | Team 03 | Done | Databricks Notebook |
| Confirmed active catalog and schema | Team 03 | Done | SQL Query Output |
| Created `trusted_silver_orders` Delta table | Team 03 | Done | Databricks SQL |
| Created `trusted_silver_refunds` Delta table | Team 03 | Done | Databricks SQL |
| Created `trusted_silver_restaurants` Delta table | Team 03 | Done | Databricks SQL |
| Created `trusted_silver_riders` Delta table | Team 03 | Done | Databricks SQL |
| Verified Trusted Silver tables using `SHOW TABLES` | Team 03 | Done | SQL Output |
| Validated row counts between Silver Candidate and Trusted Silver tables | Team 03 | Done | SQL Validation Results |

---

## 3. Key Decisions

- Used validated Silver Candidate tables as the source for Trusted Silver.
- Verified row counts after table creation to ensure no data loss.
- Approved Trusted Silver tables as the source for Week 7 Gold processing.

---

## 4. Blockers / Risks

| Blocker | Impact | Help Needed |
|---|---|---|
| No major blockers encountered | Trusted Silver tables were created and validated successfully | No additional support required |

---

## 5. Evidence Added to GitHub

- Updated Week 06 Databricks notebook.
- SQL queries for Trusted Silver table creation.
- Trusted Silver table verification.
- Row-count validation results.
- Week 06 log documentation.

---

## 6. AI Transparency Note

| Question | Response |
|---|---|
| Where AI helped | AI assisted in explaining the Week 6 workflow, SQL validation steps, and documentation preparation. |
| What we changed after AI suggestion | Reviewed the SQL execution sequence and verified the Trusted Silver table creation before validation. |
| What we verified manually | Verified table creation, table availability, and row counts using Databricks SQL. |
| What we can explain without AI | Trusted Silver creation process, SQL queries used, validation steps, and row-count verification. |

---

## 7. Next Week Preparation

- Build the Gold layer using the Trusted Silver tables.
- Define KPIs, perform aggregations, validate reconciliation, and document the Gold layer outputs.
