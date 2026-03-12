# C02: RAG Systems - Design to Production

## Overview

This course provides a comprehensive journey through Retrieval-Augmented Generation (RAG), from foundational architecture concepts to production-ready implementations. Across three modules, you will learn how to build, optimize, and evaluate RAG pipelines that ground LLM responses in your own data.

## Prerequisites

- Working knowledge of Python programming
- Basic understanding of LLMs and prompt engineering
- Familiarity with APIs and JSON data formats
- Completion of foundational LLM coursework (or equivalent experience)

## Modules

| Module | Name | Lessons | Key Topics |
|--------|------|---------|------------|
| M01 | RAG Foundations | 4 | RAG architecture, document loading, chunking strategies, embeddings and vector storage |
| M02 | Retrieval Techniques | 4 | BM25 keyword search, dense vector retrieval, hybrid retrieval, cross-encoder reranking |
| M03 | Production RAG | 4 | Citation enforcement, query rewriting, vector database management, RAG evaluation with Ragas |

## Key Tools & Technologies

- Python 3.10+
- LlamaIndex / LlamaHub data loaders
- ChromaDB, Pinecone, Weaviate, PGvector
- Sentence Transformers / embedding models
- BM25 (rank-bm25)
- Cross-encoder reranking models (Cohere, sentence-transformers)
- Ragas evaluation framework
- LangChain (optional integration)

## Learning Outcomes

- Explain the RAG architecture and articulate why RAG is preferred over fine-tuning for knowledge-grounded applications
- Build end-to-end document ingestion pipelines that load, chunk, embed, and store documents
- Implement and compare keyword, semantic, and hybrid retrieval strategies
- Apply cross-encoder reranking to improve retrieval precision
- Enforce citation grounding and prevent hallucinations in RAG outputs
- Select and manage production vector databases based on scaling requirements
- Evaluate RAG systems using the Ragas framework with faithfulness, relevance, and groundedness metrics
