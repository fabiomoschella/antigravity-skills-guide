# Appendix B: Prompt Templates Library

**Last Updated:** February 5, 2026

---

## Overview

This appendix provides a library of reusable prompt templates that you can customize for your specific needs. These templates follow best practices for effective AI-assisted development.

---

## Template Structure

All templates follow this structure:

```text
@skill-name [Action description]:

Context:
[Relevant background information]

Requirements:
[Specific requirements and constraints]

Please provide:
[Numbered list of expected outputs]
```

---

## Architecture Templates

### System Design Template

```text
@architecture Design a system for [purpose]:

Context:
- Business domain: [domain]
- Scale: [users, transactions, data volume]
- Team size: [number] engineers

Requirements:
- Availability: [percentage] uptime
- Latency: [p50/p99 targets]
- Data retention: [duration]
- Compliance: [regulations]

Constraints:
- Budget: [range]
- Timeline: [duration]
- Existing systems: [list]

Please provide:
1. High-level architecture diagram description
2. Component breakdown
3. Technology recommendations
4. Data flow design
5. Scalability approach
6. Security considerations
7. Deployment strategy
8. Cost estimation
```

---

### Architecture Review Template

```text
@architect-review Review this architecture:

System overview:
[Brief description of the system]

Current architecture:
[Description or link to diagram]

Concerns:
- [List specific concerns]

Review focus areas:
- [ ] Scalability
- [ ] Security
- [ ] Maintainability
- [ ] Cost
- [ ] Performance

Please provide:
1. Strengths of current design
2. Potential issues identified
3. Risk assessment
4. Improvement recommendations
5. Priority order for changes
```

---

## Code Development Templates

### Feature Implementation Template

```text
@[language]-expert Implement [feature name]:

Context:
- Codebase: [framework, language, version]
- Existing patterns: [relevant patterns in use]

Requirements:
- Functionality: [what it should do]
- Integration: [how it connects to existing code]
- Performance: [requirements]

Constraints:
- Must be backward compatible
- Test coverage required
- Follow existing code style

Please provide:
1. Implementation approach
2. Code structure
3. Key functions/classes
4. Error handling
5. Test cases
6. Documentation
```

---

### Code Review Request Template

```text
@code-reviewer Review this [language] code:

```[language]
[paste code here]
```

Context:
- Purpose: [what the code does]
- Critical path: [yes/no]
- Recent changes: [description]

Review priorities:
1. [Primary concern]
2. [Secondary concern]
3. [Tertiary concern]

Please review for:
1. Logic correctness
2. Error handling
3. Performance issues
4. Security vulnerabilities
5. Code style and readability
6. Test coverage gaps
```

---

### Refactoring Template

```text
@refactoring-expert Refactor this code:

```[language]
[paste code here]
```

Current issues:
- [Issue 1]
- [Issue 2]

Goals:
- [Goal 1: e.g., improve readability]
- [Goal 2: e.g., add testability]

Constraints:
- Preserve behavior exactly
- Minimize changes
- No new dependencies

Please provide:
1. Refactoring strategy
2. Step-by-step changes
3. Before/after comparison
4. How to verify behavior preserved
```

---

## DevOps Templates

### CI/CD Pipeline Template

```text
@cicd-architect Design CI/CD pipeline:

Project:
- Type: [language/framework]
- Repository: [GitHub/GitLab/etc]
- Deployment target: [Kubernetes/ECS/etc]

Requirements:
- Build steps: [list]
- Test types: [unit, integration, e2e]
- Environments: [dev, staging, prod]
- Deployment strategy: [blue-green/canary/rolling]

Please provide:
1. Pipeline stages
2. Configuration file (YAML)
3. Environment management
4. Secret handling
5. Rollback strategy
6. Notification setup
```

---

### Infrastructure Template

```text
@terraform-expert Create infrastructure for [purpose]:

Cloud provider: [AWS/Azure/GCP]

Resources needed:
- Compute: [type and quantity]
- Database: [type]
- Storage: [type and size]
- Networking: [requirements]

Requirements:
- High availability: [yes/no]
- Multi-region: [yes/no]
- Cost tier: [dev/staging/prod]

Please provide:
1. Terraform module structure
2. Resource configuration
3. Variables and outputs
4. State management
5. Security groups/IAM
6. Cost estimation
```

---

## Testing Templates

### Test Strategy Template

```text
@testing-strategist Create test strategy:

Application:
- Type: [web/mobile/API/etc]
- Tech stack: [technologies]
- Team: [size and experience]

Features to test:
- [Feature 1]
- [Feature 2]
- [Feature 3]

Quality goals:
- Coverage target: [percentage]
- Defect escape rate: [target]
- Test execution time: [target]

Please provide:
1. Test pyramid structure
2. Test types and ratios
3. Tooling recommendations
4. Automation strategy
5. Test data management
6. CI integration
```

---

### Bug Investigation Template

```text
@debugger-expert Investigate this issue:

Symptoms:
- [What is happening]
- [When it started]
- [Frequency]

Environment:
- [Production/Staging/Dev]
- [Configuration details]

Error messages:
```
[paste error messages/logs]
```

What I've tried:
- [Attempt 1]
- [Attempt 2]

Please provide:
1. Diagnostic approach
2. Data to collect
3. Likely root causes
4. Investigation steps
5. Quick fixes vs proper fixes
```

---

## Security Templates

### Security Review Template

```text
@appsec-expert Security review for [system]:

System overview:
- [Description]
- Data handled: [types]
- Authentication: [method]

Threat model:
- External attackers: [yes/no]
- Malicious insiders: [concern level]
- Compliance: [requirements]

Areas to review:
- [ ] Authentication/Authorization
- [ ] Input validation
- [ ] Data encryption
- [ ] Secrets management
- [ ] Logging/Monitoring

Please provide:
1. Security assessment
2. Vulnerability identification
3. Risk ratings
4. Remediation recommendations
5. Priority order
```

---

## Data & Analytics Templates

### Data Pipeline Template

```text
@data-engineer Design data pipeline:

Source systems:
- [System 1]: [data type, volume, frequency]
- [System 2]: [data type, volume, frequency]

Destination:
- Target: [data warehouse/lake]
- Format: [requirements]

Requirements:
- Latency: [real-time/batch/frequency]
- Data quality: [requirements]
- Historical data: [duration]

Please provide:
1. Pipeline architecture
2. ETL/ELT approach
3. Schema design
4. Quality checks
5. Monitoring and alerting
6. Error handling
```

---

## Project Management Templates

### Project Kickoff Template

```text
@project-planner Create project plan:

Project:
- Name: [project name]
- Goal: [objective]
- Timeline: [target duration]

Team:
- Size: [number]
- Roles: [list]
- Availability: [constraints]

Scope:
- In scope: [list]
- Out of scope: [list]
- Dependencies: [list]

Please provide:
1. Phase breakdown
2. Milestone definitions
3. Resource allocation
4. Risk assessment
5. Communication plan
6. Success metrics
```

---

## Customization Tips

### Making Templates Your Own

1. **Save frequently used prompts** in a personal library
2. **Add project context** that applies to all prompts
3. **Include code style preferences** where relevant
4. **Reference existing documentation** when available
5. **Specify output format** (markdown, code, diagram)

### Combining Templates

You can chain prompts for complex tasks:

```text
Step 1: @architecture Design the system
Step 2: @terraform-expert Implement infrastructure
Step 3: @testing-strategist Create test plan
Step 4: @cicd-architect Build deployment pipeline
```

---

**Next Appendix:** [Appendix C: Source Attribution →](appendix-c-attribution.md)
