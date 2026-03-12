# M01: Fine-Tuning Techniques

## Overview

Covers the core fine-tuning methodologies used to adapt language models for specific tasks and behaviors. This module progresses from supervised fine-tuning through preference optimization to parameter-efficient methods, providing hands-on experience with each approach.

## Prerequisites

- R04 course prerequisites (B01-B10, I01-I03 completed)
- Experience with PyTorch and Hugging Face Transformers
- Understanding of transformer architecture fundamentals
- Familiarity with training loops and loss functions

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Supervised Fine-Tuning (SFT) | Yes | Dataset preparation, training procedures, monitoring training curves, when to use SFT over prompting |
| L02 | RLHF & Preference Optimization (DPO) | Yes | Reinforcement Learning from Human Feedback, Direct Preference Optimization, alignment improvement |
| L03 | Parameter-Efficient Methods (LoRA & QLoRA) | Yes | LoRA adapters, QLoRA quantized fine-tuning, parameter efficiency, quality preservation |

## Key Tools

- Hugging Face Transformers and Datasets
- TRL (Transformer Reinforcement Learning) library
- PEFT (Parameter-Efficient Fine-Tuning) library
- bitsandbytes for quantization
- Weights & Biases for experiment tracking

## Learning Outcomes

- Prepare high-quality datasets for supervised fine-tuning with 2,000-10,000 examples
- Execute SFT training with proper monitoring of training curves and convergence
- Implement DPO to align model outputs with human preferences using good vs bad comparisons
- Apply LoRA and QLoRA to fine-tune models efficiently with minimal compute resources
- Evaluate trade-offs between full fine-tuning, parameter-efficient methods, and prompt engineering
