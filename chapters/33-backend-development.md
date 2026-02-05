# Chapter 33: Backend Development

**Last Updated:** February 5, 2026

---

## Overview

Backend development is the foundation of modern applications, handling business logic, data processing, and API services. Building robust, scalable, and maintainable backend systems requires expertise across languages, frameworks, and architectural patterns.

This chapter covers essential backend development skills for building production-ready server-side applications.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@nodejs-expert` | Node.js development | APIs, real-time apps, microservices |
| `@python-expert` | Python development | APIs, data processing, automation |
| `@go-expert` | Go development | High-performance services |
| `@api-designer` | API design | RESTful and GraphQL API design |

---

## 33.1 Node.js Development with @nodejs-expert

### Skill Introduction

The `@nodejs-expert` skill provides expertise in Node.js application development. It helps you build scalable, efficient backend services using JavaScript/TypeScript.

**When to use this skill:**
- Building REST and GraphQL APIs
- Real-time applications with WebSockets
- Microservices architecture
- Performance optimization

**Key strengths:**
- Deep Node.js and V8 knowledge
- Experience with Express, Fastify, NestJS
- Understanding of async patterns

---

### Node.js Development Prompts

#### Building a Production API

**Context:** You're building a production-grade REST API with Node.js.

```text
@nodejs-expert Design and implement a production Node.js REST API:

Requirements:
- TypeScript with strict mode
- RESTful design with proper HTTP semantics
- JWT authentication with refresh tokens
- PostgreSQL with connection pooling
- Redis for caching and sessions
- Structured logging
- Health checks and metrics

Features to implement:
- User registration and authentication
- Resource CRUD operations with pagination
- File uploads to S3
- Webhook notifications

Quality requirements:
- 90%+ test coverage
- OpenAPI documentation
- Rate limiting
- Graceful shutdown

Please provide:
1. Project structure and architecture
2. Framework selection (Express/Fastify/NestJS)
3. Database access patterns
4. Authentication implementation
5. Error handling strategy
6. Logging and monitoring
7. Testing approach
8. Docker configuration
```

**Expected Output:** Complete Node.js API implementation guide.

---

## 33.2 Python Development with @python-expert

### Skill Introduction

The `@python-expert` skill provides expertise in Python backend development. It helps you build APIs, data processing pipelines, and automation scripts with Python's extensive ecosystem.

**When to use this skill:**
- Building REST APIs with FastAPI/Django
- Data processing and ETL
- Machine learning integration
- Automation and scripting

**Key strengths:**
- Deep Python knowledge
- Experience with major frameworks
- Understanding of Python performance

---

### Python Development Prompts

#### FastAPI Application Development

**Context:** You're building a high-performance API with FastAPI.

```text
@python-expert Build a FastAPI application with best practices:

Requirements:
- Python 3.11+ with type hints
- Async handlers for I/O operations
- SQLAlchemy 2.0 with async support
- Pydantic v2 for validation
- JWT authentication
- Background tasks with Celery
- Redis caching

Features:
- User management with roles
- Resource API with filtering/pagination
- File processing with background tasks
- WebSocket for real-time updates

Please provide:
1. Project structure
2. FastAPI configuration
3. Dependency injection patterns
4. Database models and migrations
5. Authentication and authorization
6. Background task setup
7. Testing with pytest
8. Docker and deployment
```

**Expected Output:** FastAPI application architecture.

---

## 33.3 Go Development with @go-expert

### Skill Introduction

The `@go-expert` skill provides expertise in Go application development. It helps you build high-performance, concurrent services with Go's simplicity and efficiency.

**When to use this skill:**
- High-performance microservices
- CLI tools and utilities
- DevOps tooling
- Network services

**Key strengths:**
- Deep Go knowledge
- Experience with concurrency patterns
- Understanding of Go ecosystem

---

### Go Development Prompts

#### Building Go Microservice

**Context:** You're building a high-performance microservice in Go.

```text
@go-expert Design a production Go microservice:

Requirements:
- Clean architecture with dependency injection
- HTTP/gRPC APIs
- PostgreSQL with connection pooling
- Structured logging (zerolog or zap)
- Graceful shutdown
- Configuration management
- Health checks and metrics

Service functionality:
- Order processing service
- Receive orders via HTTP/gRPC
- Validate and enrich order data
- Publish to message queue
- Store in database

Quality requirements:
- Comprehensive testing
- OpenAPI spec for REST
- Protobuf definitions for gRPC
- Docker multi-stage build

Please provide:
1. Project structure
2. Dependency organization
3. API implementation patterns
4. Database access with sqlc or GORM
5. Error handling patterns
6. Testing strategy
7. Observability setup
8. Deployment configuration
```

**Expected Output:** Go microservice implementation guide.

---

## 33.4 API Design with @api-designer

### Skill Introduction

The `@api-designer` skill provides expertise in designing APIs that are intuitive, consistent, and developer-friendly. It helps you create APIs that consumers love to use.

**When to use this skill:**
- Designing new APIs
- API versioning strategy
- REST vs GraphQL decisions
- API documentation

**Key strengths:**
- Deep API design knowledge
- Experience with REST and GraphQL
- Understanding of developer experience

---

### API Design Prompts

#### Designing RESTful API

**Context:** You need to design a RESTful API for a new product.

```text
@api-designer Design a RESTful API for our e-commerce platform:

Resources to design:
- Products (catalog)
- Users (customers, admins)
- Orders (checkout, history)
- Carts (shopping cart)
- Reviews (product reviews)

Requirements:
- Consistent naming and patterns
- Proper HTTP method usage
- Error response format
- Pagination and filtering
- Sorting and field selection
- Versioning strategy
- Rate limiting headers

Consumers:
- Web application (SPA)
- Mobile apps (iOS, Android)
- Third-party integrations

Please provide:
1. API design principles
2. URL structure and naming
3. Resource schemas
4. Request/response examples
5. Error handling design
6. Pagination design
7. Versioning approach
8. OpenAPI specification outline
```

**Expected Output:** Comprehensive REST API design.

---

## Best Practices Summary

### Code Quality
1. **Type Safety:** Use TypeScript/type hints
2. **Linting:** Consistent code style
3. **Testing:** Comprehensive test coverage
4. **Documentation:** API docs and comments
5. **Security:** Input validation, parameterized queries

### Performance
1. **Connection Pooling:** Reuse database connections
2. **Caching:** Cache frequently accessed data
3. **Async I/O:** Non-blocking operations
4. **Pagination:** Limit data returned
5. **Profiling:** Identify bottlenecks

### Operations
1. **Logging:** Structured, actionable logs
2. **Metrics:** Key performance indicators
3. **Health Checks:** Readiness and liveness
4. **Graceful Shutdown:** Clean termination
5. **Configuration:** Environment-based

---

## Reflection Points

1. **Language Choice:** How do you choose between Node.js, Python, and Go?
2. **Framework vs Custom:** When to use frameworks vs building custom?
3. **API Evolution:** How do you handle breaking changes?
4. **Performance vs Simplicity:** How do you balance these priorities?

---

**Next Chapter:** [Chapter 34: Frontend Development →](chapter-34-frontend-development.md)
