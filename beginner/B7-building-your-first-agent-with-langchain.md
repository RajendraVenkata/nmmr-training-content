# Course B7: Building Your First Agent with LangChain

> **Build real agents using the LangChain framework** — Learn LangChain's core abstractions, create tools, build ReAct agents, and add conversation memory — all running locally with Ollama.

### Goal: Build functional AI agents using LangChain with Ollama

---

## B7.1 What is LangChain — The Orchestration Layer
- Defining LangChain — A framework for building applications powered by LLMs
- Why LangChain — Abstractions for common patterns (agents, chains, tools, memory, retrieval)
- The LangChain ecosystem — `langchain`, `langchain-core`, `langchain-community`, `langgraph`, `langsmith`
- When to use LangChain — Complex multi-step workflows, agent systems, RAG pipelines
- When not to use LangChain — Simple API calls, minimal orchestration needed
- Installing LangChain — `pip install langchain langchain-community langchain-ollama`

## B7.2 LangChain Core Concepts — Models, Prompts, Chains, Tools, Agents
- Chat models — `ChatOllama`, `ChatOpenAI`, `ChatAnthropic` — Unified interface for all providers
- Prompt templates — `ChatPromptTemplate`, `MessagesPlaceholder` for dynamic prompts
- Chains — LCEL (LangChain Expression Language) — Piping components with `|` operator
- Output parsers — `StrOutputParser`, `JsonOutputParser`, `PydanticOutputParser`
- Tools — Functions the agent can call, decorated with `@tool`
- Agents — LLMs that dynamically choose which tools to use
- Runnables — The base interface: `.invoke()`, `.stream()`, `.batch()`

## B7.3 Setting Up LangChain with Ollama (Lab)
- Installing dependencies — `pip install langchain-ollama`
- Creating a ChatOllama instance — `ChatOllama(model="llama3.1:8b")`
- Basic invocation — `model.invoke("Hello")`, understanding `AIMessage` responses
- Streaming — `model.stream()` for real-time token output
- Prompt templates with Ollama — Building and invoking chat prompt templates
- LCEL chains — `prompt | model | parser` pipeline pattern
- Testing the setup — Verifying everything works end-to-end

## B7.4 Creating Tools with `@tool` Decorator (Lab)
- The `@tool` decorator — Turning any Python function into a LangChain tool
- Tool anatomy — Function name, docstring (description), type hints (parameter schema)
- Writing good docstrings — Clear descriptions help the agent choose correctly
- Simple tools — Calculator, current time, random number generator
- Tools with complex inputs — Multiple parameters, optional parameters
- Async tools — `async def` tools for non-blocking operations
- Tool testing — Invoking tools directly before giving them to an agent
- Custom tool classes — `BaseTool` subclass for advanced use cases

## B7.5 Building a ReAct Agent with `create_tool_calling_agent` (Lab)
- The ReAct agent in LangChain — How LangChain implements the Reason + Act pattern
- `create_tool_calling_agent()` — Creating an agent from model, tools, and prompt
- The agent prompt — System message, user input, agent scratchpad
- `AgentExecutor` — The runtime that manages the agent loop
- Binding tools to the model — How LangChain passes tool definitions to the LLM
- Running the agent — `.invoke({"input": "What is 25 * 4?"})` with tool calling
- Observing the reasoning — `verbose=True` to see the thought → action → observation loop

## B7.6 AgentExecutor — Running Agents with Verbose Tracing
- What is AgentExecutor — The orchestrator that runs the agent loop
- Configuration options — `max_iterations`, `max_execution_time`, `early_stopping_method`
- Verbose mode — Seeing every step of the agent's reasoning
- Return intermediate steps — Getting the full trace of tool calls and observations
- Handling stuck agents — Max iterations, timeout, and fallback strategies
- Error handling — `handle_parsing_errors=True` for robust execution
- Callbacks — Hooking into agent events for logging and monitoring

## B7.7 Adding Conversation Memory to Agents (Lab)
- Why memory matters — Agents need to remember previous turns in a conversation
- `ConversationBufferMemory` — Storing full conversation history
- `ConversationSummaryMemory` — Summarizing history to save tokens
- `ConversationBufferWindowMemory` — Keeping only the last N exchanges
- Adding memory to an agent — `MessagesPlaceholder` for chat history in prompts
- Stateful conversations — Maintaining context across multiple user inputs
- Memory and token limits — Managing conversation length as history grows
- Persistent memory — Saving conversation state between sessions
