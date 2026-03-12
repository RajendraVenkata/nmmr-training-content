# L04: Model Architectures (MoE & Sparse)

## Overview

This lesson explores advanced model architectures that go beyond standard dense transformers. You will learn how Mixture of Experts (MoE) and sparse architectures achieve better performance per compute dollar, and understand how these designs influence model selection decisions for production applications.

## Topics Covered

- Dense vs sparse model architectures
- Mixture of Experts (MoE): routers, expert networks, and gating mechanisms
- How MoE models activate only a subset of parameters per token
- Computational efficiency gains from sparse activation
- Trade-offs: model size on disk vs active parameters during inference
- Real-world MoE models: Mixtral, GPT-4 (rumored), and others
- Implications for model selection, hosting, and cost optimization

## Key Takeaways

- MoE models can have many total parameters but only activate a fraction per forward pass
- Sparse architectures provide a way to scale model capacity without proportionally scaling compute
- The router component determines which experts handle each token, making routing quality critical
- Understanding MoE trade-offs helps you choose between dense and sparse models for specific workloads
- Model architecture knowledge informs decisions about self-hosting vs API usage and cost planning
