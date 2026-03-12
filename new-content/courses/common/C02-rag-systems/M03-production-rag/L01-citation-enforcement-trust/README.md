# L01: Citation Enforcement & Trust

## Overview

This lesson focuses on making RAG systems trustworthy by ensuring every generated answer is grounded in retrieved evidence. You will learn techniques for enforcing citations, detecting unsupported claims, and gracefully declining to answer when the retrieved context is insufficient.

## Topics Covered

- Why citation enforcement is essential for production RAG systems
- Grounding answers in evidence: linking claims to source passages
- Citation generation: inline references, footnotes, and source attribution formats
- Declining to answer when retrieved evidence is insufficient
- Preventing hallucinations through prompt engineering and output validation
- Confidence scoring and retrieval quality thresholds

## Key Takeaways

- Trustworthy RAG systems must attribute every claim to a specific retrieved passage
- Prompt engineering techniques (e.g., instructing the model to cite sources and say "I don't know") significantly reduce hallucinations
- Setting retrieval confidence thresholds allows the system to decline gracefully rather than fabricate answers
- Citation enforcement is not just a UX feature but a critical trust and compliance requirement in enterprise deployments
