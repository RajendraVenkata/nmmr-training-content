# BM25 & Dense Retrieval Deep Dive

## Overview

Deep dive into the internals of BM25 keyword search and dense vector retrieval with bi-encoders, understanding trade-offs and when each approach excels.

## Topics Covered

- BM25 algorithm internals (term frequency, inverse document frequency)
- Dense retrieval with bi-encoders and embedding similarity
- Trade-offs between sparse (BM25) and dense (vector) methods
- When each approach excels for different query types

## Lab: BM25 vs Dense Retrieval Benchmarking

Implement both BM25 and dense retrieval on a test corpus and benchmark recall, precision, and latency across different query types.

### Lab Objectives

- Implement BM25 search on a document corpus
- Implement dense vector retrieval with a bi-encoder model
- Benchmark recall, precision, and latency for both approaches
- Analyze which approach wins for different query patterns

## Key Takeaways

- BM25 excels at exact term matching; dense retrieval excels at semantic understanding
- Neither approach is universally better - the right choice depends on query patterns
- Understanding both deeply is essential for designing optimal hybrid retrieval systems
