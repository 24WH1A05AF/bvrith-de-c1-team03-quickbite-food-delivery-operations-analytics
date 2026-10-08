# QuickBite Pipeline Walkthrough

## Purpose

QuickBite is primarily a batch data engineering and analytics project.
The pipeline transforms operational food-delivery data into trusted,
business-ready Gold outputs for Power BI.

The main flow is:

SOURCE DATA → BRONZE → SILVER → DATA QUALITY → TRUSTED → GOLD → POWER BI

A separate Week 10 streaming extension was implemented for incremental
operational event processing.

---

## 1. End-to-End Batch Pipeline

```text
SOURCE DATA
     ↓
BRONZE
Raw Ingestion
     ↓
SILVER
Transformation
     ↓
DATA QUALITY
Validation
     ↓
TRUSTED DATA
Validated Records
     ↓
GOLD
Business Metrics
     ↓
POWER BI
Decision Support
