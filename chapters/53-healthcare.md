# Chapter 53: Healthcare Tech

**Last Updated:** February 5, 2026

---

## Overview

Healthcare technology builds the software that powers modern medicine. From electronic health records to telehealth platforms, healthcare tech requires deep understanding of privacy regulations, interoperability standards, and clinical workflows.

This chapter covers essential skills for building HIPAA-compliant, secure healthcare software.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@healthcare-architect` | Healthcare systems | Clinical platforms |
| `@hipaa-expert` | HIPAA compliance | Privacy requirements |
| `@health-interop-expert` | Health interoperability | HL7, FHIR standards |
| `@telehealth-expert` | Telehealth platforms | Virtual care |

---

## 53.1 Healthcare Architecture with @healthcare-architect

### Skill Introduction

The `@healthcare-architect` skill provides expertise in designing healthcare information systems. It helps you build systems that meet the unique requirements of clinical settings.

**When to use this skill:**
- Building health platforms
- EHR integrations
- Clinical workflow systems
- Patient portals

**Key strengths:**
- Healthcare domain knowledge
- Clinical workflow understanding
- Regulatory awareness

---

### Healthcare Architecture Prompts

#### Designing Telehealth Platform

**Context:** You're building a telehealth platform for a healthcare provider.

```text
@healthcare-architect Design a comprehensive telehealth platform:

Requirements:
- Video consultations (doctor-patient)
- Appointment scheduling
- Patient intake forms
- Prescription management
- EHR integration (Epic, Cerner)
- Payment processing

Clinical features:
- Waiting room functionality
- Multi-party calls (interpreters, family)
- Screen sharing for results review
- Digital prescription writing
- Clinical notes during visit
- Post-visit summaries

Compliance:
- HIPAA compliance mandatory
- BAAs with all vendors
- Audit logging
- Data encryption

Scale:
- 500 providers
- 10K patients/day
- Multi-state licensed providers

Please provide:
1. System architecture design
2. Video infrastructure approach
3. EHR integration patterns
4. HIPAA compliance architecture
5. Scheduling system design
6. Provider and patient apps
7. Clinical documentation flow
8. Disaster recovery for clinical continuity
```

**Expected Output:** Telehealth platform architecture.

---

## 53.2 HIPAA Compliance with @hipaa-expert

### Skill Introduction

The `@hipaa-expert` skill provides expertise in HIPAA compliance for software systems. It helps you implement the technical safeguards required for protected health information (PHI).

**When to use this skill:**
- HIPAA implementation
- Security assessments
- BAA requirements
- Audit preparation

**Key strengths:**
- HIPAA rule expertise
- Technical safeguard implementation
- Audit experience

---

### HIPAA Compliance Prompts

#### Implementing HIPAA Technical Safeguards

**Context:** You need to ensure your healthcare application meets HIPAA requirements.

```text
@hipaa-expert Implement HIPAA technical safeguards:

Application:
- Patient portal with PHI access
- Cloud-hosted (AWS)
- Mobile and web apps
- Integration with EHR systems

PHI types:
- Patient demographics
- Medical records
- Lab results
- Prescription history
- Appointment notes

Current state:
- Basic encryption in place
- No formal access controls
- Limited audit logging
- No formal policies

Requirements:
- Pass OCR audit
- Support third-party security assessment
- Enable BAAs with partners

Please provide:
1. Technical safeguard requirements
2. Access control implementation
3. Encryption specifications
4. Audit logging requirements
5. Transmission security
6. Authentication requirements
7. Breach detection and response
8. Documentation and policies
```

**Expected Output:** HIPAA compliance implementation plan.

---

## 53.3 Health Interoperability with @health-interop-expert

### Skill Introduction

The `@health-interop-expert` skill provides expertise in healthcare data interoperability. It helps you implement HL7, FHIR, and other standards for healthcare data exchange.

**When to use this skill:**
- EHR integrations
- FHIR API development
- Lab data exchange
- Claims processing

**Key strengths:**
- FHIR expertise
- HL7 messaging
- Integration patterns

---

### Health Interoperability Prompts

#### Implementing FHIR API

**Context:** You need to implement a FHIR-compliant API for health data exchange.

```text
@health-interop-expert Design FHIR API implementation:

Requirements:
- FHIR R4 compliance
- Patient access API (21st Century Cures)
- Provider directory
- Clinical data exchange
- Bulk data export

Resources to support:
- Patient
- Practitioner
- Observation
- Condition
- MedicationRequest
- DiagnosticReport
- Encounter

Integration needs:
- Connect to Epic via FHIR
- Connect to Cerner via FHIR
- Support SMART on FHIR authentication

Please provide:
1. FHIR server architecture
2. Resource modeling
3. Search parameter implementation
4. Authorization with SMART
5. Bulk data handling
6. Integration with EHR systems
7. Validation and conformance
8. Testing approach
```

**Expected Output:** FHIR implementation design.

---

## 53.4 Telehealth Development with @telehealth-expert

### Skill Introduction

The `@telehealth-expert` skill provides expertise in virtual care platforms. It helps you build reliable, user-friendly telehealth experiences.

**When to use this skill:**
- Video consultation features
- Remote patient monitoring
- Virtual care workflows
- Provider experience

**Key strengths:**
- Video technology
- Clinical workflows
- User experience

---

### Telehealth Development Prompts

#### Building Virtual Waiting Room

**Context:** You need to build an effective virtual waiting room experience.

```text
@telehealth-expert Design virtual waiting room experience:

Requirements:
- Patients see queue position
- Check-in and intake before visit
- Device and connection testing
- Handle provider delays gracefully
- Multi-language support
- Accessibility (screen readers)

Clinical needs:
- Insurance verification prompt
- Consent collection
- Chief complaint capture
- Vitals entry (if available)
- Medication list update

Technical needs:
- Real-time queue updates
- SMS/push notifications
- Connection quality monitoring
- Failover to phone call

Please provide:
1. Waiting room flow design
2. Queue management system
3. Pre-visit intake process
4. Connection testing approach
5. Notification strategy
6. Accessibility implementation
7. Multi-language support
8. Provider-side queue management
```

**Expected Output:** Virtual waiting room design.

---

## Best Practices Summary

### Healthcare Systems
1. **Privacy First:** PHI protection paramount
2. **Clinical Workflows:** Understand how clinicians work
3. **Reliability:** Healthcare is mission-critical
4. **Interoperability:** Use standards (FHIR)
5. **Accessibility:** Healthcare for all

### HIPAA
1. **Administrative:** Policies and training
2. **Physical:** Physical access controls
3. **Technical:** Encryption, access controls, audit
4. **Breach Response:** Plan and practice
5. **Documentation:** Everything documented

### Interoperability
1. **Standards:** Use FHIR R4
2. **Validation:** Validate all data
3. **Mapping:** Consistent terminology
4. **Testing:** Thorough integration testing
5. **Monitoring:** Track integration health

---

## Reflection Points

1. **Complexity:** Why is healthcare tech uniquely challenging?
2. **Privacy vs Functionality:** How do you balance?
3. **Legacy Systems:** How do you integrate with old EHRs?
4. **User Experience:** How do you design for clinicians with limited time?

---

**Next Chapter:** [Chapter 54: EdTech →](chapter-54-edtech.md)
