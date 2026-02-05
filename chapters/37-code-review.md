# Chapter 37: Code Review

**Last Updated:** February 5, 2026

---

## Overview

Code review is a critical practice for maintaining code quality, sharing knowledge, and catching issues before they reach production. Effective code review balances thoroughness with efficiency, providing constructive feedback that improves both the code and the developer.

This chapter covers essential code review skills for conducting and improving the code review process.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@code-reviewer` | Code review | Thorough, constructive reviews |
| `@review-guidelines` | Review standards | Establishing review practices |
| `@pr-analyzer` | PR analysis | Large PR review strategies |
| `@feedback-coach` | Review feedback | Constructive communication |
| `@code-quality-analyst` | Quality analysis | Code metrics |
| `@static-analysis-expert` | Static analysis | Automated code analysis |
| `@linter-configuration` | Linter setup | ESLint, Prettier config |
| `@eslint-config` | ESLint | JavaScript linting |
| `@prettier-config` | Prettier | Code formatting |
| `@sonarqube-expert` | SonarQube | Code quality gates |

---

## 37.1 Code Review Practice with @code-reviewer

### Skill Introduction

The `@code-reviewer` skill provides expertise in conducting effective code reviews. It helps you identify issues, provide constructive feedback, and balance thoroughness with efficiency.

**When to use this skill:**
- Reviewing pull requests
- Identifying code issues
- Providing improvement suggestions
- Learning review techniques

**Key strengths:**
- Experience with review patterns
- Knowledge of common issues
- Understanding of code quality

---

### Code Review Prompts

#### Conducting Thorough Code Review

**Context:** You need to review a complex pull request.

```text
@code-reviewer Review this pull request for our authentication service:

Changes include:
- New JWT refresh token implementation
- Token revocation endpoint
- Database migration for revoked tokens table
- Unit and integration tests

PR link: [link to PR]
Files changed: 15
Lines: +500 / -100

Review priorities:
1. Security (critical for auth code)
2. Performance (token validation on every request)
3. Correctness (token lifecycle)
4. Test coverage
5. Code quality

Please review for:
- Security vulnerabilities
- Edge cases and error handling
- Performance concerns
- Test coverage gaps
- Code maintainability
- Documentation needs
```

**Expected Output:** Comprehensive code review feedback.

---

#### Improving Review Skills

**Context:** You want to become a better code reviewer.

```text
@code-reviewer Help me improve my code review skills:

Current situation:
- I'm a mid-level developer doing code reviews
- Reviews take too long (2+ hours for large PRs)
- Not sure what to prioritize
- Feedback sometimes creates conflict
- Miss important issues sometimes

Goals:
- Conduct faster, more effective reviews
- Catch more significant issues
- Give better feedback
- Build positive relationships

Please provide:
1. Review prioritization framework
2. What to look for first
3. Common issues to check
4. Time management strategies
5. Giving constructive feedback
6. Learning from reviews you receive
7. Tools to assist reviews
8. Building review expertise over time
```

**Expected Output:** Code review improvement guide.

---

## 37.2 Review Guidelines with @review-guidelines

### Skill Introduction

The `@review-guidelines` skill helps you establish code review standards and practices for your team. It provides frameworks for consistent, effective reviews across the organization.

**When to use this skill:**
- Creating review guidelines
- Standardizing review practices
- Training team on reviews
- Improving review process

**Key strengths:**
- Experience with review programs
- Knowledge of industry practices
- Understanding of team dynamics

---

### Review Guidelines Prompts

#### Creating Team Review Guidelines

**Context:** You need to establish code review guidelines for your team.

```text
@review-guidelines Create code review guidelines for our engineering team:

Team context:
- 20 developers (varying experience levels)
- Multiple programming languages (TypeScript, Python, Go)
- Microservices architecture
- 50+ PRs per week
- No formal review process currently

Goals:
- Consistent review quality
- Reasonable turnaround time (24 hours)
- Knowledge sharing through reviews
- Positive team culture
- Catch issues before production

Please provide:
1. Review expectations document
2. What reviewers should check
3. PR authoring guidelines
4. Review turnaround SLAs
5. Approval requirements
6. How to handle disagreements
7. Review metrics to track
8. Onboarding new team members
```

**Expected Output:** Comprehensive review guidelines.

---

## 37.3 Large PR Analysis with @pr-analyzer

### Skill Introduction

The `@pr-analyzer` skill provides strategies for reviewing large or complex pull requests effectively. It helps you manage scope and ensure thorough review without excessive time investment.

**When to use this skill:**
- Reviewing large PRs
- Breaking down complex changes
- Managing review time
- Prioritizing review effort

**Key strengths:**
- Experience with large changes
- Strategies for scope management
- Understanding of risk areas

---

### Large PR Review Prompts

#### Reviewing Large Pull Request

**Context:** You need to review a very large pull request effectively.

```text
@pr-analyzer Help me review this large pull request:

PR description:
- Major refactoring of order processing
- 2000+ lines changed across 50 files
- New domain models, services, and handlers
- Database migrations
- Tests updated

Time available: 4 hours max

Concerns:
- Too large to review thoroughly
- Don't know where to start
- Risk of missing critical issues
- Need to provide feedback today

Please provide:
1. Strategy for reviewing large PRs
2. How to prioritize files/changes
3. Risk assessment approach
4. Critical areas to focus on
5. When to request PR breakdown
6. Tools to help with large reviews
7. How to document what was reviewed
8. Follow-up review process
```

**Expected Output:** Large PR review strategy.

---

## 37.4 Review Feedback with @feedback-coach

### Skill Introduction

The `@feedback-coach` skill helps you provide constructive, effective code review feedback. It focuses on communication that improves code while maintaining positive relationships.

**When to use this skill:**
- Giving constructive feedback
- Handling difficult reviews
- Responding to feedback
- Improving team communication

**Key strengths:**
- Effective communication techniques
- Experience with feedback patterns
- Understanding of team dynamics

---

### Feedback Coaching Prompts

#### Giving Constructive Feedback

**Context:** You need to provide feedback on problematic code without damaging relationships.

```text
@feedback-coach Help me give constructive feedback on this PR:

Situation:
- Junior developer's first major feature
- Several design issues in the code
- Missing error handling throughout
- Tests incomplete
- Code works but needs significant changes

Concerns:
- Don't want to discourage the developer
- Need the code improved significantly
- Want to be helpful, not harsh
- Limited time for back-and-forth

Please help with:
1. How to frame significant feedback
2. Prioritizing what to mention
3. Wording for sensitive issues
4. Suggesting improvements constructively
5. Offering to help vs just critiquing
6. When to discuss vs comment
7. Following up on feedback
8. Celebrating what's done well
```

**Expected Output:** Constructive feedback guidance.

---

## Best Practices Summary

### Conducting Reviews
1. **Understand Context:** Read PR description first
2. **Focus on Important:** Prioritize significant issues
3. **Be Specific:** Point to exact lines
4. **Suggest Solutions:** Don't just criticize
5. **Ask Questions:** When unsure

### Giving Feedback
1. **Be Kind:** Respectful tone always
2. **Be Clear:** Specific, actionable feedback
3. **Be Timely:** Review within SLA
4. **Be Consistent:** Apply same standards
5. **Be Helpful:** Intent to improve, not judge

### Process
1. **PR Size:** Encourage small PRs
2. **Automation:** Lint/test before review
3. **Turnaround:** Clear SLA expectations
4. **Follow-up:** Verify changes made
5. **Learning:** Reviews as teaching moments

---

## Reflection Points

1. **Balance:** How do you balance speed with thoroughness?
2. **Conflict:** How do you handle disagreements?
3. **Learning:** How do reviews contribute to team growth?
4. **Automation:** What should be automated vs human reviewed?

---

**Next Chapter:** [Chapter 38: Debugging →](chapter-38-debugging.md)
