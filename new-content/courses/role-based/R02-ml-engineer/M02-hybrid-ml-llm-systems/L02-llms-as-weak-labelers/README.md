# L02: LLMs as Weak Labelers

## Overview

Learn how to use LLMs to generate training labels at scale, replacing or augmenting expensive human annotation. This lesson covers noise-aware training techniques, label quality estimation, and integrating LLM-generated labels with active learning for efficient model development.

## Topics Covered

- Using LLMs to generate training labels at scale
- Noise-aware training techniques for handling label noise
- Label quality estimation and confidence scoring
- Active learning integration with LLM-generated labels
- Comparing LLM labels with human annotations: agreement metrics

## Lab: Implementing an LLM-Based Weak Labeling Pipeline with Quality Controls

Build a complete weak labeling pipeline that uses an LLM to label a large dataset, estimates label quality, filters noisy labels, and trains a model using noise-aware techniques.

### Lab Objectives

- Design labeling prompts that produce consistent, high-quality labels from an LLM
- Implement label quality estimation using confidence scoring and cross-validation
- Build a noise filtering pipeline that removes or down-weights low-confidence labels
- Train a classification model using noise-aware techniques on LLM-generated labels

## Key Takeaways

- LLM-based labeling can reduce annotation costs by 10-100x while maintaining acceptable quality
- Label noise from LLMs follows different patterns than human annotation noise; training techniques must adapt
- Quality estimation (confidence scoring, agreement metrics) is essential for trusting LLM-generated labels
- The combination of LLM weak labeling with targeted human annotation via active learning provides the best cost-quality balance
