# Chapter 3: Anatomy of a Skill

**Last Updated:** February 5, 2026

---

## 3.1 YAML Frontmatter: Name, Description, and Triggers

### Required Frontmatter Fields

Every SKILL.md file begins with YAML frontmatter that defines metadata:

```yaml
---
name: skill-name
description: >
  A comprehensive description of what this skill does,
  when it should be invoked, and what problems it solves.
---
```

### Complete Frontmatter Reference

```yaml
---
name: typescript-expert
description: >
  Advanced TypeScript development patterns including type-level programming,
  generics, conditional types, and migration strategies. Use when writing
  TypeScript code, adding type safety, or debugging type errors.
source: vibeship-spawner-skills (Apache 2.0)
risk: safe
tags:
  - typescript
  - development
  - frontend
  - backend
triggers:
  - typescript
  - type safety
  - generics
  - ts
version: 2.1.0
---
```

### Field Definitions

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | ✅ Yes | Unique identifier (lowercase, hyphens) |
| `description` | string | ✅ Yes | When and how to use the skill |
| `source` | string | Recommended | Original author/repository |
| `risk` | enum | Optional | `safe`, `medium`, `high`, `unknown` |
| `tags` | array | Optional | Categorization keywords |
| `triggers` | array | Optional | Activation keywords |
| `version` | string | Optional | Semantic version number |

### Name Conventions

```yaml
# ✅ Good names
name: react-patterns
name: api-security-best-practices
name: tdd-workflow
name: python-testing-patterns

# ❌ Bad names
name: ReactPatterns        # No camelCase
name: api_security         # No underscores
name: my skill             # No spaces
name: a                    # Too short
```

### Description Best Practices

```yaml
# ✅ Good description - explains WHAT, WHEN, WHY
description: >
  Expert in designing and building autonomous AI agents. 
  Masters tool use, memory systems, planning strategies, 
  and multi-agent orchestration. Use when: building agents, 
  AI systems, autonomous workflows, or function calling.

# ❌ Bad description - too vague
description: Helps with AI stuff

# ❌ Bad description - missing use cases
description: TypeScript patterns and best practices
```

---

## 3.2 Skill Content Structure

### Standard Sections

A well-structured skill includes these sections:

```markdown
---
name: example-skill
description: Description here
---

# Skill Title

## Purpose
Why this skill exists and what problem it solves.

## Capabilities
- Capability 1
- Capability 2
- Capability 3

## Requirements
Prerequisites and dependencies.

## Patterns
### Pattern 1
How to use the skill for this pattern.

### Pattern 2
How to use the skill for this pattern.

## Anti-Patterns
What to avoid when using this skill.

## Sharp Edges
Known limitations, edge cases, and gotchas.

## Related Skills
Skills that work well with this one.
```

### Real-World Example: AI Agents Architect

```markdown
---
name: ai-agents-architect
description: "Expert in designing and building autonomous AI agents."
source: vibeship-spawner-skills (Apache 2.0)
---

# AI Agents Architect

**Role**: AI Agent Systems Architect

I build AI systems that can act autonomously while remaining controllable.

## Capabilities

- Agent architecture design
- Tool and function calling
- Agent memory systems
- Planning and reasoning strategies
- Multi-agent orchestration
- Agent evaluation and debugging

## Requirements

- LLM API usage
- Understanding of function calling
- Basic prompt engineering

## Patterns

### ReAct Loop

Reason-Act-Observe cycle for step-by-step execution:

- Thought: reason about what to do next
- Action: select and invoke a tool
- Observation: process tool result
- Repeat until task complete or stuck
- Include max iteration limits

### Plan-and-Execute

- Planning phase: decompose task into steps
- Execution phase: execute each step
- Replanning: adjust plan based on results

## Anti-Patterns

### ❌ Unlimited Autonomy
### ❌ Tool Overload
### ❌ Memory Hoarding

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Agent loops without limits | critical | Always set max iterations |
| Vague tool descriptions | high | Write complete tool specs |
| Tool errors not surfaced | high | Explicit error handling |

## Related Skills

Works well with: `rag-engineer`, `prompt-engineer`, `backend`, `mcp-builder`
```

---

## 3.3 Patterns and Anti-Patterns

### What Are Patterns?

Patterns are **recommended approaches** that the skill teaches. They represent best practices and proven solutions.

### Pattern Structure

```markdown
## Patterns

### Pattern Name

**Context**: When to use this pattern

**Problem**: What problem it solves

**Solution**: How to implement it

**Example**:
```code
// Code example here
```

**Trade-offs**:
- Pro: Benefit 1
- Pro: Benefit 2
- Con: Drawback 1
```

### Example: Prompt Engineering Patterns

```markdown
## Patterns

### Few-Shot Learning

Teach the model by showing examples instead of explaining rules.
Include 2-5 input-output pairs that demonstrate the desired behavior.

**Example:**

```markdown
Extract key information from support tickets:

Input: "My login doesn't work and I keep getting error 403"
Output: {"issue": "authentication", "error_code": "403", "priority": "high"}

Input: "Feature request: add dark mode to settings"
Output: {"issue": "feature_request", "error_code": null, "priority": "low"}

Now process: "Can't upload files larger than 10MB, getting timeout"
```

### Chain-of-Thought Prompting

Request step-by-step reasoning before the final answer.
Improves accuracy on analytical tasks by 30-50%.

**Example:**

```markdown
Analyze this bug report and determine root cause.

Think step by step:
1. What is the expected behavior?
2. What is the actual behavior?
3. What changed recently?
4. What components are involved?
5. What is the most likely root cause?
```

### Progressive Disclosure

Start with simple prompts, add complexity only when needed:

1. **Level 1**: Direct instruction - "Summarize this article"
2. **Level 2**: Add constraints - "Summarize in 3 bullet points"
3. **Level 3**: Add reasoning - "Identify main findings, then summarize"
4. **Level 4**: Add examples - Include 2-3 example summaries
```

### What Are Anti-Patterns?

Anti-patterns are **approaches to avoid**. They represent common mistakes that lead to poor results.

### Anti-Pattern Structure

```markdown
## Anti-Patterns

### ❌ Anti-Pattern Name

**Problem**: What goes wrong

**Why it's bad**: Consequences

**Instead**: What to do instead

**Example of bad code**:
```code
// Don't do this
```

**Corrected version**:
```code
// Do this instead
```
```

### Example: Common Anti-Patterns

```markdown
## Anti-Patterns

### ❌ Over-Engineering

Starting with complex prompts before trying simple ones.

**Why it's bad:**
- Wastes tokens
- Harder to debug
- May confuse the model

**Instead:** Start simple, add complexity only when needed.

### ❌ Example Pollution

Using examples that don't match the target task.

**Why it's bad:**
- Model learns wrong patterns
- Inconsistent outputs
- Reduced accuracy

**Instead:** Use representative examples from your actual use case.

### ❌ Context Overflow

Exceeding token limits with excessive context.

**Why it's bad:**
- Information gets truncated
- Critical context may be lost
- Degraded performance

**Instead:** Prioritize relevant context, use summarization.

### ❌ Unlimited Autonomy

Letting agents run without iteration limits.

**Why it's bad:**
- Infinite loops possible
- Runaway costs
- Unpredictable behavior

**Instead:** Always set max_iterations, implement circuit breakers.
```

---

## 3.4 Sharp Edges and Warnings

### What Are Sharp Edges?

Sharp edges are **known limitations, gotchas, or edge cases** that users should be aware of. They represent places where the skill might fail or produce unexpected results.

### Sharp Edge Format

```markdown
## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Description of issue | critical/high/medium/low | How to handle it |

### Detailed Explanations

#### Issue 1: [Name]
Detailed explanation of the issue, when it occurs, and how to work around it.

#### Issue 2: [Name]
Detailed explanation...
```

### Example: Sharp Edges from Real Skills

```markdown
## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Agent loops without iteration limits | critical | Always set limits |
| Vague or incomplete tool descriptions | high | Write complete tool specs |
| Tool errors not surfaced to agent | high | Explicit error handling |
| Storing everything in agent memory | medium | Selective memory |
| Agent has too many tools | medium | Curate tools per task |
| Using multiple agents when one works | medium | Justify multi-agent |
| Agent internals not logged | medium | Implement tracing |
| Fragile parsing of agent outputs | medium | Robust output handling |

### Detailed Explanations

#### Agent Loops Without Iteration Limits

**When it happens:** Agent reasoning enters infinite loop.

**Symptoms:**
- Continuously growing context
- Repeated similar actions
- Escalating API costs

**Solution:**
```python
MAX_ITERATIONS = 10

for i in range(MAX_ITERATIONS):
    result = agent.step()
    if result.is_complete:
        break
else:
    raise AgentLoopError("Max iterations exceeded")
```

#### Vague Tool Descriptions

**When it happens:** Agent selects wrong tool or uses tool incorrectly.

**Symptoms:**
- Tool called with wrong parameters
- Unexpected tool selection
- Task failures

**Solution:**
```python
# ❌ Bad: Vague description
tools = [{"name": "search", "description": "Search for things"}]

# ✅ Good: Specific description
tools = [{
    "name": "search_products",
    "description": "Search for products by name, category, or SKU. "
                   "Returns up to 10 products with id, name, price, and stock.",
    "parameters": {
        "query": "Search query (required, 2-100 chars)",
        "category": "Filter by category (optional)",
        "limit": "Max results 1-50 (default: 10)"
    }
}]
```
```

### Severity Levels

| Level | Description | Action Required |
|-------|-------------|-----------------|
| **critical** | Can cause data loss, security issues, or system failure | Must address before production |
| **high** | Significant impact on functionality or reliability | Address in current sprint |
| **medium** | Noticeable impact but workarounds exist | Plan to address |
| **low** | Minor inconvenience or edge case | Nice to fix |

---

## 3.5 Related Skills and Dependencies

### Why Related Skills Matter

Skills often work best in combination. Related skills help users discover complementary capabilities.

### Related Skills Format

```markdown
## Related Skills

Works well with:
- `@skill-1` - Brief description of how they complement each other
- `@skill-2` - Brief description
- `@skill-3` - Brief description

### Skill Chains

For [specific task], combine:
1. `@skill-a` - First step
2. `@skill-b` - Second step
3. `@skill-c` - Final step
```

### Example: Related Skills Network

```markdown
## Related Skills

### For Feature Development

```
@brainstorming → @architecture → @tdd-workflow → @code-review
```

1. **@brainstorming**: Validate the idea and requirements
2. **@architecture**: Design the technical solution
3. **@tdd-workflow**: Implement with test-driven development
4. **@code-review**: Review before merging

### For Security Assessment

```
@threat-modeling-expert → @pentest-checklist → @vulnerability-scanner
```

1. **@threat-modeling-expert**: Identify potential threats
2. **@pentest-checklist**: Systematic security testing
3. **@vulnerability-scanner**: Automated scanning

### For API Development

```
@api-design-principles → @api-documentation-generator → @api-security-best-practices
```

1. **@api-design-principles**: Design RESTful endpoints
2. **@api-documentation-generator**: Generate OpenAPI docs
3. **@api-security-best-practices**: Secure the API

### Complementary Skills

| This Skill | Works Well With | For |
|------------|-----------------|-----|
| @react-patterns | @typescript-expert | Type-safe React |
| @fastapi-pro | @postgres-best-practices | Python APIs |
| @docker-expert | @kubernetes-architect | Container orchestration |
| @ai-agents-architect | @prompt-engineer | AI development |
```

---

## 3.6 Source Attribution and Licensing

### Why Attribution Matters

- **Respects creators**: Acknowledges the work of contributors
- **Enables updates**: Know where to find the latest version
- **License compliance**: Ensure proper usage rights
- **Quality signal**: Official sources indicate higher quality

### Attribution Format in Skills

```yaml
---
name: skill-name
description: Description here
source: author/repository (License)
---
```

### Common Sources and Their Repositories

| Source | Repository | License | Skills |
|--------|------------|---------|--------|
| **Anthropic** | [anthropics/skills](https://github.com/anthropics/skills) | MIT | Official Claude skills |
| **OpenAI** | [openai/skills](https://github.com/openai/skills) | MIT | Official Codex skills |
| **Vercel Labs** | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) | MIT | React, Web Design |
| **Supabase** | [supabase/agent-skills](https://github.com/supabase/agent-skills) | Apache 2.0 | Postgres |
| **obra** | [obra/superpowers](https://github.com/obra/superpowers) | MIT | Brainstorming, Planning |
| **vibeship** | [vibeforge1111/vibeship-spawner-skills](https://github.com/vibeforge1111/vibeship-spawner-skills) | Apache 2.0 | AI Agents, Integrations |
| **zebbern** | [zebbern/claude-code-guide](https://github.com/zebbern/claude-code-guide) | MIT | Security, Pentesting |
| **coreyhaines31** | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | MIT | Marketing, CRO |
| **VoltAgent** | [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | MIT | Context Engineering |

### License Types

| License | Commercial Use | Modification | Attribution |
|---------|----------------|--------------|-------------|
| **MIT** | ✅ Yes | ✅ Yes | Required |
| **Apache 2.0** | ✅ Yes | ✅ Yes | Required |
| **GPL 3.0** | ✅ Yes | ✅ Yes (share alike) | Required |
| **CC BY 4.0** | ✅ Yes | ✅ Yes | Required |
| **Proprietary** | Check terms | Check terms | Check terms |

### How to Attribute in Custom Skills

```yaml
---
name: my-custom-skill
description: My custom implementation based on existing patterns
source: Based on obra/superpowers (MIT) with modifications
original-source: https://github.com/obra/superpowers
license: MIT
author: Your Name
---
```

---

## Complete Skill Template

Use this template when creating new skills:

```markdown
---
name: new-skill-name
description: >
  Detailed description of what this skill does.
  Include when to use it and what problems it solves.
  Use when: trigger keywords for activation.
source: your-username/your-repo (License)
risk: safe
tags:
  - tag1
  - tag2
triggers:
  - keyword1
  - keyword2
version: 1.0.0
---

# Skill Title

**Role**: What role does this skill embody?

Brief introduction to the skill's purpose and philosophy.

## Capabilities

What this skill can do:

- Capability 1
- Capability 2
- Capability 3

## Requirements

Prerequisites:

- Requirement 1
- Requirement 2

## Patterns

### Pattern 1: Name

**Context**: When to use this pattern

**Implementation**:

```code
// Example code
```

**Trade-offs**:
- Pro: Benefit
- Con: Drawback

### Pattern 2: Name

...

## Anti-Patterns

### ❌ Anti-Pattern 1

**Problem**: What goes wrong

**Solution**: What to do instead

### ❌ Anti-Pattern 2

...

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Issue 1 | high | Solution 1 |
| Issue 2 | medium | Solution 2 |

## Best Practices

1. Best practice 1
2. Best practice 2
3. Best practice 3

## Related Skills

Works well with:
- `@related-skill-1` - How they complement
- `@related-skill-2` - How they complement

## Examples

### Example 1: Use Case

```code
// Detailed example
```

### Example 2: Use Case

```code
// Detailed example
```
```

---

## 100 Prompt Examples for Skill Creation

### Analyzing Existing Skills

```
1. "Show me the structure of the @brainstorming skill"

2. "What patterns does @typescript-expert teach?"

3. "List the anti-patterns in @react-patterns"

4. "What are the sharp edges in @ai-agents-architect?"

5. "Show related skills for @api-security-best-practices"

6. "Who created the @prompt-engineering skill and what license is it?"

7. "Compare the structure of @tdd-workflow and @testing-patterns"

8. "What triggers activate the @docker-expert skill?"

9. "Show me the capabilities section of @kubernetes-architect"

10. "What requirements does @fastapi-pro need?"
```

### Creating New Skills

```
11. "Create a new skill for React Native development following the standard format"

12. "Help me write the frontmatter for a GraphQL API skill"

13. "Generate the patterns section for a microservices skill"

14. "Write anti-patterns for a database migration skill"

15. "Create sharp edges documentation for a CI/CD skill"

16. "Define related skills for a new security auditing skill"

17. "Write a complete skill for Vue.js best practices"

18. "Create a skill template for my company's coding standards"

19. "Generate a skill for AWS Lambda development"

20. "Write a skill for technical writing best practices"
```

### Modifying Skills

```
21. "Add a new pattern to the @react-patterns skill"

22. "Update the description of @python-pro to include Python 3.12 features"

23. "Add sharp edges for async/await to @javascript-pro"

24. "Create a related skills section for @docker-expert"

25. "Add version information to @architecture skill"

26. "Expand the capabilities of @code-review skill"

27. "Add company-specific anti-patterns to @clean-code"

28. "Update @nodejs-backend-patterns with Express 5 patterns"

29. "Add testing examples to @tdd-workflow"

30. "Enhance @api-documenter with GraphQL support"
```

### Understanding Skill Formats

```
31. "Explain the YAML frontmatter format for skills"

32. "What are the required fields in a skill file?"

33. "How should I structure the patterns section?"

34. "What's the difference between patterns and anti-patterns?"

35. "How do I document sharp edges properly?"

36. "What makes a good skill description?"

37. "How do triggers work in skill activation?"

38. "What risk levels are available for skills?"

39. "How should I attribute sources in my skills?"

40. "What's the recommended structure for a skill file?"
```

### Using Skills Effectively

```
41. "Use @brainstorming to design a new skill for my team"

42. "Apply @skill-creator to help me build a custom skill"

43. "Use @documentation-templates to document a new skill"

44. "Apply @writing-skills to improve my skill documentation"

45. "Use @clean-code principles to structure my skill content"

46. "Apply @tutorial-engineer to create examples for my skill"

47. "Use @readme to write the overview for my skill collection"

48. "Apply @testing-patterns to create test examples in my skill"

49. "Use @code-review to check my skill for quality"

50. "Apply @docs-architect to organize my skill content"
```

### Skill Chaining Examples

```
51. "For a new feature, chain @brainstorming → @architecture → @tdd-workflow"

52. "For API development, use @api-design-principles → @api-documentation → @api-security"

53. "For security review, combine @threat-modeling → @pentest-checklist → @vulnerability-scanner"

54. "For frontend work, chain @react-patterns → @typescript-expert → @testing-patterns"

55. "For deployment, use @docker-expert → @kubernetes-architect → @github-actions-templates"

56. "For database design, combine @database-design → @postgres-best-practices → @prisma-expert"

57. "For ML projects, chain @data-scientist → @rag-engineer → @ai-product"

58. "For mobile apps, use @react-native-architecture → @mobile-developer → @app-store-optimization"

59. "For code quality, combine @clean-code → @code-review → @testing-patterns"

60. "For documentation, chain @docs-architect → @api-documenter → @readme"
```

### Platform-Specific Prompts

```
61. "How do I invoke skills in Claude Code?"

62. "What's the syntax for skills in Gemini CLI?"

63. "How does Cursor handle skill invocation?"

64. "Can I use skills with GitHub Copilot?"

65. "What's the skill path for OpenCode?"

66. "How do I configure skills in Antigravity IDE?"

67. "What's different about skills in Codex CLI?"

68. "How does AdaL CLI load skills automatically?"

69. "Can I use the same skills across all platforms?"

70. "How do I set up skills for multiple platforms?"
```

### Team and Organization

```
71. "Create a skill for our team's deployment protocol"

72. "Write a skill that enforces our company's code style"

73. "Generate a skill for our security compliance requirements"

74. "Create a skill for our API design standards"

75. "Write a skill for our documentation requirements"

76. "Generate a skill for our code review checklist"

77. "Create a skill for our testing requirements"

78. "Write a skill for our Git workflow"

79. "Generate a skill for our infrastructure patterns"

80. "Create a skill bundle for new developer onboarding"
```

### Advanced Skill Creation

```
81. "Create a skill with conditional logic based on project type"

82. "Write a skill that references external documentation"

83. "Generate a skill with multiple severity levels for issues"

84. "Create a skill that chains with other skills automatically"

85. "Write a skill with platform-specific sections"

86. "Generate a skill with version compatibility notes"

87. "Create a skill bundle that covers the full development lifecycle"

88. "Write a skill with interactive examples"

89. "Generate a skill with decision trees for complex scenarios"

90. "Create a meta-skill for creating other skills"
```

### Troubleshooting Skills

```
91. "Why isn't my skill being recognized by Claude Code?"

92. "How do I debug skill activation issues?"

93. "My skill description isn't triggering correctly, how do I fix it?"

94. "The skill patterns aren't being followed, what's wrong?"

95. "How do I validate my skill file format?"

96. "My skill works in Claude but not in Cursor, why?"

97. "How do I test a skill before publishing?"

98. "What's causing my skill to load slowly?"

99. "How do I fix symlink issues with skills on Windows?"

100. "How do I update a skill without losing customizations?"
```

---

## Reflection Points for Chapter 3

### Skill Structure

1. **What makes a good skill description?**
   - Clarity about purpose
   - Clear activation triggers
   - Specific use cases

2. **How do patterns differ from documentation?**
   - Patterns are actionable
   - They include examples
   - They show implementation

3. **Why are anti-patterns as important as patterns?**
   - Prevent common mistakes
   - Save debugging time
   - Improve code quality

### Quality and Maintenance

4. **How should you version your skills?**
   - Semantic versioning
   - Changelog maintenance
   - Backward compatibility

5. **What governance should teams have for skill management?**
   - Review process
   - Quality standards
   - Update procedures

6. **How do you measure skill effectiveness?**
   - Usage frequency
   - User feedback
   - Output quality

### Integration

7. **How do related skills enhance productivity?**
   - Skill chaining
   - Complementary capabilities
   - Complete workflows

8. **What's the right granularity for a skill?**
   - Single responsibility
   - Focused scope
   - Clear boundaries

---

## Summary

In this chapter, we explored:

- **YAML Frontmatter**: Required and optional fields for skill metadata
- **Content Structure**: Standard sections for patterns, anti-patterns, and examples
- **Patterns**: Recommended approaches and best practices
- **Anti-Patterns**: Common mistakes to avoid
- **Sharp Edges**: Known limitations and gotchas
- **Related Skills**: How skills work together
- **Attribution**: Proper source crediting and licensing
- **Templates**: Complete templates for creating new skills

**Key Takeaway**: A well-structured skill is the difference between a helpful AI assistant and a confused one. Invest time in clear descriptions, comprehensive patterns, and honest documentation of limitations.

---

**Previous Chapter**: [← Chapter 2: Getting Started](chapter-02-getting-started.md)

**Next Chapter**: [Chapter 4: Software Architecture Fundamentals →](chapter-04-architecture.md)
