# Module I3: Human-in-the-Loop Agents

## Duration: 4-5 hours | Lab: Approval workflow

## Learning Objectives
- Understand why human oversight is essential for production agents
- Implement interrupt/resume patterns with LangGraph checkpoints
- Build approval workflows where agents propose and humans decide
- Design escalation paths for when agents reach their limits
- Create audit trails logging every agent decision

## Topics

### I3.1 Why HITL — Trust, Safety, and Compliance
- Agents make mistakes — Humans catch them before damage
- Regulatory requirements (finance, healthcare, legal)
- Building user trust incrementally
- The spectrum: Fully autonomous → Human-supervised → Human-directed

### I3.2 Interrupt Patterns — Pause Agent, Get Approval, Resume
- LangGraph's `interrupt_before` and `interrupt_after`
- Pausing execution at specific nodes
- Serializing state to persistent storage
- Resuming with human input added to state

### I3.3 Implementing HITL with LangGraph Checkpoints
- Checkpoint backends: Memory, SQLite, PostgreSQL
- Saving graph state at interrupt points
- Loading and resuming from checkpoints
- Thread management — Multiple concurrent HITL workflows

### I3.4 Approval Workflows — Agent Proposes, Human Approves
- Pattern: Agent generates action → Presents to human → Human approves/rejects/modifies
- Displaying agent reasoning alongside proposed action
- Handling rejection — Agent re-plans with feedback
- Handling modification — Agent continues with adjusted parameters

### I3.5 Escalation — When Agents Should Hand Off to Humans
- Confidence thresholds — Low confidence = escalate
- High-stakes actions — Always require approval
- Repeated failures — Escalate after N retries
- Unrecognized intents — Pass to human for handling
- Designing clear escalation policies

### I3.6 Audit Trails and Logging Agent Decisions
- Why audit trails matter (compliance, debugging, improvement)
- What to log: Inputs, reasoning, tool calls, decisions, outputs
- Structured audit log format
- Immutable logging (append-only)
- Using audit logs to improve agent behavior over time

### I3.7 Lab: Build an Expense Approval Agent
- Agent extracts data from receipts (RAG + extraction)
- Validates against company policy (rules engine tool)
- Auto-approves expenses under $500
- Requests manager approval for expenses over $500
- Logs every decision in an audit trail

## Lab Exercises
1. Build a simple LangGraph workflow with an interrupt point
2. Implement checkpoint persistence with SQLite
3. Resume a graph after adding human approval to state
4. Build the expense approval workflow with conditional HITL gates
5. Add rejection handling — Agent re-processes with manager feedback
6. Implement audit logging — Log every decision to a structured JSON file

## Key Takeaways
- Human-in-the-loop is not optional for production agents — It's a core pattern
- LangGraph checkpoints make interrupt/resume seamless and reliable
- Design clear policies for when agents should escalate to humans
- Audit trails protect both users and developers — Log everything
- Start with more human oversight, reduce as trust is established

---
*Next: [Module I4 — Advanced RAG Patterns →](I04-advanced-rag.md)*
