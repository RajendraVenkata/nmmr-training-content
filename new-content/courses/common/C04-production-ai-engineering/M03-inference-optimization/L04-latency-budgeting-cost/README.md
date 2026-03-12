# L04: Latency Budgeting & Cost Management

## Overview

This lesson teaches you how to decompose the end-to-end latency of an AI system into measurable components and how to analyze cost on a per-request basis. You will learn to create latency budgets that allocate time to each pipeline stage, measure time-to-first-token as a user experience metric, and implement strategies to optimize the economics of AI inference at scale.

## Topics Covered

- Decomposing end-to-end latency into pipeline stage budgets
- Time-to-first-token (TTFT) measurement and its impact on perceived performance
- Cost per 1K requests analysis across all system components
- Optimization strategies for reducing latency and cost simultaneously
- Building a latency and cost model for capacity planning

## Key Takeaways

- End-to-end latency in an AI system includes network, retrieval, embedding, reranking, prompt construction, model inference, and post-processing; each stage needs an explicit budget to identify optimization opportunities
- Time-to-first-token is the most important latency metric for user-facing AI applications because it determines how quickly users perceive the system as responsive, even before the full response is generated
- Cost per request must include all components: input/output tokens, embedding API calls, vector database queries, compute time, and infrastructure overhead; tracking only model token costs gives an incomplete picture
- The most effective cost optimization strategies often involve architectural changes (caching, prompt compression, model selection) rather than infrastructure tuning
- Latency and cost optimization frequently involve trade-offs; faster responses may require more expensive infrastructure, while cheaper models may increase latency or reduce quality, making explicit budgeting essential
