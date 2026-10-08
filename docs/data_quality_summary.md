# QuickBite Data Quality Summary

## Purpose

Data Quality is the control point between transformation and business
reporting in the QuickBite pipeline.

The objective was not simply to remove bad records. The objective was to
identify contradictions, validate business relationships, refine incorrect
validation logic, and ensure that only trustworthy data reaches the Gold
layer.

```text
RAW DATA
   ↓
TRANSFORMATION
   ↓
DATA QUALITY GATE
   ↓
TRUSTED DATA
   ↓
GOLD METRICS
   ↓
POWER BI
