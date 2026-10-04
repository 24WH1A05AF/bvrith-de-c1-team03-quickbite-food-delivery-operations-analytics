# Week 08 Log — Gold to Power BI

**Week:** 8  
**Date range:** 21-09-26  -  29-09-26 
**Team:** Team 03  
**Project:** QuickBite – Food Delivery Operations Analytics

---

## 1. Sprint Goal

Establish a controlled hand-off of the approved QuickBite Gold layer to Power BI and build the first working reporting dashboard. The sprint focused on validating the Gold reporting sources, connecting the required Gold tables to Power BI, developing business-focused dashboard pages, and reconciling key dashboard measures back to their owning Gold table.

---

## 2. Work Completed

| Task | Owner | Status | Evidence |
|---|---|---|---|
| Reviewed approved Gold outputs from Week 7 | Team 03 | Done | `05_gold_aggregations.ipynb` |
| Identified Gold reporting sources required for Power BI | Team 03 | Done | Gold source register |
| Validated Gold tables and reporting outputs | Team 03 | Done | Databricks Notebook |
| Connected approved Gold tables to Power BI | Team 03 | Done | Power BI model |
| Loaded `gold_daily_operations_summary` | Team 03 | Done | Power BI model |
| Loaded `gold_daily_order_trend` | Team 03 | Done | Power BI model |
| Loaded `gold_daily_restaurant_orders` | Team 03 | Done | Power BI model |
| Loaded `gold_delivery_sla` | Team 03 | Done | Power BI model |
| Loaded `gold_restaurant_performance` | Team 03 | Done | Power BI model |
| Loaded `gold_rider_performance` | Team 03 | Done | Power BI model |
| Built Executive Overview dashboard | Team 03 | Done | Power BI Page 1 |
| Built Restaurant & Delivery Performance dashboard | Team 03 | Done | Power BI Page 2 |
| Added Total Orders KPI | Team 03 | Done | Power BI Page 1 |
| Added Delivery Rate KPI | Team 03 | Done | Power BI Page 1 |
| Added Cancellation Rate KPI | Team 03 | Done | Power BI Page 1 |
| Added Total Revenue KPI | Team 03 | Done | Power BI Page 1 |
| Added Average Delivery Time KPI | Team 03 | Done | Power BI Page 1 |
| Added 90-day order trend | Team 03 | Done | Power BI Page 1 |
| Added Orders by City comparison | Team 03 | Done | Power BI Page 1 |
| Added On-Time Delivery Trend | Team 03 | Done | Power BI Page 1 |
| Added date and city filters | Team 03 | Done | Power BI Page 1 |
| Added restaurant performance analysis | Team 03 | Done | Power BI Page 2 |
| Added cuisine-wise order analysis | Team 03 | Done | Power BI Page 2 |
| Added revenue mix by cuisine | Team 03 | Done | Power BI Page 2 |
| Added average delivery time by zone | Team 03 | Done | Power BI Page 2 |
| Added delivery rate by city | Team 03 | Done | Power BI Page 2 |
| Reconciled Total Orders against Gold | Team 03 | Done | `06_powerbi_export.ipynb` |
| Reconciled Delivery Rate against Gold | Team 03 | Done | `06_powerbi_export.ipynb` |
| Reconciled Cancellation Rate against Gold | Team 03 | Done | `06_powerbi_export.ipynb` |
| Reconciled Total Revenue against Gold | Team 03 | Done | `06_powerbi_export.ipynb` |
| Reconciled Average Delivery Time against Gold | Team 03 | Done | `06_powerbi_export.ipynb` |
| Captured Power BI and reconciliation evidence | Team 03 | Done | `screenshots/week08_*` |

---

## 3. Key Decisions

- Power BI reporting uses approved Gold outputs only.
- The six Gold reporting tables were retained as separate reporting sources rather than unnecessarily flattening them into a single dataset.
- Dashboard pages were designed around business questions and operational KPIs rather than creating one visual per Gold table.
- The first dashboard page focuses on overall QuickBite operational performance, including order volume, delivery performance, cancellation, revenue and trends.
- The second dashboard page focuses on restaurant and delivery performance, including restaurant, cuisine, city, zone and preparation-time analysis.
- KPI calculations were reconciled against the owning Gold output using the same reporting period as the Power BI dashboard.
- The Week 8 dashboard and model were treated as the working governed version, with further refinement and deeper insight storytelling planned for Week 9.

---

## 4. Blockers / Risks

| Blocker | Impact | Help Needed |
|---|---|---|
| Gold tables were initially queried using the wrong catalog/schema | The Gold tables could not be found using the incorrect fully qualified name | Resolved by validating the active catalog and schema and using `workspace.default` |
| Power BI KPI values use display rounding and abbreviation | Direct visual comparison can show rounded values compared with the underlying Gold values | Resolved through Gold-to-Power BI reconciliation using the same filter state |

**Final status:** No unresolved blocker prevented completion of the Week 8 dashboard and reconciliation.

---

## 5. Evidence Added to GitHub

- Updated `notebooks/06_powerbi_export.ipynb`
- Existing Gold aggregation notebook:
  - `notebooks/05_gold_aggregations.ipynb`
- Power BI dashboard:
  - `dashboard/powerbi_dashboard.pbix`
- Gold source register and validation evidence
- Power BI model evidence
- Executive Overview dashboard screenshot
- Restaurant & Delivery Performance dashboard screenshot
- Gold-to-Power BI reconciliation evidence
- Updated:
  - `weekly_logs/week08_log.md`

### Week 8 Screenshots

- `screenshots/week08_03_powerbi_model.png`
- `screenshots/week08_04_dashboard_page_01.png`
- `screenshots/week08_05_dashboard_page_02.png`
- `screenshots/week08_06_measure_reconciliation.png`

---

## 6. AI Transparency Note

| Question | Response |
|---|---|
| Where AI helped | AI assisted with understanding the Gold-to-Power BI hand-off, planning the reporting workflow, troubleshooting implementation issues, structuring the dashboard and preparing project documentation. |
| What we changed after AI suggestion | The team reviewed the suggested approach against the actual QuickBite Gold tables and Power BI model. The final implementation was adapted to the project's actual catalog, schema, Gold tables and dashboard structure. |
| What we verified manually | The team manually verified Gold table availability, Gold schemas, Power BI source tables, dashboard fields, KPI values, filters, dashboard pages and Gold-to-Power BI reconciliation results. |
| What we can explain without AI | The team can explain the Gold layer, Gold-to-Power BI hand-off, table purpose, KPI calculations, dashboard structure, filtering, reconciliation process and source-to-report traceability. |

---

## 7. Next Week Preparation

- Continue with the same working Power BI model and PBIX rather than rebuilding it.
- Refine dashboard visual hierarchy, labels, layout and usability.
- Test filtering and interactions across the completed dashboard pages.
- Improve presentation-ready KPI and visual context.
- Develop evidence-backed operational insights from the validated Gold outputs.
- Prepare the final business story and decision-oriented interpretation of the dashboard.
- Maintain source-to-report traceability for important visuals and KPIs.
