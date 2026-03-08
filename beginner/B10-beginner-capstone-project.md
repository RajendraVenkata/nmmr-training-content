# Course B10: Beginner Capstone Project

> **Put everything together** — Build a complete AI-Powered FAQ Assistant that uses RAG, tool calling, and provider abstraction, running locally on Ollama with a one-line swap to cloud APIs.

### Goal: Build a production-ready FAQ assistant that demonstrates all beginner-level skills

---

## B10.1 Project: AI-Powered FAQ Assistant (Lab)
- Project overview — A complete AI assistant that answers questions from company documents
- Architecture design — RAG pipeline + tool calling + provider abstraction + conversation memory
- Feature: Document ingestion — Loads company documents (PDF, text, markdown)
- Feature: RAG-powered answers — Uses vector search to find relevant context before answering
- Feature: Tool calling — Live data tools (weather, calculator, date/time, web search)
- Feature: Conversation memory — Remembers previous questions in the session
- Feature: Source attribution — Shows which documents the answer came from
- Feature: Provider abstraction — Runs on Ollama locally, one-line swap to Claude/OpenAI
- Technology stack — Python, LangChain, ChromaDB, Ollama, Docker
- Project structure — Organizing code into modules (ingestion, retrieval, tools, agent, config)
- Step-by-step build — Guided walkthrough building each component
- Testing the assistant — Sample questions, edge cases, evaluating answer quality
- Docker containerization — Packaging the entire project in a Docker container
- Deployment options — Local Docker, cloud deployment with API swap
- Stretch goals — Web UI with Gradio/Streamlit, multi-user support, analytics dashboard
