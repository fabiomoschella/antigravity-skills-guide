# Chapter 23: Application Security

**Last Updated:** February 5, 2026

---

## Overview

Application security is the practice of protecting applications from threats throughout their lifecycle. From secure coding practices to vulnerability management and security testing, building secure applications requires a holistic approach.

This chapter covers essential application security skills to help you identify vulnerabilities, implement secure coding practices, and protect your applications from attacks.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@security-architect` | Security architecture | Secure design, threat modeling |
| `@secure-code-expert` | Secure coding | Code review, vulnerability prevention |
| `@sast-expert` | Static analysis | Automated code scanning |
| `@sast-configuration` | SAST setup | Tool configuration |
| `@dast-expert` | Dynamic testing | Runtime security testing |
| `@vulnerability-scanner` | Vuln scanning | Automated scanning |
| `@pentest-checklist` | Pentest planning | Comprehensive testing |
| `@pentest-commands` | Pentest commands | Quick reference |
| `@burp-suite-testing` | Burp Suite | Web app testing |
| `@top-web-vulnerabilities` | OWASP Top 10 | Common vulnerabilities |
| `@api-fuzzing-bug-bounty` | API fuzzing | Bug bounty hunting |
| `@api-security-best-practices` | API security | Secure APIs |

---

## 23.1 Security Architecture with @security-architect

### Skill Introduction

The `@security-architect` skill provides expertise in designing secure systems from the ground up. It helps you implement defense in depth, conduct threat modeling, and make security a foundational aspect of your architecture.

**When to use this skill:**
- Designing new systems with security in mind
- Conducting threat modeling exercises
- Reviewing architecture for security gaps
- Implementing security controls and patterns
- Creating security requirements

**Key strengths:**
- Deep knowledge of security frameworks
- Experience with threat modeling methodologies
- Understanding of defense in depth strategies

---

### Security Architecture Prompts

#### Conducting Threat Modeling

**Context:** You're designing a new application and need to identify security threats.

```text
@security-architect Conduct threat modeling for our new e-commerce platform:

System overview:
- Web application (React SPA)
- REST API backend (Node.js)
- PostgreSQL database with PII
- Integration with payment processor (Stripe)
- Admin portal for internal users
- Mobile apps (iOS, Android)

Data handled:
- Customer PII (names, addresses, emails)
- Payment tokens (no raw card data)
- Order history
- Authentication credentials

Threat actors of concern:
- External attackers (opportunistic, targeted)
- Malicious insiders (employees)
- Supply chain (dependencies, third parties)

Please provide:
1. System decomposition for threat modeling
2. STRIDE analysis for each component
3. Data flow diagrams with trust boundaries
4. Prioritized threat list (likelihood x impact)
5. Mitigation strategies for top threats
6. Security requirements derived from threats
7. Residual risk assessment
```

**Expected Output:** Complete threat model with mitigations.

---

#### Designing Authentication Architecture

**Context:** You need to design a secure authentication system for multiple applications.

```text
@security-architect Design authentication architecture for our platform:

Requirements:
- Single sign-on across 5 web applications
- Mobile app authentication
- API authentication for third parties
- MFA support (TOTP, WebAuthn)
- Social login (Google, Microsoft)
- Enterprise SSO (SAML, OIDC) for B2B

Security requirements:
- Session timeout: 15 minutes idle, 8 hours absolute
- Password policy: 12+ chars, complexity, breach checking
- Brute force protection
- Secure token storage

Users:
- 100K B2C consumers
- 1K B2B enterprise users
- 50 internal admin users

Please provide:
1. Authentication architecture design
2. Identity provider selection (Auth0, Keycloak, custom)
3. Token management strategy (JWT, sessions)
4. MFA implementation approach
5. Enterprise SSO integration
6. Security controls and monitoring
7. Account recovery process
```

**Expected Output:** Complete authentication architecture.

---

## 23.2 Secure Coding with @secure-code-expert

### Skill Introduction

The `@secure-code-expert` skill provides guidance on writing secure code and identifying vulnerabilities in existing code. It helps developers prevent common security issues and adopt secure coding practices.

**When to use this skill:**
- Reviewing code for security vulnerabilities
- Learning secure coding patterns
- Fixing identified vulnerabilities
- Creating secure coding guidelines
- Training developers on security

**Key strengths:**
- Expert in OWASP Top 10 and CWE
- Experience with secure coding in multiple languages
- Knowledge of vulnerability patterns and fixes

---

### Secure Coding Prompts

#### Secure Code Review

**Context:** You need to conduct a security review of application code.

```text
@secure-code-expert Conduct a security review of this Node.js API code:

```javascript
app.get('/api/users/:id', async (req, res) => {
  const userId = req.params.id;
  const query = `SELECT * FROM users WHERE id = ${userId}`;
  const result = await db.query(query);
  res.json(result.rows[0]);
});

app.post('/api/login', async (req, res) => {
  const { email, password } = req.body;
  const user = await db.query('SELECT * FROM users WHERE email = $1', [email]);
  if (user.rows[0] && user.rows[0].password === password) {
    const token = jwt.sign({ userId: user.rows[0].id }, 'secret123');
    res.cookie('token', token);
    res.json({ success: true });
  }
});

app.get('/api/files/:filename', (req, res) => {
  const file = path.join(__dirname, 'uploads', req.params.filename);
  res.sendFile(file);
});
```

Please identify:
1. All security vulnerabilities present
2. Severity rating for each issue
3. Attack scenarios for each vulnerability
4. Secure code fixes for each issue
5. Additional security controls to add
6. Testing approaches to verify fixes
```

**Expected Output:** Security review with vulnerabilities and fixes.

---

#### Creating Secure Coding Guidelines

**Context:** You need to create secure coding guidelines for your development team.

```text
@secure-code-expert Create secure coding guidelines for our Node.js/TypeScript team:

Context:
- Building REST APIs with Express
- PostgreSQL database with TypeORM
- JWT-based authentication
- Handling PII and payment data

Topics to cover:
- Input validation and sanitization
- Authentication and authorization
- Database security (SQL injection prevention)
- Crypto and secrets management
- Error handling and logging
- Dependency management
- API security

Please provide:
1. Secure coding standard document structure
2. Rules for each topic with examples
3. Code examples (insecure vs secure)
4. Automated tool recommendations for enforcement
5. Exception handling process
6. Training plan for developers
```

**Expected Output:** Comprehensive secure coding guidelines.

---

## 23.3 Static Analysis with @sast-expert

### Skill Introduction

The `@sast-expert` skill provides expertise in Static Application Security Testing (SAST). It helps you implement automated code scanning to find vulnerabilities early in development.

**When to use this skill:**
- Setting up SAST tools in CI/CD
- Configuring and tuning SAST rules
- Triaging SAST findings
- Reducing false positives
- Selecting SAST tools

**Key strengths:**
- Experience with major SAST tools
- Knowledge of tuning for accuracy
- Understanding of CI/CD integration

---

### Static Analysis Prompts

#### Implementing SAST in CI/CD

**Context:** You want to integrate security scanning into your development pipeline.

```text
@sast-expert Implement SAST scanning in our CI/CD pipeline:

Codebase:
- TypeScript/Node.js backend
- React frontend
- Python data processing scripts
- 500K lines of code total

Current CI/CD:
- GitHub Actions
- Run on every PR and merge to main
- Pipeline takes 15 minutes currently

Requirements:
- Scan for OWASP Top 10 vulnerabilities
- Block PRs with critical/high findings
- Minimize false positives
- Developer-friendly reporting
- Cost-effective (prefer open source)

Please provide:
1. SAST tool recommendations (Semgrep, SonarQube, CodeQL)
2. Tool configuration for our stack
3. GitHub Actions workflow integration
4. Rule customization for accuracy
5. Triage workflow for findings
6. Developer feedback loop
7. Metrics to track program effectiveness
```

**Expected Output:** SAST implementation with CI/CD integration.

---

## 23.4 Dynamic Testing with @dast-expert

### Skill Introduction

The `@dast-expert` skill provides expertise in Dynamic Application Security Testing (DAST). It helps you test running applications for vulnerabilities from an attacker's perspective.

**When to use this skill:**
- Setting up automated security testing
- Configuring DAST scans for APIs
- Integrating DAST in CI/CD
- Interpreting and triaging results

**Key strengths:**
- Experience with DAST tools (ZAP, Burp)
- Knowledge of API security testing
- Understanding of scan optimization

---

### Dynamic Testing Prompts

#### API Security Testing

**Context:** You want to implement automated security testing for your APIs.

```text
@dast-expert Implement automated API security testing:

APIs to test:
- REST API (OpenAPI documented)
- GraphQL API
- 150 endpoints total
- Authentication via JWT

Test requirements:
- OWASP API Security Top 10
- Authentication and authorization testing
- Input fuzzing for injection attacks
- Business logic testing
- Rate limiting verification

Environment:
- Test environment available 24/7
- Need to run in CI/CD pipeline
- Results in SARIF format for integration

Please provide:
1. Tool selection (OWASP ZAP, Nuclei, custom)
2. OpenAPI-based scanning setup
3. Authentication handling configuration
4. Custom security test cases
5. CI/CD integration (GitHub Actions)
6. Result reporting and tracking
7. False positive management
```

**Expected Output:** API security testing implementation.

---

## Best Practices Summary

### Security Architecture
1. **Defense in Depth:** Multiple layers of security
2. **Least Privilege:** Minimal access rights
3. **Secure by Default:** Secure configurations out of the box
4. **Fail Secure:** Deny by default on failure
5. **Threat Modeling:** Regular security design reviews

### Secure Coding
1. **Input Validation:** Validate all inputs
2. **Output Encoding:** Encode outputs for context
3. **Parameterized Queries:** Prevent SQL injection
4. **Secrets Management:** Never hardcode secrets
5. **Error Handling:** Don't leak sensitive info

### Security Testing
1. **Shift Left:** Test early in development
2. **Automation:** SAST/DAST in CI/CD
3. **Coverage:** Test all code paths
4. **Triage:** Prioritize findings effectively
5. **Verification:** Confirm fixes work

---

## Reflection Points

1. **Balance:** How do you balance security with development speed?
2. **Training:** How do you upskill developers on security?
3. **Tool Selection:** How do you choose security tools?
4. **Culture:** How do you build security-aware culture?

---

**Next Chapter:** [Chapter 24: Identity & Access Management →](chapter-24-iam.md)
