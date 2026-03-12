# Module B7: Building Your First Agent with LangChain

## Duration: 5-6 hours | Lab: Research assistant

## Learning Objectives
- Understand LangChain's architecture and core abstractions
- Set up LangChain with Ollama as the LLM provider
- Create custom tools using the `@tool` decorator
- Build a ReAct agent with `create_tool_calling_agent` and `AgentExecutor`
- Add conversation memory to agents for multi-turn interactions

## Topics

### B7.1 What is LangChain — The Orchestration Layer
- LangChain's role: Simplify building LLM applications
- The problem it solves: Boilerplate code for every provider, tool, and memory system
- LangChain vs building from scratch — Tradeoffs
- LangChain ecosystem: Core, Community, LangGraph, LangSmith

### B7.2 LangChain Core Concepts
- **Models**: Unified interface to any LLM (ChatOllama, ChatOpenAI, ChatAnthropic)
- **Prompts**: Template management (ChatPromptTemplate, MessagesPlaceholder)
- **Chains**: Sequential LLM call pipelines (LCEL — LangChain Expression Language)
- **Tools**: Callable functions with descriptions
- **Agents**: LLM + tools + decision-making loop
- **Memory**: Conversation history management

### B7.3 Setting Up LangChain with Ollama
- Installing `langchain`, `langchain-ollama`, `langchain-community`
- Creating a `ChatOllama` instance
- Basic invocation — `llm.invoke("Hello")`
- Streaming responses
- Configuring model parameters (temperature, max_tokens)

### B7.4 Creating Tools with `@tool` Decorator
- The `@tool` decorator — Simplest way to create tools
- Docstrings become tool descriptions (LLM reads these!)
- Type annotations define parameter schemas automatically
- Returning results — Strings, dicts, or structured data
- Testing tools in isolation before using in agents

### B7.5 Building a ReAct Agent with `create_tool_calling_agent`
- `create_tool_calling_agent` — Creates a tool-calling agent
- `AgentExecutor` — Runs the agent loop with error handling
- Prompt template with `{agent_scratchpad}` placeholder
- The execution cycle: LLM → tool call → observation → LLM → answer
- Configuring max iterations to prevent infinite loops

### B7.6 AgentExecutor — Running Agents with Verbose Tracing
- `verbose=True` — See every step of the agent's reasoning
- Understanding the trace output: Thought → Action → Observation
- `max_iterations` — Safety limit on agent loops
- `handle_parsing_errors` — Recovering from LLM output issues
- `return_intermediate_steps` — Accessing the full reasoning chain

### B7.7 Adding Conversation Memory to Agents
- Why memory matters — Multi-turn conversations need context
- `ConversationBufferMemory` — Stores full conversation history
- `MessagesPlaceholder` for injecting chat history into prompts
- Memory with agents — Maintaining context across tool calls
- Session management — Different conversations for different users

### B7.8 Lab: Build a Research Assistant Agent
- Create 3+ tools (web search simulator, calculator, note-taker)
- Build a LangChain agent with conversation memory
- Test with multi-turn research questions
- Analyze the verbose trace output

## Lab Exercises
1. Set up LangChain with ChatOllama and make a simple call
2. Create 3 custom tools with `@tool` (calculator, word counter, date/time)
3. Build a ReAct agent and run it with `AgentExecutor(verbose=True)`
4. Add `ConversationBufferMemory` for multi-turn conversation
5. Build a research assistant that can search, calculate, and take notes
6. Analyze agent traces — Identify each Reason/Act/Observe step in the output

## Key Takeaways
- LangChain provides a unified interface that works with any LLM provider
- The `@tool` decorator makes tool creation trivial — Docstrings matter
- `AgentExecutor` handles the ReAct loop, error recovery, and iteration limits
- Verbose tracing is your best debugging tool for understanding agent behavior
- Conversation memory enables multi-turn interactions essential for real applications

---
*Next: [Module B8 — Introduction to RAG →](B08-intro-to-rag.md)*
