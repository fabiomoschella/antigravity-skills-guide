# Chapter 2: Getting Started with Skills

**Last Updated:** February 5, 2026

---

## 2.1 Installation Methods

### Overview

There are two primary methods to install Antigravity Awesome Skills:

| Method | Best For | Complexity |
|--------|----------|------------|
| **npx** | Quick setup, automatic updates | Easy |
| **git clone** | Full control, offline use | Medium |

---

### Method A: npx Installation (Recommended)

The npx installer automatically detects your platform and installs to the correct directory.

#### Universal Installation

```bash
# Default: installs to ~/.agent/skills (works with most tools)
npx antigravity-awesome-skills
```

#### Platform-Specific Installation

```bash
# For Claude Code
npx antigravity-awesome-skills --claude

# For Gemini CLI
npx antigravity-awesome-skills --gemini

# For Codex CLI
npx antigravity-awesome-skills --codex

# For Cursor IDE
npx antigravity-awesome-skills --cursor

# Custom path
npx antigravity-awesome-skills --path ./my-custom-skills
```

#### Update Existing Installation

```bash
# If directory exists, npx runs git pull automatically
npx antigravity-awesome-skills

# Force update
npx antigravity-awesome-skills --force
```

#### Troubleshooting npx

```bash
# If you see a 404 error, use the GitHub URL directly
npx github:sickn33/antigravity-awesome-skills

# View all options
npx antigravity-awesome-skills --help
```

---

### Method B: Git Clone Installation

#### Universal Path (Recommended)

```bash
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills
```

#### Platform-Specific Paths

```bash
# Claude Code
git clone https://github.com/sickn33/antigravity-awesome-skills.git .claude/skills

# Gemini CLI
git clone https://github.com/sickn33/antigravity-awesome-skills.git .gemini/skills

# Codex CLI
git clone https://github.com/sickn33/antigravity-awesome-skills.git .codex/skills

# Cursor
git clone https://github.com/sickn33/antigravity-awesome-skills.git .cursor/skills

# OpenCode
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills
```

#### Windows-Specific: Enable Symlinks

> ⚠️ **Windows Users**: This repository uses symlinks. Enable them before cloning.

```powershell
# Option 1: Enable Developer Mode in Windows Settings, OR

# Option 2: Clone with symlinks enabled
git clone -c core.symlinks=true https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills

# Option 3: Run Git as Administrator
```

#### Updating via Git

```bash
cd .agent/skills
git pull origin main
```

---

## 2.2 Directory Structures for Different Platforms

### Standard Directory Layout

```
.agent/skills/                    # or .claude/skills, .gemini/skills, etc.
├── skills/                       # All skill definitions
│   ├── brainstorming/
│   │   └── SKILL.md
│   ├── architecture/
│   │   └── SKILL.md
│   ├── react-patterns/
│   │   └── SKILL.md
│   └── ... (634+ more)
├── docs/                         # Documentation
│   ├── BUNDLES.md
│   ├── GETTING_STARTED.md
│   └── SOURCES.md
├── data/                         # Skill metadata
│   ├── catalog.json
│   ├── aliases.json
│   └── bundles.json
├── CATALOG.md                    # Complete skill catalog
├── README.md                     # Main documentation
└── skills_index.json             # Searchable index
```

### Platform Path Reference

| Platform | Default Path | Config File |
|----------|--------------|-------------|
| Claude Code | `~/.claude/skills/` | `~/.claude/settings.json` |
| Gemini CLI | `~/.gemini/skills/` | `~/.gemini/config.yaml` |
| Codex CLI | `~/.codex/skills/` | `~/.codex/config.json` |
| Cursor | `.cursor/skills/` | `.cursor/settings.json` |
| Antigravity | `~/.agent/skills/` | `~/.agent/config.yaml` |
| OpenCode | `~/.agent/skills/` | `~/.opencode/config.toml` |

---

## 2.3 Understanding SKILL.md File Format

### Basic Structure

Every skill follows this standard format:

```markdown
---
name: skill-name
description: >
  A description of what this skill does and
  when it should be invoked by the AI agent.
source: author/repository (License)
---

# Skill Title

Content describing the skill's purpose and how to use it.
```

### Complete Example: The Brainstorming Skill

```markdown
---
name: brainstorming
description: >
  Use this skill before any creative or constructive work
  (features, components, architecture, behavior changes, or functionality).
  This skill transforms vague ideas into validated designs through
  disciplined, incremental reasoning and collaboration.
source: obra/superpowers
---

# Brainstorming Ideas Into Designs

## Purpose

Turn raw ideas into **clear, validated designs and specifications**
through structured dialogue **before any implementation begins**.

## Operating Mode

You are operating as a **design facilitator and senior reviewer**.

- No creative implementation  
- No speculative features  
- No silent assumptions  

## The Process

### 1️⃣ Understand the Current Context
### 2️⃣ Understanding the Idea
### 3️⃣ Non-Functional Requirements
### 4️⃣ Understanding Lock
### 5️⃣ Explore Design Approaches
### 6️⃣ Present the Design
### 7️⃣ Decision Log
```

### Frontmatter Fields Reference

| Field | Required | Description |
|-------|----------|-------------|
| `name` | ✅ Yes | Unique identifier for the skill |
| `description` | ✅ Yes | When and how to use the skill |
| `source` | Recommended | Original author/repository |
| `risk` | Optional | Risk level: `safe`, `medium`, `high` |
| `tags` | Optional | Categorization tags |
| `triggers` | Optional | Keywords that activate the skill |

---

## 2.4 Your First Skill Invocation

### Quick Start Examples by Platform

#### Claude Code

```bash
# Start Claude Code
claude

# Invoke a skill
>> /brainstorming I want to build a task management app

# Use multiple skills
>> /architecture then /react-patterns for this project

# Get skill help
>> /skill-name --help
```

#### Gemini CLI

```bash
# Start Gemini CLI
gemini

# Invoke naturally
gemini> Use the brainstorming skill to help me plan a REST API

# Direct reference
gemini> Apply the typescript-expert skill to this code
```

#### Cursor IDE

```
# In the chat panel, use @ to invoke skills
@brainstorming I need to design a user authentication system

@react-patterns review this component

@code-review check this file for issues
```

---

### 50 Copy-Paste Prompt Examples

#### Planning & Brainstorming

```
1. Use @brainstorming to help me design a SaaS application for project management

2. Apply @brainstorming to plan the architecture for a real-time chat system

3. Use @brainstorming to validate my idea for a subscription billing service

4. @brainstorming help me think through the requirements for a mobile banking app

5. Use @brainstorming to explore solutions for a recommendation engine
```

#### Architecture

```
6. Apply @architecture to design a microservices system for e-commerce

7. Use @architecture to evaluate monolith vs microservices for my startup

8. @architecture help me create an ADR for choosing PostgreSQL over MongoDB

9. Apply @architecture to design the data flow for a real-time analytics dashboard

10. Use @architecture to review this system design for scalability issues
```

#### Code Review

```
11. Apply @code-review to analyze the changes in this pull request

12. Use @code-review to check this Python module for security vulnerabilities

13. @code-review examine this React component for performance issues

14. Apply @code-review to verify SOLID principles in this Java class

15. Use @code-review to identify potential memory leaks in this Node.js code
```

#### Frontend Development

```
16. Apply @react-patterns to refactor this class component to hooks

17. Use @react-patterns to implement proper state management for this form

18. @react-patterns help me create a reusable modal component

19. Apply @typescript-expert to add proper types to this JavaScript file

20. Use @nextjs-best-practices to optimize this page for SSR
```

#### Backend Development

```
21. Apply @fastapi-pro to create a REST API for user management

22. Use @python-patterns to implement async database operations

23. @golang-pro help me design a concurrent worker pool

24. Apply @nodejs-backend-patterns to structure this Express application

25. Use @django-pro to implement a custom authentication backend
```

#### Database

```
26. Apply @database-design to normalize this schema to 3NF

27. Use @postgres-best-practices to optimize these slow queries

28. @prisma-expert help me design the schema for a multi-tenant app

29. Apply @nosql-expert to model this data for DynamoDB

30. Use @database-architect to choose between SQL and NoSQL for my use case
```

#### Security

```
31. Apply @api-security-best-practices to secure this REST API

32. Use @pentest-checklist to assess this web application

33. @vulnerability-scanner analyze this codebase for OWASP Top 10

34. Apply @auth-implementation-patterns to implement JWT authentication

35. Use @threat-modeling-expert to create a threat model for this system
```

#### Testing

```
36. Apply @tdd-workflow to implement this feature test-first

37. Use @testing-patterns to write unit tests for this service

38. @playwright-skill create end-to-end tests for the login flow

39. Apply @python-testing-patterns to set up pytest fixtures

40. Use @test-automator to integrate tests into CI/CD
```

#### DevOps & Infrastructure

```
41. Apply @docker-expert to optimize this multi-stage Dockerfile

42. Use @kubernetes-architect to design the deployment strategy

43. @github-actions-templates create a CI/CD pipeline for this project

44. Apply @terraform-skill to provision AWS infrastructure

45. Use @aws-serverless to deploy this Lambda function
```

#### Documentation

```
46. Apply @docs-architect to create technical documentation for this API

47. Use @readme to generate a comprehensive README for this project

48. @api-documenter create OpenAPI specs for these endpoints

49. Apply @tutorial-engineer to write a getting-started guide

50. Use @documentation-templates to create developer onboarding docs
```

---

## 2.5 Troubleshooting Common Setup Issues

### Issue 1: Skills Not Found

**Symptoms:**
- "Skill not found" error
- AI doesn't recognize skill commands

**Solutions:**

```bash
# Verify installation path
ls -la ~/.agent/skills/skills/

# Check if skill exists
ls -la ~/.agent/skills/skills/brainstorming/

# Verify SKILL.md file
cat ~/.agent/skills/skills/brainstorming/SKILL.md
```

### Issue 2: Symlink Errors on Windows

**Symptoms:**
- Files appear empty
- "Permission denied" errors

**Solutions:**

```powershell
# Enable Developer Mode
# Settings > Update & Security > For Developers > Developer Mode

# Or re-clone with symlinks
git clone -c core.symlinks=true https://github.com/sickn33/antigravity-awesome-skills.git

# Verify symlinks work
dir /AL .agent\skills\skills\
```

### Issue 3: Permission Denied

**Symptoms:**
- Cannot read skill files
- Installation fails

**Solutions:**

```bash
# Fix permissions (Linux/macOS)
chmod -R 755 ~/.agent/skills/

# Fix ownership
chown -R $USER:$USER ~/.agent/skills/
```

### Issue 4: Outdated Skills

**Symptoms:**
- Missing new skills
- Features not working

**Solutions:**

```bash
# Update via git
cd ~/.agent/skills
git pull origin main

# Or reinstall via npx
npx antigravity-awesome-skills --force
```

### Issue 5: Platform Not Detecting Skills

**Symptoms:**
- Skills work in one platform but not another

**Solutions:**

```bash
# Create symlinks for all platforms
ln -s ~/.agent/skills ~/.claude/skills
ln -s ~/.agent/skills ~/.gemini/skills
ln -s ~/.agent/skills ~/.cursor/skills

# Or install to each platform separately
npx antigravity-awesome-skills --claude
npx antigravity-awesome-skills --gemini
npx antigravity-awesome-skills --cursor
```

---

## 2.6 Best Practices for Skill Organization

### Personal Skill Customization

Create a personal skills folder for customizations:

```
~/.agent/skills/
├── skills/                    # Original skills (don't modify)
└── custom/                    # Your custom skills
    ├── my-company-standards/
    │   └── SKILL.md
    ├── my-deployment-protocol/
    │   └── SKILL.md
    └── my-code-style/
        └── SKILL.md
```

### Team Skill Sharing

For team environments, use a shared repository:

```bash
# Create a team skills repo
git clone https://github.com/your-org/team-skills.git .agent/team-skills

# Reference both in your config
# skills_paths:
#   - ~/.agent/skills
#   - ~/.agent/team-skills
```

### Skill Versioning

Track skill versions for consistency:

```markdown
---
name: my-custom-skill
description: Team-specific coding standards
version: 1.2.0
last-updated: 2026-02-05
---
```

### Recommended Folder Structure for Teams

```
company-skills/
├── engineering/
│   ├── code-standards/
│   ├── review-checklist/
│   └── deployment-protocol/
├── security/
│   ├── compliance-rules/
│   └── security-review/
├── documentation/
│   ├── api-docs-template/
│   └── readme-template/
└── README.md
```

---

## Quick Reference: Installation Commands

### One-Line Installation

```bash
# Claude Code
npx antigravity-awesome-skills --claude

# Gemini CLI  
npx antigravity-awesome-skills --gemini

# Cursor
npx antigravity-awesome-skills --cursor

# Universal
npx antigravity-awesome-skills
```

### Verification Commands

```bash
# Count installed skills
ls ~/.agent/skills/skills/ | wc -l

# Search for a skill
find ~/.agent/skills -name "*react*" -type d

# View skill content
cat ~/.agent/skills/skills/brainstorming/SKILL.md
```

---

## Reflection Points for Chapter 2

1. **Which installation method is best for your workflow?**
   - Consider team collaboration needs
   - Evaluate update frequency requirements
   - Think about offline access

2. **How will you organize custom skills for your team?**
   - Shared repository vs local customizations
   - Version control strategy
   - Review process for new skills

3. **What platform-specific considerations apply to your setup?**
   - Windows symlink handling
   - Multiple platform support
   - Path configuration

---

**Next Chapter**: [Chapter 3: Anatomy of a Skill →](chapter-03-anatomy.md)
