# B.1 Rapid RFI² Operational Guide - Detailed Procedures

*Archived from appendices/07-operational-guides.md*

This document provides detailed operational guidance for executing Rapid RFI² challenges. For the strategic overview, see [Section 8.4: Rapid RFI²](../05-procurement-guide.md#84-rapid-rfi-challenge-based-procurement) and the framework summary in [Appendix B.1](../appendices/07-operational-guides.md#b1-rapid-rfi-framework).

---

## Phase 1: Problem Statement (Weeks 1-3)

Cross-functional team (program staff, IT, E3 leaders, ODI) defines:

**Problem Statement Components:**
- **Current State:** What's broken? (quantified with specific metrics)
- **Target Metric:** What does success look like? (specific, measurable outcomes)
- **Constraints:** Budget, timeline, must-integrate-with systems, regulatory requirements
- **Evaluation Criteria:** How prototypes will be judged (weighted criteria)

**Team Composition:**
- Program SME (understands the business problem)
- IT representative (understands technical landscape)
- E3 CDD or designee (owns decision authority)
- ODI advisor (ensures human-centered design principles)
- TMO Challenge Manager (manages logistics)

**Quality Checklist:**
- [ ] Problem is outcome-focused, not solution-prescriptive
- [ ] Metrics are specific and measurable
- [ ] Constraints are realistic and documented
- [ ] Evaluation criteria are objective and weighted
- [ ] Timeline allows for vendor preparation

**Example Problem Statement:**

> **Challenge:** Foster care application processing takes 45 days average. Staff spend 40% of time re-keying data from PDF forms into the case management system. 60% of applications require manual review due to missing or inconsistent data.
>
> **Target:** Reduce processing time to <5 days. Achieve 85% auto-adjudication rate for complete applications.
>
> **Constraint:** Must integrate with Legacy System X via existing API. Must comply with HIPAA and state privacy requirements. Budget envelope: $50K per prototype, $5M for production implementation.
>
> **We seek:** A partner to prototype a solution demonstrating how caseworkers can achieve these targets. We are not prescribing technology stack, provided it adheres to State Technology Standards (Appendix H).

---

## Phase 2: Concept Papers (Weeks 4-5)

**Solicitation Process:**
- Problem Statement issued to pre-qualified MSA pool (not open solicitation—vendors already vetted)
- Targeted outreach to pool vendors with relevant expertise
- Office hours scheduled for vendor questions

**Concept Paper Requirements:**
- **5-page maximum** (excluding attachments)
- Sections:
  1. Problem Understanding (1 page)
  2. Proposed Approach (2 pages)
  3. Innovation Elements (1 page)
  4. Team Capabilities (1 page)
- Required attachment: Technical Architecture Diagram (1 page)
- Optional: Relevant case studies, team resumes

**Evaluation Squad Composition:**
- Product Manager (problem owner)
- Technical SME (assesses feasibility)
- TMO representative (ensures process compliance)

**Evaluation Criteria:**

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Problem Understanding | 25% | Demonstrates deep understanding of challenge and context |
| Innovation | 25% | Novel approach with potential for breakthrough results |
| Technical Feasibility | 25% | Realistic architecture, proven technologies, integration approach |
| Team Capability | 25% | Relevant experience, appropriate staffing, delivery track record |

**Selection:**
- Select top 2-3 concepts for paid prototype phase
- Provide written feedback to non-selected vendors
- Document selection rationale for audit trail

---

## Phase 3: Paid Prototype Sprint (Weeks 6-10)

**Funding and Contracting:**
- Shortlisted vendors receive **$50K each** via:
  - P-Card for vendors with existing state contracts
  - Tier 1 task order from MSA pool
  - Micro-purchase authority where applicable
- Contract is for prototype only; production contract awarded separately based on results

**State-Provided Resources:**
- **Sandbox Environment:** Production-like technical environment provided by CDT
- **Sanitized Data:** Representative test data with PII removed/anonymized
- **System Access:** API documentation, test credentials, technical contacts
- **Challenge Manager Support:** TMO staff handling logistics

**Vendor Deliverables:**
- Working prototype (code, not slides)
- Technical documentation
- User testing results
- Production scaling estimate

**Cadence:**
- Kickoff meeting (Week 6, Day 1)
- Bi-weekly check-ins (Weeks 7, 9)
- Final prototype delivery (Week 10)

**Challenge Manager Responsibilities:**
- Coordinate sandbox provisioning with CDT
- Manage data access approvals
- Process payments
- Facilitate check-in meetings
- Document issues and lessons learned
- Prepare evaluation logistics

---

## Phase 4: Evaluation & Award (Week 11)

**Demonstration Format:**
- 30-minute live demo per vendor
- Actual prototype operation (not slides)
- 15-minute Q&A
- Audience: E3 Undersecretary, Product Team, technical evaluators, end users

**Evaluation Criteria:**

| Criterion | Weight | Measurement |
|-----------|--------|-------------|
| **User Experience** | 30% | Usability score from staff testers; accessibility compliance |
| **Technical Viability** | 30% | Successful integration with legacy sandbox; code quality |
| **Performance** | 25% | Speed, accuracy against target metrics |
| **Scalability** | 15% | Production readiness; maintainability assessment |

**Award Decision:**
- Winner announced within 3 business days of demonstrations
- Winner awarded **Tier 2 Contract ($2M-$15M)** to scale prototype to production
- Non-winners: paid for prototype work, debriefed, prototype IP retained by State

**Post-Award:**
- Transition meeting with winning vendor
- Production contract negotiation (target: 2 weeks)
- Prototype code review and security assessment
- Production timeline established
