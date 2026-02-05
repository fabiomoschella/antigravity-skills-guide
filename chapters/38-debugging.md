# Chapter 38: Debugging

**Last Updated:** February 5, 2026

---

## Overview

Debugging is the art and science of finding and fixing defects in software. Effective debugging combines systematic approaches, deep technical knowledge, and the right tools to identify root causes efficiently.

This chapter covers essential debugging skills for diagnosing issues across different environments and systems.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@debugger-expert` | Debugging techniques | Systematic bug finding |
| `@production-debugger` | Production issues | Live system debugging |
| `@memory-debugger` | Memory issues | Leaks, crashes, profiling |
| `@performance-debugger` | Performance issues | Bottleneck identification |
| `@error-analyzer` | Error analysis | Stack traces, logs |
| `@log-analyzer` | Log analysis | Log parsing, correlation |
| `@root-cause-analyst` | RCA | Incident analysis |
| `@troubleshooter` | Troubleshooting | Issue diagnosis |
| `@crash-analyzer` | Crash analysis | Dump analysis |
| `@network-debugger` | Network issues | Connectivity, latency |

---

## 38.1 Debugging Techniques with @debugger-expert

### Skill Introduction

The `@debugger-expert` skill provides expertise in systematic debugging approaches. It helps you efficiently identify root causes of defects using proven methodologies.

**When to use this skill:**
- Diagnosing complex bugs
- Learning debugging methodologies
- Choosing debugging tools
- Teaching debugging skills

**Key strengths:**
- Systematic debugging approaches
- Experience with various bug types
- Knowledge of debugging tools

---

### Debugging Prompts

#### Systematic Bug Investigation

**Context:** You're facing a complex bug that's hard to reproduce.

```text
@debugger-expert Help debug this intermittent issue:

Problem:
- API returns 500 error randomly (about 1% of requests)
- No pattern in time of day or endpoint
- Logs show "database connection timeout"
- Database metrics show normal load
- Issue started after recent deployment

Environment:
- Node.js application on Kubernetes
- PostgreSQL on RDS
- Connection pooling with pg-pool
- 10 pods handling traffic

What I've tried:
- Increased connection pool size
- Checked database CPU/memory (normal)
- Reviewed recent code changes (nothing obvious)
- Added more logging (no clear pattern)

Please help with:
1. Systematic debugging approach
2. Hypotheses to investigate
3. Data to collect
4. Debugging tools to use
5. How to reproduce intermittent issues
6. Root cause investigation methods
7. Validation of the fix
```

**Expected Output:** Systematic debugging approach.

---

## 38.2 Production Debugging with @production-debugger

### Skill Introduction

The `@production-debugger` skill provides expertise in debugging issues in live production environments. It helps you diagnose problems safely without impacting users.

**When to use this skill:**
- Live production issues
- Incident response debugging
- Post-incident analysis
- Production observability

**Key strengths:**
- Safe production debugging
- Experience with live systems
- Knowledge of observability tools

---

### Production Debugging Prompts

#### Debugging Production Incident

**Context:** There's an active production incident you need to debug.

```text
@production-debugger Help debug this active production incident:

Incident:
- Users reporting slow page loads (30+ seconds)
- Started 30 minutes ago
- Affecting approximately 50% of users
- No recent deployments
- Error rate increasing

Systems:
- React frontend on CDN
- Node.js API on EKS
- PostgreSQL database
- Redis cache
- External payment provider

Available tools:
- Datadog APM and logs
- Kubernetes metrics
- Database monitoring (RDS metrics)
- CDN analytics

What we see:
- API response times spiked to 20+ seconds
- Database CPU normal
- No obvious errors in logs

Please help with:
1. Immediate diagnostic steps
2. How to isolate the problem
3. Safe debugging techniques for production
4. Rollback decision criteria
5. Communication during incident
6. Root cause identification
7. Post-incident actions
```

**Expected Output:** Production debugging playbook.

---

## 38.3 Memory Debugging with @memory-debugger

### Skill Introduction

The `@memory-debugger` skill provides expertise in diagnosing memory-related issues like leaks, excessive usage, and crashes. It helps you use profilers and tools to identify memory problems.

**When to use this skill:**
- Memory leak investigation
- OOM crashes
- Memory usage optimization
- Heap analysis

**Key strengths:**
- Memory profiling expertise
- Experience with memory issues
- Knowledge of memory tools

---

### Memory Debugging Prompts

#### Investigating Memory Leak

**Context:** Your application is experiencing memory leaks.

```text
@memory-debugger Help investigate a memory leak in our Node.js app:

Symptoms:
- Memory grows continuously over time
- Pod restarts every 4-6 hours due to OOM
- Memory climbs even with stable traffic
- Issue appeared after upgrade to new async library

Application:
- Express.js API server
- Uses async queues for background jobs
- WebSocket connections for real-time updates
- Caches data in memory (LRU cache)

What I've tried:
- Basic heap snapshots (shows growth)
- Checked for obvious array/object accumulation
- Reviewed recent code changes

Please help with:
1. Memory profiling approach
2. Tools to identify leaks
3. Heap snapshot analysis
4. Common leak patterns in Node.js
5. Identifying the source
6. Fixing common leak types
7. Preventing future leaks
```

**Expected Output:** Memory leak investigation guide.

---

## 38.4 Performance Debugging with @performance-debugger

### Skill Introduction

The `@performance-debugger` skill provides expertise in diagnosing performance bottlenecks. It helps you identify what's making your application slow and how to fix it.

**When to use this skill:**
- Slow response times
- High resource usage
- Performance regression investigation
- Optimization opportunities

**Key strengths:**
- Performance profiling expertise
- Experience with bottleneck patterns
- Knowledge of optimization techniques

---

### Performance Debugging Prompts

#### Investigating Slow API

**Context:** Your API endpoint has become slow and you need to find out why.

```text
@performance-debugger Help debug slow API response times:

Issue:
- /api/orders endpoint takes 5+ seconds
- Was under 200ms a month ago
- Gets slower under load
- Affects user checkout experience

Endpoint details:
- Fetches order with items
- Joins 5 tables
- Some calculations in application code
- Returns about 50KB JSON

Current metrics:
- Database query: 500ms (from APM)
- Total response: 5000ms
- Gap is unclear

What I've investigated:
- Database query plan (full table scan suspected)
- Added indexes (some improvement)
- Still slow after optimization

Please help with:
1. Performance profiling approach
2. Breaking down where time is spent
3. Database optimization checks
4. Application code profiling
5. Network/serialization issues
6. Caching strategy
7. Measuring improvement
```

**Expected Output:** Performance debugging guide.

---

## Best Practices Summary

### Debugging Process
1. **Reproduce:** Confirm the issue first
2. **Isolate:** Narrow down the scope
3. **Hypothesize:** Form theories
4. **Test:** Validate hypotheses
5. **Fix:** Apply and verify fix

### Tools
1. **Debuggers:** IDE and standalone
2. **Profilers:** CPU and memory
3. **Logging:** Structured, searchable logs
4. **Tracing:** Distributed tracing
5. **Metrics:** Observable systems

### Production
1. **Non-intrusive:** Don't impact users
2. **Safe:** Feature flags for debugging
3. **Fast:** Time is critical in incidents
4. **Documented:** Record findings
5. **Communication:** Keep stakeholders informed

---

## Reflection Points

1. **Intuition vs Process:** When to use systematic vs intuitive debugging?
2. **Observability:** How do you build debuggable systems?
3. **Learning:** How do you learn from each debugging session?
4. **Prevention:** How do you prevent bugs from occurring?

---

**Next Chapter:** [Chapter 39: Refactoring →](chapter-39-refactoring.md)
