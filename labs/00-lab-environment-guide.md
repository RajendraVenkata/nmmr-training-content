# Lab Environment Guide — Docker + term.js

## Overview

Every module in the NMMR Agentic AI Training Program includes hands-on labs accessible directly from the browser via **term.js** — a terminal emulator embedded in the training website. Labs run inside Docker containers, providing isolated, reproducible environments with all dependencies pre-installed.

---

## Architecture

```
┌──────────────────────────────────────────────────────────────┐
│  Training Website (Browser)                                   │
│  ┌──────────────────────────┐ ┌────────────────────────────┐ │
│  │  Content Panel            │ │  term.js Terminal           │ │
│  │  (Markdown rendered)      │ │                             │ │
│  │                           │ │  WebSocket ↕ connection     │ │
│  └──────────────────────────┘ └─────────────┬──────────────┘ │
└──────────────────────────────────────────────┼────────────────┘
                                               │
                                               ▼
                                   ┌──────────────────────┐
                                   │  Lab Manager Service  │
                                   │  (Node.js backend)    │
                                   │  - Spawns containers  │
                                   │  - Routes WebSocket   │
                                   │  - Manages sessions   │
                                   └──────────┬───────────┘
                                              │
                              ┌───────────────┼───────────────┐
                              ▼               ▼               ▼
                     ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
                     │  Lab: B06    │ │  Lab: I02    │ │  Lab: A09    │
                     │  (DinD)      │ │  (DinD)      │ │  (DinD)      │
                     │  - Ollama    │ │  - Ollama    │ │  - K3s       │
                     │  - Python    │ │  - Postgres  │ │  - Grafana   │
                     │  - Code      │ │  - Redis     │ │  - Terraform │
                     └──────────────┘ └──────────────┘ └──────────────┘
```

---

## Docker-in-Docker (DinD) Design

Each lab runs as a **Docker-in-Docker** container, meaning the lab container itself can run Docker containers inside it. This enables:

- **Complex multi-service environments** (Ollama + Postgres + Redis + agent services)
- **Kubernetes labs** (K3s running inside the lab container)
- **Isolated networking** — Each lab has its own Docker network
- **Clean resets** — Tear down everything inside without affecting the host

### Base Lab Image Stack

```dockerfile
# Level 1: DinD Base
FROM docker:dind
# Docker daemon running inside the container

# Level 2: Development Tools
# Python 3.11, pip, git, curl, jq, vim, tmux

# Level 3: AI Tools
# Ollama runtime (CPU mode for containers, GPU passthrough optional)
# Python packages: openai, langchain, chromadb, etc.

# Level 4: Lab-specific
# Per-module dependencies, starter code, sample data
```

### Lab Image Hierarchy

```
nmmr-lab-base                    # DinD + system tools (~800MB)
├── nmmr-lab-beginner            # + Python + Ollama + basic AI libs (~2GB)
│   ├── nmmr-lab-B06             # + tool-calling starter code
│   ├── nmmr-lab-B07             # + LangChain exercises
│   └── nmmr-lab-B08             # + RAG sample docs + ChromaDB
├── nmmr-lab-intermediate        # + Postgres + Redis + advanced libs (~3GB)
│   ├── nmmr-lab-I02             # + LangGraph exercises
│   ├── nmmr-lab-I05             # + CrewAI exercises
│   └── nmmr-lab-I10             # + Full capstone starter
└── nmmr-lab-advanced            # + K3s + monitoring + cloud CLIs (~4GB)
    ├── nmmr-lab-A03             # + Azure CLI + Terraform
    ├── nmmr-lab-A09             # + Doc processing pipeline
    └── nmmr-lab-A13             # + Full capstone starter
```

---

## Lab Lifecycle

### Starting a Lab

```bash
# User clicks "Start Lab" button on training website, or types:
lab start beginner/B06-tool-calling

# What happens behind the scenes:
# 1. Lab Manager pulls/creates the lab container image
# 2. Starts a DinD container with resource limits
# 3. Mounts a persistent volume for user workspace
# 4. Starts internal services (Ollama, databases, etc.)
# 5. Connects term.js WebSocket to the container shell
# 6. User sees a terminal prompt in the browser
```

### Inside a Lab

```bash
# When the lab starts, user sees:
╔══════════════════════════════════════════════════════╗
║  NMMR Lab: B06 - Tool Calling                       ║
║  Module: Beginner → Tool Calling                     ║
║  Ollama: ✅ Running (llama3.1:8b loaded)            ║
║  Python: ✅ 3.11.9                                  ║
║  Workspace: /workspace                               ║
╚══════════════════════════════════════════════════════╝

$ ls /workspace/
exercises/          # Step-by-step exercise files
solutions/          # Reference solutions (hidden until requested)
starter-code/       # Pre-written boilerplate
data/               # Sample data for exercises
README.md           # Lab instructions

$ cat README.md
# Lab B06: Tool Calling
## Exercise 1: Define your first tool...
```

### Resetting a Lab

```bash
# Reset to clean state (keeps user workspace changes)
lab reset

# Full reset (destroys everything, pulls fresh image)
lab reset --hard
```

### Stopping a Lab

```bash
# Saves state, stops containers
lab stop

# State persists — restarting resumes where you left off
lab start beginner/B06-tool-calling   # Picks up from last state
```

---

## Resource Allocation Per Lab

| Level | CPU Limit | Memory Limit | Disk | GPU |
|-------|-----------|-------------|------|-----|
| Beginner | 2 cores | 4GB | 10GB | Optional |
| Intermediate | 4 cores | 8GB | 20GB | Optional |
| Advanced | 4 cores | 12GB | 30GB | Optional |

**Ollama in Labs**: Labs use CPU-mode Ollama by default (slower but works everywhere). If the host has a GPU, labs can be started with GPU passthrough:

```bash
lab start beginner/B06-tool-calling --gpu
```

---

## Pre-installed Software Per Level

### Beginner Labs

```
Runtime:        Python 3.11, Node.js 20, Docker CLI
AI Libs:        openai, anthropic, langchain, langchain-ollama,
                langchain-community, chromadb, sentence-transformers
Tools:          Ollama (with llama3.1:8b pre-pulled)
Dev Tools:      git, vim, nano, tmux, jq, curl, httpie
Python Tools:   pip, poetry, black, ruff, pytest
```

### Intermediate Labs (includes all Beginner)

```
Additional AI:  langgraph, crewai, instructor, pydantic,
                langsmith, playwright, beautifulsoup4
Databases:      PostgreSQL 16 (with pgvector), SQLite, ChromaDB
Cache:          Redis 7
APIs:           Mock API server (for tool integration exercises)
```

### Advanced Labs (includes all Intermediate)

```
Orchestration:  K3s (lightweight Kubernetes), Helm, kubectl
Cloud CLIs:     az (Azure), aws, gcloud
IaC:            Terraform, AWS CDK (via npm)
Monitoring:     Grafana, Prometheus, Jaeger, OpenTelemetry SDK
Security:       Trivy (container scanning), Bandit (Python security)
Load Testing:   Locust, k6
Additional:     docker-compose, skaffold (K8s dev workflow)
```

---

## Lab Container Specifications

### Dockerfile Pattern (Example: Beginner Lab)

```dockerfile
# ---- Stage 1: Base with DinD ----
FROM docker:24-dind AS base

RUN apk add --no-cache \
    python3 py3-pip git curl jq vim tmux bash \
    build-base libffi-dev openssl-dev

# ---- Stage 2: Python environment ----
RUN python3 -m venv /opt/venv
ENV PATH="/opt/venv/bin:$PATH"

COPY requirements-beginner.txt /tmp/
RUN pip install --no-cache-dir -r /tmp/requirements-beginner.txt

# ---- Stage 3: Ollama ----
RUN curl -fsSL https://ollama.com/install.sh | sh

# ---- Stage 4: Lab startup ----
COPY lab-entrypoint.sh /usr/local/bin/
COPY lab-welcome.sh /usr/local/bin/

WORKDIR /workspace
ENTRYPOINT ["lab-entrypoint.sh"]
```

### Entrypoint Script Pattern

```bash
#!/bin/bash
# lab-entrypoint.sh

# Start Docker daemon (DinD)
dockerd &
sleep 2

# Start Ollama in background
ollama serve &
sleep 3

# Pull model if not already cached
ollama pull llama3.1:8b 2>/dev/null || true

# Start any lab-specific services
if [ -f /lab/services.sh ]; then
    source /lab/services.sh
fi

# Show welcome message
lab-welcome.sh

# Drop into bash shell
exec bash
```

---

## term.js Integration

### WebSocket Connection

```
Browser (term.js) ←── WebSocket ──→ Lab Manager ←── Docker exec ──→ Lab Container
```

### term.js Configuration

```javascript
// Frontend: term.js setup
const terminal = new Terminal({
    cursorBlink: true,
    fontSize: 14,
    fontFamily: 'JetBrains Mono, monospace',
    theme: {
        background: '#0f172a',     // Match NMMR dark theme
        foreground: '#f8fafc',
        cursor: '#06b6d4',         // Accent color
        selectionBackground: '#3b82f6'
    }
});

// WebSocket connection to lab
const socket = new WebSocket(`wss://labs.nmmr.tech/ws/${labId}`);
terminal.onData(data => socket.send(data));
socket.onmessage = event => terminal.write(event.data);
```

### Split-Pane Layout

```
┌─────────────────────────────────────────────────────────┐
│  [Training Content ▼]  [Terminal ▼]  [Files ▼]          │  ← Tab bar
├──────────────────────────┬──────────────────────────────┤
│                          │                               │
│  ## Exercise 1           │  $ python agent.py            │
│                          │  > Agent thinking...          │
│  Define a calculator     │  > Using tool: calculator     │
│  tool with the following │  > Input: 1547 * 23           │
│  schema:                 │  > Result: 35581              │
│                          │  > Agent: The answer is       │
│  ```python               │    35,581.                    │
│  @tool                   │                               │
│  def calculator(...):    │  $                            │
│  ```                     │                               │
│                          │                               │
│  [Next Exercise →]       │  [Reset Lab] [Stop Lab]       │
├──────────────────────────┴──────────────────────────────┤
│  Progress: ████████░░░░░░░ 3/7 exercises complete        │
└─────────────────────────────────────────────────────────┘
```

---

## Lab Data Persistence

```
Host Volume Structure:
/data/labs/{userId}/
├── beginner/
│   ├── B06/workspace/        # User's modified files
│   ├── B07/workspace/
│   └── B08/workspace/
├── intermediate/
│   ├── I02/workspace/
│   └── ...
└── advanced/
    ├── A09/workspace/
    └── ...
```

- **Workspace files** persist between lab sessions (mounted as Docker volume)
- **Lab services** (databases, caches) are ephemeral (rebuilt on restart)
- **Ollama model cache** is shared across labs (avoid re-downloading)

---

## Lab CLI Commands Reference

```bash
lab start <level>/<module>      # Start a lab environment
lab stop                        # Stop the current lab
lab reset                       # Reset lab (keep workspace)
lab reset --hard                # Full reset (clean everything)
lab status                      # Show running labs and resource usage
lab list                        # List all available labs
lab hint                        # Get a hint for the current exercise
lab solution                    # Reveal the solution (tracked for analytics)
lab check                       # Validate your exercise solution
lab submit                      # Submit exercise for completion tracking
```

---

## Security Considerations

- Labs run with limited privileges (no host access beyond mounted volumes)
- Network isolation — Labs cannot access other students' containers
- Resource limits enforced — Prevents resource exhaustion
- DinD containers cannot escape to host Docker daemon
- Cloud credential labs use temporary, scoped credentials
- Lab containers auto-terminate after 4 hours of inactivity

---

## Building Lab Images

### For Training Content Developers

```bash
# Build a specific lab image
cd labs/beginner/B06-tool-calling
docker build -t nmmr-lab-b06:latest .

# Build all lab images
./scripts/build-all-labs.sh

# Push to container registry
docker push registry.nmmr.tech/nmmr-lab-b06:latest

# Test a lab locally
docker run -it --privileged \
  -p 8888:8888 \
  -v $(pwd)/workspace:/workspace \
  nmmr-lab-b06:latest
```

### Lab Image CI/CD

```yaml
# .github/workflows/build-labs.yml
# Triggers on changes to lab directories
# Builds and pushes updated lab images
# Runs lab validation tests (start, exercise check, stop)
```

---

*NMMR Technologies — Lab Environment Guide*
*Version 1.0 | 2025*
