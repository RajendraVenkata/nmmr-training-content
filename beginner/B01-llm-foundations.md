# Module B1: Foundations of AI & Large Language Models

## Duration: 3-4 hours | Lab: Guided exploration

## Learning Objectives
- Understand what Large Language Models are and how they evolved
- Explain the Transformer architecture at a high level
- Understand tokenization, context windows, and temperature
- Navigate the LLM landscape (OpenAI, Anthropic, Google, Meta, Mistral)
- Distinguish between open-source and closed-source models

## Topics

### B1.1 What is Artificial Intelligence — A Quick History
- From rule-based systems to machine learning to deep learning
- The breakthrough: Neural networks and GPUs
- The LLM revolution (2020-present)

### B1.2 What are Large Language Models (LLMs)
- Definition and scale (billions of parameters)
- Pre-training on internet-scale text data
- Emergent capabilities at scale

### B1.3 How LLMs Work — Transformers, Tokens, Attention
- The Transformer architecture (simplified)
- Self-attention mechanism — How models weigh word importance
- Encoder vs Decoder architectures
- Why Transformers replaced RNNs/LSTMs

### B1.4 Key Concepts
- **Context Window**: How much text the model can see at once
- **Temperature**: Controlling randomness (0 = deterministic, 1 = creative)
- **Tokens**: How models see text (not words, but sub-word pieces)
- **Hallucinations**: When models confidently produce incorrect information
- **Embeddings**: Dense vector representations of text

### B1.5 The LLM Landscape
- OpenAI (GPT-4o, GPT-4.1, o3/o4-mini)
- Anthropic (Claude 4.5, Claude 4, Haiku/Sonnet/Opus)
- Google (Gemini 2.5 Pro/Flash)
- Meta (Llama 3.x — open source)
- Mistral (Mistral Large, open-weight models)
- xAI (Grok)

### B1.6 Closed-Source vs Open-Source Models
- Tradeoffs: capability vs control vs cost
- When to use each type
- Licensing considerations for open-source models

### B1.7 Lab: Explore Different LLMs
- Chat with Ollama (Llama 3.1) via CLI
- Compare responses across models
- Experiment with temperature settings
- Count tokens and observe context window limits

## Lab Exercises
1. Install and run Ollama, chat with llama3.1:8b
2. Ask the same question to 3 different models, compare outputs
3. Experiment with temperature 0 vs 0.5 vs 1.0
4. Tokenize a paragraph and count tokens using tiktoken

## Key Takeaways
- LLMs are statistical text generators trained on massive data
- Transformers and attention are the key architectural innovations
- Understanding tokens, context windows, and temperature is essential
- Multiple providers offer models with different tradeoffs

---
*Next: [Module B2 — Setting Up Your Local AI Environment →](B02-local-ai-setup.md)*
