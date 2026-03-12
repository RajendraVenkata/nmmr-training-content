# L04: Automated Regression Gating in CI/CD

## Overview

This lesson teaches how to wire AI evaluation into your CI/CD pipeline so that quality regressions are automatically caught before they reach production. You will learn to set quality thresholds, configure evaluation jobs in GitHub Actions, and implement merge gates that prevent code changes from landing if they degrade AI output quality.

## Topics Covered

- The case for eval-gated CI/CD in AI applications
- Defining quality thresholds: minimum scores for faithfulness, relevance, and groundedness
- Structuring evaluation as a CI/CD job: test runner, dataset, and scoring
- GitHub Actions workflow configuration for evaluation jobs
- Handling evaluation job failures: blocking merges vs warning-only modes
- Balancing evaluation speed with coverage (subset testing vs full dataset)
- Tracking evaluation trends across builds and releases
- Alerting and notification on quality drops

## Lab: Setting Up an Eval-Gated CI/CD Pipeline

Build a GitHub Actions workflow that automatically runs Ragas evaluations against a golden dataset on every pull request, compares scores against defined quality thresholds, and blocks the merge if any metric falls below the minimum acceptable score.

### Lab Objectives

- Create a GitHub Actions workflow that triggers evaluation on pull requests
- Configure the workflow to run Ragas evaluations against a golden dataset
- Define quality thresholds (e.g., faithfulness >= 0.85, groundedness >= 0.80)
- Implement merge gating: fail the CI check if scores drop below thresholds
- Add evaluation score reporting as a pull request comment for reviewer visibility

## Key Takeaways

- Without automated evaluation gating, quality regressions silently accumulate in production
- Quality thresholds should be set based on baseline measurements, not arbitrary targets
- Subset evaluation on every PR provides fast feedback; full evaluation can run on merge to main
- Evaluation scores reported on pull requests make quality visible to the entire team
- Eval-gated CI/CD transforms AI quality from a hope into a guarantee
