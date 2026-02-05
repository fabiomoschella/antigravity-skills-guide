# Chapter 5: C4 Model & Visual Systems

**Last Updated:** February 5, 2026

---

## Overview

Software architecture is notoriously difficult to communicate. The "C4 Model" (Context, Container, Component, Code) is the industry standard for visualizing software architecture at different levels of abstraction. This chapter covers the skills to create clarity through diagrams and visual models using "Diagrams as Code".

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@c4-architect` | Core Methodology | Abstraction levels strategy |
| `@plantuml-expert` | Diagram Generation | Creating standard diagrams |
| `@mermaid-expert` | Markdown Diagrams | Quick, inline documentation |
| `@system-context` | Level 1: Scope | High-level overviews |
| `@container-diagram` | Level 2: Tech Stack | Applications & databases |

---

## 5.1 The C4 Philosophy with @c4-architect

### Skill Introduction

The `@c4-architect` skill acts as a mentor for the C4 methodology. NOT a drawing tool itself, but a guide on *what* to draw. It ensures you don't mix abstraction levels (e.g., showing a SQL table implementation on a high-level system diagram).

**When to use this skill:**
- Deciding which diagrams are necessary for a project
- Reviewing existing diagrams for clarity and errors
- Defining the scope and boundaries of a system
- Explaining the C4 model to a team

**Key strengths:**
- Abstraction level discipline
- Scope definition
- Notation standards (Person, System, Container)
- Relationship naming advice

---

### C4 Methodology Prompts

#### Planning Documentation Strategy

**Context:** You are documenting a legacy Monolith that is being split into Microservices.

```text
@c4-architect Plan a documentation strategy for our "Legacy -> Microservices" migration:

System: "E-Commerce Monolith" (Java/Spring)
New State:
- "Checkout Service" (Go)
- "Inventory Service" (Python)
- "Legacy Core" (Remaining Java)

Please provide:
1. List of recommended diagrams (e.g., L1 Context, L2 Container).
2. Strategy for showing the "To-Be" vs "As-Is" states.
3. How to represent the "Strangler Fig" pattern in diagrams.
```

**Expected Output:** A documentation plan prioritizing which views to create.

---

## 5.2 Context Diagrams (Level 1) with @system-context

### Skill Introduction

The `@system-context` skill focuses on the "Big Picture". It shows your system, the users who use it, and the external systems it interacts with. It hides ALL technical details (no "Java", no "SQL").

**When to use this skill:**
- Explaining the product to non-technical stakeholders
- Defining system boundaries (What do we own? What is external?)
- Onboarding new employees to the domain
- Sales decks and pitch presentations

**Key strengths:**
- High-level abstractions
- External dependency identification
- User persona mapping
- Clear boundary definition

---

### Context Diagram Prompts

#### Visualizing System Scope

**Context:** You are building a "Ride Sharing" app.

```text
@system-context Generate PlantUML for the "Ride Sharing System" Context Diagram:

Users:
- Rider (Mobile App user)
- Driver (Mobile App user)
- Admin (Web Portal user)

External Systems:
- Google Maps (Navigation)
- Stripe (Payments)
- Twilio (SMS Notifications)

Please provide:
1. Complete PlantUML Code (using C4_Context.puml).
2. Descriptive labels for relationships (e.g., "Sends ride request").
```

**Expected Output:** A PlantUML script that renders a clear System Context diagram.

---

## 5.3 Container Diagrams (Level 2) with @container-diagram

### Skill Introduction

The `@container-diagram` skill zooms in one level. It reveals the "Containers" (Applications, Services, Databases, File Stores). This is where technical choices (React, Postgres, API Gateway) are documented.

**When to use this skill:**
- Software Architecture Documents (SAD)
- Explaining the tech stack to developers
- Security reviews (Where is data stored?)
- Infrastructure planning

**Key strengths:**
- Technology stack mapping
- Protocol definition (HTTPS, gRPC, JDBC)
- Application boundary definition
- Data store identification

---

### Container Diagram Prompts

#### Documenting Microservices

**Context:** Your "Ride Sharing" system is more complex than just "The System".

```text
@container-diagram Generate PlantUML for the "Ride Sharing" Container View:

Scope: Inside the "Ride Sharing System"

Containers:
1. "Mobile App" (Flutter)
2. "API Gateway" (Nginx)
3. "Ride Matching Service" (Go)
4. "Billing Service" (Node.js)
5. "Ride Database" (Postgres)
6. "Cache" (Redis)

Please provide:
1. Complete PlantUML Code (using C4_Container.puml).
2. Relationships showing protocol and direction (e.g., App -> Gateway via HTTPS/JSON).
3. Notes on technology choices.
```

**Expected Output:** A technical high-level view of the architecture.

---

## 5.4 Diagrams as Code with @mermaid-expert

### Skill Introduction

The `@mermaid-expert` skill enables you to write diagrams directly in your Markdown documentation. It is perfect for quick, inline visualizations that live alongside your code in GitHub/GitLab.

**When to use this skill:**
- Adding flowcharts to Pull Request descriptions
- Simple Sequence Diagrams for feature logic
- State Machines for UI logic
- Quick Entity Relationship Diagrams (ERD)

**Key strengths:**
- Markdown native
- Sequence Diagrams
- State Diagrams
- Flowcharts
- Git integration

---

### Mermaid Prompts

#### Visualizing a Logic Flow

**Context:** You are documenting the "Password Reset" logic in a README.

```text
@mermaid-expert Create a Sequence Diagram for "Password Reset":

Actors: User, Browser, API, EmailProvider, Database.

Flow:
1. User clicks "Forgot Password".
2. Browser sends email to API.
3. API checks DB.
4. API generates token.
5. API sends email via Provider.
6. User clicks link.
7. User enters new password.

Please provide:
1. Valid Mermaid.js sequence diagram code.
2. Use "alt" block for the "Email not found" scenario.
```

**Expected Output:** A Mermaid code block that renders a sequence diagram.

---

## Best Practices Summary

### Consistency
- **Standard Notation:** Stick to the C4 naming (Person, System, Container). Don't invent "Bucket" or "Module" unless defined.
- **Direction:** Ideally, data flows Top-to-Bottom or Left-to-Right.

### Maintenance
- **Diagrams as Code:** Binary images (PNG/JPG) rot. Code (PlantUML/Mermaid) can be edited. Always store the source.
- **Keep it High Level:** The more detail you add (Code Level), the faster it becomes obsolete. Stick to Level 1 and 2 for long-term docs.

---

## Reflection Points

1. **Audience:** Who is this diagram for? (CEO vs Junior Dev).
2. **Obsolete Docs:** When was the last time you verified the diagram matches production?
3. **Detail Trap:** Are you documenting *classes* instead of *components*? (Stop, that's Level 4).

---

**Next Chapter:** [Chapter 6: Event-Driven Architecture & CQRS →](06-event-driven-cqrs.md)
