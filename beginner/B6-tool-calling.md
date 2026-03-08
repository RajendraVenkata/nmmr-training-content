# Course B6: Tool Calling — Giving Agents Abilities

> **Teach LLMs to use tools** — Learn how tool/function calling works, define tools with JSON schemas, and build agents that can search, calculate, read files, and more.

### Goal: Build agents that can call external tools and functions to accomplish tasks

---

## B6.1 What is Tool/Function Calling
- Defining tool calling — The ability for an LLM to request execution of external functions
- Why tools matter — LLMs can't search the web, do math, or access databases on their own
- The tool calling paradigm — LLM generates structured tool requests, your code executes them
- Tool calling vs plugins — How modern tool calling evolved from early plugin systems
- Universal support — Tool calling available in Claude, GPT, Gemini, Llama, Mistral, and more
- Tools as the bridge — Connecting LLM intelligence to real-world capabilities

## B6.2 How Tool Calling Works — The LLM Decides, Your Code Executes
- The tool calling flow — Prompt → LLM decides to call a tool → Your code runs it → Result sent back to LLM
- Step 1: Define available tools — Tell the LLM what tools exist and their parameters
- Step 2: LLM generates a tool call — Model outputs structured JSON instead of text
- Step 3: Execute the function — Your code runs the actual function with the LLM's arguments
- Step 4: Return results — Send tool output back to the LLM for final response
- The agent loop — Repeat until the LLM decides no more tools are needed
- Parallel tool calls — Some models call multiple tools simultaneously
- Forced vs optional tool use — Requiring tool use vs letting the model decide

## B6.3 Defining Tools with JSON Schemas (Lab)
- JSON Schema basics — Types, properties, required fields, descriptions
- Tool definition structure — `name`, `description`, `parameters` (JSON Schema)
- Writing good descriptions — Clear, specific descriptions help the model choose the right tool
- Parameter descriptions — Helping the model provide correct arguments
- Required vs optional parameters — When to make parameters mandatory
- Enum constraints — Limiting parameter values to a set of options
- Nested parameters — Complex tool inputs with objects and arrays
- Provider-specific formats — How tool definitions differ across Anthropic, OpenAI, Google

## B6.4 Tool Calling with Ollama (Llama 3.1 Native Support) (Lab)
- Llama 3.1+ tool calling — Native function calling support in open models
- Setting up tool calling with Ollama — API request format with `tools` parameter
- Defining tools for Ollama — JSON Schema tool definitions
- Parsing tool call responses — Extracting function name and arguments from the response
- Executing tools and returning results — The follow-up message format
- Comparing with cloud providers — How Ollama tool calling differs from Anthropic/OpenAI
- Supported models — Which Ollama models support tool calling (Llama 3.1+, Mistral, etc.)

## B6.5 Building Your First Tool — A Calculator Agent (Lab)
- Designing a calculator tool — Operations (add, subtract, multiply, divide)
- Defining the tool schema — Parameters for operation and numbers
- Implementing the function — Python function that performs the calculation
- Wiring it together — Prompt → Tool call → Execute → Respond
- Testing edge cases — Division by zero, large numbers, invalid inputs
- The complete agent loop — End-to-end calculator agent code

## B6.6 Multiple Tools — Search + Calculator + File Reader (Lab)
- Why multiple tools — Real agents need diverse capabilities
- Defining a tool set — Array of tool definitions for different functions
- Tool selection — How the LLM chooses which tool to use
- Search tool — A simple web search or document search function
- File reader tool — Reading and extracting text from files
- Combining tools in one conversation — LLM uses different tools for different sub-tasks
- Tool chaining — Output of one tool feeds into another tool call
- Managing tool context — Keeping track of tool results in conversation history

## B6.7 Handling Tool Errors Gracefully
- Why errors happen — Network failures, invalid inputs, missing data, timeouts
- Error handling patterns — Try/except around tool execution
- Returning errors to the LLM — Letting the model know what went wrong
- Retry strategies — When the LLM should try again with different parameters
- Fallback tools — Alternative tools when the primary fails
- Graceful degradation — Answering without the tool when it's unavailable
- Timeout handling — Setting execution limits on tool calls
- Logging and observability — Tracking tool calls, errors, and latencies
