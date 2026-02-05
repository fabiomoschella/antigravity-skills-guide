# Chapter 52: FinTech Development

**Last Updated:** February 5, 2026

---

## Overview

Financial technology (FinTech) development builds the software that powers modern financial services. From banking integrations to investment platforms, FinTech requires expertise in security, compliance, and precision.

This chapter covers essential skills for building secure, compliant financial software.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@fintech-architect` | FinTech architecture | Financial systems design |
| `@banking-api-expert` | Banking integration | Open Banking, aggregation |
| `@compliance-fintech` | Financial compliance | Regulatory requirements |
| `@fintech-security` | Security for finance | Financial data protection |

---

## 52.1 FinTech Architecture with @fintech-architect

### Skill Introduction

The `@fintech-architect` skill provides expertise in designing financial technology systems. It helps you architect systems that meet the unique requirements of financial services.

**When to use this skill:**
- Building financial platforms
- Payment processing systems
- Investment platforms
- Banking applications

**Key strengths:**
- Financial system patterns
- Regulatory awareness
- Security-first design

---

### FinTech Architecture Prompts

#### Designing Personal Finance App

**Context:** You're building a personal finance management application.

```text
@fintech-architect Design personal finance management platform:

Features:
- Bank account aggregation (multi-bank)
- Transaction categorization
- Spending analysis and insights
- Budget tracking and alerts
- Financial goals tracking
- Net worth calculation

Requirements:
- Connect to 10K+ financial institutions
- Real-time transaction updates
- Secure credential handling
- Historical data storage (7 years)
- Multi-currency support

Compliance:
- GDPR for EU users
- Data encryption requirements
- Audit trail for data access

Please provide:
1. System architecture design
2. Bank aggregation strategy
3. Data model for transactions
4. Categorization engine design
5. Security architecture
6. Real-time notification system
7. Analytics and insights engine
8. Mobile and web architecture
```

**Expected Output:** Personal finance platform architecture.

---

## 52.2 Banking Integration with @banking-api-expert

### Skill Introduction

The `@banking-api-expert` skill provides expertise in integrating with banking APIs and financial data providers. It helps you implement Open Banking connections and account aggregation.

**When to use this skill:**
- Bank account connections
- Transaction data retrieval
- Payment initiation
- Balance checks

**Key strengths:**
- Banking API experience
- Aggregation providers
- Financial data handling

---

### Banking Integration Prompts

#### Implementing Bank Account Aggregation

**Context:** You need to implement bank account aggregation for your app.

```text
@banking-api-expert Implement bank account aggregation:

Requirements:
- Connect to US and European banks
- Retrieve accounts and balances
- Get transaction history (24 months)
- Support checking, savings, credit cards
- Refresh data regularly
- Handle connection errors gracefully

Provider considerations:
- Plaid, MX, Yodlee, TrueLayer
- Cost per connection
- Coverage of institutions
- Reliability and uptime
- Support for OAuth vs credential

Technical needs:
- Webhook support for updates
- Error classification
- Re-authentication flows
- Rate limit handling

Please provide:
1. Provider comparison and recommendation
2. Integration architecture
3. Account linking flow
4. Data synchronization strategy
5. Error handling approach
6. Credential security
7. Webhook handling
8. Fallback strategies
```

**Expected Output:** Bank aggregation implementation plan.

---

## 52.3 Financial Compliance with @compliance-fintech

### Skill Introduction

The `@compliance-fintech` skill provides expertise in financial regulatory compliance. It helps you navigate the complex landscape of financial regulations.

**When to use this skill:**
- Regulatory requirements analysis
- Compliance implementation
- Audit preparation
- KYC/AML implementation

**Key strengths:**
- Regulatory knowledge
- Compliance implementation
- Audit experience

---

### Compliance Prompts

#### Implementing KYC/AML Compliance

**Context:** You need to implement Know Your Customer and Anti-Money Laundering.

```text
@compliance-fintech Implement KYC/AML for financial platform:

Platform type:
- Consumer lending marketplace
- Handle personal loans
- US market initially

Requirements:
- Identity verification
- Address verification
- Sanctions screening
- Fraud detection
- Suspicious activity reporting
- Record keeping

Risk tiers:
- Low risk: basic verification
- Medium risk: enhanced due diligence
- High risk: manual review

Volume:
- 10K new customers/month
- 500K transactions/month

Please provide:
1. KYC/AML program design
2. Identity verification workflow
3. Sanctions screening implementation
4. Transaction monitoring rules
5. Suspicious activity handling
6. Document retention policy
7. Vendor selection (identity providers)
8. Audit trail requirements
```

**Expected Output:** KYC/AML compliance implementation plan.

---

## 52.4 Financial Security with @fintech-security

### Skill Introduction

The `@fintech-security` skill provides expertise in security for financial applications. It helps you implement security controls appropriate for financial data.

**When to use this skill:**
- Security architecture for finance
- Encryption implementation
- Access controls
- Incident response

**Key strengths:**
- Financial security standards
- Encryption expertise
- Threat modeling

---

### Financial Security Prompts

#### Securing Financial Application

**Context:** You're designing security for a new financial application.

```text
@fintech-security Design security for financial application:

Application:
- Investment platform
- Holds user funds
- Bank connections
- Trading functionality

Data handled:
- Personal information (SSN, address)
- Bank credentials (via aggregator)
- Account balances
- Transaction history

Threats:
- Account takeover
- Credential theft
- Insider threats
- Data breaches
- Fraud

Requirements:
- SOC 2 Type II
- State money transmitter licenses
- FINRA compliance

Please provide:
1. Security architecture
2. Authentication strategy
3. Encryption at rest and transit
4. Access control model
5. Key management approach
6. Logging and monitoring
7. Incident response plan
8. Penetration testing strategy
```

**Expected Output:** Financial security design.

---

## Best Practices Summary

### Architecture
1. **Accuracy First:** Financial calculations precise
2. **Audit Trail:** Log everything
3. **Idempotency:** Safe retries
4. **Reconciliation:** Regular checks
5. **Disaster Recovery:** RPO/RTO for finance

### Compliance
1. **Know Requirements:** Regulatory landscape
2. **Document Everything:** Policies and procedures
3. **Regular Audits:** Internal and external
4. **Training:** Staff awareness
5. **Update Regularly:** Regulations change

### Security
1. **Defense in Depth:** Multiple layers
2. **Least Privilege:** Minimal access
3. **Encryption:** Everywhere
4. **Monitoring:** Continuous
5. **Response Ready:** Incident plans

---

## Reflection Points

1. **Compliance Cost:** How do you balance compliance and velocity?
2. **Build vs Partner:** When to build vs integrate?
3. **Trust:** How do you build user trust?
4. **Innovation:** How do you innovate within regulations?

---

**Next Chapter:** [Chapter 53: Healthcare Tech →](chapter-53-healthcare.md)
