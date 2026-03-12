# L02: RLHF & Preference Optimization (DPO)

## Overview

Explore how Reinforcement Learning from Human Feedback and Direct Preference Optimization are used to align model outputs with human preferences. This lesson covers the theory behind preference-based training, practical implementation of DPO, and how to measure alignment improvements.

## Topics Covered

- Reinforcement Learning from Human Feedback (RLHF) concepts and pipeline
- Direct Preference Optimization (DPO) as a simpler alternative to RLHF
- Constructing preference datasets with "good" vs "bad" output comparisons
- Alignment improvement measurement and evaluation
- Trade-offs between RLHF and DPO approaches
- Common pitfalls in preference optimization

## Lab: Implementing DPO for Model Alignment

Implement Direct Preference Optimization to improve a model's alignment using a curated preference dataset. Compare model behavior before and after DPO training using quantitative metrics.

### Lab Objectives

- Construct a preference dataset with chosen and rejected response pairs
- Configure and run a DPO training pipeline using the TRL library
- Measure alignment improvement with before/after metric comparisons
- Analyze cases where DPO succeeds and where it struggles

## Key Takeaways

- RLHF uses a separate reward model, while DPO directly optimizes on preference pairs, making it simpler to implement
- Preference data quality is critical: ambiguous or inconsistent preferences degrade alignment
- DPO is often sufficient for many alignment tasks and avoids the complexity of training a reward model
- Alignment improvements should be measured across multiple dimensions, not just a single metric
