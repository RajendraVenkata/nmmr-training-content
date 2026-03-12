# M04: Agentic RAG

## Overview

This module extends traditional RAG systems with agentic capabilities, transforming static retrieve-and-generate pipelines into autonomous systems that formulate their own queries, critique their own results, and iteratively refine retrieval until quality thresholds are met. You will build a production-ready agentic RAG system from the ground up.

## Prerequisites

- Completion of C02 (RAG Systems) or equivalent RAG experience
- Completion of M01-M03 in this course (agent foundations, orchestration, design patterns)
- Experience with vector stores and embedding models
- Understanding of retrieval evaluation metrics

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | From Static RAG to Agentic RAG | No | Limitations of static RAG, how agentic RAG extends traditional systems, autonomous query formulation, self-critique |
| L02 | Autonomous Query Formulation | No | Agent-driven query generation, query decomposition, multi-query strategies, iterative query refinement |
| L03 | Recursive Retrieval & Self-Critique | Yes | Iterating on retrieval, observing irrelevant results, refining queries, recursive loops, quality gates |
| L04 | Building a Production Agentic RAG System | Yes | End-to-end architecture, combining all components, production considerations, error handling |

## Key Tools

- LangGraph or LlamaIndex Workflows (orchestration layer)
- ChromaDB / Pinecone (vector stores)
- Sentence Transformers (embedding models)
- Ragas (evaluation framework)
- OpenAI / Anthropic SDKs (LLM providers)

## Learning Outcomes

- Explain the limitations of static RAG and how agentic RAG overcomes them
- Design agent-driven query formulation strategies including decomposition and multi-query approaches
- Implement recursive retrieval loops with self-critique and quality gates
- Build a complete production-ready agentic RAG system with error handling and monitoring
- Evaluate agentic RAG systems using faithfulness, relevance, and groundedness metrics
- Apply production hardening techniques including fallback strategies, caching, and cost controls
