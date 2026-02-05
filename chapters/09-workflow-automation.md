# Chapter 9: Workflow & Automation Architecture

**Last Updated:** February 5, 2026

---

## Overview

Workflow and automation architecture enables organizations to streamline complex processes, reduce manual intervention, and ensure consistent execution. This chapter covers skills for designing and implementing workflow systems.

### Skills Covered in This Chapter

| Skill | Source | Purpose |
|-------|--------|---------|
| `@workflow-architect` | Unknown | Workflow system design |
| `@state-machine-patterns` | Unknown | State machine implementation |
| `@process-automation` | Unknown | Business process automation |
| `@orchestration-patterns` | Unknown | Service orchestration |
| `@integration-architect` | Unknown | System integration design |
| `@n8n-mcp-tools-expert` | antigravity | n8n MCP integration |
| `@n8n-node-configuration` | antigravity | n8n node setup |
| `@n8n-code-python` | antigravity | n8n Python code |
| `@zapier-make-patterns` | antigravity | Zapier/Make automation |
| `@trigger-dev` | antigravity | Trigger.dev workflows |
| `@browser-automation` | antigravity | Browser automation |
| `@playwright-skill` | antigravity | Playwright testing |
| `@firecrawl-scraper` | antigravity | Web scraping |
| `@discord-bot-builder` | antigravity | Discord bots |
| `@telegram-bot-builder` | antigravity | Telegram bots |
| `@telegram-mini-app` | antigravity | Telegram mini apps |
| `@slack-bot-builder` | antigravity | Slack bots |
| `@browser-extension-builder` | antigravity | Browser extensions |
| `@automate-whatsapp` | antigravity | WhatsApp automation |
| `@observe-whatsapp` | antigravity | WhatsApp monitoring |
| `@twilio-communications` | antigravity | Twilio integration |

---

## 9.1 Workflow Architecture

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: workflow, automation, architecture

### Purpose

The `workflow-architect` skill provides guidance on designing robust workflow systems for complex business processes.

### Workflow Types

| Type | Description | Use Case |
|------|-------------|----------|
| **Sequential** | Step-by-step execution | Document approval |
| **Parallel** | Concurrent execution | Data processing |
| **Conditional** | Branch-based logic | Order fulfillment |
| **Event-driven** | Triggered by events | Notification system |
| **Human-in-loop** | Requires human input | Review processes |

### 40 Copy-Paste Prompts

#### Workflow Design

```
1. "Use @workflow-architect to design an order fulfillment workflow"

2. "Apply @workflow-architect to create a document approval process"

3. "Use @workflow-architect to design a customer onboarding workflow"

4. "Apply @workflow-architect to create an incident response workflow"

5. "Use @workflow-architect to design a CI/CD pipeline workflow"

6. "Apply @workflow-architect to create a hiring process workflow"

7. "Use @workflow-architect to design a refund processing workflow"

8. "Apply @workflow-architect to create a subscription lifecycle workflow"

9. "Use @workflow-architect to design a data processing pipeline"

10. "Apply @workflow-architect to create a compliance review workflow"
```

#### Error Handling

```
11. "Use @workflow-architect to implement retry strategies"

12. "Apply @workflow-architect to design compensation patterns"

13. "Use @workflow-architect to implement dead letter handling"

14. "Apply @workflow-architect to create fallback workflows"

15. "Use @workflow-architect to design timeout handling"

16. "Apply @workflow-architect to implement circuit breakers"

17. "Use @workflow-architect to create error notification workflows"

18. "Apply @workflow-architect to design rollback procedures"

19. "Use @workflow-architect to implement idempotent steps"

20. "Apply @workflow-architect to create audit logging"
```

#### Scaling Workflows

```
21. "Use @workflow-architect to design horizontal scaling"

22. "Apply @workflow-architect to implement workflow partitioning"

23. "Use @workflow-architect to create priority queues"

24. "Apply @workflow-architect to design rate limiting"

25. "Use @workflow-architect to implement load balancing"

26. "Apply @workflow-architect to create workflow sharding"

27. "Use @workflow-architect to design batch processing"

28. "Apply @workflow-architect to implement parallel execution"

29. "Use @workflow-architect to create workflow caching"

30. "Apply @workflow-architect to design workflow monitoring"
```

#### Advanced Patterns

```
31. "Use @workflow-architect to implement saga pattern"

32. "Apply @workflow-architect to create choreography vs orchestration"

33. "Use @workflow-architect to design long-running workflows"

34. "Apply @workflow-architect to implement workflow versioning"

35. "Use @workflow-architect to create dynamic workflows"

36. "Apply @workflow-architect to design sub-workflows"

37. "Use @workflow-architect to implement workflow templates"

38. "Apply @workflow-architect to create conditional branching"

39. "Use @workflow-architect to design human tasks"

40. "Apply @workflow-architect to implement approval chains"
```

---

## 9.2 State Machine Patterns

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: state-machine, patterns, logic

### Purpose

The `state-machine-patterns` skill provides guidance on implementing finite state machines for complex state management.

### State Machine Structure

```typescript
interface StateMachine {
  id: string;
  initial: string;
  states: Record<string, StateConfig>;
  context: object;
}

interface StateConfig {
  on: Record<string, string | Transition>;
  entry?: Action[];
  exit?: Action[];
  type?: 'final' | 'parallel' | 'compound';
}
```

### 30 Copy-Paste Prompts

#### State Design

```
41. "Use @state-machine-patterns to design order state machine"

42. "Apply @state-machine-patterns to create user authentication states"

43. "Use @state-machine-patterns to design payment processing states"

44. "Apply @state-machine-patterns to create document lifecycle states"

45. "Use @state-machine-patterns to design ticket workflow states"

46. "Apply @state-machine-patterns to create subscription states"

47. "Use @state-machine-patterns to design booking states"

48. "Apply @state-machine-patterns to create approval states"

49. "Use @state-machine-patterns to design game states"

50. "Apply @state-machine-patterns to create wizard step states"
```

#### XState Implementation

```
51. "Use @state-machine-patterns to implement with XState"

52. "Apply @state-machine-patterns to create hierarchical states"

53. "Use @state-machine-patterns to implement parallel states"

54. "Apply @state-machine-patterns to create guards and conditions"

55. "Use @state-machine-patterns to implement actions and side effects"

56. "Apply @state-machine-patterns to create context updates"

57. "Use @state-machine-patterns to implement delayed transitions"

58. "Apply @state-machine-patterns to create event composition"

59. "Use @state-machine-patterns to implement history states"

60. "Apply @state-machine-patterns to create spawned actors"
```

#### Testing

```
61. "Use @state-machine-patterns to test state transitions"

62. "Apply @state-machine-patterns to create transition coverage"

63. "Use @state-machine-patterns to test guard conditions"

64. "Apply @state-machine-patterns to validate state invariants"

65. "Use @state-machine-patterns to implement property-based testing"
```

---

## 9.3 Orchestration Patterns

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: orchestration, microservices, patterns

### Purpose

The `orchestration-patterns` skill provides guidance on coordinating distributed services and workflows.

### Orchestration vs Choreography

| Aspect | Orchestration | Choreography |
|--------|---------------|--------------|
| **Control** | Centralized | Distributed |
| **Coupling** | Higher | Lower |
| **Visibility** | Clear | Complex |
| **Debugging** | Easier | Harder |
| **Scalability** | Bottleneck risk | Better |

### 20 Copy-Paste Prompts

```
66. "Use @orchestration-patterns to design service orchestration"

67. "Apply @orchestration-patterns to implement distributed saga"

68. "Use @orchestration-patterns to create service mesh patterns"

69. "Apply @orchestration-patterns to design API gateway orchestration"

70. "Use @orchestration-patterns to implement workflow orchestration"

71. "Apply @orchestration-patterns to create batch orchestration"

72. "Use @orchestration-patterns to design event choreography"

73. "Apply @orchestration-patterns to implement compensation logic"

74. "Use @orchestration-patterns to create timeout handling"

75. "Apply @orchestration-patterns to design retry patterns"

76. "Use @orchestration-patterns to implement circuit breakers"

77. "Apply @orchestration-patterns to create bulkhead patterns"

78. "Use @orchestration-patterns to design fallback strategies"

79. "Apply @orchestration-patterns to implement health checking"

80. "Use @orchestration-patterns to create service discovery"
```

---

## 9.4 Integration Architecture

> **Source**: Unknown  
> **Risk Level**: Unknown  
> **Tags**: integration, api, patterns

### Purpose

The `integration-architect` skill provides guidance on designing robust system integrations.

### Integration Patterns

| Pattern | Description | Use Case |
|---------|-------------|----------|
| **Point-to-Point** | Direct connection | Simple integrations |
| **Hub-and-Spoke** | Central broker | Multiple systems |
| **ESB** | Enterprise bus | Complex routing |
| **Event Mesh** | Distributed events | Real-time systems |
| **API Gateway** | Unified interface | Microservices |

### 20 Copy-Paste Prompts

```
81. "Use @integration-architect to design API integration strategy"

82. "Apply @integration-architect to implement webhook handlers"

83. "Use @integration-architect to create message transformation"

84. "Apply @integration-architect to design data synchronization"

85. "Use @integration-architect to implement ETL pipelines"

86. "Apply @integration-architect to create real-time integration"

87. "Use @integration-architect to design batch integration"

88. "Apply @integration-architect to implement event-driven integration"

89. "Use @integration-architect to create API versioning strategy"

90. "Apply @integration-architect to design error handling"

91. "Use @integration-architect to implement retry logic"

92. "Apply @integration-architect to create monitoring and alerting"

93. "Use @integration-architect to design security for integrations"

94. "Apply @integration-architect to implement rate limiting"

95. "Use @integration-architect to create integration testing"

96. "Apply @integration-architect to design contract testing"

97. "Use @integration-architect to implement mock servers"

98. "Apply @integration-architect to create integration documentation"

99. "Use @integration-architect to design multi-cloud integration"

100. "Apply @integration-architect to implement legacy system integration"
```

---

## Workflow Template (Temporal.io)

```typescript
// Order fulfillment workflow
import { proxyActivities, sleep, condition } from '@temporalio/workflow';
import type * as activities from './activities';

const { validateOrder, processPayment, shipOrder, notifyCustomer } =
  proxyActivities<typeof activities>({
    startToCloseTimeout: '1 minute',
    retry: {
      initialInterval: '1s',
      backoffCoefficient: 2,
      maximumAttempts: 3,
    },
  });

export async function orderFulfillmentWorkflow(order: Order): Promise<OrderResult> {
  // Step 1: Validate
  const validation = await validateOrder(order);
  if (!validation.valid) {
    return { status: 'rejected', reason: validation.reason };
  }

  // Step 2: Payment
  try {
    await processPayment(order.paymentDetails);
  } catch (error) {
    await notifyCustomer(order.customerId, 'payment_failed');
    return { status: 'payment_failed' };
  }

  // Step 3: Fulfillment
  const shipmentId = await shipOrder(order);

  // Step 4: Notify
  await notifyCustomer(order.customerId, 'shipped', { shipmentId });

  return { status: 'completed', shipmentId };
}
```

---

## State Machine Example (XState)

```typescript
import { createMachine, assign } from 'xstate';

const orderMachine = createMachine({
  id: 'order',
  initial: 'pending',
  context: {
    orderId: null,
    attempts: 0,
  },
  states: {
    pending: {
      on: {
        SUBMIT: 'validating',
      },
    },
    validating: {
      invoke: {
        src: 'validateOrder',
        onDone: 'processing',
        onError: 'invalid',
      },
    },
    invalid: {
      on: {
        RETRY: {
          target: 'validating',
          actions: assign({ attempts: (ctx) => ctx.attempts + 1 }),
          guard: 'canRetry',
        },
      },
    },
    processing: {
      invoke: {
        src: 'processPayment',
        onDone: 'confirmed',
        onError: 'paymentFailed',
      },
    },
    paymentFailed: {
      on: {
        RETRY: 'processing',
        CANCEL: 'cancelled',
      },
    },
    confirmed: {
      on: {
        SHIP: 'shipped',
      },
    },
    shipped: {
      on: {
        DELIVER: 'delivered',
      },
    },
    delivered: {
      type: 'final',
    },
    cancelled: {
      type: 'final',
    },
  },
});
```

---

## Best Practices

### 1. Workflow Idempotency

```typescript
// Always check if step was already completed
async function processStep(workflowId: string, stepId: string) {
  const existing = await db.getStepResult(workflowId, stepId);
  if (existing) {
    return existing.result;
  }
  
  const result = await executeStep();
  await db.saveStepResult(workflowId, stepId, result);
  return result;
}
```

### 2. Visibility and Logging

Log workflow state transitions for debugging:
- Workflow started
- Step completed
- Error occurred
- Compensation executed

### 3. Timeout Handling

Always set timeouts:
- Step timeouts
- Workflow timeouts
- Overall SLA timeouts

### 4. Testing

Test workflows in isolation:
- Unit test individual steps
- Integration test full workflows
- Simulate failure scenarios

---

## Reflection Points for Chapter 9

1. **What workflows in your organization could be automated?**
   - Manual handoffs?
   - Approval chains?
   - Data processing?

2. **How do you handle workflow failures today?**
   - Manual intervention?
   - Automatic retry?
   - Compensation logic?

3. **What visibility do you have into workflow execution?**
   - Status tracking?
   - Error monitoring?
   - Performance metrics?

4. **How do you version and evolve workflows?**
   - Backward compatibility?
   - Migration strategies?
   - Testing approaches?

---

## Summary

This chapter covered workflow and automation architecture:

- **@workflow-architect**: Workflow system design
- **@state-machine-patterns**: State machine implementation
- **@orchestration-patterns**: Service orchestration
- **@integration-architect**: System integration

**Key Takeaway**: Well-designed workflows provide visibility, reliability, and scalability for complex business processes. Use state machines for clear state management and orchestration patterns for distributed coordination.

---

**End of Part II: Architecture & System Design Skills**

---

**Next Part**: [Part III: Business & Marketing Skills →](chapter-10-seo-content-marketing.md)
