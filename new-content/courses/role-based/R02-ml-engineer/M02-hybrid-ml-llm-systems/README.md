# M02: Hybrid ML-LLM Systems

## Overview

Learn how to integrate LLMs into classical ML workflows as powerful components. This module covers using LLMs as feature generators for downstream models, as weak labelers for scalable data annotation, and as judges for automated quality evaluation of model outputs.

## Prerequisites

- R02-M01: Classical ML in the GenAI Era
- Familiarity with LLM APIs (OpenAI, Anthropic)
- B04: Prompt Engineering (beginner track)

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | LLMs as Feature Generators | Yes | Text-to-features pipelines, embedding-based features, LLM-generated features for classification |
| L02 | LLMs as Weak Labelers | Yes | LLM-based label generation, noise-aware training, label quality estimation, active learning |
| L03 | LLM-as-Judge for Model Outputs | Yes | Automated quality scoring, human-LLM agreement metrics, evaluation at scale |

## Key Tools

- OpenAI / Anthropic APIs
- scikit-learn, XGBoost
- Sentence Transformers
- Snorkel or custom weak supervision frameworks
- pandas, NumPy

## Learning Outcomes

- Build pipelines that use LLMs to generate features for classical ML models
- Implement scalable data labeling using LLMs as weak labelers with quality controls
- Design LLM-as-Judge evaluation systems that correlate with human assessments
- Understand the trade-offs of incorporating LLMs into traditional ML workflows
