# AI Coding Assistant Deployment Guide

**A comprehensive framework for safely deploying Claude Code and similar AI coding assistants in California state government.**

**Version:** Executive Draft v1.0
**Date:** January 2026
**Prepared for:** California Department of Technology (CDT), State Agencies

---

## Overview

AI-powered coding assistants like Claude Code can significantly enhance developer productivity, but they introduce unique risks in government environments:

- **Attribution Problem**: Network monitoring cannot distinguish AI-initiated actions from human actions
- **Data Exposure**: Source code and prompts are sent to third-party AI providers
- **Security Vulnerabilities**: AI-generated code may contain security flaws
- **Compliance Complexity**: Multiple California regulations apply to AI tool usage

This guide provides a standardized, CDT-aligned approach to deploying AI coding assistants safely.

---

## Framework at a Glance

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    SIX-PHASE DEPLOYMENT MODEL                           │
├─────────────────┬─────────────────┬─────────────────┬───────────────────┤
│   Discovery &   │   Technical     │    Pilot:       │   Expansion:      │
│   Foundation    │     Setup       │ Internal Only   │  Public Systems   │
├─────────────────┼─────────────────┼─────────────────┼───────────────────┤
│  Infrastructure │   Benefits/     │                 │                   │
│  (Read-Only)    │   Services      │                 │                   │
└─────────────────┴─────────────────┴─────────────────┴───────────────────┘
                              │
                              ▼
                    ┌─────────────────┐
                    │   Risk-Based    │
                    │   Classification│
                    └─────────────────┘
                              │
                              ▼
              ┌───────────────────────────────┐
              │  CDT Consultation (if HIGH)  │
              └───────────────────────────────┘
```

---

## Documents in This Folder

| Document | Purpose | Audience |
|----------|---------|----------|
| [deployment-plan.md](./deployment-plan.md) | Complete deployment guide with technical controls, compliance requirements, and implementation roadmap | CIOs, IT Security, Program Managers |
| [executive-briefing.md](./executive-briefing.md) | 2-page summary for executive decision-making | Agency Directors, CIOs, Executive Leadership |
| [Executive Presentation](https://vanderoffice.github.io/presentations/claude-code-deployment-swrcb-2026-01-24.html) | Interactive slide deck for leadership briefings | Cabinet, Agency Directors, Executive Leadership |

---

## Risk Classification

Per [CDT GenAI Guidelines](https://cdt.ca.gov/wp-content/uploads/2024/07/3a-GenAI-Guidelines.pdf), AI coding assistant deployments are classified based on:

### Classification Factors

| Factor | Low Risk | Moderate Risk | HIGH RISK |
|--------|----------|---------------|-----------|
| System Type | Internal tools | Public-facing websites | Benefits/services, critical infrastructure |
| Data Access | Non-sensitive code | Internal business data | PII, regulated data |
| Infrastructure | Development only | Staging environments | Production, DevOps |
| Decision Impact | No citizen impact | Indirect impact | Direct impact on rights/benefits |

### Classification Implications

| Classification | CDT Consultation | Executive Sign-off | Enhanced Controls |
|----------------|------------------|-------------------|-------------------|
| Low | Optional | Manager | Standard |
| Moderate | **Recommended** | CIO-level | Enhanced |
| HIGH | **Mandatory** | CIO + Agency Director | Maximum |

---

## Compliance Requirements

California has specific requirements for AI tool deployment:

| Requirement | Source | Applicability |
|-------------|--------|---------------|
| CDT Consultation | [Technology Letter 24-01](https://cdt.ca.gov/policy/technology-letters/technology-letter-24-01/) | Moderate/HIGH risk |
| Risk Assessment (SIMM 5305-F) | [CDT SIMM](https://cdt.ca.gov/policy/simm/) | All deployments |
| Data Residency (Continental US) | [SAM 4983.1](https://www.dgs.ca.gov/Resources/SAM/TOC/4900/4983-1) | All cloud services |
| AI Inventory Reporting | [AB 302](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202320240AB302) | HIGH risk systems |
| Privacy Impact Assessment | CCPA/CPRA | If PII involved |
| Equity Impact Assessment | CDT Guidelines | Benefits/services systems |

---

## Deployment Phases

### Phase 0-1: Discovery & Foundation (Weeks 1-6)
- Answer prerequisite questions (SIEM availability, identity provider, budget)
- Complete CDT consultation (mandatory for HIGH RISK)
- Conduct risk, privacy, and equity assessments
- Procure Enterprise license with GenAI Special Provisions

### Phase 2: Technical Setup (Weeks 7-10)
- Configure SSO integration with state identity provider
- Deploy audit logging to SIEM (OpenTelemetry)
- Implement permission restrictions (deny dangerous commands)
- Configure network proxy and security hooks

### Phase 3: Pilot - Internal Systems Only (Weeks 11-16)
- 10-15 developers on internal business systems
- Daily monitoring and weekly check-ins
- Refine controls based on findings
- **Must meet success criteria before expanding**

### Phase 4-6: Controlled Expansion (Weeks 17+)
- Phase 4: Public-facing websites
- Phase 5: Infrastructure/DevOps (read-only)
- Phase 6: Benefits/services (after 6+ months proven safety)

---

## Success Criteria

Each phase requires meeting criteria before expansion:

| Criteria | Target |
|----------|--------|
| Security incidents | 0 critical |
| Policy violations | <5 |
| Training completion | 100% |
| User satisfaction | >70% positive |
| Audit completeness | 100% actions logged |

---

## Quick Start

### For Department CIOs
1. Read the [Executive Briefing](./executive-briefing.md) (5 min)
2. Determine risk classification using factors above
3. If HIGH RISK, schedule CDT consultation immediately
4. Identify executive sponsor and budget

### For IT Security Teams
1. Review Technical Security Controls in [Deployment Plan](./deployment-plan.md) Section 3
2. Verify SIEM availability or determine alternatives
3. Plan OpenTelemetry integration
4. Design permission restrictions

### For Program Managers
1. Review full [Deployment Plan](./deployment-plan.md)
2. Use Implementation Roadmap (Section 9) for project planning
3. Prepare training program (4 modules)
4. Establish governance structure

---

## Alignment with California Strategy

This guide aligns with:

- **[E3 Operational Model](../strategy/governance-model.md)** — E3 positions with technology oversight should ensure AI tool deployments meet standards
- **[Executive Accountability (TEA)](../strategy/executive-accountability.md)** — Technical executive qualification requirements apply to AI governance decisions
- **[AI Governance Principles](../archive/h5-ai-implementation-guide.md)** — Broader state AI governance framework
- **CDT GenAI Executive Order** — Statewide AI governance structure

---

## Key Technical Controls

### Attribution Solution (IT Division Concern)

Claude Code supports [OpenTelemetry logging](https://code.claude.com/docs/en/monitoring-usage):

```
Claude Code → OpenTelemetry → State SIEM (Splunk/Elastic)
                              ↓
                         Security Dashboard
                              ↓
                         Alert Rules
```

**Result**: Network logs + Claude Code logs = complete attribution of human vs. AI actions.

### Permission Restrictions

```json
{
  "permissions": {
    "deny": [
      "Bash(curl:*)", "Bash(wget:*)", "Bash(nmap:*)",
      "Bash(rm -rf:*)", "Bash(sudo:*)",
      "Read(.env)", "Read(**/secrets/**)"
    ],
    "allow": [
      "Bash(npm run:*)", "Bash(git status)",
      "Read(src/**)", "Edit(src/**)"
    ]
  }
}
```

---

## Vendor Considerations

For Claude Code specifically ([Anthropic](https://trust.anthropic.com/)):

| Feature | Status |
|---------|--------|
| SOC 2 Type II | Verified |
| ISO 27001:2022 | Verified |
| Data NOT used for training (commercial) | Verified |
| SSO/SAML support | Available |
| Zero Data Retention option | Available |
| OpenTelemetry audit logging | Available |

**Must verify before contract**: Data center locations (must be Continental US per SAM 4983.1)

---

## Related Resources

- [E3 Governance Model](../strategy/governance-model.md) — Statewide governance structure
- [Executive Accountability](../strategy/executive-accountability.md) — TEA framework for technical leadership
- [AI Implementation Guide](../archive/h5-ai-implementation-guide.md) — Broader AI governance
- [CDT GenAI Guidelines](https://cdt.ca.gov/wp-content/uploads/2024/07/3a-GenAI-Guidelines.pdf) — Official CDT guidance

---

## Version History

| Version | Date | Description | Author |
|---------|------|-------------|--------|
| Executive Draft v1.0 | January 2026 | Initial framework based on SWRCB pilot planning | Brent Vanderburgh |

---

*Effective AI governance begins with understanding risks and implementing controls appropriate to those risks.*
