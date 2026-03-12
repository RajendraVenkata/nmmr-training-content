# L02: Monitoring & Observability Layer

## Overview

Add full monitoring, observability, and CI/CD integration to the production-grade RAG system built in Part 1. This second part of the capstone focuses on operational excellence: dashboards, latency tracking, regression gates, and automated quality assurance.

## Topics Covered

- Adding full observability to a production RAG system
- Dashboard design for real-time system monitoring
- Latency tracking and performance profiling
- CI/CD integration with evaluation harnesses
- Regression gates and automated quality assurance

## Lab: Adding Monitoring, Observability, and CI/CD Eval Gates to the Capstone System (Capstone Part 2)

Extend the RAG system from Part 1 with production-grade observability, including monitoring dashboards, latency tracking, and a CI/CD pipeline that runs the evaluation harness as a deployment gate.

### Lab Objectives

- Instrument the RAG system with Prometheus metrics for latency, throughput, and quality
- Build Grafana dashboards showing real-time system health and quality trends
- Create a CI/CD pipeline that runs the evaluation harness on every code change
- Implement regression gates that block deployments when quality metrics drop below thresholds

## Key Takeaways

- Observability is not optional for production AI systems; it is a requirement for operational reliability
- CI/CD eval gates are the most effective guardrail against shipping quality regressions
- Dashboards should separate technical health metrics from AI quality metrics for different audiences
- The combination of evaluation harnesses + monitoring + regression gates creates a robust quality feedback loop
