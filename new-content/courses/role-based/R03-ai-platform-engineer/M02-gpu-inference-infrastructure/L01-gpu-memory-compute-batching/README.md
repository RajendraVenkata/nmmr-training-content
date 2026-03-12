# L01: GPU Memory Management & Compute Batching

## Overview

Learn how GPU memory allocation works for AI inference and how batching strategies maximize GPU utilization. This lesson covers memory fragmentation issues, dynamic batching, and continuous batching techniques that are essential for efficient model serving.

## Topics Covered

- GPU memory allocation for inference workloads
- Memory fragmentation causes and mitigation strategies
- Dynamic batching: grouping requests for efficient GPU utilization
- Continuous batching: processing requests as they arrive without waiting for batch fill
- Memory-efficient inference techniques for large models

## Key Takeaways

- GPU memory is the primary bottleneck for inference; understanding allocation patterns is critical
- Memory fragmentation can reduce effective GPU memory by 20-40% without proper management
- Dynamic batching increases throughput but adds latency; the batch window timeout is the key trade-off
- Continuous batching eliminates the latency penalty of dynamic batching by processing at the token level
- Memory-efficient inference techniques (gradient checkpointing, offloading) enable serving larger models on smaller GPUs
