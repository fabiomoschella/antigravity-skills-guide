# Appendix E: Troubleshooting Guide

**Last Updated:** February 5, 2026

---

## Overview

This appendix provides solutions to common issues when using AI-powered skills. Follow these troubleshooting steps to resolve problems and optimize your skill usage.

---

## Common Issues and Solutions

### Issue 1: Skill Not Recognized

**Symptoms:**
- AI doesn't understand the `@skill-name` syntax
- Skill is ignored or treated as text
- "I don't know what skill you mean" responses

**Causes:**
- Skill files not installed
- Incorrect skill directory
- Platform doesn't support skills

**Solutions:**

```bash
# 1. Verify skill installation
ls ~/.gemini/antigravity/skills/antigravity-awesome-skills/

# 2. Check skill file exists
find ~/.gemini -name "*.md" | grep skill-name

# 3. Reinstall skills
cd ~/.gemini/antigravity/skills/
rm -rf antigravity-awesome-skills
git clone https://github.com/sickn33/antigravity-awesome-skills.git
```

**Prevention:**
- Run periodic sync of skills repository
- Verify installation after updates

---

### Issue 2: Poor Quality Responses

**Symptoms:**
- Generic or vague responses
- Missing expected detail
- Response doesn't match skill purpose

**Causes:**
- Insufficient prompt context
- Missing requirements
- Ambiguous request

**Solutions:**

```text
# Bad prompt (too vague)
@architecture Design a system

# Good prompt (specific and contextual)
@architecture Design a microservices system:

Context:
- E-commerce platform
- 1M daily users
- Cloud-native (AWS)

Requirements:
- High availability (99.9%)
- Sub-100ms latency
- Event-driven architecture

Please provide:
1. System architecture diagram description
2. Service breakdown
3. Technology recommendations
4. Data flow design
```

**Best Practices:**
- Always include context
- Specify requirements explicitly
- List expected outputs
- Provide constraints

---

### Issue 3: Inconsistent Responses

**Symptoms:**
- Different answers to same prompt
- Quality varies between sessions
- Sometimes works, sometimes doesn't

**Causes:**
- AI model variability
- Context window limitations
- Session state issues

**Solutions:**

```text
# Include key context every time
@skill-name [Request]:

Previous context:
- We're building [project name]
- Using [tech stack]
- This relates to [previous work]

Current request:
[Specific request with details]
```

**Best Practices:**
- Save good prompts for reuse
- Include relevant previous context
- Be explicit about expectations
- Use templates for consistency

---

### Issue 4: Skill Conflicts

**Symptoms:**
- Wrong skill seems to activate
- Unexpected behavior
- Skill names clash

**Causes:**
- Multiple skills with similar names
- Overlapping skill definitions
- Custom skills conflicting

**Solutions:**

```bash
# 1. Check for duplicate skills
grep -r "name: architect" ~/.gemini/antigravity/skills/

# 2. Use fully qualified skill names
@antigravity/architecture instead of @architecture

# 3. Remove conflicting custom skills
rm ~/.gemini/custom-skills/conflicting-skill.md
```

**Prevention:**
- Use unique skill names for custom skills
- Organize skills in namespaced directories
- Review skill catalog before creating new ones

---

### Issue 5: Context Too Long

**Symptoms:**
- "Context too long" errors
- Truncated responses
- AI loses track of conversation

**Causes:**
- Including too much code
- Long conversation history
- Large skill files

**Solutions:**

```text
# Bad: Including entire codebase
@code-reviewer Review all files in src/

# Good: Focused review
@code-reviewer Review src/auth/login.ts:

```typescript
[relevant code only, not entire file]
```

Focus on:
- Security vulnerabilities
- Error handling
```

**Best Practices:**
- Include only relevant code
- Start new conversations for new topics
- Summarize rather than copy all context
- Use file references instead of pasting

---

### Issue 6: Outdated Information

**Symptoms:**
- Skill recommends old versions
- Deprecated patterns suggested
- Missing recent features

**Causes:**
- Skill files out of date
- AI knowledge cutoff
- Stale examples in skills

**Solutions:**

```bash
# 1. Update skills repository
cd ~/.gemini/antigravity/skills/antigravity-awesome-skills
git pull origin main

# 2. Check skill dates
head -20 skills/skill-name/SKILL.md
# Look for "Last Updated" date

# 3. Override with current version
@python-expert Build a FastAPI app (use FastAPI 0.109+ with Python 3.12)
```

**Best Practices:**
- Update skills weekly
- Specify versions in prompts when critical
- Verify recommendations against current docs

---

### Issue 7: Platform-Specific Issues

#### Gemini Code Assist

```text
Problem: Skills not loading
Solution: Ensure skills are in ~/.gemini/antigravity/skills/

Problem: Workspace not recognized
Solution: Open folder (not file) in VS Code
```

#### GitHub Copilot

```text
Problem: Custom instructions ignored
Solution: Use .github/copilot-instructions.md

Problem: Too many suggestions
Solution: Configure settings to reduce autocomplete
```

#### Cursor

```text
Problem: Rules not applied
Solution: Check .cursorrules or .cursor/rules/ location

Problem: Skills mixed with conversation
Solution: Use Composer mode for skill-based work
```

---

## Diagnostic Commands

### Check Installation

```bash
# Verify skill directory structure
tree ~/.gemini/antigravity/skills/ -L 2

# Count available skills
find ~/.gemini/antigravity/skills -name "SKILL.md" | wc -l

# Search for specific skill
grep -r "name: architecture" ~/.gemini/antigravity/skills/
```

### Test Skill Loading

```text
# Simple test prompt
@skill-name Confirm you understand this skill by summarizing its purpose.
```

### Verify Configuration

```bash
# Check VS Code settings
cat .vscode/settings.json | grep -A5 "gemini"

# Check Cursor rules
cat .cursorrules

# Check Windsurf config
cat .windsurfrules
```

---

## Getting Help

### Self-Diagnosis Checklist

1. ☐ Skills repository installed correctly?
2. ☐ Correct directory for your platform?
3. ☐ Skill name spelled correctly?
4. ☐ Prompt includes sufficient context?
5. ☐ Platform supports custom skills?
6. ☐ No conflicting skills?
7. ☐ Skills updated recently?

### Reporting Issues

If problems persist:

1. **Document the issue:**
   - Exact prompt used
   - Expected vs actual response
   - Platform and version
   - Error messages

2. **Search existing issues:**
   - GitHub Issues on repository
   - Community discussions

3. **Open new issue:**
   - Use issue template
   - Include reproduction steps
   - Attach relevant logs

---

## Quick Fixes Reference

| Problem | Quick Fix |
|---------|-----------|
| Skill not found | `git pull` in skills directory |
| Poor response | Add more context to prompt |
| Wrong skill | Use full skill name with namespace |
| Context too long | Focus on specific files/sections |
| Outdated info | Specify current versions in prompt |
| Inconsistent results | Use prompt templates |
| Platform issue | Check platform-specific docs |

---

## Success Tips

### Prompt Engineering Quick Reference

```text
✅ DO:
- Provide specific context
- List requirements clearly
- Specify output format
- Include constraints
- Use numbered lists for expected outputs

❌ DON'T:
- Use vague requests
- Skip background info
- Forget to specify tech stack
- Include irrelevant code
- Expect perfect first results
```

### Skill Usage Best Practices

1. **Start simple** - Test with basic prompts first
2. **Iterate** - Refine prompts based on results
3. **Save templates** - Keep working prompts
4. **Update regularly** - Keep skills current
5. **Combine skills** - Chain for complex tasks

---

**Thank you for using Antigravity Awesome Skills!**

Return to: [Table of Contents](../CHAPTERS_LIST.md)
