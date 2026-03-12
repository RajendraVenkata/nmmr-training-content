# L02: Tokens, Context Windows & Tokenomics

## Overview

This lesson covers the practical mechanics of tokenization, context window management, and the economics of token usage. You will develop intuition for how text maps to tokens, understand the constraints of context windows, and learn to reason about the cost implications of different token types.

## Topics Covered

- What tokens are and how text is converted to token sequences
- Tokenizer algorithms: BPE, SentencePiece, and model-specific tokenizers
- Context window sizes across major models and their practical limits
- Output tokens vs reasoning tokens: what counts and what costs
- Token budgeting: balancing input context, instructions, and output space
- Practical token intuition: estimating token counts from text length
- Tokenomics: pricing models and cost optimization strategies

## Key Takeaways

- Tokens are not words -- a single word may be multiple tokens, and common phrases may be single tokens
- Context window size is a hard constraint that includes input, instructions, and output combined
- Reasoning tokens (used by models like o1) consume context budget without appearing in the output
- Developing token intuition (roughly 4 characters per token in English) is essential for cost estimation
- Token pricing varies significantly across providers and models, making cost optimization a practical skill
