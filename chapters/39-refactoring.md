# Chapter 39: Refactoring

**Last Updated:** February 5, 2026

---

## Overview

Refactoring improves code structure without changing behavior. This chapter covers essential refactoring skills for reducing technical debt and improving maintainability.

### Skills Covered

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@refactoring-expert` | Refactoring techniques | Code improvement |
| `@legacy-code-expert` | Legacy code work | Old codebases |
| `@tech-debt-analyst` | Technical debt | Debt prioritization |
| `@code-modernization` | Code updates | Modern patterns |
| `@migration-specialist` | Migrations | Framework upgrades |
| `@dependency-updater` | Dependencies | Version updates |
| `@deprecation-handler` | Deprecations | API transitions |
| `@complexity-reducer` | Complexity | Simplification |
| `@dead-code-eliminator` | Dead code | Code cleanup |
| `@design-pattern-refactorer` | Patterns | Pattern application |

---

## 39.1 Refactoring Techniques with @refactoring-expert

### Refactoring Prompts

```text
@refactoring-expert Help refactor this complex function:

Function issues:
- 500+ lines, too many responsibilities
- Deep nesting (7+ levels)
- No tests, hard to change

Goals:
- Make it testable and maintainable
- Keep behavior identical

Provide:
1. Refactoring strategy
2. Test-first approach
3. Step-by-step plan
```

---

## 39.2 Legacy Code with @legacy-code-expert

```text
@legacy-code-expert Help me work with this legacy codebase:

System: 10+ years old, no tests, limited docs

Task: Add new payment method safely

Provide:
1. How to understand the system
2. Creating safety net (tests)
3. Making changes safely
```

---

## 39.3 Technical Debt with @tech-debt-analyst

```text
@tech-debt-analyst Help assess our technical debt:

Known debt:
- Monolith needs splitting
- Outdated dependencies
- No tests in some modules

Provide:
1. Assessment framework
2. Prioritization criteria
3. Remediation roadmap
```

---

## Best Practices

1. **Tests First:** Ensure safety net exists
2. **Small Steps:** Incremental changes
3. **Track Debt:** Maintain inventory
4. **Prioritize:** Risk and value based

---

**Next Chapter:** [Chapter 40: Version Control →](chapter-40-version-control.md)
