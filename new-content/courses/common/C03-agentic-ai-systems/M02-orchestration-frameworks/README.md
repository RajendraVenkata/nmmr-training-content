# M02: Orchestration Frameworks

## Overview

This module surveys the major agent orchestration frameworks, each offering a distinct approach to building and managing AI agents. You will gain hands-on experience with LangGraph's graph-based orchestration, LlamaIndex's event-driven workflows, smolagents' code-first paradigm, and multi-agent coordination using CrewAI and AutoGen.

## Prerequisites

- Completion of M01 (Agent Foundations) or equivalent understanding of agent architecture
- Python programming proficiency including async/await patterns
- Experience with LLM API calls and function calling
- Familiarity with Pydantic for data validation

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | LangGraph - Graph-Based Orchestration | Yes | Nodes and edges, conditional edges, cyclic logic, state management, granular execution control |
| L02 | LlamaIndex Workflows - Event-Driven Agents | Yes | Steps and events, asynchronous-first design, event broadcasting, retry events, non-linear workflows |
| L03 | smolagents - Code-First Agents | Yes | Code agents vs JSON tool calls, executing Python code blocks, expressiveness, Hugging Face integration |
| L04 | Multi-Agent Frameworks (CrewAI, AutoGen) | Yes | Specialized agent groups, manager-worker delegation, CrewAI roles, AutoGen patterns, Swarms |

## Key Tools

- LangGraph (LangChain ecosystem)
- LlamaIndex Workflows
- smolagents (Hugging Face)
- CrewAI
- AutoGen (Microsoft)
- LangSmith (tracing and debugging)

## Learning Outcomes

- Build stateful agent workflows using LangGraph with conditional branching and cyclic logic
- Design event-driven agent systems using LlamaIndex Workflows with async-first architecture
- Implement code-first agents using smolagents that write and execute Python for complex operations
- Orchestrate multi-agent systems with CrewAI using specialized roles and delegation patterns
- Compare orchestration frameworks and select the appropriate one based on use case requirements
- Debug and trace agent execution flows using observability tools
