# L01: Transformer Architecture & Self-Attention

## Overview

This lesson explains the transformer architecture that powers all modern large language models. You will learn how self-attention works, what queries, keys, and values represent, and how transformers process sequences of tokens to generate coherent outputs.

## Topics Covered

- The transformer architecture: encoder-decoder and decoder-only models
- Self-attention mechanism and why it revolutionized NLP
- Queries, keys, and values: intuition and mechanics
- Multi-head attention and parallel processing
- Positional encoding and sequence order awareness
- Feed-forward layers and layer normalization
- How transformers process input sequences to produce predictions

## Key Takeaways

- Self-attention allows each token to attend to every other token, enabling long-range dependency capture
- Queries, keys, and values are learned projections that determine how tokens relate to each other
- Multi-head attention lets the model learn different types of relationships simultaneously
- Understanding transformer internals helps you predict model behavior and debug unexpected outputs
- Decoder-only architectures (GPT-style) are the dominant design for modern generative LLMs
