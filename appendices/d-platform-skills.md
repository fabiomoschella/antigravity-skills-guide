# Appendix D: Skills by Platform

**Last Updated:** February 5, 2026

---

## Overview

This appendix organizes skills by the AI coding assistant platforms they work with. While most skills are platform-agnostic, some may work better with specific assistants.

---

## Platform Compatibility Matrix

### Legend

| Symbol | Meaning |
|--------|---------|
| ✅ | Fully compatible |
| ⚠️ | Partial compatibility |
| ❌ | Not recommended |
| 🔧 | Requires adaptation |

---

## General Compatibility

| Skill Category | Gemini Code Assist | GitHub Copilot | Cursor | Windsurf | Claude |
|----------------|-------------------|----------------|--------|----------|--------|
| Architecture | ✅ | ✅ | ✅ | ✅ | ✅ |
| DevOps | ✅ | ✅ | ✅ | ✅ | ✅ |
| Security | ✅ | ✅ | ✅ | ✅ | ✅ |
| Testing | ✅ | ✅ | ✅ | ✅ | ✅ |
| Development | ✅ | ✅ | ✅ | ✅ | ✅ |
| Data & AI | ✅ | ✅ | ✅ | ✅ | ✅ |
| Productivity | ✅ | ✅ | ✅ | ✅ | ✅ |
| Specialized | ✅ | ✅ | ✅ | ✅ | ✅ |

---

## Platform-Specific Guidance

### Gemini Code Assist

**Strengths:**
- Excellent code understanding
- Strong multi-file context
- Good at architecture discussions
- Integrated with Google Cloud

**Best Skills:**
- `@gcp-architect` - Native GCP integration
- `@architecture` - Leverages deep context
- `@code-reviewer` - Multi-file awareness

**Tips:**
```text
# Gemini works well with workspace context
@architecture Analyze the current workspace and suggest improvements

# Reference multiple files easily
@code-reviewer Review src/api/* for consistency
```

---

### GitHub Copilot

**Strengths:**
- Excellent code completion
- Strong repository awareness
- Good test generation
- GitHub ecosystem integration

**Best Skills:**
- `@tdd-coach` - Great for test generation
- `@nodejs-expert` - Strong JavaScript support
- `@python-expert` - Excellent Python patterns

**Tips:**
```text
# Copilot excels at completing code
@nodejs-expert Complete the implementation of this function

# Good for generating tests
@testing-strategist Generate unit tests for UserService
```

---

### Cursor

**Strengths:**
- Fast code editing
- Strong inline suggestions
- Good multi-model support
- Excellent for refactoring

**Best Skills:**
- `@refactoring-expert` - Inline refactoring
- `@css-expert` - Style editing
- `@react-expert` - Component development

**Tips:**
```text
# Cursor's inline mode works well
@refactoring-expert Improve this function

# Good for quick changes
@css-expert Update these styles to use CSS Grid
```

---

### Windsurf

**Strengths:**
- Agent-like behavior
- Multi-step task execution
- Terminal integration
- File system operations

**Best Skills:**
- `@devops-expert` - Terminal operations
- `@automation-expert` - Task automation
- `@cicd-architect` - Pipeline building

**Tips:**
```text
# Windsurf handles multi-step well
@devops-expert Set up the complete CI/CD pipeline for this project

# Good for automation
@automation-expert Create scripts for common development tasks
```

---

### Claude (in IDE)

**Strengths:**
- Excellent reasoning
- Strong documentation
- Good at complex explanations
- Careful about edge cases

**Best Skills:**
- `@technical-writer` - Documentation
- `@architect-review` - Detailed reviews
- `@security-expert` - Thorough analysis

**Tips:**
```text
# Claude excels at detailed analysis
@appsec-expert Conduct thorough security analysis of this module

# Great for documentation
@technical-writer Create comprehensive API documentation
```

---

## Skill Activation by Platform

### Universal Activation

Works the same across all platforms:

```text
@skill-name Your prompt here
```

### Platform-Specific Notes

| Platform | Activation | Notes |
|----------|------------|-------|
| Gemini | `@skill-name` | Full skill file access |
| Copilot | `@skill-name` | May need skill in context |
| Cursor | `@skill-name` | Works with rules files |
| Windsurf | `@skill-name` | Agent mode recommended |
| Claude | `@skill-name` | Include in system prompt |

---

## Installing Skills by Platform

### Gemini Code Assist

```bash
# Skills location
~/.gemini/antigravity/skills/

# Install command
git clone https://github.com/sickn33/antigravity-awesome-skills.git \
  ~/.gemini/antigravity/skills/antigravity-awesome-skills
```

### GitHub Copilot

```bash
# Skills as workspace instructions
.github/copilot-instructions.md

# Or in VS Code settings
.vscode/settings.json
```

### Cursor

```bash
# Rules file
.cursorrules

# Or cursor directory
.cursor/rules/
```

### Windsurf

```bash
# Rules location
.windsurfrules

# Or cascade rules
.windsurf/rules/
```

---

## Cross-Platform Tips

### Maximizing Compatibility

1. **Use standard format:** Follow the skill template format
2. **Avoid platform specifics:** Keep prompts generic
3. **Include context:** Provide necessary information in prompt
4. **Test across platforms:** Verify behavior consistency

### Adapting Skills

When a skill doesn't work on a platform:

```text
# Original skill call
@complex-skill Do something complex

# Adapted version with more context
@complex-skill Do something complex.

Context:
- We're working on [project type]
- Using [technology stack]
- The goal is [specific goal]

Please provide step-by-step guidance.
```

---

## Platform Selection Guide

### Choose Based on Task

| Task Type | Recommended Platform | Reason |
|-----------|---------------------|--------|
| Code Completion | Copilot | Fast inline suggestions |
| Refactoring | Cursor | Excellent edit mode |
| Architecture | Gemini/Claude | Deep reasoning |
| Automation | Windsurf | Multi-step execution |
| Documentation | Claude | Thorough writing |

---

**Next Appendix:** [Appendix E: Troubleshooting Guide →](appendix-e-troubleshooting.md)
