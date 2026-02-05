# Chapter 4: Software Architecture Fundamentals

**Last Updated:** February 5, 2026

---

## Overview

This chapter covers the foundational architecture skills that help you design, document, and review software systems. These skills are essential for making informed architectural decisions and maintaining architectural integrity across your projects.

### Skills Covered in This Chapter

| Skill | Source | Purpose |
|-------|--------|---------|
| `@architecture` | Unknown | Architectural decision-making framework |
| `@architect-review` | Unknown | Architecture review and validation |
| `@architecture-decision-records` | Unknown | ADR documentation |
| `@architecture-patterns` | Unknown | Clean Architecture, Hexagonal, DDD |
| `@senior-architect` | Unknown | Senior-level architectural guidance |
| `@system-design-expert` | antigravity | System design |
| `@system-design-reviewer` | antigravity | Design review |
| `@software-planner` | antigravity | Software planning |
| `@technical-spec-writer` | antigravity | Technical specs |
| `@scalability-architect` | antigravity | Scalability patterns |
| `@performance-architect` | antigravity | Performance optimization |
| `@microservices-architect` | antigravity | Microservices design |
| `@ddd-expert` | antigravity | Domain-Driven Design |
| `@monolith-to-microservices` | antigravity | Migration patterns |
| `@modular-monolith` | antigravity | Modular architecture |
| `@event-sourcing-architect` | antigravity | Event sourcing |

---

## 4.1 The Architecture Skill

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: architecture, system-design, adr

### Purpose

The `architecture` skill provides a comprehensive framework for making architectural decisions. It guides you through requirements analysis, trade-off evaluation, and ADR (Architecture Decision Record) documentation.

### When to Use

- Starting a new project or major feature
- Evaluating technology choices
- Documenting architectural decisions
- Reviewing system designs

### 50 Copy-Paste Prompts

#### Project Planning

```
1. "Use @architecture to design the high-level architecture for a new e-commerce platform"

2. "Apply @architecture to evaluate microservices vs monolith for a startup MVP"

3. "Use @architecture to plan the data architecture for a real-time analytics system"

4. "Apply @architecture to design the integration layer for a legacy system migration"

5. "Use @architecture to architect a multi-tenant SaaS application"
```

#### Technology Selection

```
6. "Use @architecture to compare PostgreSQL vs MongoDB for our user data"

7. "Apply @architecture to evaluate message queues: RabbitMQ vs Kafka vs SQS"

8. "Use @architecture to choose between REST, GraphQL, and gRPC for our API"

9. "Apply @architecture to select a caching strategy: Redis vs Memcached vs CDN"

10. "Use @architecture to evaluate serverless vs containers for our workload"
```

#### Trade-off Analysis

```
11. "Use @architecture to analyze consistency vs availability trade-offs for our distributed system"

12. "Apply @architecture to evaluate build vs buy decisions for authentication"

13. "Use @architecture to assess the trade-offs of event sourcing for our domain"

14. "Apply @architecture to compare synchronous vs asynchronous communication patterns"

15. "Use @architecture to evaluate the cost-performance trade-offs of different cloud providers"
```

#### System Design

```
16. "Use @architecture to design the authentication and authorization system"

17. "Apply @architecture to architect a notification system with multiple channels"

18. "Use @architecture to design a file upload and processing pipeline"

19. "Apply @architecture to create the architecture for a real-time collaboration feature"

20. "Use @architecture to design a rate limiting and throttling system"
```

#### Review and Validation

```
21. "Use @architecture to review this system design for scalability issues"

22. "Apply @architecture to identify single points of failure in our current architecture"

23. "Use @architecture to assess the security implications of this design"

24. "Apply @architecture to evaluate the disaster recovery capabilities"

25. "Use @architecture to review the data flow for GDPR compliance"
```

---

## 4.2 The Architect Review Skill

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: architecture, review, quality

### Purpose

The `architect-review` skill enables senior-level architectural review of system designs and code changes. It ensures architectural integrity, scalability, and maintainability.

### When to Use

- Reviewing pull requests with architectural impact
- Validating system designs before implementation
- Assessing technical debt
- Evaluating refactoring proposals

### 50 Copy-Paste Prompts

#### Code Architecture Review

```
26. "Use @architect-review to analyze this codebase for architectural anti-patterns"

27. "Apply @architect-review to evaluate the separation of concerns in this module"

28. "Use @architect-review to check if this code follows clean architecture principles"

29. "Apply @architect-review to assess the dependency graph of this project"

30. "Use @architect-review to identify coupling issues in these components"
```

#### Design Review

```
31. "Use @architect-review to validate this microservices design"

32. "Apply @architect-review to assess the API design for backward compatibility"

33. "Use @architect-review to evaluate the database schema for scalability"

34. "Apply @architect-review to review the event-driven architecture proposal"

35. "Use @architect-review to assess the security architecture"
```

#### Scalability Review

```
36. "Use @architect-review to identify bottlenecks in this architecture"

37. "Apply @architect-review to evaluate horizontal scaling capabilities"

38. "Use @architect-review to assess the caching strategy effectiveness"

39. "Apply @architect-review to review the load balancing approach"

40. "Use @architect-review to analyze the database sharding strategy"
```

#### Maintainability Review

```
41. "Use @architect-review to assess the long-term maintainability of this design"

42. "Apply @architect-review to evaluate the testing strategy for this architecture"

43. "Use @architect-review to identify areas with high technical debt"

44. "Apply @architect-review to review the documentation completeness"

45. "Use @architect-review to assess the onboarding complexity for new developers"
```

#### Migration Review

```
46. "Use @architect-review to evaluate this migration plan from monolith to microservices"

47. "Apply @architect-review to assess the database migration strategy"

48. "Use @architect-review to review the API versioning approach"

49. "Apply @architect-review to evaluate the rollback strategy"

50. "Use @architect-review to assess the feature flag implementation"
```

---

## 4.3 Architecture Decision Records (ADRs)

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: documentation, decisions, governance

### Purpose

The `architecture-decision-records` skill helps you write and maintain ADRs following best practices. ADRs provide a historical record of significant technical decisions.

### ADR Structure

```markdown
# ADR-001: [Title]

## Status
[Proposed | Accepted | Deprecated | Superseded by ADR-XXX]

## Context
What is the issue we're addressing?

## Decision
What have we decided to do?

## Consequences
What are the results of this decision?

## Alternatives Considered
What other options were evaluated?
```

### 30 Copy-Paste Prompts

#### Creating ADRs

```
51. "Use @architecture-decision-records to create an ADR for choosing PostgreSQL as our primary database"

52. "Apply @architecture-decision-records to document our decision to use Kubernetes for orchestration"

53. "Use @architecture-decision-records to write an ADR for adopting GraphQL"

54. "Apply @architecture-decision-records to document the authentication strategy decision"

55. "Use @architecture-decision-records to create an ADR for our logging architecture"

56. "Apply @architecture-decision-records to document the decision to use event sourcing"

57. "Use @architecture-decision-records to write an ADR for our caching strategy"

58. "Apply @architecture-decision-records to document the CI/CD pipeline decisions"

59. "Use @architecture-decision-records to create an ADR for the API versioning strategy"

60. "Apply @architecture-decision-records to document the microservices boundaries"
```

#### Reviewing ADRs

```
61. "Use @architecture-decision-records to review this ADR for completeness"

62. "Apply @architecture-decision-records to identify missing alternatives in this ADR"

63. "Use @architecture-decision-records to assess the consequences section"

64. "Apply @architecture-decision-records to validate the context description"

65. "Use @architecture-decision-records to check if the decision is well-justified"
```

#### Managing ADRs

```
66. "Use @architecture-decision-records to create an index of all our architectural decisions"

67. "Apply @architecture-decision-records to identify ADRs that need updating"

68. "Use @architecture-decision-records to mark this ADR as superseded"

69. "Apply @architecture-decision-records to create a decision timeline"

70. "Use @architecture-decision-records to generate an ADR template for our team"
```

---

## 4.4 Architecture Patterns

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: patterns, clean-architecture, hexagonal, ddd

### Purpose

The `architecture-patterns` skill covers implementation of proven backend architecture patterns including Clean Architecture, Hexagonal Architecture, and Domain-Driven Design.

### Pattern Overview

| Pattern | Description | Best For |
|---------|-------------|----------|
| **Clean Architecture** | Layered with dependency inversion | Complex business logic |
| **Hexagonal** | Ports and adapters | Integration-heavy systems |
| **DDD** | Domain-centric design | Complex domains |
| **CQRS** | Separate read/write models | High-scale reads |
| **Event Sourcing** | Event-based state | Audit requirements |

### 30 Copy-Paste Prompts

#### Clean Architecture

```
71. "Use @architecture-patterns to implement Clean Architecture in this Python project"

72. "Apply @architecture-patterns to refactor this module to follow Clean Architecture"

73. "Use @architecture-patterns to define the layers for our Node.js application"

74. "Apply @architecture-patterns to implement the Use Case layer"

75. "Use @architecture-patterns to create the repository interfaces"
```

#### Hexagonal Architecture

```
76. "Use @architecture-patterns to implement Hexagonal Architecture for this service"

77. "Apply @architecture-patterns to define ports and adapters for database access"

78. "Use @architecture-patterns to create the primary and secondary adapters"

79. "Apply @architecture-patterns to implement the domain hexagon"

80. "Use @architecture-patterns to design the API adapter"
```

#### Domain-Driven Design

```
81. "Use @architecture-patterns to identify bounded contexts in our domain"

82. "Apply @architecture-patterns to design the aggregate roots"

83. "Use @architecture-patterns to implement domain events"

84. "Apply @architecture-patterns to create the domain services"

85. "Use @architecture-patterns to define the ubiquitous language"
```

#### Pattern Selection

```
86. "Use @architecture-patterns to help me choose between Clean and Hexagonal architecture"

87. "Apply @architecture-patterns to evaluate if DDD is appropriate for our domain"

88. "Use @architecture-patterns to assess the complexity cost of each pattern"

89. "Apply @architecture-patterns to determine the right level of abstraction"

90. "Use @architecture-patterns to compare pattern migration strategies"
```

---

## 4.5 Senior Architect Guidance

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: senior, mentoring, guidance

### Purpose

The `senior-architect` skill provides senior-level architectural guidance for complex decisions, mentoring, and strategic planning.

### 20 Copy-Paste Prompts

```
91. "Use @senior-architect to mentor me on this architectural decision"

92. "Apply @senior-architect to provide guidance on scaling our platform"

93. "Use @senior-architect to review my technical strategy proposal"

94. "Apply @senior-architect to help me communicate this decision to stakeholders"

95. "Use @senior-architect to identify risks in our current architecture"

96. "Apply @senior-architect to create a roadmap for architectural improvements"

97. "Use @senior-architect to evaluate vendor lock-in risks"

98. "Apply @senior-architect to assess our technology stack obsolescence"

99. "Use @senior-architect to guide our platform modernization effort"

100. "Apply @senior-architect to create an architectural vision document"
```

---

## Best Practices for Architecture Skills

### 1. Start with Requirements

Always begin architectural work by clarifying:
- Functional requirements
- Non-functional requirements (performance, security, scalability)
- Constraints (budget, timeline, team skills)
- Business context

### 2. Document Decisions

Every significant decision should have:
- An ADR documenting the rationale
- Consideration of alternatives
- Known trade-offs and limitations

### 3. Review Regularly

Architecture is not static:
- Schedule periodic architecture reviews
- Update ADRs when decisions change
- Track technical debt

### 4. Consider Multiple Perspectives

Good architecture balances:
- Developer experience
- Operational concerns
- Business requirements
- Security implications

---

## Reflection Points for Chapter 4

1. **How do you currently document architectural decisions?**
   - Are decisions easily discoverable?
   - Can you trace why choices were made?

2. **What patterns does your codebase follow?**
   - Is there consistency?
   - Are patterns appropriate for the complexity?

3. **How do you evaluate architectural quality?**
   - What metrics do you use?
   - How do you identify degradation?

4. **How do you handle architectural evolution?**
   - Migration strategies
   - Backward compatibility
   - Technical debt management

---

## Related Skills

| Skill | Relationship |
|-------|--------------|
| `@c4-context` | Document system context |
| `@c4-container` | Document containers |
| `@c4-component` | Document components |
| `@event-sourcing-architect` | Event sourcing patterns |
| `@monorepo-architect` | Monorepo strategies |

---

## Summary

This chapter covered the foundational architecture skills:

- **@architecture**: Decision-making framework for technology choices
- **@architect-review**: Senior-level code and design review
- **@architecture-decision-records**: ADR creation and management
- **@architecture-patterns**: Clean, Hexagonal, and DDD implementation
- **@senior-architect**: Strategic architectural guidance

**Key Takeaway**: Good architecture is about making informed decisions, documenting rationale, and continuously evolving the system while maintaining quality.

---

**Next Chapter**: [Chapter 5: C4 Model Documentation Suite →](chapter-05-c4-documentation.md)
