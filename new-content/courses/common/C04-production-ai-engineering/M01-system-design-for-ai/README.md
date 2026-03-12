# M01: System Design for AI

## Overview

This module covers the architectural foundations needed to build production-grade AI systems. You will learn how to design APIs, containerize applications, select cloud infrastructure, and scale AI services to handle real-world traffic.

## Prerequisites

- Python proficiency and basic web development concepts
- Familiarity with HTTP, REST APIs, and JSON
- Command-line proficiency (terminal, shell basics)
- Understanding of LLM APIs from prior coursework (C01 or equivalent)

## Lessons

| Lesson | Name | Lab? | Key Topics |
|--------|------|------|------------|
| L01 | APIs, Services & Async Patterns | No | REST APIs, JSON patterns, async execution, queues, failure handling, AI models as unreliable services |
| L02 | Docker & Containerization for AI | Yes | Docker fundamentals, containerizing AI apps, multi-stage builds, environment reproducibility |
| L03 | Cloud Infrastructure Basics | No | Cloud providers for AI, compute selection, storage options, networking for AI services |
| L04 | Scaling AI Systems Under Load | No | Autoscaling strategies, load balancing, concurrent requests, SLOs for AI systems |

## Key Tools

- Docker & Docker Compose
- FastAPI / Flask for API development
- Cloud provider CLIs (AWS, Azure, GCP)
- Message queues (Redis, RabbitMQ, or cloud-native options)
- Load testing tools (Locust, k6)

## Learning Outcomes

- Design RESTful APIs that properly handle the non-deterministic nature of AI model responses
- Treat AI models as unreliable external services with appropriate retry logic and fallback strategies
- Containerize AI applications using Docker with optimized multi-stage builds
- Evaluate and select appropriate cloud compute, storage, and networking resources for AI workloads
- Design autoscaling strategies and define SLOs for AI-powered services
