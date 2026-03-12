# L03: Cloud Infrastructure Basics

## Overview

This lesson provides a practical introduction to cloud infrastructure for AI workloads. You will learn how to evaluate cloud providers, select appropriate compute resources (CPU vs GPU), choose storage solutions for models and data, and configure networking for AI service communication.

## Topics Covered

- Overview of major cloud providers for AI (AWS, Azure, GCP)
- Compute selection: CPU vs GPU instances, spot/preemptible instances for cost savings
- Storage options for models, embeddings, and vector databases
- Networking fundamentals for AI services (VPCs, load balancers, API gateways)
- Cost comparison across providers for common AI workloads

## Key Takeaways

- Cloud provider selection for AI workloads depends on GPU availability, pricing models, and existing ecosystem integration rather than brand preference
- GPU instances are expensive; understanding when you actually need GPU compute versus when CPU is sufficient can reduce costs by 10x or more
- Spot and preemptible instances can cut GPU costs by 60-90% for fault-tolerant AI workloads like batch inference and training
- Storage architecture for AI systems must account for large model files (gigabytes), fast-access vector stores, and cost-effective archival of training data
- Networking configuration (especially latency between compute and storage) can be the hidden bottleneck in AI system performance
