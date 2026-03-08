# Course B1: Foundations of AI & Large Language Models

> **A standalone introductory course** — No coding required. Understand what AI is, how LLMs work, and the landscape of models before writing a single line of code.

### Goal: Build a solid conceptual understanding of AI, LLMs, and the ecosystem

---

## Module B1.1: What is Artificial Intelligence
- A brief history of AI — Turing test, expert systems, machine learning, deep learning
- Types of AI — Narrow AI vs General AI vs Super AI
- Machine learning fundamentals — Supervised, unsupervised, reinforcement learning
- Deep learning — Neural networks, layers, weights, and biases
- The AI timeline — Key milestones from 1950 to today
- AI in everyday life — Recommendations, search, voice assistants, self-driving cars
- The generative AI revolution — Why 2022-2025 changed everything
- **Lab**: Explore AI applications — Identify AI in 10 products you use daily

## Module B1.2: What are Large Language Models (LLMs)
- From rule-based NLP to neural language models — The evolution
- What makes a model "large" — Parameters, training data, compute
- How LLMs are trained — Pre-training on internet text, supervised fine-tuning, RLHF
- The pre-training process — Next-token prediction at massive scale
- Fine-tuning explained — Adapting a base model for specific tasks
- RLHF (Reinforcement Learning from Human Feedback) — How models learn to be helpful
- Instruction tuning — Teaching models to follow directions
- Base models vs Chat models — Why you chat with fine-tuned versions
- Emergent abilities — Capabilities that appear only at scale (reasoning, in-context learning)
- **Lab**: Compare a base model vs a chat model — Observe the difference in behavior

## Module B1.3: How LLMs Work — Transformers, Tokens, Attention
- The Transformer architecture — The paper that changed everything ("Attention Is All You Need")
- Encoder vs Decoder — Why most LLMs use decoder-only architecture
- Tokenization — How text is broken into tokens (BPE, SentencePiece, tiktoken)
- Token vocabulary — Why "tokenization" is not the same as "word splitting"
- Embeddings — Converting tokens into numerical vectors
- Positional encoding — How models understand word order
- Self-attention mechanism — How every token attends to every other token
- Multi-head attention — Parallel attention for different relationships
- Feed-forward layers — Processing after attention
- Layer stacking — How depth creates understanding
- The generation process — Autoregressive next-token prediction step by step
- Sampling strategies — Greedy decoding, beam search, top-k, top-p (nucleus sampling)
- **Lab**: Visualize tokenization — Use tiktoken to see how text is broken into tokens, count tokens for different prompts

## Module B1.4: Key Concepts Every AI Practitioner Must Know
- Context window — What it is, why it matters (4K, 8K, 32K, 128K, 1M+ tokens)
- Temperature — Controlling randomness in outputs (0.0 = deterministic, 1.0+ = creative)
- Top-p (nucleus sampling) — Probability-based token filtering
- Top-k — Limiting token candidates
- Max tokens — Controlling output length
- Stop sequences — Telling the model when to stop generating
- System prompts — Setting model behavior and persona
- Hallucinations — Why models confidently generate false information
- Causes of hallucinations — Training data gaps, probabilistic generation, sycophancy
- Mitigating hallucinations — Grounding, RAG, chain-of-thought, confidence calibration
- Latency — Time-to-first-token vs tokens-per-second
- Throughput — Requests per minute, concurrent users
- Cost — Input tokens vs output tokens pricing, why output is more expensive
- **Lab**: Experiment with temperature and top-p — Generate the same prompt 10 times at different settings and compare outputs

## Module B1.5: The LLM Landscape — Who's Who
- OpenAI — GPT-4o, GPT-4o-mini, o1, o3 — The company that started the chatbot revolution
- Anthropic — Claude Opus, Sonnet, Haiku — Focus on safety and long-context
- Google — Gemini Pro, Flash, Lite — Multimodal and massive context windows
- Meta — Llama 3.1, 3.2, 3.3 — Open-weight models powering the open-source ecosystem
- Mistral AI — Mistral Large, Small, Codestral — European AI with efficient models
- Cohere — Command R+, R, Embed, Rerank — Enterprise RAG and search specialists
- xAI — Grok — Elon Musk's AI company
- DeepSeek — DeepSeek-V3, R1 — Chinese open-source models challenging closed-source performance
- Alibaba — Qwen 2.5 — Multilingual open-weight models
- Amazon — Titan, Nova — AWS-native models
- Apple — Foundation models for on-device AI
- AI21 Labs — Jamba — Hybrid SSM-Transformer architecture
- Model leaderboards — LMSYS Chatbot Arena, Open LLM Leaderboard, MMLU benchmarks
- The pace of change — How the landscape shifts every few months
- **Lab**: Compare responses from 5 different LLMs on the same prompt — Evaluate quality, style, and accuracy

## Module B1.6: Closed-Source vs Open-Source Models
- What "closed-source" means — API-only access, no model weights, provider-controlled
- What "open-weight" means — Downloadable weights but not necessarily open training data
- What "open-source" means — Weights + training code + data (rare in LLMs)
- The licensing spectrum — Proprietary → Restricted open (Llama) → Permissive open (Apache 2.0)
- Advantages of closed-source — Higher quality, managed infrastructure, easy to use, regular updates
- Advantages of open-weight — Privacy, customization, no vendor lock-in, fine-tuning, cost control
- Privacy and data residency — Why some companies must use open models
- Cost comparison — API pricing vs self-hosting costs at different scales
- Fine-tuning ability — Full control with open models vs limited fine-tuning on APIs
- When to use closed-source — Prototyping, small scale, need the best quality, no GPU infrastructure
- When to use open-weight — Production at scale, privacy requirements, custom domains, edge deployment
- Hybrid approaches — Open models for development, closed for production (or vice versa)
- The future of open AI — Trends, regulation, and the push toward openness
- **Lab**: Deploy the same task on a closed-source model (Claude/GPT) and an open model (Llama via Ollama) — Compare quality, latency, and cost

## Module B1.7: Understanding AI Safety and Ethics
- AI alignment — Making models behave as intended
- Bias in LLMs — How training data biases appear in outputs
- Content safety — How providers filter harmful content
- Prompt injection — When users trick models into ignoring instructions
- Jailbreaking — Bypassing safety guardrails
- Responsible AI principles — Fairness, transparency, accountability, privacy
- AI regulation landscape — EU AI Act, US executive orders, global approaches
- Environmental impact — Energy consumption of training and inference
- The job market impact — How AI is changing work, not replacing it
- **Lab**: Test model safety — Try edge cases and observe how different models handle sensitive topics

## Module B1.8: The AI Development Stack
- The layers of AI development — Models → APIs → Frameworks → Applications
- LLM providers — Where the models live (OpenAI, Anthropic, Google, self-hosted)
- API layers — REST APIs, SDKs, and how applications talk to models
- Orchestration frameworks — LangChain, LlamaIndex, CrewAI — Why they exist
- Vector databases — ChromaDB, Pinecone, Weaviate — Storing knowledge for retrieval
- Agent frameworks — Tools that let LLMs take actions in the real world
- Deployment platforms — Cloud (Azure, AWS, GCP), local (Ollama), edge devices
- The full picture — How all the pieces fit together to build an AI application
- What you'll build in this program — A preview of the journey ahead
- **Lab**: Map the AI stack — Draw the architecture diagram for a simple chatbot, a RAG application, and a multi-agent system
