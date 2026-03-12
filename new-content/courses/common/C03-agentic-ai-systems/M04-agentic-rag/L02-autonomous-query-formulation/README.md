# L02: Autonomous Query Formulation

## Overview

This lesson dives into how agentic RAG systems generate, decompose, and refine search queries autonomously. You will learn multi-query strategies that improve retrieval coverage, query decomposition techniques for complex questions, and iterative refinement approaches that adapt queries based on initial results.

## Topics Covered

- Agent-driven search query generation
- Query decomposition for complex multi-part questions
- Multi-query strategies for improved retrieval coverage
- Iterative query refinement based on retrieval feedback
- Query rewriting techniques (expansion, synonym substitution, abstraction)
- Balancing query specificity with recall

## Key Takeaways

- Agent-driven query generation transforms ambiguous user questions into precise, retrieval-optimized search queries
- Query decomposition breaks complex questions into independent sub-queries, each targeting a specific aspect of the information need
- Multi-query strategies generate multiple alternative queries for the same question, increasing the likelihood of retrieving all relevant documents
- Iterative refinement allows the agent to adjust queries based on what was (or was not) found in previous retrieval rounds
- The quality of query formulation directly determines retrieval quality, making it the highest-leverage improvement point in agentic RAG
