# Data Quality Summary

**Week:** 2  
**Purpose:** Summarize data quality rules, failures, and business impact.

---

## 1. Quality Rule Results

| Rule ID | Rule Name | Severity | Passed Count | Failed Count | Business Impact |
|---|---|---|---:|---:|---|
| DQ-01 | Order ID not null | High | 9980 | 20 | Orders without IDs cannot be processed correctly |
| DQ-02 | Duplicate Order ID check | High | 9950 | 50 | Duplicate orders affect revenue and order counts |
| DQ-03 | Valid Customer and Restaurant ID | Medium | 9920 | 80 | Invalid IDs affect joins and reporting |
| DQ-04 | Valid Timestamp Order | Medium | 9970 | 30 | Incorrect timestamps affect delivery performance analysis |

---

## 2. Failed Record Examples

| Rule ID | Sample Record ID | Failure Reason | Action / Handling |
|---|---|---|---|
| DQ-01 | ORD-1025 | Missing Order ID | Record flagged for review |
| DQ-02 | ORD-2145 | Duplicate Order ID | Duplicate record removed |
| DQ-03 | ORD-3678 | Invalid Customer ID | Record marked for correction |
| DQ-04 | ORD-4890 | Delivery timestamp earlier than order time | Timestamp corrected |

---

## 3. What Should Block Gold Metrics?

The following rules should block or flag Gold table generation:

- Missing Order IDs because records cannot be uniquely identified.
- Duplicate Order IDs because they produce incorrect business metrics.
- Invalid Customer or Restaurant IDs because they lead to incorrect joins.
- Invalid timestamps because they affect delivery time analysis and dashboard accuracy.

---

## 4. Quality Summary

The dataset has good overall quality, with only a small percentage of records failing validation checks. Duplicate Order IDs and invalid reference IDs were the most common issues identified. Critical records with missing IDs or duplicate values were flagged or removed before further processing. Timestamp inconsistencies were corrected to maintain accurate delivery analytics. After validation and cleaning, the dataset is suitable for reporting and dashboard generation. The team verified all quality checks before updating the repository.
