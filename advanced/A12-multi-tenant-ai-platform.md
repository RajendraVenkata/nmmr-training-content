# Course A12: Real-World Application — Multi-Tenant AI Platform

> **Build a SaaS agentic AI platform** — Tenant isolation, custom agent configuration, usage metering and billing, white-labeling, per-tenant rate limiting, and multi-region deployment.

### Goal: Build a multi-tenant platform that serves AI agents to multiple customers

---

## A12.1 Architecture for SaaS Agentic AI Platforms (Lab)
- Multi-tenant architecture — Shared infrastructure serving multiple customers
- Tenant isolation models — Shared-nothing, shared-database, shared-everything
- Platform layers — API gateway, tenant router, agent engine, data layer
- Control plane vs data plane — Managing tenants vs serving agent requests
- Onboarding flow — Tenant registration, configuration, provisioning
- Admin dashboard — Platform management, tenant overview, system health
- Technology choices — Kubernetes namespaces, database schemas, or separate instances
- Cost model — Platform operating costs vs per-tenant revenue

## A12.2 Tenant Isolation — Data, Models, Agents per Customer (Lab)
- Data isolation — Ensuring tenants cannot access each other's data
- Database isolation — Schema-per-tenant, database-per-tenant, row-level security
- Vector store isolation — Separate collections or namespaces per tenant
- Memory isolation — Per-tenant conversation and entity memory
- Model isolation — Tenant-specific model configurations and API keys
- Agent isolation — Custom agent definitions per tenant
- Network isolation — Tenant-specific VPCs or network policies
- Testing isolation — Automated testing to verify cross-tenant data leaks

## A12.3 Custom Agent Configuration per Tenant (Lab)
- Tenant configuration model — Schema for per-tenant agent customization
- Custom system prompts — Tenant-specific personas and instructions
- Custom tools — Per-tenant tool definitions and integrations
- Custom knowledge bases — Tenant-specific RAG data and embeddings
- Model selection — Per-tenant model preferences and fallbacks
- Guardrails — Tenant-specific content safety rules and filters
- Configuration UI — Self-service portal for tenant agent customization
- Configuration versioning — Tracking and rolling back configuration changes
- Hot reload — Applying configuration changes without downtime

## A12.4 Usage Metering and Billing (per Token, per Agent Call) (Lab)
- Metering strategy — What to measure (tokens, requests, tool calls, storage)
- Real-time metering — Counting usage as it happens, not after the fact
- Token tracking — Input tokens, output tokens, embedding tokens per tenant
- Metering pipeline — Event stream → Aggregation → Billing system
- Billing models — Pay-per-use, tiered pricing, flat rate, hybrid
- Usage dashboards — Self-service usage visibility for tenants
- Invoice generation — Automated billing based on metered usage
- Stripe/payment integration — Connecting metering to payment processing
- Free tier management — Rate limiting and feature gating for free tenants

## A12.5 White-Labeling and Custom Branding
- What is white-labeling — Tenants present the platform as their own product
- Custom domains — Per-tenant custom domain mapping
- Branding assets — Logos, colors, fonts per tenant
- Custom UI themes — Dynamic theming based on tenant configuration
- Email templates — Branded email notifications per tenant
- API customization — Tenant-specific API documentation and SDKs
- Embedding — Widget/iframe embedding for tenant websites

## A12.6 API Rate Limiting per Tenant (Lab)
- Why per-tenant limits — Preventing one tenant from consuming all resources
- Tier-based limits — Different rate limits for different pricing tiers
- Token-based limits — Monthly token budgets per tenant
- Request-based limits — Requests per minute/hour per tenant
- Concurrent request limits — Maximum parallel agent runs per tenant
- Burst handling — Short-term bursts vs sustained high usage
- Limit enforcement — Redis-based distributed rate limiting
- Limit communication — Headers, dashboards, and alerts for tenants

## A12.7 Multi-Region Deployment for Global Availability (Lab)
- Why multi-region — Low latency globally, compliance, disaster recovery
- Active-active vs active-passive — Trade-offs between complexity and availability
- Data replication — Cross-region database replication strategies
- Tenant routing — Directing tenants to the nearest region
- Data residency compliance — Keeping tenant data in required regions
- Failover strategies — Automatic failover when a region goes down
- Global load balancing — DNS-based and anycast routing
- Deployment coordination — Rolling out changes across regions safely
