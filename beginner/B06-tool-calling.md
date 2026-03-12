# Module B6: Tool Calling — Giving Agents Abilities

## Duration: 5-6 hours | Lab: Build multi-tool agent

## Learning Objectives
- Understand how tool/function calling works in LLMs
- Define tools using JSON schemas
- Implement the tool execution loop (LLM decides → code executes → results fed back)
- Build a multi-tool agent from scratch using Ollama
- Handle tool errors and edge cases gracefully

## Topics

### B6.1 What is Tool/Function Calling
- The concept: LLM outputs a structured "call this function" instruction
- Not magic — The LLM doesn't execute anything; your code does
- Why tool calling is the foundation of agentic AI
- History: From prompt-based tool use to native function calling

### B6.2 How Tool Calling Works — The LLM Decides, Your Code Executes
- Step 1: You describe available tools to the LLM (via JSON schema)
- Step 2: User sends a message
- Step 3: LLM decides whether to call a tool (or answer directly)
- Step 4: If tool call — LLM outputs: function name + arguments (JSON)
- Step 5: Your code executes the function with those arguments
- Step 6: You send the result back to the LLM
- Step 7: LLM uses the result to formulate the final answer

### B6.3 Defining Tools with JSON Schemas
- JSON Schema basics for tool definitions
- Required fields: name, description, parameters
- Parameter types: string, number, boolean, array, object
- Required vs optional parameters
- Writing good descriptions — The LLM reads these to decide when to use the tool
- Common mistakes in tool definitions

### B6.4 Tool Calling with Ollama (Llama 3.1 Native Support)
- Llama 3.1's native tool calling capability
- Using the OpenAI-compatible API with tools
- Request format with `tools` parameter
- Parsing `tool_calls` from the response
- Sending tool results back via `tool` role messages

### B6.5 Building Your First Tool — A Calculator Agent
- Define a calculator tool (evaluate math expressions)
- Implement the full tool call loop
- Handle the conversation: user → LLM → tool call → result → LLM → answer
- Testing with various math questions

### B6.6 Multiple Tools — Search + Calculator + File Reader
- Registering multiple tools simultaneously
- LLM chooses which tool to use based on the question
- Sequential tool calls — Agent uses one tool, then another
- Parallel tool calls — Multiple tools in one response

### B6.7 Handling Tool Errors Gracefully
- What happens when a tool fails
- Returning error messages to the LLM
- Retry strategies — Let the LLM try a different approach
- Timeout handling for slow tools
- Graceful degradation — Answering without tools when they're unavailable

### B6.8 Lab: Build a Multi-Tool Agent from Scratch with Ollama
- Build an agent with 3+ tools (calculator, weather, date/time)
- Implement the complete tool execution loop
- Handle errors and edge cases
- Add conversation history for multi-turn interactions

## Lab Exercises
1. Define a `get_weather` tool with proper JSON schema
2. Implement the tool call loop for a single tool (calculator)
3. Add 3 tools and let the LLM choose which to use
4. Handle a tool error — Make one tool intentionally fail and let the LLM recover
5. Build a multi-turn conversation where the agent uses tools across turns
6. Add a `read_file` tool that reads local text files

## Key Takeaways
- Tool calling is the bridge between LLM reasoning and real-world actions
- The LLM doesn't execute tools — It tells your code what to call
- Good tool descriptions are critical — The LLM uses them to decide when to call
- Error handling is essential — Tools fail, and agents must recover
- This pattern (LLM → tool call → result → LLM) is the core of all agentic systems

---
*Next: [Module B7 — Building Your First Agent with LangChain →](B07-langchain-basics.md)*
