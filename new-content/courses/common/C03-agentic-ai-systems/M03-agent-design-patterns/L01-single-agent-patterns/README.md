# L01: Single Agent Patterns (Reactive & Planning)

## Overview

This lesson examines the two fundamental single-agent design patterns: reactive agents that respond immediately to inputs and planning agents that decompose problems into multi-step strategies. You will learn when each pattern is appropriate and the trade-offs involved in choosing between them.

## Topics Covered

- Reactive agent pattern and immediate response behavior
- Planning agent pattern and multi-step reasoning
- When to use reactive vs planning agents
- Latency vs capability trade-offs
- Hybrid approaches combining reactive and planning behaviors
- Pattern selection criteria for production systems

## Key Takeaways

- Reactive agents process each input independently and respond immediately, making them ideal for low-latency, well-defined tasks
- Planning agents invest upfront reasoning to decompose complex problems into ordered sub-tasks before executing
- Reactive agents are simpler to build and debug but struggle with tasks requiring multi-step coordination
- Planning agents handle complex workflows but introduce latency and higher token costs from extended reasoning
- Production systems often use hybrid approaches where a reactive layer handles simple requests and escalates complex ones to a planning layer
