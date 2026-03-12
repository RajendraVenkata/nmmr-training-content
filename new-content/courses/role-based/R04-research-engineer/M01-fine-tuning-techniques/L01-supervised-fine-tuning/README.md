# L01: Supervised Fine-Tuning (SFT)

## Overview

Learn the fundamentals of supervised fine-tuning, the most common method for adapting pre-trained language models to specific tasks. This lesson covers dataset preparation best practices, training procedures, monitoring convergence, and deciding when SFT is the right approach versus prompt engineering.

## Topics Covered

- What supervised fine-tuning is and how it differs from pre-training
- Dataset preparation strategies (2,000-10,000 examples)
- Data formatting, cleaning, and quality assurance
- Training procedures and hyperparameter selection
- Monitoring training curves for convergence and overfitting
- When SFT is necessary versus prompting or few-shot approaches

## Lab: Performing SFT for Structured JSON Extraction

Fine-tune a language model using a clean, curated dataset to reliably extract structured JSON from unstructured text inputs. Monitor training metrics throughout the process and evaluate output quality.

### Lab Objectives

- Prepare and format a fine-tuning dataset for structured extraction tasks
- Configure and execute a supervised fine-tuning run with appropriate hyperparameters
- Monitor training loss curves and detect signs of overfitting
- Evaluate the fine-tuned model against a held-out test set for extraction accuracy

## Key Takeaways

- Dataset quality matters more than dataset size; 2,000 high-quality examples often outperform 10,000 noisy ones
- Training curves should be monitored for both training and validation loss to detect overfitting early
- SFT is most valuable when the task requires consistent formatting, domain-specific behavior, or reliable structured output
- Always benchmark the fine-tuned model against a strong prompt-engineering baseline before committing to SFT
