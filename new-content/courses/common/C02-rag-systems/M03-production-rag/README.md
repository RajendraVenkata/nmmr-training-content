# M03: Production RAG

## Overview

This module addresses the challenges of deploying RAG systems to production, covering citation enforcement for trust, query optimization for complex questions, vector database selection at scale, and systematic evaluation using the Ragas framework.

## Prerequisites

- Completion of M01: RAG Foundations and M02: Retrieval Techniques
- Working knowledge of hybrid retrieval and reranking pipelines
- Familiarity with vector databases (at minimum, ChromaDB from prior labs)

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Citation Enforcement & Trust | No | Grounding answers in evidence, citation generation, declining insufficient evidence, hallucination prevention |
| L02 | Query Rewriting & Multi-Stage Retrieval | No | Query decomposition, query expansion, multi-hop retrieval, iterative refinement |
| L03 | Vector Database Selection & Management | Yes | Comparing Chroma, Pinecone, Weaviate, PGvector; scaling; index management |
| L04 | RAG Evaluation with Ragas | Yes | Faithfulness, groundedness, answer relevance, context precision, evaluation pipelines |

## Key Tools

- Ragas evaluation framework
- ChromaDB, Pinecone, Weaviate, PGvector
- LLM APIs (for query rewriting and answer generation)
- Golden dataset creation tools

## Learning Outcomes

- Implement citation enforcement strategies that ground every claim in retrieved evidence
- Design query rewriting pipelines that decompose complex questions into retrievable sub-queries
- Evaluate and select vector databases based on scale, cost, managed vs self-hosted, and feature requirements
- Build and run a comprehensive RAG evaluation pipeline using Ragas metrics
- Diagnose and fix common production RAG failure modes using evaluation data
