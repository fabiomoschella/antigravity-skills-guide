# Chapter 32: Test Automation Frameworks

**Last Updated:** February 5, 2026

---

## Overview

Test automation frameworks provide the structure and tools for writing, organizing, and executing automated tests at scale. Choosing the right framework and implementing it effectively is crucial for sustainable test automation.

This chapter covers essential test automation frameworks and practices for building maintainable, reliable automated test suites.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@jest-expert` | Jest framework | JavaScript/TypeScript testing |
| `@pytest-expert` | Pytest framework | Python testing |
| `@selenium-expert` | Selenium WebDriver | Browser automation |
| `@test-architecture` | Test framework design | Custom frameworks, architecture |

---

## 32.1 Jest Testing with @jest-expert

### Skill Introduction

The `@jest-expert` skill provides expertise in Jest, the popular testing framework for JavaScript and TypeScript applications. It helps you write maintainable tests and leverage Jest's powerful features.

**When to use this skill:**
- Setting up Jest projects
- Writing unit and integration tests
- Configuring Jest for different environments
- Test organization and best practices

**Key strengths:**
- Deep Jest knowledge
- Experience with testing patterns
- Understanding of Jest ecosystem

---

### Jest Testing Prompts

#### Setting Up Jest for TypeScript Project

**Context:** You're configuring Jest for a TypeScript Node.js application.

```text
@jest-expert Set up Jest for our TypeScript Node.js project:

Project details:
- Node.js 20 with TypeScript 5
- Express.js REST API
- PostgreSQL with TypeORM
- React frontend in monorepo

Requirements:
- TypeScript support without compilation
- Code coverage reporting
- Separate configs for unit and integration tests
- Watch mode for development
- CI/CD compatible output

Current issues:
- Tests are slow to start
- Path aliases not working
- Coverage report unreliable

Please provide:
1. Jest configuration (jest.config.ts)
2. TypeScript integration setup
3. Test file patterns and organization
4. Path alias configuration
5. Coverage configuration
6. Performance optimization
7. CI/CD integration (GitHub Actions)
8. Common troubleshooting
```

**Expected Output:** Complete Jest setup for TypeScript.

---

## 32.2 Pytest Framework with @pytest-expert

### Skill Introduction

The `@pytest-expert` skill provides expertise in Pytest, the most popular testing framework for Python. It helps you write clear tests and leverage pytest's powerful fixture system.

**When to use this skill:**
- Setting up Pytest projects
- Writing fixtures and test utilities
- Organizing test suites
- Integrating with other tools

**Key strengths:**
- Deep Pytest knowledge
- Experience with fixture patterns
- Understanding of plugins ecosystem

---

### Pytest Testing Prompts

#### Implementing Pytest Fixtures

**Context:** You need to set up an effective fixture system for your test suite.

```text
@pytest-expert Design pytest fixtures for our Django application:

Application:
- Django REST Framework API
- PostgreSQL database
- Redis caching
- Celery for background tasks

Testing needs:
- Database fixtures with rollback
- API client with authentication
- Redis mocking
- Celery task testing (sync mode)
- Factory patterns for test data

Current issues:
- Tests are slow due to database setup
- Fixtures not reusable across modules
- Complex authentication setup in each test
- Difficult to test async tasks

Please provide:
1. conftest.py organization
2. Database fixture with transaction rollback
3. Authentication fixture patterns
4. Factory integration (factory_boy)
5. Redis fixture (mock or real)
6. Celery testing configuration
7. Fixture scoping strategy
8. Performance optimization
```

**Expected Output:** Pytest fixture architecture.

---

## 32.3 Selenium WebDriver with @selenium-expert

### Skill Introduction

The `@selenium-expert` skill provides expertise in Selenium WebDriver for browser automation. It helps you build reliable browser automation and cross-browser testing capabilities.

**When to use this skill:**
- Cross-browser testing requirements
- Complex browser automation
- Legacy application testing
- Mobile web testing

**Key strengths:**
- Deep Selenium knowledge
- Experience with WebDriver patterns
- Understanding of browser automation

---

### Selenium Testing Prompts

#### Building Selenium Framework

**Context:** You're building a Selenium-based test automation framework.

```text
@selenium-expert Design a Selenium test automation framework:

Application:
- Multi-page web application
- Complex forms and tables
- File upload/download
- IFrames and popups
- Authentication via SSO

Requirements:
- Cross-browser (Chrome, Firefox, Edge, Safari)
- Parallel execution
- Reporting with screenshots
- Retry on transient failures
- Easy maintenance

Language: Python with pytest

Please provide:
1. Framework architecture
2. WebDriver management (local/remote)
3. Page Object Model implementation
4. Wait strategies and synchronization
5. Screenshot and video capture
6. Parallel execution setup
7. Cross-browser configuration
8. CI/CD integration with Selenium Grid
```

**Expected Output:** Selenium framework design.

---

## 32.4 Test Architecture with @test-architecture

### Skill Introduction

The `@test-architecture` skill provides expertise in designing test automation architectures. It helps you build scalable, maintainable test frameworks that grow with your needs.

**When to use this skill:**
- Designing custom test frameworks
- Scaling existing test automation
- Standardizing across teams
- Test infrastructure planning

**Key strengths:**
- Experience with framework design
- Knowledge of architecture patterns
- Understanding of scaling challenges

---

### Test Architecture Prompts

#### Designing Enterprise Test Framework

**Context:** You need to design a test automation framework for multiple teams.

```text
@test-architecture Design an enterprise test automation framework:

Organization:
- 10 product teams
- Mix of applications: web, API, mobile
- Multiple tech stacks: Node.js, Python, Java
- Each team currently has own test approach
- Need standardization without blocking teams

Goals:
- Consistent test quality across teams
- Shared utilities and patterns
- Centralized reporting
- Reduced duplication
- Self-service for teams

Requirements:
- Support multiple languages/frameworks
- Common reporting format
- Shared infrastructure (Selenium Grid, etc.)
- Reusable test utilities
- Central dashboard for leadership

Please provide:
1. Framework architecture overview
2. Abstraction layers design
3. Shared utility library approach
4. Reporting standardization
5. Test infrastructure design
6. Team onboarding process
7. Governance model
8. Success metrics
```

**Expected Output:** Enterprise test framework architecture.

---

## Best Practices Summary

### Framework Selection
1. **Team Familiarity:** Consider existing skills
2. **Ecosystem:** Evaluate plugin and tool support
3. **Performance:** Test execution speed matters
4. **Maintenance:** Long-term maintainability
5. **Community:** Active development and support

### Test Organization
1. **Consistent Structure:** Standard folder organization
2. **Naming Conventions:** Clear, descriptive names
3. **Separation of Concerns:** Logic vs test data vs utilities
4. **Configuration:** Externalize environment configs
5. **Documentation:** Document patterns and practices

### Maintainability
1. **Page Objects:** Abstract UI interactions
2. **Test Data:** Separate from test logic
3. **Utilities:** Reusable helper functions
4. **Constants:** No hardcoded values
5. **Regular Refactoring:** Keep code clean

---

## Reflection Points

1. **Framework Choice:** How do you evaluate test frameworks?
2. **Customization:** When should you build vs buy?
3. **Standardization:** How do you balance consistency with team autonomy?
4. **Technical Debt:** How do you manage test code quality?

---

**Next Chapter:** [Chapter 33: Backend Development →](chapter-33-backend-development.md)
