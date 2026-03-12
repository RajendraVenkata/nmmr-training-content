# L03: VLLM & Nvidia Triton Deployment

## Overview

Learn how to deploy production inference servers using VLLM for LLM serving and NVIDIA Triton for multi-model serving. This lesson covers architecture, configuration, performance tuning, and monitoring for both platforms.

## Topics Covered

- VLLM architecture and deployment for LLM serving
- NVIDIA Triton Inference Server for multi-model serving
- Performance tuning: batch size, concurrency, tensor parallelism
- Monitoring GPU utilization, throughput, and latency in production
- Comparing VLLM vs. Triton vs. baseline serving approaches

## Lab: Deploying Models with VLLM and Benchmarking Against Baseline Serving

Deploy an LLM using VLLM, configure it for production, and run comprehensive benchmarks comparing throughput, latency, and GPU utilization against a baseline serving approach.

### Lab Objectives

- Deploy an open-source LLM using VLLM with optimized configuration
- Configure VLLM features: continuous batching, paged attention, tensor parallelism
- Run load tests measuring throughput, latency percentiles, and GPU utilization
- Compare VLLM performance against a baseline HuggingFace Transformers serving setup

## Key Takeaways

- VLLM provides significant throughput improvements over naive serving through paged attention and continuous batching
- NVIDIA Triton excels at multi-model serving scenarios where different model types need to share GPU resources
- Performance tuning requires iterative benchmarking; default configurations are rarely optimal for specific workloads
- Monitoring GPU utilization alongside request metrics is essential for identifying bottlenecks and optimization opportunities
