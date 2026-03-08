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

### Goal: Understand AI agents and build your first working agents locally

---

### Module B1: Foundations of AI & Large Language Models
- B1.1 What is Artificial Intelligence — A quick history
- B1.2 What are Large Language Models (LLMs)
- B1.3 How LLMs work — Transformers, tokens, attention
- B1.4 Key concepts — Context window, temperature, tokens, hallucinations
- B1.5 The LLM landscape — OpenAI, Anthropic Claude, Google Gemini, Meta Llama, Mistral
- B1.6 Closed-source vs Open-source models
- B1.7 **Lab**: Chat with different LLMs via web UI and observe differences

### Module B2: Setting Up Your Local AI Environment
- B2.1 Introduction to Ollama — Run LLMs on your machine
- B2.2 Installing Ollama (Linux/Mac/Windows)
- B2.3 Pulling and running your first model (`llama3.1:8b`)
- B2.4 Understanding model sizes, quantization, and VRAM requirements
- B2.5 Ollama CLI commands — `run`, `pull`, `list`, `ps`, `rm`
- B2.6 Ollama REST API — `http://localhost:11434`
- B2.7 **Lab**: Install Ollama, pull models, chat via CLI and API

### Module B3: Python for AI — Quick Refresher
- B3.1 Python basics recap — variables, functions, classes
- B3.2 Working with APIs — `requests` library
- B3.3 JSON handling for LLM responses
- B3.4 Async programming basics — `asyncio`, `aiohttp`
- B3.5 Virtual environments and dependency management
- B3.6 **Lab**: Python API exercises calling Ollama

### Module B4: Prompt Engineering Fundamentals
- B4.1 What is prompt engineering and why it matters
- B4.2 System prompts vs User prompts vs Assistant messages
- B4.3 Zero-shot, few-shot, and chain-of-thought prompting
- B4.4 Structured output — Getting JSON responses from LLMs
- B4.5 Prompt templates and variables
- B4.6 Common pitfalls and how to avoid them
- B4.7 **Lab**: Prompt engineering exercises with Ollama

### Module B5: Introduction to AI Agents
- B5.1 What is an AI agent — Beyond chatbots
- B5.2 Agent = LLM + Tools + Memory + Planning
- B5.3 The ReAct pattern — Reason → Act → Observe → Repeat
- B5.4 Types of agents — Conversational, task-oriented, autonomous
- B5.5 Agent vs Chain vs Simple LLM call — When to use what
- B5.6 Real-world agent examples and use cases
- B5.7 **Lab**: Trace through an agent's reasoning loop manually

### Module B6: Tool Calling — Giving Agents Abilities
- B6.1 What is tool/function calling
- B6.2 How tool calling works — The LLM decides, your code executes
- B6.3 Defining tools with JSON schemas
- B6.4 Tool calling with Ollama (Llama 3.1 native support)
- B6.5 Building your first tool — A calculator agent
- B6.6 Multiple tools — Search + calculator + file reader
- B6.7 Handling tool errors gracefully
- B6.8 **Lab**: Build a multi-tool agent from scratch with Ollama

### Module B7: Building Your First Agent with LangChain
- B7.1 What is LangChain — The orchestration layer
- B7.2 LangChain core concepts — Models, prompts, chains, tools, agents
- B7.3 Setting up LangChain with Ollama
- B7.4 Creating tools with `@tool` decorator
- B7.5 Building a ReAct agent with `create_tool_calling_agent`
- B7.6 AgentExecutor — Running agents with verbose tracing
- B7.7 Adding conversation memory to agents
- B7.8 **Lab**: Build a research assistant agent using LangChain + Ollama

### Module B8: Introduction to RAG (Retrieval Augmented Generation)
- B8.1 The problem — LLMs don't know your private data
- B8.2 What is RAG — Retrieve → Augment → Generate
- B8.3 Text splitting and chunking strategies
- B8.4 Embeddings — Converting text to vectors
- B8.5 Vector databases — ChromaDB (local, free)
- B8.6 Building a simple RAG pipeline
- B8.7 RAG with LangChain — Document loaders, retrievers, chains
- B8.8 **Lab**: Build a "Chat with your PDF" application

### Module B9: Provider Abstraction — Write Once, Run Anywhere
- B9.1 Why provider abstraction matters
- B9.2 Using the OpenAI SDK with Ollama (compatible API)
- B9.3 Swapping Ollama → OpenAI → Anthropic Claude with one-line changes
- B9.4 LangChain's provider abstraction layer
- B9.5 Environment-based configuration (dev=Ollama, prod=Claude)
- B9.6 Cost tracking and token usage monitoring
- B9.7 **Lab**: Build an agent that runs on Ollama locally, then swap to Claude API

### Module B10: Beginner Capstone Project
- B10.1 Project: **AI-Powered FAQ Assistant**
  - Loads company documents (PDF/text)
  - Uses RAG to answer questions accurately
  - Has tool calling for live data (weather, calculator, date/time)
  - Runs on Ollama locally
  - One-line swap to Claude/OpenAI for deployment
- B10.2 **Lab**: Full capstone project build in Docker environment

---

# LEVEL 2 — INTERMEDIATE

### Goal: Build multi-agent systems, complex workflows, and production-ready patterns

---

### Module I1: Deep Dive into Agent Architectures
- I1.1 Agent design patterns — Router, Planner, Executor, Critic
- I1.2 Single-agent vs Multi-agent architectures
- I1.3 Agent communication patterns — Sequential, parallel, hierarchical
- I1.4 State management in agentic systems
- I1.5 Error handling and recovery strategies
- I1.6 Agent observability — Tracing and debugging
- I1.7 **Lab**: Implement each architecture pattern with Ollama

### Module I2: LangGraph — Graph-Based Agent Workflows
- I2.1 Why LangGraph — Limitations of simple agent loops
- I2.2 Graph concepts — Nodes, edges, state, conditional branching
- I2.3 Building your first LangGraph workflow
- I2.4 State management with TypedDict and Pydantic
- I2.5 Conditional edges — Dynamic routing based on agent decisions
- I2.6 Cycles and loops — Agents that iterate until done
- I2.7 Parallel execution — Running multiple nodes simultaneously
- I2.8 **Lab**: Build a research → write → review agent workflow with LangGraph

### Module I3: Human-in-the-Loop Agents
- I3.1 Why HITL — Trust, safety, and compliance
- I3.2 Interrupt patterns — Pause agent, get approval, resume
- I3.3 Implementing HITL with LangGraph checkpoints
- I3.4 Approval workflows — Agent proposes, human approves
- I3.5 Escalation — When agents should hand off to humans
- I3.6 Audit trails and logging agent decisions
- I3.7 **Lab**: Build an expense approval agent with human approval gates

### Module I4: Advanced RAG Patterns
- I4.1 Limitations of naive RAG
- I4.2 Chunking strategies — Semantic, recursive, parent-child
- I4.3 Hybrid search — Combining vector search + keyword search (BM25)
- I4.4 Re-ranking — Cross-encoder models for better relevance
- I4.5 Multi-query RAG — Generating multiple search queries
- I4.6 Self-corrective RAG — Agent verifies and retries retrieval
- I4.7 RAG evaluation — Measuring retrieval quality and answer accuracy
- I4.8 **Lab**: Build an advanced RAG system with hybrid search and re-ranking

### Module I5: Multi-Agent Systems with CrewAI
- I5.1 What is CrewAI — Role-based multi-agent orchestration
- I5.2 Core concepts — Agents, Tasks, Crews, Processes
- I5.3 Defining agent roles — Researcher, Writer, Reviewer, Coder
- I5.4 Task dependencies and workflows
- I5.5 Sequential vs Hierarchical crew processes
- I5.6 Using CrewAI with Ollama
- I5.7 **Lab**: Build a content creation crew — Research → Write → Edit → Publish

### Module I6: Memory Systems for Agents
- I6.1 Types of memory — Short-term, long-term, episodic, semantic
- I6.2 Conversation memory — Buffer, summary, sliding window
- I6.3 Persistent memory with vector databases
- I6.4 Entity memory — Tracking facts about people, places, things
- I6.5 Memory injection strategies — When and how to recall
- I6.6 Memory management — Forgetting, updating, compressing
- I6.7 **Lab**: Build an agent with persistent long-term memory using ChromaDB

### Module I7: Structured Outputs & Reliable Agent Responses
- I7.1 The reliability problem with LLM outputs
- I7.2 Pydantic models for structured output validation
- I7.3 Instructor library — Guaranteed structured outputs
- I7.4 Retry strategies and self-correction
- I7.5 Output parsing with LangChain
- I7.6 Guardrails — Input/output validation frameworks
- I7.7 **Lab**: Build a data extraction agent with guaranteed JSON output

### Module I8: Agent Tools — Building Complex Integrations
- I8.1 Tool design principles — Clear descriptions, proper schemas
- I8.2 Building database tools — SQL query agents
- I8.3 Building API tools — REST and GraphQL integrations
- I8.4 File system tools — Reading, writing, transforming files
- I8.5 Web scraping tools — Browser automation with Playwright
- I8.6 Code execution tools — Sandboxed Python execution
- I8.7 Tool composition — Combining tools for complex tasks
- I8.8 **Lab**: Build a customer support agent with database + email + ticket tools

### Module I9: Agent Evaluation & Testing
- I9.1 Why testing agents is different from testing software
- I9.2 Unit testing tools and individual components
- I9.3 Integration testing agent workflows
- I9.4 LLM-as-judge — Using a model to evaluate agent outputs
- I9.5 Benchmarking with test datasets
- I9.6 Regression testing — Catching agent behavior changes
- I9.7 LangSmith for tracing and evaluation
- I9.8 **Lab**: Build a test suite for your agents with automated evaluation

### Module I10: Intermediate Capstone Project
- I10.1 Project: **AI-Powered Customer Support System**
  - Multi-agent crew: Triage Agent → Specialist Agent → Escalation Agent
  - RAG-based knowledge base with company docs
  - Database tools for order lookup and ticket management
  - Human-in-the-loop for refund approvals
  - Memory for returning customer context
  - Full LangGraph workflow with conditional routing
  - Runs on Ollama, deployable on Claude/OpenAI
- I10.2 **Lab**: Full capstone project with Docker-composed multi-service setup

---

# LEVEL 3 — ADVANCED

### Goal: Deploy production-grade agentic systems on the cloud with scalable architecture

---

### Module A1: Production Architecture for Agentic Systems
- A1.1 Architectural patterns — Microservices vs monolith for agents
- A1.2 Separation of concerns — Orchestrator, workers, tools, memory
- A1.3 Event-driven architecture for agents
- A1.4 Message queues — Agent communication via Redis/RabbitMQ/Azure Service Bus
- A1.5 API gateway design for agent endpoints
- A1.6 Stateless vs stateful agent deployment
- A1.7 Designing for horizontal scalability
- A1.8 **Lab**: Design and implement a scalable agent architecture with Docker Compose

### Module A2: Containerization & Orchestration
- A2.1 Docker best practices for AI applications
- A2.2 Multi-stage builds for lean agent containers
- A2.3 Docker Compose for multi-agent development environments
- A2.4 Docker-in-Docker (DinD) for agent sandboxing
- A2.5 Kubernetes fundamentals for agent deployment
- A2.6 Kubernetes operators for AI workloads
- A2.7 Helm charts for agentic system deployment
- A2.8 **Lab**: Kubernetes deployment of a multi-agent system (K3s in Docker)

### Module A3: Cloud Deployment — Azure
- A3.1 Azure architecture for agentic AI applications
- A3.2 Azure Container Apps — Serverless agent deployment
- A3.3 Azure Functions for event-driven agent triggers
- A3.4 Azure OpenAI Service integration
- A3.5 Azure AI Search for production RAG
- A3.6 Azure Service Bus for agent-to-agent communication
- A3.7 Azure Cosmos DB for agent state and memory
- A3.8 CI/CD with GitHub Actions for agent deployment
- A3.9 **Lab**: Deploy a full agentic system to Azure Container Apps

### Module A4: Cloud Deployment — AWS
- A4.1 AWS architecture for agentic AI applications
- A4.2 Amazon Bedrock — Managed agent deployment
- A4.3 AWS Lambda for serverless agent functions
- A4.4 Amazon ECS/EKS for containerized agents
- A4.5 Amazon OpenSearch for production RAG
- A4.6 Amazon SQS/SNS for agent orchestration
- A4.7 DynamoDB for agent state and session management
- A4.8 AWS CDK for infrastructure as code
- A4.9 **Lab**: Deploy a production agent system on AWS ECS with Bedrock

### Module A5: Cloud Deployment — Google Cloud Platform
- A5.1 GCP architecture for agentic AI applications
- A5.2 Google Cloud Run for serverless agent containers
- A5.3 Vertex AI Agents — Google's managed agent platform
- A5.4 Google Cloud Functions for event-driven agents
- A5.5 AlloyDB / Cloud SQL + pgvector for production RAG
- A5.6 Pub/Sub for agent messaging
- A5.7 Firestore for agent state management
- A5.8 **Lab**: Deploy agents on Cloud Run with Vertex AI integration

### Module A6: Scalability, Performance & Cost Optimization
- A6.1 Load balancing agent requests
- A6.2 Auto-scaling strategies — Scaling on queue depth, latency, token usage
- A6.3 Caching strategies — Prompt caching, semantic caching, response caching
- A6.4 Model routing — Using cheaper models for simple tasks, expensive models for complex ones
- A6.5 Token optimization — Prompt compression, context pruning
- A6.6 Batch processing vs real-time inference
- A6.7 Cost monitoring and budgeting — Per-agent, per-user, per-tenant
- A6.8 Rate limiting and throttling
- A6.9 **Lab**: Implement intelligent model routing and caching for cost optimization

### Module A7: Security, Compliance & Guardrails
- A7.1 Threat model for agentic AI systems
- A7.2 Prompt injection attacks — Detection and prevention
- A7.3 Tool call validation and sandboxing
- A7.4 PII detection and redaction in agent flows
- A7.5 Secrets management — Azure Key Vault, AWS Secrets Manager, HashiCorp Vault
- A7.6 Network security — VPCs, private endpoints, firewall rules
- A7.7 Audit logging and compliance (SOC 2, GDPR, HIPAA considerations)
- A7.8 Content safety — Input/output filtering
- A7.9 **Lab**: Implement security layers — prompt injection defense, PII redaction, audit logging

### Module A8: Monitoring, Observability & Reliability
- A8.1 Observability pillars for agents — Logs, metrics, traces
- A8.2 Distributed tracing for multi-agent systems (OpenTelemetry)
- A8.3 LLM-specific metrics — Token usage, latency, cost, error rates
- A8.4 LangSmith / LangFuse for agent observability
- A8.5 Alerting on agent failures, hallucinations, and anomalies
- A8.6 Health checks and circuit breakers
- A8.7 Graceful degradation — Fallback strategies when LLM APIs go down
- A8.8 Disaster recovery and backup strategies
- A8.9 **Lab**: Set up full observability stack — Grafana, Prometheus, OpenTelemetry for agents

### Module A9: Real-World Application — Enterprise Document Processing
- A9.1 Architecture overview — Intake → Classify → Extract → Validate → Store
- A9.2 Document classification agent — Invoices, contracts, receipts, forms
- A9.3 Data extraction agent — Key-value extraction from unstructured docs
- A9.4 Validation agent — Cross-referencing extracted data against databases
- A9.5 Human review workflow for low-confidence extractions
- A9.6 Pipeline orchestration with LangGraph
- A9.7 Azure Document Intelligence / AWS Textract integration
- A9.8 Scalable deployment on Kubernetes
- A9.9 **Lab**: Build and deploy the complete document processing pipeline

### Module A10: Real-World Application — AI-Powered Sales & CRM Agent
- A10.1 Architecture — Lead scoring, outreach, follow-up, CRM update
- A10.2 Lead qualification agent — Analyzing inbound leads
- A10.3 Personalized outreach agent — Generating tailored emails
- A10.4 Meeting scheduling agent — Calendar integration
- A10.5 CRM integration — Salesforce / HubSpot API tools
- A10.6 Multi-channel communication — Email, Slack, SMS
- A10.7 Analytics dashboard — Agent performance metrics
- A10.8 **Lab**: Build the complete sales agent system with CRM integration

### Module A11: Real-World Application — Autonomous DevOps Agent
- A11.1 Architecture — Monitor → Diagnose → Fix → Verify
- A11.2 Monitoring agent — Detecting anomalies in logs and metrics
- A11.3 Diagnostic agent — Root cause analysis using tools
- A11.4 Remediation agent — Executing fix actions with approval gates
- A11.5 Incident communication agent — Slack/Teams notifications
- A11.6 Integration with PagerDuty, Datadog, Grafana
- A11.7 Safety: Human-in-the-loop for destructive operations
- A11.8 **Lab**: Build an autonomous incident response agent

### Module A12: Real-World Application — Multi-Tenant AI Platform
- A12.1 Architecture for SaaS agentic AI platforms
- A12.2 Tenant isolation — Data, models, agents per customer
- A12.3 Custom agent configuration per tenant
- A12.4 Usage metering and billing (per token, per agent call)
- A12.5 White-labeling and custom branding
- A12.6 API rate limiting per tenant
- A12.7 Multi-region deployment for global availability
- A12.8 **Lab**: Build a multi-tenant agent platform with tenant isolation

### Module A13: Advanced Capstone Project
- A13.1 Project: **Production Agentic AI Platform on Cloud**
  - Multi-agent system deployed on Kubernetes (choice of Azure/AWS/GCP)
  - Scalable architecture with message queues and auto-scaling
  - Production RAG with hybrid search and re-ranking
  - Full observability — Tracing, metrics, dashboards
  - Security — Prompt injection defense, PII handling, audit logs
  - CI/CD pipeline with automated testing
  - Cost optimization with model routing and caching
  - Load tested to 100+ concurrent users
- A13.2 **Lab**: Full capstone with cloud deployment and load testing

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
