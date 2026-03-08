# Course I9: Agent Evaluation & Testing

> **Test and evaluate AI agents systematically** — Unit test tools, integration test workflows, use LLM-as-judge for output quality, benchmark with test datasets, and set up continuous evaluation with LangSmith.

### Goal: Build a comprehensive testing and evaluation pipeline for AI agents

---

## I9.1 Why Testing Agents is Different from Testing Software
- Non-deterministic outputs — The same input can produce different outputs
- Semantic correctness — Output may be "correct" in many different wordings
- Multi-step evaluation — Each step in an agent loop can succeed or fail
- Tool interaction testing — Verifying tool calls are correct and results are used properly
- Regression challenges — Agent behavior can change with model updates
- The evaluation spectrum — Exact match → Semantic similarity → LLM-as-judge
- Testing strategy — Layers of testing for comprehensive coverage

## I9.2 Unit Testing Tools and Individual Components (Lab)
- Testing tools in isolation — Calling tools directly with known inputs
- Mock data — Creating test fixtures for tool inputs and expected outputs
- Edge case testing — Empty inputs, invalid parameters, large data
- Error handling tests — Verifying tools handle failures gracefully
- Performance testing — Measuring tool execution time and resource usage
- Prompt template testing — Verifying rendered prompts match expectations
- Output parser testing — Ensuring parsers handle various LLM output formats
- pytest integration — Organizing agent tests with pytest fixtures and parametrize

## I9.3 Integration Testing Agent Workflows (Lab)
- End-to-end testing — Running the complete agent pipeline
- Test scenarios — Defining input/expected-output pairs for full workflows
- Mocking LLM calls — Replacing real LLM calls with deterministic responses
- Mocking tool calls — Simulating external APIs and databases
- Snapshot testing — Comparing agent traces against known-good traces
- State verification — Checking intermediate state at each agent step
- Multi-turn testing — Testing conversational agents across multiple turns
- CI/CD integration — Running agent tests in automated pipelines

## I9.4 LLM-as-Judge — Using a Model to Evaluate Agent Outputs (Lab)
- The concept — Use a powerful LLM to evaluate another LLM's output
- Judge prompts — Designing evaluation criteria and scoring rubrics
- Scoring dimensions — Relevance, accuracy, completeness, helpfulness, safety
- Binary evaluation — Pass/fail judgments for specific criteria
- Likert scale evaluation — 1-5 scoring for nuanced assessment
- Pairwise comparison — Comparing two outputs to determine which is better
- Reference-based judging — Comparing against a gold-standard answer
- Multi-judge consensus — Using multiple judges to reduce bias
- Calibrating judges — Ensuring consistent evaluation across runs

## I9.5 Benchmarking with Test Datasets (Lab)
- Building test datasets — Curating question-answer pairs for your domain
- Dataset format — Input, expected output, metadata, difficulty tags
- Automated benchmarking — Running agents against entire datasets
- Metrics calculation — Accuracy, F1, BLEU, ROUGE, semantic similarity
- Performance baselines — Establishing baseline scores to measure improvement
- Dataset versioning — Tracking dataset changes over time
- Domain-specific benchmarks — Creating benchmarks for your specific use case
- Benchmark reporting — Generating clear, actionable reports

## I9.6 Regression Testing — Catching Agent Behavior Changes
- Why regression testing — Model updates, prompt changes, and tool changes can break things
- Golden test sets — A curated set of critical test cases that must always pass
- Behavioral contracts — Defining invariants that should never change
- Diff detection — Identifying when agent outputs change significantly
- Automated regression suites — Running regression tests on every code change
- Alerting on regressions — Notifications when quality drops below thresholds
- Version pinning — Locking model versions to prevent unexpected changes

## I9.7 LangSmith for Tracing and Evaluation (Lab)
- What is LangSmith — LangChain's platform for tracing, debugging, and evaluating agents
- Setting up LangSmith — API key, environment variables, enabling tracing
- Trace visualization — Viewing the complete agent execution tree
- Run comparisons — Comparing different agent configurations side by side
- Datasets in LangSmith — Creating and managing evaluation datasets
- Evaluators — Built-in and custom evaluators for automated scoring
- Experiments — Running agents against datasets and tracking scores over time
- Feedback collection — Capturing human feedback on agent outputs
- Monitoring — Production observability with LangSmith
