# Course A5: Cloud Deployment — Google Cloud Platform

> **Deploy agentic AI systems on Google Cloud** — Cloud Run, Vertex AI Agents, Cloud Functions, AlloyDB/pgvector, Pub/Sub, Firestore, and end-to-end deployment.

### Goal: Deploy and operate a production agentic AI system on GCP

---

## A5.1 GCP Architecture for Agentic AI Applications
- Reference architecture — GCP services for agentic AI workloads
- Compute options — Cloud Run vs GKE vs Cloud Functions vs App Engine
- Data layer — Firestore, AlloyDB, Cloud SQL, BigQuery, Cloud Storage
- AI services — Vertex AI, Gemini API, Document AI, Natural Language API
- Messaging — Pub/Sub, Cloud Tasks, Eventarc, Workflows
- Security — IAM, Secret Manager, VPC Service Controls
- Networking — VPC, Cloud Load Balancing, Cloud CDN
- Cost estimation — GCP Pricing Calculator for the complete stack

## A5.2 Google Cloud Run for Serverless Agent Containers (Lab)
- What is Cloud Run — Fully managed serverless containers
- Deploying agent containers — `gcloud run deploy` with source or image
- Configuration — CPU, memory, concurrency, request timeout, min/max instances
- Auto-scaling — Scale to zero, rapid scale-up, concurrency-based scaling
- Traffic management — Revisions, traffic splitting, gradual rollouts
- Service-to-service auth — IAM-based authentication between Cloud Run services
- Custom domains — Mapping domains to Cloud Run services
- Cloud Run Jobs — Long-running batch agent tasks

## A5.3 Vertex AI Agents — Google's Managed Agent Platform (Lab)
- What is Vertex AI Agents — Google's managed agent building platform
- Agent Builder — No-code/low-code agent creation in the console
- Grounding — Connecting agents to Google Search and custom data stores
- Data stores — Uploading documents, websites, BigQuery data for agent knowledge
- Tools — Defining custom tools with OpenAPI specs or Cloud Functions
- Conversation history — Built-in multi-turn conversation management
- Testing — Console-based agent testing and evaluation
- Deployment — Publishing agents as APIs or embedding in applications

## A5.4 Google Cloud Functions for Event-Driven Agents (Lab)
- Cloud Functions for agents — Lightweight, event-driven agent logic
- HTTP functions — Agent endpoints triggered by HTTP requests
- Event-driven functions — Pub/Sub, Cloud Storage, Firestore triggers
- Python runtime — Creating agent functions with Python 3.11+
- Dependencies — `requirements.txt` for agent libraries
- Concurrency — Handling multiple agent requests per instance
- Workflows — Orchestrating multi-step agent pipelines with Cloud Workflows
- Error handling — Retry policies, dead-letter topics

## A5.5 AlloyDB / Cloud SQL + pgvector for Production RAG (Lab)
- pgvector — PostgreSQL extension for vector similarity search
- AlloyDB for AI — Google's PostgreSQL-compatible database with vector support
- Cloud SQL + pgvector — Standard PostgreSQL with vector extension
- Schema design — Text columns, vector columns, metadata, indexes
- HNSW indexes — Approximate nearest neighbor for fast vector search
- Hybrid queries — SQL filters + vector similarity in one query
- Ingestion — Batch loading documents and embeddings
- Performance tuning — Index parameters, connection pooling, query optimization

## A5.6 Pub/Sub for Agent Messaging (Lab)
- Pub/Sub for agents — Global, scalable, real-time messaging
- Topics and subscriptions — Publishing agent events, subscribing to actions
- Push vs pull subscriptions — Webhook delivery vs polling
- Ordering — Message ordering keys for sequential processing
- Dead-letter topics — Handling failed message processing
- Filtering — Attribute-based message filtering at subscription level
- Integration — Pub/Sub with Cloud Run, Cloud Functions, Dataflow

## A5.7 Firestore for Agent State Management
- Firestore for agents — Serverless, real-time, document database
- Data modeling — Collections and documents for agent state, sessions, memory
- Real-time listeners — Streaming state changes to connected clients
- Transactions — Atomic state updates across multiple documents
- TTL — Automatic document expiration for session cleanup
- Offline support — Client-side caching for mobile agent applications
- Security rules — Fine-grained access control for multi-tenant agents
- Composite indexes — Querying agent data by multiple fields
