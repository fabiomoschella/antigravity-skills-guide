# Chapter 28: Testing Fundamentals

**Last Updated:** February 5, 2026

---

## Overview

Testing is the foundation of software quality assurance. From unit tests to integration tests, a comprehensive testing strategy ensures code correctness, catches regressions, and enables confident refactoring.

This chapter covers essential testing skills to help you design effective test strategies, write maintainable tests, and achieve appropriate coverage.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@testing-expert` | Testing strategy | Test design, coverage, best practices |
| `@unit-test-expert` | Unit testing | Isolated component testing |
| `@tdd-expert` | Test-Driven Development | TDD workflow, red-green-refactor |
| `@mocking-expert` | Test doubles | Mocks, stubs, fakes, spies |

---

## 28.1 Testing Strategy with @testing-expert

### Skill Introduction

The `@testing-expert` skill provides expertise in designing comprehensive testing strategies. It helps you balance test coverage, maintainability, and execution speed for effective quality assurance.

**When to use this skill:**
- Designing testing strategies for new projects
- Improving existing test suites
- Balancing test pyramid levels
- Defining coverage requirements
- Creating testing standards

**Key strengths:**
- Deep knowledge of testing methodologies
- Experience with test architecture
- Understanding of cost-benefit trade-offs

---

### Testing Strategy Prompts

#### Designing a Testing Strategy

**Context:** You're building a new application and need a comprehensive testing approach.

```text
@testing-expert Design a testing strategy for our new e-commerce platform:

Application details:
- React frontend with TypeScript
- Node.js/Express backend
- PostgreSQL database
- External integrations: Stripe, Twilio, Shippo

Team:
- 8 developers
- No dedicated QA
- CI/CD with GitHub Actions

Goals:
- High confidence in releases
- Fast feedback for developers
- Maintainable test suite
- Enable continuous deployment

Questions to address:
- Test pyramid distribution
- Coverage targets per layer
- Testing strategy for integrations
- When to use each test type
- Testing in CI/CD

Please provide:
1. Testing strategy document
2. Test pyramid with percentage targets
3. Testing standards and conventions
4. Tool recommendations
5. CI/CD integration approach
6. Coverage measurement strategy
7. Team training needs
```

**Expected Output:** Comprehensive testing strategy document.

---

#### Improving Test Coverage

**Context:** Your codebase has low test coverage and you need to improve it strategically.

```text
@testing-expert Help improve test coverage for our legacy application:

Current state:
- 200K lines of code (Node.js)
- 15% overall test coverage
- Tests are flaky and slow
- Coverage concentrated in less critical areas
- Many critical paths untested

Goals:
- Increase coverage to 70% in 6 months
- Focus on high-value areas first
- Reduce test flakiness
- Improve test speed

Constraints:
- Limited time for testing work
- Can't stop feature development
- Team unfamiliar with testing

Please provide:
1. Coverage improvement strategy
2. Prioritization framework (what to test first)
3. Identifying critical paths approach
4. Flaky test fixing strategy
5. Test speed optimization
6. Metrics to track progress
7. Team onboarding plan
```

**Expected Output:** Test coverage improvement plan.

---

## 28.2 Unit Testing with @unit-test-expert

### Skill Introduction

The `@unit-test-expert` skill provides expertise in writing effective unit tests. It helps you isolate components, design testable code, and write clear, maintainable tests.

**When to use this skill:**
- Writing unit tests for new code
- Improving existing unit tests
- Making code more testable
- Choosing assertion patterns
- Organizing test files

**Key strengths:**
- Expert in unit testing patterns
- Experience with major testing frameworks
- Knowledge of testable design

---

### Unit Testing Prompts

#### Writing Effective Unit Tests

**Context:** You want to add comprehensive unit tests to a service class.

```text
@unit-test-expert Write unit tests for this order processing service:

```typescript
export class OrderService {
  constructor(
    private inventoryService: InventoryService,
    private paymentService: PaymentService,
    private notificationService: NotificationService,
    private orderRepository: OrderRepository
  ) {}

  async processOrder(order: CreateOrderDTO): Promise<Order> {
    // Check inventory
    const available = await this.inventoryService.checkAvailability(order.items);
    if (!available) {
      throw new InsufficientInventoryError(order.items);
    }

    // Process payment
    const payment = await this.paymentService.charge(
      order.customerId,
      order.total
    );

    // Create order
    const savedOrder = await this.orderRepository.save({
      ...order,
      paymentId: payment.id,
      status: 'CONFIRMED'
    });

    // Send notification
    await this.notificationService.sendOrderConfirmation(savedOrder);

    return savedOrder;
  }
}
```

Please provide:
1. Complete test file with Jest
2. Tests for success scenarios
3. Tests for failure scenarios (inventory, payment, notification)
4. Edge cases to test
5. Mock setup and teardown
6. Test organization approach
7. Coverage areas explained
```

**Expected Output:** Complete unit test file with comprehensive coverage.

---

## 28.3 Test-Driven Development with @tdd-expert

### Skill Introduction

The `@tdd-expert` skill provides guidance on practicing Test-Driven Development effectively. It helps you adopt the red-green-refactor cycle and design tests before implementation.

**When to use this skill:**
- Learning TDD methodology
- Designing tests before code
- Refactoring with confidence
- Improving code design through TDD

**Key strengths:**
- Deep TDD experience
- Knowledge of test design patterns
- Understanding of TDD benefits and challenges

---

### TDD Implementation Prompts

#### TDD Workflow for New Feature

**Context:** You're implementing a new feature using TDD.

```text
@tdd-expert Guide me through TDD for implementing a shopping cart:

Requirements:
- Add items to cart
- Remove items from cart
- Update item quantities
- Calculate subtotal
- Apply discount codes
- Calculate total with tax

I want to:
- Follow red-green-refactor strictly
- Design the API through tests
- Build incrementally

Please provide:
1. TDD approach for this feature
2. First test to write (simplest case)
3. Progression of tests building complexity
4. Refactoring opportunities to watch for
5. Design decisions driven by tests
6. When to write integration tests
```

**Expected Output:** TDD walkthrough with test progression.

---

## 28.4 Mocking and Test Doubles with @mocking-expert

### Skill Introduction

The `@mocking-expert` skill provides expertise in using test doubles (mocks, stubs, fakes, spies) effectively. It helps you isolate units under test and verify interactions.

**When to use this skill:**
- Mocking external dependencies
- Choosing between mock types
- Avoiding over-mocking
- Testing async and event-based code

**Key strengths:**
- Expert in mocking patterns
- Knowledge of major mocking libraries
- Understanding of when to mock vs not

---

### Mocking Prompts

#### Effective Mocking Strategies

**Context:** You need to test code with complex external dependencies.

```text
@mocking-expert Help design mocking strategy for our service tests:

Dependencies to handle:
- Database (PostgreSQL via TypeORM)
- External API (Stripe)
- Message queue (RabbitMQ)
- Cache (Redis)
- Email service (SendGrid)

Testing challenges:
- Database calls are slow
- External APIs are unreliable
- Need to verify message publishing
- Cache behavior affects results

Questions:
- When to use real vs mock database?
- How to mock Stripe safely?
- Testing async message handlers?
- Avoiding over-mocking pitfalls?

Please provide:
1. Mocking strategy per dependency type
2. When to use mocks vs fakes vs stubs
3. Test double implementation examples
4. Anti-patterns to avoid
5. Testing async/event-driven code
6. Balance between isolation and realism
```

**Expected Output:** Mocking strategy guide with examples.

---

## Best Practices Summary

### Test Design
1. **Arrange-Act-Assert:** Clear test structure
2. **One Assertion Per Test:** Focused tests
3. **Descriptive Names:** Tests as documentation
4. **Independence:** Tests don't depend on each other
5. **Determinism:** Same result every time

### Coverage
1. **Branch Coverage:** Test all branches
2. **Edge Cases:** Test boundaries
3. **Error Paths:** Test failure scenarios
4. **Priority:** Focus on critical paths
5. **Not Just Lines:** Meaningful coverage

### Maintainability
1. **DRY in Tests:** Appropriate abstraction
2. **Test Helpers:** Reusable setup code
3. **Clear Failures:** Easy to diagnose
4. **Update With Code:** Keep tests current
5. **Delete Bad Tests:** Remove flaky/useless tests

---

## Reflection Points

1. **Coverage vs Quality:** Is 100% coverage the goal?
2. **Test Speed:** How do you balance thoroughness with speed?
3. **Mocking Boundaries:** When is mocking harmful?
4. **Test Maintenance:** How do you keep tests maintainable?

---

**Next Chapter:** [Chapter 29: Integration & E2E Testing →](chapter-29-integration-testing.md)
