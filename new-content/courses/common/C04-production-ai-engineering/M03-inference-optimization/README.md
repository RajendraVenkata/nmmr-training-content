# M03: Inference Optimization

## Overview

This module focuses on making AI inference faster, cheaper, and more efficient. You will learn to self-host models with VLLM, apply quantization to reduce resource requirements, understand advanced decoding strategies, and budget latency and cost across the full request lifecycle.

## Prerequisites

- Completion of M01 and M02, or equivalent production AI experience
- Understanding of how LLMs generate text (token-by-token decoding)
- Familiarity with GPU compute concepts (helpful but not required)
- Docker proficiency from M01

## Lessons

| Lesson | Name | Lab? | Key Topics |
|--------|------|------|------------|
| L01 | Model Serving with VLLM | Yes | What VLLM is, self-hosting models, high-throughput serving, OpenAI-compatible API endpoints |
| L02 | Quantization Techniques (GGUF, Q4/Q5) | Yes | What quantization is, GGUF format, Q4 vs Q5 trade-offs, memory savings, speed improvements |
| L03 | Speculative Decoding & KV Cache | No | How speculative decoding works, KV cache reuse, memory management, compute batching |
| L04 | Latency Budgeting & Cost Management | No | Decomposing end-to-end latency, time-to-first-token, cost per 1K requests, optimization strategies |

## Key Tools

- VLLM for high-throughput model serving
- llama.cpp and GGUF tooling for quantization
- NVIDIA GPU profiling tools
- Benchmarking utilities (throughput, latency measurement)
- Cost tracking and analysis tools

## Learning Outcomes

- Deploy and serve open-source models using VLLM with OpenAI-compatible API endpoints
- Apply quantization techniques to reduce model memory footprint while managing quality trade-offs
- Understand speculative decoding and KV cache optimization strategies for faster inference
- Decompose end-to-end latency into measurable components and build latency budgets
- Analyze cost per request and implement strategies to optimize inference economics at scale
