# QuickBite — Project Documentation

This folder contains the documentation supporting the QuickBite Food
Delivery Operations Analytics project.

The documentation explains the business problem, data design,
data-quality validation, Gold-layer metrics, dashboard insights and
end-to-end engineering workflow.

---

## Documentation Index

| Document | Purpose |
|---|---|
| `problem_charter.md` | Defines the QuickBite business problem, stakeholders and project objectives |
| `data_dictionary.md` | Documents important source and transformed data fields |
| `synthetic_data_assumptions.md` | Records assumptions used in the synthetic operational datasets |
| `data_quality_summary.md` | Documents Data Quality rules, validation results and identified issues |
| `gold_metrics_definition.md` | Defines the business metrics and analytical purpose of Gold outputs |
| `dashboard_insights.md` | Documents the key business insights derived from the Power BI dashboard |
| `pipeline_walkthrough.md` | Explains the end-to-end QuickBite data engineering pipeline |
| `references.md` | Records project references and learning resources |

---

## QuickBite Engineering Story

The project follows a layered data engineering architecture:

```text
Source Data
     ↓
Bronze
     ↓
Silver
     ↓
Data Quality
     ↓
Trusted Data
     ↓
Gold
     ↓
Power BI
