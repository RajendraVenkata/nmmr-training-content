# L03: Parameter-Efficient Methods (LoRA & QLoRA)

## Overview

Learn why full fine-tuning is often prohibitively expensive and how parameter-efficient methods like LoRA and QLoRA enable fine-tuning with a fraction of the compute. This lesson covers the theory behind low-rank adaptation, quantized training, and how to preserve model quality while dramatically reducing resource requirements.

## Topics Covered

- Why full fine-tuning is expensive and often unnecessary
- LoRA (Low-Rank Adaptation) architecture and adapters
- QLoRA (Quantized LoRA) for further compute reduction
- Parameter efficiency metrics and trade-offs
- Quality preservation strategies during efficient fine-tuning
- Merging adapters and deploying fine-tuned models

## Lab: Fine-Tuning with LoRA/QLoRA and Measuring Quality Retention

Fine-tune a language model using LoRA and QLoRA methods, then benchmark the resulting model against a full fine-tuning baseline to quantify the compute savings versus quality trade-off.

### Lab Objectives

- Configure and execute a LoRA fine-tuning run with appropriate rank and alpha settings
- Apply QLoRA with 4-bit quantization for memory-efficient training
- Benchmark quality retention compared to full fine-tuning on the same task
- Measure and report compute savings (memory, time, cost) versus quality delta

## Key Takeaways

- LoRA fine-tunes only a small number of additional parameters (often less than 1% of the model), drastically reducing memory and compute
- QLoRA combines quantization with LoRA to enable fine-tuning of large models on consumer-grade hardware
- Quality retention is typically 95-99% of full fine-tuning for most downstream tasks
- Adapter rank and alpha are the key hyperparameters; higher rank captures more task-specific information but costs more
