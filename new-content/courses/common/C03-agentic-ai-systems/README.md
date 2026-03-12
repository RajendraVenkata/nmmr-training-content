# C03: Agentic AI Systems

## Overview

This course provides a comprehensive exploration of agentic AI systems, covering agent architecture, orchestration frameworks, design patterns, and agentic RAG. You will progress from understanding core agent components to building production-ready autonomous systems with guardrails and multi-agent coordination.

## Prerequisites

- Working knowledge of Python programming
- Understanding of LLMs, prompt engineering, and function calling
- Familiarity with RAG concepts (completion of C02 or equivalent experience)
- Experience making API calls to LLM providers

## Modules

| Module | Name | Lessons | Key Topics |
|--------|------|---------|------------|
| M01 | Agent Foundations | 4 | AI agents vs chatbots, core components (router, skills, memory), ReAct vs structured agents, tool calling and structured outputs |
| M02 | Orchestration Frameworks | 4 | LangGraph graph-based orchestration, LlamaIndex event-driven workflows, smolagents code-first agents, multi-agent frameworks (CrewAI, AutoGen) |
| M03 | Agent Design Patterns | 4 | Single agent patterns, multi-agent patterns, memory management, bounded autonomy and guardrails |
| M04 | Agentic RAG | 4 | Static vs agentic RAG, autonomous query formulation, recursive retrieval and self-critique, production agentic RAG systems |

## Key Tools & Technologies

- **Languages**: Python 3.10+
- **Orchestration**: LangGraph, LlamaIndex Workflows, smolagents, CrewAI, AutoGen
- **LLM Providers**: OpenAI, Anthropic, Groq
- **Validation**: Pydantic for structured output validation
- **Vector Stores**: ChromaDB, Pinecone (for agentic RAG)
- **Utilities**: LangChain, LangSmith (tracing and debugging)

## Learning Outcomes

- Distinguish AI agents from chatbots and explain the perception-reasoning-planning-action cycle
- Design agent architectures using routers, skills, and shared memory components
- Compare ReAct and structured agent paradigms and select the appropriate approach for a given use case
- Implement reliable tool calling with JSON schema enforcement and Pydantic validation
- Build agent workflows using LangGraph, LlamaIndex Workflows, and smolagents
- Orchestrate multi-agent systems with specialized roles using CrewAI and AutoGen
- Apply single-agent and multi-agent design patterns for production reliability
- Implement episodic and semantic memory strategies for conversational agents
- Add guardrails, resource limits, and human-in-the-loop checkpoints to autonomous agents
- Build production-ready agentic RAG systems with autonomous query formulation and recursive retrieval
