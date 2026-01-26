# H.4 Cybersecurity Architecture - Controls Catalog

*Archived from appendices/08-technical-appendices.md*

For strategic principles, see [Appendix H.4](../appendices/technical-standards.md#h4-cybersecurity-principles).

---

## Zero Trust Implementation Details

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

---

## Data Protection Controls

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

---

## Security Operations

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
