# M02: Retrieval Engineering

## Overview

Deep dive into the retrieval algorithms and infrastructure that power modern AI search systems. This module covers sparse and dense retrieval methods, vector indexing strategies, document chunking policies, and corpus quality management techniques essential for building high-performance retrieval pipelines.

## Prerequisites

- M01: Modern Data Stack for AI completed
- B08: Introduction to RAG fundamentals
- Understanding of embeddings and vector similarity
- Familiarity with search engine concepts

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | BM25 & Dense Retrieval Deep Dive | Yes | BM25 internals, bi-encoder dense retrieval, sparse vs dense trade-offs |
| L02 | Vector Indexing Strategies | Yes | HNSW, IVF, PQ indexing, recall-latency tuning, sharding |
| L03 | Document Normalization & Chunking Policies | Yes | Format standardization, chunking policy design, metadata preservation |
| L04 | Deduplication & Corpus Quality | No | Near-duplicate detection, quality scoring, corpus freshness |

## Key Tools

- Elasticsearch / OpenSearch for BM25
- FAISS for vector indexing research
- Pinecone, Weaviate, or Qdrant for production vector search
- Sentence Transformers for dense embeddings
- MinHash / SimHash for deduplication
- Custom Python evaluation scripts

## Learning Outcomes

- Implement and benchmark BM25 and dense retrieval methods with clear trade-off analysis
- Configure and tune vector indices (HNSW, IVF, PQ) for specific recall-latency requirements
- Design chunking policies that balance context preservation with retrieval granularity
- Build deduplication pipelines and corpus quality scoring systems for maintaining clean retrieval corpora
