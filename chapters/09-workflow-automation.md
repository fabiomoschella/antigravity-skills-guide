# Chapter 9: Workflow & Automation Architecture

**Last Updated:** February 5, 2026

---

## Overview

Workflow and automation architecture enables organizations to streamline complex processes, reduce manual intervention, and ensure consistent execution. This chapter covers skills for designing and implementing workflow systems.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@workflow-architect` | Workflow design | System architecture, process mapping |
| `@process-automation` | Business automation | ROI analysis, efficiency |
| `@n8n-mcp-tools-expert` | n8n integration | Self-hosted automation, AI agents |
| `@zapier-make-patterns` | No-code automation | Quick integrations, prototyping |
| `@playwright-skill` | Browser automation | Testing, scraping, simulation |
| `@discord-bot-builder` | ChatOps | Community management, alerts |
| `@telegram-bot-builder` | Messaging bots | Notifications, mini-apps |
| `@automate-whatsapp` | Business messaging | Customer support, alerts |

---

## 9.1 Workflow Architecture with @workflow-architect

### Skill Introduction

The `@workflow-architect` skill helps you design robust, scalable automation systems. It focuses on the architectural patterns—sequential, parallel, conditional, and event-driven—required to build reliability and error handling into your workflows.

**When to use this skill:**
- Designing a complex new automation system
- Refactoring fragile "spaghetti" automations
- Choosing the right tool (n8n vs Make vs Custom Code)
- Implementing error handling and retry logic
- Documenting process flows for stakeholders

**Key strengths:**
- Architectural pattern selection
- Error handling strategies (Dead Letter Queues)
- State management design
- Scalability planning

---

### Workflow Architecture Prompts

#### Designing a Resilient Order Processing Workflow

**Context:** You are designing an order fulfillment system that must handle failures gracefully.

```text
@workflow-architect Design a resilient order processing workflow:

Process:
1. Receive Order (Webhook)
2. Charge Credit Card (Stripe)
3. Update Inventory (Shopify)
4. Send Shipping Label (ShipStation)
5. Notify Customer (Email)

Requirements:
- Must handle 1000 orders/hour.
- If Inventory update fails, don't charge card (or refund).
- If Shipping fails, retry 3 times, then alert support.
- Must capture all failures in a log.

Please provide:
1. Workflow Diagram (Mermaid or text description)
2. Error Handling Strategy (Retries vs. Compensating Transactions)
3. State Management approach (How to track status?)
4. Tool selection recommendation (why n8n/Make/Temporal?)
```

**Expected Output:** A detailed architectural design document including failure scenarios and mitigation strategies.

---

#### Documenting an Existing Process

**Context:** You have a messy manual process for employee onboarding that needs automation.

```text
@workflow-architect Create a process map for Employee Onboarding to prepare for automation:

Current steps (Manual):
- HR sends offer letter via email.
- Candidate signs PDF.
- HR creates email account (Google Workspace).
- HR adds to Slack.
- IT ships laptop.
- Manager schedules kick-off meeting.

Goal: Automate 90% of this.

Please provide:
1. As-is Process Map (identifying bottlenecks).
2. To-be Automated Workflow design.
3. Trigger points (e.g., "Signed Contract" webhook).
4. Integration points (DocuSign, Google Admin, Slack API).
```

**Expected Output:** A clear "Before" and "After" process map ready for implementation.

---

## 9.2 n8n Automation with @n8n-mcp-tools-expert

### Skill Introduction

The `@n8n-mcp-tools-expert` skill specializes in building workflows with n8n, a powerful extendable workflow automation tool. It covers node configuration, custom code (Python/JS), and integration with AI agents.

**When to use this skill:**
- Building self-hosted automation pipelines
- Integrating custom internal APIs
- Creating complex data transformation workflows
- Connecting AI agents/LLMs to tools
- Processing large data sets (ETL)

**Key strengths:**
- Node configuration expertise
- Function node coding (JavaScript/Python)
- JSON data manipulation
- Error trigger management

---

### n8n Automation Prompts

#### Building an AI-Powered News Summarizer

**Context:** You want to build an n8n workflow that monitors RSS feeds, summarizes them with LLMs, and posts to Slack.

```text
@n8n-mcp-tools-expert Guide me to build an "AI News Summarizer" in n8n:

Inputs:
- RSS Feed URL (e.g., Hacker News)

Process:
1. Fetch latest items every hour.
2. Filter for keywords (e.g., "AI", "LLM").
3. Send content to OpenAI (GPT-4) for a succinct summary.
4. Format output as a Slack block with link.
5. Post to #news channel.

Please provide:
1. List of n8n nodes required.
2. The JavaScript code for the "Filter" Function node.
3. The Prompt to send to the LLM node.
4. JSON structure for the Slack message.
```

**Expected Output:** Implementation details for each step of the n8n workflow.

---

#### Data Transformation with Python Node

**Context:** You have messy JSON data from an API that needs cleaning before inserting into a database.

```text
@n8n-mcp-tools-expert Write Python code for an n8n Code Node to transform this data:

Input JSON (Array of objects):
[
  {"name": "John Doe", "signup_date": "2023-01-01T12:00:00Z", "plan": "free"},
  {"name": "Jane Smith", "signup_date": "2023-02-15T09:30:00", "plan": "pro"}
]

Requirements:
1. Format `signup_date` to "YYYY-MM-DD".
2. Capitalize `plan` ("Free", "Pro").
3. Add a new field `is_active` = True.
4. Return the modified JSON array.
```

**Expected Output:** Python code snippet ready to paste into an n8n Code node.

---

## 9.3 No-Code Automation with @zapier-make-patterns

### Skill Introduction

The `@zapier-make-patterns` skill focuses on using platform-as-a-service automation tools like Zapier and Make (formerly Integromat). It helps with quick prototyping, simple integrations, and utilizing scenarios efficiently.

**When to use this skill:**
- Rapidly prototyping an MVP feature
- Connecting popular SaaS apps (Gmail, Trello, Airtable)
- Simple "If This Then That" logic
- Automating personal productivity tasks
- Managing webhook integrations

**Key strengths:**
- Scenario optimization (reducing operation usage)
- Filter and Router logic
- Webhook configuration
- Data mapping between apps

---

### No-Code Automation Prompts

#### Optimizing a Make (Integromat) Scenario

**Context:** Your Make scenario is consuming too many operations and costing too much.

```text
@zapier-make-patterns Optimize this Make scenario to reduce operation usage:

Current Scenario:
1. Trigger: Watch New Emails (Gmail) - Runs every 5 mins.
2. Google Sheets: Search for Row (Check if sender exists).
3. Google Sheets: Add Row (If not exists).
4. Slack: Send Message.

Problem: It runs every 5 minutes even if no email arrives, and "Search Row" uses an op every time.

Goal: Reduce operations while keeping near real-time speed.

Please suggest:
1. Architectural changes (e.g., Webhooks vs Polling).
2. Filter logic improvements.
3. Error handling to prevent loops.
```

**Expected Output:** Optimization strategy to lower costs and improve efficiency.

---

## 9.4 Browser Automation with @playwright-skill

### Skill Introduction

The `@playwright-skill` enables you to automate web interactions that lack APIs. It uses Playwright to simulate user behavior for testing, scraping, or automating legacy web applications.

**When to use this skill:**
- Scaping data from websites without public APIs
- Automating data entry into legacy portals
- End-to-end (E2E) testing of web applications
- Generating screenshots or PDFs from web pages
- Monitoring website uptime and UI fidelity

**Key strengths:**
- Selector strategies (CSS, XPath)
- Handling dynamic content (SPAs)
- Authentication automation
- Headless browser configuration

---

### Browser Automation Prompts

#### Scraping Dynamic Data

**Context:** You need to scrape prices from a competitor's website that uses heavy JavaScript (React).

```text
@playwright-skill specific Write a Playwright script (TypeScript) to scrape product prices:

Target: `https://example-store.com/products`
Requirement:
1. Navigate to page.
2. Wait for the product grid to load (div.product-grid).
3. Scroll down to trigger lazy loading.
4. Extract "Product Name" and "Price" for all items.
5. Save to `products.json`.

Handle potential timeouts and cookie consent popups.
```

**Expected Output:** A ready-to-run Playwright script with comments explaining the logic.

---

#### Automating a Legacy Login

**Context:** You need to automate a daily report download from an old vendor portal.

```text
@playwright-skill Create a Playwright automation for a legacy portal login:

Steps:
1. Go to `portal.legacy-vendor.com`.
2. Enter Username and Password.
3. Click "Login".
4. Wait for the "Dashboard" element to appear.
5. Click "Reports" > "Daily Export".
6. specific Handle the file download event and save to `./downloads`.

Include error handling if the login fails or site is down.
```

**Expected Output:** A robust automation script for handling login and file downloads.

---

## Best Practices Summary

### Architecture First
- **Plan before building:** Draw the workflow before adding nodes.
- **Idempotency:** Ensure that running the same event twice doesn't break things (e.g., charging a card twice).
- **Loose Coupling:** Use webhooks and queues to decouple systems.

### Error Handling
- **Expect Failure:** APIs go down. Credentials expire. Build retries into every step.
- **Dead Letter Queues:** Store failed events so they can be replayed later.
- **Monitoring:** Set up alerts when workflows fail, don't just rely on checking logs manually.

### Tool Selection
- **Zapier/Make:** Best for simple, linear integrations and prototyping.
- **n8n:** Best for complex data transformation, self-hosting, and cost control.
- **Code:** Best for highly specific logic or performance-critical tasks.

---

## Reflection Points

1. **Fragility:** If one API changes, does your whole system break?
2. **Visibility:** Can you easily see the status of an order that happened yesterday?
3. **Security:** Are you managing API keys securely (not hardcoded)?
4. **Maintenance:** Who fixes the bot when it breaks while you are on vacation?

---

**Next Chapter:** [Chapter 10: SEO & Content Marketing →](10-seo-content-marketing.md)
