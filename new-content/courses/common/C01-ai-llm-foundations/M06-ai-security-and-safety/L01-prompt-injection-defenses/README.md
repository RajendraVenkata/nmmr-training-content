# L01: Prompt Injection Defenses

## Overview

This lesson covers the threat landscape of prompt injection attacks and the defense strategies needed to protect AI applications. You will learn to identify different injection types, implement input sanitization, apply output filtering, and design multi-layered defense architectures that make AI systems resilient to manipulation.

## Topics Covered

- What prompt injection is and why it is a critical AI security risk
- Direct prompt injection: overriding system instructions via user input
- Indirect prompt injection: malicious instructions embedded in retrieved content
- Jailbreaking: techniques attackers use to bypass safety guardrails
- Input sanitization: detecting and neutralizing injection attempts
- Output filtering: catching leaked system instructions and sensitive data in responses
- Multi-layered defense: combining input, output, and architectural defenses
- Testing for injection vulnerabilities: red teaming your AI system

## Key Takeaways

- Prompt injection is the most common and impactful vulnerability in LLM-based applications
- No single defense is sufficient -- effective protection requires multiple layers working together
- Input sanitization catches obvious attacks but cannot stop all injection attempts
- Output filtering is a critical last line of defense against information leakage
- Regular red teaming and adversarial testing are essential to maintain security as attacks evolve
