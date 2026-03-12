# L04: Debugging Agent Loops & Failures

## Overview

This lesson focuses on diagnosing and resolving the failure modes unique to AI agent systems. You will learn to identify common patterns like infinite loops, tool call failures, and context window exhaustion, and develop systematic approaches to debugging these issues using traces, spans, and structured logging.

## Topics Covered

- Common failure modes in agentic AI systems
- Infinite loops: detection, causes, and prevention strategies
- Tool call failures: timeouts, malformed arguments, permission errors
- Diagnosing issues using traces and spans from observability tools
- Building guardrails to prevent and recover from agent failures

## Key Takeaways

- Agents fail in ways that traditional software does not: they can enter infinite loops of reasoning, hallucinate tool names, or generate syntactically invalid tool arguments, requiring new debugging strategies
- Infinite loops in agents typically stem from the model repeatedly choosing the same action because it cannot make progress; max-iteration limits and loop detection are essential safeguards
- Tool call failures should be surfaced as structured spans in traces, capturing the tool name, arguments, error type, and retry count so that patterns can be identified across many requests
- Effective agent debugging requires combining trace inspection (what did the agent do?) with prompt analysis (why did it decide to do that?) to find root causes
- Proactive guardrails (iteration limits, token budgets, tool call validation) are more effective than reactive debugging; build them in from the start rather than adding them after failures occur
