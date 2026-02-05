# Chapter 19: Monitoring & Observability

**Last Updated:** February 5, 2026

---

## Overview

Observability is the ability to understand the internal state of a system by examining its external outputs. In complex distributed systems, comprehensive monitoring, logging, and tracing are essential for maintaining reliability and quickly diagnosing issues.

This chapter covers skills for implementing robust observability practices, from metrics collection to distributed tracing, helping you build systems that are not just monitored but truly observable.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@prometheus-expert` | Prometheus metrics | Metrics collection, alerting, PromQL |
| `@grafana-expert` | Grafana visualization | Dashboards, alerting, data exploration |
| `@datadog-expert` | Datadog platform | Full-stack observability, APM |
| `@logging-expert` | Logging systems | ELK stack, Loki, log aggregation |

---

## 19.1 Prometheus Metrics with @prometheus-expert

### Skill Introduction

The `@prometheus-expert` skill provides deep expertise in Prometheus, the open-source monitoring system that has become the de facto standard for cloud-native metrics. It helps you instrument applications, design metric architectures, and create effective alerting.

**When to use this skill:**
- Instrumenting applications with custom metrics
- Writing PromQL queries for analysis and alerting
- Designing Prometheus architecture for scale
- Creating alerting rules and runbooks
- Troubleshooting metric collection issues

**Key strengths:**
- Expert in PromQL and metric best practices
- Experience with Prometheus at scale
- Knowledge of service discovery and federation

---

### Prometheus Implementation Prompts

#### Designing a Prometheus Monitoring Stack

**Context:** You're building a Prometheus-based monitoring stack for a Kubernetes environment.

```text
@prometheus-expert Design a production Prometheus monitoring stack for our Kubernetes cluster:

Environment:
- 3 Kubernetes clusters (dev, staging, prod)
- 100+ microservices
- Need 30 days retention for metrics
- Must handle 500K samples/second
- Team of 5 manages all clusters

Requirements:
- Centralized view across clusters
- High availability for production
- Long-term storage for historical analysis
- Cost-effective storage
- Integration with PagerDuty for alerting

Current pain points:
- Prometheus OOM crashes under load
- No cross-cluster visibility
- Alert fatigue from noisy rules

Please provide:
1. Architecture design (federation, Thanos, or other)
2. Prometheus configuration for each cluster
3. Long-term storage solution (Thanos, Cortex, Mimir)
4. High availability setup
5. Resource sizing recommendations
6. Alert aggregation strategy
7. Dashboard organization
```

**Expected Output:** Complete Prometheus architecture with federation and long-term storage.

---

#### Writing Effective PromQL Queries

**Context:** You need to create queries for latency analysis and error rate monitoring.

```text
@prometheus-expert Help me write PromQL queries for our SRE dashboard:

Metrics available:
- http_request_duration_seconds (histogram)
- http_requests_total (counter with labels: method, status, handler)
- container_memory_usage_bytes
- container_cpu_usage_seconds_total

Queries needed:
1. P99 latency over 5-minute windows
2. Error rate (5xx responses / total requests)
3. Request rate by handler
4. Memory usage as percentage of limit
5. CPU usage rate
6. Apdex score (threshold: 0.5s satisfied, 2s tolerating)

For each query, include:
- The PromQL expression
- Explanation of how it works
- Common pitfalls to avoid
- Recording rule if computation is expensive
```

**Expected Output:** PromQL queries with explanations and recording rules.

---

#### Creating Alerting Rules

**Context:** You need to create meaningful alerting rules that minimize noise.

```text
@prometheus-expert Create alerting rules for our microservices platform:

Services to monitor:
- API Gateway (entry point, critical)
- User Service (authentication, high criticality)
- Order Service (business critical)
- Notification Service (lower criticality)

Alert categories needed:
- Latency degradation (P99 thresholds)
- Error rate spikes
- Availability issues
- Resource exhaustion warnings
- SLO burn rate alerts

Current problems:
- 50+ alerts firing daily
- Most are false positives
- On-call fatigue is severe
- Critical alerts buried in noise

Please provide:
1. Alert design philosophy
2. Severity level definitions
3. Alert rules for each category
4. Inhibition rules to reduce noise
5. Routing configuration for Alertmanager
6. Runbook templates for each alert type
```

**Expected Output:** Alerting rules with noise reduction strategies.

---

## 19.2 Grafana Dashboards with @grafana-expert

### Skill Introduction

The `@grafana-expert` skill provides expertise in Grafana, the leading open-source visualization platform. It helps you create informative dashboards, set up alerting, and organize observability data effectively.

**When to use this skill:**
- Creating operational dashboards
- Designing executive-level visualizations
- Setting up Grafana alerting
- Organizing dashboards and folders
- Integrating multiple data sources

**Key strengths:**
- Expert in dashboard design best practices
- Experience with various data sources
- Knowledge of Grafana provisioning and GitOps

---

### Grafana Dashboard Prompts

#### Creating an SRE Dashboard

**Context:** You need a dashboard that gives SRE teams immediate visibility into system health.

```text
@grafana-expert Design an SRE dashboard for our production environment:

Requirements:
- Single pane of glass for system health
- Works for both NOC display and incident response
- Shows RED metrics (Rate, Errors, Duration)
- Highlights anomalies and current issues
- Drill-down capability to specific services

Data sources:
- Prometheus for metrics
- Loki for logs
- Tempo for traces

Contents needed:
- Overall system health score
- Service-level error rates and latencies
- Infrastructure health (CPU, memory, disk)
- Recent deployments correlation
- Active alerts
- SLO status

Please provide:
1. Dashboard layout and design
2. Panel definitions with queries
3. Variable setup for filtering
4. Linking between dashboards
5. JSON model or provisioning YAML
6. Best practices for performance
```

**Expected Output:** Complete dashboard design with panels and queries.

---

## 19.3 Full-Stack Observability with @datadog-expert

### Skill Introduction

The `@datadog-expert` skill provides expertise in Datadog, a comprehensive cloud monitoring platform. It helps you leverage Datadog's integrated metrics, traces, and logs for full-stack observability.

**When to use this skill:**
- Implementing APM and distributed tracing
- Setting up log aggregation and analysis
- Creating monitors and alerting
- Building dashboards and notebooks
- Optimizing Datadog costs

**Key strengths:**
- Deep knowledge of Datadog products
- Experience with APM and tracing
- Understanding of cost optimization

---

### Datadog Implementation Prompts

#### Implementing APM and Tracing

**Context:** You want to implement distributed tracing across your microservices.

```text
@datadog-expert Implement Datadog APM for our microservices architecture:

Architecture:
- 25 microservices in Kubernetes
- Languages: Node.js, Python, Go
- HTTP and gRPC communication
- Kafka for async messaging
- PostgreSQL and Redis data stores

Goals:
- Trace requests across service boundaries
- Identify performance bottlenecks
- Correlate traces with logs
- Track database query performance
- Measure queue processing time

Concerns:
- Minimize performance overhead
- Control sampling for cost
- Handle high-cardinality spans

Please provide:
1. Instrumentation strategy per language
2. Agent configuration (Kubernetes DaemonSet)
3. Sampling strategy for cost control
4. Custom spans for important operations
5. Trace to log correlation setup
6. Dashboard for APM insights
7. Alerting on trace metrics
```

**Expected Output:** APM implementation plan with instrumentation and configuration.

---

## 19.4 Logging Systems with @logging-expert

### Skill Introduction

The `@logging-expert` skill provides expertise in centralized logging systems like the ELK stack, Grafana Loki, and cloud logging services. It helps you design logging architectures and extract insights from log data.

**When to use this skill:**
- Designing log aggregation architectures
- Implementing structured logging
- Creating log-based alerts
- Optimizing log storage and retention
- Troubleshooting logging pipeline issues

**Key strengths:**
- Experience with major logging platforms
- Knowledge of log parsing and enrichment
- Understanding of cost optimization

---

### Logging System Prompts

#### Designing a Logging Architecture

**Context:** You need a centralized logging system for compliance and troubleshooting.

```text
@logging-expert Design a centralized logging architecture:

Requirements:
- Aggregate logs from 50 services
- 30 days hot storage, 1 year cold storage
- Fast search for incident investigation
- Compliance with data retention policies
- Correlation between logs and traces
- Cost-effective storage

Log sources:
- Application logs (JSON structured)
- Kubernetes system logs
- Load balancer access logs
- Database audit logs

Volume:
- 500GB logs per day
- Peak: 100K events per second

Please provide:
1. Architecture design (ELK, Loki, or cloud-native)
2. Log collection and shipping
3. Index design and lifecycle
4. Retention and archival strategy
5. Search optimization
6. Access control for sensitive logs
7. Cost estimation
```

**Expected Output:** Complete logging architecture with storage strategy.

---

## Best Practices Summary

### Metrics
1. **USE Method:** Utilization, Saturation, Errors for resources
2. **RED Method:** Rate, Errors, Duration for services
3. **Naming:** Follow naming conventions consistently
4. **Labels:** Keep cardinality under control
5. **Recording Rules:** Pre-compute expensive queries

### Alerting
1. **Symptoms Not Causes:** Alert on user impact
2. **Severity Levels:** Clear definitions and routing
3. **Runbooks:** Every alert has clear remediation steps
4. **SLO-Based:** Burn rate alerts for SLOs
5. **Noise Reduction:** Regularly review and tune

### Logging
1. **Structured Logging:** Use JSON format
2. **Correlation IDs:** Enable request tracing
3. **Log Levels:** Use appropriately (not everything is ERROR)
4. **Retention:** Match business and compliance needs
5. **Sampling:** Consider for high-volume logs

---

## Reflection Points

1. **Observability vs Monitoring:** What's the difference and why does it matter?
2. **Tool Sprawl:** How do you avoid too many observability tools?
3. **Cost Control:** How do you manage observability costs at scale?
4. **Alert Fatigue:** What strategies prevent on-call burnout?

---

**Next Chapter:** [Chapter 20: Database Administration →](chapter-20-databases.md)
