# NMMR Technologies — Agentic AI Training Program

## Complete Course Outline

> **Build Agentic AI Applications from Zero to Production**
>
> A hands-on training program with integrated Docker-based lab environments where every concept comes with a runnable container you can spin up instantly via the browser terminal (term.js).

---

## Program Structure

| Level | Duration | Prerequisites | What You'll Build |
|-------|----------|--------------|-------------------|
| **Beginner** | 4-5 weeks | Basic Python knowledge | Simple agents, tool-calling bots, RAG chatbots |
| **Intermediate** | 5-6 weeks | Completed Beginner level | Multi-agent systems, complex workflows, memory-enabled agents |
| **Advanced** | 6-8 weeks | Completed Intermediate level | Production-grade, cloud-deployed, scalable agentic systems |

---

## Lab Environment

Every module includes a **Docker-based hands-on lab** accessible via the browser terminal (term.js). The terminal has two display modes:

**Default View** — Terminal fixed at the bottom, training content scrolls above it:

```
┌─────────────────────────────────────────────┐
│  Browser (Training Website)                 │
│  ┌─────────────────────────────────────────┐│
│  │  Training Content (scrollable)          ││
│  │                                         ││
│  │  Module 3: Tool Calling                 ││
│  │  ...                                    ││
│  │  [Run Lab ▶]                           ││
│  │                              ▲ scroll ▲ ││
│  ├─────────────────────────────────────────┤│
│  │  term.js Terminal (fixed at bottom)     ││
│  │  $ ollama run llama3.1:8b               ││
│  │  $ python agent.py                      ││
│  │  > Using tool: calculator               ││
│  │  > Result: 42                           ││
│  └─────────────────────────────────────────┘│
└─────────────────────────────────────────────┘
```

**Popup View** — Terminal opens as a floating overlay via a button click:

```
┌─────────────────────────────────────────────┐
│  Browser (Training Website)                 │
│  ┌─────────────────────────────────────────┐│
│  │  Training Content (full height)         ││
│  │                                         ││
│  │  Module 3: Tool Calling                 ││
│  │  ...                                    ││
│  │                                         ││
│  │       ┌──────────────────────┐          ││
│  │       │  term.js Terminal    │  [x]     ││
│  │       │  (popup overlay)     │          ││
│  │       │  $ python agent.py   │          ││
│  │       │  > Result: 42        │          ││
│  │       └──────────────────────┘          ││
│  │                                         ││
│  │                           [Terminal ▶] ││
│  └─────────────────────────────────────────┘│
└─────────────────────────────────────────────┘
```

- **Docker-in-Docker (DinD)**: Each lab spins up isolated containers
- **Pre-built images**: All dependencies pre-installed — no setup time
- **Instant reset**: Restart any lab to a clean state
- **Persistent workspace**: Your code saves between sessions

---

## Complete Table of Contents

---

# LEVEL 1 — BEGINNER

### Goal: Understand AI agents and build your first working agents locally

---

### Module B1: Foundations of AI & Large Language Models
- B1.1 What is Artificial Intelligence — A quick history
- B1.2 What are Large Language Models (LLMs)
- B1.3 How LLMs work — Transformers, tokens, attention
- B1.4 Key concepts — Context window, temperature, tokens, hallucinations
- B1.5 The LLM landscape — OpenAI, Anthropic Claude, Google Gemini, Meta Llama, Mistral
- B1.6 Closed-source vs Open-source models
- B1.7 **Lab**: Chat with different LLMs via web UI and observe differences

### Module B2: Python for AI — Quick Refresher
- B2.1 Python basics recap — variables, functions, classes
- B2.2 Working with APIs — `requests` library
- B2.3 JSON handling for LLM responses
- B2.4 Async programming basics — `asyncio`, `aiohttp`
- B2.5 Virtual environments and dependency management

### Module B3: LLM API Keys & Interaction Reference
> *A hands-on reference guide — one lesson per provider. Come back anytime you need a refresher on setting up or calling a specific LLM API.*

#### B3.1 Anthropic Claude
- Creating an Anthropic account — Sign-up walkthrough, email verification
- Navigating the Anthropic Console — Dashboard overview, usage graphs
- Generating API keys — Creating keys, naming conventions, key scoping
- API key management — Workspaces, key rotation, revoking compromised keys
- Understanding usage limits — Free tier, rate limits (RPM/TPM), billing tiers
- Setting up billing — Adding payment method, setting spend limits, usage alerts
- Installing the SDK — `pip install anthropic`, verifying installation
- The Messages API — Endpoint (`https://api.anthropic.com/v1/messages`), required headers (`x-api-key`, `anthropic-version`)
- Request format — `model`, `messages[]`, `max_tokens`, `system`, `temperature`
- Response format — Parsing `content[]`, `stop_reason`, `usage` (input/output tokens)
- Streaming responses — Using `stream=True` for real-time token output
- Multi-turn conversations — Building message history with `role: user` / `role: assistant`
- Vision capabilities — Sending images to Claude via base64 or URL
- Models overview — Claude Opus 4 (flagship reasoning), Sonnet 4 (balanced), Haiku 3.5 (fast & cheap)
- Model selection guide — When to use Opus vs Sonnet vs Haiku (cost, speed, quality trade-offs)
- Error handling — Handling `400`, `401`, `429` (rate limit), `529` (overloaded) responses
- Best practices — Secure key storage, retry logic with exponential backoff
- **Lab**: Generate your Anthropic API key and build a multi-turn chat script with Claude

#### B3.2 OpenAI (GPT)
- Creating an OpenAI account — Sign-up walkthrough, phone verification
- Navigating the OpenAI Platform — Dashboard, playground, usage tracking
- Generating API keys — Project keys vs user keys, naming and scoping
- API key management — Organization settings, team roles, key permissions
- Understanding usage limits — Free credits, tier system (Tier 1–5), rate limits per model
- Setting up billing — Adding payment method, hard/soft usage caps, auto-recharge
- Installing the SDK — `pip install openai`, verifying installation
- The Chat Completions API — Endpoint (`https://api.openai.com/v1/chat/completions`), required headers (`Authorization: Bearer`)
- Request format — `model`, `messages[]` (system/user/assistant roles), `temperature`, `max_tokens`, `response_format`
- Response format — Parsing `choices[]`, `message.content`, `finish_reason`, `usage` tokens
- Streaming responses — Using `stream=True`, handling `delta` chunks
- Multi-turn conversations — Managing conversation history, token counting with `tiktoken`
- Vision capabilities — Using GPT-4o with image inputs (`image_url` in content)
- JSON mode — Forcing structured JSON output with `response_format: { type: "json_object" }`
- Models overview — GPT-4o (flagship multimodal), GPT-4o-mini (cheap & fast), o1 (reasoning), o3 (advanced reasoning)
- Model selection guide — When to use GPT-4o vs mini vs o-series (cost, latency, reasoning depth)
- Function calling — Defining tools with JSON schema, handling `tool_calls` in response
- Error handling — Handling `401`, `429` (rate limit with `Retry-After`), `500`, `503` responses
- Best practices — Token optimization, context window management, API key rotation
- **Lab**: Generate your OpenAI API key and build a multi-turn chat with function calling

#### B3.3 Google Gemini
- Creating a Google AI Studio account — Sign-up with Google account, enabling the API
- Navigating Google AI Studio — Playground, prompt gallery, model tuning
- Generating API keys — Creating keys in AI Studio vs Google Cloud Console
- API key management — Google Cloud projects, IAM permissions, key restrictions (IP/referrer)
- Understanding usage limits — Free tier (generous RPM), pay-as-you-go pricing, quotas
- Setting up billing — Linking Google Cloud billing account, setting budgets and alerts
- Installing the SDK — `pip install google-generativeai`, verifying installation
- The Generative Language API — Endpoint, authentication methods (API key vs OAuth)
- Request format — `model`, `contents[]` (parts with text/image), `generationConfig`, `safetySettings`
- Response format — Parsing `candidates[]`, `content.parts[]`, `finishReason`, `usageMetadata`
- Streaming responses — Using `stream=True` with `generate_content()`, handling chunks
- Multi-turn conversations — Using `chat = model.start_chat()`, maintaining history
- Vision & multimodal — Sending images, audio, video, and PDFs to Gemini
- System instructions — Setting model behavior with `system_instruction` parameter
- Models overview — Gemini 2.5 Pro (flagship reasoning), Gemini 2.0 Flash (fast & multimodal), Gemini 2.0 Flash Lite (ultra-cheap)
- Model selection guide — When to use Pro vs Flash vs Lite (cost, speed, capability trade-offs)
- Grounding with Google Search — Enabling real-time web grounding in responses
- Safety settings — Configuring harm category thresholds (harassment, hate speech, etc.)
- Error handling — Handling `400`, `403` (quota exceeded), `429`, blocked content responses
- Best practices — Managing long contexts (1M+ tokens), multimodal prompt design
- **Lab**: Generate your Google AI API key and build a multimodal chat with image understanding

#### B3.4 Meta Llama
- What is Llama — Meta's open-weight large language model family
- Why Llama matters — Open-weight, free for commercial use, state-of-the-art performance
- Llama licensing — Meta's community license, acceptable use policy, commercial use terms
- Accessing Llama — Signing up at `llama.meta.com`, requesting model access, approval process
- Downloading model weights — Direct download from Meta, Hugging Face Hub (`meta-llama` org)
- Hugging Face integration — `huggingface-cli login`, `from_pretrained()`, gated model access
- Meta Llama API — Meta's hosted inference endpoint, API key generation, request/response format
- Calling Meta Llama API with Python — Using `requests` and the `llama-stack-client` SDK
- Models overview — Llama 3.1 (8B, 70B, 405B), Llama 3.2 (1B, 3B lightweight), Llama 3.2 Vision (11B, 90B), Llama 3.3 (70B)
- Model architecture — Decoder-only transformer, grouped-query attention, RoPE embeddings
- Understanding model sizes — Parameter counts, memory requirements (FP16, INT8, INT4)
- Quantization options — GPTQ, AWQ, GGUF — formats for efficient inference
- Running Llama locally — Options overview: Ollama, llama.cpp, vLLM, Hugging Face Transformers
- Running with Hugging Face Transformers — `AutoModelForCausalLM`, `pipeline()`, basic inference
- Running with llama.cpp — GGUF format, `llama-cli`, Python bindings (`llama-cpp-python`)
- Llama on cloud providers — Available on AWS Bedrock, Azure AI, Google Cloud, Groq, Together AI
- Tool calling with Llama — Built-in function calling support in Llama 3.1+
- Vision capabilities — Llama 3.2 Vision models for image understanding
- Lightweight models — Llama 3.2 1B/3B for mobile and edge deployment
- Fine-tuning overview — LoRA, QLoRA, full fine-tuning with Hugging Face PEFT
- Model selection guide — Choosing by use case: lightweight (1B/3B), general (8B), advanced (70B), frontier (405B)
- Community ecosystem — Hugging Face model hub, GGUF community quantizations, fine-tuned variants
- Error handling — Common issues with model loading, memory errors, tokenizer mismatches
- Best practices — Choosing the right format (GGUF vs HF vs AWQ), memory estimation, batch inference
- **Lab**: Download Llama 3.1 8B from Hugging Face, run inference with Transformers, and call Meta's Llama API

#### B3.5 Mistral AI
- Creating a Mistral account — Sign-up on La Plateforme, email verification
- Navigating La Plateforme — Dashboard, playground (Le Chat), usage analytics
- Generating API keys — Creating keys, naming conventions
- API key management — Key listing, deletion, workspace scoping
- Understanding usage limits — Free tier (experimental endpoints), rate limits, billing tiers
- Setting up billing — Adding payment method, cost estimator, usage alerts
- Installing the SDK — `pip install mistralai`, verifying installation
- The Chat Completions API — Endpoint (`https://api.mistral.ai/v1/chat/completions`), required headers
- Request format — `model`, `messages[]`, `temperature`, `max_tokens`, `response_format`
- Response format — Parsing `choices[]`, `message.content`, `finish_reason`, `usage`
- Streaming responses — Using `stream=True`, handling SSE chunks
- Multi-turn conversations — Building message history with roles
- JSON mode — Forcing structured JSON output
- Function calling — Defining tools, handling `tool_calls`, parallel tool execution
- Models overview — Mistral Large (flagship), Mistral Small (efficient), Codestral (code-specialized), Mistral Embed (embeddings)
- Model selection guide — When to use Large vs Small vs Codestral (reasoning, cost, code tasks)
- Code generation — Using Codestral for fill-in-the-middle and code completion
- Embeddings — Using Mistral Embed for vector search applications
- Error handling — Handling `401`, `429`, `422` (validation) responses
- Best practices — Guardrailing with `safe_prompt`, retry strategies
- **Lab**: Generate your Mistral API key and build a chat with function calling and code generation

#### B3.6 Cohere
- Creating a Cohere account — Sign-up walkthrough, trial key vs production key
- Navigating the Cohere Dashboard — Playground, API keys, usage monitoring
- Generating API keys — Trial keys (free, rate-limited) vs production keys
- API key management — Key rotation, team access, environment separation
- Understanding usage limits — Trial tier (generous free usage), production pricing, rate limits
- Setting up billing — Upgrading from trial, adding payment, cost tracking
- Installing the SDK — `pip install cohere`, verifying installation
- The Chat API — Endpoint (`https://api.cohere.com/v2/chat`), required headers
- Request format — `model`, `messages[]`, `temperature`, `max_tokens`, `connectors`, `tools`
- Response format — Parsing `message.content[]`, `finish_reason`, `usage`
- Streaming responses — Using `stream=True`, handling event types
- Multi-turn conversations — Managing chat history with `preamble` and message roles
- RAG with connectors — Built-in web search connector, custom connectors
- Grounded generation — Citations and source attribution in responses
- Models overview — Command R+ (flagship RAG/tool use), Command R (efficient), Embed v3 (multilingual embeddings), Rerank v3 (search re-ranking)
- Model selection guide — When to use Command R+ vs R vs Embed vs Rerank
- Embeddings — Generating embeddings with `input_type` (search_document, search_query, classification, clustering)
- Reranking — Using Rerank to improve search relevance
- Tool use — Defining tools, multi-step tool execution with citations
- Error handling — Handling `401`, `429`, `498` (token expired) responses
- Best practices — Leveraging Cohere's RAG strengths, embedding model selection for use case
- **Lab**: Generate your Cohere API key and build a grounded RAG chat with citations

#### B3.7 Ollama — Run Any LLM Locally
- What is Ollama — A local LLM runtime for running open-weight models on your own machine
- Why use Ollama — No API keys, no cost, full privacy, offline-capable, great for development
- Installing Ollama — Linux (`curl -fsSL https://ollama.com/install.sh | sh`), macOS (DMG), Windows (installer)
- Verifying installation — `ollama --version`, checking the background service
- Pulling your first model — `ollama pull llama3.1:8b`, understanding download sizes and storage
- Ollama model library — Browsing available models at `ollama.com/library`
- Popular models available — Llama 3.1/3.2, Mistral, Gemma 2, Phi-3, Qwen 2.5, DeepSeek, CodeLlama, Nomic Embed
- Understanding model sizes — 1B, 3B, 7B, 8B, 13B, 34B, 70B — VRAM/RAM requirements for each
- Quantization explained — Q2, Q4_0, Q4_K_M, Q5, Q8, FP16 — quality vs memory trade-offs
- Hardware guide — CPU-only (which models work), 8GB VRAM, 16GB VRAM, 24GB+ VRAM recommendations
- GPU vs CPU inference — Performance expectations, partial GPU offloading, `OLLAMA_NUM_GPU` setting
- Ollama CLI deep dive — `run`, `pull`, `list`, `ps`, `rm`, `show` (model metadata), `cp` (clone models)
- Chatting via CLI — `ollama run llama3.1:8b`, setting system prompts with `/set system`, multiline input
- Ollama REST API overview — `http://localhost:11434` — all endpoints
- Generate endpoint — `POST /api/generate` — single-turn text generation, request/response format
- Chat endpoint — `POST /api/chat` — multi-turn conversation format with message history
- Embeddings endpoint — `POST /api/embed` — generating vector embeddings locally
- OpenAI-compatible endpoint — `POST /v1/chat/completions` — drop-in replacement for OpenAI SDK
- Calling Ollama with Python — Using `requests` library directly
- Using OpenAI SDK with Ollama — `OpenAI(base_url="http://localhost:11434/v1")` for seamless switching
- Streaming responses — Handling NDJSON stream from Ollama, real-time token output
- Model customization — Creating `Modelfile` with custom system prompts, parameters, and templates
- Custom model parameters — `temperature`, `top_p`, `top_k`, `num_ctx` (context window), `repeat_penalty`
- Running multiple models — Switching between models, concurrent model loading, memory management
- Model management — Disk usage, cleaning up unused models, model storage location
- Ollama configuration — Environment variables (`OLLAMA_HOST`, `OLLAMA_MODELS`, `OLLAMA_NUM_PARALLEL`, `OLLAMA_MAX_LOADED_MODELS`)
- Network access — Binding to `0.0.0.0` for LAN access, reverse proxy setup
- Docker deployment — Running Ollama in Docker with GPU passthrough (`ollama/ollama` image)
- Troubleshooting — Common issues (port conflicts, OOM errors, slow inference), diagnostic commands
- Best practices — Model preloading, keep-alive tuning, context size optimization, choosing the right quantization
- **Lab**: Install Ollama, pull 3 different models (Llama, Mistral, Gemma), chat via CLI, call via REST API and Python, create a custom Modelfile

#### B3.8 Amazon Bedrock
- What is Amazon Bedrock — Managed access to multiple LLMs through a single API
- AWS account setup — Creating an account, IAM user setup, access keys
- Enabling models — Requesting model access in the Bedrock console (Claude, Llama, Mistral, Titan)
- Authentication — AWS access keys, IAM roles, `boto3` credential chain
- Installing the SDK — `pip install boto3`, configuring AWS CLI (`aws configure`)
- The InvokeModel API — Endpoint, regions, request signing
- Request format — Provider-specific body format (varies by model), `modelId`, `contentType`
- Response format — Parsing model-specific response bodies
- Converse API — Unified request/response format across all Bedrock models
- Streaming responses — Using `InvokeModelWithResponseStream` and `ConverseStream`
- Multi-turn conversations — Using Converse API's message history
- Models available — Claude (Anthropic), Llama (Meta), Mistral, Amazon Titan, Cohere Command
- Model selection guide — Choosing models based on task, cost, and region availability
- Guardrails — Creating Bedrock Guardrails for content filtering and PII redaction
- Knowledge Bases — Managed RAG with S3 data sources and vector stores
- Cost management — On-demand vs provisioned throughput, AWS Cost Explorer
- Error handling — Handling `ThrottlingException`, `AccessDeniedException`, `ModelNotReadyException`
- Best practices — Region selection for latency, cross-region inference, IAM least-privilege
- **Lab**: Set up AWS Bedrock, enable Claude, and build a multi-model chat using the Converse API

#### B3.9 Azure OpenAI Service
- What is Azure OpenAI — Microsoft-hosted OpenAI models with enterprise features
- Azure account setup — Creating an Azure account, subscription, resource group
- Requesting access — Applying for Azure OpenAI access, approval process
- Creating a resource — Azure OpenAI resource, selecting region, pricing tier
- Deploying models — Creating model deployments (GPT-4o, GPT-4o-mini, o1) in Azure AI Studio
- Authentication — API keys vs Azure Active Directory (Entra ID) tokens
- Installing the SDK — `pip install openai`, configuring for Azure endpoint
- The Azure Chat Completions API — Endpoint format (`https://{resource}.openai.azure.com/...`), `api-version` parameter
- Request format — Same as OpenAI but with `azure_endpoint`, `api_version`, `azure_deployment`
- Response format — Identical to OpenAI, parsing `choices[]`, `usage`
- Streaming responses — Using `stream=True`, same chunking as OpenAI
- Content filtering — Azure's built-in content safety filters, severity levels, custom filters
- Using the `openai` SDK with Azure — `AzureOpenAI` client class, environment variables
- Models available — GPT-4o, GPT-4o-mini, o1, o3, DALL-E 3, Whisper, text-embedding
- Model deployment guide — Choosing deployment type (Standard, Global, Provisioned)
- Azure AI Studio — Playground, prompt flow, model benchmarking
- Enterprise features — Private endpoints, VNet integration, managed identity, data residency
- Cost management — Token-based pricing, provisioned throughput units (PTUs), Azure Cost Management
- Error handling — Handling `401`, `429` (with `Retry-After`), `404` (deployment not found), content filter blocks
- Best practices — Deployment naming conventions, region selection, failover strategies
- **Lab**: Set up Azure OpenAI, deploy GPT-4o, and build a chat app with content filtering

#### B3.10 Quick Comparison & Cheat Sheet
- Side-by-side comparison table — Pricing per million tokens (input/output) across all providers
- Context window comparison — 4K to 2M tokens, who supports what
- Rate limits comparison — RPM and TPM across free and paid tiers
- Feature matrix — Streaming, function calling, vision, embeddings, JSON mode support per provider
- Latency benchmarks — Time-to-first-token and tokens-per-second across providers
- Strengths & weaknesses — What each provider does best (reasoning, code, RAG, cost, privacy)
- Common request/response patterns — Unified code snippets showing equivalent calls across all providers
- Environment variable best practices — Storing API keys safely (`.env`, `python-dotenv`, secrets managers)
- Security checklist — Never commit keys, `.gitignore` patterns, key rotation schedules
- Choosing the right provider — Decision flowchart by use case (cost, speed, quality, privacy, compliance)
- **Lab**: Build a unified Python script that calls all providers with the same prompt and compares responses side-by-side

### Module B4: Prompt Engineering Fundamentals
- B4.1 What is prompt engineering and why it matters
- B4.2 System prompts vs User prompts vs Assistant messages
- B4.3 Zero-shot, few-shot, and chain-of-thought prompting
- B4.4 Structured output — Getting JSON responses from LLMs
- B4.5 Prompt templates and variables
- B4.6 Common pitfalls and how to avoid them
- B4.7 **Lab**: Prompt engineering exercises with Ollama

### Module B5: Introduction to AI Agents
- B5.1 What is an AI agent — Beyond chatbots
- B5.2 Agent = LLM + Tools + Memory + Planning
- B5.3 The ReAct pattern — Reason → Act → Observe → Repeat
- B5.4 Types of agents — Conversational, task-oriented, autonomous
- B5.5 Agent vs Chain vs Simple LLM call — When to use what
- B5.6 Real-world agent examples and use cases
- B5.7 **Lab**: Trace through an agent's reasoning loop manually

### Module B6: Tool Calling — Giving Agents Abilities
- B6.1 What is tool/function calling
- B6.2 How tool calling works — The LLM decides, your code executes
- B6.3 Defining tools with JSON schemas
- B6.4 Tool calling with Ollama (Llama 3.1 native support)
- B6.5 Building your first tool — A calculator agent
- B6.6 Multiple tools — Search + calculator + file reader
- B6.7 Handling tool errors gracefully
- B6.8 **Lab**: Build a multi-tool agent from scratch with Ollama

### Module B7: Building Your First Agent with LangChain
- B7.1 What is LangChain — The orchestration layer
- B7.2 LangChain core concepts — Models, prompts, chains, tools, agents
- B7.3 Setting up LangChain with Ollama
- B7.4 Creating tools with `@tool` decorator
- B7.5 Building a ReAct agent with `create_tool_calling_agent`
- B7.6 AgentExecutor — Running agents with verbose tracing
- B7.7 Adding conversation memory to agents
- B7.8 **Lab**: Build a research assistant agent using LangChain + Ollama

### Module B8: Introduction to RAG (Retrieval Augmented Generation)
- B8.1 The problem — LLMs don't know your private data
- B8.2 What is RAG — Retrieve → Augment → Generate
- B8.3 Text splitting and chunking strategies
- B8.4 Embeddings — Converting text to vectors
- B8.5 Vector databases — ChromaDB (local, free)
- B8.6 Building a simple RAG pipeline
- B8.7 RAG with LangChain — Document loaders, retrievers, chains
- B8.8 **Lab**: Build a "Chat with your PDF" application

### Module B9: Provider Abstraction — Write Once, Run Anywhere
- B9.1 Why provider abstraction matters
- B9.2 Using the OpenAI SDK with Ollama (compatible API)
- B9.3 Swapping Ollama → OpenAI → Anthropic Claude with one-line changes
- B9.4 LangChain's provider abstraction layer
- B9.5 Environment-based configuration (dev=Ollama, prod=Claude)
- B9.6 Cost tracking and token usage monitoring
- B9.7 **Lab**: Build an agent that runs on Ollama locally, then swap to Claude API

### Module B10: Beginner Capstone Project
- B10.1 Project: **AI-Powered FAQ Assistant**
  - Loads company documents (PDF/text)
  - Uses RAG to answer questions accurately
  - Has tool calling for live data (weather, calculator, date/time)
  - Runs on Ollama locally
  - One-line swap to Claude/OpenAI for deployment
- B10.2 **Lab**: Full capstone project build in Docker environment

---

# LEVEL 2 — INTERMEDIATE

### Goal: Build multi-agent systems, complex workflows, and production-ready patterns

---

### Module I1: Deep Dive into Agent Architectures
- I1.1 Agent design patterns — Router, Planner, Executor, Critic
- I1.2 Single-agent vs Multi-agent architectures
- I1.3 Agent communication patterns — Sequential, parallel, hierarchical
- I1.4 State management in agentic systems
- I1.5 Error handling and recovery strategies
- I1.6 Agent observability — Tracing and debugging
- I1.7 **Lab**: Implement each architecture pattern with Ollama

### Module I2: LangGraph — Graph-Based Agent Workflows
- I2.1 Why LangGraph — Limitations of simple agent loops
- I2.2 Graph concepts — Nodes, edges, state, conditional branching
- I2.3 Building your first LangGraph workflow
- I2.4 State management with TypedDict and Pydantic
- I2.5 Conditional edges — Dynamic routing based on agent decisions
- I2.6 Cycles and loops — Agents that iterate until done
- I2.7 Parallel execution — Running multiple nodes simultaneously
- I2.8 **Lab**: Build a research → write → review agent workflow with LangGraph

### Module I3: Human-in-the-Loop Agents
- I3.1 Why HITL — Trust, safety, and compliance
- I3.2 Interrupt patterns — Pause agent, get approval, resume
- I3.3 Implementing HITL with LangGraph checkpoints
- I3.4 Approval workflows — Agent proposes, human approves
- I3.5 Escalation — When agents should hand off to humans
- I3.6 Audit trails and logging agent decisions
- I3.7 **Lab**: Build an expense approval agent with human approval gates

### Module I4: Advanced RAG Patterns
- I4.1 Limitations of naive RAG
- I4.2 Chunking strategies — Semantic, recursive, parent-child
- I4.3 Hybrid search — Combining vector search + keyword search (BM25)
- I4.4 Re-ranking — Cross-encoder models for better relevance
- I4.5 Multi-query RAG — Generating multiple search queries
- I4.6 Self-corrective RAG — Agent verifies and retries retrieval
- I4.7 RAG evaluation — Measuring retrieval quality and answer accuracy
- I4.8 **Lab**: Build an advanced RAG system with hybrid search and re-ranking

### Module I5: Multi-Agent Systems with CrewAI
- I5.1 What is CrewAI — Role-based multi-agent orchestration
- I5.2 Core concepts — Agents, Tasks, Crews, Processes
- I5.3 Defining agent roles — Researcher, Writer, Reviewer, Coder
- I5.4 Task dependencies and workflows
- I5.5 Sequential vs Hierarchical crew processes
- I5.6 Using CrewAI with Ollama
- I5.7 **Lab**: Build a content creation crew — Research → Write → Edit → Publish

### Module I6: Memory Systems for Agents
- I6.1 Types of memory — Short-term, long-term, episodic, semantic
- I6.2 Conversation memory — Buffer, summary, sliding window
- I6.3 Persistent memory with vector databases
- I6.4 Entity memory — Tracking facts about people, places, things
- I6.5 Memory injection strategies — When and how to recall
- I6.6 Memory management — Forgetting, updating, compressing
- I6.7 **Lab**: Build an agent with persistent long-term memory using ChromaDB

### Module I7: Structured Outputs & Reliable Agent Responses
- I7.1 The reliability problem with LLM outputs
- I7.2 Pydantic models for structured output validation
- I7.3 Instructor library — Guaranteed structured outputs
- I7.4 Retry strategies and self-correction
- I7.5 Output parsing with LangChain
- I7.6 Guardrails — Input/output validation frameworks
- I7.7 **Lab**: Build a data extraction agent with guaranteed JSON output

### Module I8: Agent Tools — Building Complex Integrations
- I8.1 Tool design principles — Clear descriptions, proper schemas
- I8.2 Building database tools — SQL query agents
- I8.3 Building API tools — REST and GraphQL integrations
- I8.4 File system tools — Reading, writing, transforming files
- I8.5 Web scraping tools — Browser automation with Playwright
- I8.6 Code execution tools — Sandboxed Python execution
- I8.7 Tool composition — Combining tools for complex tasks
- I8.8 **Lab**: Build a customer support agent with database + email + ticket tools

### Module I9: Agent Evaluation & Testing
- I9.1 Why testing agents is different from testing software
- I9.2 Unit testing tools and individual components
- I9.3 Integration testing agent workflows
- I9.4 LLM-as-judge — Using a model to evaluate agent outputs
- I9.5 Benchmarking with test datasets
- I9.6 Regression testing — Catching agent behavior changes
- I9.7 LangSmith for tracing and evaluation
- I9.8 **Lab**: Build a test suite for your agents with automated evaluation

### Module I10: Intermediate Capstone Project
- I10.1 Project: **AI-Powered Customer Support System**
  - Multi-agent crew: Triage Agent → Specialist Agent → Escalation Agent
  - RAG-based knowledge base with company docs
  - Database tools for order lookup and ticket management
  - Human-in-the-loop for refund approvals
  - Memory for returning customer context
  - Full LangGraph workflow with conditional routing
  - Runs on Ollama, deployable on Claude/OpenAI
- I10.2 **Lab**: Full capstone project with Docker-composed multi-service setup

---

# LEVEL 3 — ADVANCED

### Goal: Deploy production-grade agentic systems on the cloud with scalable architecture

---

### Module A1: Production Architecture for Agentic Systems
- A1.1 Architectural patterns — Microservices vs monolith for agents
- A1.2 Separation of concerns — Orchestrator, workers, tools, memory
- A1.3 Event-driven architecture for agents
- A1.4 Message queues — Agent communication via Redis/RabbitMQ/Azure Service Bus
- A1.5 API gateway design for agent endpoints
- A1.6 Stateless vs stateful agent deployment
- A1.7 Designing for horizontal scalability
- A1.8 **Lab**: Design and implement a scalable agent architecture with Docker Compose

### Module A2: Containerization & Orchestration
- A2.1 Docker best practices for AI applications
- A2.2 Multi-stage builds for lean agent containers
- A2.3 Docker Compose for multi-agent development environments
- A2.4 Docker-in-Docker (DinD) for agent sandboxing
- A2.5 Kubernetes fundamentals for agent deployment
- A2.6 Kubernetes operators for AI workloads
- A2.7 Helm charts for agentic system deployment
- A2.8 **Lab**: Kubernetes deployment of a multi-agent system (K3s in Docker)

### Module A3: Cloud Deployment — Azure
- A3.1 Azure architecture for agentic AI applications
- A3.2 Azure Container Apps — Serverless agent deployment
- A3.3 Azure Functions for event-driven agent triggers
- A3.4 Azure OpenAI Service integration
- A3.5 Azure AI Search for production RAG
- A3.6 Azure Service Bus for agent-to-agent communication
- A3.7 Azure Cosmos DB for agent state and memory
- A3.8 CI/CD with GitHub Actions for agent deployment
- A3.9 **Lab**: Deploy a full agentic system to Azure Container Apps

### Module A4: Cloud Deployment — AWS
- A4.1 AWS architecture for agentic AI applications
- A4.2 Amazon Bedrock — Managed agent deployment
- A4.3 AWS Lambda for serverless agent functions
- A4.4 Amazon ECS/EKS for containerized agents
- A4.5 Amazon OpenSearch for production RAG
- A4.6 Amazon SQS/SNS for agent orchestration
- A4.7 DynamoDB for agent state and session management
- A4.8 AWS CDK for infrastructure as code
- A4.9 **Lab**: Deploy a production agent system on AWS ECS with Bedrock

### Module A5: Cloud Deployment — Google Cloud Platform
- A5.1 GCP architecture for agentic AI applications
- A5.2 Google Cloud Run for serverless agent containers
- A5.3 Vertex AI Agents — Google's managed agent platform
- A5.4 Google Cloud Functions for event-driven agents
- A5.5 AlloyDB / Cloud SQL + pgvector for production RAG
- A5.6 Pub/Sub for agent messaging
- A5.7 Firestore for agent state management
- A5.8 **Lab**: Deploy agents on Cloud Run with Vertex AI integration

### Module A6: Scalability, Performance & Cost Optimization
- A6.1 Load balancing agent requests
- A6.2 Auto-scaling strategies — Scaling on queue depth, latency, token usage
- A6.3 Caching strategies — Prompt caching, semantic caching, response caching
- A6.4 Model routing — Using cheaper models for simple tasks, expensive models for complex ones
- A6.5 Token optimization — Prompt compression, context pruning
- A6.6 Batch processing vs real-time inference
- A6.7 Cost monitoring and budgeting — Per-agent, per-user, per-tenant
- A6.8 Rate limiting and throttling
- A6.9 **Lab**: Implement intelligent model routing and caching for cost optimization

### Module A7: Security, Compliance & Guardrails
- A7.1 Threat model for agentic AI systems
- A7.2 Prompt injection attacks — Detection and prevention
- A7.3 Tool call validation and sandboxing
- A7.4 PII detection and redaction in agent flows
- A7.5 Secrets management — Azure Key Vault, AWS Secrets Manager, HashiCorp Vault
- A7.6 Network security — VPCs, private endpoints, firewall rules
- A7.7 Audit logging and compliance (SOC 2, GDPR, HIPAA considerations)
- A7.8 Content safety — Input/output filtering
- A7.9 **Lab**: Implement security layers — prompt injection defense, PII redaction, audit logging

### Module A8: Monitoring, Observability & Reliability
- A8.1 Observability pillars for agents — Logs, metrics, traces
- A8.2 Distributed tracing for multi-agent systems (OpenTelemetry)
- A8.3 LLM-specific metrics — Token usage, latency, cost, error rates
- A8.4 LangSmith / LangFuse for agent observability
- A8.5 Alerting on agent failures, hallucinations, and anomalies
- A8.6 Health checks and circuit breakers
- A8.7 Graceful degradation — Fallback strategies when LLM APIs go down
- A8.8 Disaster recovery and backup strategies
- A8.9 **Lab**: Set up full observability stack — Grafana, Prometheus, OpenTelemetry for agents

### Module A9: Real-World Application — Enterprise Document Processing
- A9.1 Architecture overview — Intake → Classify → Extract → Validate → Store
- A9.2 Document classification agent — Invoices, contracts, receipts, forms
- A9.3 Data extraction agent — Key-value extraction from unstructured docs
- A9.4 Validation agent — Cross-referencing extracted data against databases
- A9.5 Human review workflow for low-confidence extractions
- A9.6 Pipeline orchestration with LangGraph
- A9.7 Azure Document Intelligence / AWS Textract integration
- A9.8 Scalable deployment on Kubernetes
- A9.9 **Lab**: Build and deploy the complete document processing pipeline

### Module A10: Real-World Application — AI-Powered Sales & CRM Agent
- A10.1 Architecture — Lead scoring, outreach, follow-up, CRM update
- A10.2 Lead qualification agent — Analyzing inbound leads
- A10.3 Personalized outreach agent — Generating tailored emails
- A10.4 Meeting scheduling agent — Calendar integration
- A10.5 CRM integration — Salesforce / HubSpot API tools
- A10.6 Multi-channel communication — Email, Slack, SMS
- A10.7 Analytics dashboard — Agent performance metrics
- A10.8 **Lab**: Build the complete sales agent system with CRM integration

### Module A11: Real-World Application — Autonomous DevOps Agent
- A11.1 Architecture — Monitor → Diagnose → Fix → Verify
- A11.2 Monitoring agent — Detecting anomalies in logs and metrics
- A11.3 Diagnostic agent — Root cause analysis using tools
- A11.4 Remediation agent — Executing fix actions with approval gates
- A11.5 Incident communication agent — Slack/Teams notifications
- A11.6 Integration with PagerDuty, Datadog, Grafana
- A11.7 Safety: Human-in-the-loop for destructive operations
- A11.8 **Lab**: Build an autonomous incident response agent

### Module A12: Real-World Application — Multi-Tenant AI Platform
- A12.1 Architecture for SaaS agentic AI platforms
- A12.2 Tenant isolation — Data, models, agents per customer
- A12.3 Custom agent configuration per tenant
- A12.4 Usage metering and billing (per token, per agent call)
- A12.5 White-labeling and custom branding
- A12.6 API rate limiting per tenant
- A12.7 Multi-region deployment for global availability
- A12.8 **Lab**: Build a multi-tenant agent platform with tenant isolation

### Module A13: Advanced Capstone Project
- A13.1 Project: **Production Agentic AI Platform on Cloud**
  - Multi-agent system deployed on Kubernetes (choice of Azure/AWS/GCP)
  - Scalable architecture with message queues and auto-scaling
  - Production RAG with hybrid search and re-ranking
  - Full observability — Tracing, metrics, dashboards
  - Security — Prompt injection defense, PII handling, audit logs
  - CI/CD pipeline with automated testing
  - Cost optimization with model routing and caching
  - Load tested to 100+ concurrent users
- A13.2 **Lab**: Full capstone with cloud deployment and load testing

---

## Appendices

### Appendix A: Docker Lab Reference
- Lab environment setup guide
- Docker-in-Docker (DinD) configuration
- Pre-built lab images index
- Troubleshooting common lab issues

### Appendix B: Model Comparison Guide
- Ollama model recommendations by use case
- Cloud model pricing comparison (Claude, GPT, Gemini)
- Model selection decision tree

### Appendix C: Tool & Framework Quick Reference
- LangChain cheat sheet
- LangGraph cheat sheet
- CrewAI cheat sheet
- Ollama command reference
- Vector database comparison

### Appendix D: Cloud Cost Calculators
- Azure cost estimation for agentic workloads
- AWS cost estimation for agentic workloads
- GCP cost estimation for agentic workloads
- Cost optimization checklist

---

## Learning Path Summary

```
BEGINNER (4-5 weeks)                INTERMEDIATE (5-6 weeks)           ADVANCED (6-8 weeks)
─────────────────────               ─────────────────────────          ──────────────────────
LLM Foundations                     Agent Architectures                Production Architecture
Local Setup (Ollama)                LangGraph Workflows                Containerization (K8s)
Python for AI                       Human-in-the-Loop                  Cloud: Azure/AWS/GCP
Prompt Engineering                  Advanced RAG                       Scalability & Cost
What are Agents                     Multi-Agent (CrewAI)               Security & Compliance
Tool Calling                        Memory Systems                     Monitoring & Observability
LangChain Basics                    Structured Outputs                 Real-World: Doc Processing
Basic RAG                           Complex Tool Integration           Real-World: Sales/CRM Agent
Provider Abstraction                Agent Testing                      Real-World: DevOps Agent
Capstone: FAQ Bot                   Capstone: Support System           Real-World: Multi-Tenant SaaS
                                                                       Capstone: Cloud Platform
```

---

*NMMR Technologies Private Limited — Agentic AI Training Program*
*Version 1.0 | 2025*
