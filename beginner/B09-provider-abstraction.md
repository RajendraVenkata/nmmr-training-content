# Module B9: Provider Abstraction — Write Once, Run Anywhere

## Duration: 3-4 hours | Lab: Multi-provider agent

## Learning Objectives
- Use the OpenAI SDK with Ollama via its compatible endpoint
- Swap between Ollama, OpenAI, and Claude with a single config change
- Implement LangChain's provider abstraction for seamless switching
- Configure environment-based provider selection (dev=Ollama, prod=Claude)
- Track token usage and costs across providers

## Topics

### B9.1 Why Provider Abstraction Matters
- Develop for free on Ollama → Deploy on Claude/OpenAI
- Avoid vendor lock-in — Switch providers without rewriting code
- Test across providers to find the best quality/cost balance
- Graceful fallback — If one provider is down, fall back to another

### B9.2 Using the OpenAI SDK with Ollama (Compatible API)
- Ollama's OpenAI-compatible endpoint: `http://localhost:11434/v1`
- `from openai import OpenAI` → Works with Ollama out of the box
- Changing `base_url` and `api_key` is all it takes to switch
- What's compatible and what's not (edge cases)

### B9.3 Swapping Ollama → OpenAI → Anthropic Claude
- OpenAI SDK: Change `base_url` for each provider
- Native SDKs: `openai`, `anthropic` — Direct API access
- Anthropic's messages API vs OpenAI's chat completions API
- Handling API differences transparently

### B9.4 LangChain's Provider Abstraction Layer
- `ChatOllama`, `ChatOpenAI`, `ChatAnthropic` — Same interface
- Factory pattern for provider selection
- All tools, agents, and chains work identically regardless of provider
- `configurable_alternatives` — Runtime provider switching

### B9.5 Environment-Based Configuration (dev=Ollama, prod=Claude)
- `.env` file pattern for provider configuration
- `AI_PROVIDER`, `AI_MODEL`, `AI_BASE_URL` environment variables
- Factory function that reads config and returns the right LLM
- Docker environment variables for deployment
- Separate `.env.development` and `.env.production` files

### B9.6 Cost Tracking and Token Usage Monitoring
- Why tracking matters — Cloud APIs charge per token
- Token counting: `tiktoken` for OpenAI, model-specific for others
- Logging token usage per request
- Building a cost calculator (input tokens × rate + output tokens × rate)
- Setting budget alerts and daily limits
- Free development on Ollama = unlimited experimentation

### B9.7 Lab: Build an Agent That Runs on Ollama, Then Swap to Claude
- Build a functional agent using Ollama locally
- Implement provider abstraction with environment variables
- Swap to OpenAI/Claude API (if keys available) with zero code changes
- Compare response quality and latency across providers
- Track and log token usage

## Lab Exercises
1. Build a chat function using OpenAI SDK pointing to Ollama
2. Change only `base_url` and `api_key` to point to OpenAI (mock or real)
3. Create a provider factory function that reads from environment variables
4. Build a LangChain agent using `ChatOllama`, then swap to `ChatOpenAI`
5. Implement token counting and cost estimation logging
6. Run the same 10 test prompts across 2 providers, compare quality in a report

## Key Takeaways
- Provider abstraction is a best practice — Never hardcode a single LLM provider
- Ollama's OpenAI-compatible API makes switching nearly free
- LangChain's unified interface gives you provider independence out of the box
- Environment-based configuration makes deployment across environments seamless
- Cost tracking is essential — Know what your agent costs before production

---
*Next: [Module B10 — Beginner Capstone Project →](B10-capstone-faq-assistant.md)*
