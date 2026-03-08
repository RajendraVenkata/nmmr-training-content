# Course I8: Agent Tools — Building Complex Integrations

> **Build production-grade tools for AI agents** — Design tools for databases, APIs, file systems, web scraping, and code execution, then compose them for complex real-world tasks.

### Goal: Build robust, production-ready tools that give agents real-world capabilities

---

## I8.1 Tool Design Principles — Clear Descriptions, Proper Schemas
- The tool design mindset — Tools are the bridge between LLM intelligence and the real world
- Naming conventions — Short, descriptive, action-oriented tool names
- Description writing — Clear, specific descriptions that help the LLM choose correctly
- Schema design — Well-defined parameters with types, descriptions, and constraints
- Input validation — Sanitizing and validating tool inputs before execution
- Output format — Consistent, parseable output that the LLM can understand
- Error messages — Informative errors that help the LLM self-correct
- Idempotency — Designing tools that are safe to retry

## I8.2 Building Database Tools — SQL Query Agents (Lab)
- Why database tools — Agents that can query and analyze data
- Read-only tools — SELECT queries for safe data retrieval
- Schema exposure — Giving the agent table/column information
- Natural language to SQL — LLM generates SQL from user questions
- Query validation — Checking SQL before execution (preventing injection, limiting scope)
- Result formatting — Converting query results into LLM-friendly text
- Parameterized queries — Preventing SQL injection with prepared statements
- Write operations — INSERT, UPDATE with approval gates
- Connection management — Connection pooling, timeouts, cleanup

## I8.3 Building API Tools — REST and GraphQL Integrations (Lab)
- REST API tools — Wrapping external APIs as agent tools
- Authentication handling — API keys, OAuth tokens, session management
- Request building — Dynamic URL construction, headers, query parameters, body
- Response parsing — Extracting relevant data from API responses
- Rate limit handling — Respecting API rate limits, implementing backoff
- GraphQL tools — Query building, variable injection, response traversal
- Pagination — Handling multi-page API responses
- Caching — Avoiding redundant API calls with response caching
- Error mapping — Translating API errors into agent-friendly messages

## I8.4 File System Tools — Reading, Writing, Transforming Files (Lab)
- File reading tools — Text, CSV, JSON, YAML, PDF, DOCX
- File writing tools — Creating and updating files safely
- Directory tools — Listing, searching, organizing files
- File transformation — Converting between formats
- Safety constraints — Sandboxing file access to specific directories
- Path validation — Preventing directory traversal attacks
- Large file handling — Streaming reads for files that don't fit in memory
- Temporary files — Working with temp directories for intermediate results

## I8.5 Web Scraping Tools — Browser Automation with Playwright (Lab)
- Why web scraping tools — Agents that can read and interact with web pages
- Playwright basics — Headless browser automation in Python
- Page navigation — Loading URLs, waiting for content, handling redirects
- Content extraction — Selecting elements, extracting text, parsing tables
- JavaScript rendering — Scraping dynamic, JS-rendered content
- Form interaction — Filling forms, clicking buttons, submitting data
- Anti-scraping considerations — Rate limiting, robots.txt, ethical scraping
- Structured extraction — Using LLMs to extract structured data from HTML

## I8.6 Code Execution Tools — Sandboxed Python Execution (Lab)
- Why code execution — Agents that can write and run code for data analysis, calculations
- Security concerns — Running untrusted code is dangerous
- Sandboxing approaches — Docker containers, subprocess with limits, restricted builtins
- Python sandbox — Limiting imports, restricting file access, timeout enforcement
- Input/output handling — Passing data in, capturing output and errors
- Memory and CPU limits — Preventing resource exhaustion
- Pre-installed packages — Making common libraries available in the sandbox
- Code review before execution — Optional human approval for generated code

## I8.7 Tool Composition — Combining Tools for Complex Tasks (Lab)
- Why composition — Real tasks require multiple tools working together
- Sequential composition — Output of one tool feeds into another
- Parallel composition — Running independent tools simultaneously
- Conditional composition — Choosing tools based on intermediate results
- Tool chains — Pre-defined sequences of tool calls
- Meta-tools — Tools that orchestrate other tools
- Context passing — Sharing data between composed tool calls
- Error propagation — Handling failures in composed tool pipelines
