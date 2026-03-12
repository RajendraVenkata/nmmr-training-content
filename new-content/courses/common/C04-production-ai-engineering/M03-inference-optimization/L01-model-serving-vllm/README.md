# L01: Model Serving with VLLM

## Overview

This lesson introduces VLLM as a high-performance inference engine for serving large language models. You will learn how to self-host open-source models, configure VLLM for high-throughput serving, and expose OpenAI-compatible API endpoints that can serve as drop-in replacements for hosted model APIs.

## Topics Covered

- What VLLM is and how it achieves high-throughput inference
- Self-hosting open-source models (Llama, Mistral, and others)
- Configuring VLLM for production serving (batching, parallelism, memory management)
- OpenAI-compatible API endpoints for seamless integration
- Comparing self-hosted serving costs versus API-based model access

## Lab: Deploying a Model with VLLM and Benchmarking Throughput

Deploy an open-source language model using VLLM, configure it for production use, and run systematic benchmarks to measure throughput, latency, and resource utilization under varying load conditions.

### Lab Objectives

- Install and configure VLLM to serve an open-source language model
- Launch a VLLM server with OpenAI-compatible API endpoints
- Send requests to the VLLM endpoint and verify correct responses
- Benchmark throughput (requests per second) and latency (P50/P95) under increasing concurrent load
- Compare serving performance metrics against direct API calls to a hosted model provider

## Key Takeaways

- VLLM uses PagedAttention and continuous batching to achieve significantly higher throughput than naive model serving approaches
- OpenAI-compatible endpoints mean that switching from a hosted API to self-hosted VLLM often requires only changing the base URL, with no code changes
- Self-hosting makes economic sense when request volume is high enough that API costs exceed the cost of GPU infrastructure, typically at thousands of requests per day or more
- Throughput and latency are inversely related in model serving; batching more requests improves throughput but increases per-request latency, requiring careful tuning based on SLO requirements
