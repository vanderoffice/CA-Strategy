# California Enterprise Modernization Plan
## Technical Appendices

**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency
**Date:** January 2026
**Version:** Executive Draft v1.8

---

## Table of Contents

- [Appendix C: Readiness Assessment Framework](#appendix-c-readiness-assessment-framework)
- [Appendix D: Glossary](#appendix-d-glossary)
- [Appendix H: Technology Architecture](#appendix-h-technology-architecture)

---

## Appendix C: Readiness Assessment Framework

> **Note:** The complete Readiness Assessment is a standalone evaluation toolkit maintained separately. This summary provides the strategic framework; the full instrument is available in the [toolkit/readiness-assessment](../toolkit/readiness-assessment/) folder.

### Purpose

The Readiness Assessment enables strategic resource allocation by evaluating department preparedness for modernization. Rather than spreading investment across all 170 departments, the framework identifies which organizations are positioned for success and which need foundational development first.

### Assessment Domains

| Domain | Weight | What It Measures |
|--------|--------|------------------|
| **Leadership & Governance** | 20% | Executive sponsorship, IT alignment, decision structures |
| **Technology Infrastructure** | 20% | Cloud adoption, API maturity, data governance, AI readiness |
| **Organizational Culture** | 15% | Change readiness, digital literacy, innovation appetite |
| **Cybersecurity & Risk** | 15% | SIMM 5300 compliance, security governance |
| **Service Delivery** | 15% | Digital maturity, user-centered design adoption |
| **Funding & Portfolio** | 15% | Project management maturity, Stage 1-ready pipeline |

### Readiness Tiers

| Tier | Score Range | Status | Investment Approach |
|------|-------------|--------|---------------------|
| **1** | 4.0-5.0 | Ready Now | Priority funding for high-impact projects |
| **2** | 3.0-3.9 | Near-Ready | Conditional funding with targeted capability-building |
| **3** | 2.0-2.9 | Developing | Capacity-building grants; not project funding |
| **4** | 1.0-1.9 | Early Stage | Foundational organizational development |

### How It's Used

1. **Department self-assessment** with evidence documentation
2. **TMO validation** with optional site visits
3. **Tier classification** determining funding eligibility
4. **Gap analysis** identifying capability-building priorities
5. **Reassessment** annually or upon major change

### Full Toolkit

| Document | Purpose |
|----------|---------|
| [README](../toolkit/readiness-assessment/README.md) | Framework overview |
| [Assessment Guide](../toolkit/readiness-assessment/readiness-assessment-guide.md) | Methodology and procedures |
| [Assessment Instrument](../toolkit/readiness-assessment/enhanced-readiness-assessment.md) | Complete scoring rubrics |

---

## Appendix D: Glossary

**ADKAR:** Awareness, Desire, Knowledge, Ability, Reinforcement - Change management model

**API:** Application Programming Interface - Software intermediary allowing applications to communicate

**Breakthrough Fund:** California Breakthrough Modernization Fund - Revolving fund with private-sector seed capital and efficiency savings reinvestment

**CDT:** California Department of Technology

**Chief Deputy Director for E3:** Department-level position with operational responsibility for efficiency and effectiveness modernization

**E3:** Enterprise Efficiency and Effectiveness - Operational model creating forcing mechanism for government efficiency through institutional design

**Fellowship:** Governor's Innovation Fellowship Program - 6-month cohort program developing modernization leaders

**Independent Office:** Independent Office of State Data Governance - Cross-branch governance body

**Modular Contracting:** Contract structure limiting individual IT contracts to $15M maximum to reduce risk and increase competition

**ODI:** Office of Data and Innovation

**OKR:** Objectives and Key Results - Goal-setting framework

**PAL:** Project Approval Lifecycle - CDT's four-stage framework for IT project oversight

**Readiness Assessment:** Technology Readiness Assessment Framework - Standardized methodology evaluating department readiness across six domains

**RFI²:** Request for Innovative Ideas - Problem-based procurement method

**Service Mesh:** Decentralized infrastructure layer handling service-to-service communication

**SIMM:** Statewide Information Management Manual - California IT policy

**Strangler Pattern:** Legacy system modernization approach incrementally replacing components

**TMO:** Transformation Management Office - Central coordination function for modernization

**Undersecretary for E3:** Agency-level position with authority over technology, data governance, and performance management

**Zero Trust:** Security model requiring continuous verification, not one-time authentication

---

## Appendix H: Technology Architecture

> **Appendix Summary:** Strategic principles for enterprise technology. For detailed implementation specifications, see the [archive folder](../archive/).

### Standards Hierarchy

California's technology implementations must comply with multiple regulatory frameworks:

| Priority | Framework | Scope |
|----------|-----------|-------|
| 1 | Federal Program Requirements | Systems handling federal data (HIPAA, CJIS, FedRAMP) |
| 2 | California SIMM/SAM | All state IT systems |
| 3 | NIST Frameworks | Security, risk management |
| 4 | Industry Standards | Domain-specific (HL7 FHIR, NIEM) |

### H.0 Architecture Principles

1. **API-First:** All capabilities exposed as documented, versioned APIs
2. **Loosely Coupled:** Services communicate through APIs and events, not direct database access
3. **Hybrid Cloud:** Critical systems on-premises with cloud burst capacity
4. **Zero Trust:** Every request authenticated and authorized; no implicit trust
5. **Data Sovereignty:** Citizen data governed by consent
6. **Strangler Pattern:** Legacy systems wrapped with APIs and gradually replaced
7. **AI-Ready:** Data architecture supports machine learning and automation

### H.1 API Management Strategy

**Centralized Gateway:** Single entry point for all API traffic with consistent security, monitoring, and governance.

**Developer Portal:** Unified catalog of all state government APIs with interactive documentation, self-service provisioning, and sandbox environments.

**API Classification:**

| Tier | Access | Authentication | Rate Limit |
|------|--------|----------------|------------|
| Public | Any developer | API key | 10K/day |
| Partner | Approved orgs | OAuth 2.0 | 100K/day |
| Internal | State systems | Mutual TLS | 1M/day |

**Deployment Targets:** 75 APIs by Year 1, 150 by Year 2, 200 by Year 3

### H.2 Legacy Modernization

**Strangler Pattern Process:**
1. Create API facade wrapping legacy system
2. Build cloud-native microservice for one function
3. Route new requests to microservice
4. Migrate incrementally based on usage
5. Decommission legacy when usage reaches zero

**Sunset Timelines:**
- High technical debt + high criticality: 2-year maximum
- High technical debt + medium criticality: 3-year maximum
- Medium technical debt: 5-year maximum

**Targets:** 40% legacy reduction over 5 years

### H.3 Cloud Strategy Principles

**Hybrid Architecture:** Cloud-first for new development with on-premises redundancy for critical systems.

| Workload Type | Deployment | Rationale |
|---------------|------------|-----------|
| New applications | Cloud-native | Scalability, cost efficiency |
| Critical systems | Hybrid (cloud + on-prem) | Resilience during outages |
| Legacy systems | Gradual migration | Strangler pattern approach |

**Key Requirements:**
- FedRAMP-certified providers only (AWS GovCloud, Azure Government, GCP)
- 99.9% uptime SLA (99.99% for critical systems)
- Quarterly failover testing for hybrid systems

**Target:** 50% of workloads in cloud by Year 3

> **For implementation details:** See [Cloud Implementation Guide](../archive/h3-cloud-implementation-detail.md)

### H.4 Cybersecurity Principles

**Zero Trust Framework:**
- Identity-based access (not network location)
- Least privilege enforcement
- Continuous verification throughout sessions
- Assume breach design

**Encryption Standards:**
- In transit: TLS 1.3 (minimum 1.2)
- At rest: AES-256

**Compliance Frameworks:**
- NIST Cybersecurity Framework
- NIST 800-53 (Moderate or High baseline)
- California SIMM 5300

> **For controls catalog:** See [Security Controls Catalog](../archive/h4-security-controls-catalog.md)

### H.5 AI Governance Principles

**Vision:** Enable staff to create AI-powered workflows using state-approved patterns and shared infrastructure.

**Approved Use Patterns:**

| Pattern | Example Use Cases |
|---------|-------------------|
| Data Analysis | Automated quality checks, natural language queries, anomaly detection |
| Document Processing | Form extraction, classification, summarization, translation |
| Workflow Automation | Case prioritization, routing, status notifications |
| Knowledge Systems | Policy chatbots, decision support, institutional memory |

**Guardrails:**
- Clear labeling of AI-generated content
- Human review for high-stakes decisions
- Documented bias testing
- Explainability requirements
- Full audit logging

> **For deployment process:** See [AI Implementation Guide](../archive/h5-ai-implementation-guide.md)

### H.6 Technology Standards Summary

| Domain | Key Standards |
|--------|---------------|
| **APIs** | REST, JSON, OpenAPI 3.0, OAuth 2.0 |
| **Health Data** | HL7 FHIR, ICD-10, LOINC |
| **Justice Data** | NIEM, CJIS |
| **Security** | NIST 800-53, Zero Trust, TLS 1.3 |
| **Cloud** | FedRAMP, Terraform/IaC |

> **For complete catalog:** See [Technology Standards Catalog](../archive/h6-technology-standards-full.md)

---

> This document is part of the California Enterprise Modernization recommendation. See also:
> - [Executive Summary](../strategy/executive-summary.md) — Start here for an overview
> - [Governance Model](../strategy/governance-model.md) — E3 structure and leadership
> - [Data Governance](../strategy/data-governance.md) — Independent Office and data sharing
> - [Talent Development](../strategy/talent-development.md) — Digital Capability Model, Data Steward Network
> - [Funding & Implementation](../strategy/funding.md) — Breakthrough Fund
> - [Procurement Guide](../strategy/procurement.md) — Modular contracting and RFI²
> - [Templates](templates.md) — Fillable forms
> - [Operational Frameworks](operational-guides.md) — Program frameworks
> - [Budget and Governance](budget-models.md) — Budget models

---

## Version History

| Version | Date | Description | Author |
|---------|------|-------------|--------|
| Executive Draft v1.4 | January 2026 | Streamlined for strategic review; implementation details moved to archive | Claude |
| Executive Draft v1.2 | December 8, 2025 | Initial complete version | Brent Vanderburgh |

---

**Document Version:** Executive Draft v1.8
**Date:** January 2026
**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency

---

*End of California Enterprise Modernization Plan - Technical Appendices*
