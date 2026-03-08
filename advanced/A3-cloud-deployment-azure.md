# Course A3: Cloud Deployment — Azure

> **Deploy agentic AI systems on Microsoft Azure** — Container Apps, Functions, Azure OpenAI, AI Search, Service Bus, Cosmos DB, and CI/CD with GitHub Actions.

### Goal: Deploy and operate a production agentic AI system on Azure

---

## A3.1 Azure Architecture for Agentic AI Applications
- Reference architecture — Azure services for agentic AI workloads
- Compute options — Container Apps vs App Service vs AKS vs Functions
- Data layer — Cosmos DB, Azure SQL, Azure Storage
- AI services — Azure OpenAI, AI Search, Document Intelligence
- Messaging — Service Bus, Event Grid, Event Hubs
- Security — Managed Identity, Key Vault, Private Endpoints
- Networking — VNet integration, DNS, Application Gateway
- Cost estimation — Pricing calculator for the complete architecture

## A3.2 Azure Container Apps — Serverless Agent Deployment (Lab)
- What is Container Apps — Serverless containers with auto-scaling
- Creating a Container App — Azure CLI and portal walkthrough
- Container configuration — Image, CPU, memory, environment variables
- Scaling rules — HTTP-based, queue-based, custom (KEDA) scaling
- Revisions — Traffic splitting, blue-green deployments, canary releases
- Managed identity — Passwordless authentication to Azure services
- Custom domains and TLS — Production-ready HTTPS endpoints
- Dapr integration — Sidecar for service-to-service communication and state

## A3.3 Azure Functions for Event-Driven Agent Triggers (Lab)
- Azure Functions for agents — Lightweight, event-driven agent invocation
- Trigger types — HTTP, Timer, Queue, Blob, Event Grid triggers
- Agent orchestration with Durable Functions — Stateful workflows, fan-out/fan-in
- Python Function Apps — Creating and deploying Python-based agent functions
- Bindings — Input/output bindings to Azure services
- Cold start optimization — Reducing startup latency for agent functions
- Premium plan — Pre-warmed instances for consistent performance

## A3.4 Azure OpenAI Service Integration (Lab)
- Deploying models — GPT-4o, o1, embedding models on Azure
- Private endpoints — Securing Azure OpenAI behind VNet
- Managed identity authentication — No API keys in code
- Content filtering — Configuring Azure's content safety filters
- Provisioned throughput — Reserved capacity for predictable performance
- Multi-region deployment — Failover and load balancing across regions
- Monitoring — Azure Monitor metrics for Azure OpenAI usage

## A3.5 Azure AI Search for Production RAG (Lab)
- What is Azure AI Search — Enterprise search with vector and keyword support
- Index creation — Defining fields, vector configurations, semantic ranking
- Data ingestion — Indexers for Blob Storage, SQL, Cosmos DB
- Hybrid search — Vector + keyword + semantic ranking in one query
- Skillsets — AI enrichment during indexing (OCR, entity extraction, translation)
- Security — RBAC, managed identity, private endpoints
- Scaling — Replicas for throughput, partitions for data volume

## A3.6 Azure Service Bus for Agent-to-Agent Communication (Lab)
- Service Bus for agents — Reliable, ordered, transactional messaging
- Queues — Point-to-point agent communication
- Topics and subscriptions — Pub/sub for broadcasting agent events
- Sessions — Ordered message processing per conversation
- Dead-letter queue — Handling failed messages
- Message scheduling — Delayed message delivery for retries
- Integration with Container Apps — KEDA scaling based on queue depth

## A3.7 Azure Cosmos DB for Agent State and Memory
- Why Cosmos DB — Global distribution, multi-model, low latency
- Data modeling — Designing collections for agent state, memory, conversations
- Partition strategy — Choosing partition keys for agent workloads
- Change feed — Reacting to state changes in real-time
- TTL — Automatic cleanup of expired agent sessions
- Vector search — Cosmos DB vector capabilities for RAG
- Cost optimization — Request units, serverless vs provisioned throughput

## A3.8 CI/CD with GitHub Actions for Agent Deployment (Lab)
- Pipeline design — Build → Test → Deploy for agent systems
- Docker build and push — Building and pushing to Azure Container Registry
- Environment management — Dev, staging, production with GitHub environments
- Secrets management — GitHub secrets for Azure credentials
- Automated testing — Running agent tests in CI pipeline
- Deployment strategies — Rolling update, blue-green, canary via GitHub Actions
- Infrastructure as code — Bicep/Terraform for Azure resource provisioning
- Monitoring integration — Post-deployment health checks and smoke tests
