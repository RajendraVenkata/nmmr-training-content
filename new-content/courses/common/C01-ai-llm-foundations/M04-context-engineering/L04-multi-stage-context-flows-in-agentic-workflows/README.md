# L04: Multi-Stage Context Flows in Agentic Workflows

## Overview

This lesson tackles the challenge of managing context across multiple steps in agentic AI workflows. You will learn how to propagate relevant context between agent steps, manage state across turns, and apply pruning strategies that keep context focused and within budget as workflows grow in complexity.

## Topics Covered

- Context propagation across sequential agent steps
- State management: what to carry forward and what to discard
- Context pruning strategies: summarization, relevance scoring, recency weighting
- Scratchpad and working memory patterns for multi-step reasoning
- Context handoff between different agents in a multi-agent system
- Handling context window exhaustion in long-running workflows
- Debugging context issues in multi-stage pipelines

## Lab: Building a Multi-Stage Context Pipeline for an Agentic Workflow

Build a multi-step agentic workflow where each stage receives context from the previous stage, adds its own tool outputs, prunes less relevant information, and passes a refined context to the next stage -- demonstrating practical context flow management.

### Lab Objectives

- Implement a three-stage agentic pipeline with context propagation between stages
- Build a context manager that tracks token usage across stages
- Implement context pruning that summarizes older context to free up window space
- Add a scratchpad mechanism for maintaining key facts across stages
- Verify that the final stage has access to all critical information despite context pruning

## Key Takeaways

- Multi-stage workflows require explicit context management -- context does not manage itself
- Not all context from earlier stages is relevant to later stages; selective propagation is essential
- Summarization-based pruning preserves information density while freeing context window space
- Scratchpad patterns let agents maintain critical facts without carrying full conversation history
- Context flow debugging is a distinct skill that requires visibility into what each stage receives and produces
