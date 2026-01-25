# Executive Briefing: AI Coding Assistant Deployment

**Date**: January 2026
**Classification**: Varies by deployment (see Risk Classification)
**Prepared for**: California State Agency Executive Leadership

---

## Bottom Line Up Front

**AI coding assistants like Claude Code CAN be deployed safely in California state government**, but require:

- **CDT consultation** before procurement (mandatory for HIGH RISK)
- **8-9 month phased rollout** (not immediate full deployment)
- **Executive sponsorship** at CIO level
- **Investment** in logging, monitoring, and training infrastructure

---

## What is Claude Code?

An AI-powered coding assistant that helps developers write, review, and debug code. It runs on developer workstations and can execute commands, read files, and suggest code changes.

---

## Risk Classification

Per [CDT GenAI Guidelines](https://cdt.ca.gov/wp-content/uploads/2024/07/3a-GenAI-Guidelines.pdf):

| System Type | Classification | CDT Consultation |
|-------------|---------------|------------------|
| Internal tools only | LOW | Optional |
| Public-facing websites | MODERATE | Recommended |
| Benefits/services systems | **HIGH** | **Mandatory** |
| Critical infrastructure | **HIGH** | **Mandatory** |
| Infrastructure/DevOps | **HIGH** | **Mandatory** |

**HIGH RISK** = mandatory CDT consultation before procurement.

---

## Key Compliance Requirements

| Requirement | Source | Status |
|-------------|--------|--------|
| CDT consultation before procurement | [Technology Letter 24-01](https://cdt.ca.gov/policy/technology-letters/technology-letter-24-01/) | Required for Moderate/HIGH |
| GenAI Risk Assessment (SIMM 5305-F) | [CDT SIMM](https://cdt.ca.gov/policy/simm/) | **Required** |
| Data must stay in Continental US | [SAM 4983.1](https://www.dgs.ca.gov/Resources/SAM/TOC/4900/4983-1) | Verify with vendor |
| High-risk AI inventory reporting | [AB 302](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202320240AB302) | **Required** |
| Privacy Impact Assessment | CCPA Regulations | **Required** |
| Equity Impact Assessment | CDT Guidelines | **Required** |

---

## IT Security Concern: Resolved

**Original concern**: Network monitoring can't distinguish human actions from AI-initiated actions.

**Solution**: Claude Code supports [OpenTelemetry logging](https://code.claude.com/docs/en/monitoring-usage) that tags all AI actions with timestamps, user IDs, and session data. Combined with network logs, this provides complete attribution.

---

## Vendor (Anthropic) Compliance

| Certification | Status | Source |
|--------------|--------|--------|
| SOC 2 Type II | Verified | [Trust Center](https://trust.anthropic.com/) |
| ISO 27001:2022 | Verified | [Privacy Center](https://privacy.claude.com/en/articles/10015870-what-certifications-has-anthropic-obtained) |
| Data NOT used for training | Verified (commercial) | [Data Usage Policy](https://code.claude.com/docs/en/data-usage) |
| SSO/SAML support | Available | [Security Docs](https://code.claude.com/docs/en/security) |
| Zero Data Retention option | Available | [ZDR Info](https://privacy.claude.com/en/articles/8956058-i-have-a-zero-data-retention-agreement-with-anthropic-what-products-does-it-apply-to) |

**Must verify before contract**: Data center locations (must be Continental US per SAM 4983.1)

---

## Timeline Overview

| Phase | Duration | Scope |
|-------|----------|-------|
| 0: Discovery | Weeks 1-2 | Answer prerequisite questions, schedule CDT consultation |
| 1: Foundation | Weeks 3-6 | CDT consultation, assessments, procurement |
| 2: Technical Setup | Weeks 7-10 | SSO, logging, permissions, monitoring |
| 3: Pilot | Weeks 11-16 | **Internal systems only** (10-15 developers) |
| 4: Expansion | Weeks 17-24 | Add public websites |
| 5: Infrastructure | Weeks 25-32 | DevOps (read-only) |
| 6: Benefits Systems | Week 33+ | Only after 6+ months proven safety |

**Total: ~8-9 months to full deployment**

---

## Cost Estimate

| Item | Estimate | Notes |
|------|----------|-------|
| Claude Code Enterprise | ~$20/user/month | Verify with Anthropic Sales |
| SIEM (if not existing) | Varies | May use CDT shared service |
| Training development | Staff time | 4 modules required |
| External security audit | $15-50K | Annual requirement |

---

## Immediate Action Items (Week 1)

| # | Action | Owner |
|---|--------|-------|
| 1 | Confirm SIEM availability | IT Security |
| 2 | **Identify executive sponsor** | Leadership |
| 3 | **Schedule CDT consultation** | CIO |
| 4 | Review budget | Finance |
| 5 | Identify pilot developers (10-15) | Department leads |

---

## Executive Decision Required

**Approve or decline proceeding to Phase 0 (Discovery) and CDT consultation.**

If approved:
- CIO becomes accountable for GenAI governance
- CDT consultation must occur before any procurement
- Quarterly reporting to CDT required

---

## Risk Mitigation Summary

| Risk | Mitigation |
|------|------------|
| Data exposure | Permission restrictions block sensitive file access |
| Unattributed actions | OpenTelemetry logging tags all AI activity |
| Malicious code | Mandatory human code review before deployment |
| Compliance violation | Phased rollout with gates at each stage |
| Shadow AI | Formal program reduces unauthorized tool use |

---

## Full Plan Reference

Complete 10-section plan with all technical details, compliance citations, and implementation checklists:

**Location**: [deployment-plan.md](./deployment-plan.md)

---

## Alignment with Statewide Strategy

This deployment guide aligns with:

- **[E3 Operational Model](../../strategy/governance-model.md)** — E3 positions ensure qualified oversight of AI deployments
- **[Executive Accountability (TEA)](../../strategy/executive-accountability.md)** — Technical executive standards apply to AI governance decisions
- **[CDT GenAI Executive Order](https://cdt.ca.gov/technology-innovation/artificial-intelligence-community/genai-executive-order/)** — Statewide AI governance requirements

---

*All regulatory claims in this briefing are hyperlinked to official sources. See deployment plan Appendix D for complete reference list.*
