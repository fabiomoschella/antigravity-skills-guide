# Chapter 18: Infrastructure as Code

**Last Updated:** February 5, 2026

---

## Overview

Infrastructure as Code (IaC) transforms infrastructure management from manual, error-prone processes into automated, version-controlled, and reproducible workflows. By treating infrastructure like software, teams can apply software engineering practices—version control, code review, testing, and CI/CD—to their infrastructure.

This chapter covers essential IaC skills using industry-leading tools like Terraform, Pulumi, and Ansible, helping you build reliable, maintainable infrastructure automation.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@terraform-expert` | HashiCorp Terraform | Multi-cloud IaC, declarative infrastructure |
| `@terraform-patterns` | Terraform patterns | Best practices |
| `@terraform-aws-modules` | Terraform AWS | AWS modules |
| `@terraform-module-development` | Module development | Reusable modules |
| `@terraform-state-management` | State management | Remote state |
| `@pulumi-expert` | Pulumi infrastructure | Programming language IaC, complex logic |
| `@ansible-expert` | Ansible automation | Configuration management, ad-hoc automation |
| `@ansible-role-development` | Ansible roles | Reusable roles |
| `@cloudformation-expert` | AWS CloudFormation | AWS-native IaC |
| `@bicep-patterns` | Azure Bicep | Azure IaC |
| `@nix-and-nixos` | Nix/NixOS | Reproducible builds |
| `@nixos-environment-management` | NixOS | System configuration |

---

## 18.1 Terraform Mastery with @terraform-expert

### Skill Introduction

The `@terraform-expert` skill provides deep expertise in HashiCorp Terraform, the most widely adopted IaC tool. It helps you write maintainable Terraform code, design module architectures, and implement Terraform at scale.

**When to use this skill:**
- Writing Terraform configurations for any cloud
- Designing reusable Terraform modules
- Implementing Terraform in CI/CD pipelines
- Troubleshooting state and provider issues
- Migrating from other IaC tools to Terraform

**Key strengths:**
- Expert in Terraform HCL and best practices
- Experience with module design patterns
- Knowledge of state management strategies

---

### Terraform Development Prompts

#### Designing a Terraform Module Architecture

**Context:** You need to structure Terraform code for a large organization with multiple teams and environments.

```text
@terraform-expert Design a scalable Terraform module architecture for our organization:

Context:
- 10 development teams
- 3 environments per team (dev, staging, prod)
- AWS as primary cloud (some GCP)
- Mix of applications: web apps, data pipelines, ML workloads

Requirements:
- Reusable modules across teams
- Consistent security and compliance
- Team autonomy for application-specific resources
- Central platform team owns shared infrastructure
- Clear separation between environments

Current pain points:
- Copy-paste between environments
- Drift between similar setups
- No standards enforcement
- Difficult to update shared patterns

Please provide:
1. Repository structure (mono-repo vs multi-repo)
2. Module hierarchy and organization
3. Module versioning strategy
4. Variable and output conventions
5. State management approach (workspaces, separate backends)
6. CI/CD pipeline design
7. Testing strategy for modules
8. Documentation requirements
```

**Expected Output:** Complete Terraform architecture with repository structure and module design.

---

#### Building a Production-Ready VPC Module

**Context:** You need a reusable VPC module that implements your organization's networking standards.

```text
@terraform-expert Create a production-ready AWS VPC Terraform module:

Requirements:
- Support for multiple availability zones (configurable)
- Public and private subnets per AZ
- NAT Gateway for private subnet internet access
- VPC endpoints for AWS services (S3, ECR, etc.)
- Flow logs for network monitoring
- Configurable CIDR blocks
- Tagging strategy for cost allocation

Security requirements:
- No direct internet access for private subnets
- VPC endpoints to reduce data transfer costs
- Network ACLs as additional security layer

Flexibility needed:
- Optional NAT Gateway (for cost savings in dev)
- Configurable number of AZs
- Support for VPC peering connections
- Transit Gateway attachment option

Please provide:
1. Complete module code (main.tf, variables.tf, outputs.tf)
2. Examples directory with usage patterns
3. README with documentation
4. Validation rules for inputs
5. Tests using Terratest or similar
```

**Expected Output:** Production-ready VPC module with documentation and tests.

---

#### Implementing Terraform CI/CD

**Context:** You need to automate Terraform deployments with proper review and approval workflows.

```text
@terraform-expert Design a Terraform CI/CD pipeline with GitOps practices:

Requirements:
- Plan on pull request, apply on merge to main
- Environment promotion (dev → staging → prod)
- Cost estimation before apply
- Policy enforcement (prevent common mistakes)
- Approval gates for production
- Drift detection

Tools available:
- GitHub Actions for CI/CD
- Terraform Cloud (optional)
- AWS as target cloud

Team workflow:
- Feature branches for changes
- Pull request review required
- Platform team approves production changes

Please provide:
1. GitHub Actions workflow files
2. Branch and environment strategy
3. Terraform Cloud workspace configuration (if used)
4. Policy-as-code setup (Sentinel or OPA)
5. Cost estimation integration
6. Drift detection automation
7. Rollback procedures
```

**Expected Output:** Complete Terraform CI/CD pipeline with GitHub Actions.

---

#### Managing Terraform State at Scale

**Context:** You're experiencing state-related issues as your Terraform usage grows.

```text
@terraform-expert Help us manage Terraform state for a large deployment:

Current issues:
- State file is 50MB and growing
- Terraform plan takes 10+ minutes
- State locks timeout during long operations
- Team stepping on each other's changes
- Difficulty refactoring without breaking state

Environment:
- 2000+ resources in AWS
- Single monolithic state file
- S3 backend with DynamoDB locking
- 15 engineers making changes

Please provide:
1. State splitting strategy
2. Migration plan to multiple state files
3. Resource moving between states
4. State file performance optimization
5. Locking and concurrency best practices
6. Import/export procedures
7. Disaster recovery for state
```

**Expected Output:** State management strategy with migration plan.

---

## 18.2 Pulumi Development with @pulumi-expert

### Skill Introduction

The `@pulumi-expert` skill provides expertise in Pulumi, an IaC platform that uses general-purpose programming languages. It's ideal when you need complex logic, testing, or want to use familiar languages.

**When to use this skill:**
- When you need programming constructs (loops, conditionals, functions)
- For teams more comfortable with TypeScript, Python, or Go
- When you want unit testing for infrastructure
- For complex resource generation logic

**Key strengths:**
- Expert in Pulumi across multiple languages
- Experience with Pulumi patterns and best practices
- Knowledge of testing infrastructure code

---

### Pulumi Development Prompts

#### Creating Infrastructure with TypeScript

**Context:** You want to use TypeScript for infrastructure to leverage type safety and IDE support.

```text
@pulumi-expert Create a Pulumi TypeScript project for our Kubernetes infrastructure:

Requirements:
- EKS cluster with managed node groups
- VPC with proper networking
- IAM roles for service accounts (IRSA)
- Add-ons: AWS Load Balancer Controller, External DNS
- Type-safe configuration
- Reusable component resources

Team preferences:
- TypeScript for type safety
- Familiar with npm/yarn workflows
- Want unit tests for infrastructure

Please provide:
1. Project structure
2. Pulumi.yaml and package.json
3. Component resources for reusability
4. Configuration management approach
5. Unit tests using Pulumi mocks
6. CI/CD integration
7. Comparison benefits vs Terraform
```

**Expected Output:** Complete Pulumi TypeScript project with components and tests.

---

## 18.3 Configuration Management with @ansible-expert

### Skill Introduction

The `@ansible-expert` skill provides expertise in Ansible for configuration management and automation. While modern architectures often use immutable infrastructure, Ansible remains valuable for configuration, orchestration, and legacy environments.

**When to use this skill:**
- Configuration management for VMs and bare metal
- Application deployment automation
- Orchestrating complex multi-step processes
- Managing legacy infrastructure
- ad-hoc automation tasks

**Key strengths:**
- Deep Ansible expertise
- Experience with role and collection development
- Knowledge of Ansible Tower/AWX

---

### Ansible Automation Prompts

#### Automating Application Deployment

**Context:** You need to automate deploying a Java application to a fleet of servers.

```text
@ansible-expert Create an Ansible playbook for deploying our Java application:

Application:
- Spring Boot application (JAR file)
- Running on 20 Ubuntu servers
- Behind an HAProxy load balancer
- Uses PostgreSQL database
- Stores config in /etc/myapp/

Deployment requirements:
- Zero-downtime rolling deployment
- Health check before adding to load balancer
- Rollback capability on failure
- Configuration templating per environment
- Secret injection from HashiCorp Vault

Please provide:
1. Playbook structure (roles, tasks, handlers)
2. Inventory organization
3. Rolling deployment strategy
4. Health check implementation
5. Rollback mechanism
6. Vault integration
7. CI/CD integration
```

**Expected Output:** Complete Ansible deployment automation with roles.

---

## Best Practices Summary

### Infrastructure as Code
1. **Version Control:** All IaC in Git with review process
2. **Modularity:** Create reusable, tested modules
3. **Immutability:** Prefer replacement over modification
4. **State Management:** Secure, backed-up remote state
5. **Testing:** Test modules before production use

### Terraform Specific
1. **Formatting:** Use `terraform fmt` consistently
2. **Validation:** Run `terraform validate` in CI
3. **Planning:** Always review plans before apply
4. **Workspaces:** Use for environment separation (or separate state files)
5. **Providers:** Pin and document provider versions

### Security
1. **Secrets:** Never commit secrets to repositories
2. **State Security:** Encrypt state at rest and in transit
3. **Least Privilege:** Minimal permissions for IaC execution
4. **Audit:** Log all infrastructure changes

---

## Reflection Points

1. **Tool Selection:** When would you choose Pulumi over Terraform?
2. **State Strategies:** How do you decide between monolithic and split state?
3. **Testing:** What level of testing is appropriate for IaC?
4. **Drift:** How do you handle infrastructure drift?

---

**Next Chapter:** [Chapter 19: Monitoring & Observability →](chapter-19-monitoring.md)
