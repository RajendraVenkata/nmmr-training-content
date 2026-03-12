# M02: GPU & Inference Infrastructure

## Overview

Deep dive into the GPU-specific challenges of AI inference infrastructure. This module covers GPU memory management and compute batching, KV cache optimization for transformer models, and deploying production inference servers with VLLM and NVIDIA Triton.

## Prerequisites

- R03-M01: Serving & Orchestration
- Understanding of transformer model architecture basics
- Familiarity with GPU hardware concepts (VRAM, CUDA cores)

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | GPU Memory Management & Compute Batching | No | GPU memory allocation, fragmentation, dynamic batching, continuous batching |
| L02 | KV Cache Optimization | No | KV cache fundamentals, eviction strategies, paged attention, memory management |
| L03 | VLLM & Nvidia Triton Deployment | Yes | VLLM architecture, Triton for multi-model serving, performance tuning, monitoring |

## Key Tools

- NVIDIA GPUs and CUDA toolkit
- VLLM
- NVIDIA Triton Inference Server
- nvidia-smi and GPU profiling tools
- Prometheus for GPU metrics

## Learning Outcomes

- Manage GPU memory effectively for inference workloads, including batching strategies
- Understand and optimize KV cache behavior for transformer model serving
- Deploy models using VLLM and benchmark against baseline serving approaches
- Configure multi-model serving with NVIDIA Triton for production environments
