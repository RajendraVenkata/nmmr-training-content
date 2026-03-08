# Course A1: Production Architecture for Agentic Systems

> **Design scalable, production-ready architectures for AI agents** — Microservices vs monolith, event-driven design, message queues, API gateways, and horizontal scalability patterns.

### Goal: Architect agentic AI systems that scale reliably in production

---

## A1.1 Architectural Patterns — Microservices vs Monolith for Agents
- Monolithic agent systems — Single service handling all agent logic
- Microservices for agents — Each agent or capability as an independent service
- When monolith works — Simple agents, small teams, early-stage development
- When microservices win — Complex systems, independent scaling, team autonomy
- Service boundaries — Splitting by agent role, tool type, or workflow stage
- Communication between services — Sync (REST/gRPC) vs async (message queues)
- Trade-offs — Complexity, latency, debugging, deployment

## A1.2 Separation of Concerns — Orchestrator, Workers, Tools, Memory
- The orchestrator layer — Central coordination of agent workflows
- Worker agents — Specialized agents that execute specific tasks
- Tool services — Dedicated microservices for tool execution (DB, API, files)
- Memory services — Centralized memory store accessible by all agents
- Configuration service — Dynamic agent configuration without redeployment
- Gateway service — API entry point with auth, rate limiting, request routing
- Clean interfaces — Defining contracts between components

## A1.3 Event-Driven Architecture for Agents (Lab)
- Why event-driven — Agents naturally produce and react to events
- Event types — Agent started, tool called, decision made, task completed, error occurred
- Event sourcing — Recording every agent action as an immutable event
- CQRS pattern — Separating command (actions) from query (reads) paths
- Event handlers — Triggering downstream actions based on events
- Event replay — Reconstructing agent state from event history
- Eventual consistency — Handling distributed state across agent services

## A1.4 Message Queues — Agent Communication via Redis/RabbitMQ/Azure Service Bus (Lab)
- Why message queues — Decoupled, reliable, asynchronous agent communication
- Redis Streams — Lightweight, fast, great for development and small-scale
- RabbitMQ — Feature-rich, routing, dead-letter queues, clustering
- Azure Service Bus — Enterprise-grade, sessions, transactions, auto-forwarding
- Amazon SQS — Managed, scalable, integrated with AWS ecosystem
- Queue patterns — Work queues, pub/sub, request-reply, priority queues
- Message schemas — Defining structured messages for agent communication
- Dead letter handling — Managing failed messages and retry logic
- Ordering guarantees — FIFO vs best-effort, partitioned ordering

## A1.5 API Gateway Design for Agent Endpoints (Lab)
- Why an API gateway — Single entry point, auth, rate limiting, routing
- Gateway responsibilities — Authentication, authorization, request validation, routing
- REST API design — Endpoints for agent invocation, status, history
- WebSocket support — Real-time streaming of agent responses
- Rate limiting — Per-user, per-tenant, per-endpoint limits
- Request/response transformation — Normalizing inputs and outputs
- Health endpoints — Liveness and readiness probes for agent services
- API versioning — Managing breaking changes in agent APIs

## A1.6 Stateless vs Stateful Agent Deployment
- Stateless agents — No local state, all state in external stores
- Stateful agents — In-memory state for active conversations
- Benefits of stateless — Easy scaling, no sticky sessions, simple failover
- When stateful is needed — Long-running agents, real-time streaming, WebSocket connections
- Externalizing state — Redis, databases, object storage for state persistence
- Session affinity — Routing returning users to the same instance when needed
- State migration — Moving state between instances during scaling events

## A1.7 Designing for Horizontal Scalability (Lab)
- Horizontal vs vertical scaling — Adding instances vs bigger machines
- Stateless design for scaling — Ensuring any instance can handle any request
- Load balancer configuration — Round-robin, least-connections, weighted routing
- Auto-scaling triggers — CPU, memory, queue depth, request latency, token throughput
- Database scaling — Read replicas, connection pooling, sharding
- Vector store scaling — Partitioning, replication, distributed search
- Bottleneck identification — Profiling to find the scaling constraint
- Capacity planning — Estimating resources for target concurrent users
