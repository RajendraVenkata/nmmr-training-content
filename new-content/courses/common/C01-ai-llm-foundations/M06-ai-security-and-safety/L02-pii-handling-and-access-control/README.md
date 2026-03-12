# L02: PII Handling & Access Control

## Overview

This lesson addresses the challenge of identifying, protecting, and controlling access to personally identifiable information (PII) within AI pipelines. You will learn to detect PII in inputs and outputs, apply anonymization techniques, and design access control patterns that prevent unauthorized data exposure through AI systems.

## Topics Covered

- Types of PII and their sensitivity levels in AI contexts
- PII detection: regex patterns, NER models, and tools like Microsoft Presidio
- Anonymization techniques: masking, tokenization, synthetic data substitution
- PII in AI pipeline stages: ingestion, processing, storage, and output
- Access control patterns for AI systems: role-based, attribute-based, and context-aware
- Audit logging: tracking who accessed what data through AI interactions
- Compliance considerations: GDPR, CCPA, and industry-specific regulations
- Designing AI systems that minimize PII exposure by default

## Key Takeaways

- AI systems can inadvertently expose PII through generated outputs, even when inputs are sanitized
- PII detection must happen at multiple pipeline stages: input, retrieval, and output
- Anonymization is not just masking -- effective techniques preserve data utility while protecting identity
- Access control for AI systems must consider what data the model can access, not just what users can access
- Compliance is not optional -- understanding GDPR and CCPA requirements is essential for production AI systems
