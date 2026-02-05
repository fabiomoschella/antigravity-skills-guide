# Chapter 20: Database Administration

**Last Updated:** February 5, 2026

---

## Overview

Databases are the heart of most applications, storing critical business data and enabling complex queries. Effective database administration ensures performance, reliability, and security for your data layer.

This chapter covers essential database skills from relational powerhouses like PostgreSQL and MySQL to NoSQL solutions like MongoDB, helping you design, optimize, and maintain database systems effectively.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@postgresql-expert` | PostgreSQL administration | Relational data, complex queries, ACID |
| `@mysql-expert` | MySQL administration | Web applications, replication, scaling |
| `@mongodb-expert` | MongoDB administration | Document data, flexible schemas, scaling |
| `@database-architect` | Database design | Schema design, data modeling, migrations |

---

## 20.1 PostgreSQL Mastery with @postgresql-expert

### Skill Introduction

The `@postgresql-expert` skill provides deep expertise in PostgreSQL, the world's most advanced open-source relational database. It helps you optimize queries, design schemas, configure replication, and troubleshoot performance issues.

**When to use this skill:**
- Query optimization and EXPLAIN analysis
- Schema design and normalization
- Replication and high availability setup
- Performance tuning and configuration
- Backup and recovery planning

**Key strengths:**
- Expert knowledge of PostgreSQL internals
- Experience with performance optimization
- Knowledge of advanced features (JSONB, partitioning, extensions)

---

### PostgreSQL Administration Prompts

#### Optimizing Slow Queries

**Context:** Your application is experiencing slow database queries affecting user experience.

```text
@postgresql-expert Help optimize these slow PostgreSQL queries:

Query 1 (Order History - 8 seconds):
```sql
SELECT o.*, c.name, p.title
FROM orders o
JOIN customers c ON o.customer_id = c.id
JOIN order_items oi ON o.id = oi.order_id
JOIN products p ON oi.product_id = p.id
WHERE o.created_at > NOW() - INTERVAL '30 days'
AND c.segment = 'enterprise'
ORDER BY o.created_at DESC
LIMIT 100;
```

Query 2 (Product Search - 5 seconds):
```sql
SELECT * FROM products
WHERE name ILIKE '%laptop%'
OR description ILIKE '%laptop%'
ORDER BY created_at DESC;
```

Table sizes:
- orders: 50 million rows
- customers: 2 million rows
- products: 500K rows
- order_items: 200 million rows

Please provide:
1. EXPLAIN ANALYZE interpretation guidance
2. Index recommendations
3. Query rewriting suggestions
4. Partitioning recommendations if applicable
5. Configuration tuning for these workloads
6. Monitoring setup for query performance
```

**Expected Output:** Query optimization plan with indexes and rewrites.

---

#### Implementing High Availability

**Context:** You need to set up PostgreSQL replication for high availability.

```text
@postgresql-expert Design a highly available PostgreSQL architecture:

Requirements:
- Zero data loss (synchronous replication)
- Automatic failover under 30 seconds
- Read replicas for reporting workloads
- Cross-region DR capability
- Primary database: 500GB, 10K transactions/second

Current setup:
- Single PostgreSQL 15 instance on AWS
- RDS is an option but prefer self-managed for control

Questions to address:
- Patroni vs RDS vs Aurora
- Synchronous vs asynchronous replication
- Connection pooling (PgBouncer)
- Backup strategy

Please provide:
1. Architecture comparison (self-managed vs RDS vs Aurora)
2. Recommended architecture with diagram description
3. Patroni cluster configuration
4. PgBouncer setup for connection pooling
5. Failover testing approach
6. Backup and point-in-time recovery
7. Monitoring and alerting setup
```

**Expected Output:** HA architecture with Patroni configuration.

---

#### Database Performance Tuning

**Context:** Your PostgreSQL instance is underperforming despite having adequate hardware.

```text
@postgresql-expert Tune our PostgreSQL configuration for better performance:

Hardware:
- 64GB RAM
- 16 vCPUs
- NVMe SSD storage (100K IOPS)

Workload:
- OLTP with some reporting queries
- 70% reads, 30% writes
- Average connection count: 200
- Peak connections: 500

Current issues:
- High CPU wait times
- Connection pool exhaustion
- Autovacuum impacting performance
- Checkpoint spikes

Current config (mostly defaults):
- shared_buffers = 128MB
- work_mem = 4MB
- max_connections = 100

Please provide:
1. postgresql.conf optimizations with explanations
2. Memory allocation strategy
3. Checkpoint tuning
4. Autovacuum configuration
5. Connection pooling recommendations
6. Monitoring queries for tracking improvements
```

**Expected Output:** Configuration tuning guide with specific settings.

---

## 20.2 MySQL Administration with @mysql-expert

### Skill Introduction

The `@mysql-expert` skill provides expertise in MySQL, one of the most popular relational databases. It helps you optimize MySQL for web applications, implement replication, and troubleshoot performance issues.

**When to use this skill:**
- MySQL query optimization
- Replication setup (async, semi-sync, group)
- InnoDB tuning and optimization
- Migration from older MySQL versions
- Aurora MySQL considerations

**Key strengths:**
- Deep knowledge of MySQL internals
- Experience with MySQL at scale
- Familiarity with MySQL variants (MariaDB, Percona)

---

### MySQL Administration Prompts

#### MySQL Replication Setup

**Context:** You need to set up MySQL replication for read scaling.

```text
@mysql-expert Design MySQL replication for our application:

Requirements:
- One primary, three read replicas
- Automatic failover capability
- Geographic distribution (US East, US West)
- Must support GTID-based replication
- Handle replication lag gracefully in application

Current setup:
- MySQL 8.0 single instance
- 200GB database, 5K queries/second
- 80% reads, 20% writes

Please provide:
1. Replication topology design
2. GTID configuration
3. Orchestrator or MySQL Router setup
4. Application connection strategy
5. Lag monitoring and alerting
6. Failover testing procedure
```

**Expected Output:** MySQL replication architecture with configuration.

---

## 20.3 MongoDB Administration with @mongodb-expert

### Skill Introduction

The `@mongodb-expert` skill provides expertise in MongoDB, the leading document database. It helps you design schemas, implement sharding, and optimize queries for document workloads.

**When to use this skill:**
- Schema design for document databases
- Sharding and replica set configuration
- Aggregation pipeline optimization
- Migration from relational to MongoDB
- Atlas configuration and optimization

**Key strengths:**
- Expert in MongoDB internals
- Experience with sharding at scale
- Knowledge of aggregation framework

---

### MongoDB Administration Prompts

#### Designing a Sharded Cluster

**Context:** Your MongoDB instance is hitting scaling limits.

```text
@mongodb-expert Design a sharded MongoDB cluster for our growing dataset:

Current state:
- Single MongoDB 6.0 replica set
- 2TB database, growing 100GB/month
- Queries slowing down significantly
- Collections: events (1B docs), users (50M docs)

Requirements:
- Handle 5 billion documents
- 50K writes/second, 100K reads/second
- Geographic distribution for latency
- Maintain query performance

Workload patterns:
- Events queried by tenant_id and timestamp
- Users queried by email and tenant_id
- Heavy aggregations for reporting

Please provide:
1. Sharding strategy and key selection
2. Cluster topology design
3. Migration approach from replica set
4. Index optimization for sharded queries
5. Balancer configuration
6. Monitoring and alerting
```

**Expected Output:** Sharded cluster design with shard key selection.

---

## 20.4 Database Design with @database-architect

### Skill Introduction

The `@database-architect` skill helps you design effective database schemas, implement data modeling best practices, and plan migrations between database systems.

**When to use this skill:**
- Designing new database schemas
- Normalizing or denormalizing existing schemas
- Planning database migrations
- Choosing between database technologies
- Implementing data modeling patterns

**Key strengths:**
- Experience with multiple database paradigms
- Knowledge of data modeling patterns
- Understanding of trade-offs and best practices

---

### Database Design Prompts

#### Designing a Multi-Tenant Schema

**Context:** You're building a SaaS application and need to design for multi-tenancy.

```text
@database-architect Design a multi-tenant database schema for our SaaS platform:

Application:
- Project management SaaS (like Asana/Jira)
- Expected: 1000 tenants, 50 users on average per tenant
- Largest tenants may have 10K users
- Need strong data isolation for enterprise customers

Data requirements:
- Projects, tasks, comments, attachments
- User management per tenant
- Custom fields per tenant
- Audit logging

Considerations:
- Some tenants need dedicated infrastructure
- Cost efficiency for small tenants
- Query performance at scale

Please provide:
1. Multi-tenancy strategy comparison (shared schema, schema per tenant, database per tenant)
2. Recommended approach with justification
3. Schema design for chosen approach
4. Row-level security implementation
5. Query patterns for tenant isolation
6. Migration path as tenants grow
```

**Expected Output:** Multi-tenant schema design with isolation strategy.

---

## Best Practices Summary

### Performance
1. **Indexing:** Create indexes for common query patterns
2. **Query Analysis:** Regular EXPLAIN analysis
3. **Connection Pooling:** Always use connection pooling
4. **Configuration:** Tune for your workload
5. **Monitoring:** Track slow queries and resource usage

### Reliability
1. **Backups:** Regular, tested backups
2. **Replication:** HA for critical databases
3. **Failover:** Tested automatic failover
4. **Recovery:** Documented RTO and RPO
5. **Maintenance:** Regular vacuum/analyze (PostgreSQL)

### Security
1. **Least Privilege:** Minimal database permissions
2. **Encryption:** At rest and in transit
3. **Audit Logging:** Track sensitive operations
4. **Network Isolation:** Databases in private subnets
5. **Secrets Management:** Rotate credentials regularly

---

## Reflection Points

1. **SQL vs NoSQL:** How do you choose the right database technology?
2. **Scaling:** When do you shard vs scale vertically?
3. **Cloud Managed:** When is RDS/Atlas preferable to self-managed?
4. **Schema Evolution:** How do you handle schema changes in production?

---

**Next Chapter:** [Chapter 21: Network & Security Infrastructure →](chapter-21-network-security.md)
