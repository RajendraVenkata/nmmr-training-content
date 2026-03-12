# L01: Tracing with LangFuse & LangSmith

## Overview

This lesson introduces tracing as a foundational observability practice for AI systems. You will learn how to instrument AI pipelines so that every step -- retrieval, reranking, prompt construction, and LLM call -- is visible, making it possible to understand exactly what happened during each request and diagnose issues quickly.

## Topics Covered

- What tracing is and why it matters for AI pipelines
- Instrumenting AI pipelines with spans and traces
- Seeing every step: retrieval, reranking, prompt assembly, LLM call, post-processing
- Debugging production issues using trace data
- Comparing LangFuse (open-source) and LangSmith (LangChain ecosystem)

## Lab: Instrumenting a RAG Pipeline with LangFuse for Full Request Tracing

Instrument an existing RAG pipeline with LangFuse to capture detailed traces of every step, from the initial user query through document retrieval, context assembly, LLM generation, and final response delivery.

### Lab Objectives

- Set up a LangFuse instance and configure it to receive traces from an AI application
- Add tracing instrumentation to each stage of a RAG pipeline (retrieval, reranking, LLM call)
- Capture metadata such as token counts, latency per step, and retrieved document scores
- Use the LangFuse dashboard to inspect traces, identify bottlenecks, and debug a simulated failure
- Compare trace output quality between LangFuse and LangSmith for the same pipeline

## Key Takeaways

- Without tracing, debugging AI pipelines in production is effectively guesswork; traces reveal exactly what the system did for each request
- Each step in an AI pipeline (retrieval, reranking, LLM call) should be a separate span within a trace, enabling precise identification of where issues or latency occur
- LangFuse provides an open-source, self-hostable tracing solution well-suited for teams that need full data control
- Traces are not just for debugging; they provide the raw data needed for latency analysis, cost tracking, and quality evaluation at scale
