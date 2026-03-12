# L03: Speculative Decoding & KV Cache

## Overview

This lesson explores advanced inference optimization techniques that accelerate LLM generation without sacrificing output quality. You will learn how speculative decoding uses a smaller draft model to speed up generation, how KV cache reuse eliminates redundant computation, and how memory management and compute batching further improve inference efficiency.

## Topics Covered

- How speculative decoding works (draft model + verification)
- KV cache: what it stores, why reuse matters, and cache management strategies
- Memory management for inference (GPU memory allocation, cache eviction policies)
- Compute batching techniques for improved throughput
- When each optimization technique provides the most benefit

## Key Takeaways

- Speculative decoding uses a small, fast draft model to generate candidate tokens that the larger target model verifies in parallel, achieving speedups of 2-3x without any change in output quality
- The KV cache stores previously computed key-value attention states so they do not need to be recomputed for each new token, and managing this cache efficiently is critical for serving long sequences
- KV cache reuse across requests with shared prefixes (such as system prompts) can significantly reduce time-to-first-token for workloads with common prompt structures
- Memory management is the central challenge of inference optimization; GPU memory must be carefully budgeted between model weights, KV cache, and batch buffers
- These optimizations are complementary: speculative decoding improves generation speed, KV cache reuse reduces redundant computation, and batching improves hardware utilization, and they can be combined for maximum effect
