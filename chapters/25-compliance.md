# Chapter 25: Compliance & Governance

**Last Updated:** February 5, 2026

---

## Overview

Compliance and governance ensure that organizations meet regulatory requirements and maintain consistent security standards. In cloud environments, this requires continuous monitoring, documentation, and automated enforcement.

This chapter covers skills for implementing compliance frameworks, automating controls, and maintaining governance at scale.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@compliance-expert` | Compliance frameworks | SOC 2, ISO, regulatory compliance |
| `@gdpr-expert` | Data privacy | GDPR, CCPA, privacy regulations |
| `@audit-expert` | Audit management | Evidence collection, audit preparation |
| `@policy-as-code-expert` | Policy automation | OPA, Sentinel, automated enforcement |

---

## 25.1 Compliance Frameworks with @compliance-expert

### Skill Introduction

The `@compliance-expert` skill provides expertise in implementing compliance frameworks like SOC 2, ISO 27001, PCI-DSS, and HIPAA. It helps you understand requirements and implement appropriate controls.

**When to use this skill:**
- Preparing for compliance certifications
- Mapping controls to requirements
- Implementing security frameworks
- Gap analysis and remediation planning
- Continuous compliance monitoring

**Key strengths:**
- Deep knowledge of major frameworks
- Experience with compliance implementations
- Understanding of control mapping

---

### Compliance Implementation Prompts

#### Implementing SOC 2 Compliance

**Context:** Your organization needs to achieve SOC 2 Type II certification.

```text
@compliance-expert Help us achieve SOC 2 Type II certification:

Current state:
- SaaS product serving enterprise customers
- AWS infrastructure
- 50 employees
- No formal security program
- Some security controls in place informally

Business drivers:
- Enterprise customers requiring SOC 2
- Sales team losing deals without certification
- 6-month timeline to certification

Trust service criteria needed:
- Security (required)
- Availability
- Confidentiality

Please provide:
1. SOC 2 readiness assessment approach
2. Gap analysis framework
3. Control mapping to AWS environment
4. Documentation requirements
5. Evidence collection strategy
6. Remediation prioritization
7. Auditor selection guidance
8. Timelines and milestones
```

**Expected Output:** SOC 2 implementation roadmap.

---

#### Mapping Controls Across Frameworks

**Context:** You need to satisfy multiple compliance frameworks efficiently.

```text
@compliance-expert Help map controls across multiple frameworks:

Frameworks to satisfy:
- SOC 2 Type II
- ISO 27001:2022
- GDPR
- HIPAA (future customer requirement)

Goals:
- Single control set satisfying all frameworks
- Avoid duplicate effort
- Streamlined evidence collection
- Clear mapping documentation

Current controls:
- Basic access controls
- Encryption at rest and transit
- Logging and monitoring
- Incident response plan
- Some policies documented

Please provide:
1. Unified control framework approach
2. Control mapping matrix
3. Gap identification across frameworks
4. Implementation priority
5. Evidence reuse strategy
6. Compliance management tooling
7. Maintenance and update process
```

**Expected Output:** Unified compliance framework with mappings.

---

## 25.2 Data Privacy with @gdpr-expert

### Skill Introduction

The `@gdpr-expert` skill provides expertise in data privacy regulations including GDPR, CCPA, and emerging privacy laws. It helps you implement privacy-by-design principles and maintain compliance.

**When to use this skill:**
- Implementing GDPR compliance
- Data protection impact assessments
- Privacy-by-design implementation
- Data subject request handling
- Cross-border data transfers

**Key strengths:**
- Deep knowledge of privacy regulations
- Experience with privacy implementations
- Understanding of technical controls for privacy

---

### Privacy Implementation Prompts

#### Implementing GDPR Compliance

**Context:** Your application handles EU personal data and must comply with GDPR.

```text
@gdpr-expert Help implement GDPR compliance for our SaaS platform:

Application context:
- B2B SaaS with EU customers
- Collects: names, emails, job titles, usage data
- Some customers upload PII of their customers
- Third-party integrations (analytics, CRM)
- Data stored in AWS EU region

Current gaps:
- No documented lawful basis
- Unclear data retention policies
- Data subject requests handled manually
- No DPIA completed
- Privacy policy needs update

Please provide:
1. GDPR compliance assessment
2. Lawful basis documentation
3. Data mapping and inventory
4. DPIA template and process
5. Data subject request automation
6. Third-party processor agreements (DPA)
7. Privacy policy requirements
8. Technical controls implementation
```

**Expected Output:** GDPR compliance implementation plan.

---

## 25.3 Audit Management with @audit-expert

### Skill Introduction

The `@audit-expert` skill provides expertise in managing security audits and collecting evidence. It helps you prepare for audits, streamline evidence collection, and maintain audit readiness.

**When to use this skill:**
- Preparing for SOC 2/ISO audits
- Automating evidence collection
- Managing audit relationships
- Remediating audit findings
- Continuous audit readiness

**Key strengths:**
- Experience with major audit firms
- Knowledge of evidence requirements
- Understanding of audit processes

---

### Audit Management Prompts

#### Automating Evidence Collection

**Context:** You want to automate evidence collection for continuous compliance.

```text
@audit-expert Design an automated evidence collection system:

Compliance frameworks:
- SOC 2 Type II (annual audit)
- ISO 27001 (annual surveillance)

Evidence types needed:
- Access reviews (quarterly)
- Change management approvals
- Security training completion
- Vulnerability scan results
- Incident reports
- Policy acknowledgments
- System configurations

Current tools:
- AWS for infrastructure
- GitHub for code/changes
- Okta for identity
- Jira for ticketing
- Confluence for documentation

Please provide:
1. Evidence collection architecture
2. Automation for each evidence type
3. Evidence repository design
4. Retention and versioning
5. Audit portal for auditors
6. Alert system for evidence gaps
7. Tool recommendations
```

**Expected Output:** Automated evidence collection system design.

---

## 25.4 Policy as Code with @policy-as-code-expert

### Skill Introduction

The `@policy-as-code-expert` skill provides expertise in implementing policy as code for automated governance. It helps you enforce security and compliance policies through code rather than manual processes.

**When to use this skill:**
- Implementing automated policy enforcement
- Using OPA, Sentinel, or Kyverno
- Shift-left compliance checking
- Automated remediation
- Policy versioning and testing

**Key strengths:**
- Expert in OPA/Rego
- Experience with cloud-native policy
- Knowledge of policy enforcement patterns

---

### Policy as Code Prompts

#### Implementing OPA for Kubernetes

**Context:** You want to enforce policies in your Kubernetes clusters.

```text
@policy-as-code-expert Implement OPA Gatekeeper for Kubernetes policy:

Policies to enforce:
- All images from approved registries only
- No containers running as root
- Resource requests/limits required
- No privileged containers
- Network policies required for namespaces
- Labels required (team, environment)
- No latest image tag

Environment:
- 3 EKS clusters (dev, staging, prod)
- 100+ namespaces
- Mix of team-owned and platform-owned workloads

Requirements:
- Warn in dev, deny in prod
- Exceptions for specific namespaces
- Policy as code in Git
- Testing before deployment
- Monitoring of violations

Please provide:
1. Gatekeeper installation and configuration
2. Constraint templates for each policy
3. Constraints for environment-specific enforcement
4. Exception handling approach
5. CI/CD integration for policy testing
6. Violation monitoring and alerting
7. Developer experience considerations
```

**Expected Output:** OPA Gatekeeper implementation with policies.

---

## Best Practices Summary

### Compliance
1. **Continuous Compliance:** Ongoing, not point-in-time
2. **Control Mapping:** Unified controls for multiple frameworks
3. **Automation:** Automate where possible
4. **Evidence:** Maintain continuous evidence collection
5. **Updates:** Stay current with framework changes

### Privacy
1. **Privacy by Design:** Build privacy in from start
2. **Data Minimization:** Collect only what's needed
3. **Transparency:** Clear privacy communications
4. **Subject Rights:** Automate DSR handling
5. **Vendor Management:** DPAs with all processors

### Governance
1. **Policy as Code:** Automated enforcement
2. **Shift Left:** Early compliance checking
3. **Exceptions:** Documented exception process
4. **Monitoring:** Continuous compliance monitoring
5. **Training:** Regular security awareness

---

## Reflection Points

1. **Balance:** How do you balance compliance with agility?
2. **Automation:** What compliance tasks can't be automated?
3. **Culture:** How do you build a compliance-aware culture?
4. **Vendors:** How do you manage third-party compliance?

---

**Next Chapter:** [Chapter 26: Security Operations →](chapter-26-secops.md)
