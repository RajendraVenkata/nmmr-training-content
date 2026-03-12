# L01: Container Orchestration for AI

## Overview

Learn how to containerize and orchestrate AI workloads using Docker and Kubernetes, with special attention to GPU-aware scheduling and container optimization for model serving. This lesson covers the unique infrastructure requirements of AI workloads compared to traditional applications.

## Topics Covered

- Docker for AI workloads: base images, CUDA drivers, model packaging
- Kubernetes basics for AI: deployments, services, resource management
- GPU-aware scheduling with NVIDIA device plugins
- Container optimization for model serving: image size, startup time, health checks

## Lab: Deploying an AI Model in a Containerized Environment with GPU Support

Build and deploy a containerized AI model serving application on Kubernetes with GPU support, including proper resource requests, health checks, and rolling updates.

### Lab Objectives

- Create a Docker image optimized for AI model serving with GPU support
- Deploy the containerized model on Kubernetes with GPU resource requests
- Configure health checks and readiness probes for model warm-up
- Implement rolling updates that maintain availability during model version changes

## Key Takeaways

- AI containers require GPU driver compatibility, large model files, and specific CUDA versions, making them distinct from typical web service containers
- GPU-aware scheduling ensures models land on nodes with the right GPU type and available memory
- Container startup time is critical for autoscaling; optimize image size and model loading
- Health checks must account for model warm-up time to avoid routing traffic to unready instances
