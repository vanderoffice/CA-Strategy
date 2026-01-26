# H.6 Technology Standards - Complete Catalog

*Archived from appendices/08-technical-appendices.md*

For summary standards, see [Appendix H.6](../appendices/technical-standards.md#h6-technology-standards-summary).

---

## H.6.1 API Standards

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

---

## H.6.2 Data Exchange Standards

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

---

## H.6.3 Cybersecurity Standards

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

---

## H.6.4 Cloud Standards

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
