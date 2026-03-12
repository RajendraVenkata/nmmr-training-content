# Module B2: Setting Up Your Local AI Environment

## Duration: 2-3 hours | Lab: Installation + first chat

## Learning Objectives
- Install and configure Ollama on your operating system
- Pull, manage, and run local LLM models
- Understand model sizes, quantization, and VRAM requirements
- Interact with models via both CLI and REST API
- Configure GPU acceleration for faster inference

## Topics

### B2.1 Introduction to Ollama — Run LLMs on Your Machine
- What Ollama does — Local LLM runtime
- Why local models matter — Privacy, cost, speed, offline access
- System requirements — CPU, RAM, GPU recommendations

### B2.2 Installing Ollama (Linux/Mac/Windows)
- One-line install for Linux/Mac
- Windows installer and WSL2 considerations
- Verifying the installation
- Starting the Ollama service

### B2.3 Pulling and Running Your First Model
- `ollama pull llama3.1:8b` — Downloading your first model
- `ollama run llama3.1:8b` — Interactive chat
- Understanding download sizes and storage locations
- Model variants — instruct, chat, code-specialized

### B2.4 Understanding Model Sizes, Quantization, and VRAM
- What quantization is (Q4_K_M, Q5_K_M, Q8_0, FP16)
- Tradeoff: Size vs quality vs speed
- VRAM calculator — How to pick the right model for your GPU
- CPU-only vs GPU-accelerated inference

### B2.5 Ollama CLI Commands
- `ollama run` — Interactive chat
- `ollama pull` / `ollama push` — Model management
- `ollama list` — See installed models
- `ollama ps` — See running models and VRAM usage
- `ollama rm` — Remove models to free space
- `ollama create` — Create custom models with Modelfiles

### B2.6 Ollama REST API
- Base URL: `http://localhost:11434`
- `/api/generate` — Single completion
- `/api/chat` — Multi-turn conversation
- `/v1/chat/completions` — OpenAI-compatible endpoint
- Request/response format and parameters
- Streaming responses

### B2.7 Lab: Install Ollama, Pull Models, Chat via CLI and API
- Install Ollama on the lab environment
- Pull llama3.1:8b and mistral:7b
- Have conversations via CLI
- Make API calls with curl
- Compare response times between models

## Lab Exercises
1. Install Ollama and verify with `ollama --version`
2. Pull llama3.1:8b and run an interactive chat session
3. Use `curl` to call the REST API and get a completion
4. Pull a second model (mistral:7b) and compare response quality
5. Check VRAM usage with `ollama ps` while models are loaded
6. Use the OpenAI-compatible endpoint (`/v1/chat/completions`)

## Key Takeaways
- Ollama makes running local LLMs as easy as `ollama run`
- Understanding quantization helps you pick the right model for your hardware
- The REST API enables programmatic access for building applications
- The OpenAI-compatible endpoint means your code works with both local and cloud models

---
*Next: [Module B3 — Python for AI: Quick Refresher →](B03-python-for-ai.md)*
