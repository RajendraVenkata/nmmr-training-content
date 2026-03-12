# M03: Inference Optimization at Scale

## Overview

Master advanced techniques for optimizing AI inference cost and performance at scale. This module covers model quantization, speculative decoding for faster generation, and comprehensive cost optimization and performance tuning strategies for production inference systems.

## Prerequisites

- R03-M01: Serving & Orchestration
- R03-M02: GPU & Inference Infrastructure
- Understanding of model architecture and weight representation

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Quantization Deep Dive | Yes | Weight quantization, GGUF formats, INT4/INT8, quality-performance trade-offs |
| L02 | Speculative Decoding | No | Draft-verify paradigm, speedup analysis, when to use speculative decoding |
| L03 | Cost Optimization & Performance Tuning | No | Cost per token analysis, batch size optimization, model routing, capacity planning |

## Key Tools

- llama.cpp / GGUF tools
- bitsandbytes / AutoGPTQ
- VLLM with quantized models
- GPU profiling tools (Nsight Systems, nvidia-smi)
- Cost analysis spreadsheets and calculators

## Learning Outcomes

- Apply different quantization techniques (INT4, INT8, GGUF) and measure their impact on quality and performance
- Understand speculative decoding and identify workloads where it provides meaningful speedups
- Perform cost-per-token analysis and optimize inference costs through model routing and batch size tuning
- Conduct capacity planning for inference infrastructure based on traffic patterns and SLO requirements
