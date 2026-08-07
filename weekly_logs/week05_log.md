# Week 05 Log — Silver Candidate Layer Transformation

**Week:** 5  
**Date range:** 03 August 2026 – 07 August 2026  
**Team:** Team 03  
**Project:** QuickBite – Food Delivery Operations Analytics

---

## 1. Sprint Goal

The goal of Week 5 was to implement the Silver Candidate Layer of the QuickBite data pipeline in Databricks. The team focused on reading Bronze Delta tables, performing data standardization, converting required columns to appropriate data types, creating business-oriented calculated columns, storing the transformed data as Silver Candidate Delta tables, validating the transformation results, and updating the project documentation.

---

## 2. Work Completed

| Task | Owner | Status | Evidence |
|------|-------|--------|----------|
| Read Bronze Orders table into Spark DataFrame | Team 03 | Done | `Week05_Silver_Candidate_Transformation` Notebook |
| Read Bronze Restaurants table into Spark DataFrame | Team 03 | Done | `Week05_Silver_Candidate_Transformation` Notebook |
| Read Bronze Riders table into Spark DataFrame | Team 03 | Done | `Week05_Silver_Candidate_Transformation` Notebook |
| Read Bronze Refunds table into Spark DataFrame | Team 03 | Done | `Week05_Silver_Candidate_Transformation` Notebook |
| Standardized string columns using `trim()`, `upper()`, and `initcap()` | Team 03 | Done | Transformation Notebook |
| Converted required columns to Date, Timestamp, and Double data types | Team 03 | Done | Transformation Notebook |
| Created business-oriented calculated columns | Team 03 | Done | Transformation Notebook |
| Created Silver Candidate Delta tables | Team 03 | Done | Databricks Catalog |
| Validated Silver Candidate tables using row count comparison | Team 03 | Done | SQL Query Results |
| Updated Week 05 documentation and notebook | Team 03 | Done | GitHub Repository |

---

## 3. Key Decisions

- Used Bronze Delta tables as the source for all Silver transformations.
- Standardized text columns using `trim()`, `upper()`, and `initcap()` to improve data consistency.
- Converted only the columns that required type changes instead of recasting all columns.
- Created calculated columns to support business reporting and analytics.
- Stored all transformed datasets as Silver Candidate Delta tables.
- Validated Silver Candidate tables by comparing row counts with Bronze tables.

---

## 4. Transformations Performed

### Orders

**Standardization**
- city
- delivery_zone
- final_status
- payment_method
- payment_status
- required_vehicle_category
- time_band
- source_system

**Type Conversion**
- No additional type conversion was required because the important timestamp and numeric columns were already stored with appropriate data types.

**Calculated Columns**
- delivery_time_minutes
- gross_order_value_inr
- total_charges

---

### Restaurants

**Standardization**
- city
- cuisine_primary
- delivery_zone
- restaurant_name
- service_status
- zone_group

**Type Conversion**
- opened_date → Date
- record_updated_at → Timestamp

**Calculated Columns**
- restaurant_age_days

---

### Riders

**Standardization**
- home_city
- service_zone
- zone_group
- vehicle_type
- service_status
- shift_type

**Type Conversion**
- max_service_radius_km → Double
- onboarding_date → Date
- record_updated_at → Timestamp

**Calculated Columns**
- experience_days

---

### Refunds

**Standardization**
- refund_reason
- refund_status
- refund_channel
- source_system

**Type Conversion**
- refund_requested_ts → Timestamp
- refund_approved_ts → Timestamp
- refund_amount_inr → Double

**Calculated Columns**
- refund_processing_minutes

---

## 5. Blockers / Risks

| Blocker | Impact | Resolution |
|---------|--------|------------|
| String columns required conversion before calculations | Business calculations could not be performed | Converted required columns to Date, Timestamp, and Double |
| Inconsistent text values due to extra spaces and mixed case | Reduced reporting consistency | Standardized values using `trim()`, `upper()`, and `initcap()` |
| Need to preserve all records during transformation | Risk of data loss | Validated Silver row counts against Bronze tables |

---

## 6. Evidence Added to GitHub

- Updated `weekly_logs/week05_log.md`
- Updated `Week05_Silver_Candidate_Transformation` notebook
- Added Silver Candidate transformation scripts
- Added calculated column implementation
- Added validation SQL queries and screenshots
- Updated Evidence Tracker

---

## 7. AI Transparency Note

| Question | Response |
|----------|----------|
| Where AI helped | AI helped explain the Silver Layer workflow, data standardization, data type conversion, calculated columns, Delta Lake implementation, and Spark SQL transformations. |
| What we changed after AI suggestion | The team standardized textual data, converted required data types, implemented calculated columns, and validated the Silver Candidate tables. |
| What we verified manually | Data transformations, calculated columns, row counts, Silver Candidate table creation, and validation results were manually verified before updating GitHub. |
| What we can explain without AI | We can explain the Silver Layer implementation, data standardization, type conversion, calculated columns, validation process, Delta tables, and the role of the Silver Layer in the Medallion Architecture. |

---

## 8. Next Week Preparation

- Begin implementation of the Silver Approved Layer.
- Perform data quality validation.
- Handle duplicate and invalid records.
- Validate business rules.
- Create final Silver Delta tables.
- Prepare datasets for the Gold Layer.
- Continue updating project documentation and GitHub repository.
