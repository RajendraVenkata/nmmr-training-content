# L02: Speculative Decoding

## Overview

Learn how speculative decoding accelerates LLM inference by using a fast draft model to propose tokens that are then verified by the full model in parallel. This lesson covers the draft-verify paradigm, speedup analysis, and guidance on when speculative decoding is most effective.

## Topics Covered

- How speculative decoding works: the draft-verify paradigm
- Draft model selection and training considerations
- Speedup analysis: theoretical bounds and practical performance
- When speculative decoding provides meaningful benefits
- Integration with existing serving infrastructure

## Key Takeaways

- Speculative decoding uses a small, fast draft model to propose multiple tokens, which the full model verifies in a single forward pass
- Speedups of 2-3x are typical, but depend on the acceptance rate of draft tokens
- Speculative decoding works best when the draft model closely matches the target model's distribution
- The technique is most effective for long generation tasks where autoregressive decoding dominates total latency
- Speculative decoding does not change the output distribution of the target model; it only changes the speed of generation
