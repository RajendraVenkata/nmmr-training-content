# Course I2: LangGraph — Graph-Based Agent Workflows

> **Build complex agent workflows as graphs** — Learn LangGraph's node-edge-state model, conditional branching, cycles, parallel execution, and build sophisticated multi-step agent pipelines.

### Goal: Design and implement graph-based agent workflows using LangGraph

---

## I2.1 Why LangGraph — Limitations of Simple Agent Loops
- The problem with linear agents — Simple loops can't handle branching, retries, or parallelism
- What LangGraph solves — Explicit control flow with graph-based orchestration
- LangGraph vs LangChain agents — When to use which
- LangGraph vs other frameworks — Comparison with Prefect, Airflow, custom orchestration
- Key selling points — Persistence, streaming, human-in-the-loop, visualization
- Installing LangGraph — `pip install langgraph`

## I2.2 Graph Concepts — Nodes, Edges, State, Conditional Branching
- Graphs 101 — Nodes (functions), edges (connections), state (shared data)
- The `StateGraph` class — Creating a graph with a typed state schema
- Nodes — Python functions that receive state and return state updates
- Edges — Connecting nodes in sequence
- Conditional edges — Routing to different nodes based on state or LLM decisions
- Entry and exit points — `START` and `END` special nodes
- Graph compilation — `.compile()` to create a runnable graph

## I2.3 Building Your First LangGraph Workflow (Lab)
- Designing a simple workflow — Input → Process → Output
- Defining state — TypedDict with the fields your workflow needs
- Creating node functions — Functions that transform state
- Adding edges — Connecting nodes in order
- Compiling and running — `.compile()` then `.invoke()`
- Visualizing the graph — `.get_graph().draw_mermaid()` for diagram output
- Inspecting results — Reading final state after execution

## I2.4 State Management with TypedDict and Pydantic (Lab)
- TypedDict for state — Lightweight state definitions with type hints
- Pydantic for state — Validated, documented state with defaults
- State reducers — How multiple node outputs merge into state (replace, append, custom)
- Annotation-based reducers — `Annotated[list, operator.add]` for list accumulation
- Nested state — Complex state with sub-objects
- State channels — Separate channels for different data flows
- Debugging state — Inspecting state at each step of execution

## I2.5 Conditional Edges — Dynamic Routing Based on Agent Decisions (Lab)
- Why conditional routing — Different paths for different scenarios
- `add_conditional_edges()` — Routing based on a function's return value
- LLM-based routing — The model decides which path to take
- Classification-based routing — Route by intent, topic, or complexity
- Multi-path branching — More than two possible routes
- Default paths — Fallback when no condition matches
- Combining conditions — Complex routing logic with multiple criteria

## I2.6 Cycles and Loops — Agents That Iterate Until Done (Lab)
- Why cycles matter — Many tasks need iterative refinement
- Creating a cycle — Edge from a later node back to an earlier node
- Breaking the loop — Conditional edge that routes to END when done
- Iteration limits — Preventing infinite loops with `recursion_limit`
- Self-corrective agents — Generate → Evaluate → Retry cycle
- Reflection loops — Agent reviews its own output and improves
- Multi-step tool use — Agent calls tools repeatedly until satisfied

## I2.7 Parallel Execution — Running Multiple Nodes Simultaneously
- Why parallel execution — Speed up independent sub-tasks
- Fan-out pattern — One node dispatching to multiple parallel nodes
- Fan-in pattern — Collecting results from parallel nodes
- `Send()` API — Dynamically spawning parallel branches
- Parallel with shared state — How concurrent nodes update state safely
- Use cases — Parallel web searches, multi-document analysis, multi-model comparison
- Performance considerations — When parallelism helps vs adds overhead
