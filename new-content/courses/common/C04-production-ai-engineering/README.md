# C04: Production AI Engineering

## Overview

This course bridges the gap between hobbyist AI projects and enterprise-grade AI systems. You will learn how to design, deploy, observe, optimize, and continuously deliver AI applications that are reliable, scalable, and cost-effective in production environments.

## Prerequisites

- Proficiency in Python and basic software engineering practices
- Familiarity with LLM APIs (OpenAI, Anthropic, or similar)
- Understanding of RAG pipelines and AI agents (C02 or equivalent)
- Basic command-line and Git proficiency
- Exposure to cloud platforms (any provider) is helpful but not required

## Modules

| Module | Name | Lessons | Key Topics |
|--------|------|---------|------------|
| M01 | System Design for AI | 4 | APIs, Docker, cloud infrastructure, scaling under load |
| M02 | Observability & Monitoring | 4 | Tracing, latency/cost metrics, dashboards, debugging agent failures |
| M03 | Inference Optimization | 4 | VLLM serving, quantization, speculative decoding, latency budgeting |
| M04 | CI/CD for AI Systems | 3 | AI-aware pipelines, eval-gated deployments, LLM-as-judge validation |

## Key Tools & Technologies

- Docker & container orchestration
- VLLM for model serving
- LangFuse & LangSmith for tracing
- Arize Phoenix for monitoring dashboards
- GGUF quantization tooling
- GitHub Actions / CI/CD platforms
- Cloud providers (AWS, Azure, GCP)
- Prometheus, Grafana (metrics and alerting)

## Learning Outcomes

- Design robust system architectures that treat AI models as unreliable external services
- Containerize and deploy AI applications using Docker and cloud infrastructure
- Instrument AI pipelines with end-to-end tracing and build monitoring dashboards
- Define and track production metrics including P50/P95 latency, cost per request, and quality baselines
- Optimize inference performance using VLLM, quantization, and speculative decoding
- Build CI/CD pipelines that incorporate evaluation steps and quality-gated deployments
- Diagnose and fix common production failures including agent loops and tool call errors
- Budget latency and cost across the full request lifecycle of an AI system
