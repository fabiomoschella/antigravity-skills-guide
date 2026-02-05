# Chapter 17: Cloud Platforms

**Last Updated:** February 5, 2026

---

## Overview

Cloud platforms have fundamentally changed how organizations build and operate software. Understanding AWS, Azure, and Google Cloud Platform enables you to leverage managed services, scale globally, and optimize costs effectively.

This chapter covers skills for working with major cloud providers, from architecture design to service-specific implementations. Whether you're cloud-native or migrating from on-premises, these skills help you navigate the complexity of modern cloud environments.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@aws-architect` | AWS architecture and services | AWS design, service selection, Well-Architected |
| `@aws-lambda` | AWS Lambda | Serverless functions |
| `@aws-cdk-patterns` | AWS CDK | Infrastructure as code |
| `@aws-cognito` | AWS Cognito | Authentication |
| `@aws-amplify` | AWS Amplify | Full-stack apps |
| `@azure-architect` | Azure architecture and services | Azure design, enterprise integration |
| `@azure-functions` | Azure Functions | Serverless functions |
| `@gcp-architect` | Google Cloud architecture | GCP design, data/ML platforms |
| `@google-cloud-functions` | Cloud Functions | GCP serverless |
| `@cloud-cost-expert` | Cloud cost optimization | FinOps, cost reduction, budgeting |
| `@cloudflare-workers` | Cloudflare Workers | Edge computing |
| `@cloudflare-zero-trust` | Cloudflare Zero Trust | Security |
| `@firebase-auth` | Firebase Auth | Mobile/web auth |
| `@firebase-development` | Firebase | App development |
| `@supabase-expert` | Supabase | Backend as a service |
| `@supabase-best-practices` | Supabase | Best practices |
| `@vercel-deployment` | Vercel | Frontend deployment |
| `@vercel-v0` | Vercel v0 | AI-assisted development |
| `@fly-io-deployment` | Fly.io | Edge deployment |

---

## 17.1 AWS Architecture with @aws-architect

### Skill Introduction

The `@aws-architect` skill provides expert guidance on Amazon Web Services, the leading cloud platform. It helps you design architectures following AWS Well-Architected Framework principles and select the right services for your workloads.

**When to use this skill:**
- Designing new AWS architectures
- Migrating workloads to AWS
- Optimizing existing AWS deployments
- Implementing security and compliance on AWS
- Troubleshooting AWS service issues

**Key strengths:**
- Deep knowledge of 200+ AWS services
- Experience with Well-Architected Framework
- Practical guidance on cost optimization

---

### AWS Architecture Prompts

#### Designing a Scalable Web Application

**Context:** You're building a new SaaS application on AWS that needs to scale globally.

```text
@aws-architect Design a scalable, highly available architecture for our SaaS platform:

Application requirements:
- Web application with REST API
- 100K daily active users initially, growing to 1M
- Low latency for users globally (US, EU, Asia)
- 99.9% availability target
- GDPR compliance for EU users

Technical stack:
- React frontend
- Node.js API
- PostgreSQL database
- Redis for caching/sessions
- File storage for user uploads
- Background job processing

Please provide:
1. Architecture diagram description
2. Service selection with justification
3. Multi-region strategy
4. Database architecture (RDS, Aurora, or other)
5. CDN and edge configuration
6. Security architecture (VPC, WAF, etc.)
7. Disaster recovery approach
8. Estimated monthly cost at each scale point
```

**Expected Output:** Complete AWS architecture with service selections and cost estimates.

---

#### Implementing Serverless Architecture

**Context:** You want to build an event-driven application using AWS serverless services.

```text
@aws-architect Design a serverless architecture for our event processing system:

Requirements:
- Process 10,000 events per second at peak
- Events from multiple sources (API, IoT, file uploads)
- Transform and enrich events
- Store in data warehouse and trigger real-time actions
- Cost-effective (pay only for usage)

Event types:
- User activity events (80% volume)
- Transaction events (15% volume, requires ACID)
- System events (5% volume)

Please provide:
1. Serverless architecture design
2. Event ingestion (API Gateway, Kinesis, EventBridge)
3. Processing layer (Lambda, Step Functions)
4. Storage layer (DynamoDB, S3, Athena)
5. Error handling and dead letter queues
6. Monitoring and observability
7. Cold start mitigation strategies
8. Cost projection vs traditional architecture
```

**Expected Output:** Serverless architecture leveraging Lambda, EventBridge, and other managed services.

---

#### AWS Security Architecture

**Context:** You need to implement enterprise-grade security on AWS.

```text
@aws-architect Design a security architecture for our AWS environment:

Context:
- Multi-account AWS organization (20 accounts)
- PCI-DSS compliance required for payment systems
- SOC 2 certification in progress
- 500 IAM users across accounts

Requirements:
- Centralized identity management
- Network security and segmentation
- Data encryption everywhere
- Audit logging and monitoring
- Incident detection and response
- Secrets management

Current gaps:
- IAM users have excessive permissions
- No network segmentation
- Logging is inconsistent

Please provide:
1. AWS Organization structure
2. Identity and access management strategy
3. Network architecture with security boundaries
4. Encryption strategy (KMS, key policies)
5. Logging and monitoring (CloudTrail, GuardDuty, Security Hub)
6. Incident response automation
7. Compliance evidence collection
```

**Expected Output:** Comprehensive AWS security architecture meeting compliance requirements.

---

## 17.2 Azure Architecture with @azure-architect

### Skill Introduction

The `@azure-architect` skill provides expertise on Microsoft Azure, particularly strong for enterprise scenarios and Microsoft ecosystem integration. It helps you design Azure solutions and leverage Azure's unique capabilities.

**When to use this skill:**
- Designing Azure architectures
- Integrating with Microsoft 365 and Active Directory
- Implementing hybrid cloud scenarios
- Building on Azure PaaS services

**Key strengths:**
- Deep knowledge of Azure services
- Experience with enterprise and hybrid scenarios
- Expertise in Azure AD and identity

---

### Azure Architecture Prompts

#### Hybrid Cloud Architecture

**Context:** Your organization needs to extend on-premises infrastructure to Azure.

```text
@azure-architect Design a hybrid cloud architecture connecting our datacenter to Azure:

Current on-premises:
- VMware virtualization (200 VMs)
- Active Directory (5000 users)
- SQL Server databases
- File servers (50TB)
- Legacy applications that can't move

Goals:
- Extend capacity to Azure for burst workloads
- Enable remote workforce access
- Modernize some applications over time
- Single identity across on-prem and cloud

Requirements:
- Secure connectivity (no public internet exposure)
- Latency under 10ms for hybrid scenarios
- Consistent management across environments
- Gradual migration path

Please provide:
1. Network connectivity architecture (ExpressRoute, VPN)
2. Identity integration (Azure AD Connect, hybrid join)
3. VM extension strategy (Azure Arc)
4. Storage connectivity (Azure File Sync)
5. Security architecture
6. Management and monitoring
7. Migration approach for suitable workloads
```

**Expected Output:** Hybrid architecture design with connectivity, identity, and migration strategies.

---

#### Azure Kubernetes Service Design

**Context:** You're deploying containerized applications on AKS.

```text
@azure-architect Design an enterprise AKS deployment:

Requirements:
- Production Kubernetes cluster
- 50 microservices, 200 pods
- Integration with Azure AD for authentication
- Private cluster (no public endpoint)
- Multiple environments (dev, staging, prod)

Integrations needed:
- Azure Key Vault for secrets
- Azure Container Registry
- Azure Monitor for observability
- Azure Policy for governance

Please provide:
1. AKS cluster architecture
2. Network design (Azure CNI, private cluster)
3. Node pool strategy
4. Azure AD integration (AKS-managed Azure AD)
5. GitOps deployment approach
6. Monitoring and logging setup
7. Security hardening
8. Cost optimization strategies
```

**Expected Output:** Enterprise AKS architecture with Azure integrations.

---

## 17.3 Google Cloud Platform with @gcp-architect

### Skill Introduction

The `@gcp-architect` skill provides expertise on Google Cloud Platform, known for its data analytics, machine learning, and Kubernetes-native capabilities. It helps you leverage GCP's unique strengths.

**When to use this skill:**
- Designing GCP architectures
- Building data platforms on BigQuery
- Implementing ML workloads with Vertex AI
- Working with GKE (Google Kubernetes Engine)

**Key strengths:**
- Deep knowledge of GCP services
- Expertise in data and ML platforms
- Experience with GKE and serverless

---

### GCP Architecture Prompts

#### Building a Data Platform on GCP

**Context:** You're building a modern data platform leveraging GCP's analytics services.

```text
@gcp-architect Design a data platform architecture on GCP:

Requirements:
- Ingest data from SaaS tools, databases, and streaming sources
- Process 5TB daily data volume
- Enable self-service analytics for business users
- Support data science and ML workloads
- Implement data governance and cataloging

Data sources:
- Salesforce, HubSpot (SaaS)
- Cloud SQL (transactional)
- Pub/Sub (streaming events)
- Cloud Storage (file drops)

Users:
- 50 business analysts (SQL)
- 10 data scientists (Python, notebooks)
- 5 data engineers

Please provide:
1. Data platform architecture
2. Ingestion layer (Dataflow, Fivetran, custom)
3. Storage layer (BigQuery, Cloud Storage)
4. Processing layer (Dataflow, Dataproc)
5. Serving layer (Looker, BigQuery BI Engine)
6. ML platform integration (Vertex AI)
7. Governance (Data Catalog, column-level security)
8. Cost optimization strategies
```

**Expected Output:** Complete GCP data platform architecture.

---

## 17.4 Cloud Cost Optimization with @cloud-cost-expert

### Skill Introduction

The `@cloud-cost-expert` skill focuses on optimizing cloud spending across all major providers. It helps you implement FinOps practices, identify waste, and right-size resources.

**When to use this skill:**
- Analyzing and reducing cloud costs
- Implementing FinOps practices
- Right-sizing resources
- Selecting pricing models (reserved, spot, savings plans)

**Key strengths:**
- Cross-cloud cost optimization expertise
- FinOps framework knowledge
- Practical cost reduction strategies

---

### Cost Optimization Prompts

#### Reducing AWS Costs by 40%

**Context:** Your AWS bill has grown significantly and leadership wants cost reduction.

```text
@cloud-cost-expert Help us reduce our AWS costs by 40%:

Current spend:
- $150K/month total
- EC2: $80K (mix of on-demand instances)
- RDS: $30K (several large instances)
- S3: $15K (growing rapidly)
- Data Transfer: $10K
- Other: $15K

Environment:
- 200 EC2 instances across environments
- Dev/staging running 24/7
- No reserved instances or savings plans
- No tagging strategy

Team:
- No dedicated FinOps person
- Developers provision resources freely

Please provide:
1. Quick wins (this month)
2. Medium-term optimizations (3 months)
3. Long-term strategy (6+ months)
4. Reserved/Savings Plans recommendations
5. Right-sizing analysis approach
6. Cost governance policies
7. Tagging strategy for allocation
8. Tools and dashboards for visibility
```

**Expected Output:** Detailed cost reduction plan with prioritized actions.

---

## Best Practices Summary

### Cloud Architecture
1. **Well-Architected:** Follow cloud provider frameworks
2. **Multi-AZ:** Design for availability zone failures
3. **Managed Services:** Prefer managed over self-managed
4. **Infrastructure as Code:** Version control all infrastructure
5. **Security First:** Implement defense in depth

### Cost Management
1. **Visibility:** Tag everything for cost allocation
2. **Right-sizing:** Match resources to actual needs
3. **Commitments:** Use reserved capacity for steady-state
4. **Automation:** Auto-stop non-production resources
5. **Review:** Regular cost reviews and optimization

---

## Reflection Points

1. **Multi-Cloud:** When does multi-cloud make sense?
2. **Vendor Lock-in:** How do you balance managed services with portability?
3. **Cost vs Speed:** How do you balance cost optimization with time to market?
4. **Cloud Native:** When should you refactor vs lift-and-shift?

---

**Next Chapter:** [Chapter 18: Infrastructure as Code →](chapter-18-infrastructure-as-code.md)
