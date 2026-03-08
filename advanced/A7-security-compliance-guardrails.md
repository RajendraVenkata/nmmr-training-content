# Course A7: Security, Compliance & Guardrails

> **Secure agentic AI systems for production** — Threat modeling, prompt injection defense, tool sandboxing, PII handling, secrets management, network security, compliance, and content safety.

### Goal: Implement comprehensive security and compliance for production agentic AI systems

---

## A7.1 Threat Model for Agentic AI Systems
- Why threat modeling for agents — Agents have unique attack surfaces
- STRIDE for agents — Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege
- Attack surface mapping — Prompts, tools, memory, APIs, data stores
- Threat actors — External attackers, malicious users, compromised tools
- Risk assessment — Likelihood × impact for each threat
- Mitigation strategies — Defense in depth, least privilege, input validation
- Threat model documentation — Creating and maintaining threat models

## A7.2 Prompt Injection Attacks — Detection and Prevention (Lab)
- What is prompt injection — User input that hijacks the LLM's instructions
- Direct injection — Malicious instructions in user messages
- Indirect injection — Hidden instructions in retrieved documents, tool results, emails
- Detection techniques — Pattern matching, classifier-based detection, LLM-as-judge
- Prevention strategies — Input sanitization, instruction hierarchy, output filtering
- Prompt armoring — Techniques to make system prompts more resistant
- Canary tokens — Detecting when system prompts are leaked
- Testing — Red-teaming your agents for injection vulnerabilities

## A7.3 Tool Call Validation and Sandboxing (Lab)
- Why tool validation — Agents can be tricked into calling tools maliciously
- Input validation — Schema validation, type checking, range limits
- Allowlisting — Restricting which tools can be called in which contexts
- Parameter sanitization — Preventing injection through tool parameters (SQL, command injection)
- Execution sandboxing — Running tools in isolated environments
- Resource limits — CPU, memory, time, network limits for tool execution
- Output validation — Checking tool results before feeding back to the LLM
- Audit logging — Recording every tool call for forensic analysis

## A7.4 PII Detection and Redaction in Agent Flows (Lab)
- What is PII — Personally Identifiable Information types and sensitivity levels
- Detection methods — Regex patterns, NER models, cloud services (Azure AI, AWS Comprehend)
- Redaction strategies — Masking, tokenization, generalization
- Where to redact — Input processing, before LLM call, in tool results, in outputs
- Reversible tokenization — Replacing PII with tokens, restoring for authorized use
- PII in RAG — Handling sensitive data in document stores and retrieval
- PII in logs — Ensuring PII doesn't leak into log files
- Compliance mapping — PII handling requirements for GDPR, CCPA, HIPAA

## A7.5 Secrets Management — Azure Key Vault, AWS Secrets Manager, HashiCorp Vault (Lab)
- Why secrets management — API keys, database passwords, tokens must be secure
- Azure Key Vault — Storing and retrieving secrets with managed identity
- AWS Secrets Manager — Automatic rotation, cross-account access
- HashiCorp Vault — Self-hosted secrets management, dynamic secrets
- Environment variables — Using secrets as env vars in containers
- Secret rotation — Automated key rotation without downtime
- Least privilege — Granting minimum necessary secret access
- Audit logging — Tracking who accessed which secrets and when

## A7.6 Network Security — VPCs, Private Endpoints, Firewall Rules
- Network isolation — VPC/VNet design for agent infrastructure
- Private endpoints — Keeping LLM API traffic off the public internet
- Service-to-service security — mTLS, service mesh, identity-based auth
- Egress control — Restricting outbound network access from agent containers
- WAF (Web Application Firewall) — Protecting agent API endpoints
- DDoS protection — Defending against volumetric attacks
- Network segmentation — Isolating different agent tiers and tenants

## A7.7 Audit Logging and Compliance (SOC 2, GDPR, HIPAA Considerations)
- Compliance requirements — What SOC 2, GDPR, and HIPAA mean for AI systems
- Audit log requirements — What to log, retention periods, immutability
- Data residency — Keeping data in specific geographic regions
- Right to erasure — Implementing GDPR deletion requests for agent data
- Data processing agreements — Contracts with LLM providers
- Access controls — RBAC for agent administration
- Compliance monitoring — Continuous compliance checking and reporting

## A7.8 Content Safety — Input/Output Filtering (Lab)
- Why content safety — Preventing harmful, inappropriate, or biased outputs
- Input filtering — Detecting and blocking harmful user inputs
- Output filtering — Scanning LLM responses before returning to users
- Provider safety features — Azure Content Safety, OpenAI moderation, Anthropic safety
- Custom classifiers — Training content safety models for your domain
- Toxicity detection — Identifying harmful, abusive, or offensive content
- Bias detection — Monitoring for discriminatory or biased outputs
- Safety metrics — Tracking safety incidents and false positive rates
