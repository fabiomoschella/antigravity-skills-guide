# Chapter 26: Security Operations

**Last Updated:** February 5, 2026

---

## Overview

Security Operations (SecOps) is the practice of monitoring, detecting, and responding to security threats in real-time. A mature SecOps function combines people, processes, and technology to protect the organization from cyber threats.

This chapter covers essential SecOps skills for building detection capabilities, responding to incidents, and maintaining security posture.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@soc-analyst` | Security operations | Detection, triage, investigation |
| `@incident-responder` | Incident handling | Response, containment, recovery |
| `@threat-hunter` | Proactive detection | Threat hunting, hypothesis-driven analysis |
| `@siem-expert` | SIEM configuration | Log analysis, correlation, alerting |

---

## 26.1 Security Operations with @soc-analyst

### Skill Introduction

The `@soc-analyst` skill provides expertise in security operations center (SOC) activities. It helps you detect threats, triage alerts, and investigate security events effectively.

**When to use this skill:**
- Building detection capabilities
- Triaging security alerts
- Investigating suspicious activities
- Creating alert playbooks
- SOC process improvement

**Key strengths:**
- Experience with common attack patterns
- Knowledge of detection techniques
- Understanding of triage methodologies

---

### Security Operations Prompts

#### Building Detection Engineering

**Context:** You want to improve your security detection capabilities.

```text
@soc-analyst Design a detection engineering program:

Current state:
- Basic cloud security monitoring (GuardDuty, SecurityHub)
- SIEM deployed but underutilized
- High false positive rate
- Limited custom detections
- Reactive rather than proactive

Environment:
- AWS cloud infrastructure
- Kubernetes workloads
- SaaS applications (O365, Salesforce)
- 1000 endpoints

Goals:
- Reduce false positives by 80%
- Detect sophisticated attacks (beyond commodity threats)
- Measure detection coverage against MITRE ATT&CK
- Enable threat hunting capabilities

Please provide:
1. Detection engineering framework
2. MITRE ATT&CK coverage analysis approach
3. Detection development lifecycle
4. Priority detection use cases
5. Tuning and false positive reduction
6. Detection testing methodology
7. Metrics and KPIs for detection program
```

**Expected Output:** Detection engineering program design.

---

#### Alert Triage Playbooks

**Context:** You need standardized playbooks for common alert types.

```text
@soc-analyst Create alert triage playbooks for common scenarios:

Alert types to cover:
- Brute force authentication attempts
- Suspicious AWS API activity
- Malware detected on endpoint
- Data exfiltration indicators
- Phishing reported by user
- Privileged access anomaly

For each playbook, include:
- Alert description and context
- Severity classification criteria
- Initial triage steps
- Investigation questions to answer
- Escalation criteria
- Containment actions
- Documentation requirements

Environment context:
- AWS cloud
- Windows/Mac endpoints with EDR
- Okta for identity
- Office 365 for email

Please provide comprehensive playbooks for each alert type.
```

**Expected Output:** Alert triage playbooks for each scenario.

---

## 26.2 Incident Response with @incident-responder

### Skill Introduction

The `@incident-responder` skill provides expertise in handling security incidents from detection to recovery. It helps you respond effectively to threats and minimize business impact.

**When to use this skill:**
- Responding to active incidents
- Creating incident response plans
- Conducting tabletop exercises
- Post-incident analysis
- Improving IR capabilities

**Key strengths:**
- Experience with incident handling
- Knowledge of containment techniques
- Understanding of forensics and evidence

---

### Incident Response Prompts

#### Responding to a Ransomware Incident

**Context:** You've detected potential ransomware activity in your environment.

```text
@incident-responder Guide response to suspected ransomware incident:

Indicators observed:
- Multiple file encryption events on file shares
- Suspicious PowerShell execution on several workstations
- Outbound connections to known malicious IPs
- Ransom note found on one system

Environment:
- Windows Active Directory (500 users)
- AWS cloud workloads
- Network segmentation in place
- Backups: daily, to separate network segment
- No dedicated IR team (IT handles incidents)

Current status:
- Activity first detected 1 hour ago
- Spread appears ongoing
- Critical systems status unknown

Please provide:
1. Immediate containment actions
2. Assessment and scoping steps
3. Evidence preservation priorities
4. Communication plan (internal/external)
5. Eradication approach
6. Recovery sequencing
7. Post-incident activities
```

**Expected Output:** Ransomware incident response guide.

---

#### Creating Incident Response Plan

**Context:** You need a comprehensive incident response plan.

```text
@incident-responder Create an incident response plan for our organization:

Organization context:
- 500 employees, technology company
- AWS cloud infrastructure
- Handles customer PII and financial data
- 24/7 operations requirement
- Compliance: SOC 2, GDPR

IR team:
- 3 security engineers (not dedicated IR)
- IT operations team available
- Legal and communications available

Requirements:
- Align with NIST Incident Response framework
- Clear escalation paths
- Communication templates
- Regulatory notification requirements
- Integration with existing runbooks

Please provide:
1. IR plan structure and contents
2. Incident classification and severity
3. Roles and responsibilities
4. Communication procedures
5. External party engagement (legal, forensics, LE)
6. Post-incident review process
7. Plan testing and update schedule
```

**Expected Output:** Comprehensive incident response plan.

---

## 26.3 Threat Hunting with @threat-hunter

### Skill Introduction

The `@threat-hunter` skill provides expertise in proactive threat detection through hypothesis-driven investigation. It helps you find threats that evade automated detection.

**When to use this skill:**
- Developing threat hunting hypotheses
- Creating hunting procedures
- Analyzing threat intelligence
- Validating detection coverage
- Uncovering hidden threats

**Key strengths:**
- Knowledge of adversary techniques
- Experience with hunting methodologies
- Understanding of data analysis

---

### Threat Hunting Prompts

#### Developing Threat Hunting Program

**Context:** You want to establish proactive threat hunting capabilities.

```text
@threat-hunter Design a threat hunting program:

Environment:
- AWS cloud (100+ accounts)
- 5000 endpoints (EDR deployed)
- SIEM with 90 days retention
- CloudTrail, VPC Flow Logs, DNS logs available

Team:
- 2 security analysts (limited hunting experience)
- Monthly time allocation: 40 hours total

Goals:
- Proactive identification of threats
- Improve detection capabilities based on findings
- Measure hunting effectiveness

Threat actors of concern:
- Financially motivated attackers
- Insider threats
- APT groups (based on industry targeting)

Please provide:
1. Threat hunting methodology
2. Hypothesis development process
3. Initial hunting focuses (priority areas)
4. Data requirements and preparation
5. Hunting tooling recommendations
6. Metrics and success criteria
7. Hunting calendar/schedule
```

**Expected Output:** Threat hunting program framework.

---

## 26.4 SIEM Configuration with @siem-expert

### Skill Introduction

The `@siem-expert` skill provides expertise in Security Information and Event Management systems. It helps you collect, analyze, and correlate security events effectively.

**When to use this skill:**
- SIEM deployment and configuration
- Log source integration
- Correlation rule development
- Dashboard and reporting creation
- SIEM optimization

**Key strengths:**
- Experience with major SIEM platforms
- Knowledge of log sources and parsing
- Understanding of correlation logic

---

### SIEM Implementation Prompts

#### Optimizing SIEM Detection

**Context:** Your SIEM is generating too much noise and missing real threats.

```text
@siem-expert Optimize our SIEM for better detection:

Current state:
- Splunk Enterprise
- 500GB/day log ingestion
- 200+ alerts firing daily
- 90% false positive rate estimated
- SOC overwhelmed, ignoring most alerts

Log sources:
- AWS CloudTrail (all accounts)
- Windows event logs (security)
- Endpoint detection (CrowdStrike)
- Firewall logs
- Web proxy logs
- Office 365 audit logs

Issues:
- Alert fatigue causing real threats to be missed
- Poorly tuned correlation rules
- No baseline for normal behavior
- High storage costs

Please provide:
1. Alert assessment and prioritization
2. Tuning strategy for each alert category
3. Baseline development approach
4. Detection coverage improvement
5. Dashboard design for SOC efficiency
6. Log ingestion optimization (cost)
7. Metrics to track improvement
```

**Expected Output:** SIEM optimization plan.

---

## Best Practices Summary

### Detection
1. **Layered Detection:** Multiple detection techniques
2. **High Fidelity:** Prioritize quality over quantity
3. **Threat Intelligence:** Incorporate IOCs and TTPs
4. **Testing:** Regular detection testing
5. **Coverage:** Map to MITRE ATT&CK

### Response
1. **Preparation:** Plans before incidents
2. **Practice:** Regular tabletops and exercises
3. **Containment:** Fast containment capabilities
4. **Communication:** Pre-defined templates and channels
5. **Learning:** Post-incident reviews

### Hunting
1. **Hypothesis-Driven:** Structured approach
2. **Intelligence-Led:** Based on threat landscape
3. **Document:** Record all hunting activities
4. **Improve:** Feed findings back to detection
5. **Metrics:** Track hunting effectiveness

---

## Reflection Points

1. **Automation:** What SecOps tasks should be automated vs human?
2. **Burnout:** How do you prevent SOC burnout?
3. **Metrics:** How do you measure SecOps effectiveness?
4. **Skills:** What skills are most important for SecOps roles?

---

**Next Chapter:** [Chapter 27: Cryptography & Data Protection →](chapter-27-cryptography.md)
