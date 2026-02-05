# Chapter 27: Cryptography & Data Protection

**Last Updated:** February 5, 2026

---

## Overview

Cryptography is fundamental to modern security, protecting data confidentiality, integrity, and authenticity. Proper implementation of cryptographic controls is essential for securing applications and meeting compliance requirements.

This chapter covers essential cryptography skills for implementing encryption, managing keys, and protecting sensitive data.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@crypto-expert` | Cryptographic implementation | Encryption, hashing, signing |
| `@kms-expert` | Key management | Key lifecycle, HSM, cloud KMS |
| `@pki-expert` | PKI infrastructure | Certificates, CA management |
| `@data-protection-expert` | Data security | Tokenization, masking, DLP |

---

## 27.1 Cryptography Implementation with @crypto-expert

### Skill Introduction

The `@crypto-expert` skill provides expertise in implementing cryptographic controls correctly. It helps you choose appropriate algorithms, implement them securely, and avoid common cryptographic pitfalls.

**When to use this skill:**
- Selecting cryptographic algorithms
- Implementing encryption/decryption
- Secure password storage
- Digital signatures
- Random number generation

**Key strengths:**
- Deep knowledge of cryptographic primitives
- Experience with common pitfalls
- Understanding of compliance requirements

---

### Cryptography Implementation Prompts

#### Implementing Encryption at Rest

**Context:** You need to implement encryption for sensitive data stored in your database.

```text
@crypto-expert Design encryption at rest for sensitive database fields:

Application context:
- Node.js backend with PostgreSQL
- Sensitive fields: SSN, credit card numbers (tokens), health data
- Need to search encrypted fields in some cases
- Compliance: HIPAA, PCI-DSS

Requirements:
- Field-level encryption (not just disk encryption)
- Key rotation capability
- Performance considerations (thousands of queries/second)
- Different keys for different data classifications

Current approach:
- No application-level encryption
- Using RDS with storage encryption only

Please provide:
1. Encryption algorithm selection
2. Key hierarchy design
3. Implementation approach (envelope encryption)
4. Searchable encryption considerations
5. Code examples for encrypt/decrypt operations
6. Key rotation procedure
7. Performance optimization
```

**Expected Output:** Field-level encryption design and implementation.

---

#### Secure Password Storage

**Context:** You're implementing user authentication and need secure password storage.

```text
@crypto-expert Design secure password storage for our application:

Requirements:
- Store passwords for 1M+ users
- Protect against database breaches
- Support password verification efficiently
- Meet current security best practices

Questions:
- Which hashing algorithm (Argon2, bcrypt, scrypt)?
- What work factor/iterations?
- Should we use pepper in addition to salt?
- How to handle password upgrades (when algorithms change)?

Please provide:
1. Algorithm selection with justification
2. Parameter recommendations
3. Implementation code example
4. Migration strategy for existing passwords
5. Security considerations and common mistakes
```

**Expected Output:** Password storage implementation guide.

---

## 27.2 Key Management with @kms-expert

### Skill Introduction

The `@kms-expert` skill provides expertise in key management systems and practices. It helps you manage the full lifecycle of cryptographic keys securely.

**When to use this skill:**
- Designing key management architecture
- Implementing cloud KMS
- Key rotation strategies
- HSM integration
- Key lifecycle management

**Key strengths:**
- Experience with cloud KMS (AWS, Azure, GCP)
- Knowledge of key management best practices
- Understanding of HSM deployment

---

### Key Management Prompts

#### Designing Key Management Architecture

**Context:** You need a comprehensive key management strategy for your organization.

```text
@kms-expert Design key management architecture for our cloud environment:

Environment:
- AWS as primary cloud
- Multi-account organization
- Applications needing encryption keys
- Secrets that need secure storage

Use cases:
- Application-level encryption keys
- Database encryption (RDS)
- S3 bucket encryption
- Secrets for applications (API keys, credentials)
- Certificate private keys
- Customer-managed keys (for B2B customers)

Requirements:
- Separation of duties for key operations
- Audit trail for all key usage
- Key rotation without downtime
- Cross-account key sharing (where appropriate)
- Compliance with PCI-DSS key management

Please provide:
1. Key hierarchy design
2. AWS KMS architecture
3. Key policy design for access control
4. Key rotation strategy
5. Cross-account access patterns
6. Secrets management integration
7. Monitoring and alerting
```

**Expected Output:** Key management architecture design.

---

## 27.3 PKI Infrastructure with @pki-expert

### Skill Introduction

The `@pki-expert` skill provides expertise in Public Key Infrastructure for managing digital certificates. It helps you design and operate PKI for authentication and encryption.

**When to use this skill:**
- Designing certificate infrastructure
- Implementing mTLS
- Certificate lifecycle management
- Private CA deployment
- Certificate automation

**Key strengths:**
- Deep PKI knowledge
- Experience with certificate automation
- Understanding of trust models

---

### PKI Implementation Prompts

#### Implementing mTLS for Microservices

**Context:** You want to implement mutual TLS for service-to-service communication.

```text
@pki-expert Implement mTLS for our microservices:

Environment:
- 50 microservices in Kubernetes
- Services communicate via HTTP/gRPC
- Istio service mesh deployed
- Need both service and user authentication

Requirements:
- Automatic certificate provisioning
- Short-lived certificates (24-hour)
- Certificate rotation without downtime
- Support for non-Kubernetes services
- Audit trail for certificate issuance

Questions to address:
- Build vs buy private CA
- Certificate distribution mechanism
- Revocation approach
- Monitoring and alerting

Please provide:
1. PKI architecture design
2. Private CA options (AWS PCA, Vault, cert-manager)
3. Certificate issuance workflow
4. Service identity model
5. Certificate rotation automation
6. Monitoring and troubleshooting
7. Non-mesh service integration
```

**Expected Output:** mTLS implementation with PKI design.

---

## 27.4 Data Protection with @data-protection-expert

### Skill Introduction

The `@data-protection-expert` skill provides expertise in protecting sensitive data through various techniques including tokenization, masking, and data loss prevention.

**When to use this skill:**
- Implementing tokenization
- Data masking for non-production
- Data loss prevention strategies
- Data classification
- Privacy-enhancing technologies

**Key strengths:**
- Experience with tokenization systems
- Knowledge of data masking techniques
- Understanding of DLP implementation

---

### Data Protection Prompts

#### Implementing Data Tokenization

**Context:** You need to tokenize payment data to reduce PCI-DSS scope.

```text
@data-protection-expert Implement tokenization for payment data:

Current state:
- E-commerce application processing payments
- Currently storing encrypted card numbers
- Full PCI-DSS scope for application
- Want to reduce scope with tokenization

Requirements:
- Replace PANs with tokens
- Support recurring payments
- Integration with payment processor
- Token format: last 4 digits visible
- Token vault high availability

Options to evaluate:
- Build vs payment processor tokenization
- Vault architecture options

Please provide:
1. Tokenization architecture options
2. Token format and generation
3. Token vault design
4. Integration approach
5. Migration from encrypted storage
6. PCI scope reduction analysis
7. Ongoing operations
```

**Expected Output:** Tokenization implementation design.

---

## Best Practices Summary

### Cryptography
1. **Standard Algorithms:** Use well-vetted algorithms
2. **No Custom Crypto:** Don't invent your own
3. **Key Separation:** Different keys for different purposes
4. **Secure Random:** Cryptographically secure RNG
5. **Regular Updates:** Stay current with algorithm changes

### Key Management
1. **Least Privilege:** Minimal key access
2. **Rotation:** Regular key rotation
3. **Audit:** Log all key operations
4. **Separation of Duties:** No single person controls keys
5. **Recovery:** Tested backup and recovery

### Data Protection
1. **Classify First:** Know your data before protecting it
2. **Minimize:** Don't store what you don't need
3. **Layer Protection:** Multiple protection mechanisms
4. **Test:** Verify protection effectiveness
5. **Monitor:** Detect data handling anomalies

---

## Reflection Points

1. **Algorithm Choice:** How do you evaluate new cryptographic algorithms?
2. **Key Access:** Who should have access to encryption keys?
3. **Quantum:** How are you preparing for post-quantum cryptography?
4. **Performance:** How do you balance security with performance?

---

**Next Chapter:** [Chapter 28: Testing Fundamentals →](chapter-28-testing-fundamentals.md)
