# Level 1 — Beginner: Foundations of Agentic AI

## Overview

Welcome to the Beginner level of the NMMR Agentic AI Training Program. This level takes you from zero AI knowledge to building your first working AI agents — entirely on your local machine using free, open-source tools.

**Duration**: 4-5 weeks (self-paced)
**Prerequisites**: Basic Python programming knowledge
**Cost**: $0 (everything runs locally with Ollama)

---

## What You'll Learn

By the end of this level, you will:

- Understand how Large Language Models work under the hood
- Set up a complete local AI development environment with Ollama
- Master prompt engineering techniques for reliable AI outputs
- Understand what AI agents are and how they differ from chatbots
- Build agents that can call tools (search, calculate, read files)
- Use LangChain to orchestrate agent workflows
- Build a RAG (Retrieval Augmented Generation) system to chat with your own documents
- Write provider-agnostic code that runs on Ollama locally and Claude/OpenAI in production

---

## What You'll Build

| Module | Project |
|--------|---------|
| B2 | Local AI environment with Ollama |
| B4 | Prompt engineering cookbook |
| B6 | Multi-tool calculator + search agent |
| B7 | Research assistant with LangChain |
| B8 | "Chat with your PDF" RAG application |
| B9 | Provider-swappable agent |
| **B10** | **Capstone: AI-Powered FAQ Assistant** |

---

## Lab Environment

Every module includes a Docker-based lab. Each lab container comes with:

- Python 3.11+ pre-installed
- Ollama running with `llama3.1:8b` pre-loaded
- All required Python packages pre-installed
- VS Code Server (optional) for in-browser editing
- Pre-written starter code and exercises

To start any lab:
```bash
# From the training terminal
lab start beginner/B06-tool-calling
```

---

## Modules

### Module B1: Foundations of AI & Large Language Models
**Duration**: 3-4 hours | **Lab**: Guided exploration

Learn what LLMs are, how they work (transformers, tokens, attention), and the landscape of available models. Understand the key concepts — context windows, temperature, hallucinations — that you'll use throughout the course.

**Key Topics**:
- Transformer architecture simplified
- Tokenization and how models "see" text
- Pre-training and fine-tuning process
- Model landscape: OpenAI, Anthropic, Google, Meta, Mistral
- Open-source vs closed-source tradeoffs

---

### Module B2: Setting Up Your Local AI Environment
**Duration**: 2-3 hours | **Lab**: Installation + first chat

Install Ollama and run your first local LLM. Learn model management, understand quantization (why models come in different sizes), and interact with models via both CLI and REST API.

**Key Topics**:
- Ollama installation and configuration
- Model pulling and management
- Understanding model sizes and VRAM requirements
- Ollama REST API (`http://localhost:11434`)
- GPU acceleration setup

---

### Module B3: Python for AI — Quick Refresher
**Duration**: 3-4 hours | **Lab**: Python exercises

A focused refresher on the Python skills you'll need: working with APIs, handling JSON, async programming, and dependency management. If you're already comfortable with Python, you can skim this module.

**Key Topics**:
- REST API calls with `requests` and `httpx`
- JSON serialization/deserialization
- Async/await with `asyncio`
- Virtual environments and `pip`
- Type hints for better code quality

---

### Module B4: Prompt Engineering Fundamentals
**Duration**: 4-5 hours | **Lab**: Prompt experiments

Master the art of writing effective prompts. Learn system prompts, few-shot examples, chain-of-thought reasoning, and how to get reliable structured (JSON) output from LLMs.

**Key Topics**:
- System vs user vs assistant message roles
- Zero-shot, few-shot, and chain-of-thought prompting
- Getting JSON output reliably
- Prompt templates with variables
- Debugging bad outputs — prompt iteration workflow

---

### Module B5: Introduction to AI Agents
**Duration**: 3-4 hours | **Lab**: Conceptual + trace exercises

Understand what makes an AI agent different from a simple chatbot. Learn the agent loop (Reason → Act → Observe), the components of an agent (LLM, Tools, Memory, Planning), and when to use agents vs simpler approaches.

**Key Topics**:
- The agent paradigm: LLM + Tools + Memory + Planning
- ReAct pattern (Reason-Act)
- Agent types: conversational, task-oriented, autonomous
- When agents are overkill — choosing the right approach
- Agent failure modes and how to handle them

---

### Module B6: Tool Calling — Giving Agents Abilities
**Duration**: 5-6 hours | **Lab**: Build multi-tool agent

The core of agentic AI — teach your LLM to use tools. Define tools with JSON schemas, let the model decide which tool to call, execute the tool, and feed results back. Build a multi-tool agent from scratch.

**Key Topics**:
- Tool/function calling protocol
- JSON schema tool definitions
- Tool execution loop
- Error handling and retries
- Multiple tools working together
- Ollama's native tool calling (Llama 3.1)

---

### Module B7: Building Your First Agent with LangChain
**Duration**: 5-6 hours | **Lab**: Research assistant

Use LangChain to build agents without all the boilerplate. Learn LangChain's abstractions — models, prompts, chains, tools, agents — and build a research assistant that can search the web, read files, and answer questions.

**Key Topics**:
- LangChain architecture overview
- ChatOllama integration
- Custom tools with `@tool` decorator
- `create_tool_calling_agent` + `AgentExecutor`
- Adding conversation memory
- Verbose tracing for debugging

---

### Module B8: Introduction to RAG (Retrieval Augmented Generation)
**Duration**: 5-6 hours | **Lab**: Chat with PDF

Build your first RAG system — the most popular real-world LLM application pattern. Load documents, split them into chunks, create embeddings, store in a vector database (ChromaDB), and retrieve relevant context to answer questions accurately.

**Key Topics**:
- Why RAG exists — solving the knowledge problem
- Document loading (PDF, text, web pages)
- Text splitting strategies
- Embeddings and vector similarity
- ChromaDB for local vector storage
- RAG chain with LangChain
- Evaluating RAG quality

---

### Module B9: Provider Abstraction — Write Once, Run Anywhere
**Duration**: 3-4 hours | **Lab**: Multi-provider agent

The secret to cost-effective AI development: write your agent once and run it on any model. Learn to abstract your LLM provider so you develop for free on Ollama and deploy on Claude or OpenAI with a single configuration change.

**Key Topics**:
- OpenAI SDK compatibility with Ollama
- LangChain's provider abstraction
- Environment-based configuration
- Cost tracking and token monitoring
- Testing across providers
- Performance comparison: local vs cloud

---

### Module B10: Beginner Capstone Project
**Duration**: 8-10 hours | **Lab**: Full project build

Put everything together. Build a complete AI-Powered FAQ Assistant that:
- Loads company documents into a RAG knowledge base
- Answers questions using retrieval + generation
- Has tools for live data (weather, calculator, date/time)
- Maintains conversation history
- Runs on Ollama locally, swappable to Claude/OpenAI

**Deliverables**:
- Working FAQ assistant with RAG + tools
- Provider-agnostic configuration
- Documentation and testing
- Docker-composed deployment

---

## Next Steps

After completing the Beginner level, you're ready for **Level 2 — Intermediate**, where you'll build multi-agent systems, complex graph-based workflows, and production-ready patterns.

---

*NMMR Technologies — Agentic AI Training Program | Beginner Level*
