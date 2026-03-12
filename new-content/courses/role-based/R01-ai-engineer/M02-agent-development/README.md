# M02: Agent Development

## Overview

Master the design and implementation of production-grade AI agents using LangGraph. This module covers building agentic workflows with state machines, implementing intelligent tool routing and planner patterns, and adding persistent memory and state management.

## Prerequisites

- B05: Introduction to Agents (beginner track)
- B06: Tool Calling (beginner track)
- R01-M01: Advanced RAG Engineering
- Familiarity with LangChain and LangGraph basics

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Agentic Workflows with LangGraph | Yes | State machines, conditional routing, tool integration, error recovery |
| L02 | Tool Router & Planner Patterns | Yes | Tool routers, NLP classifiers, planner patterns, latency reduction |
| L03 | Memory & State Management | Yes | Agent memory systems, state persistence, context window optimization |

## Key Tools

- LangGraph
- LangChain
- Redis / PostgreSQL for state persistence
- NLP classifiers (scikit-learn, sentence-transformers)
- OpenAI / Anthropic APIs

## Learning Outcomes

- Build multi-step agentic workflows with conditional routing and error recovery using LangGraph
- Design tool routers using both LLM-based and classifier-based approaches for optimal latency
- Implement persistent memory systems with hierarchical memory architectures
- Manage agent state across conversation turns and sessions
