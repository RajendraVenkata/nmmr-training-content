# Course B9: Provider Abstraction — Write Once, Run Anywhere

> **Build LLM applications that aren't locked to a single provider** — Learn to swap between Ollama, OpenAI, Claude, and others with minimal code changes using provider abstraction patterns.

### Goal: Build agents that can seamlessly switch between LLM providers

---

## B9.1 Why Provider Abstraction Matters
- Vendor lock-in — The risk of building everything around one provider's API
- Cost optimization — Different providers for different tasks (cheap for simple, premium for complex)
- Reliability — Fallback to another provider when one is down or rate-limited
- Development vs production — Free local models for dev, cloud APIs for production
- Compliance — Some environments require specific providers (government, healthcare)
- The abstraction goal — Write your agent logic once, swap the LLM with a config change

## B9.2 Using the OpenAI SDK with Ollama (Compatible API) (Lab)
- Ollama's OpenAI-compatible endpoint — `http://localhost:11434/v1`
- Configuring the OpenAI SDK — `OpenAI(base_url="http://localhost:11434/v1", api_key="ollama")`
- Chat completions — Same code works against Ollama and OpenAI
- Streaming — Identical streaming interface across both
- Tool calling — Function calling works through the compatibility layer
- Limitations — Features that differ between Ollama and true OpenAI
- The power of compatibility — One codebase, multiple backends

## B9.3 Swapping Ollama → OpenAI → Anthropic Claude with One-Line Changes (Lab)
- Environment variable pattern — `LLM_PROVIDER=ollama|openai|anthropic`
- Factory function — `get_llm_client(provider)` that returns the right client
- Unified interface — Wrapping provider-specific SDKs behind a common API
- Request/response mapping — Normalizing different API formats
- Testing the swap — Same prompt, three different providers, comparing outputs
- Configuration-driven selection — `config.yaml` or `.env` for provider selection

## B9.4 LangChain's Provider Abstraction Layer
- The `BaseChatModel` interface — All LangChain chat models share the same API
- Swapping models — `ChatOllama` → `ChatOpenAI` → `ChatAnthropic` with one line
- Why this works — LangChain normalizes `invoke()`, `stream()`, `batch()` across providers
- Tool calling abstraction — Same `@tool` definitions work with all providers
- Agent portability — An agent built with Ollama runs on Claude without changes
- LCEL chains — Provider-agnostic chain definitions

## B9.5 Environment-Based Configuration (dev=Ollama, prod=Claude) (Lab)
- Development workflow — Free, fast, private with Ollama during development
- Production deployment — Claude or GPT for quality, reliability, and scale
- Environment files — `.env.development`, `.env.production` with different providers
- Configuration management — `pydantic-settings` for typed configuration
- Feature flags — Gradual rollout from dev to production models
- CI/CD integration — Automated testing with Ollama, deployment with cloud APIs
- Cost tracking — Monitoring usage across environments

## B9.6 Cost Tracking and Token Usage Monitoring
- Why track costs — LLM API costs can escalate quickly without visibility
- Token counting — Input tokens vs output tokens, counting before sending
- Provider pricing — Understanding per-million-token pricing across providers
- LangChain callbacks — `get_openai_callback()` for automatic token tracking
- Custom token tracking — Building a middleware that logs every API call
- Cost estimation — Predicting costs before running expensive operations
- Budget alerts — Setting spending limits and notification thresholds
- Optimization strategies — Caching, shorter prompts, cheaper models for simple tasks
