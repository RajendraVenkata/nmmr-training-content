# Course I3: Human-in-the-Loop Agents

> **Build agents that know when to ask for help** — Implement interrupt patterns, approval workflows, escalation logic, and audit trails using LangGraph checkpoints.

### Goal: Build agents with human oversight, approval gates, and escalation capabilities

---

## I3.1 Why HITL — Trust, Safety, and Compliance
- The autonomy spectrum — Fully autonomous vs fully supervised vs hybrid
- Trust building — Humans need to verify before trusting agents with critical tasks
- Safety requirements — Destructive actions need human approval
- Compliance — Regulatory requirements for human oversight (finance, healthcare, legal)
- Liability — Who is responsible when an autonomous agent makes a mistake
- The right level of autonomy — Task criticality determines how much human involvement

## I3.2 Interrupt Patterns — Pause Agent, Get Approval, Resume (Lab)
- What is an interrupt — Pausing agent execution to wait for human input
- LangGraph interrupts — `interrupt()` function to pause at any node
- Interrupt before — Pausing before a critical action is executed
- Interrupt after — Pausing after a decision is made, before proceeding
- Resuming execution — `Command(resume=...)` to continue with human input
- Timeout handling — What happens when humans don't respond in time
- Multiple interrupt points — Several approval gates in one workflow

## I3.3 Implementing HITL with LangGraph Checkpoints (Lab)
- What are checkpoints — Saved snapshots of graph state at each step
- Checkpoint storage — In-memory, SQLite, PostgreSQL backends
- `MemorySaver` — Simple in-memory checkpointer for development
- `SqliteSaver` — Persistent checkpoints for production
- Thread management — Each conversation gets its own checkpoint thread
- Replaying from checkpoints — Resuming interrupted workflows
- State inspection — Viewing checkpoint state for debugging

## I3.4 Approval Workflows — Agent Proposes, Human Approves (Lab)
- The propose-approve pattern — Agent suggests an action, human confirms
- Designing approval nodes — Clear presentation of what the agent wants to do
- Approval with modifications — Human can approve, reject, or modify the proposal
- Batch approvals — Reviewing multiple agent proposals at once
- Conditional approval — Auto-approve low-risk actions, require approval for high-risk
- Approval UI patterns — CLI prompts, web dashboards, Slack integrations
- Audit trail — Recording who approved what and when

## I3.5 Escalation — When Agents Should Hand Off to Humans
- Defining escalation triggers — Low confidence, out-of-scope, high-risk, customer request
- Confidence-based escalation — Agent measures its own certainty
- Complexity-based escalation — Tasks that exceed agent capabilities
- Sentiment-based escalation — Detecting frustrated or upset users
- Graceful handoff — Providing context to the human agent
- Hybrid resolution — Human and AI working together on escalated cases
- Escalation metrics — Tracking escalation rates and reasons

## I3.6 Audit Trails and Logging Agent Decisions
- Why audit trails — Accountability, debugging, compliance, improvement
- What to log — Every decision, tool call, human interaction, and outcome
- Structured logging — JSON-formatted logs with timestamps, agent IDs, action types
- Immutable audit logs — Append-only storage for compliance
- Log analysis — Finding patterns in agent behavior and failures
- Retention policies — How long to keep logs, data privacy considerations
- Reporting — Dashboards and reports for stakeholders
