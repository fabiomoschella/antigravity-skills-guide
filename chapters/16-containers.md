# Chapter 16: Container Orchestration

**Last Updated:** February 5, 2026

---

## Overview

Container orchestration has revolutionized how we deploy and manage applications at scale. Containers provide lightweight, consistent environments, while orchestration platforms like Kubernetes handle the complexity of running containers across clusters of machines.

This chapter covers essential skills for mastering Docker containerization and Kubernetes orchestration, enabling you to build, deploy, and operate containerized applications with confidence.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@docker-expert` | Docker containerization | Building images, container runtime, Docker Compose |
| `@docker-best-practices` | Docker best practices | Production containers |
| `@dockerfile-optimization` | Dockerfile optimization | Image size reduction |
| `@docker-compose-patterns` | Docker Compose | Multi-container apps |
| `@kubernetes-expert` | Kubernetes orchestration | Cluster management, workload deployment, scaling |
| `@kubernetes-deployment-patterns` | K8s deployment | Deployment strategies |
| `@kubernetes-yaml-generator` | K8s YAML | Manifest generation |
| `@kubernetes-manifests-best-practices` | K8s manifests | Best practices |
| `@kubernetes-config-auditor` | K8s audit | Security audit |
| `@helm-expert` | Kubernetes packaging | Chart development, release management |
| `@helm-charts-best-practices` | Helm charts | Best practices |
| `@argo-workflows` | Argo | CI/CD workflows |
| `@service-mesh-expert` | Service mesh implementation | Istio, Linkerd, traffic management |
| `@coolify` | Coolify | Self-hosted PaaS |

---

## 16.1 Docker Mastery with @docker-expert

### Skill Introduction

The `@docker-expert` skill provides comprehensive guidance on Docker containerization. From writing efficient Dockerfiles to optimizing image sizes and implementing security best practices, this skill helps you master the foundation of container-based development.

**When to use this skill:**
- Writing and optimizing Dockerfiles
- Debugging container issues
- Implementing multi-stage builds
- Designing container security practices
- Creating Docker Compose configurations

**Key strengths:**
- Deep knowledge of Docker internals and best practices
- Experience with image optimization techniques
- Security-focused container development

---

### Docker Development Prompts

#### Writing Production-Ready Dockerfiles

**Context:** You need to containerize a Node.js application for production deployment.

```text
@docker-expert Create a production-ready Dockerfile for our Node.js application:

Application details:
- Node.js 20 with TypeScript
- Express.js REST API
- Dependencies: ~100 npm packages
- Needs to run as non-root user
- Connects to PostgreSQL and Redis

Requirements:
- Multi-stage build for small final image
- Vulnerability-free base image
- Efficient layer caching for fast builds
- Health check endpoint
- Graceful shutdown handling
- Environment variable configuration

Current issues:
- Image is 1.2GB (too large)
- Builds take 8 minutes
- Running as root

Please provide:
1. Optimized multi-stage Dockerfile
2. .dockerignore file
3. Explanation of each optimization
4. Security hardening measures
5. Expected final image size
6. Build and run commands
```

**Expected Output:** Optimized Dockerfile with multi-stage build, resulting in image under 200MB.

---

#### Debugging Container Issues

**Context:** Your container is crashing in production and you need to diagnose the issue.

```text
@docker-expert Help debug our crashing Docker container:

Symptoms:
- Container exits with code 137 (OOMKilled)
- Sometimes exits with code 1 (application error)
- Works fine locally, fails in Kubernetes
- Memory limit set to 512MB

Application:
- Java Spring Boot application
- Heap size not explicitly configured
- Processes large JSON payloads

Logs show:
- "java.lang.OutOfMemoryError: Java heap space"
- Sometimes no error before exit

Please provide:
1. Diagnosis approach and tools
2. Memory analysis techniques
3. JVM configuration for containers
4. Dockerfile changes for better error handling
5. Kubernetes resource configuration
6. Monitoring recommendations
7. Prevention strategies
```

**Expected Output:** Debugging guide with JVM tuning and container configuration fixes.

---

#### Docker Compose for Development

**Context:** You need a local development environment that matches production as closely as possible.

```text
@docker-expert Create a Docker Compose setup for local development:

Application stack:
- React frontend (needs hot reload)
- Node.js API (needs hot reload)
- Python ML service
- PostgreSQL database
- Redis cache
- Elasticsearch for search
- RabbitMQ for async processing

Requirements:
- Fast startup time
- Code hot reloading for frontend and API
- Persistent data between restarts
- Easy to reset to clean state
- Matches production configuration
- Works on Mac, Windows, and Linux

Please provide:
1. docker-compose.yml with all services
2. Dockerfile.dev for development images
3. Volume mounting strategy
4. Network configuration
5. Environment variables management
6. Helper scripts (start, stop, reset, logs)
7. Documentation for team onboarding
```

**Expected Output:** Complete Docker Compose development environment with helper scripts.

---

## 16.2 Kubernetes Orchestration with @kubernetes-expert

### Skill Introduction

The `@kubernetes-expert` skill provides deep expertise in Kubernetes, the de facto standard for container orchestration. It helps you design, deploy, and operate applications on Kubernetes clusters of any size.

**When to use this skill:**
- Designing Kubernetes architectures
- Writing deployment manifests and configurations
- Troubleshooting cluster and workload issues
- Implementing security and networking policies
- Scaling and optimizing Kubernetes workloads

**Key strengths:**
- Expert knowledge of Kubernetes internals
- Experience with production cluster management
- Familiar with major managed Kubernetes platforms (EKS, GKE, AKS)

---

### Kubernetes Deployment Prompts

#### Designing a Production Deployment

**Context:** You need to deploy a microservice to Kubernetes with production-grade configuration.

```text
@kubernetes-expert Create production-ready Kubernetes manifests for our API service:

Service details:
- REST API handling 5000 requests/minute
- Stateless (session stored in Redis)
- Requires 256MB memory, 100m CPU typically
- Spikes to 1GB memory, 500m CPU under load
- Needs access to secrets (DB credentials, API keys)

Requirements:
- High availability (survive node failures)
- Automatic scaling based on CPU and custom metrics
- Zero-downtime deployments
- Resource limits to prevent noisy neighbor
- Security context (non-root, read-only filesystem)
- Network policies for isolation
- PodDisruptionBudget for maintenance

Please provide:
1. Deployment manifest with all best practices
2. Service and Ingress configuration
3. HorizontalPodAutoscaler with custom metrics
4. PodDisruptionBudget
5. NetworkPolicy
6. Secret management approach (External Secrets, Sealed Secrets)
7. Explanation of each configuration choice
```

**Expected Output:** Complete set of Kubernetes manifests following production best practices.

---

#### Implementing Zero-Downtime Deployments

**Context:** Your deployments are causing brief outages and you need to fix them.

```text
@kubernetes-expert Help us achieve true zero-downtime deployments:

Current issues:
- 5-10 seconds of 5xx errors during deployment
- Some requests timeout during rollout
- Health checks pass but app not fully ready
- Database migrations cause issues

Application:
- Spring Boot API in Kubernetes
- Rolling update strategy
- 3 replicas minimum
- Startup time: 30 seconds
- Connects to PostgreSQL

Please provide:
1. Analysis of common zero-downtime pitfalls
2. Proper readiness and liveness probe configuration
3. Startup probe for slow-starting apps
4. PreStop hook for graceful shutdown
5. Rolling update strategy tuning
6. Database migration strategy
7. Testing approach to verify zero-downtime
```

**Expected Output:** Configuration changes and process improvements for true zero-downtime deployments.

---

#### Kubernetes Troubleshooting Guide

**Context:** You're experiencing intermittent issues in your Kubernetes cluster.

```text
@kubernetes-expert Help troubleshoot our Kubernetes issues:

Symptoms:
- Pods randomly evicted (but cluster has resources)
- Intermittent network timeouts between services
- Some pods stuck in Pending state
- Memory usage doesn't match requests

Cluster:
- EKS 1.28 with 20 nodes (m5.2xlarge)
- Cluster Autoscaler enabled
- Istio service mesh
- 150 pods running

Please provide:
1. Systematic troubleshooting methodology
2. Commands for diagnosing each symptom
3. Common causes and solutions
4. Monitoring and alerting to catch issues early
5. Prevention strategies
6. Runbook for on-call engineers
```

**Expected Output:** Comprehensive troubleshooting guide with commands and runbooks.

---

## 16.3 Helm Chart Development with @helm-expert

### Skill Introduction

The `@helm-expert` skill specializes in Helm, the package manager for Kubernetes. It helps you create, manage, and deploy Helm charts for consistent, reproducible Kubernetes deployments.

**When to use this skill:**
- Creating Helm charts for your applications
- Managing chart dependencies and versions
- Implementing chart testing strategies
- Setting up Helm repositories

**Key strengths:**
- Expert in Helm chart best practices
- Experience with chart templating patterns
- Knowledge of Helm security considerations

---

### Helm Development Prompts

#### Creating a Reusable Helm Chart

**Context:** You need to create a Helm chart that can deploy your application across multiple environments.

```text
@helm-expert Create a production-grade Helm chart for our microservice:

Requirements:
- Deploy to dev, staging, and prod with different configurations
- Support for multiple replicas and autoscaling
- Ingress with TLS configuration
- ConfigMaps and Secrets management
- Service account with IRSA (AWS)
- Resource requests and limits per environment
- Health checks and security contexts

Application:
- Container image: myapp:latest
- Needs environment-specific database URLs
- Different resource requirements per environment
- Ingress hosts vary by environment

Please provide:
1. Complete chart directory structure
2. Chart.yaml and values.yaml
3. templates/deployment.yaml with conditionals
4. templates/ingress.yaml with TLS
5. templates/_helpers.tpl with utility functions
6. values-dev.yaml, values-staging.yaml, values-prod.yaml
7. NOTES.txt for post-install information
8. Chart testing with helm-unittest
```

**Expected Output:** Complete Helm chart with environment-specific values files.

---

## 16.4 Service Mesh with @service-mesh-expert

### Skill Introduction

The `@service-mesh-expert` skill provides guidance on implementing service mesh technologies like Istio and Linkerd. Service meshes add observability, security, and traffic management to microservices architectures.

**When to use this skill:**
- Evaluating service mesh solutions
- Implementing traffic management (canary, A/B testing)
- Adding mTLS encryption between services
- Setting up observability with service mesh

**Key strengths:**
- Deep knowledge of Istio and Linkerd
- Experience with traffic management patterns
- Understanding of service mesh performance implications

---

### Service Mesh Prompts

#### Implementing Istio Traffic Management

**Context:** You want to use Istio for canary deployments and traffic shifting.

```text
@service-mesh-expert Help us implement canary deployments with Istio:

Current setup:
- Istio 1.20 installed on Kubernetes
- 10 microservices with sidecar injection
- Using VirtualService for routing

Goals:
- Canary deployment with 1% traffic initially
- Automatic rollback on error rate spike
- Header-based routing for testing
- Gradual traffic shift based on metrics

Please provide:
1. VirtualService configuration for canary
2. DestinationRule for traffic policies
3. Flagger configuration for automated canary
4. Prometheus metrics to watch
5. Rollback triggers and thresholds
6. Testing the canary deployment
7. Dashboard for canary monitoring
```

**Expected Output:** Complete Istio configuration for automated canary deployments.

---

## Best Practices Summary

### Docker
1. **Multi-stage Builds:** Reduce image size significantly
2. **Non-root User:** Never run containers as root
3. **Layer Caching:** Order Dockerfile for optimal caching
4. **Security Scanning:** Scan images for vulnerabilities
5. **Minimal Base Images:** Use distroless or alpine bases

### Kubernetes
1. **Resource Limits:** Always set requests and limits
2. **Health Probes:** Implement all three probe types
3. **Security Context:** Apply principle of least privilege
4. **Network Policies:** Implement zero-trust networking
5. **Pod Disruption Budgets:** Ensure availability during maintenance

### Helm
1. **Semantic Versioning:** Version charts appropriately
2. **Values Documentation:** Document all values thoroughly
3. **Template Testing:** Test charts before deployment
4. **Dependencies:** Manage dependencies explicitly

---

## Reflection Points

1. **Container Size:** How small can you make your production images?
2. **Kubernetes Complexity:** When is Kubernetes overkill?
3. **Service Mesh Trade-offs:** What's the performance cost of a service mesh?
4. **Multi-tenancy:** How do you isolate workloads in shared clusters?

---

**Next Chapter:** [Chapter 17: Cloud Platforms →](chapter-17-cloud-platforms.md)
