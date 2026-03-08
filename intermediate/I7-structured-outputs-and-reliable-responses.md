# Course I7: Structured Outputs & Reliable Agent Responses

> **Make agent outputs predictable and trustworthy** — Use Pydantic validation, the Instructor library, retry strategies, output parsers, and guardrails to guarantee structured, reliable LLM responses.

### Goal: Build agents that produce consistent, validated, structured outputs every time

---

## I7.1 The Reliability Problem with LLM Outputs
- Why LLM outputs are unreliable — Non-deterministic, format-inconsistent, prone to hallucination
- The downstream impact — Broken parsers, failed integrations, bad user experience
- Types of output failures — Missing fields, wrong types, extra text, invalid JSON, hallucinated data
- The cost of retries — Each failed output wastes tokens and time
- The goal — Guaranteed structured output with validation and self-correction
- Approaches overview — Provider features, libraries, custom validation

## I7.2 Pydantic Models for Structured Output Validation (Lab)
- Pydantic refresher — Models, fields, validators, serialization
- Defining output schemas — Pydantic models that describe expected LLM output
- Field validation — Type checking, constraints (`ge`, `le`, `min_length`, `max_length`)
- Custom validators — `@field_validator` for business logic validation
- Nested models — Complex output structures with sub-objects
- Optional fields — Handling fields that may or may not be present
- Enum fields — Restricting values to a defined set
- From LLM output to Pydantic — Parsing JSON responses into validated models

## I7.3 Instructor Library — Guaranteed Structured Outputs (Lab)
- What is Instructor — A library that patches LLM clients for structured output
- Installing Instructor — `pip install instructor`
- Patching clients — `instructor.from_openai()`, `instructor.from_anthropic()`
- Defining response models — Pydantic models as the expected output type
- Automatic retry — Instructor retries with validation errors fed back to the LLM
- Max retries — Configuring retry limits and backoff
- Streaming structured output — Partial model updates as tokens arrive
- Instructor with Ollama — Using the OpenAI-compatible endpoint
- Validation context — Passing extra context to validators
- Complex extractions — Nested models, lists of objects, multi-step extraction

## I7.4 Retry Strategies and Self-Correction
- Why retries work — LLMs can fix their own mistakes when told what went wrong
- Simple retry — Try again with the same prompt
- Retry with error feedback — Include the validation error in the retry prompt
- Retry with examples — Add a correct example when retrying
- Exponential backoff — Increasing delay between retries
- Max retry limits — Preventing infinite retry loops
- Fallback strategies — Use a different model or simpler schema on persistent failure
- Self-correction patterns — Agent reviews and fixes its own output

## I7.5 Output Parsing with LangChain (Lab)
- `StrOutputParser` — Simple string extraction
- `JsonOutputParser` — Parsing JSON from LLM responses
- `PydanticOutputParser` — Validated parsing with Pydantic models
- Format instructions — Auto-generating prompt instructions from the parser
- `OutputFixingParser` — Automatic fix attempts on parse failures
- `RetryOutputParser` — Retry with the original prompt and error
- Streaming parsers — Parsing partial output during streaming
- Custom parsers — Building domain-specific output parsers

## I7.6 Guardrails — Input/Output Validation Frameworks (Lab)
- What are guardrails — Validators that run before and after LLM calls
- Input guardrails — Validating and sanitizing user input
- Output guardrails — Checking LLM output against rules
- Content safety guardrails — Filtering harmful or inappropriate content
- Factuality guardrails — Checking if output is grounded in provided context
- PII guardrails — Detecting and redacting personal information
- Custom guardrails — Building domain-specific validation rules
- Guardrails frameworks — NeMo Guardrails, Guardrails AI, custom implementations
- Combining guardrails — Layering multiple validators for defense in depth
