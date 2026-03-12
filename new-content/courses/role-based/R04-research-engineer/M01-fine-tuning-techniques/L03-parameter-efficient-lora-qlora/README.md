# Parameter-Efficient Methods - LoRA & QLoRA

## Overview

Master parameter-efficient fine-tuning with LoRA and QLoRA, which enable fine-tuning large models at a fraction of the compute cost by training only small adapter layers rather than all parameters.

## Topics Covered

- Why full fine-tuning is expensive and often unnecessary
- LoRA adapter mechanism and how it works
- QLoRA: quantized LoRA for further memory efficiency
- Quality preservation with fewer trainable parameters

## Lab: Fine-Tuning with LoRA/QLoRA

Fine-tune a model using both LoRA and QLoRA, comparing memory savings and quality retention across approaches.

### Lab Objectives

- Fine-tune a model using LoRA adapters
- Apply QLoRA for reduced memory fine-tuning
- Compare memory usage, training time, and quality across methods
- Measure quality retention vs compute savings trade-offs

## Key Takeaways

- LoRA trains only ~0.1-1% of parameters while achieving near-full fine-tuning quality
- QLoRA enables fine-tuning on consumer GPUs through quantization
- Parameter-efficient methods make fine-tuning accessible without expensive infrastructure
