# Course I1: Deep Dive into Agent Architectures

> **Master the design patterns behind powerful AI agents** — Learn Router, Planner, Executor, and Critic patterns, single vs multi-agent designs, communication strategies, state management, error recovery, and observability.

### Goal: Design and implement different agent architecture patterns for various use cases

---

## I1.1 Agent Design Patterns — Router, Planner, Executor, Critic
- The Router pattern — Classifying input and directing to the right specialist
- The Planner pattern — Breaking complex tasks into ordered sub-steps
- The Executor pattern — Carrying out planned steps using tools
- The Critic pattern — Reviewing and improving outputs before returning
- Combining patterns — Router → Planner → Executor → Critic pipeline
- Pattern selection — Matching the right pattern to your use case
- Trade-offs — Simplicity vs capability, latency vs quality

## I1.2 Single-Agent vs Multi-Agent Architectures
- Single-agent systems — One LLM handles everything, simpler but limited
- Multi-agent systems — Specialized agents collaborating on complex tasks
- When single-agent is enough — Straightforward tasks, limited tool set
- When to go multi-agent — Diverse expertise needed, parallel work, complex workflows
- Coordination overhead — The cost of multi-agent communication
- Hybrid approaches — A single orchestrator dispatching to specialist agents

## I1.3 Agent Communication Patterns — Sequential, Parallel, Hierarchical
- Sequential — Agents run one after another, output feeds into the next
- Parallel — Multiple agents work simultaneously on independent sub-tasks
- Hierarchical — A supervisor agent delegates to and coordinates worker agents
- Broadcast — One agent sends a message to all others
- Request-reply — Agent A asks Agent B a question and waits for a response
- Shared blackboard — Agents read and write to a shared state
- Choosing the right pattern — Task dependencies dictate communication design

## I1.4 State Management in Agentic Systems (Lab)
- What is agent state — The data that persists across steps in an agent loop
- Conversation state — Chat history, context window management
- Task state — Current step, completed steps, pending actions
- World state — External data the agent has gathered (tool results, retrieved docs)
- State serialization — Saving and loading agent state (JSON, Pydantic models)
- Checkpointing — Saving state at key points for recovery and replay
- State schemas — Defining typed state with TypedDict or Pydantic
- Shared state in multi-agent systems — How agents share and update common state

## I1.5 Error Handling and Recovery Strategies (Lab)
- Types of failures — LLM errors, tool failures, timeout, invalid output, hallucinations
- Retry with backoff — Exponential backoff for transient failures
- Self-correction — Agent detects its own error and retries with a different approach
- Fallback strategies — Alternative tools, simpler models, cached responses
- Circuit breakers — Stopping repeated failures before they cascade
- Human escalation — When to hand off to a human operator
- Graceful degradation — Providing a partial answer when full resolution fails
- Dead letter handling — Logging unrecoverable failures for later review

## I1.6 Agent Observability — Tracing and Debugging (Lab)
- Why observability matters — Agents are non-deterministic and hard to debug
- Logging agent decisions — Capturing thoughts, tool calls, and observations
- Tracing frameworks — LangSmith, LangFuse, OpenTelemetry for agents
- Trace anatomy — Spans for each agent step, parent-child relationships
- Debugging agent failures — Reading traces to find where things went wrong
- Cost tracking per trace — Knowing how much each agent run costs
- Replay and reproduce — Re-running a trace to reproduce issues
- Dashboard design — Key metrics for agent health and performance
