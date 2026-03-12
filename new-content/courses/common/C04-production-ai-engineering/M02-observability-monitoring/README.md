# M02: Observability & Monitoring

## Overview

This module teaches you how to gain visibility into the behavior of AI systems in production. You will learn to instrument pipelines with tracing, define meaningful metrics, build monitoring dashboards, and systematically debug failures in agent-based systems.

## Prerequisites

- Completion of M01 (System Design for AI) or equivalent experience
- Working knowledge of AI pipelines (RAG, agents, tool calling)
- Familiarity with APIs and basic cloud deployment concepts

## Lessons

| Lesson | Name | Lab? | Key Topics |
|--------|------|------|------------|
| L01 | Tracing with LangFuse & LangSmith | Yes | What tracing is, instrumenting AI pipelines, viewing retrieval/reranking/LLM steps, debugging with traces |
| L02 | Metrics - Latency (P50/P95), Cost & Coverage | No | Why P50/P95 not averages, cost per request tracking, citation coverage metrics, quality baselines |
| L03 | Building Monitoring Dashboards | Yes | Dashboard design for AI, key metrics to display, alerting on quality degradation, user feedback integration |
| L04 | Debugging Agent Loops & Failures | No | Common agent failure modes, infinite loops, tool call failures, diagnosing issues via traces and spans |

## Key Tools

- LangFuse for open-source tracing
- LangSmith for LangChain ecosystem tracing
- Arize Phoenix for monitoring dashboards
- Prometheus and Grafana for metrics collection and visualization
- OpenTelemetry for standardized instrumentation

## Learning Outcomes

- Instrument AI pipelines with end-to-end tracing to see every step from retrieval through LLM response
- Define and track production-grade metrics including P50/P95 latency, cost per request, and citation coverage
- Build monitoring dashboards that surface quality degradation and integrate user feedback signals
- Systematically diagnose and resolve common agent failures including infinite loops and tool call errors
- Establish quality baselines and configure alerts that fire when system behavior degrades
