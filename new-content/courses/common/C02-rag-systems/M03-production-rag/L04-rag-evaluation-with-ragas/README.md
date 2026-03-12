# L04: RAG Evaluation with Ragas

## Overview

This lesson teaches you how to systematically evaluate RAG systems using the Ragas framework. You will learn how to measure faithfulness, groundedness, answer relevance, and context precision, and build evaluation pipelines that use golden datasets to track quality over time.

## Topics Covered

- Why systematic evaluation is essential for production RAG systems
- Ragas framework overview and its metric categories
- Faithfulness: does the answer contain only information supported by the retrieved context?
- Groundedness: are generated claims traceable to specific retrieved passages?
- Answer relevance: does the answer actually address the user's question?
- Context precision: are the retrieved documents relevant to the query?
- Context recall: does the retrieval capture all necessary information?
- Building golden datasets for repeatable evaluation
- Setting up automated evaluation pipelines for continuous monitoring

## Lab: Running a Full Ragas Evaluation Suite on a RAG System with a Golden Dataset

Create a golden dataset of question-answer-context triples, run a complete Ragas evaluation across all key metrics, analyze the results to identify weaknesses, and establish baseline scores for ongoing monitoring.

### Lab Objectives

- Create a golden dataset with questions, expected answers, and reference contexts
- Configure and run a Ragas evaluation covering faithfulness, relevance, and context metrics
- Analyze evaluation results to identify specific failure modes (e.g., low faithfulness, poor context precision)
- Establish baseline metric scores and define quality thresholds for production readiness

## Key Takeaways

- RAG evaluation requires measuring both retrieval quality (context precision, recall) and generation quality (faithfulness, relevance)
- Ragas provides a standardized, LLM-assisted evaluation framework that automates much of the assessment process
- Golden datasets are essential for repeatable, comparable evaluation across system iterations
- Continuous evaluation pipelines catch regressions early and provide data-driven guidance for RAG optimization
