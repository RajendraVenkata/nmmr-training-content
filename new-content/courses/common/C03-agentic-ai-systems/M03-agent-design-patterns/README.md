# M03: Agent Design Patterns

## Overview

This module covers the essential design patterns for building reliable and production-ready AI agents. You will learn single-agent and multi-agent architectural patterns, implement memory management strategies for maintaining context, and apply guardrails and human-in-the-loop mechanisms to ensure bounded autonomy.

## Prerequisites

- Completion of M01 (Agent Foundations) and M02 (Orchestration Frameworks)
- Experience building agent workflows with at least one orchestration framework
- Understanding of LLM context windows and token costs
- Familiarity with async programming patterns in Python

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Single Agent Patterns (Reactive & Planning) | No | Reactive agents, planning agents, pattern selection criteria, trade-offs |
| L02 | Multi-Agent Patterns (Leader-Worker, Parallel) | No | Leader-worker setups, hierarchical task decomposition, parallel execution, multi-agent ensembles |
| L03 | Memory Management (Episodic & Semantic) | Yes | Episodic memory, semantic memory, memory hierarchies, context window cost management |
| L04 | Bounded Autonomy & Guardrails | Yes | Hallucination prevention, resource limits, explainability, human-in-the-loop, gating sensitive operations |

## Key Tools

- LangGraph / LlamaIndex Workflows (for pattern implementation)
- Vector stores for semantic memory (ChromaDB)
- LangSmith for execution tracing
- Custom guardrail implementations

## Learning Outcomes

- Select between reactive and planning agent patterns based on task complexity and latency requirements
- Design multi-agent systems using leader-worker, parallel, and ensemble patterns
- Implement episodic memory to track past interactions and semantic memory for long-term context retrieval
- Manage context window costs through memory hierarchies and selective context loading
- Add guardrails that prevent hallucination-driven actions and enforce resource limits
- Implement human-in-the-loop checkpoints for high-stakes decisions and sensitive operations
