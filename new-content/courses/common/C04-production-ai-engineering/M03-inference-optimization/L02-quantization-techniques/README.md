# L02: Quantization Techniques (GGUF, Q4/Q5)

## Overview

This lesson covers model quantization as a practical technique for reducing the memory footprint and improving the inference speed of large language models. You will learn what quantization is, how the GGUF format works, and how to evaluate the trade-offs between different quantization levels (Q4, Q5, Q8) in terms of quality, speed, and memory usage.

## Topics Covered

- What quantization is and why it matters for deployment
- The GGUF format and its role in the quantization ecosystem
- Q4 vs Q5 vs Q8: quality, speed, and memory trade-offs
- Memory savings from quantization and implications for hardware requirements
- Speed improvements and when quantization enables new deployment scenarios

## Lab: Quantizing a Model and Comparing Quality vs Speed vs Memory Trade-offs

Quantize the same base model at multiple quantization levels and run systematic comparisons to measure the impact on output quality, inference speed, and memory consumption.

### Lab Objectives

- Use llama.cpp or equivalent tooling to quantize a model at Q4, Q5, and Q8 levels
- Measure memory consumption for each quantization level and compare to the full-precision baseline
- Benchmark inference speed (tokens per second) across all quantization levels
- Evaluate output quality by running a standardized prompt set and comparing responses across quantization levels
- Create a trade-off analysis table that maps quantization level to quality, speed, and memory for informed deployment decisions

## Key Takeaways

- Quantization reduces model precision (from 16-bit to 4-bit or 5-bit) to dramatically cut memory usage, often enabling models to run on hardware that could not support them at full precision
- Q4 quantization typically reduces memory by approximately 75% compared to FP16, with measurable but often acceptable quality degradation for many use cases
- Q5 offers a strong middle ground, retaining more quality than Q4 while still providing substantial memory savings
- The quality impact of quantization is task-dependent: factual recall and reasoning tasks degrade more than creative text generation, so evaluation must be done on your specific use case
- GGUF has emerged as the standard format for quantized model distribution, with broad tooling support across inference engines
