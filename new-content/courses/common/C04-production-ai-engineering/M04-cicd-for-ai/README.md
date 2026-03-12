# M04: CI/CD for AI Systems

## Overview

This module covers how to build continuous integration and deployment pipelines specifically designed for AI applications. You will learn how AI CI/CD differs from traditional software, how to gate deployments on evaluation quality, and how to validate non-deterministic outputs using both programmatic checks and LLM-as-judge techniques.

## Prerequisites

- Completion of M01 through M03, or equivalent production AI experience
- Familiarity with Git, GitHub, and basic CI/CD concepts
- Understanding of AI evaluation metrics and quality measurement from C03 or equivalent
- Experience with containerized deployments from M01

## Lessons

| Lesson | Name | Lab? | Key Topics |
|--------|------|------|------------|
| L01 | AI-Aware CI/CD Pipelines | Yes | How AI CI/CD differs from traditional, eval steps in pipelines, prompt versioning, artifact management |
| L02 | Eval-Gated Deployments | No | Quality thresholds for deployment, automatic build failure on quality drops, prompt change regression detection |
| L03 | Deterministic Validation & LLM-as-Judge | No | LLMs judging non-deterministic outputs, programmatic checks, validation before delivery, combining validation methods |

## Key Tools

- GitHub Actions for CI/CD pipeline orchestration
- Prompt versioning and management tools
- Evaluation frameworks (custom and open-source)
- LLM-as-judge evaluation harnesses
- Docker for reproducible build and test environments

## Learning Outcomes

- Design CI/CD pipelines that incorporate evaluation steps specific to AI applications
- Implement prompt versioning and artifact management for reproducible AI deployments
- Configure quality thresholds that automatically block deployments when evaluation scores drop
- Detect regressions introduced by prompt changes before they reach production
- Combine programmatic validation with LLM-as-judge techniques to validate non-deterministic AI outputs
