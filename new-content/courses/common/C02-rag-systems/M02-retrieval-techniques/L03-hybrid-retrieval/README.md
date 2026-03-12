# L03: Hybrid Retrieval (BM25 + Vector)

## Overview

This lesson teaches you how to combine keyword-based BM25 search with dense vector retrieval to get the best of both approaches. You will learn fusion strategies that merge ranked results from multiple retrievers into a single, higher-quality result set.

## Topics Covered

- Why hybrid retrieval outperforms either approach alone
- Combining BM25 keyword scores with vector similarity scores
- Fusion strategies: linear combination, reciprocal rank fusion (RRF), and weighted fusion
- Reciprocal Rank Fusion in detail: how RRF merges ranked lists without score normalization
- Tuning the balance between keyword and semantic retrieval
- When to use hybrid retrieval versus a single retrieval method

## Lab: Implementing Hybrid Retrieval Combining BM25 and Vector Search

Build a hybrid retrieval pipeline that runs BM25 keyword search and dense vector search in parallel, then merges the results using Reciprocal Rank Fusion to produce a unified ranked list.

### Lab Objectives

- Implement BM25 search over a document corpus using the rank-bm25 library
- Implement dense vector search over the same corpus using ChromaDB
- Combine results from both retrievers using Reciprocal Rank Fusion
- Compare retrieval quality of BM25-only, vector-only, and hybrid approaches on a set of test queries

## Key Takeaways

- Hybrid retrieval captures both exact keyword matches and semantic relationships, covering more query types
- Reciprocal Rank Fusion is a simple, effective method for merging ranked lists without requiring score normalization
- The optimal balance between keyword and semantic components depends on the domain and query distribution
- Hybrid retrieval is the recommended default for production RAG systems due to its robustness across query types
