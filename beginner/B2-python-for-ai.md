# Course B2: Python for AI — Quick Refresher

> **A fast-paced refresher course** — Get up to speed with the Python skills you need for AI development. Covers core syntax, API interaction, JSON handling, async programming, and environment management.

### Goal: Ensure you have the Python fundamentals needed to build AI applications

---

## Module B2.1: Python Basics Recap — Variables, Functions, Classes
- Python installation check — Verifying Python 3.10+ is installed, `python --version`
- The Python REPL — Interactive exploration, quick testing
- Variables and data types — `str`, `int`, `float`, `bool`, `None`
- Type hints — Adding type annotations for clarity (`def greet(name: str) -> str`)
- Collections — `list`, `dict`, `tuple`, `set` and when to use each
- List comprehensions — Concise list creation (`[x for x in range(10) if x > 5]`)
- Dictionary comprehensions — Building dicts inline
- String formatting — f-strings, `.format()`, template strings
- Functions — Parameters, return values, default arguments, `*args`, `**kwargs`
- Lambda functions — Anonymous functions for quick operations
- Classes and objects — `__init__`, instance methods, class methods, properties
- Dataclasses — `@dataclass` for clean data containers (heavily used in AI code)
- Pydantic models — Data validation and settings management (used by LangChain, FastAPI)
- Error handling — `try`/`except`/`finally`, custom exceptions
- Context managers — `with` statements for resource management
- Generators and iterators — `yield`, lazy evaluation for large datasets
- **Lab**: Build a simple data processor — Read a CSV, transform data using classes, output results

## Module B2.2: Working with APIs — The `requests` Library
- What is a REST API — HTTP methods (GET, POST, PUT, DELETE), status codes
- Installing requests — `pip install requests`
- Making GET requests — Fetching data, query parameters
- Making POST requests — Sending JSON payloads, headers
- Authentication — API keys in headers (`Authorization: Bearer`), query params
- Request headers — `Content-Type`, `Accept`, custom headers
- Handling responses — Status codes, `.json()`, `.text`, `.status_code`
- Error handling for APIs — Checking status codes, handling timeouts, retries
- Session objects — Reusing connections, persistent headers
- Rate limiting — Respecting API limits, implementing backoff strategies
- Timeouts — Setting connection and read timeouts
- SSL and certificates — Handling HTTPS, certificate verification
- Pagination — Handling paginated API responses
- Streaming responses — Processing large responses chunk by chunk
- **Lab**: Build an API client — Fetch data from a public API, handle errors and pagination, display results

## Module B2.3: JSON Handling for LLM Responses
- JSON basics — Structure, data types, nesting
- `json` module — `json.loads()`, `json.dumps()`, `json.load()`, `json.dump()`
- Parsing LLM responses — Extracting text, usage stats, metadata from API responses
- Pretty printing — `json.dumps(data, indent=2)` for readable output
- Navigating nested JSON — Accessing deeply nested fields safely
- Default values — Using `.get()` to avoid `KeyError`
- JSON Schema — Understanding schema definitions (used in tool calling)
- Structured output parsing — Extracting JSON from LLM text responses
- Handling malformed JSON — Common issues when LLMs generate JSON (trailing commas, comments)
- `json.JSONDecodeError` — Catching and handling parse errors gracefully
- Converting between Python objects and JSON — Serialization patterns
- Working with JSON files — Reading/writing configuration files, conversation logs
- **Lab**: Parse LLM responses — Process sample API responses from different providers, extract key fields, handle edge cases

## Module B2.4: Async Programming Basics — `asyncio` and `aiohttp`
- Why async matters for AI — Concurrent API calls, non-blocking I/O
- Sync vs async — Understanding the event loop concept
- `async` and `await` keywords — Defining and calling coroutines
- `asyncio.run()` — Entry point for async programs
- `asyncio.gather()` — Running multiple coroutines concurrently
- `asyncio.create_task()` — Scheduling coroutines for execution
- Installing aiohttp — `pip install aiohttp`
- Async HTTP requests — `aiohttp.ClientSession` for non-blocking API calls
- Making concurrent API calls — Calling multiple LLM endpoints simultaneously
- Async context managers — `async with` for sessions and connections
- Async generators — `async for` for streaming responses
- Error handling in async code — `try`/`except` in coroutines
- Semaphores — Limiting concurrent requests to respect rate limits
- `asyncio.wait()` and `asyncio.as_completed()` — Advanced concurrency patterns
- Mixing sync and async — Running async code from synchronous contexts
- Debugging async code — Common pitfalls (forgetting `await`, blocking the event loop)
- **Lab**: Concurrent LLM calls — Send the same prompt to 3 different APIs simultaneously, compare response times and outputs

## Module B2.5: Virtual Environments and Dependency Management
- Why virtual environments matter — Isolation, reproducibility, avoiding conflicts
- `venv` — Creating and activating virtual environments (`python -m venv .venv`)
- Activating on different platforms — Windows, macOS, Linux
- `pip` — Installing packages, `pip install`, `pip freeze`
- `requirements.txt` — Pinning dependencies, `pip freeze > requirements.txt`
- `pip install -r requirements.txt` — Reproducing environments
- Version pinning — `==`, `>=`, `~=`, `<` — Why exact pinning matters
- `pyproject.toml` — Modern Python project configuration
- Poetry — Dependency management with lock files (`poetry install`, `poetry add`)
- `uv` — Fast Python package installer and resolver
- `.env` files — Storing API keys and secrets securely
- `python-dotenv` — Loading environment variables from `.env` files
- `.gitignore` — Keeping secrets and virtual environments out of version control
- Project structure — Organizing an AI project (`src/`, `tests/`, `config/`, `.env`)
- **Lab**: Set up an AI project — Create a virtual environment, install AI SDKs (anthropic, openai, google-generativeai), configure `.env` with API keys, verify everything works
