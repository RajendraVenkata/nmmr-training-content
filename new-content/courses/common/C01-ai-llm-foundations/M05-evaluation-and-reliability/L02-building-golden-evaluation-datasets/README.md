# L02: Building Golden Evaluation Datasets

## Overview

This lesson teaches how to curate a golden evaluation dataset -- a set of 50-200 verified question-answer pairs that serve as the ground truth for measuring AI system quality. You will learn dataset design principles, annotation guidelines, and quality assurance processes for building evaluation sets that are representative, unbiased, and maintainable.

## Topics Covered

- What makes a golden dataset "golden": verified, representative, diverse
- Dataset size guidelines: why 50-200 pairs is the practical sweet spot
- Question design: covering happy paths, edge cases, and adversarial inputs
- Answer annotation: writing reference answers with sufficient detail
- Annotation guidelines: ensuring consistency across multiple annotators
- Dataset diversity: covering different question types, topics, and difficulty levels
- Version controlling and evolving datasets over time
- Common pitfalls: overfitting to your eval set, annotation bias, stale datasets

## Lab: Creating a Golden Evaluation Dataset for a Domain-Specific AI System

Design and build a golden evaluation dataset of 50+ question-answer pairs for a domain-specific AI system, complete with annotation guidelines, difficulty categorization, and a quality review process.

### Lab Objectives

- Define the scope and domain coverage for the evaluation dataset
- Write annotation guidelines that ensure consistent answer quality
- Create 50+ question-answer pairs spanning easy, medium, and hard difficulty levels
- Include edge cases and adversarial questions that test system robustness
- Implement a peer review process to verify answer quality and consistency

## Key Takeaways

- A well-curated golden dataset is the single most valuable asset for AI system evaluation
- Dataset quality matters more than quantity -- 50 excellent pairs beat 500 sloppy ones
- Annotation guidelines prevent drift and inconsistency as multiple people contribute to the dataset
- Golden datasets must evolve as the system changes -- stale datasets measure the wrong things
- Edge cases and adversarial inputs in the dataset catch failure modes that happy-path testing misses
