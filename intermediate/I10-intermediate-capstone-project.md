# Course I10: Intermediate Capstone Project

> **Build a complete AI-Powered Customer Support System** — A multi-agent crew with RAG knowledge base, database tools, human-in-the-loop approvals, full LangGraph workflow, and comprehensive testing.

### Goal: Build a production-ready multi-agent customer support system demonstrating all intermediate skills

---

## I10.1 Project: AI-Powered Customer Support System (Lab)
- Project overview — A complete customer support system powered by multiple AI agents
- Architecture design — Multi-agent crew with LangGraph orchestration
- Agent: Triage Agent — Classifies incoming requests by type and urgency
- Agent: Specialist Agent — Answers product/service questions using RAG knowledge base
- Agent: Escalation Agent — Handles complex cases and routes to human support
- Feature: RAG knowledge base — Company docs, FAQs, product manuals in ChromaDB
- Feature: Database tools — Order lookup, ticket creation, status updates
- Feature: Human-in-the-loop — Approval gates for refund processing and account changes
- Feature: Customer memory — Remembering returning customers and their history
- Feature: Structured outputs — Validated responses with Pydantic models
- Workflow: LangGraph graph — Conditional routing based on triage classification
- Workflow: Sequential processing — Triage → Route → Resolve → Respond
- Workflow: Escalation path — Auto-escalation on low confidence or customer request
- Testing: Unit tests — Tool and component testing with pytest
- Testing: Integration tests — End-to-end workflow testing with mocked LLMs
- Testing: LLM-as-judge — Automated quality evaluation of agent responses
- Technology stack — Python, LangChain, LangGraph, CrewAI, ChromaDB, Ollama, Docker
- Docker setup — Multi-service Docker Compose with all components
- Provider abstraction — Runs on Ollama locally, swappable to Claude/OpenAI
- Step-by-step build — Guided walkthrough building each component
- Stretch goals — Web UI, analytics dashboard, multi-language support
