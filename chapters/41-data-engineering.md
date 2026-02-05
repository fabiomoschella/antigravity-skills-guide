# Chapter 41: Data Engineering

**Last Updated:** February 5, 2026

---

## Overview

Data engineering is the backbone of modern data-driven organizations. It encompasses the design, construction, and maintenance of systems that collect, store, and analyze data at scale. This chapter explores essential skills for building robust data pipelines, implementing ETL/ELT processes, and managing data infrastructure.

In the age of big data, data engineers must balance performance, reliability, and cost while handling increasingly complex data ecosystems. The skills covered here will help you leverage AI assistance to accelerate your data engineering workflows.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@data-engineer` | General data engineering tasks | Pipeline design, architecture decisions, data modeling |
| `@airflow-expert` | Apache Airflow orchestration | DAG creation, workflow automation, scheduling |
| `@spark-expert` | Apache Spark processing | Big data transformations, streaming, analytics |
| `@dbt-expert` | dbt transformations | SQL-based transforms, data testing, documentation |

---

## 41.1 Data Engineering Fundamentals with @data-engineer

### Skill Introduction

The `@data-engineer` skill is your go-to assistant for designing and implementing enterprise-grade data systems. It combines deep knowledge of data architecture patterns, best practices, and modern tooling to help you build scalable, maintainable data infrastructure.

**When to use this skill:**
- Designing new data pipelines from scratch
- Evaluating architecture decisions (batch vs. streaming, lake vs. warehouse)
- Implementing data governance and quality frameworks
- Troubleshooting performance issues in existing pipelines

**Key strengths:**
- Understands both traditional ETL and modern ELT patterns
- Familiar with major cloud data platforms (AWS, GCP, Azure)
- Can generate implementation code in Python, SQL, and Scala

---

### Pipeline Architecture Prompts

#### Designing a Real-Time Data Pipeline

**Context:** You're building a data platform for an e-commerce company that needs real-time insights into customer behavior and order processing.

```text
@data-engineer Design a complete real-time data pipeline architecture for an e-commerce platform with:

Requirements:
- Ingest clickstream events (50K events/second peak)
- Process order transactions in near real-time (< 2 min latency)
- Store raw events for replay and historical analysis
- Feed real-time dashboards for operations team
- Support both streaming analytics and batch ML training

Tech constraints:
- AWS cloud environment
- Existing PostgreSQL for transactions
- Team familiar with Python and SQL

Please provide:
1. Architecture diagram description
2. Technology recommendations with justification
3. Data flow for both streaming and batch paths
4. Estimated infrastructure sizing
5. Key operational considerations
```

**Expected Output:** A comprehensive architecture document with component selection (e.g., Kinesis/Kafka, Spark Streaming, Delta Lake), data flow diagrams, and implementation roadmap.

---

#### Implementing Change Data Capture (CDC)

**Context:** You need to sync changes from an operational PostgreSQL database to a data warehouse without impacting production performance.

```text
@data-engineer Implement a CDC (Change Data Capture) solution to sync data from PostgreSQL to Snowflake:

Current state:
- PostgreSQL 14 with 50+ tables
- Critical tables: orders (100M rows), customers (5M rows), products (500K rows)
- Need to capture inserts, updates, and deletes
- Maximum acceptable lag: 15 minutes

Requirements:
- Minimal impact on source database
- Handle schema changes gracefully
- Support initial full load + ongoing incremental sync
- Provide monitoring and alerting

Please provide:
1. Tool recommendation (Debezium, Airbyte, Fivetran, custom)
2. Architecture design
3. Configuration for the recommended approach
4. Schema evolution handling strategy
5. Monitoring setup
```

**Expected Output:** Detailed implementation guide with Debezium/Kafka configuration, connector setup, and operational runbooks.

---

#### Data Lake Architecture

**Context:** Your organization is transitioning from a traditional data warehouse to a modern lakehouse architecture.

```text
@data-engineer Design a data lakehouse architecture for our analytics platform:

Current situation:
- Legacy Teradata warehouse (expensive, hard to scale)
- Multiple data sources: CRM, ERP, web analytics, IoT sensors
- 500TB historical data, growing 2TB/month
- 50 analysts and data scientists as consumers

Goals:
- Reduce costs by 60%
- Enable both SQL analytics and ML workloads
- Maintain ACID transactions where needed
- Support data governance and access control

Please provide:
1. Lakehouse architecture design (medallion architecture)
2. Storage layer recommendations (Delta Lake/Iceberg/Hudi)
3. Compute layer options
4. Data governance implementation
5. Migration strategy from Teradata
6. Cost estimation comparison
```

**Expected Output:** Complete lakehouse design with bronze/silver/gold layer definitions, technology stack, and migration plan.

---

### Data Quality & Governance Prompts

#### Implementing Data Quality Framework

**Context:** Data quality issues are causing downstream problems. You need a comprehensive quality framework.

```text
@data-engineer Create a data quality framework for our data platform:

Pain points:
- Duplicate records in customer data
- Missing values in critical fields
- Late-arriving data breaking SLAs
- No visibility into data quality trends

Requirements:
- Automated quality checks in pipelines
- Historical quality metrics tracking
- Alerting on quality degradation
- Self-service quality dashboards

Data stack:
- Airflow for orchestration
- Spark for processing
- Delta Lake for storage
- dbt for transformations

Please provide:
1. Quality dimensions to measure (completeness, accuracy, etc.)
2. Tool recommendations (Great Expectations, dbt tests, Soda)
3. Implementation architecture
4. Example quality checks for common patterns
5. Dashboard design for quality monitoring
```

**Expected Output:** Framework document with quality rules, implementation code, and monitoring setup.

---

#### Data Catalog Implementation

**Context:** Your organization lacks visibility into available datasets and their lineage.

```text
@data-engineer Design and implement a data catalog solution:

Current challenges:
- Analysts can't find relevant datasets
- No documentation for existing tables
- Unknown data lineage
- Duplicate datasets across teams

Requirements:
- Automatic metadata extraction from sources
- Search and discovery capabilities
- Data lineage visualization
- Integration with existing tools (Airflow, dbt, Spark)
- Business glossary support

Please provide:
1. Tool comparison (DataHub, Amundsen, Atlan, Collibra)
2. Architecture for chosen solution
3. Metadata extraction setup
4. Lineage integration approach
5. Adoption strategy for the organization
```

**Expected Output:** Catalog implementation plan with tool selection, configuration, and rollout strategy.

---

## 41.2 Apache Airflow with @airflow-expert

### Skill Introduction

The `@airflow-expert` skill specializes in Apache Airflow, the most popular open-source workflow orchestration platform. It can help you design DAGs, implement complex scheduling patterns, troubleshoot issues, and optimize Airflow performance.

**When to use this skill:**
- Creating new DAGs for data pipelines
- Debugging task failures and scheduling issues
- Optimizing Airflow performance (parallelism, pools, queues)
- Migrating workflows from other schedulers
- Implementing custom operators and hooks

**Key strengths:**
- Deep knowledge of Airflow internals and best practices
- Can generate production-ready DAG code
- Familiar with Airflow 2.x features (TaskFlow API, dynamic task mapping)

---

### DAG Development Prompts

#### Creating a Production-Ready ETL DAG

**Context:** You need to build a daily ETL pipeline that extracts data from multiple sources, transforms it, and loads it into a data warehouse.

```text
@airflow-expert Create a production-ready Airflow DAG for a daily ETL pipeline:

Pipeline requirements:
- Extract from: PostgreSQL (3 tables), S3 (JSON files), REST API
- Transform: Clean, deduplicate, join datasets
- Load: Snowflake data warehouse
- Schedule: Daily at 2 AM UTC
- SLA: Complete within 2 hours

Operational requirements:
- Idempotent tasks (safe to retry)
- Proper error handling and notifications
- Task-level retries with exponential backoff
- Monitoring via Slack alerts
- Backfill support for historical runs

Please provide:
1. Complete DAG code using TaskFlow API
2. Custom operators if needed
3. Configuration management approach
4. Testing strategy
5. Deployment instructions
```

**Expected Output:** Complete Python DAG file with proper structure, error handling, and documentation.

---

#### Dynamic Task Generation

**Context:** You need to process files from S3 where the number of files varies each day.

```text
@airflow-expert Implement a DAG with dynamic task mapping for processing variable S3 files:

Scenario:
- S3 bucket receives 10-100 CSV files daily
- Each file needs: validation, transformation, loading
- Files can be processed in parallel
- Failed files shouldn't block others
- Need summary task after all files processed

Requirements:
- Use Airflow 2.x dynamic task mapping
- Handle failures gracefully (continue on error)
- Log processing statistics per file
- Send summary notification with success/failure counts

Please provide:
1. DAG code with expand() for dynamic mapping
2. Error handling strategy
3. XCom usage for passing results
4. Trigger rules for summary task
```

**Expected Output:** DAG implementation using modern Airflow 2.x patterns with dynamic task generation.

---

#### Cross-DAG Dependencies

**Context:** You have multiple DAGs that need to run in sequence, managed by different teams.

```text
@airflow-expert Design a cross-DAG dependency pattern for our data platform:

Current DAGs:
- raw_ingestion_dag: Loads raw data (runs hourly)
- staging_transform_dag: Transforms to staging (depends on ingestion)
- datamart_build_dag: Builds datamarts (depends on staging)
- ml_feature_dag: Generates ML features (depends on datamarts)

Challenges:
- DAGs owned by different teams
- Need loose coupling (avoid breaking changes)
- Some DAGs run on different schedules
- Need visibility into overall pipeline status

Please provide:
1. Comparison of approaches (ExternalTaskSensor, TriggerDagRunOperator, Datasets)
2. Recommended pattern using Airflow Datasets (2.4+)
3. Implementation code
4. Monitoring dashboard design
5. Handling of partial failures
```

**Expected Output:** Cross-DAG dependency implementation with Datasets API and monitoring setup.

---

### Airflow Operations Prompts

#### Performance Optimization

**Context:** Your Airflow installation is struggling with scaling issues.

```text
@airflow-expert Optimize our Airflow deployment for better performance:

Current issues:
- Scheduler lag of 30+ seconds
- Tasks queuing for too long
- Webserver slow to load
- Database CPU at 80%

Environment:
- Airflow 2.5 on Kubernetes (MWAA-like setup)
- 200 DAGs, 5000 tasks/day
- PostgreSQL backend
- Celery executor with 20 workers

Please provide:
1. Diagnosis steps to identify bottlenecks
2. Configuration tuning recommendations
3. Database optimization (indexes, queries)
4. Scaling strategy (horizontal vs vertical)
5. Monitoring metrics to track
```

**Expected Output:** Performance optimization guide with specific configuration changes and expected improvements.

---

## 41.3 Apache Spark with @spark-expert

### Skill Introduction

The `@spark-expert` skill provides deep expertise in Apache Spark for large-scale data processing. Whether you're building batch ETL jobs, streaming applications, or ML pipelines, this skill can help you write efficient, scalable Spark code.

**When to use this skill:**
- Writing Spark jobs (Python, Scala, SQL)
- Optimizing Spark performance (partitioning, caching, broadcast)
- Implementing Spark Streaming or Structured Streaming
- Building Spark ML pipelines
- Troubleshooting Spark job failures

**Key strengths:**
- Expert in Spark internals (catalyst optimizer, tungsten)
- Can generate optimized code for specific use cases
- Familiar with Databricks, EMR, and other Spark platforms

---

### Spark Development Prompts

#### Optimizing a Slow Spark Job

**Context:** A critical Spark job is taking too long and causing SLA breaches.

```text
@spark-expert Optimize this slow Spark job that processes sales data:

Current performance:
- Runtime: 4 hours (SLA: 1 hour)
- Data size: 500GB partitioned Parquet
- Cluster: 10 x r5.2xlarge workers
- Multiple shuffles and OOM errors

Job description:
- Read sales transactions (500GB)
- Join with customer dimension (50GB)
- Join with product dimension (5GB)
- Aggregate by region/category/month
- Write to Delta Lake

Current code pattern:
```python
sales_df = spark.read.parquet("s3://bucket/sales/")
customers_df = spark.read.parquet("s3://bucket/customers/")
products_df = spark.read.parquet("s3://bucket/products/")

result = sales_df \
    .join(customers_df, "customer_id") \
    .join(products_df, "product_id") \
    .groupBy("region", "category", col("date").substr(0, 7).alias("month")) \
    .agg(sum("amount"), count("*"))
```

Please provide:
1. Analysis of performance bottlenecks
2. Optimized code with explanations
3. Configuration recommendations (spark.conf)
4. Partitioning and bucketing strategy
5. Monitoring approach for future runs
```

**Expected Output:** Optimized Spark job with broadcast joins, proper partitioning, and configuration tuning.

---

#### Real-Time Streaming Pipeline

**Context:** You need to process events from Kafka in real-time for fraud detection.

```text
@spark-expert Build a Spark Structured Streaming application for fraud detection:

Requirements:
- Consume transactions from Kafka topic (10K events/sec)
- Enrich with customer data from Delta Lake
- Apply ML model for fraud scoring
- Output: suspicious transactions to alert topic, all to Delta Lake
- Exactly-once processing semantics
- Handle late arrivals (5-minute watermark)

Integration points:
- Kafka cluster (Confluent Cloud)
- Delta Lake on S3
- MLflow model registry

Please provide:
1. Complete streaming application code
2. Watermarking and windowing strategy
3. State management approach
4. Checkpointing configuration
5. Scaling and monitoring recommendations
```

**Expected Output:** Production-ready Structured Streaming application with all components.

---

## 41.4 dbt Transformations with @dbt-expert

### Skill Introduction

The `@dbt-expert` skill specializes in dbt (data build tool), the standard for SQL-based data transformations. It can help you design dbt projects, write efficient models, implement testing strategies, and optimize dbt performance.

**When to use this skill:**
- Structuring dbt projects (staging, intermediate, marts)
- Writing complex SQL transformations
- Implementing dbt tests and documentation
- Optimizing dbt build performance
- Setting up dbt CI/CD

**Key strengths:**
- Expert in dbt best practices and patterns
- Can generate well-structured, maintainable models
- Familiar with dbt Cloud and dbt Core

---

### dbt Development Prompts

#### Designing a dbt Project Structure

**Context:** You're starting a new dbt project and want to follow best practices.

```text
@dbt-expert Design a dbt project structure for our e-commerce analytics:

Domain areas:
- Sales & Orders
- Customer Analytics
- Product Performance
- Marketing Attribution
- Finance & Revenue

Data sources:
- PostgreSQL (transactional)
- Stripe (payments)
- Google Analytics
- Shopify

Team:
- 5 analytics engineers
- Multiple downstream consumers (BI, ML)

Please provide:
1. Directory structure following best practices
2. Naming conventions
3. Staging layer design
4. Intermediate models approach
5. Mart layer organization
6. dbt_project.yml configuration
7. packages.yml with recommended packages
```

**Expected Output:** Complete dbt project skeleton with folder structure, configurations, and example models.

---

#### Implementing Slowly Changing Dimensions

**Context:** You need to track historical changes to customer attributes.

```text
@dbt-expert Implement SCD Type 2 for customer dimension in dbt:

Source table: raw.customers
- customer_id (PK)
- email
- name
- segment (changes over time)
- address (changes over time)
- updated_at

Requirements:
- Track all historical changes to segment and address
- Maintain current/historical flags
- Support point-in-time analysis
- Efficient incremental processing
- Handle late-arriving updates

Please provide:
1. Snapshot configuration
2. Supporting staging models
3. Dimension model with surrogate keys
4. Example usage in fact tables
5. Testing approach for SCDs
```

**Expected Output:** dbt snapshot configuration and dimension model with complete SCD Type 2 implementation.

---

#### dbt Testing Strategy

**Context:** You need a comprehensive testing strategy for your dbt project.

```text
@dbt-expert Create a testing strategy for our dbt project:

Current state:
- 50+ models across staging/marts
- No tests implemented yet
- Data quality issues reported by consumers

Requirements:
- Catch data quality issues early
- Validate business logic
- Monitor for anomalies
- Integrate with CI/CD
- Provide visibility to stakeholders

Please provide:
1. Testing philosophy (what to test where)
2. Schema tests approach
3. Custom data test examples
4. dbt-expectations implementation
5. dbt-audit-helper for refactoring
6. CI/CD integration with dbt Cloud or GitHub Actions
7. Test coverage monitoring
```

**Expected Output:** Comprehensive testing guide with example tests and CI/CD configuration.

---

## 41.5 Advanced Topics

### Designing Medallion Architecture

```text
@data-engineer Design a medallion (bronze/silver/gold) architecture for our data lakehouse:

Domain: Financial services data platform

Data sources:
- Core banking system (transactions, accounts)
- CRM (customers, interactions)
- Market data feeds (real-time prices)
- Regulatory reports

Requirements:
- Clear separation of concerns between layers
- Data quality enforcement at each layer
- Support for both batch and streaming
- Lineage and audit capabilities
- Cost-effective storage tiering

Please provide:
1. Layer definitions and responsibilities
2. Schema evolution strategy per layer
3. Data quality gates between layers
4. Retention policies
5. Access control model
6. Example data flows
```

---

### Implementing Data Mesh

```text
@data-engineer Help us implement data mesh principles in our organization:

Current challenges:
- Centralized data team is bottleneck
- Domain teams have no data ownership
- Slow time to value for new data products
- Governance is reactive, not preventive

Organization:
- 5 product domains (Payments, Users, Orders, Inventory, Marketing)
- Each domain has engineering team
- Central platform team for infrastructure

Please provide:
1. Data mesh implementation roadmap
2. Domain ownership model
3. Self-serve data platform components
4. Federated governance approach
5. Data product specifications
6. Technology recommendations
7. Change management strategy
```

---

## Best Practices Summary

### Data Pipeline Design
1. **Idempotency:** All pipelines should be safe to retry
2. **Monitoring:** Implement comprehensive observability
3. **Testing:** Test data pipelines like you test code
4. **Documentation:** Maintain living documentation

### Performance
1. **Partitioning:** Choose partition keys carefully
2. **Incremental:** Process incrementally when possible
3. **Caching:** Use caching strategically
4. **Right-sizing:** Match resources to workload

### Governance
1. **Quality:** Implement quality checks at every stage
2. **Lineage:** Track data from source to consumption
3. **Access Control:** Implement least-privilege access
4. **Retention:** Define and enforce retention policies

---

## Reflection Points

1. **Architecture Decisions:** How do you balance real-time vs batch processing needs?
2. **Tool Selection:** When would you choose Airflow vs Prefect vs Dagster?
3. **Cost Optimization:** How can you reduce cloud data platform costs?
4. **Team Structure:** Should data engineering be centralized or embedded in domains?

---

**Next Chapter:** [Chapter 42: Machine Learning →](chapter-42-machine-learning.md)
