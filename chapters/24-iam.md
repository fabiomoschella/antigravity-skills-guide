# Chapter 24: Identity & Access Management

**Last Updated:** February 5, 2026

---

## Overview

Identity and Access Management (IAM) is the framework of policies and technologies that ensures the right individuals have appropriate access to technology resources. In modern cloud environments, robust IAM is critical for security and compliance.

This chapter covers essential IAM skills for cloud platforms, helping you design and implement secure access control systems.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@iam-architect` | IAM architecture | Strategy, design, implementation |
| `@aws-iam-expert` | AWS IAM | Roles, policies, organizations |
| `@azure-ad-expert` | Azure Active Directory | Identity, conditional access |
| `@okta-expert` | Okta identity | SSO, lifecycle management |

---

## 24.1 IAM Architecture with @iam-architect

### Skill Introduction

The `@iam-architect` skill provides expertise in designing identity and access management systems. It helps you create secure, scalable IAM architectures that meet both security requirements and user experience needs.

**When to use this skill:**
- Designing enterprise IAM strategy
- Implementing role-based access control (RBAC)
- Creating access governance frameworks
- Integrating identity systems across platforms

**Key strengths:**
- Deep knowledge of IAM principles
- Experience with identity federation
- Understanding of compliance requirements

---

### IAM Architecture Prompts

#### Designing Enterprise IAM Strategy

**Context:** You need to create an IAM strategy for a growing organization.

```text
@iam-architect Design an enterprise IAM strategy for our organization:

Current state:
- 2000 employees, growing 20% annually
- Multiple SaaS applications (50+)
- AWS and Azure cloud accounts
- On-premises Active Directory
- No centralized identity governance
- Manual provisioning/deprovisioning

Requirements:
- Single identity across all systems
- Automated user lifecycle management
- Self-service for common requests
- Privileged access management
- Compliance with SOC 2 and GDPR
- Contractor and partner access

Please provide:
1. IAM strategy framework
2. Identity provider architecture
3. Access management model (RBAC, ABAC)
4. Lifecycle management automation
5. Privileged access management approach
6. Federation and SSO strategy
7. Governance and compliance
8. Implementation roadmap
```

**Expected Output:** Complete IAM strategy with implementation plan.

---

#### Implementing Zero Trust Access

**Context:** You want to implement zero trust principles for application access.

```text
@iam-architect Design zero trust access for our applications:

Applications:
- Internal web applications (10+)
- Cloud SaaS applications (30+)
- APIs and services
- Database access for developers

Users:
- 500 employees (mix of office and remote)
- 100 contractors
- Some privileged IT administrators

Current state:
- VPN for remote access to internal apps
- Password-based authentication mostly
- Limited MFA adoption

Goals:
- Verify every access request
- No implicit trust based on network
- Continuous authentication/authorization
- Granular access policies
- Modern user experience (no VPN)

Please provide:
1. Zero trust architecture design
2. Identity verification requirements
3. Device trust model
4. Context-aware access policies
5. VPN-less access implementation
6. Continuous authorization approaches
7. User experience considerations
```

**Expected Output:** Zero trust access architecture.

---

## 24.2 AWS IAM with @aws-iam-expert

### Skill Introduction

The `@aws-iam-expert` skill provides deep expertise in AWS Identity and Access Management. It helps you implement secure, scalable access controls for AWS resources.

**When to use this skill:**
- Designing AWS IAM policies
- Implementing cross-account access
- Setting up AWS Organizations
- Troubleshooting IAM permission issues
- Implementing least privilege

**Key strengths:**
- Expert in AWS IAM policy language
- Experience with multi-account strategies
- Knowledge of AWS security best practices

---

### AWS IAM Prompts

#### Implementing Least Privilege

**Context:** You need to implement least privilege access for your AWS environment.

```text
@aws-iam-expert Help implement least privilege across our AWS accounts:

Current state:
- 20 AWS accounts in Organizations
- Many users have AdministratorAccess
- Service roles have overly broad permissions
- No policy review process
- 500+ IAM policies (mostly custom)

Goals:
- Right-size existing permissions
- Implement just-in-time access for sensitive actions
- Standardize policies across accounts
- Enable self-service within guardrails

Tools available:
- IAM Access Analyzer
- CloudTrail logs (90 days)

Please provide:
1. Assessment methodology (unused permissions)
2. Policy refactoring strategy
3. Permission boundaries implementation
4. SCP guardrails for Organizations
5. Just-in-time access patterns
6. Policy management workflow
7. Monitoring and alerting for privilege escalation
```

**Expected Output:** Least privilege implementation plan.

---

#### Designing Cross-Account Access

**Context:** You need to enable secure access between AWS accounts.

```text
@aws-iam-expert Design cross-account access for our AWS Organization:

Account structure:
- Management account (billing, organization)
- Shared services (CI/CD, monitoring)
- Dev, Staging, Prod workload accounts
- Security account (CloudTrail, GuardDuty)
- 10 team-specific accounts

Access patterns:
- CI/CD needs to deploy to all workload accounts
- Developers need read access to lower environments
- On-call needs access to production for incidents
- Security team needs read access everywhere
- Some roles need to assume roles in other accounts

Please provide:
1. Cross-account role strategy
2. Trust policy patterns
3. Role naming conventions
4. Permission boundaries for assumed roles
5. Session policies for transitive access
6. Audit and monitoring approach
7. Access review process
```

**Expected Output:** Cross-account access architecture.

---

## 24.3 Azure Active Directory with @azure-ad-expert

### Skill Introduction

The `@azure-ad-expert` skill provides expertise in Azure Active Directory (now Entra ID). It helps you implement identity management, SSO, and conditional access for Microsoft cloud and hybrid environments.

**When to use this skill:**
- Configuring Azure AD for enterprise
- Implementing conditional access policies
- Setting up hybrid identity
- Managing application registrations
- Implementing B2B and B2C scenarios

**Key strengths:**
- Deep Azure AD/Entra ID knowledge
- Experience with hybrid identity
- Understanding of conditional access

---

### Azure AD Prompts

#### Implementing Conditional Access

**Context:** You want to implement conditional access policies for security.

```text
@azure-ad-expert Design conditional access policies for our organization:

Environment:
- 1000 users in Azure AD
- Microsoft 365 E5 licenses
- 50 cloud applications (Azure AD integrated)
- Mix of managed and BYOD devices

Security requirements:
- MFA for all users (context-aware)
- Block legacy authentication
- Compliant device required for sensitive apps
- Location-based policies (block risky countries)
- Session controls for unmanaged devices

User groups:
- Standard users (800)
- Privileged users (50)
- Contractors (150)

Please provide:
1. Conditional access policy framework
2. Policy prioritization and ordering
3. Specific policies for each requirement
4. Named locations configuration
5. Device compliance integration
6. Testing and rollout approach
7. Monitoring and reporting
```

**Expected Output:** Conditional access policy design.

---

## 24.4 Identity Platforms with @okta-expert

### Skill Introduction

The `@okta-expert` skill provides expertise in Okta, a leading identity platform. It helps you implement SSO, lifecycle management, and API access management with Okta.

**When to use this skill:**
- Implementing Okta for enterprise
- Configuring SSO integrations
- Setting up user provisioning
- Implementing MFA and adaptive authentication
- API access management

**Key strengths:**
- Deep Okta platform knowledge
- Experience with SCIM provisioning
- Understanding of Okta workflows

---

### Okta Implementation Prompts

#### Implementing SSO with Okta

**Context:** You're deploying Okta as your identity provider.

```text
@okta-expert Implement Okta SSO for our organization:

Applications to integrate:
- AWS accounts (SAML)
- Salesforce (SAML)
- Slack (SCIM + SAML)
- GitHub Enterprise (SAML)
- Custom internal apps (OIDC)
- 30+ additional SaaS apps

User sources:
- Primary: Azure AD (hybrid sync from on-prem AD)
- Need to coexist with Azure AD as source

Requirements:
- SSO for all applications
- Automated provisioning (SCIM where possible)
- Group-based application assignment
- Adaptive MFA based on risk
- Self-service password reset

Please provide:
1. Okta architecture design
2. Azure AD integration approach
3. Application integration strategy
4. Provisioning configuration
5. MFA policies
6. Rollout and migration plan
7. Monitoring and support processes
```

**Expected Output:** Okta implementation plan.

---

## Best Practices Summary

### IAM Strategy
1. **Centralize Identity:** Single source of truth
2. **Least Privilege:** Minimal necessary access
3. **Separation of Duties:** No single point of failure
4. **Just-in-Time:** Temporary elevated access
5. **Review Regularly:** Periodic access reviews

### Authentication
1. **Strong MFA:** Phishing-resistant preferred
2. **Passwordless:** When possible
3. **SSO:** Reduce password fatigue
4. **Session Management:** Appropriate timeouts
5. **Secure Recovery:** MFA for recovery too

### Authorization
1. **RBAC/ABAC:** Appropriate model for needs
2. **Policy as Code:** Version control policies
3. **Principle of Least Privilege:** Start minimal
4. **Audit Access:** Log all access decisions
5. **Automate Reviews:** Regular certification

---

## Reflection Points

1. **Usability:** How do you balance security with user experience?
2. **Legacy Systems:** How do you handle systems without modern IAM support?
3. **Privileged Access:** What's the right PAM strategy?
4. **Federation:** When is federation appropriate vs direct integration?

---

**Next Chapter:** [Chapter 25: Compliance & Governance →](chapter-25-compliance.md)
