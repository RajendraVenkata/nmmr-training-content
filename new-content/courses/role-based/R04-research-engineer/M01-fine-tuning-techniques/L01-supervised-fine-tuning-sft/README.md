# Supervised Fine-Tuning (SFT)

## Overview

Learn when supervised fine-tuning is necessary over prompting, how to prepare clean datasets of 2,000-10,000 examples, and how to monitor training curves for optimal results.

## Topics Covered

- What SFT is and when it's necessary over prompting
- Dataset preparation: 2,000-10,000 clean examples
- Training procedures and hyperparameter selection
- Monitoring training curves and detecting overfitting

## Lab: SFT for Structured JSON Extraction

Perform supervised fine-tuning on a model for structured JSON extraction, measuring quality improvements with before/after comparisons.

### Lab Objectives

- Prepare a clean fine-tuning dataset for JSON extraction
- Perform SFT using Hugging Face TRL/PEFT
- Monitor training curves during the fine-tuning process
- Measure before/after accuracy and JSON validity rate

## Key Takeaways

- SFT makes a model consistently excellent at a narrow task
- Dataset quality matters more than dataset quantity for fine-tuning
- Training curves reveal overfitting and help select optimal checkpoints
