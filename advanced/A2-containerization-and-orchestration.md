# Course A2: Containerization & Orchestration

> **Package and deploy AI agents with Docker and Kubernetes** — Best practices for AI containers, multi-stage builds, Docker Compose, DinD sandboxing, Kubernetes fundamentals, operators, and Helm charts.

### Goal: Containerize and orchestrate multi-agent systems for production deployment

---

## A2.1 Docker Best Practices for AI Applications
- Base image selection — `python:3.11-slim` vs `python:3.11-bookworm` vs distroless
- Layer optimization — Ordering Dockerfile instructions for efficient caching
- Dependency management — `requirements.txt` vs `poetry.lock` in Docker
- Model files in containers — When to bake in vs mount vs download at runtime
- Environment variables — Configuration via env vars, `.env` files, secrets
- Non-root users — Running containers as non-root for security
- Health checks — `HEALTHCHECK` instructions for container readiness
- `.dockerignore` — Keeping images lean by excluding unnecessary files

## A2.2 Multi-Stage Builds for Lean Agent Containers (Lab)
- Why multi-stage — Separate build dependencies from runtime
- Builder stage — Installing compilers, building C extensions, compiling assets
- Runtime stage — Minimal image with only runtime dependencies
- Copying artifacts — `COPY --from=builder` for selective file transfer
- Size comparison — Multi-stage vs single-stage image size differences
- Cache optimization — Leveraging build cache across stages
- Security scanning — Scanning final image for vulnerabilities
- Example: Agent container — Full multi-stage Dockerfile for a LangChain agent

## A2.3 Docker Compose for Multi-Agent Development Environments (Lab)
- Compose architecture — Defining multi-service agent systems
- Service definitions — Agent services, databases, vector stores, message queues
- Networking — Service discovery, DNS resolution, custom networks
- Volume management — Persistent data, shared volumes between services
- Environment configuration — `.env` files, environment-specific overrides
- Dependency ordering — `depends_on`, health checks, wait-for scripts
- Development workflow — Hot reload, debugging, log aggregation
- Profiles — Enabling/disabling services for different development scenarios

## A2.4 Docker-in-Docker (DinD) for Agent Sandboxing (Lab)
- What is DinD — Running Docker inside a Docker container
- Why DinD for agents — Isolated execution environments for untrusted code
- Security considerations — Privileged mode, socket mounting, rootless DinD
- Sysbox runtime — Secure DinD without privileged mode
- Agent sandbox pattern — Spin up a container, run code, capture output, destroy
- Resource limits — CPU, memory, disk, network limits for sandboxed containers
- Network isolation — Preventing sandboxed containers from accessing the host network
- Cleanup strategies — Automatic container removal, image pruning

## A2.5 Kubernetes Fundamentals for Agent Deployment (Lab)
- Kubernetes concepts — Pods, Deployments, Services, ConfigMaps, Secrets
- Pod design for agents — Single-agent vs sidecar vs multi-container pods
- Deployments — Rolling updates, rollback, replica management
- Services — ClusterIP, NodePort, LoadBalancer for agent exposure
- ConfigMaps and Secrets — Externalizing agent configuration and API keys
- Namespaces — Isolating environments (dev, staging, production)
- Resource requests and limits — CPU and memory allocation for agent workloads
- Persistent volumes — Storage for vector databases, model files, agent state

## A2.6 Kubernetes Operators for AI Workloads
- What are operators — Custom controllers for managing complex applications
- Why operators for AI — Automating model deployment, scaling, updates
- Existing operators — KServe, Seldon Core, NVIDIA GPU Operator
- Custom operator basics — CRDs (Custom Resource Definitions), controllers
- Agent-specific operators — Managing agent lifecycle, scaling, configuration
- GPU scheduling — Requesting and managing GPU resources in Kubernetes
- Node affinity — Scheduling agents on GPU vs CPU nodes

## A2.7 Helm Charts for Agentic System Deployment (Lab)
- What is Helm — Package manager for Kubernetes
- Chart anatomy — `Chart.yaml`, `values.yaml`, templates
- Templating — `{{ .Values }}`, conditionals, loops, helpers
- Values files — Environment-specific configuration (dev, staging, prod)
- Dependencies — Including sub-charts for databases, queues, vector stores
- Release management — Install, upgrade, rollback, history
- Chart repositories — Hosting and sharing Helm charts
- Example: Agent system chart — Complete Helm chart for a multi-agent deployment
