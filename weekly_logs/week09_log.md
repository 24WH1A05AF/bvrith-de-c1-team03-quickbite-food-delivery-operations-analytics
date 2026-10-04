# Week 09 Log — Dashboard Refinement and Insight Communication

**Week:** 9  
**Date range:** 28 September 2026 – 4 October 2026  
**Team:** Team 03  
**Project:** QuickBite – Food Delivery Operations Analytics

---

## 1. Sprint Goal

Refine the validated Week-8 Power BI dashboard by improving visual
alignment, consistency and usability. Test slicer and filter interactions,
reconcile important dashboard values with the owning Gold tables, and
document evidence-backed dashboard insights.

---

## 2. Work Completed

| Task | Owner | Status | Evidence |
|---|---|---|---|
| Reviewed the existing Week-8 Power BI dashboard and Gold-only model | Team 03 | Done | `dashboard/powerbi_dashboard.pbix` |
| Aligned KPI cards, visual borders and dashboard elements | Team 03 | Done | `screenshots/week09_02_refined_page_01.png` |
| Improved spacing, alignment and visual hierarchy | Team 03 | Done | `screenshots/week09_02_refined_page_01.png` |
| Standardized titles, labels and number formatting | Team 03 | Done | Power BI dashboard |
| Refined Executive Overview page | Team 03 | Done | `screenshots/week09_02_refined_page_01.png` |
| Refined Restaurant & Delivery Performance page | Team 03 | Done | `screenshots/week09_03_refined_page_02.png` |
| Tested city, date and relevant slicer/filter interactions | Team 03 | Done | `screenshots/week09_04_filter_interaction.png` |
| Reconciled an important filtered Power BI value with its owning Gold table | Team 03 | Done | `screenshots/week09_05_filtered_reconciliation.png` |
| Documented evidence-backed dashboard observations | Team 03 | Done | `docs/dashboard_insights.md` |
| Updated dashboard documentation and Week-9 evidence | Team 03 | Done | `dashboard/README.md`, `screenshots/week09_*.png` |

---

## 3. Key Decisions

- Continued with the same validated Week-8 Power BI model instead of
  rebuilding the dashboard.
- Kept the approved Gold tables as the only business data sources for the
  dashboard.
- Improved visual consistency by aligning borders, KPI cards, spacing and
  dashboard elements.
- Standardized formatting, titles and labels to improve readability.
- Kept dashboard pages organized around business questions rather than
  creating one visual for each Gold table.
- Tested slicer and filter behaviour without introducing unsafe
  relationships.
- Preserved the existing KPI definitions and business meaning.
- Reconciled important dashboard values with their owning Gold tables under
  matching filter conditions.
- Documented insights only from observations supported by the dashboard and
  Gold data.

---

## 4. Blockers / Risks

| Blocker | Impact | Help Needed |
|---|---|---|
| Initial visual elements had inconsistent spacing and border alignment | Reduced dashboard consistency and readability | Resolved through manual alignment and formatting |
| Slicer/filter interactions required validation across visuals | Risk of unintended filtering between visuals | Resolved by testing visual interactions |
| Dashboard values needed to remain traceable to their owning Gold tables | Risk of reporting mismatch if filter states differed | Resolved through Gold-to-Power BI reconciliation |

**Final Status:** No unresolved Week-9 blocker.

---

## 5. Evidence Added to GitHub

screenshots/
└── week09_01_refined_page_01.png

---

## 6. AI Transparency Note

| Question | Response |
|---|---|
| Where AI helped | AI helped us understand the Week-9 refinement workflow, plan dashboard improvements, troubleshoot Power BI issues, structure the documentation and identify the required evidence. |
| What we changed after AI suggestion | We adapted the suggestions to our actual QuickBite dashboard, Gold tables, Power BI pages and repository structure. We manually performed the visual alignment, border adjustments, spacing improvements and formatting changes. |
| What we verified manually | We manually verified the Gold sources, Power BI model, dashboard visuals, KPI values, slicer/filter behaviour, reconciliation results, screenshots and documentation. |
| What we can explain without AI | Every team member can explain the Gold-to-Power BI flow, dashboard pages, KPI ownership, filtering behaviour, reconciliation process and the purpose of the documented insights. |

---

## 7. Next Week Preparation

- Preserve the validated Week-9 batch Power BI dashboard and Gold model.
- Begin the approved streaming implementation workflow.
- Process incremental streaming events through the Bronze, Silver and Gold
  layers.
- Validate streaming data, checkpoints and incremental processing.
- Reconcile streaming Gold outputs and prepare Week-10 evidence.
- Keep the validated batch dashboard separate from the new streaming
  workflow.
