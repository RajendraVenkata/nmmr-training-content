# Course B3: LLM API Keys & Interaction Reference

> *A hands-on reference guide — one lesson per provider. Come back anytime you need a refresher on setting up or calling a specific LLM API.*

### Goal: Know how to set up, authenticate, and interact with every major LLM provider

---

## B3.1 Anthropic Claude (Lab)
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

## B3.2 OpenAI (GPT) (Lab)
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

## B3.3 Google Gemini (Lab)
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

## B3.4 Meta Llama (Lab)
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

## B3.5 Mistral AI (Lab)
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

## B3.6 Cohere (Lab)
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

## B3.7 Ollama — Run Any LLM Locally (Lab)
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

## B3.8 Amazon Bedrock (Lab)
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

## B3.9 Azure OpenAI Service (Lab)
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

## B3.10 Hugging Face — The Open AI Platform (Lab)
- What is Hugging Face — The GitHub of machine learning: models, datasets, Spaces, and inference
- Creating a Hugging Face account — Sign-up walkthrough, profile setup
- Generating access tokens — Settings → Access Tokens, fine-grained vs read/write tokens
- Token management — Token scoping (read, write, fine-grained), revocation, organization tokens
- Understanding usage limits — Free tier (Inference API rate limits), Pro subscription, Enterprise plans
- Setting up billing — Pro plan features, Inference Endpoints pricing, Spaces GPU billing
- Installing the SDK — `pip install huggingface_hub transformers`, verifying installation
- Hugging Face Hub — Browsing models, filtering by task (text-generation, embeddings, image), model cards
- The Inference API (Serverless) — Free hosted inference for popular models
- Inference API endpoint — `https://api-inference.huggingface.co/models/{model_id}`, required headers (`Authorization: Bearer`)
- Request format — `inputs` (text prompt), `parameters` (temperature, max_new_tokens, top_p)
- Response format — Parsing `generated_text`, handling different task outputs
- Streaming responses — Using SSE with the Inference API for real-time output
- Chat Completions compatible endpoint — OpenAI-compatible API for chat models
- Using OpenAI SDK with Hugging Face — `OpenAI(base_url="https://api-inference.huggingface.co/v1")` for seamless switching
- `huggingface_hub` Python client — `InferenceClient` for typed, easy API calls
- Multi-turn conversations — Building chat history with `InferenceClient.chat_completion()`
- Popular models on Hub — Llama, Mistral, Phi, Gemma, Qwen, Falcon, StarCoder, BLOOM
- Gated models — Accepting license agreements for restricted models (Llama, Gemma)
- Downloading models locally — `huggingface-cli download`, `snapshot_download()`, cache management
- Running models locally with Transformers — `pipeline()`, `AutoModelForCausalLM`, `AutoTokenizer`
- Text generation pipeline — Loading a model, generating text, configuring generation parameters
- Embeddings — Using Sentence Transformers and embedding models from the Hub
- Inference Endpoints (Dedicated) — Deploying models on dedicated GPU infrastructure
- Creating an Inference Endpoint — Choosing model, instance type (GPU), region, scaling options
- Spaces — Hosting Gradio/Streamlit demos, GPU-accelerated Spaces
- Datasets — Browsing and loading datasets with `datasets` library for fine-tuning and evaluation
- Fine-tuning on Hugging Face — AutoTrain, Trainer API, pushing fine-tuned models to Hub
- Model evaluation — Using `evaluate` library, Open LLM Leaderboard for benchmarking
- Error handling — Handling `401` (invalid token), `429` (rate limit), `503` (model loading) responses
- Best practices — Caching models locally, choosing the right inference method (API vs local vs Endpoint), model size vs quality

## B3.11 Quick Comparison & Cheat Sheet (Lab)
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
