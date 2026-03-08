# Course A13: Advanced Capstone Project

> **Build and deploy a production-grade agentic AI platform on the cloud** — Multi-agent system on Kubernetes, scalable architecture, production RAG, full observability, security, CI/CD, cost optimization, and load testing.

### Goal: Deliver a production-ready, cloud-deployed, scalable agentic AI system demonstrating all advanced skills

---

## A13.1 Project: Production Agentic AI Platform on Cloud (Lab)
- Project overview — A complete production-grade agentic AI platform deployed on cloud infrastructure
- Cloud provider choice — Azure, AWS, or GCP (student selects their preferred platform)
- Architecture: Multi-agent system — Specialized agents for different tasks deployed as microservices
- Architecture: Kubernetes deployment — All services running on managed Kubernetes (AKS/EKS/GKE)
- Architecture: Message queues — Agent-to-agent communication via Service Bus/SQS/Pub/Sub
- Architecture: Auto-scaling — Horizontal pod autoscaler with custom metrics (queue depth, latency)
- Feature: Production RAG — Hybrid search with re-ranking using cloud search services
- Feature: Full observability — OpenTelemetry tracing, Prometheus metrics, Grafana dashboards
- Feature: Security — Prompt injection defense, PII redaction, secrets management, audit logging
- Feature: CI/CD pipeline — GitHub Actions for build, test, and deploy with staging and production environments
- Feature: Cost optimization — Intelligent model routing (cheap models for simple tasks, premium for complex)
- Feature: Caching — Semantic caching for repeated queries, tool result caching
- Feature: Rate limiting — Per-user and per-endpoint rate limiting with graceful degradation
- Feature: Health checks — Liveness, readiness, and startup probes for all services
- Feature: Circuit breakers — Automatic failover when LLM providers go down
- Testing: Automated test suite — Unit, integration, and end-to-end tests in CI
- Testing: LLM-as-judge evaluation — Automated quality scoring on evaluation datasets
- Testing: Load testing — Simulating 100+ concurrent users with k6 or Locust
- Step-by-step build — Guided walkthrough building each component over multiple sessions
- Deliverables — Working system, architecture documentation, runbook, cost analysis
- Stretch goals — Multi-tenant support, analytics dashboard, mobile API, webhook integrations
