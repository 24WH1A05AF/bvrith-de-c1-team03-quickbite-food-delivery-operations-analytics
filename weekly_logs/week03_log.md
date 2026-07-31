# Week 03 Log — Data Profiling, Schema Validation & Initial ETL

**Week:** 3
**Date range:** **25 July 2026 – 30 July 2026**
**Team:** Team 03
**Project:** QuickBite – Food Delivery Operations Analytics

---

## 1. Sprint Goal

The goal of Week 3 was to import the QuickBite datasets into Databricks, perform data profiling and schema validation, carry out data quality checks, and prepare the datasets for the Bronze layer by creating temporary views and conducting exploratory analysis.

---

## 2. Work Completed

| Task                                                                                             | Owner        | Status | Evidence              |
| ------------------------------------------------------------------------------------------------ | ------------ | ------ | --------------------- |
| Imported QuickBite datasets into Databricks                                                      | G. Shamithri | Done   | Databricks Notebook   |
| Validated schemas of all datasets                                                                | G. Shamithri | Done   | Notebook output       |
| Performed data profiling and record count analysis                                               | K. Ramya     | Done   | Databricks Notebook   |
| Checked null values and duplicate records                                                        | P. Sowmya    | Done   | Notebook results      |
| Created temporary SQL views for analysis                                                         | G. Shamithri | Done   | SQL Notebook          |
| Performed exploratory SQL analysis (city, revenue, payment mode, order status, delivery metrics) | Team 03      | Done   | Databricks Notebook   |
| Joined datasets to prepare an integrated analytical view                                         | Team 03      | Done   | SQL Queries           |
| Updated project notebook and GitHub repository                                                   | Team 03      | Done   | GitHub Commit History |

---

## 3. Key Decisions

* Used Databricks notebooks for centralized data profiling and SQL analysis.
* Created temporary SQL views before implementing the Bronze layer.
* Verified data quality before proceeding with ETL development.
* Prepared an integrated analytical view to support future Silver and Gold layer development.

---

## 4. Blockers / Risks

| Blocker                                                    | Impact                                               | Help Needed                                                                     |
| ---------------------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------- |
| Initial issues while loading Parquet files into Databricks | Delayed data import and profiling                    | Resolved by correcting the file loading method and validating the dataset paths |
| Understanding relationships among multiple datasets        | Required additional validation before joining tables | Team discussion and schema verification                                         |

---

## 5. Evidence Added to GitHub

* Updated Week 03 Databricks notebook.
* Added data profiling and schema validation results.
* Added SQL analysis queries.
* Added integrated analytical view queries.
* Updated Evidence Tracker with Week 03 progress.

---

## 6. AI Transparency Note

| Question                            | Response                                                                                                                                                                   |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Where AI helped                     | AI assisted in understanding Spark SQL syntax, explaining Databricks concepts, improving SQL queries, and refining the weekly documentation.                               |
| What we changed after AI suggestion | The notebook queries were reviewed, modified, and validated to match the project datasets before being committed.                                                          |
| What we verified manually           | Dataset loading, schema validation, record counts, SQL query outputs, joins, and profiling results were manually verified in Databricks.                                   |
| What we can explain without AI      | We can explain the Databricks workflow, dataset import process, schema validation, data profiling, SQL analysis, temporary views, and the overall ETL preparation process. |

---

## 7. Next Week Preparation

* Create Bronze Delta tables for all source datasets.
* Implement the Silver layer by cleaning and transforming data.
* Develop Gold-layer analytical tables and KPIs.
* Continue documenting the ETL pipeline and updating the GitHub repository.
