# L02: Function Calling & Structured Outputs

## Overview

This lesson teaches how to use function calling to let LLMs invoke external tools and how to enforce structured output formats using JSON schemas and Pydantic validation. These patterns are essential for building reliable AI applications that integrate with external systems.

## Topics Covered

- Function calling: concept, flow, and provider implementations
- Defining tool schemas for function calling
- Processing function call responses and executing tools
- JSON schema enforcement for structured model outputs
- Pydantic models for response validation and type safety
- Handling validation failures and implementing retry mechanisms
- Multi-step function calling chains

## Lab: Implementing Function Calling with Structured JSON Output Validation

Build a Python application that defines tool schemas, sends them to an LLM, processes function call responses, executes the corresponding functions, and validates all outputs using Pydantic models -- with automatic retry on validation failure.

### Lab Objectives

- Define function/tool schemas in the format expected by LLM providers
- Send function definitions alongside user messages in API calls
- Parse function call responses and execute the corresponding Python functions
- Define Pydantic models for expected output structures
- Implement retry logic that re-prompts the model when output validation fails

## Key Takeaways

- Function calling transforms LLMs from text generators into tool-using agents
- Well-defined tool schemas are critical -- ambiguous schemas lead to incorrect function calls
- Pydantic validation catches malformed outputs before they reach downstream systems
- Retry mechanisms with corrective feedback improve structured output reliability significantly
