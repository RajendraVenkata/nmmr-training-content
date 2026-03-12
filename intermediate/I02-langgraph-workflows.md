# Module I2: LangGraph — Graph-Based Agent Workflows

## Duration: 6-8 hours | Lab: Multi-step workflow

## Learning Objectives
- Model agent workflows as directed graphs with LangGraph
- Define state schemas, nodes, and edges
- Implement conditional branching for dynamic routing
- Build cycles and loops with controlled termination
- Execute nodes in parallel for performance
- Use checkpointing for persistence and human-in-the-loop

## Topics

### I2.1 Why LangGraph — Limitations of Simple Agent Loops
- Simple ReAct loop: Linear, no branching, hard to compose
- Real-world workflows need: Branches, parallels, loops, human review
- LangGraph: Model agents as stateful graphs
- When LangGraph is overkill vs when it's essential

### I2.2 Graph Concepts — Nodes, Edges, State
- **Nodes**: Functions that process and update state (often LLM calls)
- **Edges**: Connections between nodes defining flow
- **State**: Typed data that flows through the graph and accumulates
- `StateGraph` — The main class for building graphs
- `START` and `END` — Special entry/exit nodes

### I2.3 Building Your First LangGraph Workflow
- Define a state schema with `TypedDict`
- Create node functions that read/write state
- Add edges connecting nodes
- Compile the graph
- Invoke and stream results

### I2.4 State Management with TypedDict and Pydantic
- `TypedDict` for simple state schemas
- Annotated reducers — How state updates accumulate (e.g., append to list)
- Pydantic models for validated state
- State channels and message handling
- Accessing and updating state within nodes

### I2.5 Conditional Edges — Dynamic Routing
- `add_conditional_edges` — Route based on state
- Router functions that inspect state and return next node name
- Multiple conditional branches from a single node
- Default routes and error handling paths

### I2.6 Cycles and Loops — Agents That Iterate Until Done
- Creating cycles with conditional edges back to earlier nodes
- Loop termination conditions (quality check, max iterations, convergence)
- Preventing infinite loops with counters
- Self-improving loops: Generate → Review → Revise → Check quality → Done

### I2.7 Parallel Execution — Running Multiple Nodes Simultaneously
- Fan-out: One node sends to multiple parallel nodes
- Fan-in: Merge results from parallel nodes
- `Send` API for dynamic fan-out
- Performance benefits of parallel execution

### I2.8 Lab: Build a Research → Write → Review Workflow
- Research node: Gather information (parallel web searches)
- Write node: Draft article from research
- Review node: Evaluate quality (loop back to write if needed)
- Output node: Format and deliver final result

## Lab Exercises
1. Build a simple 3-node linear graph (input → process → output)
2. Add conditional edges — Route to different processing nodes based on input type
3. Implement a self-improving loop (write → review → revise → check → done/loop)
4. Add parallel execution — Fan out to 3 research nodes, fan in results
5. Combine all patterns into the research → write → review workflow
6. Add state persistence with checkpointing — Resume a graph mid-execution

## Key Takeaways
- LangGraph makes complex agent workflows explicit and debuggable
- Conditional edges enable dynamic routing based on agent decisions
- Cycles with termination conditions create self-improving agents
- Parallel execution dramatically speeds up independent agent tasks
- State management is the backbone — Well-designed state schemas make everything easier

---
*Next: [Module I3 — Human-in-the-Loop Agents →](I03-human-in-the-loop.md)*
