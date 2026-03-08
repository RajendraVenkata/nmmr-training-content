# NMMR Technologies — Agentic AI Training Program

## Complete Course Outline

> **Build Agentic AI Applications from Zero to Production**
>
> A hands-on training program with integrated Docker-based lab environments where every concept comes with a runnable container you can spin up instantly via the browser terminal (term.js).

---

## Program Structure

| Level | Duration | Prerequisites | What You'll Build |
|-------|----------|--------------|-------------------|
| **Beginner** | 4-5 weeks | Basic Python knowledge | Simple agents, tool-calling bots, RAG chatbots |
| **Intermediate** | 5-6 weeks | Completed Beginner level | Multi-agent systems, complex workflows, memory-enabled agents |
| **Advanced** | 6-8 weeks | Completed Intermediate level | Production-grade, cloud-deployed, scalable agentic systems |

---

## Lab Environment

Every module includes a **Docker-based hands-on lab** accessible via the browser terminal (term.js). The terminal has two display modes:

**Default View** — Terminal fixed at the bottom, training content scrolls above it:

```
┌─────────────────────────────────────────────┐
│  Browser (Training Website)                 │
│  ┌─────────────────────────────────────────┐│
│  │  Training Content (scrollable)          ││
│  │                                         ││
│  │  Module 3: Tool Calling                 ││
│  │  ...                                    ││
│  │  [Run Lab ▶]                           ││
│  │                              ▲ scroll ▲ ││
│  ├─────────────────────────────────────────┤│
│  │  term.js Terminal (fixed at bottom)     ││
│  │  $ ollama run llama3.1:8b               ││
│  │  $ python agent.py                      ││
│  │  > Using tool: calculator               ││
│  │  > Result: 42                           ││
│  └─────────────────────────────────────────┘│
└─────────────────────────────────────────────┘
```

**Popup View** — Terminal opens as a floating overlay via a button click:

```
┌─────────────────────────────────────────────┐
│  Browser (Training Website)                 │
│  ┌─────────────────────────────────────────┐│
│  │  Training Content (full height)         ││
│  │                                         ││
│  │  Module 3: Tool Calling                 ││
│  │  ...                                    ││
│  │                                         ││
│  │       ┌──────────────────────┐          ││
│  │       │  term.js Terminal    │  [x]     ││
│  │       │  (popup overlay)     │          ││
│  │       │  $ python agent.py   │          ││
│  │       │  > Result: 42        │          ││
│  │       └──────────────────────┘          ││
│  │                                         ││
│  │                           [Terminal ▶] ││
│  └─────────────────────────────────────────┘│
└─────────────────────────────────────────────┘
```

- **Docker-in-Docker (DinD)**: Each lab spins up isolated containers
- **Pre-built images**: All dependencies pre-installed — no setup time
- **Instant reset**: Restart any lab to a clean state
- **Persistent workspace**: Your code saves between sessions

---

## Complete Table of Contents

---

# LEVEL 1 — BEGINNER

---

### Course B1: Foundations of AI & Large Language Models
> A standalone introductory course (no coding required) — covers AI history, how LLMs work, the model landscape, open vs closed-source, safety & ethics, and the AI development stack. *(See `beginner/B1-foundations-of-ai-and-llms.md` for full details.)*

---

### Goal: Build your first working agents locally

---

### Course B2: Python for AI — Quick Refresher
> A fast-paced refresher covering core Python, REST APIs with `requests`, JSON handling, async programming with `asyncio`/`aiohttp`, and virtual environment setup. *(See `beginner/B2-python-for-ai.md` for full details.)*

### Course B3: LLM API Keys & Interaction Reference
> A hands-on reference guide with one lesson per provider (Anthropic, OpenAI, Google Gemini, Meta Llama, Mistral, Cohere, Ollama, AWS Bedrock, Azure OpenAI, Hugging Face) plus a comparison cheat sheet. *(See `beginner/B3-llm-api-keys-and-interaction-reference.md` for full details.)*

### Course B4: Prompt Engineering Fundamentals
> Master prompt design — system/user/assistant roles, zero-shot, few-shot, chain-of-thought, structured JSON output, prompt templates, and common pitfalls. *(See `beginner/B4-prompt-engineering-fundamentals.md` for full details.)*

### Course B5: Introduction to AI Agents
> Understand AI agents beyond chatbots — the ReAct pattern, agent components (LLM + Tools + Memory + Planning), agent types, and real-world use cases. *(See `beginner/B5-introduction-to-ai-agents.md` for full details.)*

### Course B6: Tool Calling — Giving Agents Abilities
> Teach LLMs to call external functions — JSON Schema tool definitions, tool calling with Ollama, building calculator and multi-tool agents, and error handling. *(See `beginner/B6-tool-calling.md` for full details.)*

### Course B7: Building Your First Agent with LangChain
> Build agents using LangChain — core concepts, LCEL chains, `@tool` decorator, ReAct agents with `create_tool_calling_agent`, AgentExecutor, and conversation memory with Ollama. *(See `beginner/B7-building-your-first-agent-with-langchain.md` for full details.)*

### Course B8: Introduction to RAG (Retrieval Augmented Generation)
> Give LLMs access to private data — text splitting, embeddings, ChromaDB vector store, building a RAG pipeline from scratch, and RAG with LangChain document loaders and retrievers. *(See `beginner/B8-introduction-to-rag.md` for full details.)*

### Course B9: Provider Abstraction — Write Once, Run Anywhere
> Avoid vendor lock-in — OpenAI SDK with Ollama, one-line provider swapping, LangChain abstraction layer, environment-based config, and cost tracking. *(See `beginner/B9-provider-abstraction.md` for full details.)*

### Course B10: Beginner Capstone Project
> Build an AI-Powered FAQ Assistant — combines RAG, tool calling, conversation memory, and provider abstraction, running on Ollama with one-line swap to cloud APIs. *(See `beginner/B10-beginner-capstone-project.md` for full details.)*

---

# LEVEL 2 — INTERMEDIATE

### Goal: Build multi-agent systems, complex workflows, and production-ready patterns

---

### Course I1: Deep Dive into Agent Architectures
> Agent design patterns (Router, Planner, Executor, Critic), single vs multi-agent, communication patterns, state management, error recovery, and observability. *(See `intermediate/I1-deep-dive-into-agent-architectures.md` for full details.)*

### Course I2: LangGraph — Graph-Based Agent Workflows
> Graph-based orchestration with nodes, edges, state, conditional branching, cycles, parallel execution, and building sophisticated multi-step agent pipelines. *(See `intermediate/I2-langgraph-graph-based-agent-workflows.md` for full details.)*

### Course I3: Human-in-the-Loop Agents
> Interrupt patterns, approval workflows, LangGraph checkpoints, escalation logic, and audit trails for agents that know when to ask humans for help. *(See `intermediate/I3-human-in-the-loop-agents.md` for full details.)*

### Course I4: Advanced RAG Patterns
> Beyond naive RAG — semantic/parent-child chunking, hybrid search (vector + BM25), re-ranking, multi-query RAG, self-corrective retrieval, and evaluation. *(See `intermediate/I4-advanced-rag-patterns.md` for full details.)*

### Course I5: Multi-Agent Systems with CrewAI
> Role-based multi-agent orchestration — agents, tasks, crews, processes, defining roles, task dependencies, sequential vs hierarchical workflows with Ollama. *(See `intermediate/I5-multi-agent-systems-with-crewai.md` for full details.)*

### Course I6: Memory Systems for Agents
> Short-term, long-term, episodic, and entity memory — conversation buffers, persistent vector DB memory, entity tracking, recall strategies, and memory management. *(See `intermediate/I6-memory-systems-for-agents.md` for full details.)*

### Course I7: Structured Outputs & Reliable Agent Responses
> Pydantic validation, Instructor library, retry strategies, LangChain output parsers, and guardrails for guaranteed structured, reliable LLM responses. *(See `intermediate/I7-structured-outputs-and-reliable-responses.md` for full details.)*

### Course I8: Agent Tools — Building Complex Integrations
> Production-grade tools for databases (SQL agents), REST/GraphQL APIs, file systems, web scraping (Playwright), code execution (sandboxed), and tool composition. *(See `intermediate/I8-agent-tools-building-complex-integrations.md` for full details.)*

### Course I9: Agent Evaluation & Testing
> Unit testing tools, integration testing workflows, LLM-as-judge, benchmarking with test datasets, regression testing, and LangSmith for tracing and evaluation. *(See `intermediate/I9-agent-evaluation-and-testing.md` for full details.)*

### Course I10: Intermediate Capstone Project
> Build an AI-Powered Customer Support System — multi-agent crew (Triage → Specialist → Escalation), RAG knowledge base, database tools, HITL approvals, LangGraph workflow, and Docker Compose deployment. *(See `intermediate/I10-intermediate-capstone-project.md` for full details.)*

---

# LEVEL 3 — ADVANCED

### Goal: Deploy production-grade agentic systems on the cloud with scalable architecture

---

### Course A1: Production Architecture for Agentic Systems
> Microservices vs monolith, event-driven architecture, message queues (Redis/RabbitMQ/Service Bus), API gateway design, stateless/stateful deployment, and horizontal scalability. *(See `advanced/A1-production-architecture-for-agentic-systems.md` for full details.)*

### Course A2: Containerization & Orchestration
> Docker best practices, multi-stage builds, Docker Compose, DinD sandboxing, Kubernetes fundamentals, operators for AI workloads, and Helm charts. *(See `advanced/A2-containerization-and-orchestration.md` for full details.)*

### Course A3: Cloud Deployment — Azure
> Azure Container Apps, Functions, Azure OpenAI, AI Search, Service Bus, Cosmos DB, and CI/CD with GitHub Actions for agentic AI deployment. *(See `advanced/A3-cloud-deployment-azure.md` for full details.)*

### Course A4: Cloud Deployment — AWS
> Amazon Bedrock, Lambda, ECS/EKS, OpenSearch, SQS/SNS, DynamoDB, and AWS CDK infrastructure as code for agentic AI deployment. *(See `advanced/A4-cloud-deployment-aws.md` for full details.)*

### Course A5: Cloud Deployment — Google Cloud Platform
> Cloud Run, Vertex AI Agents, Cloud Functions, AlloyDB/pgvector, Pub/Sub, and Firestore for agentic AI deployment on GCP. *(See `advanced/A5-cloud-deployment-gcp.md` for full details.)*

### Course A6: Scalability, Performance & Cost Optimization
> Load balancing, auto-scaling, caching (prompt/semantic/response), model routing, token optimization, batch processing, cost monitoring, and rate limiting. *(See `advanced/A6-scalability-performance-cost-optimization.md` for full details.)*

### Course A7: Security, Compliance & Guardrails
> Threat modeling, prompt injection defense, tool sandboxing, PII redaction, secrets management, network security, compliance (SOC 2/GDPR/HIPAA), and content safety. *(See `advanced/A7-security-compliance-guardrails.md` for full details.)*

### Course A8: Monitoring, Observability & Reliability
> OpenTelemetry tracing, LLM metrics, LangSmith/LangFuse, alerting, health checks, circuit breakers, graceful degradation, and disaster recovery. *(See `advanced/A8-monitoring-observability-reliability.md` for full details.)*

### Course A9: Real-World Application — Enterprise Document Processing
> Multi-agent document pipeline — classification, extraction, validation, human review, LangGraph orchestration, Azure Doc Intelligence/AWS Textract, and Kubernetes deployment. *(See `advanced/A9-enterprise-document-processing.md` for full details.)*

### Course A10: Real-World Application — AI-Powered Sales & CRM Agent
> Lead scoring, personalized outreach, meeting scheduling, Salesforce/HubSpot integration, multi-channel communication, and analytics dashboards. *(See `advanced/A10-ai-powered-sales-crm-agent.md` for full details.)*

### Course A11: Real-World Application — Autonomous DevOps Agent
> Monitor → Diagnose → Fix → Verify pipeline with PagerDuty/Datadog/Grafana integration, automated remediation with approval gates, and incident communication. *(See `advanced/A11-autonomous-devops-agent.md` for full details.)*

### Course A12: Real-World Application — Multi-Tenant AI Platform
> SaaS platform architecture — tenant isolation, custom agent config, usage metering/billing, white-labeling, per-tenant rate limiting, and multi-region deployment. *(See `advanced/A12-multi-tenant-ai-platform.md` for full details.)*

### Course A13: Advanced Capstone Project
> Production Agentic AI Platform on Cloud — multi-agent on Kubernetes, scalable architecture, production RAG, full observability, security, CI/CD, cost optimization, and load testing to 100+ concurrent users. *(See `advanced/A13-advanced-capstone-project.md` for full details.)*

---

## Appendices

### Appendix A: Docker Lab Reference
- Lab environment setup guide
- Docker-in-Docker (DinD) configuration
- Pre-built lab images index
- Troubleshooting common lab issues

### Appendix B: Model Comparison Guide
- Ollama model recommendations by use case
- Cloud model pricing comparison (Claude, GPT, Gemini)
- Model selection decision tree

### Appendix C: Tool & Framework Quick Reference
- LangChain cheat sheet
- LangGraph cheat sheet
- CrewAI cheat sheet
- Ollama command reference
- Vector database comparison

### Appendix D: Cloud Cost Calculators
- Azure cost estimation for agentic workloads
- AWS cost estimation for agentic workloads
- GCP cost estimation for agentic workloads
- Cost optimization checklist

---

## Learning Path Summary

```
BEGINNER (4-5 weeks)                INTERMEDIATE (5-6 weeks)           ADVANCED (6-8 weeks)
─────────────────────               ─────────────────────────          ──────────────────────
LLM Foundations                     Agent Architectures                Production Architecture
Local Setup (Ollama)                LangGraph Workflows                Containerization (K8s)
Python for AI                       Human-in-the-Loop                  Cloud: Azure/AWS/GCP
Prompt Engineering                  Advanced RAG                       Scalability & Cost
What are Agents                     Multi-Agent (CrewAI)               Security & Compliance
Tool Calling                        Memory Systems                     Monitoring & Observability
LangChain Basics                    Structured Outputs                 Real-World: Doc Processing
Basic RAG                           Complex Tool Integration           Real-World: Sales/CRM Agent
Provider Abstraction                Agent Testing                      Real-World: DevOps Agent
Capstone: FAQ Bot                   Capstone: Support System           Real-World: Multi-Tenant SaaS
                                                                       Capstone: Cloud Platform
```

---

*NMMR Technologies Private Limited — Agentic AI Training Program*
*Version 1.0 | 2025*
