# Module B3: Python for AI — Quick Refresher

## Duration: 3-4 hours | Lab: Python exercises

## Learning Objectives
- Make HTTP requests to REST APIs using `requests` and `httpx`
- Parse and construct JSON for LLM communication
- Use async/await for concurrent API calls
- Manage Python environments and dependencies
- Apply type hints for better code quality

## Topics

### B3.1 Python Basics Recap
- Variables, data types, control flow
- Functions and closures
- Classes and objects — Enough for tool definitions
- List comprehensions and generators
- Exception handling — try/except patterns

### B3.2 Working with APIs — `requests` Library
- GET and POST requests
- Headers, authentication, and API keys
- Sending JSON payloads
- Handling response status codes
- Timeout and retry patterns

### B3.3 JSON Handling for LLM Responses
- `json.loads()` / `json.dumps()` — Parse and serialize
- Navigating nested JSON structures
- Extracting data from LLM API responses
- Handling malformed JSON from LLM outputs
- `json.JSONDecodeError` handling

### B3.4 Async Programming Basics
- Why async matters for AI — Concurrent API calls
- `asyncio` event loop basics
- `async def` and `await`
- `aiohttp` for async HTTP requests
- `asyncio.gather()` — Running multiple calls in parallel
- When to use sync vs async

### B3.5 Virtual Environments and Dependency Management
- `python -m venv` — Creating isolated environments
- `pip install` and `requirements.txt`
- `pip freeze` — Locking dependencies
- Brief intro to `poetry` for modern dependency management
- `.env` files and `python-dotenv` for configuration

### B3.6 Lab: Python API Exercises Calling Ollama
- Set up a virtual environment
- Call Ollama API with `requests`
- Parse JSON responses and extract content
- Make async calls to compare multiple models simultaneously
- Build a simple CLI chat app in Python

## Lab Exercises
1. Create a virtual environment and install `requests`, `httpx`, `python-dotenv`
2. Write a Python script that sends a prompt to Ollama and prints the response
3. Parse a complex nested JSON response and extract specific fields
4. Write an async script that sends the same prompt to 3 models simultaneously
5. Build a simple interactive CLI chat loop with conversation history
6. Add error handling for timeouts, connection errors, and malformed responses

## Key Takeaways
- REST API calls with `requests` are the foundation of LLM integration
- JSON parsing is critical — LLMs communicate via structured JSON
- Async programming enables efficient parallel model calls
- Virtual environments keep your project dependencies clean and reproducible

---
*Next: [Module B4 — Prompt Engineering Fundamentals →](B04-prompt-engineering.md)*
