# Chapter 31: Quality Assurance

**Last Updated:** February 5, 2026

---

## Overview

Quality Assurance (QA) encompasses the processes and practices that ensure software meets quality standards before reaching users. From test planning to bug tracking and release quality gates, QA practices are essential for delivering reliable software.

This chapter covers essential QA skills for establishing quality processes, managing testing activities, and ensuring consistent software quality.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@qa-lead` | QA strategy | Process design, team leadership |
| `@test-planner` | Test planning | Test case design, coverage analysis |
| `@bug-analyst` | Bug management | Triage, tracking, reporting |
| `@release-qa` | Release quality | Go/no-go decisions, release testing |

---

## 31.1 QA Strategy with @qa-lead

### Skill Introduction

The `@qa-lead` skill provides expertise in designing and leading quality assurance practices. It helps you establish QA processes, build testing culture, and drive quality across the organization.

**When to use this skill:**
- Establishing QA practices
- Building QA teams and processes
- Defining quality metrics
- Quality culture transformation

**Key strengths:**
- Experience with QA leadership
- Knowledge of quality frameworks
- Understanding of team dynamics

---

### QA Strategy Prompts

#### Building QA Practice from Scratch

**Context:** Your organization has no formal QA process and wants to establish one.

```text
@qa-lead Help establish QA practices for our engineering organization:

Current state:
- 50 developers across 6 teams
- No dedicated QA roles
- Developers write their own tests (inconsistently)
- No formal testing process
- Quality issues discovered in production

Goals:
- Improve release quality
- Reduce production bugs by 50%
- Establish consistent QA practices
- Build quality culture (not QA team as gatekeepers)

Constraints:
- Limited budget for new hires
- Teams resistant to process changes
- Fast-paced release schedule

Please provide:
1. QA maturity assessment framework
2. QA practice roadmap
3. Role recommendations (embedded vs centralized)
4. Testing standards and guidelines
5. Quality metrics to track
6. Team enablement approach
7. Change management strategy
```

**Expected Output:** QA practice establishment plan.

---

## 31.2 Test Planning with @test-planner

### Skill Introduction

The `@test-planner` skill provides expertise in designing test plans and test cases. It helps you ensure comprehensive coverage through structured test planning.

**When to use this skill:**
- Creating test plans for features
- Designing test cases and scenarios
- Ensuring requirements coverage
- Managing test documentation

**Key strengths:**
- Experience with test design techniques
- Knowledge of coverage methods
- Understanding of test documentation

---

### Test Planning Prompts

#### Creating Comprehensive Test Plan

**Context:** You need to create a test plan for a new feature release.

```text
@test-planner Create a test plan for our new subscription management feature:

Feature overview:
- Subscription signup with multiple plans
- Plan upgrades and downgrades
- Billing cycle management
- Cancellation with refund calculation
- Trial period handling

Requirements:
- Users can select from 3 subscription tiers
- Upgrade takes effect immediately with prorated billing
- Downgrade takes effect at next billing cycle
- Cancellation can be immediate or at period end
- 14-day free trial for new users

Integration points:
- Stripe for payment processing
- Email service for notifications
- User management service

Please provide:
1. Test plan document structure
2. Test scope (in/out of scope)
3. Test scenarios by feature area
4. Test cases with expected results
5. Test data requirements
6. Environment requirements
7. Risk assessment and mitigation
8. Test schedule and effort estimate
```

**Expected Output:** Comprehensive test plan document.

---

## 31.3 Bug Management with @bug-analyst

### Skill Introduction

The `@bug-analyst` skill provides expertise in managing bugs throughout their lifecycle. It helps you triage issues effectively, track quality metrics, and communicate quality status.

**When to use this skill:**
- Establishing bug triage processes
- Analyzing bug trends
- Prioritizing bug fixes
- Quality reporting

**Key strengths:**
- Experience with bug management
- Knowledge of triage methodologies
- Understanding of quality metrics

---

### Bug Management Prompts

#### Implementing Bug Triage Process

**Context:** Your team struggles with bug prioritization and management.

```text
@bug-analyst Design a bug triage process for our product team:

Current issues:
- 500+ open bugs (growing)
- No clear priority criteria
- Critical bugs get lost in noise
- Developers frustrated with bug assignments
- Stakeholders unclear on bug status

Team structure:
- 3 product managers
- 20 developers
- Support team reports bugs
- Users report via feedback button

Goals:
- Reduce bug backlog to manageable level
- Clear priority and severity criteria
- Timely response to critical issues
- Visibility for all stakeholders

Please provide:
1. Severity and priority definitions
2. Triage process workflow
3. SLA by severity level
4. Bug lifecycle states
5. Escalation procedures
6. Weekly bug review cadence
7. Metrics and reporting
8. Stakeholder communication
```

**Expected Output:** Bug triage process documentation.

---

## 31.4 Release Quality with @release-qa

### Skill Introduction

The `@release-qa` skill provides expertise in ensuring quality at release time. It helps you define release criteria, conduct release testing, and make go/no-go decisions.

**When to use this skill:**
- Defining release quality gates
- Release testing procedures
- Go/no-go decision making
- Post-release validation

**Key strengths:**
- Experience with release processes
- Knowledge of quality gates
- Understanding of risk management

---

### Release Quality Prompts

#### Defining Release Quality Gates

**Context:** You need to establish clear quality gates for releases.

```text
@release-qa Define release quality gates for our CI/CD pipeline:

Release types:
- Feature releases (bi-weekly)
- Hotfix releases (as needed)
- Major version releases (quarterly)

Current challenges:
- Unclear when code is "ready" for release
- Different teams have different standards
- Some releases cause production incidents
- Rollbacks are common (10% of releases)

Existing automation:
- Unit tests in CI
- Integration tests in CI
- Staging environment available
- Basic smoke tests in production

Please provide:
1. Quality gate framework
2. Gates per release type
3. Automated check requirements
4. Manual approval criteria
5. Rollback criteria and process
6. Post-release validation checklist
7. Exception handling process
8. Metrics to track release quality
```

**Expected Output:** Release quality gates framework.

---

## Best Practices Summary

### QA Strategy
1. **Shift Left:** Test early in development
2. **Quality Ownership:** Everyone owns quality
3. **Risk-Based:** Focus on high-risk areas
4. **Metrics-Driven:** Measure what matters
5. **Continuous Improvement:** Regular retrospectives

### Test Planning
1. **Requirements Coverage:** Trace tests to requirements
2. **Risk Analysis:** Prioritize by risk
3. **Test Data:** Plan data needs early
4. **Environment:** Align environments with needs
5. **Maintenance:** Update plans as changes occur

### Bug Management
1. **Clear Criteria:** Objective severity/priority
2. **Timely Triage:** Regular triage cadence
3. **Root Cause:** Analyze for patterns
4. **Communication:** Stakeholder visibility
5. **Closure:** Define done for bugs

---

## Reflection Points

1. **QA Role:** Should QA be embedded in teams or centralized?
2. **Automation vs Manual:** What's the right balance?
3. **Quality Metrics:** What metrics indicate quality?
4. **Release Speed:** How do you balance speed with quality?

---

**Next Chapter:** [Chapter 32: Test Automation Frameworks →](chapter-32-test-automation.md)
