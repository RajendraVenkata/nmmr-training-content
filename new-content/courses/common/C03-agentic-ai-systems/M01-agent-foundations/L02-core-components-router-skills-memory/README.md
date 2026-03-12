# Core Components - Router, Skills, Memory

## Overview

Understand the three primary components that make up every robust agentic system: the Router (decision-making hub), Skills/Execution Branches (the workers), and Memory/Shared State (persistent context).

## Topics Covered

- The Router: LLM function calling vs NLP classifiers vs rule-based routing
- Skills / Execution Branches: SQL generators, RAG retrievers, logic blocks
- Memory / Shared State: persisting context, execution logs, state hierarchy
- Production patterns for each component

## Key Takeaways

- Every agent consists of a Router, Skills, and Memory working together
- The Router can use LLM function calling for complex routing or classifiers for low-latency routing
- Memory management (what to persist vs discard) is critical for cost and context window control
