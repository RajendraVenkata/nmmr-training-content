# L03: Recursive Retrieval & Self-Critique

## Overview

This lesson covers the recursive retrieval loop at the heart of agentic RAG, where the agent iterates on its own retrieval results, identifies gaps and irrelevant content, refines queries, and continues until quality gates are satisfied. You will implement a self-critiquing retrieval agent with built-in quality thresholds.

## Topics Covered

- Iterating on retrieval results to improve quality
- Observing and classifying irrelevant results
- Refining queries based on retrieval feedback
- Recursive retrieval loops and termination conditions
- Quality gates and relevance thresholds
- Preventing infinite retrieval loops with bounded iteration

## Lab: Building a Recursive Retrieval Agent with Self-Critique

Build a retrieval agent that evaluates its own results for relevance and completeness, refines its queries when results are insufficient, and iterates recursively until quality gates are met or iteration limits are reached.

### Lab Objectives

- Implement a retrieval step that returns results along with relevance scores
- Build a self-critique step where the agent evaluates whether retrieved content answers the original question
- Create query refinement logic that generates improved queries based on critique feedback
- Set up quality gates with configurable relevance thresholds
- Add bounded iteration with a maximum loop count to prevent runaway retrieval

## Key Takeaways

- Recursive retrieval transforms RAG from a single-pass pipeline into an iterative refinement process that converges on high-quality results
- Self-critique enables the agent to detect when retrieved context is irrelevant, incomplete, or contradictory before generating a response
- Quality gates define explicit thresholds that retrieved content must meet before the agent proceeds to generation
- Bounded iteration (maximum loop counts) is essential to prevent infinite retrieval cycles and control costs
- The combination of recursive retrieval and self-critique significantly improves answer quality for complex, knowledge-intensive questions
