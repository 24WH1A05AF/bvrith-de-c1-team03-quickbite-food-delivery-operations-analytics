# Week 04 Log — Bronze Layer Data Ingestion

**Week:** 4  
**Date range:** 27 July 2026 – 31 July 2026  
**Team:** Team 03  
**Project:** QuickBite – Food Delivery Operations Analytics

---

## 1. Sprint Goal

The goal of Week 4 was to implement the Bronze Layer of the QuickBite data pipeline in Databricks. The team focused on ingesting raw datasets from multiple file formats, creating Bronze Delta tables, enriching the data with metadata columns, validating the ingestion results, and updating the project documentation.

---

## 2. Work Completed

| Task | Owner | Status | Evidence |
|---|---|---|---|
| Loaded Orders dataset (Parquet) into Spark DataFrame | Team 03 | Done | `Week04_Bronze_Ingestion` Notebook |
| Loaded Restaurants dataset (JSON) into Spark DataFrame | Team 03 | Done | `Week04_Bronze_Ingestion` Notebook |
| Loaded Riders dataset (CSV) into Spark DataFrame | Team 03 | Done | `Week04_Bronze_Ingestion` Notebook |
| Loaded Refunds dataset (CSV) into Spark DataFrame | Team 03 | Done | `Week04_Bronze_Ingestion` Notebook |
| Created temporary SQL views for all datasets | Team 03 | Done | SQL Notebook |
| Created Bronze temporary views | Team 03 | Done | SQL Notebook |
| Created Bronze Delta tables | Team 03 | Done | Databricks Catalog |
| Added metadata columns (`ingestion_time`, `load_date`, `source_file`) to Bronze tables | Team 03 | Done | Bronze Delta Tables |
| Validated Bronze tables by comparing row counts and sample records with source data | Team 03 | Done | SQL Query Results |
| Updated Week 04 documentation and notebook | Team 03 | Done | GitHub Repository |

---

## 3. Key Decisions

- Used Spark readers (`parquet`, `json`, and `csv`) according to the source file format.
- Stored all Bronze datasets as Delta tables for reliable storage and future processing.
- Added metadata columns (`ingestion_time`, `load_date`, and `source_file`) to support auditing and data lineage.
- Validated Bronze tables by comparing them with the original datasets before completing the sprint.

---

## 4. Blockers / Risks

| Blocker | Impact | Help Needed |
|---|---|---|
| Incorrect file path while reading source datasets | Initial data ingestion failed | Verified Unity Catalog volume path and corrected file locations |
| Error while creating permanent views from temporary views | Bronze view creation failed | Used temporary Bronze views before creating Delta tables |
| Different source file formats required different Spark readers | Data loading issues | Used the appropriate Spark reader for each dataset |

---

## 5. Evidence Added to GitHub

- Updated `weekly_logs/week04_log.md`
- Updated `Week04_Bronze_Ingestion` notebook
- Added Bronze Layer SQL scripts
- Added metadata implementation to Bronze tables
- Added validation queries and screenshots
- Updated the Evidence Tracker

---

## 6. AI Transparency Note

| Question | Response |
|---|---|
| Where AI helped | AI helped explain the Bronze Layer workflow, Spark DataFrame operations, Delta Lake implementation, metadata columns, and SQL queries for validation. |
| What we changed after AI suggestion | The team corrected file paths, selected the appropriate Spark readers, added metadata columns, and validated the Bronze tables by comparing them with the original datasets. |
| What we verified manually | Row counts, sample records, metadata columns, Delta table creation, and validation results were manually verified before updating GitHub. |
| What we can explain without AI | We can explain the Bronze Layer implementation, Spark DataFrames, temporary views, Delta tables, metadata columns, the validation process, and the role of the Bronze Layer in the Medallion Architecture. |

---

## 7. Next Week Preparation

- Begin implementation of the Silver Layer.
- Read data from Bronze Delta tables.
- Perform data cleaning and transformation.
- Handle missing values and duplicate records.
- Standardize data types.
- Create and validate Silver Delta tables.
- Continue updating project documentation and GitHub repository.
