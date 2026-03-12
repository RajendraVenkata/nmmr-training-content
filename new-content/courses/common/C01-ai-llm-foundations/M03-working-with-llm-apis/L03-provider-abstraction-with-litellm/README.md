# L03: Provider Abstraction with LiteLLM

## Overview

This lesson introduces LiteLLM as a provider abstraction layer that lets you call 100+ LLM models using a single, standardized API format. You will learn how to build vendor-agnostic AI clients that can switch providers without code changes, implement model routing, and optimize costs across providers.

## Topics Covered

- The case for provider abstraction in production AI systems
- LiteLLM installation and configuration
- Standardized API format: one interface for all providers
- Multi-provider support: OpenAI, Anthropic, Groq, Azure, and more
- Model routing and fallback strategies
- Cost tracking and optimization across providers
- Migrating existing provider-specific code to LiteLLM

## Lab: Building a Provider-Agnostic LLM Client Using LiteLLM

Build a reusable LLM client class that uses LiteLLM to send requests to multiple providers, implements automatic fallback when a provider is unavailable, tracks costs per request, and can switch providers via configuration without changing application code.

### Lab Objectives

- Install and configure LiteLLM with multiple provider API keys
- Build a client class that abstracts provider-specific details behind a unified interface
- Implement automatic fallback: if one provider fails, try the next
- Add cost tracking that logs token usage and estimated cost per request
- Demonstrate switching providers by changing a single configuration value

## Key Takeaways

- Provider abstraction eliminates vendor lock-in and enables flexible model selection
- LiteLLM's unified interface simplifies code and reduces the surface area for provider-specific bugs
- Automatic fallback chains improve reliability by routing around provider outages
- Cost tracking across providers enables data-driven decisions about which models to use for which tasks
