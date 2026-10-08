# QuickBite — Databricks Notebooks

This folder contains the Databricks notebooks used to build the
QuickBite Food Delivery Operations Analytics pipeline.

## Notebook Workflow

| Notebook | Purpose |
|---|---|
| `01_data_exploration.ipynb` | Explore source data and identify initial data issues |
| `02_bronze_ingestion.ipynb` | Ingest source data into the Bronze layer |
| `03_silver_transformations.ipynb` | Standardize and transform data into Silver |
| `04_data_quality_checks.ipynb` | Execute Data Quality validation rules |
| `05_gold_aggregations.ipynb` | Create business-ready Gold outputs |
| `06_powerbi_export.ipynb` | Prepare and validate Gold outputs for Power BI |
| `07_streaming_simulation.ipynb` | Process incremental delivery-status events |

## Batch Pipeline

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
