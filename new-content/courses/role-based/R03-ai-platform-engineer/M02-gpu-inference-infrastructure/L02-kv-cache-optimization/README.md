# L02: KV Cache Optimization

## Overview

Understand the KV (key-value) cache mechanism in transformer models and learn optimization strategies that reduce memory usage while maintaining performance. This lesson covers cache eviction strategies, paged attention, and memory management techniques for long-sequence inference.

## Topics Covered

- What KV cache is and why it matters for inference performance
- Cache eviction strategies for managing memory under pressure
- Paged attention: virtual memory concepts applied to KV cache
- Memory management for long-sequence inference
- Trade-offs between cache size, throughput, and maximum sequence length

## Key Takeaways

- The KV cache stores previously computed attention keys and values, avoiding recomputation and enabling fast autoregressive generation
- KV cache memory grows linearly with sequence length and batch size, often becoming the dominant memory consumer
- Paged attention (used by VLLM) applies virtual memory concepts to KV cache, reducing fragmentation and enabling larger batches
- Cache eviction strategies must balance memory savings against generation quality degradation
- Understanding KV cache behavior is essential for capacity planning and optimizing concurrent request handling
