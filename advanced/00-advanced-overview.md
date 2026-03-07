# Level 3 — Advanced: Production-Grade Agentic AI on the Cloud

## Overview

The Advanced level transforms you from an AI developer into an AI platform engineer. You'll learn to deploy, scale, secure, and monitor agentic AI systems in production on all three major cloud platforms. This level includes four real-world applications that mirror actual enterprise deployments.

**Duration**: 6-8 weeks (self-paced)
**Prerequisites**: Completed Intermediate level (or equivalent experience)
**Cost**: Cloud labs may incur small charges ($5-20 total for cloud deployments). Local Docker/K3s labs remain free.

---

## What You'll Learn

By the end of this level, you will:

- Design scalable, production-grade architectures for agentic AI systems
- Containerize and orchestrate agents with Docker and Kubernetes
- Deploy agentic systems on Azure, AWS, and GCP
- Implement auto-scaling, caching, and model routing for cost optimization
- Secure agents against prompt injection, PII leaks, and abuse
- Build full observability stacks with tracing, metrics, and alerting
- Build four real-world enterprise applications from architecture to deployment
- Design and operate multi-tenant AI platforms

---

## What You'll Build

| Module | Project |
|--------|---------|
| A1 | Scalable agent architecture (Docker Compose) |
| A2 | Kubernetes deployment of multi-agent system |
| A3 | Azure Container Apps deployment |
| A4 | AWS ECS + Bedrock deployment |
| A5 | GCP Cloud Run + Vertex AI deployment |
| A6 | Intelligent model routing and caching system |
| A7 | Security layer — injection defense, PII redaction, audit |
| A8 | Full observability stack (Grafana + Prometheus + OTel) |
| A9 | **Real-World: Enterprise Document Processing Pipeline** |
| A10 | **Real-World: AI-Powered Sales & CRM Agent** |
| A11 | **Real-World: Autonomous DevOps Incident Agent** |
| A12 | **Real-World: Multi-Tenant AI Platform** |
| **A13** | **Capstone: Production Agentic AI Platform on Cloud** |

---

## Lab Environment

Advanced labs extend the environment significantly:

- **K3s** (lightweight Kubernetes) running inside Docker
- **Docker Compose** stacks with 5-10 services
- **Cloud CLI tools** pre-installed (az, aws, gcloud)
- **Terraform** for infrastructure-as-code
- **Monitoring stack** (Grafana, Prometheus, Jaeger)
- **Load testing tools** (Locust, k6)
- **Security scanning tools** (Trivy, Bandit)

```bash
# Start an advanced lab
lab start advanced/A09-document-processing

# Start a cloud deployment lab (requires cloud credentials)
lab start advanced/A03-azure-deployment --cloud
```

---

## Modules

### Module A1: Production Architecture for Agentic Systems
**Duration**: 6-8 hours | **Lab**: Architecture implementation

Learn how to architect agentic AI systems for production — not as a monolith, but as a set of loosely coupled services that can scale independently. Design patterns for microservices, event-driven architectures, and message queues.

**Key Topics**:
- Monolith vs microservices for agent systems
- Service decomposition — Orchestrator, workers, tools, memory, gateway
- Event-driven architecture — Agents communicating via events
- Message queues — Redis Streams, RabbitMQ, Azure Service Bus
- API gateway design — Rate limiting, auth, request routing
- Stateless agent design for horizontal scaling
- Async agent execution — Fire-and-forget with callbacks
- Database patterns — Shared vs per-agent data stores

**Lab Project**: Design and implement a microservices-based agent architecture using Docker Compose — API Gateway → Orchestrator → Worker Agents → Tool Services → Memory Store. Load test to verify scalability.

---

### Module A2: Containerization & Orchestration
**Duration**: 6-8 hours | **Lab**: Kubernetes deployment

Package agents as production-grade containers and deploy them on Kubernetes. Learn multi-stage Docker builds, health checks, resource limits, and Kubernetes concepts (pods, deployments, services, ConfigMaps, Secrets).

**Key Topics**:
- Docker best practices for AI workloads
- Multi-stage builds — Small, secure images
- Health checks and readiness probes
- Resource limits — CPU, memory, GPU allocation
- Docker Compose for local development
- Docker-in-Docker for agent sandboxing (secure code execution)
- Kubernetes fundamentals — Pods, Deployments, Services, Ingress
- ConfigMaps and Secrets for agent configuration
- Helm charts for repeatable deployments
- K3s for lightweight local Kubernetes

**Lab Project**: Take the architecture from A1 and deploy it on K3s (Kubernetes running inside Docker). Configure health checks, auto-restart, resource limits, and rolling updates.

---

### Module A3: Cloud Deployment — Azure
**Duration**: 8-10 hours | **Lab**: Full Azure deployment

Deploy a production agentic AI system on Azure using the most cost-effective services. Azure Container Apps for serverless agent hosting, Azure AI Search for production RAG, Cosmos DB for agent state, and GitHub Actions CI/CD.

**Key Topics**:
- Azure architecture for AI workloads
- Azure Container Apps — Serverless containers with auto-scaling
- Azure Functions for event-driven agent triggers
- Azure OpenAI Service — Managed GPT/embedding models
- Azure AI Search — Production vector + keyword search
- Azure Service Bus — Reliable agent-to-agent messaging
- Azure Cosmos DB — Global-scale agent state and memory
- Azure Key Vault for secrets management
- GitHub Actions CI/CD pipeline
- Cost optimization — Reserved capacity, spot instances, consumption plans

**Lab Project**: Deploy the customer support system from Intermediate capstone on Azure — Container Apps for agents, AI Search for RAG, Cosmos DB for memory, Service Bus for orchestration, GitHub Actions for CI/CD.

---

### Module A4: Cloud Deployment — AWS
**Duration**: 8-10 hours | **Lab**: Full AWS deployment

Deploy agentic AI on AWS using Bedrock for managed models, ECS for container orchestration, and the broader AWS ecosystem for a fully managed production setup.

**Key Topics**:
- AWS architecture for AI workloads
- Amazon Bedrock — Managed access to Claude, Llama, and other models
- Amazon Bedrock Agents — Managed agent orchestration
- Amazon ECS (Fargate) — Serverless container hosting
- Amazon EKS — Managed Kubernetes for complex deployments
- Amazon OpenSearch — Production vector search
- Amazon SQS/SNS — Message queues for agent orchestration
- DynamoDB — Serverless agent state and session storage
- AWS CDK — Infrastructure as code (TypeScript)
- Cost optimization — Spot instances, Savings Plans, right-sizing

**Lab Project**: Deploy a multi-agent system on AWS — ECS Fargate for agents, Bedrock for model inference, OpenSearch for RAG, SQS for task queuing, DynamoDB for state. Deploy with AWS CDK.

---

### Module A5: Cloud Deployment — Google Cloud Platform
**Duration**: 6-8 hours | **Lab**: GCP deployment

Deploy agents on GCP using Cloud Run for serverless containers, Vertex AI for model access, and GCP's data services for a lean production setup.

**Key Topics**:
- GCP architecture for AI workloads
- Google Cloud Run — Serverless containers with auto-scaling to zero
- Vertex AI — Access to Gemini and managed agent builders
- Google Cloud Functions for lightweight agent triggers
- AlloyDB / Cloud SQL + pgvector — PostgreSQL-based vector search
- Pub/Sub — Event-driven agent communication
- Firestore — Real-time agent state management
- Cloud Build for CI/CD
- Cost optimization — Committed use discounts, auto-scaling policies

**Lab Project**: Deploy an agent system on GCP — Cloud Run for agents, Vertex AI for models, Cloud SQL + pgvector for RAG, Pub/Sub for messaging. Implement auto-scaling to zero for cost efficiency.

---

### Module A6: Scalability, Performance & Cost Optimization
**Duration**: 6-8 hours | **Lab**: Optimization implementation

Production agents must be fast, cheap, and reliable. Learn strategies for load balancing, auto-scaling, intelligent caching, model routing (cheap models for easy tasks, expensive models for hard ones), and comprehensive cost management.

**Key Topics**:
- Load balancing strategies for LLM workloads
- Auto-scaling triggers — Queue depth, latency percentiles, token throughput
- Prompt caching — Reusing common prompt prefixes
- Semantic caching — Cache responses for semantically similar queries
- Model routing — Classify task difficulty, route to appropriate model
- Token optimization — Prompt compression, context pruning
- Batch processing for non-real-time workloads
- Cost allocation — Per-agent, per-user, per-tenant metering
- Rate limiting and quota management
- Performance benchmarking methodology

**Lab Project**: Build an intelligent model router that classifies incoming requests by complexity and routes them: simple questions → Llama 8B (free), medium → Claude Haiku ($), complex → Claude Sonnet ($$). Add semantic caching to avoid redundant LLM calls. Measure cost savings.

---

### Module A7: Security, Compliance & Guardrails
**Duration**: 6-8 hours | **Lab**: Security layer implementation

Agentic AI systems introduce new attack surfaces. Learn to defend against prompt injection, validate tool calls, redact PII, manage secrets securely, and build audit trails for compliance.

**Key Topics**:
- Threat modeling for agentic AI systems
- Prompt injection — Direct, indirect, and multi-step attacks
- Prompt injection detection and defense strategies
- Tool call validation — Sandboxing, allowlists, parameter validation
- PII detection and redaction (Microsoft Presidio, custom regex)
- Secrets management — Key Vault, Secrets Manager, Vault
- Network security — VPCs, private endpoints, egress filtering
- Audit logging — Immutable logs of all agent decisions and actions
- Content safety — Input/output filtering for harmful content
- Compliance considerations — SOC 2, GDPR, HIPAA
- Data residency — Keeping data in specific regions

**Lab Project**: Build a security middleware layer for an agent system — Prompt injection detector (ML-based + heuristic), PII redactor (detect and mask sensitive data before LLM), tool call validator (sandbox + allowlist), and immutable audit logger.

---

### Module A8: Monitoring, Observability & Reliability
**Duration**: 6-8 hours | **Lab**: Observability stack setup

Build a complete observability stack for agentic AI. Structured logging, distributed tracing across multi-agent calls, LLM-specific metrics (tokens, latency, cost), dashboards, and alerting.

**Key Topics**:
- Three pillars: Logs, Metrics, Traces
- Structured logging for agent systems
- Distributed tracing with OpenTelemetry
- Tracing across multi-agent, multi-service calls
- LLM-specific metrics — Token usage, latency P50/P95/P99, cost, error rates
- LangSmith / LangFuse for LLM-specific observability
- Grafana dashboards for agent monitoring
- Prometheus for metrics collection
- Alerting — Agent failures, hallucination detection, cost anomalies
- Health checks and circuit breakers
- Graceful degradation — Fallback when LLM APIs are down
- Chaos engineering for agent systems

**Lab Project**: Set up a complete observability stack — Grafana dashboards showing agent metrics, Prometheus collecting metrics from agent services, OpenTelemetry distributed tracing across a multi-agent workflow, and alerts for error rates and cost spikes.

---

### Module A9: Real-World Application — Enterprise Document Processing
**Duration**: 10-12 hours | **Lab**: Complete pipeline build

Build an enterprise document processing system that classifies, extracts, validates, and routes documents using a multi-agent pipeline. This mirrors real deployments at insurance companies, law firms, and financial institutions.

**Key Topics**:
- Pipeline architecture: Intake → Classify → Extract → Validate → Store → Route
- Document classification agent (invoices, contracts, receipts, forms)
- Key-value extraction from unstructured documents
- Table extraction and structured data handling
- Validation agent — Cross-referencing against databases
- Confidence scoring — When to escalate to human review
- Azure Document Intelligence / AWS Textract integration
- Batch processing for high-volume document intake
- Scalable deployment on Kubernetes

**Lab Project**: Build and deploy the complete document processing pipeline — Upload PDFs → Classification agent → Extraction agent (different extractors per document type) → Validation agent (checks against sample database) → Human review queue for low-confidence extractions → Storage.

---

### Module A10: Real-World Application — AI-Powered Sales & CRM Agent
**Duration**: 10-12 hours | **Lab**: Full sales agent system

Build an AI sales assistant that qualifies leads, generates personalized outreach, manages follow-ups, and updates CRM — an increasingly common deployment in B2B sales organizations.

**Key Topics**:
- Sales pipeline automation architecture
- Lead qualification agent — Scoring based on company data and behavior
- Personalized outreach agent — Context-aware email generation
- Follow-up scheduling agent — Calendar integration
- CRM integration tools — Salesforce/HubSpot API patterns
- Multi-channel communication — Email, Slack, SMS
- A/B testing outreach strategies
- Analytics dashboard — Conversion metrics, agent performance
- HITL: Sales rep approval before sending

**Lab Project**: Build the complete system — Lead intake webhook → Qualification agent (scores and enriches) → Outreach agent (generates personalized email) → Human approval gate → Email sending → Follow-up scheduler → CRM update agent. Mock Salesforce API for testing.

---

### Module A11: Real-World Application — Autonomous DevOps Agent
**Duration**: 10-12 hours | **Lab**: Incident response agent

Build an autonomous DevOps agent that monitors systems, diagnoses incidents, proposes fixes, and (with human approval) executes remediation. Increasingly used for SRE and on-call automation.

**Key Topics**:
- Incident response architecture: Monitor → Alert → Diagnose → Fix → Verify
- Log analysis agent — Pattern recognition in application logs
- Metrics analysis agent — Detecting anomalies in time-series data
- Root cause analysis — Correlating logs, metrics, and events
- Remediation agent — Executing playbook actions (restart services, scale up, rollback)
- Safety guardrails — Human-in-the-loop for destructive operations
- Communication agent — Slack/Teams incident notifications and updates
- Integration with PagerDuty, Datadog, Grafana
- Runbook automation — Encoding operational procedures as agent tools
- Post-incident reporting agent

**Lab Project**: Build an autonomous incident response system — Simulated monitoring stack generates alerts → Diagnostic agent analyzes logs and metrics → Proposes remediation → Human approves → Execution agent performs fix → Verification agent confirms resolution → Communication agent posts Slack summary.

---

### Module A12: Real-World Application — Multi-Tenant AI Platform
**Duration**: 10-12 hours | **Lab**: Multi-tenant platform build

Build a SaaS platform that serves multiple customers, each with their own agents, data, and configurations. This is the architecture behind companies like AI customer support platforms, AI writing tools, and AI analytics dashboards.

**Key Topics**:
- Multi-tenant architecture patterns
- Tenant isolation — Separate data, models, and agent configurations
- Per-tenant customization — System prompts, tools, knowledge bases
- Usage metering — Token counting, API call tracking per tenant
- Billing integration — Stripe-like metering and invoicing
- Rate limiting per tenant
- Tenant onboarding automation
- White-labeling and branding
- Multi-region deployment for global tenants
- Tenant data migration and backup

**Lab Project**: Build a multi-tenant AI platform — Tenant registration → Custom agent configuration per tenant → Isolated RAG knowledge bases → Usage metering (per-token billing) → Rate limiting → Admin dashboard showing tenant usage. Deploy with tenant isolation verified.

---

### Module A13: Advanced Capstone Project
**Duration**: 15-20 hours | **Lab**: Full cloud deployment

The ultimate project: build a production-grade agentic AI platform and deploy it to the cloud. This capstone integrates every concept from all three levels.

**System Requirements**:
- Multi-agent system with at least 3 specialized agents
- Deployed on Kubernetes (choice of Azure AKS, AWS EKS, or GCP GKE)
- Production RAG with hybrid search and re-ranking
- Message queue-based agent orchestration
- Auto-scaling based on load
- Full security — Prompt injection defense, PII handling, audit logs
- Complete observability — Tracing, metrics, dashboards, alerts
- CI/CD pipeline with automated testing
- Cost optimization — Model routing, caching, efficient scaling
- Load tested to handle 100+ concurrent users
- Documentation — Architecture diagrams, runbooks, API docs

**Deliverables**:
1. Source code repository with CI/CD
2. Kubernetes manifests / Helm charts
3. Terraform/CDK infrastructure code
4. Architecture decision document
5. Observability dashboards
6. Load test results
7. Security audit report
8. Cost analysis and optimization report
9. Deployment runbook

**Evaluation Criteria**:
- Architecture quality and scalability design
- Code quality and testing coverage
- Security posture
- Operational readiness (monitoring, alerting, runbooks)
- Cost efficiency
- Documentation completeness

---

## Cloud Cost Guide for Labs

| Module | Local Lab (Free) | Cloud Lab (Estimated Cost) |
|--------|-----------------|---------------------------|
| A1-A2 | Docker + K3s | $0 |
| A3 | Simulated | Azure: ~$5-10 |
| A4 | Simulated | AWS: ~$5-10 |
| A5 | Simulated | GCP: ~$3-8 |
| A6-A8 | Docker stack | $0 |
| A9-A12 | Docker stack | $0 |
| A13 | K3s locally | Cloud: ~$10-20 |

**Tips to minimize cloud costs**:
- Use free tier services wherever possible
- Tear down resources immediately after lab completion
- Use spot/preemptible instances for workers
- Set billing alerts at $5 increments

---

## Next Steps

After completing the Advanced level, you are a **production-ready Agentic AI engineer** capable of:
- Designing scalable agent architectures
- Deploying on any major cloud platform
- Building enterprise-grade applications
- Operating agents in production with security and observability

**Certification**: Complete all three levels + capstone projects to earn the NMMR Agentic AI Developer certification.

---

*NMMR Technologies — Agentic AI Training Program | Advanced Level*
