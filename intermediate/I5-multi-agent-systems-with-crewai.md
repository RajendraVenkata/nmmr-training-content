# Course I5: Multi-Agent Systems with CrewAI

> **Orchestrate teams of specialized AI agents** — Learn CrewAI's role-based approach to multi-agent systems with agents, tasks, crews, and processes for collaborative AI workflows.

### Goal: Build multi-agent teams that collaborate to complete complex tasks

---

## I5.1 What is CrewAI — Role-Based Multi-Agent Orchestration
- Defining CrewAI — A framework for building teams of AI agents with defined roles
- The crew metaphor — Agents as team members with specific jobs
- Why CrewAI — Simpler than building multi-agent systems from scratch
- CrewAI vs LangGraph — When to use each (role-based collaboration vs graph workflows)
- CrewAI vs AutoGen — Comparison of multi-agent frameworks
- Installing CrewAI — `pip install crewai crewai-tools`

## I5.2 Core Concepts — Agents, Tasks, Crews, Processes
- Agents — Autonomous units with a role, goal, and backstory
- Tasks — Specific assignments given to agents with expected output
- Crews — Collections of agents working together
- Processes — How the crew operates (sequential, hierarchical)
- Tools — Functions agents can use to accomplish their tasks
- Memory — Shared and individual agent memory within a crew
- The execution flow — How a crew processes tasks from start to finish

## I5.3 Defining Agent Roles — Researcher, Writer, Reviewer, Coder (Lab)
- Role design principles — Clear responsibilities, non-overlapping expertise
- The Researcher role — Gathers information, searches the web, finds facts
- The Writer role — Produces content based on research and requirements
- The Reviewer role — Critiques and improves outputs from other agents
- The Coder role — Writes, tests, and debugs code
- Custom roles — Designing agents for your specific domain
- Backstory engineering — How detailed backstories improve agent performance
- Goal specificity — Writing clear, measurable goals for each agent

## I5.4 Task Dependencies and Workflows (Lab)
- Task definition — Description, expected output, agent assignment
- Sequential tasks — Output of one task feeds into the next
- Task dependencies — Explicitly defining which tasks depend on others
- Context passing — How task outputs become context for downstream tasks
- Async tasks — Running tasks that don't block the main flow
- Task callbacks — Hooking into task completion events
- Output validation — Ensuring tasks produce the expected format

## I5.5 Sequential vs Hierarchical Crew Processes (Lab)
- Sequential process — Tasks run one by one in defined order
- Hierarchical process — A manager agent delegates and coordinates
- When to use sequential — Linear workflows with clear step order
- When to use hierarchical — Complex tasks needing dynamic delegation
- The manager agent — How it decides which agent handles what
- Hybrid approaches — Sequential phases with hierarchical sub-crews
- Performance comparison — Trade-offs between the two approaches

## I5.6 Using CrewAI with Ollama (Lab)
- Configuring CrewAI for Ollama — Setting the LLM provider to local models
- Model selection — Which Ollama models work best with CrewAI
- Performance tuning — Context window, temperature, and model size considerations
- Tool compatibility — Ensuring CrewAI tools work with Ollama
- Switching to cloud — Swapping from Ollama to Claude/GPT for production
- Cost comparison — Free local development vs cloud API costs
- Limitations — What works differently with local models vs cloud APIs
