# M01: Advanced RAG Engineering

## Overview

Deep dive into building production-quality RAG systems that go beyond basic retrieval. This module covers domain-specific system design, hybrid search strategies, and citation enforcement patterns that are essential for trustworthy AI applications.

## Prerequisites

- B08: Introduction to RAG (beginner track)
- Familiarity with vector databases and embedding models
- Working knowledge of Python and LLM APIs

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Domain-Specific RAG Systems | Yes | Domain-specific chunking, specialized embedding selection, "Ask My Doc" systems |
| L02 | Hybrid Search Implementation | Yes | BM25 + vector search fusion, reciprocal rank fusion, retrieval quality optimization |
| L03 | Production RAG with Citation Enforcement | Yes | Citation generation pipelines, evidence grounding, trust metrics, fallback handling |

## Key Tools

- LangChain / LlamaIndex
- ChromaDB, Pinecone, or Weaviate
- BM25 (rank_bm25 or Elasticsearch)
- Sentence Transformers / embedding APIs
- Python evaluation scripts

## Learning Outcomes

- Build domain-specific RAG systems tailored to legal, healthcare, or technical documentation use cases
- Implement and tune hybrid search combining BM25 and dense vector retrieval
- Enforce strict citation grounding in generated responses with fallback handling
- Measure and optimize retrieval quality using precision, recall, and MRR metrics
