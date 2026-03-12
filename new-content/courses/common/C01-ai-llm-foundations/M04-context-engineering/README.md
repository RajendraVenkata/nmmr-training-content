# M04: Context Engineering

## Overview

This module covers the discipline of context engineering -- designing and managing everything a model sees to produce optimal outputs. Moving beyond simple prompt engineering, you will learn to craft system instructions, manage retrieved documents and tool outputs within context budgets, and build multi-stage context flows for agentic workflows.

## Prerequisites

- Completion of M02 (understanding of tokens and context windows)
- Completion of M03 (experience calling LLM APIs)
- Familiarity with basic prompt writing

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | From Prompt Engineering to Context Engineering | No | Evolution beyond prompts, context as a system, full context management |
| L02 | System Instructions Design | No | System prompts, role definition, constraints, output formatting |
| L03 | Managing Retrieved Documents & Tool Outputs | No | Injecting retrieved context, tool output formatting, context budgets |
| L04 | Multi-Stage Context Flows in Agentic Workflows | Yes | Context propagation, state management, context pruning strategies |

## Key Tools

- LLM provider APIs (OpenAI, Anthropic)
- Token counting utilities (tiktoken)
- Context window visualization tools
- Prompt management libraries

## Learning Outcomes

- Articulate the shift from prompt engineering to context engineering and why it matters
- Design system instructions that consistently produce high-quality, well-formatted outputs
- Manage context window budgets when combining instructions, retrieved documents, and tool outputs
- Implement context pruning strategies that preserve the most relevant information
- Build multi-stage context pipelines that maintain coherence across agentic workflow steps
- Apply context engineering principles to improve output quality in production AI systems
