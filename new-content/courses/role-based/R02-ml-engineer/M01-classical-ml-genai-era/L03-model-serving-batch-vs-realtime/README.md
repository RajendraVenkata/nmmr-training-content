# L03: Model Serving - Batch vs Real-Time

## Overview

Understand when to use batch processing versus real-time inference for model serving, and learn the architectural patterns behind each approach. This lesson covers latency requirements, throughput optimization, and choosing the right serving strategy for different use cases.

## Topics Covered

- When to use batch processing vs. real-time inference
- Latency requirements and SLA design for model serving
- Throughput optimization techniques
- Serving architecture patterns: REST APIs, gRPC, message queues
- Cost considerations for different serving strategies

## Key Takeaways

- The choice between batch and real-time serving is driven by latency requirements and cost constraints
- Batch serving is more cost-effective for use cases that can tolerate minutes-to-hours of latency
- Real-time serving requires careful attention to model loading, warm-up, and scaling strategies
- Many production systems use a hybrid approach: real-time for user-facing requests, batch for analytics and reporting
- Model serving architecture should be designed for the 99th percentile latency, not the average
