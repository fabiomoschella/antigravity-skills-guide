# Chapter 22: Cost Optimization & FinOps

**Last Updated:** February 5, 2026

---

## Overview

As cloud spending grows, organizations need disciplined approaches to managing cloud costs. FinOps (Financial Operations) combines systems, best practices, and culture to bring financial accountability to cloud spending.

This chapter covers skills for optimizing cloud costs, implementing FinOps practices, and building cost-aware organizations.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@finops-expert` | FinOps practices | Cost governance, culture, processes |
| `@cost-optimizer` | Cost reduction | Finding and eliminating waste |
| `@reserved-capacity-expert` | Commitment planning | RIs, Savings Plans, CUDs |
| `@cloud-billing-expert` | Billing analysis | Chargebacks, allocation, forecasting |

---

## 22.1 FinOps Practices with @finops-expert

### Skill Introduction

The `@finops-expert` skill provides comprehensive guidance on implementing FinOps practices. It helps you build a cost-conscious culture, implement governance, and drive accountability for cloud spending.

**When to use this skill:**
- Establishing a FinOps practice
- Creating cost governance policies
- Building cost visibility and accountability
- Driving organizational change for cost efficiency

**Key strengths:**
- Deep knowledge of FinOps framework
- Experience with organizational change
- Understanding of cloud economics

---

### FinOps Implementation Prompts

#### Establishing a FinOps Practice

**Context:** Your organization wants to implement FinOps to manage growing cloud costs.

```text
@finops-expert Help us establish a FinOps practice for our organization:

Current state:
- $2M monthly cloud spend (growing 30% YoY)
- No centralized visibility into costs
- Engineering teams don't know their spending
- Finance struggles with cloud invoices
- No reserved capacity planning

Organization:
- 300 engineers across 25 teams
- Central cloud platform team
- Finance/accounting team manages budgets

Goals:
- Create cost visibility for all stakeholders
- Enable teams to optimize their own spending
- Implement reserved capacity strategy
- Build forecasting capability
- Establish governance without slowing down teams

Please provide:
1. FinOps maturity assessment
2. Organizational structure (FinOps team composition)
3. Stakeholder engagement plan
4. Cost visibility implementation
5. Chargeback/showback strategy
6. Governance framework
7. Success metrics and KPIs
8. 12-month implementation roadmap
```

**Expected Output:** Complete FinOps implementation plan.

---

#### Implementing Cost Allocation

**Context:** You need to allocate cloud costs to teams and projects for accountability.

```text
@finops-expert Design a cost allocation strategy for our cloud environment:

Requirements:
- Allocate costs to 25 development teams
- Separate environments (dev, staging, prod)
- Track costs per project/product
- Support for shared resources
- Integration with financial systems

Current challenges:
- Inconsistent tagging across resources
- Shared resources hard to allocate
- No historical cost data by team
- Engineering doesn't trust the numbers

Tech stack:
- AWS multi-account organization
- Kubernetes (shared clusters)
- Some shared databases and caches

Please provide:
1. Tagging strategy and taxonomy
2. Tag enforcement mechanisms
3. Shared cost allocation methods
4. Kubernetes cost allocation (namespace-level)
5. Reporting and dashboards
6. Integration with finance systems
7. Change management for adoption
```

**Expected Output:** Cost allocation strategy with tagging and enforcement.

---

## 22.2 Cost Optimization with @cost-optimizer

### Skill Introduction

The `@cost-optimizer` skill provides expertise in finding and eliminating cloud waste. It helps you identify optimization opportunities and implement cost reduction strategies.

**When to use this skill:**
- Identifying cost optimization opportunities
- Right-sizing resources
- Eliminating unused resources
- Optimizing data transfer costs
- Implementing spot/preemptible instances

**Key strengths:**
- Experience with cost optimization across clouds
- Knowledge of practical optimization techniques
- Understanding of cost-performance trade-offs

---

### Cost Optimization Prompts

#### Comprehensive Cost Review

**Context:** You need to reduce cloud costs significantly within a quarter.

```text
@cost-optimizer Conduct a comprehensive cost review of our AWS environment:

Current spend breakdown:
- EC2: $500K/month (mostly on-demand)
- RDS: $150K/month
- S3: $100K/month
- Data Transfer: $80K/month
- EKS: $50K/month
- Other: $120K/month

Total: $1M/month, need to reduce by 30%

Infrastructure:
- 500 EC2 instances across environments
- Dev/staging running full-time
- No Savings Plans or Reserved Instances
- Large EBS volumes, many unattached
- Multiple unused load balancers

Please provide:
1. Priority optimization opportunities (quick wins)
2. Right-sizing recommendations methodology
3. Unused resource identification
4. Reserved capacity strategy
5. Architecture optimizations
6. Data transfer cost reduction
7. Implementation timeline with expected savings
8. Monitoring to track progress
```

**Expected Output:** Cost optimization plan with prioritized actions and savings estimates.

---

#### Implementing Spot Instances

**Context:** You want to leverage spot instances for cost savings without sacrificing reliability.

```text
@cost-optimizer Help us implement spot instances for our workloads:

Workloads suitable for spot:
- Batch processing jobs (can restart if interrupted)
- CI/CD build agents
- Development/staging environments
- Stateless web tier (behind load balancer)
- Data processing with Spark

Workloads NOT suitable:
- Production databases
- Stateful services with long-running transactions
- Time-sensitive jobs that can't be interrupted

Environment:
- AWS EKS for Kubernetes workloads
- EC2 for legacy applications
- Batch job framework (custom)

Please provide:
1. Spot instance strategy by workload type
2. Instance type diversification approach
3. Capacity management and fallback
4. EKS spot implementation (Karpenter/Cluster Autoscaler)
5. Spot termination handling
6. Cost comparison and savings projection
7. Monitoring and alerting
```

**Expected Output:** Spot instance implementation strategy.

---

## 22.3 Reserved Capacity with @reserved-capacity-expert

### Skill Introduction

The `@reserved-capacity-expert` skill provides expertise in cloud commitment planning, including Reserved Instances, Savings Plans, and Committed Use Discounts.

**When to use this skill:**
- Planning reserved capacity purchases
- Analyzing commitment coverage
- Optimizing commitment portfolios
- Managing commitment lifecycle

**Key strengths:**
- Expert in AWS, Azure, and GCP commitment models
- Experience with commitment optimization
- Understanding of flexibility vs discount trade-offs

---

### Reserved Capacity Prompts

#### Planning AWS Savings Plans

**Context:** You need to implement a Savings Plans strategy for significant discounts.

```text
@reserved-capacity-expert Design an AWS Savings Plans strategy:

Current usage:
- $600K monthly compute spend (EC2, Fargate, Lambda)
- Mix of instance types across regions
- Steady-state: ~70% of usage consistent month-to-month
- Variable: ~30% fluctuates with demand

Current coverage:
- No Savings Plans or RIs
- All on-demand pricing

Goals:
- Maximize discount while maintaining flexibility
- Don't overcommit on unpredictable workloads
- 1-year commitments preferred (3-year for very stable)

Please provide:
1. Compute vs EC2 Instance Savings Plans comparison
2. Coverage target recommendation
3. Analysis approach using Cost Explorer
4. Purchase strategy (staggered vs bulk)
5. Commitment sizing methodology
6. Monitoring recommendation renewal
7. Expected savings calculation
```

**Expected Output:** Savings Plans strategy with coverage recommendations.

---

## 22.4 Cloud Billing with @cloud-billing-expert

### Skill Introduction

The `@cloud-billing-expert` skill provides expertise in cloud billing analysis, forecasting, and financial operations.

**When to use this skill:**
- Analyzing cloud invoices
- Building cost forecasts
- Implementing showback/chargeback
- Anomaly detection in spending

**Key strengths:**
- Experience with cloud billing APIs
- Knowledge of cost forecasting methods
- Understanding of financial integration

---

### Cloud Billing Prompts

#### Building Cost Forecasting

**Context:** You need to forecast cloud costs for budget planning.

```text
@cloud-billing-expert Help build cost forecasting for our cloud spend:

Requirements:
- Monthly forecasts for next 12 months
- Quarterly forecasts for budget cycles
- Account for known growth plans
- Track accuracy over time

Current data:
- 24 months of historical spend data
- Seasonality (Q4 higher due to traffic)
- Planned new projects with estimated impact
- Reserved capacity already purchased

Challenges:
- Actual spend often exceeds forecasts
- Hard to predict new project costs
- Reserved capacity makes forecasting complex

Please provide:
1. Forecasting methodology
2. Data preparation and analysis
3. Handling seasonality and trends
4. Incorporating planned changes
5. Confidence intervals and ranges
6. Forecast accuracy tracking
7. Reporting for finance and leadership
```

**Expected Output:** Cost forecasting methodology and implementation.

---

## Best Practices Summary

### FinOps Culture
1. **Accountability:** Teams own their costs
2. **Visibility:** Everyone can see spending
3. **Optimization:** Continuous improvement mindset
4. **Collaboration:** Engineering, finance, business aligned
5. **Centralization:** FinOps practice coordinates efforts

### Cost Optimization
1. **Right-sizing:** Match resources to actual needs
2. **Unused Resources:** Regular cleanup cycles
3. **Commitments:** Cover stable workloads
4. **Spot/Preemptible:** Use for fault-tolerant workloads
5. **Architecture:** Design for cost efficiency

### Governance
1. **Budgets:** Set and enforce budgets
2. **Alerts:** Anomaly detection and notifications
3. **Policies:** Guardrails for provisioning
4. **Reviews:** Regular cost review cadence
5. **Reporting:** Consistent, actionable reports

---

## Reflection Points

1. **Culture:** How do you make engineers care about cost?
2. **Accuracy:** How do you improve forecast accuracy?
3. **Trade-offs:** When is spending more the right choice?
4. **Automation:** What cost controls should be automated?

---

**Next Chapter:** [Chapter 23: Application Security →](chapter-23-application-security.md)
