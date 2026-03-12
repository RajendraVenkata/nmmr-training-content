# L03: Evaluation Frameworks - Ragas & TrueLens

## Overview

This lesson introduces Ragas and TrueLens as automated evaluation frameworks for measuring AI system quality programmatically. You will learn to run faithfulness and groundedness evaluations on RAG pipelines, interpret evaluation scores, and use framework outputs to identify specific failure points in your system.

## Topics Covered

- Ragas framework: architecture, metrics, and usage patterns
- TrueLens: feedback functions, tracing, and evaluation dashboards
- Measuring faithfulness programmatically using LLM-as-judge patterns
- Measuring groundedness: verifying outputs against source documents
- Context relevance and answer relevance metrics
- Interpreting evaluation scores: what is "good enough"?
- Identifying failure patterns from evaluation results
- Comparing Ragas vs TrueLens: when to use which

## Lab: Running Automated Evaluations Using Ragas on a RAG Pipeline

Set up the Ragas framework, connect it to a RAG pipeline, run automated evaluations against a golden dataset, analyze the results to identify weak points, and generate an evaluation report with actionable improvement recommendations.

### Lab Objectives

- Install and configure the Ragas evaluation framework
- Connect Ragas to an existing RAG pipeline for end-to-end evaluation
- Run faithfulness, relevance, and groundedness evaluations on a golden dataset
- Analyze per-question scores to identify specific failure patterns
- Generate an evaluation summary report with scores and improvement recommendations

## Key Takeaways

- Ragas and TrueLens automate evaluation work that would take hours to do manually
- LLM-as-judge evaluation is not perfect but is far more consistent and scalable than human vibe checks
- Per-question score analysis is more actionable than aggregate scores alone
- Evaluation frameworks reveal systemic issues (e.g., retrieval misses, context formatting problems) that are hard to spot manually
- Regular automated evaluation runs are the foundation for continuous quality improvement
