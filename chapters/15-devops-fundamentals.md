# Chapter 15: DevOps Fundamentals

**Last Updated:** February 5, 2026

---

## Overview

DevOps represents a cultural and technical movement that bridges the gap between development and operations teams. By embracing automation, continuous integration, and infrastructure as code, organizations can deliver software faster, more reliably, and with greater confidence.

This chapter introduces foundational DevOps skills that will transform how you build, deploy, and operate software systems. Whether you're starting your DevOps journey or looking to enhance existing practices, these skills provide AI-assisted capabilities to accelerate your workflows.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@devops-expert` | General DevOps practices | Culture, processes, toolchain selection |
| `@devops-troubleshooter` | Problem solving | Debugging DevOps issues |
| `@cicd-architect` | CI/CD pipeline design | Build automation, deployment strategies |
| `@cicd-automation-workflow-automate` | Workflow automation | Automated pipelines |
| `@github-actions-templates` | GitHub Actions | CI/CD templates |
| `@github-workflow-automation` | GitHub workflows | Automation |
| `@gitlab-ci-patterns` | GitLab CI | Pipeline patterns |
| `@gitops-workflow` | GitOps | Git-centric deployments |
| `@sre-expert` | Site Reliability Engineering | Reliability, SLOs, incident management |
| `@slo-implementation` | SLO implementation | Service level objectives |
| `@on-call-handoff-patterns` | On-call | Handoff procedures |
| `@release-engineer` | Release management | Versioning, rollouts, feature flags |
| `@deployment-engineer` | Deployment | Deployment strategies |
| `@deployment-pipeline-design` | Pipeline design | CI/CD architecture |
| `@deployment-procedures` | Procedures | Deployment runbooks |

---

## 15.1 DevOps Culture and Practices with @devops-expert

### Skill Introduction

The `@devops-expert` skill provides comprehensive guidance on DevOps principles, practices, and tooling. It helps organizations adopt DevOps culture, select appropriate tools, and implement processes that improve collaboration and delivery speed.

**When to use this skill:**
- Evaluating DevOps maturity and creating improvement roadmaps
- Selecting tools for your DevOps toolchain
- Designing team structures and workflows
- Implementing DevOps metrics and KPIs

**Key strengths:**
- Deep understanding of DevOps principles (CALMS, Three Ways)
- Experience with various organizational contexts
- Practical guidance on tool selection and implementation

---

### DevOps Transformation Prompts

#### Assessing DevOps Maturity

**Context:** Your organization wants to understand its current DevOps capabilities and create an improvement plan.

```text
@devops-expert Conduct a DevOps maturity assessment for our organization:

Current state:
- 15 development teams, 200+ developers
- Mix of monolithic and microservices applications
- Manual deployments taking 2-4 hours each
- Production incidents average 3 per week
- No standardized CI/CD across teams

Areas to assess:
- Culture and collaboration
- Automation and tooling
- Measurement and metrics
- Sharing and knowledge management
- Continuous improvement practices

Please provide:
1. Maturity model framework with levels
2. Assessment questionnaire for teams
3. Scoring methodology
4. Gap analysis approach
5. Prioritized improvement roadmap
6. Quick wins vs long-term initiatives
7. Success metrics to track progress
```

**Expected Output:** Comprehensive maturity assessment framework with specific recommendations for improvement.

---

#### Building a DevOps Toolchain

**Context:** You need to design a modern DevOps toolchain for a mid-size organization.

```text
@devops-expert Design a comprehensive DevOps toolchain for our organization:

Requirements:
- Support 20 development teams
- Mix of Java, Python, Node.js, and Go applications
- Cloud-native on AWS (some on-premises legacy)
- Budget: $50K/year for tooling
- Prefer open-source where possible

Categories to cover:
- Source control and code review
- CI/CD pipelines
- Artifact management
- Infrastructure as code
- Configuration management
- Monitoring and observability
- Security scanning
- Collaboration and documentation

Please provide:
1. Tool recommendations for each category
2. Integration architecture between tools
3. Cost breakdown
4. Implementation timeline
5. Training requirements
6. Migration path from current tools
```

**Expected Output:** Complete toolchain design with tool selection rationale and integration plan.

---

#### Implementing DevOps Metrics (DORA)

**Context:** You want to measure and improve your software delivery performance using industry-standard metrics.

```text
@devops-expert Implement DORA metrics tracking for our engineering organization:

Current situation:
- No consistent metrics across teams
- Leadership asks "how fast can we ship?"
- No visibility into deployment frequency or failure rates
- Incident management is reactive

Goals:
- Track four key DORA metrics
- Benchmark against industry standards
- Create dashboards for teams and leadership
- Drive continuous improvement

Tech stack:
- GitHub for source control
- Jenkins and GitHub Actions for CI/CD
- PagerDuty for incident management
- Jira for project tracking

Please provide:
1. DORA metrics definitions and collection approach
2. Data sources and integration points
3. Dashboard design (team and org level)
4. Benchmarking methodology
5. Improvement strategies for each metric
6. Gamification ideas to drive adoption
```

**Expected Output:** Complete DORA metrics implementation guide with dashboards and improvement strategies.

---

## 15.2 CI/CD Pipeline Architecture with @cicd-architect

### Skill Introduction

The `@cicd-architect` skill specializes in designing and implementing continuous integration and continuous deployment pipelines. It helps you create automated, reliable, and fast pipelines that enable frequent, safe releases.

**When to use this skill:**
- Designing new CI/CD pipelines from scratch
- Optimizing existing pipeline performance
- Implementing advanced deployment strategies
- Troubleshooting build and deployment issues

**Key strengths:**
- Expert in major CI/CD platforms (GitHub Actions, GitLab CI, Jenkins, CircleCI)
- Deep knowledge of deployment strategies (blue-green, canary, rolling)
- Experience with pipeline security and compliance

---

### Pipeline Design Prompts

#### Designing a Multi-Environment Pipeline

**Context:** You need to create a CI/CD pipeline that promotes code through development, staging, and production environments.

```text
@cicd-architect Design a production-grade CI/CD pipeline for our microservices:

Application details:
- 15 microservices in Kubernetes
- Languages: Java (Spring Boot), Node.js, Python
- Mono-repo structure
- Average 50 commits/day across services

Environments:
- Development: Auto-deploy on commit
- Staging: Deploy after tests pass, manual approval for sensitive services
- Production: Canary deployment with automatic rollback

Requirements:
- Build time under 10 minutes
- Parallel testing where possible
- Security scanning (SAST, dependency, container)
- Quality gates with coverage thresholds
- Slack notifications for failures
- Audit trail for compliance

Please provide:
1. Pipeline architecture diagram description
2. Stage definitions and gates
3. GitHub Actions workflow files
4. Caching strategy for fast builds
5. Secret management approach
6. Rollback procedures
7. Monitoring and alerting setup
```

**Expected Output:** Complete pipeline design with workflow files and operational documentation.

---

#### Implementing Trunk-Based Development

**Context:** Your team wants to move from long-lived feature branches to trunk-based development.

```text
@cicd-architect Help us transition to trunk-based development:

Current state:
- Feature branches lasting 2-4 weeks
- Merge conflicts are common
- Integration happens late in development
- Releases are painful and risky

Goals:
- Developers commit to main multiple times per day
- All commits are production-ready
- Fast, reliable CI pipeline
- Feature flags for incomplete work

Team:
- 8 developers on one product
- Moderate test coverage (60%)
- React frontend, Node.js backend

Please provide:
1. Trunk-based development workflow design
2. Branch policies and protection rules
3. Feature flag strategy and tooling
4. CI pipeline optimizations for fast feedback
5. Testing strategy adjustments
6. Team practices and guidelines
7. Transition plan from current workflow
```

**Expected Output:** Complete trunk-based development implementation guide with workflow changes and tooling.

---

#### Optimizing Build Performance

**Context:** Your CI pipeline is too slow, causing developer frustration and reducing deployment frequency.

```text
@cicd-architect Optimize our slow CI pipeline:

Current metrics:
- Average build time: 45 minutes
- Test suite: 25 minutes
- Docker build: 12 minutes
- Deployment: 8 minutes
- Flaky test rate: 15%

Pipeline details:
- GitHub Actions
- Java Spring Boot monolith
- PostgreSQL for tests
- Docker image built every run
- 2000+ unit tests, 500+ integration tests

Goals:
- Build time under 15 minutes
- Reduce flaky tests to under 2%
- Maintain test coverage
- Cost-effective (minimize compute)

Please provide:
1. Analysis of bottlenecks
2. Caching strategies (dependencies, Docker layers, test results)
3. Test parallelization approach
4. Incremental build techniques
5. Flaky test identification and fixing
6. Pipeline configuration changes
7. Expected improvements with timelines
```

**Expected Output:** Optimization plan with specific configuration changes and expected time savings.

---

## 15.3 Site Reliability Engineering with @sre-expert

### Skill Introduction

The `@sre-expert` skill brings Google's Site Reliability Engineering practices to your organization. It helps you balance reliability with feature velocity, implement service level objectives, and build self-healing systems.

**When to use this skill:**
- Defining SLOs, SLIs, and error budgets
- Designing on-call and incident response processes
- Implementing chaos engineering
- Building observability and alerting systems

**Key strengths:**
- Deep expertise in SRE principles and practices
- Experience with large-scale distributed systems
- Practical guidance on toil reduction and automation

---

### SRE Implementation Prompts

#### Defining Service Level Objectives

**Context:** You need to establish SLOs for your customer-facing services.

```text
@sre-expert Help us define SLOs for our e-commerce platform:

Services:
- Web frontend (React, served via CDN)
- API gateway (handles 10K requests/minute)
- Order service (critical business transactions)
- Search service (powers product discovery)
- Payment service (integrates with Stripe)

Current state:
- No formal SLOs defined
- "Five nines" mentioned but not measured
- Alerts based on gut feeling
- Customer complaints are primary reliability signal

Please provide:
1. SLO methodology and framework
2. Recommended SLIs for each service type
3. Suggested SLO targets with rationale
4. Error budget policy
5. Alerting strategy based on SLOs
6. Stakeholder communication approach
7. SLO review cadence
```

**Expected Output:** Complete SLO framework with specific targets and error budget policies.

---

#### Designing Incident Response

**Context:** Your incident response is ad-hoc and stressful. You need a structured approach.

```text
@sre-expert Design an incident management process for our platform:

Current issues:
- No clear ownership during incidents
- Communication is chaotic
- Post-mortems rarely completed
- Same incidents keep recurring
- On-call is dreaded by the team

Requirements:
- Clear roles and responsibilities
- Communication templates
- Severity classification
- Escalation paths
- Blameless post-mortem process
- Learning and improvement loop

Tools available:
- PagerDuty for alerting
- Slack for communication
- Confluence for documentation

Please provide:
1. Incident severity definitions
2. Role definitions (Incident Commander, Communications, etc.)
3. Incident response playbook template
4. Communication templates for each severity
5. Post-mortem template and process
6. Metrics to track incident performance
7. On-call best practices and burnout prevention
```

**Expected Output:** Complete incident management framework with templates and playbooks.

---

#### Implementing Chaos Engineering

**Context:** You want to proactively test your system's resilience before failures happen in production.

```text
@sre-expert Help us implement chaos engineering practices:

System:
- Kubernetes-based microservices (25 services)
- AWS infrastructure (EKS, RDS, ElastiCache)
- Event-driven with Kafka
- 99.9% availability target

Goals:
- Validate our resilience assumptions
- Find weaknesses before customers do
- Build confidence in our failure handling
- Train teams on incident response

Concerns:
- Don't want to impact real customers
- Team is nervous about breaking things
- Need leadership buy-in

Please provide:
1. Chaos engineering principles and selling points
2. Maturity model for adoption
3. First experiments (low risk, high value)
4. Tool recommendations (Chaos Monkey, Litmus, Gremlin)
5. Game day runbook
6. Safety mechanisms and guardrails
7. Success metrics
```

**Expected Output:** Chaos engineering adoption plan with specific experiments and safety measures.

---

## 15.4 Release Management with @release-engineer

### Skill Introduction

The `@release-engineer` skill focuses on the art and science of releasing software safely and efficiently. It covers versioning strategies, deployment techniques, feature flags, and rollback procedures.

**When to use this skill:**
- Designing release processes and checklists
- Implementing feature flag systems
- Planning major version releases
- Creating rollback and recovery procedures

**Key strengths:**
- Expertise in semantic versioning and release strategies
- Experience with gradual rollout techniques
- Knowledge of feature flag platforms and patterns

---

### Release Management Prompts

#### Implementing Feature Flags

**Context:** You want to decouple deployment from release and enable gradual feature rollouts.

```text
@release-engineer Design a feature flag system for our application:

Requirements:
- Toggle features on/off without deployment
- Gradual rollout (percentage-based)
- User segment targeting (beta users, enterprise, etc.)
- A/B testing capability
- Audit trail for compliance
- Quick kill switch for issues

Application:
- React frontend, Node.js backend
- 500K monthly active users
- Mobile apps (iOS, Android)

Please provide:
1. Feature flag platform comparison (LaunchDarkly, Split, Unleash, custom)
2. Flag taxonomy and naming conventions
3. SDK integration patterns
4. Flag lifecycle management
5. Testing strategies with flags
6. Technical debt prevention (flag cleanup)
7. Governance and approval process
```

**Expected Output:** Feature flag strategy with platform selection and implementation patterns.

---

#### Designing a Release Train

**Context:** You want to establish a predictable release cadence for your product.

```text
@release-engineer Help us implement a release train model:

Current situation:
- Ad-hoc releases when features are "ready"
- Release dates slip frequently
- Quality varies between releases
- Stakeholders frustrated with unpredictability

Goals:
- Predictable 2-week release cycle
- Clear cut-off dates for features
- Consistent quality standards
- Hotfix process for critical issues
- Stakeholder visibility and communication

Team:
- 4 feature teams contributing to one product
- Shared QA resources
- Product managers for each team

Please provide:
1. Release train schedule template
2. Roles and responsibilities
3. Feature freeze and code freeze policies
4. Quality gates and release criteria
5. Communication plan for stakeholders
6. Hotfix process outside the train
7. Metrics to measure release health
```

**Expected Output:** Complete release train framework with schedule and processes.

---

## Best Practices Summary

### DevOps Culture
1. **Collaboration:** Break down silos between Dev and Ops
2. **Automation:** Automate everything you can
3. **Measurement:** Define and track meaningful metrics
4. **Sharing:** Foster knowledge sharing across teams
5. **Continuous Improvement:** Regular retrospectives and learning

### CI/CD
1. **Fast Feedback:** Aim for builds under 10 minutes
2. **Reliable Pipelines:** Reduce flakiness to near zero
3. **Security:** Shift security left with automated scanning
4. **Observability:** Monitor pipeline health and trends
5. **Self-Service:** Enable teams to own their pipelines

### Reliability
1. **SLOs:** Define and track service level objectives
2. **Error Budgets:** Balance reliability with innovation
3. **Blameless Culture:** Focus on systems, not individuals
4. **Chaos Engineering:** Test resilience proactively
5. **Automation:** Reduce toil through automation

---

## Reflection Points

1. **Culture vs Tools:** How do you balance cultural change with tool adoption?
2. **Metrics Gaming:** How do you prevent teams from gaming DORA metrics?
3. **Reliability Trade-offs:** When is it okay to burn error budget?
4. **On-Call Sustainability:** How do you maintain healthy on-call practices?

---

**Next Chapter:** [Chapter 16: Container Orchestration →](chapter-16-containers.md)
