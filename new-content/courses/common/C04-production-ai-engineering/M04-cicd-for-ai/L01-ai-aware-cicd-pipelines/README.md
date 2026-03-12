# L01: AI-Aware CI/CD Pipelines

## Overview

This lesson covers how to build CI/CD pipelines that account for the unique requirements of AI applications. You will learn how AI CI/CD differs from traditional software delivery, how to incorporate evaluation steps into build pipelines, how to version prompts alongside code, and how to manage AI-specific artifacts such as model weights and evaluation datasets.

## Topics Covered

- How AI CI/CD differs from traditional software CI/CD
- Incorporating evaluation steps into CI/CD pipelines
- Prompt versioning: tracking prompt changes alongside code changes
- Artifact management for AI systems (models, embeddings, evaluation datasets)
- Pipeline design patterns for AI applications

## Lab: Building a CI/CD Pipeline That Includes Evaluation Steps for an AI Application

Build a complete CI/CD pipeline using GitHub Actions that runs standard tests, executes AI-specific evaluations against a test dataset, and reports quality metrics as part of the build process.

### Lab Objectives

- Set up a GitHub Actions workflow for an AI application with standard build and test steps
- Add an evaluation step that runs the AI application against a curated test dataset
- Capture and report evaluation metrics (accuracy, latency, cost) as pipeline outputs
- Implement prompt versioning by tracking prompt templates in version control with change history
- Configure the pipeline to fail when evaluation scores drop below defined thresholds

## Key Takeaways

- Traditional CI/CD pipelines test whether code works correctly; AI CI/CD pipelines must also test whether the AI produces good outputs, requiring evaluation steps that go beyond unit and integration tests
- Prompt changes can have as much impact on system behavior as code changes, so prompts must be versioned, reviewed, and tested with the same rigor as source code
- AI artifacts (model snapshots, evaluation datasets, prompt versions) need dedicated management strategies because they are large, change independently from code, and directly affect system quality
- A well-designed AI CI/CD pipeline catches quality regressions before deployment, transforming AI quality management from a manual, post-deployment activity into an automated, pre-deployment gate
