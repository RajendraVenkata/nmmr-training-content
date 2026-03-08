# Course A8: Monitoring, Observability & Reliability

> **Make agentic systems observable and reliable** — Logs, metrics, traces with OpenTelemetry, LLM-specific monitoring, alerting, health checks, circuit breakers, graceful degradation, and disaster recovery.

### Goal: Build comprehensive observability and reliability for production agent systems

---

## A8.1 Observability Pillars for Agents — Logs, Metrics, Traces
- The three pillars — Logs (what happened), Metrics (how much), Traces (how long)
- Agent-specific challenges — Non-deterministic behavior, multi-step workflows, tool calls
- Structured logging — JSON logs with agent ID, step, tool, duration, tokens
- Key metrics — Latency, throughput, error rate, token usage, cost per request
- Distributed traces — Following a request through multiple agent services
- Correlation IDs — Linking logs, metrics, and traces for a single agent run
- Observability as a first-class concern — Instrumenting from day one, not as an afterthought

## A8.2 Distributed Tracing for Multi-Agent Systems (OpenTelemetry) (Lab)
- What is OpenTelemetry — Vendor-neutral observability framework
- OTEL SDK for Python — `opentelemetry-api`, `opentelemetry-sdk` installation
- Auto-instrumentation — Automatic tracing for HTTP, database, message queue calls
- Manual spans — Creating custom spans for agent steps, tool calls, LLM invocations
- Span attributes — Adding agent-specific metadata (model, tokens, cost, tool name)
- Context propagation — Passing trace context across service boundaries
- Exporters — Sending traces to Jaeger, Zipkin, Grafana Tempo, cloud providers
- Trace visualization — Reading waterfall diagrams to debug agent performance

## A8.3 LLM-Specific Metrics — Token Usage, Latency, Cost, Error Rates (Lab)
- Token metrics — Input tokens, output tokens, total tokens per request
- Latency metrics — Time-to-first-token (TTFT), tokens-per-second, total response time
- Cost metrics — Cost per request, cost per agent run, cost per user/tenant
- Error metrics — API errors, rate limit hits, timeout errors, content filter blocks
- Quality metrics — Hallucination rate, tool call accuracy, user satisfaction
- Model comparison metrics — Same queries across different models
- Aggregation — Per-minute, per-hour, per-day rollups for dashboards
- Alerting thresholds — Setting baselines and detecting anomalies

## A8.4 LangSmith / LangFuse for Agent Observability (Lab)
- LangSmith — LangChain's commercial observability platform
- LangFuse — Open-source alternative for LLM observability
- Trace capture — Automatic logging of LangChain/LangGraph agent runs
- Run comparison — Side-by-side comparison of agent executions
- Cost tracking — Automatic cost calculation per trace
- Evaluation — Running evaluators on production traces
- Feedback — Collecting user feedback on agent responses
- Datasets — Creating evaluation datasets from production data
- Self-hosted LangFuse — Running LangFuse on your own infrastructure

## A8.5 Alerting on Agent Failures, Hallucinations, and Anomalies
- Alert types — Critical (system down), Warning (degradation), Info (notable events)
- Error rate alerts — Spikes in LLM API errors, tool failures, parsing errors
- Latency alerts — Response times exceeding SLA thresholds
- Cost alerts — Unexpected cost spikes indicating runaway agents
- Quality alerts — Drops in evaluation scores or user satisfaction
- Anomaly detection — Statistical methods for detecting unusual agent behavior
- Alert routing — PagerDuty, Slack, email based on severity
- Alert fatigue prevention — Grouping, deduplication, escalation policies

## A8.6 Health Checks and Circuit Breakers (Lab)
- Liveness checks — Is the agent service process running
- Readiness checks — Can the agent service handle requests (LLM reachable, DB connected)
- Startup probes — Waiting for slow-starting agent services
- Circuit breaker pattern — Stopping calls to failing services
- Circuit breaker states — Closed (flowing), Open (blocked), Half-Open (testing)
- Circuit breaker for LLM APIs — Handling provider outages gracefully
- Implementation — `pybreaker`, `tenacity`, custom circuit breaker classes
- Monitoring circuit breaker state — Dashboards showing circuit health

## A8.7 Graceful Degradation — Fallback Strategies When LLM APIs Go Down
- Why degradation planning — LLM APIs have outages, rate limits, and slow periods
- Fallback hierarchy — Primary model → Secondary model → Cached response → Error message
- Provider failover — Automatic switching between Anthropic, OpenAI, Ollama
- Cached responses — Serving cached answers for common queries during outages
- Reduced functionality — Disabling non-essential tools during degraded operation
- User communication — Informing users about reduced capabilities
- Recovery detection — Automatically restoring full functionality when APIs recover

## A8.8 Disaster Recovery and Backup Strategies
- DR planning for agents — What to recover and in what order
- State backup — Regular snapshots of vector stores, agent state, conversation history
- Multi-region deployment — Active-passive or active-active across regions
- Database replication — Cross-region replication for critical agent data
- Configuration backup — Version-controlled agent configuration and prompts
- Recovery testing — Regular DR drills to verify recovery procedures
- RTO and RPO — Defining recovery time and data loss objectives
- Runbook creation — Step-by-step recovery procedures for common failure scenarios
