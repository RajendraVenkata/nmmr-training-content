# M03: Working with LLM APIs

## Overview

This module teaches the practical skills of integrating with LLM provider APIs. You will learn to make API calls, parse responses, implement function calling with structured outputs, and build provider-agnostic clients using abstraction layers like LiteLLM.

## Prerequisites

- Completion of M01 (Python and TypeScript fundamentals)
- Completion of M02 (understanding of tokens and context windows)
- Familiarity with REST APIs and JSON

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | Calling Model APIs & Parsing Outputs | Yes | REST APIs, JSON request/response, error handling, rate limits |
| L02 | Function Calling & Structured Outputs | Yes | Function calling patterns, JSON schema, Pydantic validation, retries |
| L03 | Provider Abstraction with LiteLLM | Yes | Multi-provider support, model routing, standardized API, cost optimization |

## Key Tools

- OpenAI Python SDK
- Anthropic Python SDK
- Groq Python SDK
- LiteLLM
- Pydantic for validation
- httpx / requests for HTTP calls

## Learning Outcomes

- Make API calls to OpenAI, Anthropic, and Groq endpoints with proper authentication and error handling
- Parse and validate structured JSON responses from LLM APIs
- Implement function calling patterns that let models invoke external tools
- Enforce output structure using JSON schemas and Pydantic validation
- Build a provider-agnostic LLM client that can switch between providers with zero code changes
- Handle rate limits, retries, and transient failures gracefully in production
