# L01: LangGraph - Graph-Based Orchestration

## Overview

This lesson introduces LangGraph, a graph-based orchestration framework for building stateful agent workflows. You will learn how to define nodes and edges, implement conditional branching, handle cyclic logic, and manage state across complex multi-step agent interactions.

## Topics Covered

- Nodes and edges architecture in LangGraph
- Conditional edges for dynamic workflow routing
- Cyclic logic for iterative agent processes
- State management and state schemas
- Granular control over execution flow
- Checkpointing and persistence

## Lab: Building a Stateful Agent Workflow with LangGraph

Build a multi-step agent workflow using LangGraph that processes user requests through conditional branches, iterates when necessary using cyclic edges, and maintains state across the entire execution.

### Lab Objectives

- Define a LangGraph state schema with typed fields for agent context
- Create nodes that perform distinct agent actions (retrieval, reasoning, tool calling)
- Implement conditional edges that route execution based on intermediate results
- Add cyclic logic that allows the agent to retry or refine its approach
- Persist and inspect state at each step for debugging and observability

## Key Takeaways

- LangGraph models agent workflows as directed graphs where nodes represent actions and edges represent transitions
- Conditional edges enable dynamic routing based on runtime state, allowing agents to adapt their execution path
- Cyclic edges support iterative refinement loops where agents can re-evaluate and retry actions
- Explicit state management provides full visibility into what the agent knows and has done at every step
