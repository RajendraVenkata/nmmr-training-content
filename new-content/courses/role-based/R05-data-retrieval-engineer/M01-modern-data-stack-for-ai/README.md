# M01: Modern Data Stack for AI

## Overview

Covers the data engineering foundations required to feed AI systems with clean, reliable data. This module addresses ETL orchestration, data lineage and quality, and the unique challenges of building pipelines for unstructured data formats commonly used in AI applications.

## Prerequisites

- R05 course prerequisites (B01-B10, I01-I03 completed)
- Working knowledge of Python and SQL
- Basic understanding of data pipeline concepts
- Familiarity with command-line tools and scripting

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | ETL Orchestration with Airflow & DBT | Yes | Airflow DAGs, DBT transformations, pipeline scheduling, data freshness |
| L02 | Data Lineage & Quality Constraints | No | Lineage tracking, validation rules, quality monitoring over time |
| L03 | Unstructured Data Pipelines | No | PDF/HTML/image processing, document normalization, metadata extraction, pipeline scalability |

## Key Tools

- Apache Airflow
- DBT (Data Build Tool)
- Great Expectations or Soda for data quality
- Document parsers (PyMuPDF, Unstructured, Apache Tika)
- Python data processing libraries

## Learning Outcomes

- Build ETL pipelines with Airflow DAGs for scheduling and orchestrating AI data ingestion
- Apply DBT transformations to prepare data for AI consumption
- Implement data lineage tracking to trace data from source to model input
- Establish quality constraints and validation rules that catch data issues before they reach models
- Design pipelines for processing unstructured formats including PDFs, HTML, and images at scale
