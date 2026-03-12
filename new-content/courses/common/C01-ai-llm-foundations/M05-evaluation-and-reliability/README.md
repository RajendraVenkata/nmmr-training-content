# M05: Evaluation & Reliability

## Overview

This module teaches how to measure and ensure the quality of AI system outputs through rigorous evaluation. You will move beyond subjective "vibe checks" to build golden datasets, run automated evaluations using frameworks like Ragas and TrueLens, and wire evaluation gates into CI/CD pipelines to prevent quality regressions.

## Prerequisites

- Completion of M03 (experience working with LLM APIs)
- Completion of M04 (understanding of context engineering)
- Basic familiarity with CI/CD concepts

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Beyond Vibe Evals - Metrics That Matter | No | Faithfulness, relevance, groundedness, why vibes fail |
| L02 | Building Golden Evaluation Datasets | Yes | Curating 50-200 Q&A pairs, dataset design, annotation guidelines |
| L03 | Evaluation Frameworks - Ragas & TrueLens | Yes | Ragas framework, TrueLens, programmatic faithfulness measurement |
| L04 | Automated Regression Gating in CI/CD | Yes | CI/CD eval integration, quality thresholds, merge gating |

## Key Tools

- Ragas evaluation framework
- TrueLens
- pytest for test harness
- GitHub Actions / CI/CD platforms
- pandas for dataset management

## Learning Outcomes

- Identify and apply quantitative evaluation metrics (faithfulness, relevance, groundedness) to AI outputs
- Design and curate golden evaluation datasets with 50-200 verified question-answer pairs
- Run automated evaluations using the Ragas framework on RAG pipelines
- Configure quality thresholds that must pass before code changes can be merged
- Set up CI/CD pipelines that automatically run evaluations and gate deployments on quality scores
- Distinguish between meaningful quality metrics and unreliable subjective assessments
