# L01: Calling Model APIs & Parsing Outputs

## Overview

This lesson covers the fundamentals of calling LLM provider APIs, constructing well-formed requests, handling responses, and managing common failure modes like rate limits and timeouts. You will work with OpenAI, Anthropic, and Groq APIs to build practical integration skills.

## Topics Covered

- REST API fundamentals for LLM providers
- Authentication: API keys, headers, and security best practices
- Constructing JSON request payloads (messages, model, temperature, max_tokens)
- Parsing JSON responses and extracting generated content
- Error handling: HTTP status codes, API-specific error types
- Rate limit management: understanding limits, backoff strategies, retry logic
- Streaming responses for real-time output display

## Lab: Making API Calls to OpenAI/Anthropic/Groq

Write Python scripts that call each of the three major LLM provider APIs, send identical prompts, parse their responses into a unified format, and handle errors gracefully -- including rate limit retries with exponential backoff.

### Lab Objectives

- Configure API keys securely using environment variables
- Make completion requests to OpenAI, Anthropic, and Groq APIs
- Parse and normalize responses from each provider into a common format
- Implement exponential backoff retry logic for rate limit errors
- Compare response quality, latency, and token usage across providers

## Key Takeaways

- Each LLM provider has a slightly different API format, but the core patterns are consistent
- API keys must never be hardcoded -- always use environment variables or secret managers
- Rate limits are a production reality -- robust retry logic with exponential backoff is non-negotiable
- Streaming responses improve user experience for long-form generation tasks
