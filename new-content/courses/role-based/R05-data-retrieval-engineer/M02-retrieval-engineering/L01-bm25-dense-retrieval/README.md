# L01: BM25 & Dense Retrieval Deep Dive

## Overview

Understand the internals of both BM25 (sparse) and dense retrieval methods, their strengths and weaknesses, and when to use each approach. This lesson provides hands-on experience implementing and benchmarking both methods on a test corpus to build intuition for real-world retrieval system design.

## Topics Covered

- BM25 algorithm internals (term frequency, inverse document frequency, length normalization)
- Dense retrieval with bi-encoder models
- Trade-offs between sparse and dense retrieval methods
- When BM25 excels (exact keyword matching, known terminology)
- When dense retrieval excels (semantic similarity, paraphrasing)
- Hybrid retrieval as a practical default

## Lab: Implementing and Benchmarking BM25 vs Dense Retrieval

Implement both BM25 and dense retrieval on a test corpus, then run comparative benchmarks measuring precision, recall, and latency to understand when each method performs best.

### Lab Objectives

- Implement BM25 search using Elasticsearch or the rank_bm25 library
- Implement dense retrieval using a bi-encoder model and vector similarity search
- Design evaluation queries that highlight the strengths and weaknesses of each approach
- Benchmark both methods on precision, recall, MRR, and latency metrics

## Key Takeaways

- BM25 is highly effective for exact keyword matching and remains a strong baseline that is difficult to beat on many benchmarks
- Dense retrieval captures semantic similarity and handles paraphrasing, but may miss exact terms
- Hybrid approaches (combining BM25 and dense retrieval) often outperform either method alone
- The optimal retrieval strategy depends on the query distribution and corpus characteristics of the specific use case
