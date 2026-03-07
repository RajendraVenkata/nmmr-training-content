# Level 2 — Intermediate: Multi-Agent Systems & Production Patterns

## Overview

The Intermediate level takes you from building single agents to orchestrating complex multi-agent systems. You'll learn graph-based workflows (LangGraph), human-in-the-loop patterns, advanced RAG, memory systems, and how to test and evaluate agents rigorously.

**Duration**: 5-6 weeks (self-paced)
**Prerequisites**: Completed Beginner level (or equivalent experience)
**Cost**: $0 for local development; ~$2-5 if you want to test on Claude/OpenAI

---

## What You'll Learn

By the end of this level, you will:

- Design and implement various agent architecture patterns
- Build complex workflows with LangGraph (conditional branching, loops, parallel execution)
- Implement human-in-the-loop approval workflows
- Build advanced RAG with hybrid search, re-ranking, and self-correction
- Orchestrate multi-agent crews with CrewAI
- Implement persistent memory systems for agents
- Guarantee structured outputs from LLMs using Pydantic and Instructor
- Build complex tool integrations (databases, APIs, web scraping, code execution)
- Test and evaluate agents systematically

---

## What You'll Build

| Module | Project |
|--------|---------|
| I1 | Agent architecture pattern library |
| I2 | Research → Write → Review pipeline (LangGraph) |
| I3 | Expense approval agent with HITL gates |
| I4 | Advanced RAG with hybrid search + re-ranking |
| I5 | Content creation crew (CrewAI multi-agent) |
| I6 | Agent with persistent long-term memory |
| I7 | Structured data extraction agent |
| I8 | Customer support agent with DB + email tools |
| I9 | Automated agent test suite |
| **I10** | **Capstone: AI-Powered Customer Support System** |

---

## Lab Environment

Intermediate labs build on the Beginner environment and add:

- ChromaDB and PostgreSQL (pgvector) for vector storage
- Redis for caching and message queuing
- SQLite databases with sample data
- Mock API servers for tool integration testing
- LangSmith-compatible tracing

```bash
# Start an intermediate lab
lab start intermediate/I02-langgraph-workflows
```

---

## Modules

### Module I1: Deep Dive into Agent Architectures
**Duration**: 5-6 hours | **Lab**: Architecture patterns

Move beyond the simple ReAct loop. Learn specialized architecture patterns — Router agents that dispatch to specialists, Planner-Executor patterns for complex tasks, Critic agents that review and improve output, and how to choose the right pattern for each use case.

**Key Topics**:
- Router pattern — Classify intent, dispatch to specialist
- Planner-Executor pattern — Plan steps, execute sequentially
- Critic pattern — Generate → Review → Refine
- Reflection pattern — Agent evaluates its own output
- State management across agent calls
- Error handling and recovery strategies
- Observability and debugging

**Lab Project**: Implement each architecture pattern with Ollama, compare their behavior on the same set of tasks.

---

### Module I2: LangGraph — Graph-Based Agent Workflows
**Duration**: 6-8 hours | **Lab**: Multi-step workflow

LangGraph is where agentic AI gets powerful. Model your agent workflows as directed graphs with conditional branching, loops, and parallel execution. Build workflows that can't be expressed as simple chains.

**Key Topics**:
- Nodes, edges, and state in LangGraph
- `StateGraph` and `TypedDict` state schemas
- Conditional edges for dynamic routing
- Cycles — agents that iterate until a condition is met
- Parallel node execution
- Subgraphs — Composing complex workflows
- Checkpointing and persistence

**Lab Project**: Build a research agent workflow — Plan research → Gather information (parallel web searches) → Write draft → Review → Revise (loop until quality threshold met) → Output final result.

---

### Module I3: Human-in-the-Loop Agents
**Duration**: 4-5 hours | **Lab**: Approval workflow

Real-world agents need human oversight. Learn to build interrupt points where agents pause, present their proposed action to a human, and wait for approval before continuing. Essential for any business-critical agent deployment.

**Key Topics**:
- Why HITL — Regulatory compliance, trust, safety
- LangGraph interrupt mechanism
- Checkpoint-based pause and resume
- Approval patterns — Approve, reject, modify
- Escalation — When to hand off entirely to humans
- Audit trail design — Logging every decision
- Timeout handling — What happens if no human responds

**Lab Project**: Build an expense report processing agent — Extracts data from receipts → Validates against policy → Requests manager approval for items over $500 → Submits approved expenses.

---

### Module I4: Advanced RAG Patterns
**Duration**: 6-8 hours | **Lab**: Advanced RAG pipeline

Basic RAG has limitations — wrong chunks retrieved, no answer validation, poor handling of complex queries. Learn advanced patterns that dramatically improve RAG quality: hybrid search, re-ranking, multi-query expansion, and self-corrective RAG.

**Key Topics**:
- Semantic chunking (vs fixed-size)
- Parent-child chunk relationships
- Hybrid search — Vector (semantic) + BM25 (keyword)
- Cross-encoder re-ranking for better relevance
- Multi-query RAG — LLM generates multiple search perspectives
- Self-corrective RAG — Agent evaluates if retrieval was sufficient
- RAG evaluation metrics — Faithfulness, relevance, coverage
- Handling tables, images, and structured data in RAG

**Lab Project**: Build an advanced RAG system over a technical documentation set — Hybrid search with re-ranking, multi-query expansion, and a self-correction loop that re-retrieves if the first attempt wasn't relevant enough.

---

### Module I5: Multi-Agent Systems with CrewAI
**Duration**: 5-6 hours | **Lab**: Content creation crew

Build systems where multiple specialized agents collaborate. CrewAI makes it easy to define agent roles, assign tasks, and orchestrate their execution in sequential or hierarchical workflows.

**Key Topics**:
- CrewAI concepts — Agents, Tasks, Crews, Processes
- Role-based agent design
- Task dependencies and handoffs
- Sequential vs Hierarchical process flows
- Memory sharing between crew members
- CrewAI with Ollama (local execution)
- Crew debugging and optimization

**Lab Project**: Build a content creation crew — Researcher agent gathers information → Writer agent creates article → Editor agent reviews for quality and accuracy → Publisher agent formats and outputs.

---

### Module I6: Memory Systems for Agents
**Duration**: 5-6 hours | **Lab**: Long-term memory agent

Give your agents the ability to remember — both within a conversation and across sessions. Learn different memory types and how to implement persistent, searchable memory that makes agents contextually aware over time.

**Key Topics**:
- Short-term memory — Conversation buffers and sliding windows
- Summary memory — Compressing long conversations
- Long-term memory — Persistent storage in vector databases
- Entity memory — Tracking facts about people, places, concepts
- Episodic memory — Recalling past interactions and outcomes
- Memory injection strategies — When and what to recall
- Memory management — Updating, forgetting, consolidating

**Lab Project**: Build a personal assistant agent with persistent memory — Remembers user preferences, past conversations, and facts about their work. Uses ChromaDB for long-term storage.

---

### Module I7: Structured Outputs & Reliable Agent Responses
**Duration**: 4-5 hours | **Lab**: Data extraction agent

LLMs don't always produce well-formatted output. Learn techniques to guarantee structured, validated responses — critical for agents that feed data into downstream systems.

**Key Topics**:
- The reliability problem — Why raw LLM output breaks pipelines
- Pydantic models for output schemas
- Instructor library — Constrained decoding / retry-based validation
- LangChain output parsers
- Self-correction — LLM fixes its own malformed output
- Guardrails frameworks — Input/output validation
- Handling validation failures gracefully

**Lab Project**: Build a data extraction agent that processes unstructured job listings and outputs perfectly structured JSON with validated fields (title, company, salary range, requirements, location).

---

### Module I8: Agent Tools — Building Complex Integrations
**Duration**: 6-8 hours | **Lab**: Customer support agent

Real-world agents need real-world tools. Learn to build robust tool integrations for databases, REST APIs, web scraping, file operations, and sandboxed code execution.

**Key Topics**:
- Tool design principles — Clear names, good descriptions, proper schemas
- Database tools — Natural language to SQL
- REST API tools — CRUD operations via agent
- Web scraping tools — Playwright-based browser automation
- File system tools — Read, write, transform documents
- Code execution tools — Secure Python sandboxing (E2B)
- Tool composition — Chaining tools for complex operations
- Error handling, retries, and timeout management

**Lab Project**: Build a customer support agent with integrated tools — Order lookup (database), ticket creation (API), email sending (SMTP), and knowledge base search (RAG). The agent routes between tools based on the customer's question.

---

### Module I9: Agent Evaluation & Testing
**Duration**: 5-6 hours | **Lab**: Test suite development

Agents are non-deterministic — testing them requires different approaches than traditional software. Learn unit testing for tools, integration testing for workflows, LLM-as-judge evaluation, and regression testing to catch behavior changes.

**Key Topics**:
- Why agent testing is different — Non-determinism, tool side effects
- Unit testing individual tools
- Integration testing agent workflows with mock tools
- LLM-as-judge — Using a model to grade agent outputs
- Golden dataset evaluation — Testing against known-good answers
- Regression testing — Detecting behavior drift
- A/B testing agent variants
- LangSmith for tracing, evaluation, and comparison

**Lab Project**: Build a comprehensive test suite for the customer support agent from I8 — Unit tests for each tool, integration tests for the workflow, LLM-as-judge evaluation for response quality, and a regression test set.

---

### Module I10: Intermediate Capstone Project
**Duration**: 10-15 hours | **Lab**: Full project build

Build a complete AI-Powered Customer Support System that demonstrates mastery of all intermediate concepts:

**System Architecture**:
```
Customer Message
      ↓
[Triage Agent] → Classify intent
      ↓
┌─────┼──────────┐
↓     ↓          ↓
[FAQ] [Order]  [Complaint]    ← Specialist Agents
Agent  Agent    Agent
  ↓     ↓          ↓
  └─────┼──────────┘
        ↓
[Response Agent] → Format + send
        ↓
[Escalation?] → Human review (if needed)
```

**Features**:
- Multi-agent crew with role-based specialists (Triage, FAQ, Order, Complaint, Response)
- LangGraph workflow with conditional routing based on intent
- RAG knowledge base for FAQ answers
- Database tools for order lookup and ticket management
- Human-in-the-loop for refund approvals over $100
- Persistent memory for returning customer context
- Structured output for CRM ticket creation
- Full test suite with LLM-as-judge evaluation

**Deliverables**:
- Docker Compose setup with all services
- Working multi-agent system
- Test suite with >80% coverage
- Performance evaluation report

---

## Next Steps

After completing the Intermediate level, you're ready for **Level 3 — Advanced**, where you'll deploy production-grade agentic systems on the cloud with scalable, secure, observable architectures.

---

*NMMR Technologies — Agentic AI Training Program | Intermediate Level*
