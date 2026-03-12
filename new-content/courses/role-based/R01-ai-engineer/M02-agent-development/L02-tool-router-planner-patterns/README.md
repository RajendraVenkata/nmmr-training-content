# L02: Tool Router & Planner Patterns

## Overview

Learn how to design intelligent tool routing systems and planner patterns that efficiently direct user requests to the right tools. This lesson covers both LLM-based and classifier-based routing approaches to minimize latency while maintaining accuracy.

## Topics Covered

- Designing tool routers for multi-tool agent systems
- NLP classifiers for high-speed routing decisions
- Planner patterns for decomposing complex tasks
- Reducing latency through routing optimization
- Comparing LLM-based vs. classifier-based routing trade-offs

## Lab: Implementing a Tool Router with Both LLM and Classifier-Based Routing

Build a tool routing system that supports both LLM-based routing (for complex queries) and classifier-based routing (for fast, common queries), with automatic fallback between the two approaches.

### Lab Objectives

- Train a lightweight NLP classifier for high-speed tool routing on common query types
- Implement LLM-based routing for complex or ambiguous queries
- Build a hybrid router that selects the routing method based on query complexity
- Benchmark latency and accuracy differences between routing approaches

## Key Takeaways

- Classifier-based routing can reduce latency by 10-50x compared to LLM-based routing for common patterns
- Planner patterns decompose complex requests into a sequence of tool calls before execution
- Hybrid routing (classifier for common cases, LLM for edge cases) provides the best latency-accuracy balance
- Tool routing accuracy directly impacts the user experience and should be monitored in production
