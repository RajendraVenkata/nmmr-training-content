# L03: Secret Management & Access Control

## Overview

Learn how to securely manage API keys, model access credentials, and sensitive data within AI infrastructure. This lesson covers secret rotation, access control for AI systems, and handling PII in AI pipelines while maintaining compliance with security requirements.

## Topics Covered

- API key management for AI services (OpenAI, Anthropic, cloud APIs)
- Secret rotation strategies and automation
- Access control for AI systems: RBAC, service accounts, least privilege
- PII handling in AI infrastructure: data masking, encryption at rest, audit logging

## Key Takeaways

- AI systems often require many API keys and credentials; centralized secret management (e.g., Vault) is essential
- Secret rotation must be automated and tested; manual rotation leads to outages and security gaps
- Access control should follow the principle of least privilege: models and services should only access what they need
- PII in AI pipelines requires special handling: data masking in logs, encryption, and audit trails for compliance
- Never embed API keys in container images, environment variables visible in dashboards, or version control
