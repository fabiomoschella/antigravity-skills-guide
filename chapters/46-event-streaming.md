# Chapter 46: Event Streaming

**Last Updated:** February 5, 2026

---

## Overview

Event streaming enables real-time data processing and event-driven architectures. It forms the backbone of modern distributed systems, allowing applications to react to events as they happen rather than relying on batch processing.

This chapter covers essential skills for building robust, scalable streaming data platforms.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@kafka-expert` | Apache Kafka mastery | Event streaming, messaging |
| `@streaming-architect` | Stream architecture | Real-time pipelines |
| `@event-processing` | Event processing | CEP, stream analytics |
| `@schema-registry-expert` | Schema management | Event schema evolution |

---

## 46.1 Apache Kafka with @kafka-expert

### Skill Introduction

The `@kafka-expert` skill provides deep expertise in Apache Kafka for building event streaming platforms. It helps you design topics, configure producers/consumers, and operate Kafka clusters at scale.

**When to use this skill:**
- Building event-driven architectures
- Real-time data pipelines
- Message queue replacement
- Change data capture

**Key strengths:**
- Deep Kafka internals knowledge
- Experience with cluster operations
- Understanding of Kafka ecosystem

---

### Apache Kafka Prompts

#### Designing Kafka-Based Event Platform

**Context:** You're building an event streaming platform for a financial services company.

```text
@kafka-expert Design enterprise Kafka event streaming platform:

Requirements:
- 500K events per second peak
- Multi-datacenter deployment
- 30-day event retention
- Exactly-once semantics where needed
- Schema registry for contracts
- Real-time and batch consumers

Event types:
- Transaction events (high volume, low latency)
- User activity events
- System audit logs
- Change data capture from databases
- External partner integrations

Operational requirements:
- Zero message loss for critical events
- Sub-second end-to-end latency
- High availability (99.99%)
- Disaster recovery
- Encryption in transit and at rest

Please provide:
1. Cluster sizing and architecture
2. Topic design and partitioning strategy
3. Producer configuration for guarantees
4. Consumer group design
5. Schema registry setup
6. Security configuration
7. Monitoring and alerting
8. Disaster recovery approach
```

**Expected Output:** Enterprise Kafka platform design.

---

#### Kafka Performance Optimization

**Context:** Your Kafka cluster is experiencing performance issues.

```text
@kafka-expert Optimize Kafka cluster performance:

Current issues:
- Consumer lag growing during peaks
- Producer latency spikes to 500ms+
- Broker CPU at 90% utilization
- Rebalances taking 10+ minutes

Current setup:
- 6 broker cluster
- 200 topics, 2000 partitions
- 100 consumer groups
- 50K messages/second average

Constraints:
- Cannot add brokers immediately
- Limited maintenance windows
- Must maintain availability

Please provide:
1. Performance diagnosis approach
2. Broker configuration tuning
3. Producer optimization
4. Consumer optimization
5. Partition rebalancing strategy
6. Topic configuration review
7. JVM tuning recommendations
8. Long-term scaling plan
```

**Expected Output:** Kafka performance optimization guide.

---

## 46.2 Stream Architecture with @streaming-architect

### Skill Introduction

The `@streaming-architect` skill provides expertise in designing streaming data architectures. It helps you build real-time data pipelines that process, transform, and analyze events as they flow.

**When to use this skill:**
- Designing real-time analytics
- Building data processing pipelines
- Event-driven microservices
- Stream processing decisions

**Key strengths:**
- End-to-end streaming design
- Technology selection expertise
- Understanding of streaming patterns

---

### Stream Architecture Prompts

#### Real-Time Analytics Pipeline

**Context:** You need to build a real-time analytics platform for user behavior.

```text
@streaming-architect Design real-time analytics pipeline:

Data sources:
- Clickstream from web/mobile (50K events/second)
- Transaction events (10K events/second)
- Inventory updates (1K events/second)
- External data feeds

Analytics requirements:
- Real-time dashboard updates (< 5 second delay)
- Session aggregations (active users, session duration)
- Funnel analysis in real-time
- Anomaly detection on metrics
- A/B test metric calculations
- Historical comparison (vs yesterday, last week)

Output destinations:
- Real-time dashboards (WebSocket)
- Alerting system
- Data warehouse (for deeper analysis)
- Machine learning features

Please provide:
1. Overall architecture design
2. Stream processing framework selection
3. Windowing and aggregation strategy
4. State management approach
5. Late data handling
6. Exactly-once processing design
7. Scaling considerations
8. Monitoring and observability
```

**Expected Output:** Real-time analytics architecture.

---

## 46.3 Event Processing with @event-processing

### Skill Introduction

The `@event-processing` skill provides expertise in complex event processing (CEP) and stream analytics. It helps you build sophisticated event detection, pattern matching, and real-time decision systems.

**When to use this skill:**
- Complex event pattern detection
- Real-time alerting and decisions
- Fraud detection systems
- IoT event processing

**Key strengths:**
- CEP patterns and algorithms
- Stream processing frameworks
- Real-time decision systems

---

### Event Processing Prompts

#### Building Fraud Detection System

**Context:** You need to build a real-time fraud detection system.

```text
@event-processing Design real-time fraud detection system:

Transaction types:
- Card payments (100K/minute)
- Wire transfers
- ACH transactions
- Peer-to-peer payments

Detection requirements:
- Sub-second decision for card payments
- Pattern detection (velocity, geography, device)
- Behavioral anomaly detection
- Known fraud pattern matching
- Network analysis (related accounts)

Patterns to detect:
- Velocity checks (X transactions in Y minutes)
- Geographic impossibility (transactions in distant locations)
- Device fingerprint changes
- Unusual merchant categories
- Amount pattern anomalies

Please provide:
1. Event stream architecture
2. CEP rule engine design
3. Pattern matching implementation
4. State management for user profiles
5. Model scoring integration
6. Alert generation and routing
7. False positive management
8. Performance optimization
```

**Expected Output:** Fraud detection system design.

---

## 46.4 Schema Management with @schema-registry-expert

### Skill Introduction

The `@schema-registry-expert` skill provides expertise in managing event schemas and data contracts. It helps you implement schema evolution strategies that maintain compatibility across producers and consumers.

**When to use this skill:**
- Implementing schema registry
- Schema evolution planning
- Breaking change management
- Data contract enforcement

**Key strengths:**
- Schema evolution patterns
- Compatibility rules
- Data governance

---

### Schema Registry Prompts

#### Implementing Schema Governance

**Context:** You need to implement schema governance for your event platform.

```text
@schema-registry-expert Implement schema governance for Kafka:

Current situation:
- 200 topics with no schema enforcement
- Frequent breaking changes causing consumer failures
- No documentation of event formats
- Multiple teams producing events

Goals:
- Enforce schemas on all new topics
- Migrate existing topics gradually
- Prevent breaking changes
- Enable schema discovery

Requirements:
- Avro/Protobuf/JSON Schema support
- Compatibility enforcement
- Schema evolution workflow
- CI/CD integration
- Developer self-service

Please provide:
1. Schema registry deployment
2. Compatibility strategy by topic type
3. Schema evolution workflow
4. CI/CD pipeline integration
5. Migration plan for existing topics
6. Developer guidelines
7. Schema documentation approach
8. Breaking change process
```

**Expected Output:** Schema governance implementation plan.

---

## Best Practices Summary

### Event Design
1. **Immutability:** Events are immutable facts
2. **Self-Describing:** Include schema version
3. **Ordering:** Design for out-of-order delivery
4. **Idempotency:** Enable safe replay
5. **Schemas:** Define and enforce contracts

### Processing
1. **Exactly-Once:** When business requires
2. **Checkpointing:** Regular state saves
3. **Backpressure:** Handle overload gracefully
4. **Windowing:** Choose appropriate window types
5. **Late Data:** Define handling policies

### Operations
1. **Lag Monitoring:** Track consumer lag
2. **Throughput:** Monitor message rates
3. **Latency:** Measure end-to-end
4. **Dead Letters:** Handle poison pills
5. **Replay:** Enable event replay

---

## Reflection Points

1. **Event Granularity:** Fine-grained vs coarse events?
2. **Retention:** How long to keep events?
3. **Ordering Guarantees:** When is ordering critical?
4. **Kafka vs Alternatives:** When to choose Kafka vs other solutions?

---

**Next Chapter:** [Chapter 47: Productivity →](chapter-47-productivity.md)
