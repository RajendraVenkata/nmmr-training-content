# L03: Deterministic Validation & LLM-as-Judge

## Overview

This lesson addresses the fundamental challenge of validating non-deterministic AI outputs. You will learn how to combine programmatic checks (format validation, keyword presence, length constraints) with LLM-as-judge techniques (using one LLM to evaluate the output of another) to build comprehensive validation pipelines that catch quality issues before responses reach users.

## Topics Covered

- Using LLMs to judge non-deterministic outputs from other LLMs
- Programmatic (deterministic) checks: format, structure, length, keyword validation
- Validation before user delivery: pre-response quality gates
- Combining programmatic and LLM-based validation into unified pipelines
- Designing effective judge prompts and scoring rubrics

## Key Takeaways

- Non-deterministic AI outputs cannot be validated with traditional assertion-based testing alone; LLM-as-judge provides a scalable way to evaluate open-ended responses for relevance, accuracy, and tone
- Programmatic checks should always run first as they are fast, deterministic, and cheap; reserve LLM-as-judge for aspects that cannot be checked programmatically, such as factual accuracy and response helpfulness
- LLM-as-judge is not a silver bullet; judge models have their own biases and failure modes, so judge prompts must be carefully designed with clear scoring rubrics and calibrated against human evaluations
- Combining both approaches creates a layered validation pipeline: deterministic checks filter out structurally invalid responses quickly, while LLM-based evaluation catches subtler quality issues in the remaining responses
- Pre-delivery validation (checking responses before sending them to users) adds latency but can prevent harmful, inaccurate, or low-quality responses from ever reaching production users
