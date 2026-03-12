# AI Professional Training Curriculum 2026

## Overview

A comprehensive training program designed for AI professionals in 2026, covering the full spectrum from foundational skills to role-specific specializations. The curriculum is structured as **Common Courses** (required for all roles) and **Role-Based Specializations** (tailored to specific career paths).

---

## Curriculum Structure

### Common Courses (Required for All Roles)

| Code | Course | Modules | Focus |
|------|--------|---------|-------|
| C01 | [AI & LLM Foundations](./common/C01-ai-llm-foundations/) | 6 | Programming, LLM concepts, APIs, context engineering, evals, security |
| C02 | [RAG Systems - Design to Production](./common/C02-rag-systems/) | 3 | Data ingestion, retrieval techniques, production RAG |
| C03 | [Agentic AI Systems](./common/C03-agentic-ai-systems/) | 4 | Agent architecture, orchestration frameworks, design patterns, agentic RAG |
| C04 | [Production AI Engineering](./common/C04-production-ai-engineering/) | 4 | System design, observability, inference optimization, CI/CD |
| C05 | [Career Development for AI Professionals](./common/C05-career-development/) | 4 | Portfolio, interviews, personal branding, first 90 days |

### Role-Based Specializations

| Code | Specialization | Modules | Target Role |
|------|---------------|---------|-------------|
| R01 | [AI Engineer](./role-based/R01-ai-engineer/) | 4 | Applied LLM / GenAI Engineer |
| R02 | [ML Engineer](./role-based/R02-ml-engineer/) | 3 | Classical ML + GenAI hybrid |
| R03 | [AI Platform Engineer](./role-based/R03-ai-platform-engineer/) | 3 | LLM Ops / AI Infrastructure |
| R04 | [Research Engineer](./role-based/R04-research-engineer/) | 2 | Post-Training / Fine-Tuning Engineer |
| R05 | [Data & Retrieval Engineer](./role-based/R05-data-retrieval-engineer/) | 2 | Unstructured data & search pipelines |
| R06 | [Customer-Facing AI Roles](./role-based/R06-customer-facing-ai/) | 3 | Forward Deployed Engineer, TAM, Developer Advocate |
| R07 | [AI Generalist](./role-based/R07-ai-generalist/) | 2 | Outcome-driven, cross-functional AI |

---

## Learning Paths by Role

### AI Engineer
1. C01 -> C02 -> C03 -> C04 -> R01

### ML Engineer
1. C01 -> C02 -> C04 -> R02

### AI Platform Engineer
1. C01 -> C04 -> R03

### Research Engineer
1. C01 -> C02 -> R04

### Data & Retrieval Engineer
1. C01 -> C02 -> C04 -> R05

### Customer-Facing AI Roles
1. C01 -> C02 -> C03 -> C05 -> R06

### AI Generalist
1. C01 -> C02 -> C03 -> C05 -> R07

---

## Prerequisites

- Basic programming experience (any language)
- Familiarity with command line / terminal
- A computer with 16GB+ RAM recommended (for local model labs)
- Python 3.10+ installed
- Git basics

---

## Baseline Skills for All Technical AI Roles

Regardless of specialization, all learners completing this curriculum will be fluent in:

- **Programming**: Python (non-negotiable) + SQL for data access
- **AI Fundamentals**: Tokens, context windows, LLM concepts
- **Evaluation**: Building eval harnesses, measuring system reliability
- **Security**: Prompt injection defenses, data leakage controls

---

## Key Tools Across the Curriculum

| Category | Tools |
|----------|-------|
| Core Programming | Python, SQL, TypeScript |
| Orchestration & Agents | LangGraph, LlamaIndex, CrewAI, AutoGen, smolagents |
| Vector Databases | ChromaDB, Pinecone, Weaviate, PGvector |
| Inference & Serving | VLLM, Nvidia Triton, BentoML, Ollama |
| Evaluation & Quality | Ragas, LangSmith, TrueLens, Galileo |
| Observability & Tracing | LangFuse, Arize Phoenix, OpenTelemetry |
| Data Engineering | DBT, Airflow, Spark |
| Fine-Tuning & Training | Hugging Face (TRL, PEFT), Axolotl, Weights & Biases |
| App Development | FastAPI, Streamlit, Gradio |
| Enterprise Connectivity | MCP (Model Context Protocol) |
| Local Model Execution | Ollama, LiteLLM |

---

## Content Format

Each level has its own README:
- **Course README**: Overview, objectives, modules list, prerequisites
- **Module README**: Learning objectives, lessons list, key tools
- **Lesson README**: Topics covered, lab description (where applicable), key takeaways
