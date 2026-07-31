Week 04 Log — Bronze Layer Data Ingestion

Week: 4
Date Range: 28 July 2026 – 31 July 2026 (Update if your instructor specifies different dates.)
Team: Team 03 (Replace with your actual team name/number.)
Project: QuickBite – Food Delivery Data Engineering Pipeline

1. Sprint Goal

The goal of this sprint was to implement the Bronze layer of the QuickBite ETL pipeline in Databricks. This included ingesting raw datasets from multiple file formats, creating Bronze Delta tables, adding metadata columns, and validating the ingested data.

2. Work Completed
Task	Owner	Status	Evidence
Loaded Orders dataset (Parquet) into Spark DataFrame	Team 03	Done	Week04_Bronze_Ingestion Notebook
Loaded Restaurants dataset (JSON) into Spark DataFrame	Team 03	Done	Week04_Bronze_Ingestion Notebook
Loaded Riders dataset (CSV) into Spark DataFrame	Team 03	Done	Week04_Bronze_Ingestion Notebook
Loaded Refunds dataset (CSV) into Spark DataFrame	Team 03	Done	Week04_Bronze_Ingestion Notebook
Created temporary SQL views for all datasets	Team 03	Done	Databricks Notebook
Created Bronze temporary views	Team 03	Done	Databricks Notebook
Created Bronze Delta tables	Team 03	Done	Databricks Catalog
Added metadata columns (ingestion_time, load_date, source_file)	Team 03	Done	Bronze Delta Tables
Validated Bronze tables by comparing row counts and sample records with source data	Team 03	Done	SQL Query Results
3. Key Decisions
Used Spark readers based on file format (parquet, json, and csv).
Stored all Bronze datasets as Delta tables.
Added metadata columns to improve data lineage and auditing.
Validated Bronze tables by comparing them with the original source views.
4. Blockers / Risks
Blocker	Impact	Help Needed
Incorrect file paths during initial ingestion	Data could not be loaded	Verified Unity Catalog volume paths and corrected file locations
Error while creating persistent views from temporary views	Bronze view creation failed	Used temporary Bronze views before creating Delta tables
5. Evidence Added to GitHub
Week04_Bronze_Ingestion notebook updated.
Bronze layer SQL queries added.
Screenshots of Bronze table validation added.
Metadata implementation documented.
Delta table verification (DESCRIBE DETAIL) included.
6. AI Transparency Note
Question	Response
Where AI helped	AI assisted in understanding the Bronze layer workflow, Databricks SQL syntax, Delta Lake concepts, metadata columns, and troubleshooting ingestion issues.
What we changed after AI suggestion	Updated file paths, selected the correct Spark readers for each file type, added metadata columns (ingestion_time, load_date, source_file), and validated the Bronze tables against the original datasets.
What we verified manually	Verified row counts, compared sample records between source views and Bronze tables, confirmed metadata columns, and checked that all tables were stored in Delta format.
What we can explain without AI	We can explain the complete Bronze layer implementation, Spark DataFrames, temporary views, Delta tables, metadata columns, validation process, and the role of the Bronze layer in the Medallion Architecture.
7. Next Week Preparation
Implement the Silver Layer.
Perform data cleaning and transformation.
Remove duplicate records.
Handle null values.
Convert data types where necessary.
Create Silver Delta tables.
Validate cleaned datasets before moving to the Gold layer.
Before submitting, replace these placeholders:
Date Range → Use the dates your instructor expects.
Team → Your actual team name or number.
Project → Your exact project title if it differs from "QuickBite – Food Delivery Data Engineering Pipeline".

This version is professional, accurately reflects the work you completed, and is suitable for uploading as your Week 4 sprint log.
