# R04: Research Engineer Specialization

## Overview

Bridges the gap between academic papers and real-world products. This course explores model behavior, fine-tuning techniques, and evaluation science, equipping engineers to adapt and optimize models for production use cases.

## Prerequisites

- Beginner course track (B01-B10) completed
- Intermediate course track (I01-I03) completed
- Strong Python skills and experience with ML frameworks (PyTorch or similar)
- Understanding of transformer architectures and LLM fundamentals

## Target Role

Research Engineers operate at the intersection of applied research and engineering. They translate techniques from academic papers into production-ready implementations, conduct fine-tuning experiments, design rigorous evaluation frameworks, and optimize models for performance and safety. This role requires deep technical understanding of model internals and training methodologies.

## Modules

| Module | Name | Lessons | Key Topics |
|--------|------|---------|------------|
| M01 | Fine-Tuning Techniques | 3 | Supervised fine-tuning, RLHF & DPO, LoRA & QLoRA |
| M02 | Model Optimization | 3 | Knowledge distillation, evaluation science, safety tuning & alignment |

## Key Tools & Technologies

- PyTorch / Hugging Face Transformers
- PEFT (Parameter-Efficient Fine-Tuning) library
- TRL (Transformer Reinforcement Learning) library
- Weights & Biases / MLflow for experiment tracking
- Hugging Face Datasets and Evaluate libraries
- bitsandbytes for quantization
- DeepSpeed / FSDP for distributed training

## Learning Outcomes

- Perform supervised fine-tuning on language models with properly prepared datasets and training monitoring
- Implement preference optimization techniques (RLHF, DPO) to improve model alignment
- Apply parameter-efficient fine-tuning methods (LoRA, QLoRA) to reduce compute costs while preserving quality
- Distill large models into smaller, deployable student models with minimal performance loss
- Design and execute rigorous model evaluation pipelines with appropriate metrics and benchmarks
- Apply safety tuning and red-teaming strategies to improve model alignment and reduce harmful outputs
