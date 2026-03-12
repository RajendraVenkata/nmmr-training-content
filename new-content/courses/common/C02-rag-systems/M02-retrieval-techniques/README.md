# M02: Retrieval Techniques

## Overview

This module covers the retrieval stage of the RAG pipeline in depth, progressing from keyword-based search through semantic vector retrieval to advanced hybrid and reranking approaches. You will learn how to select and combine retrieval strategies to maximize the relevance of documents returned to the LLM.

## Prerequisites

- Completion of M01: RAG Foundations (document loading, chunking, embeddings, vector storage)
- Understanding of vector similarity and embedding representations
- A working ChromaDB setup with stored embeddings from M01 labs

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | BM25 Keyword Search | No | How BM25 works, term frequency, inverse document frequency, when keyword search excels |
| L02 | Dense Vector Retrieval | No | Semantic search with embeddings, similarity metrics, advantages over keyword search |
| L03 | Hybrid Retrieval (BM25 + Vector) | Yes | Combining keyword and semantic search, fusion strategies, reciprocal rank fusion |
| L04 | Cross-Encoder Reranking | Yes | Cross-encoder scoring, query-document pair evaluation, Cohere reranker, precision improvement |

## Key Tools

- rank-bm25 (Python BM25 implementation)
- ChromaDB or other vector database for semantic search
- Sentence Transformers (bi-encoder and cross-encoder models)
- Cohere Rerank API
- Reciprocal Rank Fusion utilities

## Learning Outcomes

- Explain how BM25 keyword search works and identify scenarios where it outperforms semantic search
- Implement dense vector retrieval using embeddings and similarity metrics
- Combine BM25 and vector search into a hybrid retrieval pipeline using reciprocal rank fusion
- Apply cross-encoder reranking to a candidate set to improve retrieval precision
- Select the appropriate retrieval strategy based on query characteristics and data properties
