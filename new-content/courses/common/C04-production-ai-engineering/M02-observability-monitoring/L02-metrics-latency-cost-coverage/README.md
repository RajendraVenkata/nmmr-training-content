# L02: Metrics - Latency (P50/P95), Cost & Coverage

## Overview

This lesson teaches you how to define, collect, and interpret the metrics that matter for AI systems in production. You will learn why percentile-based latency measurements are essential, how to track cost per request, how to measure citation coverage for RAG systems, and how to establish quality baselines that detect degradation.

## Topics Covered

- Why P50/P95 latency matters more than averages for AI systems
- Cost per request tracking across model calls, embeddings, and infrastructure
- Citation coverage metrics for RAG systems (what percentage of responses are grounded)
- Defining quality baselines and thresholds for production AI
- Setting up metric collection and aggregation pipelines

## Key Takeaways

- Average latency hides the experience of your worst-affected users; P95 latency reveals the tail that often determines user satisfaction and SLO compliance
- Cost per request in AI systems has multiple components (model tokens, embedding calls, vector DB queries, compute time) and must be tracked holistically to manage spending
- Citation coverage measures what fraction of AI-generated claims are backed by retrieved sources, providing a quantifiable proxy for trustworthiness in RAG systems
- Quality baselines must be established before deployment so that degradation can be detected automatically rather than discovered through user complaints
- Metrics without thresholds and alerts are just dashboards; the value of metrics comes from defining what "good" looks like and being notified when reality diverges
