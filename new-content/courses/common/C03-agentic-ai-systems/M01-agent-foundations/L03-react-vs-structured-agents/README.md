# L03: ReAct vs Structured Agents

## Overview

This lesson contrasts first-generation ReAct agents with second-generation structured agents, explaining why the industry shifted toward more constrained architectures. You will understand the failure modes of unbounded reasoning loops and how structured agents with defined execution flows address these challenges.

## Topics Covered

- First-generation ReAct agents and the Reason-Act paradigm
- Failure modes of ReAct: unbounded solution spaces and reasoning loops
- Second-generation structured agents and their design philosophy
- Defined execution flows and constrained action spaces
- Model function calling as the backbone of structured agents
- When to choose ReAct vs structured approaches

## Key Takeaways

- ReAct agents interleave reasoning and action steps, giving the LLM freedom to determine the next step at each iteration
- Unbounded solution spaces in ReAct agents lead to hallucination-driven actions, infinite loops, and unpredictable costs
- Structured agents constrain the execution flow to predefined paths, making behavior more predictable and reliable
- Model function calling provides a structured interface between the LLM and available tools, reducing ambiguity
- The industry trend is moving toward structured agents for production systems, reserving ReAct-style flexibility for exploratory or research contexts
