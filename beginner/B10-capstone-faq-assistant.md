# Module B10: Beginner Capstone Project — AI-Powered FAQ Assistant

## Duration: 8-10 hours | Lab: Full project build

## Learning Objectives
- Combine all beginner skills into a complete, working application
- Build a RAG-powered FAQ assistant with tool calling
- Implement provider-agnostic architecture (Ollama → Claude swap)
- Structure a project for maintainability and deployment
- Test and document an agentic AI application

## Project Overview

Build a complete **AI-Powered FAQ Assistant** that:
- Loads company documents into a RAG knowledge base
- Answers questions using retrieval + generation
- Has tools for live data (weather, calculator, date/time)
- Maintains conversation history across interactions
- Runs on Ollama locally, swappable to Claude/OpenAI with a config change

## Architecture

```
User Question
      ↓
[Conversation Memory] ← Recall previous context
      ↓
[Agent (LLM + Tools)]
      ├── Tool: RAG Knowledge Base Search
      │         └── ChromaDB → Retrieve relevant docs
      ├── Tool: Calculator
      ├── Tool: Date/Time
      └── Tool: Weather (simulated)
      ↓
[LLM generates answer with context]
      ↓
Answer to User
```

## Project Structure

```
capstone-faq-assistant/
├── config/
│   ├── .env.development      # Ollama config
│   ├── .env.production        # Claude/OpenAI config
│   └── settings.py            # Configuration loader
├── data/
│   ├── documents/             # Source PDFs/text files
│   └── vectorstore/           # ChromaDB persistent storage
├── src/
│   ├── agent/
│   │   ├── __init__.py
│   │   ├── agent.py           # Main agent setup
│   │   └── prompts.py         # System prompts and templates
│   ├── tools/
│   │   ├── __init__.py
│   │   ├── rag_tool.py        # RAG knowledge base search
│   │   ├── calculator.py      # Math calculator
│   │   ├── datetime_tool.py   # Date and time
│   │   └── weather.py         # Simulated weather API
│   ├── rag/
│   │   ├── __init__.py
│   │   ├── ingest.py          # Document loading and embedding
│   │   ├── retriever.py       # Vector search
│   │   └── splitter.py        # Text chunking
│   ├── llm/
│   │   ├── __init__.py
│   │   └── provider.py        # Provider factory (Ollama/OpenAI/Claude)
│   └── memory/
│       ├── __init__.py
│       └── conversation.py    # Conversation memory management
├── tests/
│   ├── test_tools.py          # Unit tests for each tool
│   ├── test_rag.py            # RAG pipeline tests
│   ├── test_agent.py          # Agent integration tests
│   └── test_provider.py       # Provider switching tests
├── main.py                    # CLI entry point
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
└── README.md
```

## Implementation Steps

### Step 1: Project Setup (30 min)
- Initialize project structure
- Set up virtual environment and install dependencies
- Configure environment variables for Ollama

### Step 2: Provider Abstraction (45 min)
- Implement `provider.py` — Factory that returns LLM based on config
- Support Ollama, OpenAI, Anthropic
- Test with basic chat completion

### Step 3: RAG Pipeline (2 hours)
- Implement document loading (PDF, text, markdown)
- Implement text splitting with configurable chunk sizes
- Generate embeddings and store in ChromaDB
- Build retriever with similarity search
- Create the RAG search tool

### Step 4: Tools (1.5 hours)
- Build calculator tool (safe math expression evaluation)
- Build date/time tool (current date, time zones, date math)
- Build simulated weather tool (returns mock data)
- Test each tool in isolation

### Step 5: Agent Assembly (1.5 hours)
- Create system prompt for the FAQ assistant persona
- Register all tools with the agent
- Set up conversation memory
- Configure AgentExecutor with error handling and iteration limits
- Test the complete agent

### Step 6: CLI Interface (1 hour)
- Build an interactive command-line interface
- Support commands: `/help`, `/clear`, `/sources`, `/quit`
- Display source documents when RAG is used
- Show tool usage in verbose mode

### Step 7: Testing (1.5 hours)
- Unit tests for each tool
- RAG pipeline tests (ingestion, retrieval, answer quality)
- Agent integration tests (multi-turn conversations)
- Provider switching test (verify same behavior across providers)

### Step 8: Docker Packaging (1 hour)
- Write Dockerfile with multi-stage build
- Create docker-compose.yml (app + ChromaDB)
- Test containerized deployment
- Document setup and usage in README

## Lab Exercises
1. Set up the project structure and install all dependencies
2. Implement the provider factory and verify it works with Ollama
3. Build the RAG pipeline — Ingest sample documents, test retrieval
4. Implement all 4 tools and test each independently
5. Assemble the complete agent and run multi-turn conversations
6. Write tests achieving >80% coverage on tools and RAG pipeline
7. Package with Docker and verify the container runs correctly
8. (Bonus) Swap to Claude/OpenAI API and compare answer quality

## Evaluation Criteria

| Criteria | Weight | Description |
|----------|--------|-------------|
| Functionality | 30% | All features work correctly |
| RAG Quality | 20% | Relevant documents retrieved, accurate answers |
| Code Quality | 15% | Clean, well-structured, type-hinted code |
| Provider Abstraction | 15% | Seamless swap between providers |
| Testing | 10% | Meaningful tests with good coverage |
| Documentation | 10% | Clear README, code comments, setup instructions |

## Key Takeaways
- A complete agent combines RAG + tools + memory + provider abstraction
- Project structure matters — Clean separation enables maintainability
- Testing agents requires testing components individually and as a system
- Docker packaging makes your agent portable and deployable
- This architecture scales — Add more tools, better RAG, and smarter models

---
*Congratulations! You've completed the Beginner level.*
*Next: [Level 2 — Intermediate: Multi-Agent Systems →](../intermediate/00-intermediate-overview.md)*
