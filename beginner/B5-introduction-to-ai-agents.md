# Course B5: Introduction to AI Agents

> **Understand what AI agents are and how they work** — Go beyond simple chatbots to learn the core concepts of autonomous AI agents including the ReAct pattern, agent types, and real-world use cases.

### Goal: Understand the architecture and reasoning patterns behind AI agents

---

## B5.1 What is an AI Agent — Beyond Chatbots
- Chatbot vs Agent — A chatbot responds, an agent takes action
- Defining an AI agent — An LLM that can perceive, reason, plan, and act autonomously
- The agency spectrum — From simple completion to fully autonomous systems
- What makes agents powerful — They can use tools, access data, and make decisions
- Examples of agents in production — Customer support, code assistants, research agents, workflow automation
- The agent revolution — Why agents are the next frontier of AI applications

## B5.2 Agent = LLM + Tools + Memory + Planning
- The four pillars of an agent — LLM (brain), Tools (hands), Memory (context), Planning (strategy)
- The LLM as the reasoning engine — Decision-making, natural language understanding
- Tools — Functions the agent can call (search, calculate, read files, call APIs)
- Memory — Short-term (conversation) and long-term (persistent knowledge)
- Planning — Breaking complex tasks into subtasks, choosing next actions
- How the pillars interact — The agent loop: perceive → think → decide → act → observe

## B5.3 The ReAct Pattern — Reason → Act → Observe → Repeat (Lab)
- What is ReAct — Reasoning and Acting interleaved in a loop
- The ReAct cycle — Thought → Action → Observation → Thought → ...
- Thought — The model reasons about what to do next
- Action — The model calls a tool or takes a step
- Observation — The result of the action feeds back into the next thought
- Why ReAct works — Explicit reasoning improves decision quality
- ReAct vs direct prompting — When reasoning chains outperform single-shot answers
- ReAct trace — Reading and understanding an agent's reasoning log
- Stopping conditions — How the agent knows when it's done (final answer, max iterations)

## B5.4 Types of Agents — Conversational, Task-Oriented, Autonomous
- Conversational agents — Chat-based, maintain dialog, answer questions
- Task-oriented agents — Focused on completing a specific job (book a flight, fill a form)
- Autonomous agents — Self-directed, long-running, goal-seeking (AutoGPT-style)
- Reactive agents — Respond to events without long-term planning
- Proactive agents — Anticipate needs and act without being asked
- Single-purpose vs general-purpose — Specialized agents vs Swiss Army knife agents
- Choosing agent type — Matching agent design to your use case

## B5.5 Agent vs Chain vs Simple LLM Call — When to Use What
- Simple LLM call — One prompt, one response, no tools needed
- Chains — Sequential steps: prompt → LLM → parse → prompt → LLM → output
- Agents — Dynamic, the LLM decides what to do next based on context
- When to use simple calls — Translation, summarization, classification
- When to use chains — Known multi-step workflows, data transformation pipelines
- When to use agents — Open-ended tasks, tool use required, dynamic decision-making
- Cost and complexity trade-offs — Agents are powerful but more expensive and harder to debug
- The principle of minimal complexity — Use the simplest approach that solves the problem

## B5.6 Real-World Agent Examples and Use Cases
- Customer support agents — Answering questions, looking up orders, processing refunds
- Code assistants — Writing, reviewing, debugging, and deploying code
- Research agents — Searching the web, summarizing papers, compiling reports
- Data analysis agents — Querying databases, generating charts, explaining insights
- Workflow automation agents — Processing emails, scheduling meetings, filing documents
- Creative agents — Writing content, generating marketing copy, brainstorming ideas
- DevOps agents — Monitoring systems, responding to alerts, running diagnostics
- The future of agents — Where the technology is heading
