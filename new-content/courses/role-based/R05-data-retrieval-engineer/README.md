# R05: Data & Retrieval Engineer Specialization

## Overview

Builds the data foundation that makes retrieval-heavy AI systems possible. This course covers managing unstructured data pipelines, implementing hybrid search, and engineering robust retrieval systems at scale.

## Prerequisites

- Beginner course track (B01-B10) completed
- Intermediate course track (I01-I03) completed
- B08: Introduction to RAG fundamentals
- Proficiency in Python and SQL
- Familiarity with data pipeline concepts and ETL workflows

## Target Role

Data & Retrieval Engineers design and maintain the data infrastructure that powers AI retrieval systems. They build ETL pipelines for unstructured data, implement and optimize search algorithms (sparse and dense), design chunking and indexing strategies, and ensure corpus quality at scale. This role requires expertise in both traditional data engineering and modern vector search technologies.

## Modules

| Module | Name | Lessons | Key Topics |
|--------|------|---------|------------|
| M01 | Modern Data Stack for AI | 3 | ETL orchestration, data lineage & quality, unstructured data pipelines |
| M02 | Retrieval Engineering | 4 | BM25 & dense retrieval, vector indexing, chunking policies, deduplication & corpus quality |

## Key Tools & Technologies

- Apache Airflow for pipeline orchestration
- DBT for data transformations
- Elasticsearch / BM25 search engines
- Vector databases (Pinecone, Weaviate, Qdrant, Milvus)
- FAISS for vector indexing research
- Sentence Transformers / embedding models
- Document parsers (PyMuPDF, Unstructured, Tika)
- Python data processing libraries (Pandas, Polars)

## Learning Outcomes

- Design and implement ETL pipelines for AI data ingestion using Airflow and DBT
- Establish data lineage tracking and quality constraints for AI training and retrieval data
- Build scalable pipelines for processing unstructured documents (PDFs, HTML, images)
- Implement and benchmark BM25 and dense retrieval methods with trade-off analysis
- Configure and tune vector indexing strategies (HNSW, IVF, PQ) for optimal recall and latency
- Design document chunking policies that preserve context, metadata, and document structure
- Implement deduplication and corpus quality scoring to maintain high-quality retrieval corpora
