# L02: LlamaIndex Workflows - Event-Driven Agents

## Overview

This lesson covers LlamaIndex Workflows, an event-driven framework for building agent systems. You will learn how steps and events create flexible, asynchronous-first architectures that support non-linear execution, event broadcasting, and built-in retry mechanisms.

## Topics Covered

- Steps and events architecture in LlamaIndex Workflows
- Asynchronous-first design principles
- Event broadcasting and event listeners
- Retry events on failure for resilient execution
- Non-linear workflow patterns
- Comparing event-driven vs graph-based orchestration

## Lab: Creating an Event-Driven Agent with LlamaIndex Workflows

Create an agent using LlamaIndex Workflows that responds to events asynchronously, broadcasts results to multiple listeners, and handles failures through retry events without breaking the overall workflow.

### Lab Objectives

- Define workflow steps that respond to typed events
- Implement async event handlers for parallel processing
- Set up event broadcasting to trigger multiple downstream steps from a single event
- Add retry event logic that re-attempts failed steps with modified parameters
- Build a non-linear workflow where steps execute based on event availability rather than sequential order

## Key Takeaways

- LlamaIndex Workflows use an event-driven model where steps are triggered by events rather than explicit edges
- The async-first design enables concurrent execution of independent steps, improving throughput
- Event broadcasting allows a single result to trigger multiple downstream processes simultaneously
- Retry events provide built-in resilience by re-attempting failed steps without restarting the entire workflow
- Event-driven architectures excel when workflows have many independent branches or require high concurrency
