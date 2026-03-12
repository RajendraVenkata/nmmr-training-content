# L01: Knowledge Distillation

## Overview

Learn the teacher-student model paradigm for compressing large language models into smaller, more efficient versions. This lesson covers distillation strategies, training procedures for student models, and how to maintain high performance while significantly reducing model size and inference cost.

## Topics Covered

- Teacher-student model paradigm and its theoretical foundations
- Training smaller models from larger ones using soft labels
- Distillation strategies (logit matching, feature matching, attention transfer)
- Maintaining performance while reducing model size and inference cost
- Selecting appropriate student model architectures
- Benchmarking distilled models against teacher baselines

## Lab: Distilling a Large Model into a Smaller Student Model

Distill a large language model into a smaller student model using knowledge distillation techniques. Benchmark the student model against the teacher on a suite of evaluation tasks to quantify the performance-efficiency trade-off.

### Lab Objectives

- Set up a teacher-student distillation pipeline with appropriate loss functions
- Train a student model using soft labels from the teacher model
- Benchmark the student model on accuracy, latency, and memory footprint
- Analyze the performance-efficiency frontier across different student sizes

## Key Takeaways

- Knowledge distillation transfers the "dark knowledge" embedded in soft probability distributions, not just hard labels
- Smaller student models can retain 90-95% of teacher performance at a fraction of the inference cost
- The choice of distillation loss function and temperature parameter significantly impacts student quality
- Distilled models are especially valuable for edge deployment and latency-sensitive production environments
