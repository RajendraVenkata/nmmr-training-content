# L03: Managing Retrieved Documents & Tool Outputs

## Overview

This lesson addresses the challenge of injecting retrieved documents and tool outputs into the context window effectively. You will learn formatting strategies, context window budget management, and techniques for ensuring the model uses injected context correctly without hallucinating beyond it.

## Topics Covered

- Injecting retrieved documents into the context window
- Formatting retrieved content: delimiters, metadata, and source attribution
- Tool output formatting: structured vs unstructured results
- Context window budget management: allocating tokens across components
- Prioritizing and truncating context when the window is full
- Grounding instructions: telling the model to use only provided context
- Handling conflicting information across multiple retrieved documents
- Measuring context utilization and relevance

## Key Takeaways

- How you format injected context matters as much as what you inject -- clear delimiters and metadata help the model
- Context window budget management requires intentional allocation across system instructions, retrieved docs, and output space
- Grounding instructions ("answer only based on the provided documents") reduce hallucination significantly
- When context overflows the window, intelligent truncation and prioritization outperform naive truncation
- Monitoring which retrieved content the model actually uses helps optimize retrieval quality over time
