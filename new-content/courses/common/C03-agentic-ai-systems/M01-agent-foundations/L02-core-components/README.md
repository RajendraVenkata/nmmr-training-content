# L02: Core Components - Router, Skills, Memory

## Overview

This lesson examines the three core architectural components that make AI agents function: the Router (decision-making hub), Skills (execution branches), and Memory (shared state). You will learn how these components interact to enable autonomous agent behavior.

## Topics Covered

- The Router as the decision-making hub
- Router implementation approaches: LLM function calling, NLP classifiers, rule-based systems
- Skills and execution branches (SQL generators, RAG retrievers, API callers)
- Memory and shared state management
- Persisting context across agent interactions
- Execution logs and observability

## Key Takeaways

- The Router is the central decision-making component that determines which skill to invoke based on the current input and context
- Routers can be implemented using LLM function calling for flexibility, NLP classifiers for speed, or rule-based systems for determinism
- Skills are specialized execution branches that perform specific tasks such as database queries, document retrieval, or API calls
- Memory provides the shared state that enables agents to maintain context across multiple interactions and steps
- Execution logs are essential for debugging, auditing, and improving agent behavior over time
