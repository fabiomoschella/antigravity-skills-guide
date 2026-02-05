# Chapter 21: Network & Security Infrastructure

**Last Updated:** February 5, 2026

---

## Overview

Network infrastructure forms the backbone of modern distributed systems. From virtual private clouds to load balancers and DNS configuration, understanding network architecture is essential for building secure, performant, and reliable systems.

This chapter covers essential networking skills for cloud and on-premises environments, helping you design and implement robust network architectures.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@network-architect` | Network design | VPC design, topology, connectivity |
| `@load-balancer-expert` | Load balancing | Traffic distribution, HA, performance |
| `@dns-expert` | DNS configuration | Domain management, routing strategies |
| `@firewall-expert` | Security infrastructure | Network security, segmentation |

---

## 21.1 Network Architecture with @network-architect

### Skill Introduction

The `@network-architect` skill provides expertise in designing network architectures for cloud and hybrid environments. It helps you create secure, scalable, and cost-effective network topologies.

**When to use this skill:**
- Designing VPC and subnet architectures
- Planning hybrid cloud connectivity
- Implementing network segmentation
- Troubleshooting network issues
- Optimizing network costs

**Key strengths:**
- Deep knowledge of cloud networking (AWS, Azure, GCP)
- Experience with hybrid and multi-cloud architectures
- Understanding of network security best practices

---

### Network Design Prompts

#### Designing a Multi-Account VPC Architecture

**Context:** You need to design a network architecture for an AWS multi-account organization.

```text
@network-architect Design a scalable VPC architecture for our AWS organization:

Organization structure:
- 20 AWS accounts (dev, staging, prod, shared services)
- Need connectivity between accounts
- Central egress for internet access
- On-premises datacenter connectivity
- Third-party SaaS integrations via VPN

Security requirements:
- Network isolation between environments
- Centralized traffic inspection
- Compliance logging for network flows
- DDoS protection for public services

Traffic patterns:
- Inter-account service communication
- Internet egress for all environments
- Ingress for customer-facing applications
- VPN to on-premises for legacy systems

Please provide:
1. VPC design per account type
2. Connectivity strategy (Transit Gateway, peering)
3. CIDR planning and IP address management
4. Internet egress architecture
5. Hybrid connectivity design
6. Network security (NACLs, Security Groups, firewall)
7. Monitoring and troubleshooting approach
```

**Expected Output:** Complete multi-account network architecture.

---

#### Implementing Zero Trust Networking

**Context:** You want to implement zero trust principles in your network architecture.

```text
@network-architect Help implement zero trust networking for our infrastructure:

Current state:
- Traditional perimeter security (VPN for access)
- Flat network inside VPC
- Services communicate freely within VPC
- Users VPN in and access everything

Goals:
- Verify every connection (no implicit trust)
- Micro-segmentation between services
- Identity-based access (not network-based)
- Continuous verification

Environment:
- Kubernetes workloads on EKS
- Some EC2-based legacy services
- Remote workforce (no VPN ideally)

Please provide:
1. Zero trust principles and implementation
2. Network micro-segmentation approach
3. Service-to-service authentication (mTLS)
4. User access without VPN (BeyondCorp-style)
5. Kubernetes network policies
6. Implementation roadmap
7. Monitoring and verification
```

**Expected Output:** Zero trust implementation plan.

---

## 21.2 Load Balancing with @load-balancer-expert

### Skill Introduction

The `@load-balancer-expert` skill provides expertise in load balancing for high availability and performance. It covers cloud load balancers, application delivery controllers, and traffic management strategies.

**When to use this skill:**
- Designing load balancing architectures
- Implementing SSL termination
- Configuring health checks
- Optimizing application delivery
- Troubleshooting load balancer issues

**Key strengths:**
- Experience with AWS ALB/NLB, Azure Load Balancer, GCP
- Knowledge of Layer 4 vs Layer 7 load balancing
- Understanding of advanced routing strategies

---

### Load Balancing Prompts

#### Designing a Global Load Balancing Strategy

**Context:** You need to distribute traffic globally for a multi-region application.

```text
@load-balancer-expert Design global load balancing for our multi-region deployment:

Requirements:
- Application deployed in US East, EU West, Asia Pacific
- Route users to nearest region
- Handle region failures with automatic failover
- SSL termination at the edge
- Path-based routing for different services

Traffic patterns:
- 60% US, 25% Europe, 15% Asia
- Peak: 100K requests/second globally
- Mix of HTTP API and WebSocket

Application architecture:
- Frontend: React app served from S3/CloudFront
- Backend: Kubernetes services in each region
- Database: Regional with async replication

Please provide:
1. Global load balancing architecture
2. DNS-based vs anycast routing comparison
3. AWS Global Accelerator vs CloudFront strategy
4. Health check and failover configuration
5. SSL certificate management
6. WebSocket support considerations
7. Monitoring and alerting
```

**Expected Output:** Global load balancing architecture with failover.

---

## 21.3 DNS Management with @dns-expert

### Skill Introduction

The `@dns-expert` skill provides expertise in DNS configuration and management. It helps you implement DNS strategies for high availability, performance, and traffic management.

**When to use this skill:**
- Designing DNS architectures
- Implementing DNS-based routing
- Migrating between DNS providers
- Troubleshooting DNS issues
- Optimizing DNS performance

**Key strengths:**
- Deep knowledge of DNS protocols
- Experience with Route 53, Cloudflare, GCP Cloud DNS
- Understanding of advanced routing policies

---

### DNS Management Prompts

#### Implementing DNS for High Availability

**Context:** You need a DNS strategy that supports multi-region failover.

```text
@dns-expert Design DNS configuration for multi-region high availability:

Current setup:
- Primary region: us-east-1
- Secondary region: eu-west-1
- Using Route 53 for DNS
- Multiple services under api.example.com

Requirements:
- Automatic failover on region failure
- Geo-based routing for latency optimization
- 30-second failover time
- Health monitoring at application level

Services:
- api.example.com → main API
- auth.example.com → authentication
- static.example.com → CDN content
- ws.example.com → WebSocket connections

Please provide:
1. DNS architecture design
2. Health check configuration
3. Failover policies and TTL settings
4. Geo-routing configuration
5. Monitoring and alerting
6. Disaster recovery testing approach
```

**Expected Output:** DNS configuration for high availability.

---

## 21.4 Network Security with @firewall-expert

### Skill Introduction

The `@firewall-expert` skill provides expertise in network security, including firewalls, WAFs, and network segmentation. It helps you protect your infrastructure from network-based threats.

**When to use this skill:**
- Designing firewall rules and policies
- Implementing Web Application Firewalls
- Network segmentation for security
- DDoS protection strategies
- Compliance with security requirements

**Key strengths:**
- Experience with cloud and on-premises firewalls
- Knowledge of WAF rule writing
- Understanding of attack patterns and mitigations

---

### Network Security Prompts

#### Implementing WAF Protection

**Context:** You need to protect your web applications from common attacks.

```text
@firewall-expert Implement WAF protection for our web applications:

Applications:
- E-commerce site (customer PII, payment data)
- REST API (JSON-based)
- Admin portal (internal users)

Threats to protect against:
- OWASP Top 10 (SQLi, XSS, etc.)
- Bot attacks and scraping
- DDoS at application layer
- API abuse and rate limiting

Current state:
- No WAF in place
- Some attacks detected in logs
- PCI-DSS compliance required

Tools available:
- AWS WAF or CloudFlare
- Budget conscious

Please provide:
1. WAF architecture design
2. Managed rules vs custom rules approach
3. Rule configuration for OWASP Top 10
4. Bot management strategy
5. Rate limiting configuration
6. Logging and monitoring
7. False positive handling process
```

**Expected Output:** WAF implementation with rule configuration.

---

## Best Practices Summary

### Network Architecture
1. **Segmentation:** Isolate environments and tiers
2. **Documentation:** Maintain network diagrams
3. **IP Planning:** Plan CIDR blocks for growth
4. **Connectivity:** Choose appropriate connectivity methods
5. **Monitoring:** Track network flows and metrics

### Load Balancing
1. **Health Checks:** Comprehensive application-level checks
2. **Connection Draining:** Graceful instance removal
3. **SSL:** Proper certificate management
4. **Logging:** Access logs for troubleshooting
5. **Autoscaling:** Integrate with scaling policies

### Security
1. **Defense in Depth:** Multiple security layers
2. **Least Privilege:** Minimal network access
3. **Encryption:** TLS for all network traffic
4. **Monitoring:** Detect suspicious activity
5. **Updates:** Keep security rules current

---

## Reflection Points

1. **Complexity:** How do you balance security with network complexity?
2. **Multi-Cloud:** How do you design networks spanning multiple clouds?
3. **IPv6:** When should you prioritize IPv6 adoption?
4. **Cost:** How do you optimize network transfer costs?

---

**Next Chapter:** [Chapter 22: Cost Optimization & FinOps →](chapter-22-finops.md)
