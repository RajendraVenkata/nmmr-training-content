# L02: Data Quality & Pipeline Management

## Overview

Learn how to build robust data quality pipelines and manage ML data infrastructure at scale. This lesson covers data quality constraints, pipeline orchestration, data lineage tracking, quality gates, and monitoring for data drift that can silently degrade model performance.

## Topics Covered

- Data quality constraints and validation frameworks
- Pipeline orchestration with Airflow or Prefect
- Data lineage tracking and provenance
- Quality gates for data pipelines
- Monitoring data drift and distribution shifts

## Key Takeaways

- Data quality issues are the most common cause of ML model degradation in production
- Automated data quality checks (schema validation, distribution checks, completeness) should run at every pipeline step
- Data lineage tracking enables root-cause analysis when model performance degrades
- Data drift detection must be continuous; point-in-time checks miss gradual distribution shifts
- Pipeline orchestration tools (Airflow, Prefect) provide the reliability and observability needed for production data workflows
