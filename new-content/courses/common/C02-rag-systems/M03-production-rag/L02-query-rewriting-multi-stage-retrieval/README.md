# L02: Query Rewriting & Multi-Stage Retrieval

## Overview

This lesson addresses the challenge of handling complex, ambiguous, or multi-part user queries in RAG systems. You will learn how to decompose queries, expand them for better recall, and implement multi-hop retrieval that iteratively refines results.

## Topics Covered

- Why raw user queries often fail to retrieve the best documents
- Query decomposition: breaking complex questions into simpler sub-queries
- Query expansion: adding related terms and synonyms to improve recall
- Multi-hop retrieval: using initial results to inform subsequent retrieval rounds
- Iterative refinement: re-querying based on partial answers
- HyDE (Hypothetical Document Embeddings) for query transformation
- Balancing query rewriting cost and latency with retrieval quality improvements

## Key Takeaways

- User queries are often vague, ambiguous, or multi-faceted, making direct retrieval suboptimal
- Query decomposition transforms a complex question into targeted sub-queries that each retrieve focused evidence
- Multi-hop retrieval allows the system to answer questions that require combining information from multiple documents
- Query rewriting adds latency and cost, so it should be applied selectively based on query complexity
