# Course A4: Cloud Deployment — AWS

> **Deploy agentic AI systems on Amazon Web Services** — Bedrock, Lambda, ECS/EKS, OpenSearch, SQS/SNS, DynamoDB, and infrastructure as code with AWS CDK.

### Goal: Deploy and operate a production agentic AI system on AWS

---

## A4.1 AWS Architecture for Agentic AI Applications
- Reference architecture — AWS services for agentic AI workloads
- Compute options — ECS vs EKS vs Lambda vs App Runner
- Data layer — DynamoDB, RDS, S3, ElastiCache
- AI services — Bedrock, SageMaker, Comprehend, Textract
- Messaging — SQS, SNS, EventBridge, Step Functions
- Security — IAM, Secrets Manager, VPC, PrivateLink
- Networking — VPC design, subnets, NAT Gateway, ALB
- Cost estimation — AWS Pricing Calculator for the complete stack

## A4.2 Amazon Bedrock — Managed Agent Deployment (Lab)
- Bedrock Agents — Managed agent runtime with built-in tool calling
- Agent configuration — Instructions, model selection, action groups
- Action groups — Defining tools as Lambda functions or API schemas
- Knowledge bases — Managed RAG with S3 data sources
- Session management — Stateful conversations with session attributes
- Guardrails — Content filtering, topic blocking, PII redaction
- Testing — Bedrock console test window and API testing
- Monitoring — CloudWatch metrics for Bedrock agent invocations

## A4.3 AWS Lambda for Serverless Agent Functions (Lab)
- Lambda for agents — Event-driven, pay-per-execution agent logic
- Python Lambda functions — Creating agent tool functions
- Trigger sources — API Gateway, SQS, EventBridge, S3 events
- Lambda layers — Packaging shared dependencies (langchain, boto3)
- Cold start optimization — Provisioned concurrency, minimal dependencies
- Step Functions — Orchestrating multi-step agent workflows
- Timeout management — Handling long-running agent tasks (15 min limit)
- Error handling — Dead-letter queues, retry policies, error destinations

## A4.4 Amazon ECS/EKS for Containerized Agents (Lab)
- ECS Fargate — Serverless containers for agent deployment
- Task definitions — CPU, memory, environment, secrets configuration
- Service configuration — Desired count, load balancing, auto-scaling
- EKS — Managed Kubernetes for complex agent deployments
- EKS with Karpenter — Intelligent auto-scaling for diverse workloads
- GPU instances — Deploying agents with local model inference
- Service mesh — App Mesh for agent-to-agent communication
- Logging — CloudWatch Logs, Fluent Bit for container log aggregation

## A4.5 Amazon OpenSearch for Production RAG (Lab)
- OpenSearch for RAG — Full-text + vector search in one service
- Index design — Mappings for text fields, vector fields, metadata
- k-NN search — Vector similarity search with HNSW or IVF algorithms
- Hybrid search — Combining BM25 text search with vector search
- Ingestion pipelines — Automated document processing and indexing
- Security — Fine-grained access control, encryption, VPC
- Scaling — Data nodes, master nodes, UltraWarm for cost optimization

## A4.6 Amazon SQS/SNS for Agent Orchestration (Lab)
- SQS for agents — Reliable message queuing between agent services
- Standard vs FIFO queues — Ordering guarantees and deduplication
- SNS for events — Fan-out notifications to multiple agent consumers
- EventBridge — Advanced event routing with content-based filtering
- Dead-letter queues — Handling failed agent messages
- Visibility timeout — Preventing duplicate processing
- Long polling — Efficient message retrieval

## A4.7 DynamoDB for Agent State and Session Management
- DynamoDB for agents — Low-latency, scalable key-value and document store
- Table design — Partition key, sort key for agent session data
- Single-table design — Modeling multiple entity types in one table
- TTL — Automatic cleanup of expired sessions
- Streams — Reacting to state changes with Lambda triggers
- Global tables — Multi-region replication for global agent deployments
- On-demand vs provisioned — Capacity modes for agent workloads

## A4.8 AWS CDK for Infrastructure as Code (Lab)
- What is CDK — Define cloud infrastructure in Python
- CDK constructs — L1 (CloudFormation), L2 (curated), L3 (patterns)
- Stacking — Organizing resources into logical stacks
- Agent infrastructure stack — VPC, ECS, DynamoDB, SQS, Bedrock
- Environment configuration — Dev, staging, production via CDK contexts
- CI/CD integration — CDK Pipelines for automated deployment
- Testing — Snapshot tests, fine-grained assertions
- Best practices — Construct libraries, reusable patterns, tagging
