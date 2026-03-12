# L04: Bounded Autonomy & Guardrails

## Overview

This lesson addresses the critical challenge of keeping autonomous agents safe and predictable. You will learn how to prevent hallucination-driven actions, enforce resource limits, make execution paths explainable, and implement human-in-the-loop checkpoints for high-stakes decisions.

## Topics Covered

- Preventing hallucination-driven actions in autonomous agents
- Resource limits: token budgets, API call caps, and time bounds
- Execution path explainability and audit trails
- Human-in-the-loop for high-stakes decisions
- Gating sensitive operations with approval workflows
- Designing fail-safe defaults and graceful degradation

## Lab: Adding Guardrails and Human-in-the-Loop to an Autonomous Agent

Extend an autonomous agent with guardrails that enforce resource limits, gate sensitive operations behind human approval, and provide clear execution traces for every decision the agent makes.

### Lab Objectives

- Implement token budget and API call limits that halt execution when exceeded
- Add classification logic that identifies high-stakes actions requiring human approval
- Build a human-in-the-loop checkpoint that pauses agent execution and presents the proposed action for review
- Create execution trace logs that capture the reasoning chain for every agent decision
- Test guardrails by simulating scenarios where the agent attempts actions beyond its authorized scope

## Key Takeaways

- Unbounded agent autonomy is a liability in production; every agent needs explicit limits on what it can do and how much it can spend
- Resource limits (token budgets, API call caps, time bounds) prevent runaway costs and infinite loops
- Human-in-the-loop checkpoints are essential for high-stakes operations such as financial transactions, data deletion, or external communications
- Execution path explainability enables auditing, debugging, and building trust with stakeholders
- Well-designed guardrails do not reduce agent capability; they focus agent autonomy on the domain where it adds value
