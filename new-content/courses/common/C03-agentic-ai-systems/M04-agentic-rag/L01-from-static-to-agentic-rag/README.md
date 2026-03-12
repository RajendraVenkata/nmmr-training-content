# L01: From Static RAG to Agentic RAG

## Overview

This lesson examines the limitations of traditional static RAG pipelines and introduces agentic RAG as the next evolution. You will learn how agentic RAG systems autonomously formulate queries, evaluate retrieval quality, and self-correct when results are insufficient.

## Topics Covered

- Limitations of static RAG pipelines
- How agentic RAG extends traditional RAG systems
- Autonomous query formulation as an agent capability
- Self-critique of retrieval results
- The shift from fixed pipelines to adaptive retrieval loops
- Use cases where agentic RAG outperforms static RAG

## Key Takeaways

- Static RAG pipelines use a fixed retrieve-then-generate flow that cannot adapt when initial retrieval returns poor results
- Agentic RAG wraps the retrieval process in an agent loop that can reformulate queries, switch retrieval strategies, and iterate until quality is sufficient
- Autonomous query formulation allows the agent to generate optimized search queries rather than relying on raw user input
- Self-critique enables the agent to evaluate whether retrieved context actually answers the question before generating a response
- Agentic RAG is most valuable for complex, multi-faceted questions where a single retrieval pass is unlikely to surface all relevant information
