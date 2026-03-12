# L02: Vector Indexing Strategies

## Overview

Explore the major vector indexing methods used in production search systems, including HNSW, IVF, and Product Quantization. This lesson covers how to tune indices for the right balance of recall and latency, and strategies for scaling vector search to large corpora through sharding.

## Topics Covered

- HNSW (Hierarchical Navigable Small World) graphs
- IVF (Inverted File Index) for partitioned search
- PQ (Product Quantization) for memory-efficient indexing
- Tuning indices for recall vs latency trade-offs
- Scaling vector search with sharding strategies
- Choosing the right index type for different workloads

## Lab: Comparing Vector Indexing Strategies

Build and benchmark different vector index types on the same corpus, tuning parameters to find the optimal recall-latency trade-off for different use case requirements.

### Lab Objectives

- Build HNSW, IVF, and PQ indices on a shared embedding corpus
- Tune index parameters (ef_construction, nprobe, m) and measure their impact
- Plot recall-latency curves for each index configuration
- Recommend index configurations for different production scenarios (high-recall vs low-latency)

## Key Takeaways

- HNSW provides excellent recall at moderate latency and is the most common choice for production systems
- IVF is faster for very large corpora but requires careful tuning of the number of clusters and probes
- Product Quantization dramatically reduces memory footprint but trades off some recall accuracy
- Index choice should be driven by the specific recall, latency, and memory constraints of the production environment
