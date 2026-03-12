# L01: APIs, Services & Async Patterns

## Overview

This lesson covers how to design APIs and service architectures for AI-powered applications. You will learn REST API patterns for AI endpoints, asynchronous execution strategies for long-running model calls, and how to treat AI models as unreliable external services that require robust failure handling.

## Topics Covered

- REST APIs and JSON request/response patterns for AI services
- Asynchronous execution models for long-running AI calls
- Services and message queues for decoupling AI workloads
- Failure handling strategies (retries, timeouts, circuit breakers)
- Treating AI models as unreliable external services
- Designing for graceful degradation when model APIs are unavailable

## Key Takeaways

- AI endpoints require different API design considerations than traditional CRUD services, including streaming responses, longer timeouts, and non-deterministic outputs
- Asynchronous patterns with queues and callbacks are essential for production AI systems where model inference can take seconds to minutes
- Treating every AI model call as an unreliable external service call (with retries, fallbacks, and circuit breakers) is the foundation of resilient AI system design
- Failure handling is not optional in production AI systems; plan for model API outages, rate limits, and degraded responses from the start
