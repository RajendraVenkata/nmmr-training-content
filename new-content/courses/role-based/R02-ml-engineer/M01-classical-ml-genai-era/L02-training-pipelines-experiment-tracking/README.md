# L02: Training Pipelines & Experiment Tracking

## Overview

Learn how to build reproducible training pipelines with integrated experiment tracking using Weights & Biases. This lesson covers model versioning, hyperparameter management, and establishing reproducible workflows that enable confident iteration.

## Topics Covered

- Building reproducible training pipelines
- Experiment tracking with Weights & Biases (W&B)
- Model versioning and artifact management
- Hyperparameter management and search strategies
- Reproducibility best practices: seeds, environments, data snapshots

## Lab: Setting Up an Experiment-Tracked Training Pipeline with W&B

Build a complete training pipeline with W&B integration that logs hyperparameters, metrics, model artifacts, and dataset versions, enabling full experiment reproducibility and comparison.

### Lab Objectives

- Set up a W&B project with experiment tracking for a classification task
- Implement a training pipeline that logs hyperparameters, metrics, and artifacts automatically
- Run a hyperparameter sweep and compare results using W&B dashboards
- Version datasets and models to enable full experiment reproducibility

## Key Takeaways

- Without experiment tracking, teams waste time re-running experiments and lose track of what worked
- Model versioning and artifact management are essential for production ML systems
- Hyperparameter search should be systematic (grid, random, or Bayesian) rather than ad-hoc
- Reproducibility requires tracking not just code and parameters, but also data versions and environment configurations
