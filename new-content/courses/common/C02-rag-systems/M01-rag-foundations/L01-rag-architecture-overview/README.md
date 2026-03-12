# L01: RAG Architecture Overview

## Overview

This lesson introduces Retrieval-Augmented Generation as an architectural pattern for grounding LLM responses in external knowledge. You will learn why RAG has become the dominant approach for enterprise AI applications and walk through each stage of the RAG pipeline.

## Topics Covered

- What is Retrieval-Augmented Generation (RAG)
- Why RAG over fine-tuning: cost, freshness, and control advantages
- The 5 stages of a RAG pipeline: Loading, Indexing, Storing, Querying, Evaluation
- How retrieval grounds LLM responses and reduces hallucinations
- Enterprise use cases for RAG (knowledge bases, customer support, document Q&A, compliance)
- RAG system components and how they interact

## Key Takeaways

- RAG augments LLMs with external knowledge at query time, avoiding the cost and rigidity of fine-tuning
- The five-stage pipeline (Load, Index, Store, Query, Evaluate) provides a structured framework for building RAG systems
- RAG is preferred when data changes frequently, when source attribution is required, or when domain-specific accuracy is critical
- Enterprise adoption of RAG spans industries including healthcare, finance, legal, and customer service
