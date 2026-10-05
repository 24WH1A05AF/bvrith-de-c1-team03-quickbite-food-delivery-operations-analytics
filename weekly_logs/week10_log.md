# Week 10 Log — Streaming Simulation and Validation

**Week:** 10  
**Date range:** 5 October 2026 – 11 October 2026  
**Team:** Team 03  
**Project:** QuickBite – Food Delivery Operations Analytics

---

## 1. Sprint Goal

Demonstrate incremental QuickBite order-event processing using Spark
Structured Streaming and Auto Loader. Build and validate the Streaming
Bronze → Silver → Gold flow using controlled event drops and document the
results with execution evidence.

---

## 2. Work Completed

| Task | Owner | Status | Evidence |
|---|---|---|---|
| Created QuickBite streaming JSON event source | Team 03 | Done | `07_streaming_simulation.ipynb` |
| Configured Auto Loader for incremental ingestion | Team 03 | Done | `week10_01_streaming_incremental.png` |
| Processed multiple event drops using checkpoint-based processing | Team 03 | Done | `week10_01_streaming_incremental.png` |
| Created Streaming Bronze and Silver layers | Team 03 | Done | `07_streaming_simulation.ipynb` |
| Created Streaming Gold order-status and KPI outputs | Team 03 | Done | `week10_02_streaming_gold.png` |
| Performed streaming data-quality validation | Team 03 | Done | `week10_03_streaming_validation.png` |
| Documented streaming architecture and event contract | Team 03 | Done | `streaming/` |

---

## 3. Key Decisions

- Used Spark Structured Streaming with Auto Loader for incremental JSON
  ingestion.
- Used a dedicated checkpoint path to maintain streaming progress.
- Maintained a separate Streaming Bronze → Silver → Gold flow from the
  existing batch reporting layer.
- Used the supported `availableNow` execution approach in the Databricks
  environment.
- Kept the existing Power BI dashboard unchanged during Week 10.
- Used actual QuickBite execution results for streaming validation.

---

## 4. Blockers / Risks

| Blocker | Impact | Help Needed |
|---|---|---|
| Initial streaming volume path was unavailable in Unity Catalog | Streaming source could not be created at the intended location | Resolved by using the existing QuickBite volume with a dedicated streaming-events folder |
| `input_file_name()` was not supported in the Unity Catalog environment | Initial Bronze metadata logic failed | Resolved by using Auto Loader `_metadata.file_path` |
| Continuous `processingTime` trigger was unsupported on the cluster | Continuous trigger could not be used | Resolved using the supported `availableNow` execution approach |

**Final Status:** No unresolved blocker remained after the streaming pipeline was validated.

---

## 5. Evidence Added to GitHub
- '/Workspace/Users/24wh1a6610@bvrithyderabad.edu.in/Quickbite/QuickBite_Week10_Live_Streaming'
- 'week10_01_streaming_incremental.png'
- 'week10_02_streaming_gold.png'

---

## 6. AI Transparency Note

| Question | Response |
|---|---|
| Where AI helped | AI helped us understand Structured Streaming, Auto Loader, checkpointing, Bronze/Silver/Gold streaming design, troubleshooting and Week-10 documentation requirements. |
| What we changed after AI suggestion | We adapted the suggestions to the actual QuickBite volume paths, table names, event structure and supported Databricks execution mode. |
| What we verified manually | We manually verified the event drops, Auto Loader execution, checkpoint path, Bronze and Silver outputs, Streaming Gold tables, KPI results and validation queries. |
| What we can explain without AI | We can explain the complete QuickBite streaming flow, incremental event processing, checkpoint role, Bronze/Silver/Gold layers, Streaming Gold KPIs and validation process. |

---

## 7. Next Week Preparation

- Preserve the validated QuickBite streaming pipeline and evidence.
- Review the batch and streaming flows together.
- Identify and resolve any remaining integration or consistency issues.
- Prepare the complete QuickBite pipeline for final review and demonstration.
