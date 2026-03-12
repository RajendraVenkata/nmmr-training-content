# NMMR Agentic AI Training Content

> **Build Agentic AI Applications from Zero to Production**

This repository contains the complete training curriculum for the NMMR Technologies Agentic AI Training Program — a hands-on course with integrated Docker-based lab environments.

---

## Repository Structure

```
nmmr-training-content/
├── 00-course-outline.md            # Master table of contents (all 3 levels)
├── README.md                       # This file
├── trainings.md                    # LLM foundations reference material
│
├── beginner/                       # Level 1 — Foundations (4-5 weeks)
│   ├── 00-beginner-overview.md     # Level overview and learning path
│   ├── B01-llm-foundations.md
│   ├── B02-local-ai-setup.md
│   ├── B03-python-for-ai.md
│   ├── B04-prompt-engineering.md
│   ├── B05-intro-to-agents.md
│   ├── B06-tool-calling.md
│   ├── B07-langchain-basics.md
│   ├── B08-intro-to-rag.md
│   ├── B09-provider-abstraction.md
│   └── B10-capstone-faq-assistant.md
│
├── intermediate/                   # Level 2 — Multi-Agent Systems (5-6 weeks)
│   ├── 00-intermediate-overview.md
│   ├── I01-agent-architectures.md
│   ├── I02-langgraph-workflows.md
│   ├── I03-human-in-the-loop.md
│   ├── I04-advanced-rag.md
│   ├── I05-multi-agent-crewai.md
│   ├── I06-memory-systems.md
│   ├── I07-structured-outputs.md
│   ├── I08-complex-tools.md
│   ├── I09-agent-evaluation.md
│   └── I10-capstone-customer-support.md
│
├── advanced/                       # Level 3 — Production & Cloud (6-8 weeks)
│   ├── 00-advanced-overview.md
│   ├── A01-production-architecture.md
│   ├── A02-containerization-orchestration.md
│   ├── A03-cloud-azure.md
│   ├── A04-cloud-aws.md
│   ├── A05-cloud-gcp.md
│   ├── A06-scalability-cost.md
│   ├── A07-security-compliance.md
│   ├── A08-monitoring-observability.md
│   ├── A09-real-world-document-processing.md
│   ├── A10-real-world-sales-crm.md
│   ├── A11-real-world-devops-agent.md
│   ├── A12-real-world-multi-tenant.md
│   └── A13-capstone-production-platform.md
│
└── labs/                           # Docker lab environment docs
    └── 00-lab-environment-guide.md # Lab architecture, DinD, term.js integration
```

---

## Quick Start

### For Learners

1. Start with `00-course-outline.md` to see the full program
2. Navigate to `beginner/00-beginner-overview.md` for Level 1
3. Work through modules B01–B10 sequentially
4. Each module has a Docker lab — click "Start Lab" on the training website

### For Content Developers

1. Each module follows a consistent structure:
   - Title, Duration, Lab type
   - Learning Objectives
   - Topics with subtopics
   - Lab Exercises
   - Key Takeaways
   - Next module link
2. Lab Dockerfiles live alongside their module content
3. See `labs/00-lab-environment-guide.md` for lab architecture details

---

## Program Summary

| Level | Modules | Duration | Key Technologies |
|-------|---------|----------|-----------------|
| **Beginner** | B01–B10 | 4-5 weeks | Ollama, Python, LangChain, ChromaDB, basic RAG |
| **Intermediate** | I01–I10 | 5-6 weeks | LangGraph, CrewAI, advanced RAG, memory, testing |
| **Advanced** | A01–A13 | 6-8 weeks | Kubernetes, Azure/AWS/GCP, security, observability |

**Total**: 33 modules covering 15-19 weeks of content

---

## Development Approach

- **Develop on Ollama** (free, local) → **Deploy on Claude/OpenAI** (paid, production)
- Every code example works with Ollama locally via provider abstraction
- Cloud modules include both simulated (free) and real cloud (small cost) lab options

---

*NMMR Technologies Private Limited*
