# L04: Cross-Encoder Reranking

## Overview

This lesson introduces cross-encoder reranking as a second-stage retrieval step that dramatically improves precision. You will learn how cross-encoders differ from bi-encoders, how they score query-document pairs jointly, and how to integrate reranking into your RAG pipeline.

## Topics Covered

- What cross-encoders do and how they differ from bi-encoders
- Query-document pair scoring: joint attention over the full input
- Why cross-encoders are more accurate but too slow for first-stage retrieval
- Two-stage retrieval: fast retrieval followed by precise reranking
- Using Cohere Rerank API for production reranking
- Open-source cross-encoder models from Sentence Transformers
- Setting the reranking cutoff: how many candidates to rerank

## Lab: Adding a Cross-Encoder Reranker to Improve Retrieval Precision

Add a cross-encoder reranking step to an existing retrieval pipeline. Retrieve a broad set of candidates using hybrid search, then rerank them with a cross-encoder to surface the most relevant documents.

### Lab Objectives

- Integrate a cross-encoder model into an existing retrieval pipeline as a reranking step
- Configure the candidate pool size and reranking cutoff for optimal precision-latency balance
- Compare retrieval precision before and after reranking on a set of test queries
- Evaluate the latency trade-off of adding a reranking step to the pipeline

## Key Takeaways

- Cross-encoders process query-document pairs jointly, achieving higher accuracy than bi-encoder similarity search
- Reranking is used as a second stage because cross-encoders are too computationally expensive for full-corpus search
- A typical two-stage pipeline retrieves 50-100 candidates with fast search, then reranks the top results with a cross-encoder
- Adding reranking consistently improves precision and is one of the highest-impact optimizations for RAG quality
