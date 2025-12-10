# California Enterprise Modernization Plan
## Technical Appendices

**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency
**Date:** December 8, 2025
**Version:** Executive Draft v1.2

---

## Table of Contents

- [Appendix C: Readiness Assessment Framework](#appendix-c-readiness-assessment-framework)
- [Appendix D: Glossary](#appendix-d-glossary)
- [Appendix H: Technology Architecture Details](#appendix-h-technology-architecture-details)
  - [H.1 API Management Strategy](#h1-api-management-strategy)
  - [H.2 Legacy System Modernization](#h2-legacy-system-modernization)
  - [H.3 Cloud Strategy](#h3-cloud-strategy)
  - [H.4 Cybersecurity Architecture](#h4-cybersecurity-architecture)
  - [H.5 Staff Empowerment for Agentic Data Systems](#h5-staff-empowerment-for-agentic-data-systems)
  - [H.6 Technology Standards Catalog](#h6-technology-standards-catalog)

*Note: Budget and Financial Models (Appendix F) and Performance and Change Management Framework (Appendix G) have been moved to [Budget and Governance Appendices](09-budget-and-governance.md).*

---

## Appendix C: Readiness Assessment Framework

> **Note:** The complete Readiness Assessment Framework has been moved to a dedicated folder for easier use and maintenance. This appendix provides a summary; see the full documentation below.

**Full Documentation:**
- [Readiness Assessment Guide](readiness-assessment/readiness-assessment-guide.md) — Strategic rationale, conceptual foundations, and implementation procedures
- [Enhanced Readiness Assessment](readiness-assessment/enhanced-readiness-assessment.md) — Complete assessment instrument with detailed scoring rubrics

### C.1 Assessment Domains (Summary)

The assessment evaluates six critical domains:

| Domain | Weight | Key Indicators |
|--------|--------|----------------|
| **1. Leadership and Governance** | 20% | Executive sponsorship, IT strategic alignment, governance structures |
| **2. Data and Technology Infrastructure** | 20% | Cloud adoption, API/interoperability, data governance |
| **3. Organizational Culture and Workforce** | 15% | Change readiness, digital literacy, modern technology roles |
| **4. Cybersecurity and Risk** | 15% | Policy compliance (SIMM 5300), security governance |
| **5. Service Delivery** | 15% | Digital service maturity, user-centered design |
| **6. Funding and Portfolio Management** | 15% | Project management maturity, Stage 1-ready projects |

### C.2 Scoring Methodology (Summary)

**Maturity Scale (1-5):**
- **1 (Initial):** Ad hoc, reactive, no formal processes
- **2 (Emerging):** Basic awareness, inconsistent practices
- **3 (Developing):** Defined processes, partial implementation
- **4 (Managed):** Consistent execution, measurable outcomes
- **5 (Optimized):** Continuous improvement, industry-leading

**Readiness Tiers:**
- **Tier 1 (4.0-5.0):** Ready Now — Priority funding for high-impact projects
- **Tier 2 (3.0-3.9):** Near-Ready — Conditional funding with capability-building
- **Tier 3 (2.0-2.9):** Developing — Capacity-building grants, not project funding
- **Tier 4 (1.0-1.9):** Early Stage — Foundational organizational development

*For complete scoring rubrics with detailed examples, see [Enhanced Readiness Assessment](readiness-assessment/enhanced-readiness-assessment.md).*

---

## Appendix D: Glossary

**ADKAR:** Awareness, Desire, Knowledge, Ability, Reinforcement - Change management model

**AGPA:** Associate Governmental Program Analyst - Civil service classification

**API:** Application Programming Interface - Software intermediary allowing applications to communicate

**Breakthrough Fund:** California Breakthrough Modernization Fund - Revolving fund with private-sector seed capital and efficiency savings reinvestment

**CalAcademy:** California training platform managed by ODI for state employee skill development

**CCPA:** California Consumer Privacy Act - State data privacy law

**CDO:** Chief Data Officer

**CDT:** California Department of Technology

**Chief Deputy Director for E3:** Department-level position with operational responsibility for efficiency and effectiveness modernization

**CJIS:** Criminal Justice Information Services - FBI standards for data security and exchange

**DevOps:** Development and Operations - Software development methodology emphasizing collaboration and automation

**DOF:** Department of Finance

**E3:** Enterprise Efficiency and Effectiveness - Operational model creating forcing mechanism for government efficiency through institutional design

**ESB:** Enterprise Service Bus - Centralized integration platform (not adopted; Service Mesh preferred)

**FedRAMP:** Federal Risk and Authorization Management Program - Cloud security certification

**Fellowship:** Governor's Innovation Fellowship Program - 6-month cohort program developing modernization leaders

**FISMA:** Federal Information Security Management Act

**GovOps:** Government Operations Agency

**HL7 FHIR:** Health Level 7 Fast Healthcare Interoperability Resources - Health data exchange standard

**IaaS:** Infrastructure as a Service - Cloud computing model

**Independent Office:** Independent Office of State Data Governance - Cross-branch governance body

**KPI:** Key Performance Indicator

**MDM:** Master Data Management - Practices ensuring uniform, accurate data across systems

**MOU:** Memorandum of Understanding

**NIEM:** National Information Exchange Model - Criminal justice data standard

**NIST:** National Institute of Standards and Technology

**ODI:** Office of Data and Innovation

**OKR:** Objectives and Key Results - Goal-setting framework

**PaaS:** Platform as a Service - Cloud computing model

**PE:** Professional Engineer - Licensed engineering professional

**PG:** Professional Geologist - Licensed geoscience professional

**PIA:** Privacy Impact Assessment

**PPM:** Project Portfolio Management

**RDS:** Research Data Specialist - Civil service classification for data professionals

**RFI²:** Request for Innovative Ideas - Problem-based procurement method

**RFP:** Request for Proposals

**ROI:** Return on Investment

**SaaS:** Software as a Service - Cloud computing model

**Service Mesh:** Decentralized infrastructure layer handling service-to-service communication

**SIMM:** Statewide Information Management Manual - California IT policy

**SLA:** Service Level Agreement

**SME:** Subject Matter Expert

**SSA:** Staff Services Analyst - Civil service classification

**Strangler Pattern:** Legacy system modernization approach incrementally replacing components

**TMO:** Transformation Management Office - Central coordination function for modernization

**Undersecretary for E3:** Agency-level position with authority over technology, data governance, and performance management

**Citizen Journey Team:** Cross-agency team redesigning government services around life events rather than agency boundaries

**Modular Contracting:** Contract structure limiting individual IT contracts to $15M maximum to reduce risk and increase competition

**PAL:** Project Approval Lifecycle - CDT's four-stage framework for IT project oversight (Stage 1: Business Analysis, Stage 2: Alternatives Analysis, Stage 3: Solution Development, Stage 4: Project Readiness)

**Readiness Assessment:** Technology Readiness Assessment Framework - Standardized methodology evaluating department readiness for modernization across six domains

**Senior Fellow:** Graduate of Governor's Innovation Fellowship who remains engaged as mentor, advisor, or transition to permanent E3 position

**Stage 1:** First phase of PAL focusing on business case development, problem definition, and preliminary cost-benefit analysis

**Zero Trust:** Security model requiring continuous verification, not one-time authentication

---

## Appendix H: Technology Architecture Details

> **Appendix Summary:** This appendix provides comprehensive technical architecture guidance across six domains: API Management (H.1), Legacy Modernization (H.2), Cloud Strategy (H.3), Cybersecurity (H.4), Agentic Data Systems (H.5), and Technology Standards (H.6). Use as reference for technical implementation decisions.

This appendix provides comprehensive technical architecture guidance for California's enterprise modernization initiative, incorporating and expanding upon the Technology Standards Catalog.

### Standards Hierarchy

California's technology implementations must comply with multiple regulatory frameworks. The following hierarchy applies when standards conflict or overlap:

| Priority | Framework | Scope | Authority |
|----------|-----------|-------|-----------|
| 1 | **Federal Program Requirements** | Systems handling federal data (HIPAA, CJIS, FedRAMP) | Required for federal funding/data access |
| 2 | **California SIMM/SAM** | All state IT systems | CDT policy; mandatory compliance |
| 3 | **NIST Frameworks** | Security, risk management | Recommended baseline; exceeds SIMM where specified |
| 4 | **Industry Standards** | Domain-specific (HL7 FHIR, NIEM) | Required for interoperability |

**Decision Tree for Compliance:**
1. Does the system handle federal data (health, criminal justice, tax)? → Apply federal program requirements (HIPAA, CJIS, IRS Pub 1075)
2. Does the system require federal authorization? → Apply FedRAMP + SIMM 5300
3. All other systems → Apply SIMM 5300 as baseline; NIST 800-53 controls where SIMM is silent
4. Domain-specific data exchange → Apply relevant interoperability standards (HL7 FHIR for health, NIEM for justice)

### H.1 API Management Strategy

**Centralized API Gateway:**

A unified API gateway provides the entry point for all API traffic, enabling consistent security, monitoring, and governance across California's digital services.

**Core Capabilities:**
- Single entry point for all API traffic (internal and external)
- Enforces authentication, authorization, rate limiting, and logging
- Provides analytics on API usage patterns and performance
- Enables A/B testing and canary deployments for continuous improvement
- Supports versioning and backward compatibility

**Developer Portal:**

A comprehensive developer portal democratizes access to California's government services through well-documented, self-service APIs.

**Features:**
- Unified catalog of all state government APIs (searchable by function, agency, data type)
- Interactive API documentation (OpenAPI/Swagger specifications)
- Self-service API key provisioning with approval workflows
- Code samples and SDKs in multiple languages (Python, JavaScript, Java, C#)
- Sandbox environments for testing without production impact
- Support forums and ticketing system for developer assistance
- Usage dashboards showing consumption and performance

**API Classification:**

California establishes three tiers of APIs with appropriate access controls and service levels:

**Public APIs:** Available to any consumer (developers, researchers, businesses, citizens)
- Minimal authentication (API key registration with email verification)
- Generous rate limits (10,000 requests/day per key)
- Published on public developer portal (developer.ca.gov)
- Examples: Business registry lookup, public datasets, geospatial data, licensing information

**Partner APIs:** Available to approved external organizations (contractors, research institutions, local governments)
- OAuth 2.0 authentication with formal approval process
- Moderate rate limits (100,000 requests/day)
- Formal SLA and dedicated support channels
- Examples: Case management systems, benefit eligibility verification, identity verification

**Internal APIs:** Available only to state government systems and authorized staff
- Mutual TLS authentication with certificate management
- High rate limits (1,000,000 requests/day)
- Internal developer portal with additional security documentation
- Examples: PII data access, financial systems, law enforcement databases

**Deployment Targets:** 75 APIs by Year 1, 150 by Year 2, 200 by Year 3 (final distribution: 50 public, 50 partner, 100 internal)

### H.2 Legacy System Modernization

**Strangler Pattern:**

California adopts the strangler pattern for legacy modernization, avoiding risky "big bang" replacements in favor of incremental transformation while maintaining operational continuity.

**Process:**
1. **Create API Facade:** Wrap legacy system with API layer providing modern interface to old functionality
2. **Build New Microservice:** Develop cloud-native service replicating one discrete function
3. **Route Intelligently:** Direct new requests to microservice while legacy requests continue to old system
4. **Migrate Gradually:** Incrementally shift functionality to new services based on usage patterns and risk assessment
5. **Decommission Legacy:** Remove legacy system components when usage reaches zero and all functionality migrated

**Benefits:**
- **Lower Risk:** No catastrophic cutover; system remains operational throughout migration
- **Continuous Value:** Users experience improvements incrementally rather than waiting years
- **Course Correction:** Ability to pause, adjust strategy, or pivot based on learnings
- **Service Availability:** Maintains citizen access throughout modernization process
- **Resource Flexibility:** Can accelerate or slow migration based on resource availability and competing priorities

**Sunset Timelines:**

California establishes clear timelines for legacy system retirement based on technical debt and criticality:

- **High technical debt + high criticality:** 2-year maximum lifespan from assessment
- **High technical debt + medium criticality:** 3-year maximum
- **Medium technical debt:** 5-year maximum
- **Automatic review trigger:** Systems exceeding planned lifecycle must justify continuation annually

**Modernization Portfolio Targets:**
- **Year 1:** Complete comprehensive assessment across all departments; decommission 10% of legacy systems (40 systems)
- **Year 2:** Decommission 10% more (20% cumulative); complete API facades for 50 high-priority systems
- **Year 3:** Decommission 10% more (30% cumulative); achieve 50% reduction in legacy technical debt
- **Years 4-5:** Achieve 40% total legacy reduction target while maintaining operational stability

### H.3 Cloud Strategy

**Hybrid Cloud with On-Premises Redundancy:**

To protect state business operations in the event of internet outage or cloud service disruption, California adopts a hybrid cloud strategy that maintains on-premises redundancy for critical systems.

**Architecture Principles:**

**Cloud-First for New Development:** All new systems deployed to cloud unless specific exception granted based on:
- Data sovereignty requirements (specific statutes mandating on-premises storage)
- Latency requirements incompatible with cloud architecture
- Cost analysis showing on-premises more cost-effective over 5-year horizon
- Security requirements exceeding cloud provider capabilities

**Critical System Redundancy:** Mission-critical systems maintain on-premises backup capability enabling continued operations during cloud outages.

**Hybrid Connectivity:** Secure, redundant connections between cloud and on-premises infrastructure:
- Multiple dedicated interconnects from different providers
- VPN backup connectivity
- Automatic failover between connectivity paths
- Continuous monitoring of connection health

**Multi-Cloud Strategy:** Avoid single cloud vendor lock-in through multi-cloud deployment where feasible:
- Critical applications deployed across multiple cloud providers
- Containerized workloads enabling portability
- Infrastructure-as-Code supporting multi-cloud deployment
- Careful analysis of multi-cloud complexity vs. flexibility benefits

**Critical Systems Requiring On-Premises Redundancy:**

Examples of systems that must maintain on-premises operational capability:

- **Emergency Services:** 911 dispatch, CAL FIRE coordination, emergency management systems, emergency alert systems
- **Law Enforcement:** Criminal justice information systems, arrest and booking systems, warrant management
- **Public Safety:** Prison management systems, probation and parole tracking, sex offender registry
- **Benefits Delivery:** CalFresh, Medi-Cal eligibility, unemployment insurance payments, child support
- **Critical Infrastructure:** Water management systems, power grid coordination, transportation management
- **Financial Systems:** Payroll processing, tax collection, treasury operations, pension management

**Implementation Strategy:**
- **Primary workloads run in cloud** for scalability, elasticity, and cost efficiency
- **Critical data replicated to on-premises systems** in near-real-time (typically < 5 minute lag)
- **On-premises systems capable of maintaining operations** during internet disruption (degraded capacity acceptable)
- **Regular failover testing** (quarterly minimum) to ensure redundancy effectiveness
- **Automated failback** when cloud connectivity restored, with data reconciliation
- **Clear procedures** for manual intervention if automated failover fails

**Cloud Provider Requirements:**
- FedRAMP-certified cloud providers (AWS GovCloud, Microsoft Azure Government, Google Cloud Platform)
- FISMA compliance appropriate to data sensitivity (Moderate or High)
- StateRAMP (California-specific requirements including data residency, audit access, breach notification)
- SLA guarantees: 99.9% uptime for production services, 99.99% for critical systems
- Geographic redundancy within California or western United States where possible

**Cloud-Native Architecture:**

California adopts modern cloud-native patterns to maximize cloud benefits:

- **Containers and Orchestration:** Docker containers managed by Kubernetes enabling portability and scaling
- **Serverless Computing:** AWS Lambda, Azure Functions, or Google Cloud Functions for event-driven workloads
- **Managed Services:** Leverage cloud provider services reducing operational overhead (managed databases, message queues, caching)
- **Infrastructure as Code (IaC):** Terraform or CloudFormation for repeatable, version-controlled infrastructure
- **Automated Backup and Disaster Recovery:** Cloud-native backup with cross-region replication
- **Auto-Scaling:** Automatically adjust capacity based on demand
- **Immutable Infrastructure:** Replace rather than update infrastructure components

**Migration Approach:**
- **Prioritize high-cost, low-complexity workloads first** (quick wins demonstrating value)
- **Use lift-and-shift for initial migration**, then re-architect for cloud-native over time
- **Implement strong cloud governance:** Cost management, security controls, compliance monitoring, tagging standards
- **Data center consolidation** as workloads migrate, reducing facilities costs
- **Hybrid period of 3-5 years** recognizing gradual transition

**Target:** 50% of workloads in cloud by Year 3, with all critical systems maintaining on-premises redundancy

### H.4 Cybersecurity Architecture

**Zero Trust Architecture:**

California transitions from perimeter-based security to Zero Trust, recognizing that threats exist both outside and inside the network.

**Core Principles:**
- **Identity-based access:** Authentication based on user/service identity, not network location
- **Least privilege:** Minimum necessary access for users and systems
- **Assume breach:** Design assuming attackers have network access
- **Verify explicitly:** Authenticate and authorize every access request
- **Continuous verification:** Re-authenticate throughout session, not just at login

**Implementation:**

**Single Federated Identity System:**
- Unified identity management for all state services and employees
- Multi-factor authentication (MFA) required for all accounts
- Risk-based authentication adjusting requirements based on user behavior and context
- Single sign-on (SSO) reducing password fatigue and improving user experience
- Integration with CalHR for employee lifecycle management

**Access Control:**
- Role-based access control (RBAC) with regular access reviews
- Attribute-based access control (ABAC) for fine-grained permissions
- Just-in-time (JIT) access for privileged operations
- Session recording for auditing high-risk actions

**Network Segmentation:**
- Micro-segmentation limiting lateral movement
- Software-defined perimeter (SDP) controlling network access
- East-west traffic inspection (not just north-south)

**Standards Compliance:**

**NIST Cybersecurity Framework:**
- Identify, Protect, Detect, Respond, Recover functions
- Maturity assessment and roadmap for improvement
- Alignment with federal requirements for interoperability

**NIST 800-53 Security and Privacy Controls:**
- Moderate or High baseline depending on data sensitivity
- Continuous monitoring and control assessment
- Documentation of control implementation and effectiveness

**California-Specific SIMM 5300 Requirements:**
- State-specific security and privacy requirements
- Information security program requirements
- Incident reporting obligations

**Data Protection:**

**Encryption:**
- **In Transit:** TLS 1.3 for all network communications (TLS 1.2 minimum)
- **At Rest:** AES-256 encryption for all databases and file storage
- Key management via Hardware Security Modules (HSM) or cloud key management services
- Regular key rotation following NIST guidelines

**PII Protection:**
- Automatic PII detection and classification
- Redaction of PII in logs and error messages
- Tokenization for PII in non-production environments
- Data loss prevention (DLP) tools monitoring PII movement

**Audit Logging:**
- All data access logged with user, timestamp, data accessed, action performed
- Logs retained for 7 years (or longer for high-sensitivity data)
- Centralized log aggregation and analysis
- Tamper-proof log storage
- Regular review of access patterns and anomalies

**Security Operations:**

**24/7 Security Monitoring:**
- Security Information and Event Management (SIEM) aggregating logs from all systems
- Security Operations Center (SOC) staffed 24/7/365
- Automated threat detection using machine learning
- Integration with threat intelligence feeds

**Automated Threat Detection and Response:**
- Intrusion detection and prevention systems (IDS/IPS)
- Endpoint detection and response (EDR)
- User and entity behavior analytics (UEBA)
- Automated response to common threats (e.g., blocking suspicious IPs)

**Incident Response:**
- Documented incident response plan with defined roles and procedures
- Tabletop exercises quarterly testing response procedures
- Forensic capabilities for investigation
- Communication protocols for breach notification
- Post-incident reviews and lessons learned

**Vulnerability Management:**
- Continuous vulnerability scanning of all systems
- Automated patching for non-critical systems
- Expedited patching for critical vulnerabilities (48-hour target)
- Regular penetration testing (annual for critical systems, biennial for others)
- Bug bounty program encouraging responsible disclosure

**Security Awareness:**
- Annual security training required for all employees
- Monthly security tips and phishing simulations
- Specialized training for developers (secure coding) and administrators (hardening)
- Recognition program for security champions

### H.5 Staff Empowerment for Agentic Data Systems

**Vision:**

Enable California state staff to create AI-powered data workflows using state-approved patterns and shared infrastructure, accelerating data analysis and decision-making while maintaining security, privacy, and quality standards.

**State-Approved Design Patterns:**

California develops and maintains a library of approved agentic design patterns that staff can use to build data workflows safely:

**Data Analysis and Visualization:**
- Automated data quality checking and reporting
- Natural language queries translating to SQL or API calls
- Automated dashboard generation based on data characteristics
- Anomaly detection and alerting

**Document Processing and Extraction:**
- Intelligent form data extraction from PDFs and images
- Document classification and routing
- Summarization of lengthy reports and submissions
- Translation of documents into multiple languages

**Workflow Automation and Case Management:**
- Automated case prioritization based on urgency and complexity
- Intelligent case routing to appropriate staff
- Automated status updates and notifications
- Predictive analytics for case outcomes

**Knowledge Base and Expert Systems:**
- Chatbots answering citizen questions based on policy documents
- Decision support systems incorporating regulations and best practices
- Automated policy impact analysis
- Institutional knowledge capture from retiring staff

**Standards and Guardrails:**

Every agentic design pattern must meet California's requirements for:

**Content Classification:**
- Clear labeling of AI-generated content
- Distinction between AI analysis and human judgment
- Appropriate disclaimers for citizen-facing content

**Accuracy Requirements:**
- Validation thresholds for AI outputs (typically 95%+ accuracy for production use)
- Human review requirements for high-stakes decisions
- Fallback to human judgment when confidence below threshold

**Bias Testing:**
- Documented testing for demographic bias
- Disparate impact analysis where applicable
- Mitigation strategies for identified biases

**Transparency:**
- Explainability of AI decisions (how conclusion reached)
- Data provenance (what data informed the analysis)
- Model cards documenting capabilities and limitations

**Logging and Audit:**
- All AI interactions logged for audit and improvement
- Feedback mechanisms capturing accuracy and usefulness
- Regular review of AI performance and drift

**Version Control:**
- Documented versions of prompts, models, and training data
- Rollback capability when new versions underperform
- A/B testing of model improvements

**Shared Infrastructure:**

California provides shared infrastructure enabling staff to build agentic workflows without individual departments procuring and managing AI systems:

**CDT-Operated Enterprise AI Platform:**
- Centralized access to approved large language models (LLMs)
- Compute resources for training and inference
- Managed services for common AI tasks (OCR, translation, sentiment analysis)
- Unified billing and cost allocation
- Enterprise security and compliance controls

**Departmental Sandboxes:**
- Isolated environments for experimentation and development
- Access to production data copies (anonymized where appropriate)
- Testing framework for validating accuracy and performance
- Promotion pathway from sandbox to pilot to production

**Template Library:**
- Pre-built templates for common use cases
- Customization guidance for department-specific needs
- Community contributions from across state government
- Documentation and training materials

**Deployment Process:**

California establishes a streamlined pathway from idea to production:

1. **Sandbox Development:** Staff build and test agentic workflow in departmental sandbox (days/weeks)
2. **Testing and Validation:** Automated testing validates accuracy, bias, security (1-2 weeks)
3. **Security Scan:** Automated security scanning checks for vulnerabilities and policy compliance (days)
4. **Peer Review:** Review by E3 data governance team ensuring standards compliance (1 week)
5. **Pilot Deployment:** Limited rollout to small user group with monitoring (4-8 weeks)
6. **Production Deployment:** Full rollout with ongoing monitoring and improvement (ongoing)

**Timeline:** Sandbox to production in 8-12 weeks for typical workflow (versus 12-18 months traditional system development)

**Expected Impact:**
- Staff able to automate 20-30% of routine data analysis tasks
- Faster insights enabling more responsive policy and operations
- Reduced backlog of data requests and analysis needs
- Upskilling of workforce in AI literacy and capabilities
- Democratization of data analysis beyond specialized analysts

### H.6 Technology Standards Catalog

#### H.6.1 API Standards

**Required Standards (All APIs):**
- RESTful design following HTTP semantics
- JSON as primary data format (XML supported for legacy compatibility)
- HTTPS only (no unencrypted HTTP)
- Versioning in URL path (e.g., /api/v2/permits)
- Pagination for list endpoints (maximum 100 items per page)
- Standard error responses with HTTP status codes and messages
- OpenAPI 3.0 specification for all APIs

**Authentication and Authorization:**
- OAuth 2.0 for external consumers (citizens, businesses, third-party developers)
- Mutual TLS for high-security government-to-government APIs
- API keys with rotation requirements (maximum 90-day validity)
- Role-based access control (RBAC) aligned with data sensitivity

**Data Protection:**
- TLS 1.3 encryption for all API traffic
- PII redaction in logs and error messages
- Rate limiting to prevent abuse (varies by API classification)
- IP whitelisting for high-sensitivity APIs

**Performance Requirements:**
- < 200ms average response time (95th percentile)
- < 500ms maximum response time (99th percentile)
- 99.95% availability for production APIs
- Graceful degradation under load

#### H.6.2 Data Exchange Standards

**Health and Human Services:**
- HL7 FHIR (Fast Healthcare Interoperability Resources) for health data exchange
- ICD-10 for diagnosis coding
- CPT for treatment and service coding
- LOINC for laboratory observations

**Justice and Corrections:**
- NIEM (National Information Exchange Model) for criminal justice data
- UCR (Uniform Crime Reporting) for crime statistics
- CJIS (Criminal Justice Information Services) standards for security

**Education:**
- CEDS (Common Education Data Standards) for enrollment, graduation, assessment
- SIF (Schools Interoperability Framework) for student information systems

**Geospatial:**
- OGC Standards (Open Geospatial Consortium) for GIS interoperability
- USNG (United States National Grid) for location referencing

#### H.6.3 Cybersecurity Standards

**Framework:**
- NIST Cybersecurity Framework (Identify, Protect, Detect, Respond, Recover)
- NIST 800-53 security and privacy controls
- California SIMM 5300 requirements

**Specific Controls:**
- DISA STIGs for configuration standards
- Zero Trust Architecture principles
- Encryption: TLS 1.3 (transit), AES-256 (at rest)
- Multi-factor authentication for all administrative access
- Security logging and monitoring (SIEM)
- Regular vulnerability scanning and penetration testing
- Incident response plan and tabletop exercises

#### H.6.4 Cloud Standards

**Approved Cloud Providers:**
- AWS GovCloud
- Microsoft Azure Government
- Google Cloud Platform (with appropriate certifications)

**Required Certifications:**
- FedRAMP Authorized (Moderate or High depending on data sensitivity)
- FISMA compliance
- StateRAMP (California-specific requirements)

**Architecture Principles:**
- Hybrid cloud with on-premises redundancy for critical systems
- Cloud-native design (containers, serverless, managed services) where appropriate
- Multi-cloud strategy to avoid vendor lock-in
- Infrastructure as Code (IaC) using Terraform or CloudFormation
- Automated backup and disaster recovery

---

> This document is part of the California Enterprise Modernization recommendation. See also:
> - [Executive Summary](./01-executive-summary.md) — Start here for an overview
> - [Governance Model](./02-governance-model.md) — E3 structure, leadership roles, and data governance
> - [Talent Development](./03-talent-development.md) — Fellowship program and workforce development
> - [Funding & Implementation](./04-funding-implementation.md) — Breakthrough Fund structure
> - [Procurement Guide](./05-procurement-guide.md) — Technology and procurement innovation
> - [Templates](06-templates.md) — Fillable forms and templates
> - [Operational Guides](07-operational-guides.md) — Program guides and frameworks
> - [Budget and Governance Appendices](09-budget-and-governance.md) — Budget models and change management

---

## Version History

| Version | Date | Description | Author |
|---------|------|-------------|--------|
| Executive Draft v1.2 | December 8, 2025 | Removed "Document Owner" footer line | Brent Vanderburgh |
| Executive Draft v1.1 | December 8, 2025 | Updated version numbering and added document owner | Brent Vanderburgh |
| Executive Draft v1.0 | December 2025 | Initial executive draft with Appendices C, D, H (technical standards and architecture) | Brent Vanderburgh |

---

**Document Version:** Executive Draft v1.2
**Date:** December 8, 2025
**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency

---

*End of California Enterprise Modernization Plan - Technical Appendices*
