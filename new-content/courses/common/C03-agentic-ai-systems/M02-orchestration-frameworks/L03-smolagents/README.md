# L03: smolagents - Code-First Agents

## Overview

This lesson introduces smolagents, a code-first agent framework from Hugging Face where agents write and execute Python code blocks instead of making JSON-based tool calls. You will learn how code agents achieve greater expressiveness for complex operations and integrate with the Hugging Face ecosystem.

## Topics Covered

- Code agents vs JSON-based tool call agents
- Writing and executing Python code blocks as agent actions
- Expressiveness advantages for complex multi-step operations
- Hugging Face model and dataset integration
- Security considerations for code execution
- When code-first agents outperform tool-calling agents

## Lab: Building a Code-First Agent with smolagents

Build an agent using smolagents that solves complex tasks by generating and executing Python code, leveraging the expressiveness of code to handle operations that would be cumbersome with predefined tool schemas.

### Lab Objectives

- Set up a smolagents environment with a supported LLM backend
- Create custom tools that the code agent can invoke within generated code
- Build an agent that solves a multi-step data processing task by writing Python code
- Implement safety boundaries for code execution (sandboxing, timeout limits)
- Compare the code agent's approach with an equivalent JSON tool-calling agent

## Key Takeaways

- Code agents write executable Python instead of selecting from predefined tool schemas, enabling far greater flexibility
- The code-first approach excels at tasks requiring data manipulation, conditional logic, or chaining multiple operations
- smolagents integrates natively with Hugging Face models and datasets, simplifying access to the ML ecosystem
- Code execution introduces security risks that must be mitigated through sandboxing, timeouts, and restricted imports
- Code agents are best suited for technical users and use cases where the action space is too large for predefined tools
