# L03: LLM-as-Judge for Model Outputs

## Overview

Learn how to use LLMs as automated evaluators for classical model outputs, enabling quality assessment at scale without requiring human reviewers for every prediction. This lesson covers designing judge prompts, measuring human-LLM agreement, and building scalable evaluation systems.

## Topics Covered

- Using LLMs to evaluate classical model outputs
- Automated quality scoring with LLM judges
- Human-LLM agreement metrics and calibration
- Designing effective judge prompts with rubrics
- Scaling LLM-based evaluation for production systems

## Lab: Building an LLM-as-Judge Evaluation System for Model Outputs

Build an automated evaluation system that uses an LLM to score model outputs against defined quality criteria, calibrate scores against human judgments, and generate evaluation reports.

### Lab Objectives

- Design judge prompts with clear rubrics for evaluating model outputs
- Implement an LLM-based scoring pipeline that evaluates outputs at scale
- Measure human-LLM agreement using correlation metrics (Cohen's kappa, Spearman's rho)
- Build an evaluation report generator that summarizes quality across different model versions

## Key Takeaways

- LLM-as-Judge enables evaluation at scale where human review is too expensive or too slow
- Judge prompt design with explicit rubrics is critical for consistent and reliable scoring
- Human-LLM agreement must be measured and calibrated; LLM judges are not a perfect substitute for human evaluation
- LLM-as-Judge works best for subjective quality dimensions (coherence, relevance, tone) where exact match metrics fall short
