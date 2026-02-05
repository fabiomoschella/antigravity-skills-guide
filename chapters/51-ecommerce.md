# Chapter 51: E-commerce Development

**Last Updated:** February 5, 2026

---

## Overview

E-commerce development builds the platforms that power online retail. From product catalogs to checkout flows, e-commerce systems require expertise in performance, security, and user experience to convert browsers into buyers.

This chapter covers essential skills for building robust, scalable e-commerce platforms.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@ecommerce-architect` | E-commerce architecture | Platform design |
| `@payment-expert` | Payment integration | Payments, PCI compliance |
| `@payment-integration` | Payment integrations | Multiple gateways |
| `@stripe-integration` | Stripe payments | Stripe implementation |
| `@paypal-integration` | PayPal payments | PayPal implementation |
| `@shopify-development` | Shopify dev | Shopify stores |
| `@shopify-apps` | Shopify apps | Custom Shopify apps |
| `@inventory-expert` | Inventory systems | Stock management |
| `@cart-checkout-expert` | Cart and checkout | Conversion optimization |
| `@algolia-search` | Algolia search | E-commerce search |

---

## 51.1 E-commerce Architecture with @ecommerce-architect

### Skill Introduction

The `@ecommerce-architect` skill provides expertise in designing e-commerce platforms. It helps you architect scalable, performant systems for online retail.

**When to use this skill:**
- Building e-commerce platforms
- Platform modernization
- Multi-channel commerce
- Marketplace design

**Key strengths:**
- E-commerce patterns
- Scalability design
- Integration experience

---

### E-commerce Architecture Prompts

#### Designing E-commerce Platform

**Context:** You're building a new e-commerce platform from scratch.

```text
@ecommerce-architect Design a modern e-commerce platform:

Business requirements:
- B2C fashion retailer
- 50K products across 500 categories
- 1 million monthly visitors
- Multi-currency and multi-language
- Mobile-first experience

Functional requirements:
- Product catalog with variants (size, color)
- Inventory management across warehouses
- Cart and wishlist
- Multiple payment methods
- Shipping calculation and tracking
- Customer accounts and order history
- Promotions and discount codes

Non-functional requirements:
- Sub-second page loads
- 99.9% availability
- Handle flash sales (10x traffic)
- PCI DSS compliance

Please provide:
1. Overall architecture design
2. Service decomposition
3. Database design strategy
4. Caching architecture
5. Search implementation
6. Third-party integrations
7. Mobile app considerations
8. Scalability approach
```

**Expected Output:** E-commerce platform architecture.

---

## 51.2 Payment Integration with @payment-expert

### Skill Introduction

The `@payment-expert` skill provides expertise in payment processing integration. It helps you implement secure, compliant payment systems with multiple payment methods.

**When to use this skill:**
- Implementing payments
- PCI compliance
- Payment provider selection
- Subscription billing

**Key strengths:**
- Payment gateway experience
- PCI compliance knowledge
- Fraud prevention

---

### Payment Integration Prompts

#### Implementing Payment Processing

**Context:** You need to implement payment processing for your e-commerce platform.

```text
@payment-expert Design payment processing for e-commerce:

Requirements:
- Credit/debit cards (Visa, Mastercard, Amex)
- Digital wallets (Apple Pay, Google Pay, PayPal)
- Buy now pay later (Klarna, Affirm)
- Multiple currencies (USD, EUR, GBP)
- Subscriptions for repeat orders
- Refunds and chargebacks

Compliance:
- PCI DSS compliance required
- GDPR for EU customers
- Strong Customer Authentication (SCA)

Volume:
- 10K transactions per day
- Average order value $75
- 2% fraud rate target

Please provide:
1. Payment provider recommendation
2. Integration architecture
3. PCI scope reduction strategy
4. Card tokenization approach
5. 3D Secure implementation
6. Fraud prevention measures
7. Refund and chargeback handling
8. Reconciliation process
```

**Expected Output:** Payment system implementation plan.

---

## 51.3 Inventory Management with @inventory-expert

### Skill Introduction

The `@inventory-expert` skill provides expertise in inventory management systems. It helps you design systems that track stock accurately and handle complex fulfillment scenarios.

**When to use this skill:**
- Inventory tracking systems
- Multi-warehouse fulfillment
- Stock synchronization
- Order management

**Key strengths:**
- Inventory patterns
- Fulfillment optimization
- Real-time stock management

---

### Inventory Management Prompts

#### Designing Inventory System

**Context:** You need to design an inventory management system.

```text
@inventory-expert Design inventory management system:

Business context:
- Fashion retailer with 50K SKUs
- 3 warehouses in different regions
- Online and 20 retail stores
- Multiple channels (web, app, Amazon)

Requirements:
- Real-time inventory visibility
- Reserve stock for carts
- Allocate orders to warehouses
- Back-order handling
- Low stock alerts
- Inventory transfers

Challenges:
- Overselling during flash sales
- Inventory discrepancies
- Channel synchronization lag
- Pre-orders and backorders

Please provide:
1. Inventory data model
2. Real-time stock tracking
3. Reservation system design
4. Multi-warehouse allocation
5. Channel synchronization
6. Cycle count integration
7. Performance optimization
8. Audit and reconciliation
```

**Expected Output:** Inventory system design.

---

## 51.4 Cart and Checkout with @cart-checkout-expert

### Skill Introduction

The `@cart-checkout-expert` skill provides expertise in shopping cart and checkout optimization. It helps you design frictionless checkout experiences that maximize conversion.

**When to use this skill:**
- Cart implementation
- Checkout optimization
- Abandoned cart recovery
- Guest checkout flows

**Key strengths:**
- Conversion optimization
- Checkout UX patterns
- Cart persistence

---

### Cart and Checkout Prompts

#### Optimizing Checkout Flow

**Context:** Your checkout has high abandonment rates.

```text
@cart-checkout-expert Optimize checkout to reduce abandonment:

Current metrics:
- 70% cart abandonment rate
- 4-step checkout process
- 3-minute average completion time
- 30% drop at shipping step

Current flow:
1. Cart review
2. Login/Register or Guest
3. Shipping address and method
4. Payment and confirmation

Known issues:
- Forced account creation
- Shipping costs surprise
- Too many form fields
- Payment errors not clear
- Mobile experience poor

Please provide:
1. Checkout UX audit framework
2. Streamlined flow design
3. Guest checkout optimization
4. Address auto-completion
5. Payment error handling
6. Mobile checkout improvements
7. Cart recovery strategies
8. A/B testing priorities
```

**Expected Output:** Checkout optimization plan.

---

## Best Practices Summary

### Architecture
1. **Scalability:** Design for peaks
2. **Performance:** Every millisecond matters
3. **Reliability:** Downtime = lost sales
4. **Security:** Protect customer data
5. **Mobile First:** Mobile commerce dominates

### Payments
1. **PCI Compliance:** Non-negotiable
2. **Multiple Methods:** Reduce friction
3. **Fraud Balance:** Don't over-reject
4. **Clear Errors:** Help users recover
5. **Tokenization:** Minimize data handling

### Inventory
1. **Real-Time:** Accurate availability
2. **Reserve:** Prevent overselling
3. **Buffer:** Safety stock for peaks
4. **Sync:** Channel consistency
5. **Audit:** Regular reconciliation

---

## Reflection Points

1. **Build vs Buy:** When to use platforms like Shopify?
2. **Performance vs Features:** How do you prioritize?
3. **Fraud vs Conversion:** How do you balance?
4. **Omnichannel:** How do you unify online and offline?

---

**Next Chapter:** [Chapter 52: FinTech →](chapter-52-fintech.md)
