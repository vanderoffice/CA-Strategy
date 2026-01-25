# AI Coding Assistant Deployment Plan

**A comprehensive guide for safely deploying Claude Code in California state government.**

> **Document Status**: All regulatory and vendor claims are hyperlinked to official sources for verification. See [Appendix D](#appendix-d-verified-sources--references) for complete source list.

**Version:** Executive Draft v1.0
**Date:** January 2026
**Prepared for:** California Department of Technology, State Agencies

---

## Executive Summary

This plan addresses deploying Claude Code (an AI coding assistant) in California state government. While developed initially for the **State Water Resources Control Board (SWRCB)** as a pilot, the framework applies to any state agency.

**Key Finding**: Claude Code CAN be deployed safely, but deployments involving benefits/services systems or critical infrastructure require the most stringent controls and mandatory CDT consultation.

**Critical First Step**: Verify whether your agency has a SIEM (Security Information and Event Management) system. If not, one must be established or leveraged from another state agency before deployment.

### Immediate Action Items (Week 1)

| # | Action | Owner | Notes |
|---|--------|-------|-------|
| 1 | Confirm SIEM availability | IT Security | Required for audit logging |
| 2 | Identify executive sponsor | Leadership | Must be CIO or direct report |
| 3 | Schedule CDT consultation | Sponsor/CIO | Mandatory for HIGH RISK classification |
| 4 | Review budget for Enterprise license | Finance | ~$20/user/month estimated |
| 5 | Identify 10-15 pilot developers | Department leads | For initial pilot group |

---

## Table of Contents

1. [Understanding the Risks](#1-understanding-the-risks)
2. [California-Specific Requirements](#2-california-specific-requirements)
3. [Technical Security Controls](#3-technical-security-controls)
4. [Data Protection Framework](#4-data-protection-framework)
5. [Governance & Policy Framework](#5-governance--policy-framework)
6. [Procurement & Vendor Management](#6-procurement--vendor-management)
7. [Training & Awareness Program](#7-training--awareness-program)
8. [Monitoring & Incident Response](#8-monitoring--incident-response)
9. [Implementation Roadmap](#9-implementation-roadmap)
10. [Verification & Testing Plan](#10-verification--testing-plan)

---

## 1. Understanding the Risks

### 1.1 The Attribution Problem

**The Issue**: When Claude Code runs a command (like a network scan), it uses the employee's credentials and appears to come from their computer. Network monitors cannot tell if a human or the AI initiated the action.

**Why This Matters**:
- Security teams can't investigate incidents accurately
- Audit trails become unreliable
- Compliance reporting is compromised
- Accountability becomes unclear

**Solution**: Implement logging at the Claude Code level that tags all AI-initiated actions, then correlate with network logs.

### 1.2 Security Risks

| Risk | What Could Happen | Severity |
|------|-------------------|----------|
| **Credential Exposure** | AI sees API keys, passwords in code and sends them to Anthropic's servers | HIGH |
| **Malicious Code Generation** | AI suggests code with security vulnerabilities (happens ~50% of the time in studies) | HIGH |
| **Prompt Injection** | Attacker hides instructions in filenames or GitHub issues that trick the AI | HIGH |
| **Data Exfiltration** | Sensitive government data sent to AI provider as part of prompts | HIGH |
| **Supply Chain Attack** | AI suggests installing malicious software packages | MEDIUM |

### 1.3 Operational Risks

| Risk | What Could Happen | Severity |
|------|-------------------|----------|
| **Shadow AI** | Employees use unauthorized AI tools, bypassing controls | HIGH |
| **Over-reliance** | Staff stop thinking critically about AI suggestions | MEDIUM |
| **Code Quality Decline** | More code produced, but harder to maintain | MEDIUM |
| **Knowledge Erosion** | Staff lose skills when AI does the work | LOW |

### 1.4 Legal & Compliance Risks

| Risk | What Could Happen | Severity |
|------|-------------------|----------|
| **CCPA Violation** | Personal data processed without proper safeguards | HIGH |
| **Copyright Issues** | AI generates code copied from copyrighted sources | MEDIUM |
| **License Violations** | AI suggests code with incompatible open-source licenses | MEDIUM |
| **Liability Uncertainty** | Unclear who is responsible when AI-generated code fails | MEDIUM |

---

## 2. California-Specific Requirements

> All claims in this section are hyperlinked to official sources for verification.

### 2.1 Mandatory Compliance Framework

#### Executive Order N-12-23 (September 6, 2023)
**Source**: [Official Executive Order PDF](https://www.gov.ca.gov/wp-content/uploads/2023/09/AI-EO-No.12-_-GGN-Signed.pdf) | [GovOps Summary](https://www.govops.ca.gov/generative-ai-genai-executive-order/)

- Must establish GenAI governance structure
- Must train workforce on responsible AI use
- Must inventory all high-risk AI uses
- Must report to CDT (California Department of Technology)
- Legal counsel must evaluate AI impact on regulatory issues

#### CDT GenAI Procurement Guidelines (March 2024, updated July 2024)
**Source**: [GenAI Guidelines PDF](https://cdt.ca.gov/wp-content/uploads/2024/07/3a-GenAI-Guidelines.pdf) | [Technology Letter 24-01](https://cdt.ca.gov/policy/technology-letters/technology-letter-24-01/)

- Risk classification required (Low/Moderate/High) via [SIMM 5305-F GenAI Risk Assessment](https://cdt.ca.gov/policy/simm/)
- CDT consultation **mandatory** for Moderate/High risk procurements
- Executive-level accountability (CIO/AIO responsible)
- All GenAI uses must be inventoried and reported to CDT
- GenAI Special Provisions required in contracts for moderate/high-risk

#### Data Residency (SAM Section 4983.1)
**Source**: [SAM 4983.1 Cloud Computing Policy](https://www.dgs.ca.gov/Resources/SAM/TOC/4900/4983-1)

- **Physical data storage must be in Continental United States**
- Remote access from outside continental US prohibited without State CISO approval
- California Cloud Services Assessment (CCSA) required before new cloud accounts
- Exit strategy required for all cloud services

#### Assembly Bill 302 (Signed October 13, 2023)
**Source**: [AB 302 Full Text](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202320240AB302)

- CDT must maintain comprehensive inventory of all high-risk automated decision systems
- Annual reporting to legislature required
- Must document: decisions system makes, intended benefits, alternatives, research on efficacy

#### SB 53 - Transparency in Frontier AI Act (Effective January 1, 2026)
**Source**: [SB 53 Full Text](https://leginfo.legislature.ca.gov/faces/billTextClient.xhtml?bill_id=202520260SB53)

- Applies to "frontier models" (>10²⁶ FLOPs) and large developers (>$500M revenue)
- Requires public safety frameworks, transparency reports, incident reporting
- **Note**: This primarily affects AI vendors (Anthropic, OpenAI, etc.), not government users

#### AB 2013 - Training Data Transparency Act (Effective January 1, 2026)
**Source**: [AB 2013 Full Text](https://leginfo.legislature.ca.gov/faces/billTextClient.xhtml?bill_id=202320240AB2013)

- AI developers must disclose training data sources, ownership, and composition
- Government procurement should verify vendor compliance with this disclosure

#### CCPA/CPRA Automated Decision-Making Technology Regulations
**Source**: [CPPA Final Regulations](https://cppa.ca.gov/announcements/2025/20250923.html)

- **Regulations effective January 1, 2026**
- ADMT defined as technology that "replaces or substantially replaces human decisionmaking"
- Requires: consent/opt-out procedures, detailed disclosures, risk assessments
- **Relevance**: If Claude Code assists in decisions affecting Californians (permits, benefits), these regulations may apply

### 2.2 Risk Classification

Based on CDT guidelines, determine classification:

| System Type | Classification | CDT Consultation |
|-------------|---------------|------------------|
| Internal tools, non-sensitive | LOW | Optional |
| Public-facing websites | MODERATE | Recommended |
| Benefits/services systems | **HIGH** | **Mandatory** |
| Critical infrastructure | **HIGH** | **Mandatory** |
| Infrastructure/DevOps access | **HIGH** | **Mandatory** |

**What HIGH RISK means**:
- CDT consultation is **mandatory** before procurement
- Executive-level (CIO) sign-off required
- Enhanced monitoring and controls
- More frequent audits
- May require additional security assessment

### 2.3 Required Assessments Before Deployment

| Assessment | Required By | Timeline |
|------------|-------------|----------|
| Risk Classification | CDT Guidelines | Before procurement |
| Privacy Impact Assessment | CCPA Regulations | Before deployment |
| Equity Impact Assessment | CDT Guidelines | Before deployment |
| CDT Consultation | CDT Guidelines | Before contract signing |
| Security Assessment | SAM/SIMM | Before deployment |

---

## 3. Technical Security Controls

### 3.1 Authentication & Access Control

**Requirement**: Only authorized employees can use Claude Code, with activity tied to their identity.

```
┌─────────────────────────────────────────────────────┐
│  State Identity Provider (SSO/SAML)                 │
│  ↓                                                  │
│  Claude Code Enterprise (linked to state accounts)  │
│  ↓                                                  │
│  Role-Based Access (by department/job function)     │
│  ↓                                                  │
│  Individual Session Logging (all actions tracked)   │
└─────────────────────────────────────────────────────┘
```

**Controls**:
- Single Sign-On through state identity provider
- Multi-factor authentication required
- Automatic session timeout
- Access revocation when employee leaves

### 3.2 Permission Restrictions

**Requirement**: Claude Code should only be able to do what's necessary, nothing more.

**Recommended Permission Configuration**:

```json
{
  "permissions": {
    "deny": [
      "Bash(curl:*)",
      "Bash(wget:*)",
      "Bash(nc:*)",
      "Bash(telnet:*)",
      "Bash(nmap:*)",
      "Bash(rm -rf:*)",
      "Bash(sudo:*)",
      "Read(.env)",
      "Read(**/secrets/**)",
      "Read(**/credentials/**)",
      "Read(**/*.pem)",
      "Read(**/*.key)",
      "WebFetch(*)"
    ],
    "allow": [
      "Bash(npm run:*)",
      "Bash(npm test:*)",
      "Bash(python -m pytest:*)",
      "Bash(git status)",
      "Bash(git diff:*)",
      "Bash(git log:*)",
      "Read(src/**)",
      "Edit(src/**)"
    ]
  }
}
```

**Plain Language**:
- **BLOCKED**: Network tools, destructive commands, accessing secrets
- **ALLOWED**: Running tests, viewing code changes, editing source files

### 3.3 Audit Logging & SIEM Integration

**CRITICAL PREREQUISITE**: Verify whether your agency has a SIEM before proceeding.

**If no SIEM exists**:

| Option | Pros | Cons |
|--------|------|------|
| Use CDT's statewide SIEM (if available) | No new procurement, standardized | May require coordination |
| Deploy agency-specific SIEM | Full control | Cost, time to implement |
| Use cloud-native logging (AWS CloudWatch, etc.) | Quick setup | Less correlation capability |
| Partner with another agency | Shared cost | Governance complexity |

**What Gets Logged** (via [OpenTelemetry](https://code.claude.com/docs/en/monitoring-usage)):
- Every command Claude Code executes
- Every file it reads or modifies
- Every prompt the user sends
- Success/failure of each action
- Timestamps and session IDs
- Cost and token usage

**Integration Architecture**:
```
Claude Code → OpenTelemetry → State SIEM (Splunk/Elastic)
                              ↓
                         Security Dashboard
                              ↓
                         Alert Rules
```

**Configuration**:
```bash
# Environment variables for audit logging
CLAUDE_CODE_ENABLE_TELEMETRY=1
OTEL_METRICS_EXPORTER=otlp
OTEL_LOGS_EXPORTER=otlp
OTEL_EXPORTER_OTLP_ENDPOINT=https://siem.ca.gov:4317
OTEL_LOG_USER_PROMPTS=1
OTEL_RESOURCE_ATTRIBUTES="department=YOUR_DEPT,agency=YOUR_AGENCY"
```

**This Solves the Attribution Problem**: Network logs + Claude Code logs = complete picture of who did what and whether AI was involved.

### 3.4 Network Controls

**Architecture**:
```
┌─────────────────────────────────────────────────────┐
│  Developer Workstation                              │
│  └─ Claude Code                                     │
│      └─ Proxy (state-controlled)                    │
│          └─ Firewall Rules                          │
│              ├─ ALLOW: api.anthropic.com            │
│              ├─ ALLOW: github.com (if approved)     │
│              ├─ ALLOW: npm/pip registries           │
│              └─ BLOCK: Everything else              │
└─────────────────────────────────────────────────────┘
```

### 3.5 Infrastructure/DevOps Special Controls

**Why Extra Controls**: Allowing AI to assist with infrastructure work requires additional safeguards.

**Recommended Restrictions for Infrastructure Work**:

```json
{
  "permissions": {
    "deny": [
      "Bash(terraform destroy:*)",
      "Bash(kubectl delete:*)",
      "Bash(docker rm:*)",
      "Bash(aws ec2 terminate:*)",
      "Bash(*--force*)",
      "Bash(shutdown:*)",
      "Bash(iptables:*)",
      "Bash(systemctl stop:*)"
    ],
    "allow": [
      "Bash(terraform plan:*)",
      "Bash(kubectl get:*)",
      "Bash(kubectl describe:*)",
      "Bash(docker ps:*)",
      "Bash(docker logs:*)",
      "Bash(aws ec2 describe:*)",
      "Bash(systemctl status:*)"
    ]
  }
}
```

**Plain Language**:
- **BLOCKED**: Anything that deletes, stops, or modifies running infrastructure
- **ALLOWED**: Viewing, planning, and describing infrastructure (read-only operations)

**Additional Controls for Infrastructure**:
1. **Separate environment**: Claude Code for infrastructure should run in isolated environment
2. **No production access**: AI should only work in dev/staging, never production
3. **Change approval**: All infrastructure changes require human approval AND peer review
4. **Time-based restrictions**: Consider limiting infrastructure AI use to business hours only

### 3.6 Security Hooks (Policy Enforcement)

**Example: Pre-Execution Validation Hook**:
```bash
#!/bin/bash
# This script runs BEFORE Claude Code executes any command
# Exit code 2 = BLOCK the action

command=$(echo "$INPUT" | jq -r '.tool_input.command')

# Check for sensitive patterns
if [[ "$command" =~ (password|secret|key|token|credential) ]]; then
  logger -t CLAUDE_CODE_BLOCK "Blocked sensitive command: $command"
  echo "Policy violation: Command may expose sensitive data" >&2
  exit 2
fi

# Log all commands for audit
logger -t CLAUDE_CODE "User: $USER Executing: $command"
exit 0
```

### 3.7 Benefits/Services Systems Controls

For agencies managing permits, benefits, or rights affecting Californians:

**Required Controls**:

1. **No automated decisions**: Claude Code must NOT generate code that automatically approves/denies permits without human review

2. **Audit trail for decision logic**: Any code affecting decisions must be documented with comments explaining the logic

3. **Equity review**: Before deploying AI-assisted code changes:
   - Review for potential disparate impact
   - Consider effects on vulnerable communities
   - Document equity assessment

4. **Testing requirements**: AI-generated code for benefits systems requires:
   - Unit tests for all decision paths
   - Edge case testing
   - Regression testing against historical decisions
   - Human review of test results

**Recommended Phased Approach**:

| Phase | Systems | Timeline |
|-------|---------|----------|
| 1 | Internal business systems | Months 1-3 |
| 2 | Public-facing websites | Months 4-6 |
| 3 | Infrastructure/DevOps (read-only) | Months 7-9 |
| 4 | Benefits/services systems | Month 10+ (after proven safety) |

---

## 4. Data Protection Framework

### 4.1 Data Classification for Claude Code Use

| Classification | Can Use with Claude Code? | Conditions |
|----------------|---------------------------|------------|
| **Public** | Yes | Standard controls |
| **Internal** | Limited | Enhanced logging, no sensitive fields |
| **Confidential** | No | Zero Data Retention mode only |
| **Restricted** | No | Not permitted |

### 4.2 What Data Goes to Anthropic?

When you use Claude Code, the following is sent to Anthropic's servers:

**SENT**:
- Your prompts/questions
- Code snippets you ask about
- File contents Claude reads
- Command outputs

**NOT SENT** (with Enterprise):
- Data is NOT used for training
- 30-day retention (or Zero Data Retention available)

### 4.3 Preventing Sensitive Data Exposure

**Technical Controls**:

1. **Pre-prompt scanning**: Hook that checks prompts for sensitive patterns
```bash
# Block prompts containing SSN, credit card, etc.
if echo "$PROMPT" | grep -qE '[0-9]{3}-[0-9]{2}-[0-9]{4}'; then
  echo "SSN detected - prompt blocked"
  exit 2
fi
```

2. **File access restrictions**: Block Claude from reading sensitive files
```json
{
  "permissions": {
    "deny": [
      "Read(**/*.env)",
      "Read(**/config/secrets/**)",
      "Read(**/credentials/**)"
    ]
  }
}
```

3. **Data Loss Prevention (DLP)**: Network-level monitoring for sensitive data leaving workstations

### 4.4 Data Residency Compliance

**Verification Required**:
- Anthropic API servers must be in Continental US
- Confirm with Anthropic legal/compliance team
- Document in risk assessment

**Alternative if Needed**:
- AWS Bedrock (Claude available, runs in US regions)
- Google Vertex AI (Claude available, runs in US regions)
- Both offer more geographic control

---

## 5. Governance & Policy Framework

### 5.1 Organizational Structure

```
┌─────────────────────────────────────────────────────┐
│  Executive Sponsor (CIO or Designee)                │
│  - Accountable for all GenAI use                    │
│  - Signs off on risk assessments                    │
│  - Reports to CDT                                   │
├─────────────────────────────────────────────────────┤
│  AI Governance Committee                            │
│  - IT Security, Legal, Privacy, HR representatives  │
│  - Reviews use cases and risks                      │
│  - Approves new deployments                         │
├─────────────────────────────────────────────────────┤
│  GenAI Subject Matter Expert                        │
│  - Day-to-day oversight                             │
│  - Monitors usage and compliance                    │
│  - Handles incidents                                │
├─────────────────────────────────────────────────────┤
│  Department Leads                                   │
│  - Approve use within their teams                   │
│  - Ensure staff training completed                  │
│  - Report issues upward                             │
└─────────────────────────────────────────────────────┘
```

### 5.2 Acceptable Use Policy

**Required Policy Elements**:

1. **Who Can Use It**
   - Only employees who have completed training
   - Only for approved job functions
   - Personal use prohibited

2. **What It Can Be Used For**
   - Writing and reviewing code
   - Debugging and troubleshooting
   - Documentation assistance
   - Learning and skill development

3. **What It CANNOT Be Used For**
   - Processing personal information of Californians
   - Accessing confidential or restricted data
   - Making automated decisions affecting people
   - Bypassing security controls or reviews

4. **Required Practices**
   - Review all AI-generated code before using
   - Never paste sensitive data into prompts
   - Report any suspicious AI behavior
   - Document AI assistance in code comments

### 5.3 Code Review Requirements

**AI-Generated Code Review Checklist**:

- [ ] Security vulnerabilities checked (SQL injection, XSS, etc.)
- [ ] No hardcoded credentials or secrets
- [ ] Proper input validation
- [ ] Error handling appropriate
- [ ] License compliance verified
- [ ] Aligns with state coding standards
- [ ] Human reviewer understands all changes

**Mandatory Human Review**: All AI-generated code must be reviewed by a human developer before deployment.

### 5.4 Documentation Requirements

| Document | Contents | Update Frequency |
|----------|----------|------------------|
| AI Use Inventory | All Claude Code deployments, users, use cases | Quarterly |
| Risk Assessment | Identified risks and mitigations | Annually |
| Incident Log | Any security or compliance issues | As needed |
| Training Records | Who has been trained, when | Ongoing |
| Audit Reports | Usage statistics, compliance status | Monthly |

---

## 6. Procurement & Vendor Management

### 6.1 Required Contract Provisions

Per CDT GenAI Special Provisions, contracts must include:

1. **Data Protection**
   - Contractor cannot use state data for AI training
   - Data must remain in US
   - Encryption in transit and at rest required

2. **Security Requirements**
   - State access to security logs at no cost
   - Breach notification within 24 hours
   - Annual security assessments

3. **AI-Specific Terms**
   - AI outputs identified/watermarked
   - No discriminatory or harmful outputs
   - IP warranties for training data

4. **Compliance**
   - SOC 2 Type II certification
   - Willingness to support state audits
   - Subcontractor same obligations

### 6.2 Vendor Assessment Checklist

Before signing with Anthropic (or any AI vendor):

- [ ] SOC 2 Type II report reviewed
- [ ] Data Processing Agreement signed
- [ ] Data residency confirmed (US only)
- [ ] Training data exclusion confirmed
- [ ] Retention policy acceptable
- [ ] Incident response procedures documented
- [ ] Enterprise features available (SSO, audit logs, etc.)
- [ ] Contract includes GenAI Special Provisions

### 6.3 Anthropic-Specific Considerations

> All claims below are linked to official Anthropic sources for verification.

**Verified Compliance** (Source: [Anthropic Trust Center](https://trust.anthropic.com/) | [Privacy Center](https://privacy.claude.com/)):
- SOC 2 Type II certified ([Certifications](https://privacy.claude.com/en/articles/10015870-what-certifications-has-anthropic-obtained))
- ISO 27001:2022 certified
- ISO/IEC 42001:2023 certified (AI-specific)
- HIPAA-ready (BAA available)

**Data Handling** (Source: [Data Usage](https://code.claude.com/docs/en/data-usage)):
- Commercial users: **Data NOT used for training** unless explicitly opted in
- Default retention: 30 days
- Zero Data Retention (ZDR) available for Enterprise API customers ([ZDR Info](https://privacy.claude.com/en/articles/8956058-i-have-a-zero-data-retention-agreement-with-anthropic-what-products-does-it-apply-to))

**Enterprise Features** (Source: [Security Docs](https://code.claude.com/docs/en/security)):
- SAML 2.0 and OIDC SSO supported
- SCIM provisioning for automated user management
- Role-based access control (RBAC)
- Audit logging
- Custom data retention controls

**Must Verify with Anthropic Sales Before Procurement**:
- Exact data center locations (must confirm Continental US per SAM 4983.1)
- Specific retention periods under government contract
- Indemnification terms for AI-generated code
- California government-specific contract terms availability
- Pricing for government entities

---

## 7. Training & Awareness Program

### 7.1 Required Training Modules

**Module 1: AI Basics for Government** (All Staff)
- What AI can and cannot do
- Risks of AI tools
- State policy on AI use
- How to report concerns

**Module 2: Claude Code User Training** (Developers)
- How to use Claude Code safely
- What data can/cannot be shared
- How to review AI-generated code
- Security best practices

**Module 3: AI Security for IT Staff** (IT/Security)
- Prompt injection attacks
- Detection and response
- Monitoring and alerting
- Incident procedures

**Module 4: AI Governance** (Leadership)
- Compliance requirements
- Risk management
- Reporting obligations
- Accountability structure

### 7.2 Training Schedule

| Audience | Training | When | Renewal |
|----------|----------|------|---------|
| All developers | Module 1 + 2 | Before access granted | Annual |
| IT/Security staff | Module 1 + 3 | Before deployment | Annual |
| Leadership | Module 1 + 4 | Before deployment | Annual |
| New employees | Appropriate modules | Onboarding | - |

---

## 8. Monitoring & Incident Response

### 8.1 Monitoring Dashboard

**Key Metrics to Track**:

| Metric | Why It Matters | Alert Threshold |
|--------|----------------|-----------------|
| Commands executed per user | Detect unusual activity | >100/day |
| Failed permission requests | Policy violations | >10/day |
| Sensitive pattern matches | Data exposure attempts | Any |
| Error rates | System health | >5% |
| Cost per department | Budget management | Budget threshold |

### 8.2 Alert Rules

**Critical Alerts** (Immediate response):
- Attempt to access credential files
- Network scan commands detected
- Sensitive data patterns in prompts
- Multiple rapid permission failures

**Warning Alerts** (Review within 24 hours):
- Unusual usage patterns
- New file types being accessed
- Commands outside normal profile
- Cost spikes

### 8.3 Incident Response Procedures

**AI-Specific Incident Types**:

| Incident | Response |
|----------|----------|
| Credential exposed to AI | Rotate credential immediately, review AI logs |
| Suspicious code generated | Quarantine code, security review, report |
| Prompt injection detected | Block user session, investigate source |
| Data exfiltration suspected | Preserve logs, forensic analysis, notify leadership |

**Incident Response Steps**:
1. **Detect**: Alert triggered or user report
2. **Contain**: Suspend AI access for affected user/system
3. **Investigate**: Review AI logs, network logs, code changes
4. **Remediate**: Fix vulnerability, rotate credentials, patch
5. **Report**: Document incident, notify as required
6. **Learn**: Update policies/controls to prevent recurrence

### 8.4 Regular Audits

| Audit Type | Frequency | Conducted By |
|------------|-----------|--------------|
| Access review | Monthly | IT Security |
| Usage compliance | Quarterly | Governance team |
| Security controls | Annually | External auditor |
| Policy effectiveness | Annually | Governance committee |

---

## 9. Implementation Roadmap

### Pre-Implementation: Questions to Answer First

| Question | Who to Ask | Why It Matters |
|----------|------------|----------------|
| Does your agency have a SIEM? | IT Security | Determines logging strategy |
| What is your identity provider? | IT | Determines SSO integration approach |
| What proxy does your agency use? | Network team | Required for network controls |
| Has your agency done AI procurements before? | Procurement | Determines if CDT relationship exists |
| Who is the executive sponsor? | Leadership | Required for CDT consultation |
| What is the budget? | Finance | Determines Enterprise vs. other options |

### Phase 0: Discovery & Prerequisites (Weeks 1-2)

| Task | Owner | Deliverable |
|------|-------|-------------|
| Answer pre-implementation questions | Project lead | Completed questionnaire |
| Identify SIEM solution | IT Security | SIEM decision documented |
| Identify executive sponsor | Leadership | Named sponsor |
| Initial CDT contact | CIO/sponsor | CDT consultation scheduled |
| Budget confirmation | Finance | Approved budget |

### Phase 1: Foundation (Weeks 3-6)

| Task | Owner | Deliverable |
|------|-------|-------------|
| Complete risk classification | Governance lead | Risk classification document |
| Complete CDT consultation | CIO | CDT approval/guidance |
| Complete Privacy Impact Assessment | Privacy Officer | PIA document |
| Complete Equity Impact Assessment | Governance | Equity assessment |
| Draft Acceptable Use Policy | Legal/Governance | Draft policy for review |
| Procure Enterprise license | Procurement | Signed contract with GenAI provisions |

### Phase 2: Technical Setup (Weeks 7-10)

| Task | Owner | Deliverable |
|------|-------|-------------|
| Configure SSO integration | IT | Working authentication |
| Set up audit logging to SIEM | IT Security | Logs flowing, dashboards created |
| Implement permission restrictions | IT | Managed settings deployed |
| Configure network proxy | Network team | Proxy rules active |
| Deploy security hooks | IT Security | Hooks blocking policy violations |
| Create alert rules | IT Security | Alerts configured in SIEM |

### Phase 3: Pilot - Internal Systems Only (Weeks 11-16)

| Task | Owner | Deliverable |
|------|-------|-------------|
| Select pilot group (10-15 developers) | Department leads | Pilot participant list |
| Train pilot participants (Modules 1+2) | Training team | 100% training completion |
| **SCOPE: Internal business systems ONLY** | - | No public systems, no benefits systems |
| Daily monitoring and review | IT Security | Daily monitoring reports |
| Weekly pilot check-ins | Governance | Weekly status reports |
| Collect and analyze feedback | Governance | Feedback summary |
| Refine controls based on findings | IT | Updated configuration |
| Document any incidents | IT Security | Incident log (target: 0 critical) |

**Pilot Success Criteria** (must meet before expanding):
- Zero critical security incidents
- <5 policy violations
- 100% training completion
- >70% developer satisfaction
- All actions logged successfully

### Phase 4: Expansion - Add Public Websites (Weeks 17-24)

| Task | Owner | Deliverable |
|------|-------|-------------|
| Review Phase 3 success criteria | Governance | Go/no-go decision |
| Expand scope to public-facing websites | Department leads | Updated scope document |
| Add developers working on public sites | Department leads | Expanded user list |
| Train new participants | Training team | Training completion |
| Enhanced monitoring for public systems | IT Security | Additional alert rules |
| Document lessons learned | Governance | Lessons learned report |

### Phase 5: Infrastructure/DevOps (Read-Only) (Weeks 25-32)

| Task | Owner | Deliverable |
|------|-------|-------------|
| Review Phases 3-4 safety record | Governance | Safety assessment |
| Deploy extra restrictions for infrastructure | IT | Infrastructure-specific controls |
| Train infrastructure team (Module 3) | Training team | IT staff training complete |
| Pilot with infrastructure team (read-only only) | IT | Limited infrastructure pilot |
| **IMPORTANT**: No production changes via AI | IT | Enforced at permission level |

### Phase 6: Benefits/Services Systems (Week 33+, After Proven Safety)

| Task | Owner | Deliverable |
|------|-------|-------------|
| Review 6+ months of safety data | Governance | Comprehensive safety review |
| Complete additional equity assessment | Governance | Equity review for benefits systems |
| CDT check-in for benefits system expansion | CIO | CDT approval for expansion |
| Very limited pilot with benefits systems | Department leads | Carefully scoped pilot |
| Enhanced code review requirements | Engineering leads | Review checklist for benefits code |

### Ongoing Operations (All Phases)

| Task | Owner | Frequency |
|------|-------|-----------|
| Usage monitoring and review | IT Security | Daily |
| Compliance report to governance | IT Security | Monthly |
| CDT reporting (as required) | CIO | Quarterly |
| Policy review and update | Governance | Quarterly |
| Risk reassessment | Governance | Annually |
| Training refresh | Training team | Annually |
| External security audit | External auditor | Annually |

### Timeline Summary

```
Weeks 1-2:   Discovery & Prerequisites
Weeks 3-6:   Foundation (CDT consultation, policies, procurement)
Weeks 7-10:  Technical Setup (SSO, logging, permissions, hooks)
Weeks 11-16: Pilot - Internal Systems Only
Weeks 17-24: Expansion - Public Websites
Weeks 25-32: Infrastructure/DevOps (Read-Only)
Week 33+:    Benefits/Services (After Proven Safety)
```

**Total time to full deployment: ~8-9 months**

This extended timeline reflects HIGH RISK classifications and the need to prove safety at each stage.

---

## 10. Verification & Testing Plan

### 10.1 Pre-Deployment Testing

**Security Control Verification**:

| Test | Expected Result | Pass/Fail |
|------|-----------------|-----------|
| Attempt blocked command (curl) | Command blocked, logged | |
| Attempt to read .env file | Access denied, logged | |
| Send prompt with SSN pattern | Prompt blocked, alert generated | |
| User without training tries access | Access denied | |
| Logs appear in SIEM | Events visible within 5 minutes | |

**Authentication Testing**:

| Test | Expected Result | Pass/Fail |
|------|-----------------|-----------|
| SSO login works | User authenticated via state IdP | |
| MFA required | Cannot bypass MFA | |
| Session timeout | Auto-logout after inactivity | |
| Access revocation | Disabled user cannot access | |

### 10.2 Pilot Success Criteria

| Criteria | Target | Measurement |
|----------|--------|-------------|
| Security incidents | 0 critical | Incident log |
| Policy violations | <5 | Alert log |
| User satisfaction | >70% positive | Survey |
| Training completion | 100% | Training records |
| Audit log completeness | 100% actions logged | Log review |

### 10.3 Ongoing Compliance Verification

**Monthly**:
- Review access list against HR records
- Sample audit of AI interactions
- Check for policy violations

**Quarterly**:
- Full compliance review
- CDT reporting
- Risk assessment update

**Annually**:
- External security audit
- Policy review and update
- Training program refresh
- Full risk reassessment

---

## Appendices

### Appendix A: Key Contacts

| Role | Responsibility |
|------|----------------|
| Executive Sponsor | Final accountability, CDT liaison |
| AI Governance Lead | Day-to-day oversight |
| IT Security Lead | Technical controls, monitoring |
| Legal/Privacy | Policy compliance, contracts |
| Training Coordinator | Training delivery |

### Appendix B: Reference Documents

- CDT GenAI Procurement Guidelines (July 2024)
- Executive Order N-12-23
- SAM Section 4983.1 (Cloud Computing)
- SAM Section 5305 (Data Classification)
- Assembly Bill 302
- NIST AI Risk Management Framework

### Appendix C: Glossary

| Term | Definition |
|------|------------|
| **Prompt** | The question or instruction you give to the AI |
| **Prompt Injection** | Attack where malicious instructions are hidden in data the AI reads |
| **Zero Data Retention** | Option where AI provider keeps no record of your interactions |
| **SIEM** | Security Information and Event Management - central security monitoring |
| **SSO** | Single Sign-On - login once to access multiple systems |
| **Managed Settings** | Configuration that IT controls, users cannot change |

### Appendix D: Verified Sources & References

> All sources verified January 2026. Links should be re-verified before presenting to executives.

**California State Government Sources**:

| Document | URL |
|----------|-----|
| Executive Order N-12-23 | https://www.gov.ca.gov/wp-content/uploads/2023/09/AI-EO-No.12-_-GGN-Signed.pdf |
| GovOps GenAI Page | https://www.govops.ca.gov/generative-ai-genai-executive-order/ |
| CDT GenAI Guidelines | https://cdt.ca.gov/wp-content/uploads/2024/07/3a-GenAI-Guidelines.pdf |
| Technology Letter 24-01 | https://cdt.ca.gov/policy/technology-letters/technology-letter-24-01/ |
| SAM 4983.1 | https://www.dgs.ca.gov/Resources/SAM/TOC/4900/4983-1 |
| CDT SIMM | https://cdt.ca.gov/policy/simm/ |
| AB 302 | https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202320240AB302 |
| SB 53 | https://leginfo.legislature.ca.gov/faces/billTextClient.xhtml?bill_id=202520260SB53 |
| AB 2013 | https://leginfo.legislature.ca.gov/faces/billTextClient.xhtml?bill_id=202320240AB2013 |
| CPPA Regulations | https://cppa.ca.gov/regulations/ccpa_updates.html |

**Anthropic Official Sources**:

| Document | URL |
|----------|-----|
| Trust Center | https://trust.anthropic.com/ |
| Privacy Center | https://privacy.claude.com/ |
| Certifications | https://privacy.claude.com/en/articles/10015870-what-certifications-has-anthropic-obtained |
| Security Docs | https://code.claude.com/docs/en/security |
| Data Usage | https://code.claude.com/docs/en/data-usage |
| ZDR Info | https://privacy.claude.com/en/articles/8956058-i-have-a-zero-data-retention-agreement-with-anthropic-what-products-does-it-apply-to |
| Monitoring (OpenTelemetry) | https://code.claude.com/docs/en/monitoring-usage |
| Settings | https://code.claude.com/docs/en/settings |
| Hooks | https://code.claude.com/docs/en/hooks |

---

## Summary: Critical Success Factors

1. **Executive Sponsorship**: CIO must own this and report to CDT
2. **Technical Controls**: Logging, permissions, and hooks are non-negotiable
3. **Training**: No one uses Claude Code without completing training
4. **Code Review**: Every line of AI-generated code gets human review
5. **Monitoring**: Active monitoring with alerts, not just logging
6. **Documentation**: Everything documented for compliance and audits
7. **Continuous Improvement**: Learn from incidents, update controls

---

## Version History

| Version | Date | Description | Author |
|---------|------|-------------|--------|
| Executive Draft v1.0 | January 2026 | Initial framework based on SWRCB pilot planning | Brent Vanderburgh |

---

*Document Verification Status: All California regulatory references verified against official sources. All Anthropic claims verified against official Trust Center and Privacy Center documentation.*
