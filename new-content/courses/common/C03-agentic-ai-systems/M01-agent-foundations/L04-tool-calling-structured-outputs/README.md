# L04: Tool Calling & Structured Outputs

## Overview

This lesson covers the practical implementation of reliable tool calling and structured output generation for AI agents. You will learn how to enforce JSON output schemas, validate responses with Pydantic, and build retry mechanisms that handle malformed LLM outputs gracefully.

## Topics Covered

- Implementing reliable function calling with LLM APIs
- JSON output schema enforcement techniques
- Pydantic model validation for structured outputs
- Retry mechanisms for malformed outputs
- Error handling strategies for tool calling failures
- Best practices for tool definition and parameter design

## Lab: Building an Agent with Reliable Tool Calling

Build an agent that uses LLM function calling to interact with external tools, enforcing structured outputs through Pydantic models. Implement retry logic that detects and recovers from malformed responses automatically.

### Lab Objectives

- Define tool schemas using JSON Schema and register them with an LLM provider
- Implement Pydantic models to validate tool call arguments and return values
- Build a retry mechanism that re-prompts the LLM when output validation fails
- Handle edge cases including partial responses, timeout errors, and unsupported tool calls
- Test the agent end-to-end with multiple tools and verify output consistency

## Key Takeaways

- Reliable tool calling requires strict schema definitions that leave no room for ambiguity in parameter types or descriptions
- Pydantic validation acts as a safety net that catches malformed outputs before they propagate through the agent pipeline
- Retry mechanisms should include exponential backoff and a maximum retry count to prevent infinite loops and runaway costs
- Well-designed tool descriptions significantly reduce the frequency of malformed outputs from the LLM
