# Course B4: Prompt Engineering Fundamentals

> **Master the art and science of communicating with LLMs** — Learn how to craft effective prompts, use system messages, apply prompting techniques, and get structured outputs reliably.

### Goal: Write effective prompts that produce consistent, high-quality LLM responses

---

## B4.1 What is Prompt Engineering and Why It Matters
- Defining prompt engineering — The practice of designing inputs to get desired outputs from LLMs
- Why prompts matter — The same model produces wildly different results based on how you ask
- The prompt-output relationship — How small changes in wording create large changes in response
- Prompt engineering as a skill — Iterative refinement, testing, and evaluation
- The cost of bad prompts — Wasted tokens, wrong answers, hallucinations, inconsistent outputs
- Prompt engineering vs fine-tuning — When each approach makes sense
- The prompt development lifecycle — Draft → Test → Evaluate → Refine → Deploy

## B4.2 System Prompts vs User Prompts vs Assistant Messages
- The three message roles — `system`, `user`, `assistant` and their purposes
- System prompts — Setting persona, behavior rules, output format, and constraints
- User prompts — The actual question or instruction from the end user
- Assistant messages — Previous model responses for context continuity
- How models prioritize roles — System instructions generally take precedence
- Writing effective system prompts — Persona, rules, format, examples, edge cases
- System prompt length — Short vs detailed, when more context helps
- Multi-turn context — How conversation history affects model responses
- Token budget — Balancing system prompt length with available context window

## B4.3 Zero-Shot, Few-Shot, and Chain-of-Thought Prompting (Lab)
- Zero-shot prompting — Asking without examples, relying on model knowledge
- When zero-shot works — Simple tasks, well-known formats, clear instructions
- Few-shot prompting — Providing 2-5 examples to guide the model's output format and style
- Crafting effective few-shot examples — Diverse, representative, edge-case-covering
- The impact of example order — How example ordering affects model behavior
- Chain-of-thought (CoT) prompting — "Let's think step by step"
- Why CoT works — Breaking complex reasoning into sequential steps
- Zero-shot CoT — Adding "think step by step" without examples
- Few-shot CoT — Providing examples with reasoning chains
- Self-consistency — Generating multiple reasoning paths and taking the majority answer
- Tree-of-thought — Exploring multiple reasoning branches
- Choosing the right technique — Task complexity determines the approach

## B4.4 Structured Output — Getting JSON Responses from LLMs (Lab)
- Why structured output — Programmatic parsing, API integration, data pipelines
- Asking for JSON in the prompt — Explicit format instructions
- JSON mode — Provider-specific flags (`response_format: { type: "json_object" }`)
- Defining output schemas — Specifying exact field names, types, and nesting
- Using examples for format — Few-shot with JSON examples
- Handling nested structures — Lists, objects, arrays of objects
- Common failure modes — Missing fields, extra text around JSON, invalid syntax
- Validation and error recovery — Parsing responses, retrying on malformed output
- Pydantic for validation — Defining expected schemas, auto-validating responses
- XML and YAML alternatives — When other structured formats work better
- Tool calling as structured output — Using function calling to force schema compliance

## B4.5 Prompt Templates and Variables
- What are prompt templates — Reusable prompts with placeholder variables
- String formatting — Python f-strings, `.format()`, `string.Template`
- LangChain PromptTemplate — `PromptTemplate.from_template()`, input variables
- Chat prompt templates — `ChatPromptTemplate` with system/user/assistant message templates
- Dynamic few-shot — Selecting examples based on input similarity
- Template composition — Combining multiple templates into complex prompts
- Parameterized system prompts — Adjusting behavior based on user context
- Template versioning — Tracking prompt changes over time
- Template libraries — Building a reusable collection of proven prompts

## B4.6 Common Pitfalls and How to Avoid Them (Lab)
- Vague instructions — Being too ambiguous leads to inconsistent outputs
- Information overload — Too much context confuses the model
- Conflicting instructions — Contradictory rules cause unpredictable behavior
- Positional bias — Models pay more attention to the beginning and end
- Sycophancy — Models agreeing with incorrect user statements
- Prompt injection risks — User input overriding system instructions
- Not specifying output format — Getting prose when you need structured data
- Ignoring edge cases — Prompts that work for happy paths but fail on edge cases
- Over-relying on temperature — Using temperature when prompt clarity is the real issue
- Not testing with diverse inputs — Prompts that work for one example but fail generally
