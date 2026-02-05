# Chapter 4: Software Architecture Fundamentals

**Last Updated:** February 5, 2026

---

## Overview

Architecture is the art of making expensive trade-offs. This chapter covers the foundational skills to design, document, and review software systems. These skills help you move from "coding features" to "designing systems".

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@architecture` | Decision Framework | System design, technology selection |
| `@architect-review` | Validation | Pull requests, design documents |
| `@adr-writer` | Documentation | Creating Architecture Decision Records |
| `@system-design-interviewer` | Practice | Preparing for system design interviews |

---

## 4.1 The Architecture Skill with @architecture

### Skill Introduction

The `@architecture` skill provides a framework for structural decision-making. It forces you to think about non-functional requirements (scalability, availability, latency) before choosing a technology stack.

**When to use this skill:**
- Designing a new system from scratch (Design Doc)
- Evaluating "Buy vs Build" decisions
- Choosing between conflicting technologies (SQL vs NoSQL)
- Planning for high-scale traffic events

**Key strengths:**
- Trade-off analysis
- Non-functional requirement gathering
- Component decomposition
- Data flow modeling

---

### Architecture Prompts

#### Designing a New System

**Context:** You are designing a "Ticket Booking System" that needs to handle massive spikes.

```text
@architecture Design the High-Level Architecture for a Concert Ticketing System:

Constraints:
- Traffic: 100k requests/second during popular sales.
- Inventory: Strict "No double booking" rule.
- Latency: < 500ms for booking confirmation.

Please provide:
1. High-Level Diagram description.
2. Database choice (Relational vs NoSQL) with justification specifically for the "Inventory" problem.
3. Caching strategy (Redis) to handle the read load.
4. Queue mechanism for booking requests.
```

**Expected Output:** A system design focusing on consistency and peak load handling.

---

#### Technology Selection (Trade-off Analysis)

**Context:** You need to choose a database for a social graph.

```text
@architecture Compare technology options for a "Social Friend Graph":

Scenario:
- 10M Users.
- Heavy "Friends of Friends" queries.
- Write heavy (lots of follows/unfollows).

Options: PostgreSQL (Relational) vs Neo4j (Graph) vs DynamoDB (Key-Value).

Please provide:
1. Detailed Trade-off Matrix (Pros/Cons) for each.
2. Recommendation for this specific use case.
3. How to handle the scaling limit of the chosen solution.
```

**Expected Output:** A reasoned technology decision based on access patterns.

---

## 4.2 The Architect Review Skill with @architect-review

### Skill Introduction

The `@architect-review` skill acts as a Senior Staff Engineer reviewing your work. It looks for "Code Smells" at the architectural level, such as tight coupling, circular dependencies, and single points of failure.

**When to use this skill:**
- Reviewing a complex Pull Request
- Auditing a legacy codebase for refactoring
- Validating a proposed API design
- checking for security vulnerabilities in design

**Key strengths:**
- Anti-pattern detection
- Coupling analysis
- Scalability bottleneck identification
- Security design review

---

### Review Prompts

#### Reviewing a Database Schema

**Context:** You are reviewing a proposed schema for an E-commerce Order system.

```text
@architect-review Review this Database Schema for scalability issues:

Tables:
- Users (id, name, email)
- Orders (id, user_id, total, status, created_at)
- OrderItems (id, order_id, product_id, price)
- Products (id, name, current_price, stock)

Concern:
- What happens when "Products.current_price" changes? Does history change?

Please provide:
1. Identification of the "Historical Data Mutation" bug.
2. Suggestion for fixing it (Denormalization).
3. Indexing recommendations for the "Orders" table for a "My Recent Orders" query.
```

**Expected Output:** Identification of critical data integrity issues and fixes.

---

#### Reviewing a Microservice Split

**Context:** A team wants to split the "User Service" into "Profile Service" and "Auth Service".

```text
@architect-review Evaluate this Microservice Split proposal:

Current: Monolithic User Service.
Proposed:
1. Auth Service (Login, Token generation)
2. Profile Service (Name, Avatar, Bio)

Communication:
- Profile Service calls Auth Service to validate tokens on every request.

Please critique:
1. Identify the "Chatty Service" anti-pattern.
2. Analyze the impact on latency.
3. Suggest a better pattern (e.g., JWT validation at Gateway).
```

**Expected Output:** A critique of the distributed system design pointing out coupling and latency risks.

---

## 4.3 Architecture Decision Records with @adr-writer

### Skill Introduction

The `@adr-writer` skill helps you document *why* a decision was made. It follows the standard ADR structure (Context, Decision, Consequences) to create a permanent record of architectural history.

**When to use this skill:**
- Documenting a major technology choice
- Recording a decision to accept Technical Debt
- Explaining a pivot in strategy
- Onboarding new team members (Read the ADRs!)

**Key strengths:**
- Structured writing (MADR format)
- Objective tone
- Explicit trade-off documentation
- "Consequences" analysis (Positive and Negative)

---

### ADR Prompts

#### Writing a Standard ADR

**Context:** You decided to use PostgreSQL instead of MongoDB.

```text
@adr-writer detailed Write an Architecture Decision Record (ADR) for choosing PostgreSQL:

Context:
- We need ACID transactions for financial data.
- Our team knows SQL well.
- The data is highly relational (Users -> Accounts -> Transactions).

Decision: Use PostgreSQL 16.

Please provide:
1. The ADR in Markdown format.
2. Status: Accepted.
3. Consequences:
   - Positive: Data integrity, familiar tooling.
   - Negative: Harder to shard horizontally than Mongo.
```

**Expected Output:** A formal ADR document ready for the repository.

---

## Best Practices Summary

### Simplicity
- **Minimize Moving Parts:** Every new service or database increases operational complexity. Default to "Boring Technology".
- **Monolith First:** Don't start with Microservices. Start with a Modular Monolith.

### Documentation
- **Diagrams over Text:** A C4 Context diagram is worth 10 pages of text.
- **Write it Down:** If it's not in an ADR, it didn't happen.

### Evolution
- **Design for Change:** Architecture is about keeping options open.
- **Two-Way Doors:** distinguish between reversible and irreversible decisions. Spend time on the irreversible ones.

---

## Reflection Points

1. **Conway's Law:** Does your architecture mirror your org chart? Should it?
2. **Resume Driven Development:** Are you choosing tools because they are cool, or because they solve the problem?
3. **Failure Modes:** You designed for success. Did you design for what happens when the Database dies?

---

**Next Chapter:** [Chapter 5: C4 Model & Visual Systems →](05-c4-documentation.md)
