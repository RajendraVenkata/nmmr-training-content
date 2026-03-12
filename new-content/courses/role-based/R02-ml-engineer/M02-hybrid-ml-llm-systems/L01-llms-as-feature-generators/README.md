# L01: LLMs as Feature Generators

## Overview

Learn how to use LLMs to generate rich features for classical ML models. This lesson covers text-to-features pipelines, embedding-based feature extraction, and techniques for combining LLM-generated features with traditional feature engineering for improved model performance.

## Topics Covered

- Using LLMs to generate features for classical ML models
- Text-to-features pipelines: structured extraction from unstructured text
- Embedding-based features from LLM APIs
- Combining LLM features with traditional engineered features
- Cost and latency considerations for LLM-based feature generation

## Lab: Building a Hybrid Pipeline Where an LLM Generates Features for a Classification Model

Build an end-to-end pipeline where an LLM extracts structured features from unstructured text, which are then fed into a classical classification model alongside traditional features.

### Lab Objectives

- Design prompts that extract structured features from unstructured text inputs
- Build a feature generation pipeline that processes text through an LLM API
- Combine LLM-generated features with traditional features in a unified feature matrix
- Compare model performance with and without LLM-generated features

## Key Takeaways

- LLMs can extract nuanced features from unstructured text that traditional NLP techniques miss
- LLM-generated features complement, rather than replace, traditional feature engineering
- Cost management is critical: batch processing and caching reduce LLM API expenses for feature generation
- Embedding-based features are often more cost-effective than prompt-based extraction for high-volume pipelines
