# Module B4: Prompt Engineering Fundamentals

## Duration: 4-5 hours | Lab: Prompt experiments

## Learning Objectives
- Understand the role of system, user, and assistant messages
- Apply zero-shot, few-shot, and chain-of-thought prompting techniques
- Get reliable structured (JSON) output from LLMs
- Design reusable prompt templates with variables
- Debug and iterate on prompts that produce poor results

## Topics

### B4.1 What is Prompt Engineering and Why It Matters
- The prompt is your interface to the LLM
- Small prompt changes → big output differences
- Prompt engineering as a core agentic AI skill
- The cost of bad prompts — Hallucinations, wrong format, wasted tokens

### B4.2 System Prompts vs User Prompts vs Assistant Messages
- **System prompt**: Sets the LLM's role, behavior, and constraints
- **User message**: The actual question or instruction
- **Assistant message**: Previous LLM responses (for multi-turn context)
- How models weight each role differently
- Crafting effective system prompts for agents

### B4.3 Zero-Shot, Few-Shot, and Chain-of-Thought Prompting
- **Zero-shot**: Direct instruction with no examples
- **Few-shot**: Providing 2-3 examples of desired input/output pairs
- **Chain-of-thought (CoT)**: "Think step by step" — Forcing reasoning
- **Self-consistency**: Running CoT multiple times and taking majority answer
- When to use each technique
- Cost implications (more tokens = more cost)

### B4.4 Structured Output — Getting JSON Responses from LLMs
- Why structured output matters for agents (tools need JSON)
- Prompting for JSON: "Respond in valid JSON format..."
- JSON schema in the prompt — Defining expected structure
- Common failures and workarounds
- Validation and error handling for LLM-generated JSON

### B4.5 Prompt Templates and Variables
- Parameterized prompts with f-strings
- Jinja2-style templates
- LangChain `PromptTemplate` and `ChatPromptTemplate`
- Reusable prompt libraries
- Version controlling your prompts

### B4.6 Common Pitfalls and How to Avoid Them
- Vague instructions → Vague outputs
- Contradictory constraints
- Context window overflow (too much in the prompt)
- Hallucination triggers — Asking about obscure topics
- The "just one more instruction" trap

### B4.7 Lab: Prompt Engineering Exercises with Ollama
- Craft system prompts for different agent personas
- Compare zero-shot vs few-shot on classification tasks
- Chain-of-thought for math problems
- Get reliable JSON output from Llama 3.1

## Lab Exercises
1. Write a system prompt that makes the LLM act as a Python code reviewer
2. Use few-shot prompting to classify customer support tickets into categories
3. Apply chain-of-thought to solve a multi-step word problem
4. Get the LLM to output valid JSON with a specific schema (name, age, skills)
5. Build a prompt template with variables for a product description generator
6. Debug a failing prompt — Iteratively improve it until it works reliably

## Key Takeaways
- System prompts define agent behavior — They're the most important prompt layer
- Few-shot examples dramatically improve output consistency
- Chain-of-thought unlocks reasoning for complex tasks
- Structured output (JSON) is essential for tool-calling agents
- Prompt iteration is a skill — Start simple, test, refine

---
*Next: [Module B5 — Introduction to AI Agents →](B05-intro-to-agents.md)*
