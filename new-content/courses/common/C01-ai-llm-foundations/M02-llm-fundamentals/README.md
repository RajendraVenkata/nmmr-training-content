# M02: LLM Fundamentals

## Overview

This module provides a deep understanding of how large language models work under the hood. You will learn about transformer architectures, tokenization mechanics, the full training lifecycle, and modern model architectures like Mixture of Experts -- building the conceptual foundation needed to use LLMs effectively.

## Prerequisites

- Basic understanding of machine learning concepts (helpful but not required)
- Completion of M01 or equivalent programming experience

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Transformer Architecture & Self-Attention | No | Self-attention mechanism, queries/keys/values, sequence processing |
| L02 | Tokens, Context Windows & Tokenomics | No | Tokenization, context limits, output vs reasoning tokens, token intuition |
| L03 | The Training Lifecycle | No | Pre-training, fine-tuning, knowledge cutoffs |
| L04 | Model Architectures (MoE & Sparse) | No | Mixture of Experts, sparse architectures, compute optimization |

## Key Tools

- Tokenizer visualization tools (tiktoken, Anthropic tokenizer)
- Model documentation (OpenAI, Anthropic, Meta)
- Transformer architecture diagrams and interactive visualizations

## Learning Outcomes

- Explain how self-attention allows transformers to process and relate tokens across a sequence
- Describe the role of queries, keys, and values in the attention mechanism
- Estimate token counts and manage context window budgets for different models
- Distinguish between output tokens and reasoning tokens and their cost implications
- Trace the full LLM training lifecycle from pre-training through fine-tuning
- Explain how Mixture of Experts architectures optimize computational resources
- Make informed model selection decisions based on architecture characteristics
