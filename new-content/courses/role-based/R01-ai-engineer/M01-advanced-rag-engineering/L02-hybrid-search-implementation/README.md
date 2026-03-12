# L02: Hybrid Search Implementation

## Overview

Explore how to combine BM25 keyword search with dense vector retrieval to build hybrid search systems that outperform either approach alone. This lesson covers reciprocal rank fusion tuning and retrieval quality benchmarking.

## Topics Covered

- Production BM25 + vector search fusion architectures
- Reciprocal rank fusion (RRF) algorithm and tuning
- Retrieval quality optimization and benchmarking
- When to favor keyword search vs. semantic search
- Scaling hybrid search for production workloads

## Lab: Implementing and Tuning Hybrid Search with Quality Benchmarks

Implement a hybrid search system that combines BM25 and vector search, tune the fusion parameters using reciprocal rank fusion, and benchmark retrieval quality against single-method baselines.

### Lab Objectives

- Set up a BM25 index alongside a vector store for the same corpus
- Implement reciprocal rank fusion to merge results from both retrieval methods
- Tune fusion parameters (k-value, score weighting) to maximize retrieval quality
- Build a benchmark suite comparing hybrid vs. keyword-only vs. vector-only retrieval

## Key Takeaways

- Hybrid search consistently outperforms pure keyword or pure vector search across most benchmarks
- Reciprocal rank fusion provides a simple yet effective method for combining ranked result lists
- The optimal fusion parameters depend on the corpus and query distribution; tuning is essential
- BM25 excels at exact term matching while vector search handles semantic similarity and paraphrasing
