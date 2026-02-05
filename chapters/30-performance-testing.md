# Chapter 30: Performance & Load Testing

**Last Updated:** February 5, 2026

---

## Overview

Performance testing validates that your application meets speed and scalability requirements under various conditions. From baseline performance measurement to load testing at scale, understanding performance characteristics is crucial for production readiness.

This chapter covers essential performance testing skills for measuring, analyzing, and optimizing application performance.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@performance-tester` | Performance testing | Strategy, baseline, benchmarking |
| `@k6-expert` | k6 load testing | Script development, testing |
| `@jmeter-expert` | JMeter testing | Complex scenarios, enterprise |
| `@performance-analyst` | Results analysis | Bottleneck identification |
| `@gatling-expert` | Gatling | Scala-based load testing |
| `@locust-expert` | Locust | Python load testing |
| `@benchmark-expert` | Benchmarking | Micro-benchmarks |
| `@stress-test-expert` | Stress testing | Breaking points |
| `@web-vitals-expert` | Web Vitals | Core web vitals |
| `@lighthouse-expert` | Lighthouse | Web performance audit |

---

## 30.1 Performance Testing Strategy with @performance-tester

### Skill Introduction

The `@performance-tester` skill provides expertise in designing comprehensive performance testing strategies. It helps you plan tests, define metrics, and establish performance baselines.

**When to use this skill:**
- Designing performance test strategy
- Defining performance requirements
- Establishing baseline metrics
- Creating performance test plans

**Key strengths:**
- Experience with performance testing methodologies
- Knowledge of performance metrics
- Understanding of testing types (load, stress, soak)

---

### Performance Testing Prompts

#### Designing Performance Test Strategy

**Context:** You need to create a performance testing strategy for your application before a major launch.

```text
@performance-tester Design performance testing strategy for our e-commerce platform:

Application overview:
- Node.js API serving mobile and web clients
- 50 API endpoints
- PostgreSQL database
- Redis caching
- Runs on Kubernetes (AWS EKS)

Expected load:
- Normal: 1,000 concurrent users
- Peak: 10,000 concurrent users (Black Friday)
- Critical transactions: checkout, search, product pages

Current state:
- No formal performance testing
- Production issues during previous sale events
- Unknown breaking point

Requirements:
- Establish performance baselines
- Identify breaking points
- Validate scaling capability
- SLA: P95 latency < 500ms, error rate < 0.1%

Please provide:
1. Performance testing strategy document
2. Types of tests to run (load, stress, soak, spike)
3. Test scenarios and user journeys
4. Environment recommendations
5. Metrics to collect and analyze
6. Tool recommendations
7. Testing cadence and CI/CD integration
```

**Expected Output:** Comprehensive performance testing strategy.

---

## 30.2 k6 Load Testing with @k6-expert

### Skill Introduction

The `@k6-expert` skill provides expertise in k6, a modern load testing tool built for developers. It helps you write efficient load tests using JavaScript and integrate them into CI/CD pipelines.

**When to use this skill:**
- Writing k6 test scripts
- Configuring load patterns
- Analyzing k6 results
- CI/CD integration

**Key strengths:**
- Deep k6 knowledge
- Experience with test scripting
- Understanding of load patterns

---

### k6 Testing Prompts

#### Creating k6 Load Tests

**Context:** You want to implement k6 for load testing your API.

```text
@k6-expert Create k6 load tests for our REST API:

Endpoints to test:
- POST /api/auth/login (authentication)
- GET /api/products (list with pagination)
- GET /api/products/:id (detail)
- POST /api/cart (add to cart)
- POST /api/orders (checkout - most critical)

Load requirements:
- Baseline: 100 VUs for 10 minutes
- Load test: Ramp 0→500 VUs over 5 min, hold 10 min
- Stress test: Ramp to breaking point
- Spike test: Sudden 10x traffic increase

Test requirements:
- Realistic user flow (browse → cart → checkout)
- Authentication token management
- Dynamic data from responses
- Thresholds for pass/fail

Please provide:
1. k6 project structure
2. Test scripts for each scenario type
3. Shared utilities (auth, data generation)
4. Threshold configuration
5. Custom metrics
6. CI/CD integration (GitHub Actions)
7. Results visualization approach
```

**Expected Output:** Complete k6 test implementation.

---

## 30.3 JMeter Testing with @jmeter-expert

### Skill Introduction

The `@jmeter-expert` skill provides expertise in Apache JMeter for enterprise-grade performance testing. It helps you create complex test scenarios with JMeter's extensive features.

**When to use this skill:**
- Complex protocol testing
- Enterprise testing scenarios
- Distributed load testing
- Legacy system testing

**Key strengths:**
- Deep JMeter expertise
- Experience with distributed testing
- Knowledge of protocol support

---

### JMeter Testing Prompts

#### Distributed Load Testing

**Context:** You need to run large-scale distributed load tests.

```text
@jmeter-expert Set up distributed JMeter testing for large-scale load:

Requirements:
- Generate 10,000 concurrent users
- Test from multiple geographic locations
- Support for HTTP/HTTPS and WebSocket
- Parameterized test data (100K users)
- Real-time monitoring during tests

Infrastructure:
- AWS available for test infrastructure
- Need to run on-demand for cost efficiency
- Tests scheduled for specific dates

Test scenario:
- E-commerce checkout flow
- 10 steps with think time
- Dynamic correlation of session tokens

Please provide:
1. Distributed JMeter architecture
2. Master-slave configuration
3. AWS infrastructure setup
4. Test data management
5. Real-time monitoring solution
6. Results aggregation
7. Cost optimization
```

**Expected Output:** Distributed JMeter testing setup.

---

## 30.4 Performance Analysis with @performance-analyst

### Skill Introduction

The `@performance-analyst` skill provides expertise in analyzing performance test results and identifying bottlenecks. It helps you interpret metrics and recommend optimizations.

**When to use this skill:**
- Analyzing test results
- Identifying bottlenecks
- Recommending optimizations
- Creating performance reports

**Key strengths:**
- Experience with metrics analysis
- Knowledge of bottleneck patterns
- Understanding of optimization strategies

---

### Performance Analysis Prompts

#### Analyzing Load Test Results

**Context:** You've completed load testing and need to analyze results.

```text
@performance-analyst Analyze these load test results and identify issues:

Test configuration:
- 500 concurrent users over 30 minutes
- E-commerce checkout flow

Results summary:
- Median response time: 250ms
- P95 response time: 2,500ms
- P99 response time: 8,000ms
- Error rate: 2.3%
- Throughput: 150 requests/second

Observations:
- Response time degradation started at 300 users
- Database CPU hit 95% at peak
- Memory usage grew steadily (no plateau)
- Some 504 timeout errors from API gateway

Breakdown by endpoint:
- /products: 100ms median, 500ms P95
- /checkout: 500ms median, 5,000ms P95 ⚠️
- /search: 200ms median, 3,000ms P95 ⚠️

Please provide:
1. Results interpretation
2. Bottleneck identification
3. Root cause hypotheses
4. Optimization recommendations
5. Follow-up tests to run
6. Infrastructure scaling recommendations
7. Performance report summary for stakeholders
```

**Expected Output:** Performance analysis with recommendations.

---

## Best Practices Summary

### Test Design
1. **Realistic Scenarios:** Model actual user behavior
2. **Think Time:** Include realistic pauses
3. **Data Variety:** Use diverse test data
4. **Gradual Ramp:** Don't spike immediately
5. **Steady State:** Run long enough for stability

### Metrics
1. **Response Time:** P50, P95, P99 latencies
2. **Throughput:** Requests per second
3. **Error Rate:** Failed requests percentage
4. **Resource Usage:** CPU, memory, network, disk
5. **Concurrency:** Active users/connections

### Analysis
1. **Baseline First:** Establish normal performance
2. **Isolate Variables:** Change one thing at a time
3. **Correlate Metrics:** Look for patterns across metrics
4. **Profile Deeply:** Drill into slow operations
5. **Document Findings:** Record all observations

---

## Reflection Points

1. **Production Parity:** How close should test environment be to production?
2. **Test Frequency:** How often should you run performance tests?
3. **Cost vs Coverage:** How do you balance test thoroughness with infrastructure cost?
4. **Realistic Load:** How do you model realistic user behavior?

---

**Next Chapter:** [Chapter 31: Quality Assurance →](chapter-31-quality-assurance.md)
