# Chapter 6: Event-Driven Architecture & CQRS

**Last Updated:** February 5, 2026

---

## Overview

As systems scale, strict request/response architectures often become bottlenecks. Event-Driven Architecture (EDA) and Command Query Responsibility Segregation (CQRS) allow for highly scalable, decoupled systems. This chapter covers the skills to design, implement, and manage these asynchronous patterns.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@eda-architect` | Event Strategy | Designing event flows, choosing brokers |
| `@cqrs-expert` | Pattern Implementation | Separating Reads from Writes |
| `@event-sourcing` | Audit & Replay | Financial systems, complete history |
| `@message-queue-expert` | Broker Infrastructure | Kafka, RabbitMQ, SQS configuration |
| `@event-schema-designer` | Contract Management | Schema Registry, Avro, Protobuf |

---

## 6.1 Event-Driven Strategy with @eda-architect

### Skill Introduction

The `@eda-architect` skill helps you design the topology of an event-driven system. It focuses on event granularity, choreography vs orchestration, and handling eventual consistency.

**When to use this skill:**
- Decoupling a monolith into microservices
- Designing a system that needs near real-time updates
- Handling "bursty" traffic loads
- Designing for failure (dead letter queues, retry policies)

**Key strengths:**
- Topology design (Pub/Sub vs Streaming)
- Event Granularity advice (Notification vs State Transfer)
- Failure handling patterns
- Consistency models

---

### EDA Architecture Prompts

#### Designing an E-Commerce Order Flow

**Context:** You are moving from a synchronous "Place Order" API to an async flow to handle Black Friday traffic.

```text
@eda-architect Design an Event-Driven flow for "Order Placement":

Scenario:
- User places order -> Inventory checked -> Payment processed -> Shipping scheduled -> Email sent.
- High Scale (10k orders/min).

Please provide:
1. The choreography diagram (Event storming).
2. List of Events (e.g., `OrderPlaced`, `InventoryReserved`, `PaymentFailed`).
3. How to handle the failure case (Saga Pattern) if Payment fails after Inventory is reserved.
```

**Expected Output:** A robust event flow design including compensation logic (Sagas).

---

#### Choosing the Right Broker

**Context:** You are debating between Kafka, RabbitMQ, and AWS EventBridge.

```text
@eda-architect detailed Compare Message Brokers for our use case:

Requirements:
1. High throughput (Log aggregation).
2. Replayability is mandatory (we need to re-process past events).
3. strict ordering per partition.

Candidates: Kafka vs RabbitMQ vs SQS/SNS.

Please provide:
1. The recommendation.
2. The Trade-off analysis (Complexity vs Features).
3. Why the others are insufficient for "Replayability".
```

**Expected Output:** A reasoned architectural decision on infrastructure.

---

## 6.2 CQRS Implementation with @cqrs-expert

### Skill Introduction

The `@cqrs-expert` skill (Command Query Responsibility Segregation) separates operations that read data from operations that update data. This allows independent scaling of read and write workloads.

**When to use this skill:**
- Optimizing a specialized View Model (e.g., a Dashboard) that requires complex joins
- High-contention domains (Ticket booking systems)
- Systems where reads vastly outnumber writes (1000:1 ratio)
- Implementing Task-Based UIs

**Key strengths:**
- Command handling patterns
- Query projection design
- Denormalization strategies
- Synchronization lag handling

---

### CQRS Prompts

#### Designing a Read Protocol

**Context:** Your "User Profile" write model is a complex normalized SQL database, but the Dashboard search needs to be instant.

```text
@cqrs-expert Design a Read Projection for "User Search":

Write Model: Relational SQL (3rd Normal Form).
Read Requirement: Instant search by Name, Location, and Skills.

Please provide:
1. The Denormalized structure (e.g., for Elasticsearch or Mongo).
2. The Event Handler logic (`UserUpdated` -> Update Read DB).
3. Strategy for handling "Eventual Consistency" (User updates profile, but search result is old for 1 second).
```

**Expected Output:** A design for a high-performance Read Model.

---

## 6.3 Event Sourcing with @event-sourcing

### Skill Introduction

The `@event-sourcing` skill deals with systems where state is determined by a sequence of events, rather than just current state. It is crucial for audit trails, financial ledgers, and debugging.

**When to use this skill:**
- Building improved audit logs (Who changed what and when?)
- Financial/Accounting systems
- Complex domains where "Intent" matters (Why did the state change?)
- Debugging (Replaying events to reproduce a bug)

**Key strengths:**
- Aggregate design
- Snapshotting strategies
- Projection replay
- Versioning events

---

### Event Sourcing Prompts

#### Modeling a Bank Account

**Context:** A simple "Balance" column is not enough. You need a perfect history of transactions.

```text
@event-sourcing Model a Bank Account using Event Sourcing:

Operations: Open Account, Deposit, Withdraw, Application Fee, Close Account.

Please provide:
1. The definition of the Aggregate (`BankAccount`).
2. The list of Events (`MoneyDeposited`, `BalanceOverdrawn`).
3. The "Apply" methods logic (How state changes based on events).
4. Code example in TypeScript.
```

**Expected Output:** A domain model where state is derived purely from an event stream.

---

## 6.4 Schema Design with @event-schema-designer

### Skill Introduction

The `@event-schema-designer` skill ensures that your events are well-defined contracts. In distributed systems, changing an event structure can break downstream consumers. This skill manages that risk.

**When to use this skill:**
- Defining schemas for a Schema Registry (Avro/Protobuf)
- Planning breaking changes in event structures
- Documenting events for other teams
- Ensuring forward/backward compatibility

**Key strengths:**
- Schema Definition (IDL)
- Versioning strategies
- Compatibility modes (Forward, Backward, Full)
- Documentation generation

---

### Schema Prompts

#### Handling a Breaking Change

**Context:** You need to rename a field in an event that 5 other teams consume.

```text
@event-schema-designer Plan a schema evolution for the `OrderCreated` event:

Change: Renaming `userId` to `customerId` and moving `address` into a nested object.
Constraint: Zero downtime. Consumers handle the old format.

Please provide:
1. The strategy (Parallel fields? Versioning the topic?).
2. The Avro/JSON Schema definition for the transition period.
3. The rollout plan for consumers.
```

**Expected Output:** A safe migration plan for a public API contract.

---

## Best Practices Summary

### Design
- **Events are Facts:** Name them in the past tense (`UserRegistered`, not `RegisterUser`).
- **Fat Events:** Prefer including changed data in the event (State Transfer) to avoid consumers calling back to the API.

### Infrastructure
- **Idempotency:** Consumers MUST be able to handle the same message twice without corruption.
- **Poison Pills:** Always have a Dead Letter Queue (DLQ) for messages that crash consumers.

### Complexity
- **Don't Over-Engineer:** If a CRUD API works, don't use Event Sourcing. It adds significant complexity.

---

## Reflection Points

1. **Observability:** Can you trace a request from HTTP -> Event -> Consumer -> Database? (Distributed Tracing).
2. **Consistency:** Is "Eventual Consistency" acceptable for your users? (e.g., "Why didn't my post update immediately?").
3. **Data Privacy:** How do you handle GDPR "Right to be Forgotten" in an immutable Event Store? (Crypto-shredding).

---

**Next Chapter:** [Chapter 7: Monorepo & Build Architecture →](07-monorepo-build.md)
