# M06: AI Security & Safety

## Overview

This module covers the critical security and safety considerations for AI applications. You will learn to defend against prompt injection attacks, handle personally identifiable information (PII) properly, and implement controls to prevent training data and sensitive information from leaking through AI system outputs.

## Prerequisites

- Completion of M03 (experience working with LLM APIs)
- Completion of M04 (understanding of context engineering and system instructions)
- Basic understanding of application security concepts

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Prompt Injection Defenses | No | Injection types, defense strategies, input sanitization, output filtering |
| L02 | PII Handling & Access Control | No | PII identification, anonymization, access control patterns |
| L03 | Data Leakage Controls | No | Training data leakage prevention, output filtering, monitoring |

## Key Tools

- Input sanitization libraries
- PII detection tools (Presidio, custom regex patterns)
- Output filtering frameworks
- Security monitoring and logging tools
- Access control middleware

## Learning Outcomes

- Identify and classify different types of prompt injection attacks
- Implement multi-layered defense strategies against prompt injection
- Detect and handle PII in AI pipeline inputs and outputs
- Apply anonymization techniques to protect sensitive data in AI workflows
- Design access control patterns that limit what data AI systems can access and expose
- Implement output filtering and monitoring to prevent data leakage in production systems
