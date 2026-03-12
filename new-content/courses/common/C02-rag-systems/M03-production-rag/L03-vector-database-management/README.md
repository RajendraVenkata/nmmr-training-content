# L03: Vector Database Selection & Management

## Overview

This lesson provides a practical comparison of vector database options for production RAG deployments. You will learn how to evaluate Chroma, Pinecone, Weaviate, and PGvector on criteria including scalability, cost, managed vs self-hosted trade-offs, and index optimization.

## Topics Covered

- Comparing vector databases: ChromaDB, Pinecone, Weaviate, and PGvector
- Managed vs self-hosted: cost, operational complexity, and control trade-offs
- Scaling considerations: millions to billions of vectors
- Index types (HNSW, IVF, flat) and their performance characteristics
- Index management: building, updating, and rebuilding indexes
- Metadata filtering, namespaces, and multi-tenancy
- Backup, migration, and disaster recovery for vector data

## Lab: Deploying and Managing a Production Vector Database with Index Optimization

Set up a vector database for production use, load a significant document corpus, configure indexing for optimal query performance, and benchmark retrieval latency and recall under different configurations.

### Lab Objectives

- Deploy a vector database and configure it for a production-like workload
- Load a large document set and measure indexing time and storage requirements
- Experiment with index parameters (e.g., HNSW ef_construction, M values) and measure their impact on recall and latency
- Implement metadata filtering and verify its effect on query performance

## Key Takeaways

- There is no one-size-fits-all vector database; the right choice depends on scale, budget, operational capacity, and feature needs
- Pinecone offers a fully managed experience ideal for teams without infrastructure expertise, while PGvector integrates naturally with existing PostgreSQL deployments
- Index tuning (HNSW parameters, segment sizes) has a significant impact on the recall-latency trade-off
- Planning for index rebuilds, data migrations, and backup strategies is essential for production reliability
