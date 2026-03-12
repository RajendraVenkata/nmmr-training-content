# Module B5: Introduction to AI Agents

## Duration: 3-4 hours | Lab: Conceptual + trace exercises

## Learning Objectives
- Define what an AI agent is and how it differs from a chatbot
- Understand the four components: LLM + Tools + Memory + Planning
- Trace through the ReAct (Reason-Act-Observe) loop
- Identify different types of agents and their use cases
- Know when to use agents vs simpler approaches

## Topics

### B5.1 What is an AI Agent — Beyond Chatbots
- Chatbot: Takes input → Generates output (one shot)
- Agent: Takes a goal → Plans → Uses tools → Iterates → Achieves goal
- The key difference: Agents have autonomy and can take actions
- Real-world examples: Coding assistants, research agents, customer support

### B5.2 Agent = LLM + Tools + Memory + Planning
- **LLM (Brain)**: The reasoning engine that decides what to do
- **Tools (Hands)**: External capabilities — Search, calculate, read files, call APIs
- **Memory (Context)**: Conversation history + long-term knowledge
- **Planning (Strategy)**: Breaking goals into steps, deciding order of execution
- How these four components work together

### B5.3 The ReAct Pattern — Reason → Act → Observe → Repeat
- **Reason**: LLM thinks about what to do next
- **Act**: LLM decides to call a tool with specific parameters
- **Observe**: The tool executes and returns results
- **Repeat**: LLM processes results and decides next action (or gives final answer)
- The termination condition — When does the agent stop?
- Tracing through a complete agent loop step by step

### B5.4 Types of Agents
- **Conversational agents**: Multi-turn dialogue with context
- **Task-oriented agents**: Complete a specific goal (book a flight, file a report)
- **Autonomous agents**: Long-running, self-directed (AutoGPT-style)
- **Collaborative agents**: Multiple agents working together
- Choosing the right type for your use case

### B5.5 Agent vs Chain vs Simple LLM Call — When to Use What
- **Simple LLM call**: Single question → single answer (FAQ, translation)
- **Chain**: Fixed sequence of LLM calls (summarize → translate → format)
- **Agent**: Dynamic — LLM decides what to do based on the situation
- Decision framework: Start simple, add complexity only when needed
- Over-engineering warning — Not everything needs an agent

### B5.6 Real-World Agent Examples and Use Cases
- Customer support agent (tool: knowledge base search, ticket creation)
- Research assistant (tool: web search, document reading)
- Code generation agent (tool: code execution, file writing)
- Data analysis agent (tool: SQL queries, chart generation)
- DevOps agent (tool: log analysis, service restart)

### B5.7 Lab: Trace Through an Agent's Reasoning Loop
- Walk through a pre-built agent's execution trace
- Identify each Reason-Act-Observe step
- Predict what the agent should do next at each step
- Identify failure cases and how to handle them

## Lab Exercises
1. Read an agent execution trace and label each step (Reason/Act/Observe)
2. Given a goal, manually write out the agent's planning steps
3. Identify which tools an agent would need for 5 different scenarios
4. Design an agent architecture (LLM + Tools + Memory) for a recipe assistant
5. Compare a chain vs agent approach for the same task — Note the tradeoffs

## Key Takeaways
- Agents are LLMs that can reason, plan, and take actions using tools
- The ReAct loop (Reason → Act → Observe) is the core agent pattern
- Four components define an agent: LLM, Tools, Memory, Planning
- Not everything needs an agent — Start simple and add complexity when needed
- Understanding the agent loop is essential before building one

---
*Next: [Module B6 — Tool Calling: Giving Agents Abilities →](B06-tool-calling.md)*
