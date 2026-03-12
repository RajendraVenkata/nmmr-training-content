# M01: Agent Foundations

## Overview

This module establishes the foundational concepts of agentic AI systems. You will learn what distinguishes AI agents from simple chatbots, explore the core architectural components that make agents work, compare first-generation and second-generation agent paradigms, and implement reliable tool calling with structured outputs.

## Prerequisites

- Understanding of LLMs and how they generate text
- Experience with LLM API calls and function calling basics
- Python programming proficiency
- Familiarity with JSON schemas and data validation

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | What is an AI Agent - Beyond Chatbots | No | Defining AI agents vs chatbots, autonomy, perception-reasoning-planning-action cycle, reactive vs planning agents |
| L02 | Core Components - Router, Skills, Memory | No | Router as decision-making hub, skills/execution branches, memory and shared state, execution logs |
| L03 | ReAct vs Structured Agents | No | First-generation ReAct agents, unbounded solution spaces, second-generation structured agents, model function calling |
| L04 | Tool Calling & Structured Outputs | Yes | Function calling implementation, JSON output schema enforcement, Pydantic validation, retry mechanisms |

## Key Tools

- Python 3.10+
- OpenAI / Anthropic SDKs (function calling)
- Pydantic for schema validation
- JSON Schema for output enforcement

## Learning Outcomes

- Define what an AI agent is and explain how it differs from a chatbot
- Describe the perception-reasoning-planning-action cycle that drives agent behavior
- Identify and explain the roles of routers, skills, and memory in agent architecture
- Compare ReAct agents with structured agents and articulate the trade-offs of each approach
- Implement reliable tool calling with JSON schema enforcement and Pydantic-validated outputs
- Build retry mechanisms to handle malformed LLM outputs gracefully
