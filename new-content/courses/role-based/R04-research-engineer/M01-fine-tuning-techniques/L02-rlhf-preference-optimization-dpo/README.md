# RLHF & Preference Optimization (DPO)

## Overview

Implement Direct Preference Optimization (DPO) by showing models comparisons of "good" vs "bad" outputs to improve alignment, and understand the broader RLHF paradigm.

## Topics Covered

- Reinforcement Learning from Human Feedback (RLHF) concepts
- Direct Preference Optimization (DPO) methodology
- Creating "good" vs "bad" output comparison datasets
- Measuring alignment improvement after preference tuning

## Lab: Implementing DPO for Model Alignment

Implement DPO training to improve model alignment, with a detailed report showing before/after metric comparisons.

### Lab Objectives

- Create a preference comparison dataset with chosen/rejected pairs
- Implement DPO training using Hugging Face TRL
- Generate before/after metric comparison reports
- Analyze alignment improvement across different task types

## Key Takeaways

- DPO is simpler than full RLHF while achieving comparable alignment results
- Preference data (good vs bad pairs) is the key input for alignment tuning
- Measurable before/after comparison is essential to justify fine-tuning investment
