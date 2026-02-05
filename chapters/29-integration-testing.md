# Chapter 29: Integration & E2E Testing

**Last Updated:** February 5, 2026

---

## Overview

Integration testing verifies that components work together correctly, while end-to-end (E2E) testing validates complete user workflows. Together, they ensure your application functions properly as a complete system.

This chapter covers skills for designing and implementing effective integration and E2E testing strategies.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@integration-test-expert` | Integration testing | API testing, component integration |
| `@e2e-test-expert` | End-to-end testing | User workflow validation |
| `@playwright-expert` | Browser automation | UI testing, cross-browser |
| `@cypress-expert` | Cypress testing | Fast E2E, developer experience |

---

## 29.1 Integration Testing with @integration-test-expert

### Skill Introduction

The `@integration-test-expert` skill provides expertise in testing component interactions. It helps you design integration tests that catch issues unit tests miss while remaining faster than full E2E tests.

**When to use this skill:**
- Testing API endpoints
- Testing database interactions
- Testing service composition
- Testing external integrations

**Key strengths:**
- Experience with integration test design
- Knowledge of test data management
- Understanding of test isolation

---

### Integration Testing Prompts

#### Designing API Integration Tests

**Context:** You need to create integration tests for your REST API.

```text
@integration-test-expert Design integration tests for our REST API:

API endpoints to test:
POST /api/orders - Create order
GET /api/orders/:id - Get order
PUT /api/orders/:id - Update order
DELETE /api/orders/:id - Cancel order
GET /api/orders - List orders with pagination/filtering

Dependencies:
- PostgreSQL database
- Redis cache
- Stripe payment integration
- External inventory service

Testing approach needed:
- Database setup/teardown
- External service handling
- Authentication testing
- Error response validation

Please provide:
1. Integration test architecture
2. Test setup and teardown strategy
3. Database testing approach (real vs test containers)
4. External service mocking strategy
5. Authentication in tests
6. Example test cases for each endpoint
7. CI/CD considerations
```

**Expected Output:** Integration testing strategy with examples.

---

#### Testing with Containers

**Context:** You want to use containers for realistic integration testing.

```text
@integration-test-expert Implement container-based integration testing:

Services to test against:
- PostgreSQL (primary database)
- Redis (caching)
- Elasticsearch (search)
- RabbitMQ (messaging)

Requirements:
- Realistic database behavior
- Fast test startup
- Isolated test runs
- Works in CI/CD (GitHub Actions)

Current issues:
- Tests use in-memory mocks that miss real bugs
- CI environment different from local
- Flaky tests due to shared test database

Please provide:
1. Testcontainers setup for each service
2. Container management in test lifecycle
3. Parallel test execution approach
4. CI/CD integration with containers
5. Performance optimization
6. Data seeding strategy
7. Debugging containerized tests
```

**Expected Output:** Container-based testing implementation.

---

## 29.2 End-to-End Testing with @e2e-test-expert

### Skill Introduction

The `@e2e-test-expert` skill provides expertise in designing end-to-end tests that validate complete user journeys. It helps you balance coverage with test maintenance and execution time.

**When to use this skill:**
- Designing E2E test strategy
- Identifying critical user journeys
- Reducing E2E test flakiness
- Optimizing E2E test execution

**Key strengths:**
- Experience with E2E test design
- Knowledge of flakiness reduction
- Understanding of test prioritization

---

### E2E Testing Prompts

#### Designing E2E Test Strategy

**Context:** You need an E2E testing strategy for your web application.

```text
@e2e-test-expert Design E2E testing strategy for our SaaS application:

Application:
- React SPA with multiple pages
- User registration and authentication
- Multi-step checkout flow
- Admin dashboard
- Real-time notifications

User journeys to cover:
- New user registration to first purchase
- Returning user login and repeat purchase
- Admin managing orders and users
- Password reset flow
- Subscription management

Challenges:
- Tests currently take 45 minutes
- 30% of tests are flaky
- Hard to run locally
- Coverage gaps in critical flows

Please provide:
1. E2E test strategy document
2. Critical journey prioritization
3. Flakiness reduction approach
4. Test execution optimization
5. Local development workflow
6. CI/CD integration
7. Maintenance strategy
```

**Expected Output:** E2E testing strategy with prioritized journeys.

---

## 29.3 Playwright Testing with @playwright-expert

### Skill Introduction

The `@playwright-expert` skill provides expertise in Playwright for cross-browser testing. It helps you write reliable, fast browser tests with modern automation capabilities.

**When to use this skill:**
- Cross-browser testing needs
- Modern web app testing
- API and browser test integration
- Component testing with Playwright

**Key strengths:**
- Deep Playwright knowledge
- Experience with modern testing patterns
- Understanding of browser automation

---

### Playwright Testing Prompts

#### Implementing Playwright Tests

**Context:** You want to implement Playwright for your E2E testing.

```text
@playwright-expert Set up Playwright testing for our application:

Application:
- Next.js web application
- OAuth login (Google, Microsoft)
- File upload functionality
- Real-time updates (WebSocket)
- Responsive design (desktop, tablet, mobile)

Requirements:
- Cross-browser testing (Chrome, Firefox, Safari)
- Mobile viewport testing
- Visual regression testing
- Parallel execution
- CI/CD integration (GitHub Actions)

Please provide:
1. Playwright project setup
2. Configuration for multiple browsers
3. Authentication handling (OAuth)
4. Page Object Model implementation
5. File upload testing approach
6. Visual regression setup
7. Parallel execution configuration
8. GitHub Actions workflow
```

**Expected Output:** Playwright implementation guide.

---

#### Handling Flaky Tests

**Context:** Your Playwright tests are failing intermittently.

```text
@playwright-expert Help fix flaky Playwright tests:

Symptoms:
- Tests pass locally but fail in CI
- Random timeout failures
- Element not visible errors
- Race conditions with data
- Authentication session issues

Test environment:
- Running in GitHub Actions
- Parallel execution enabled
- Tests against staging environment
- Average test time: 30 seconds per test

Please provide:
1. Flakiness diagnosis approach
2. Common causes and fixes
3. Waiting and retry strategies
4. Test isolation improvements
5. CI-specific configurations
6. Logging and debugging tips
7. Monitoring flakiness over time
```

**Expected Output:** Flakiness resolution guide.

---

## 29.4 Cypress Testing with @cypress-expert

### Skill Introduction

The `@cypress-expert` skill provides expertise in Cypress for fast, reliable E2E testing. It helps you leverage Cypress's developer experience and unique capabilities.

**When to use this skill:**
- Fast feedback E2E testing
- Developer-centric test authoring
- Time travel debugging needs
- Component testing with Cypress

**Key strengths:**
- Deep Cypress knowledge
- Experience with Cypress patterns
- Understanding of Cypress limitations

---

### Cypress Testing Prompts

#### Setting Up Cypress

**Context:** You're adopting Cypress for testing your React application.

```text
@cypress-expert Set up Cypress for our React application:

Application:
- Create React App with TypeScript
- REST API backend
- JWT authentication
- Interactive data tables
- Form validation

Testing needs:
- E2E tests for critical flows
- Component tests for complex UI
- API testing for backend validation
- CI/CD integration

Please provide:
1. Cypress project configuration
2. TypeScript integration
3. Custom commands for authentication
4. Fixtures and data management
5. Component testing setup
6. API stubbing vs real backend
7. CI/CD setup (GitHub Actions)
8. Best practices for our use case
```

**Expected Output:** Cypress setup guide.

---

## Best Practices Summary

### Integration Tests
1. **Real Dependencies:** Use containers when possible
2. **Isolated Data:** Each test manages its own data
3. **Fast Feedback:** Keep tests under 30 seconds
4. **Focused Scope:** Test integrations, not everything
5. **Meaningful Assertions:** Verify actual integration behavior

### E2E Tests
1. **Critical Paths:** Focus on key user journeys
2. **Resilient Selectors:** Use data attributes
3. **Avoid Coupling:** Tests independent of each other
4. **Realistic Data:** Use production-like test data
5. **Readable Tests:** Easy to understand and maintain

### Flakiness Prevention
1. **Explicit Waits:** Wait for specific conditions
2. **Retry Logic:** Handle transient failures
3. **Isolation:** No shared state between tests
4. **Stable Environment:** Consistent test environment
5. **Monitoring:** Track flakiness metrics

---

## Reflection Points

1. **Test Pyramid:** What's the right balance of E2E to unit tests?
2. **Maintenance Cost:** How do you keep E2E tests maintainable?
3. **Speed vs Coverage:** How do you balance E2E coverage with execution time?
4. **Real vs Mock:** When should E2E tests use real backends?

---

**Next Chapter:** [Chapter 30: Performance & Load Testing →](chapter-30-performance-testing.md)
