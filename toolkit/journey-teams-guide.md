# B.5 Citizen Journey Teams - Complete Operating Guide

*Archived from appendices/07-operational-guides.md*

This document provides comprehensive operational guidance for Citizen Journey Teams. For the strategic framework, see [Appendix B.5](../appendices/operational-guides.md#b5-citizen-journey-teams-framework).

---

## B.5.1 The Journey-Centric Model

**Organizing Around Life Events:**

Traditional government organizes around agencies. Citizens experience life events that require multiple agencies:
- Having a baby (Health, Vital Records, Social Services, Tax)
- Starting a business (Secretary of State, Tax, Licensing, Permitting)
- Disaster recovery (Emergency Services, Housing, Insurance, Small Business)
- Losing a job (EDD, Covered California, CalFresh, Workforce Development)
- Caring for aging parents (Aging Services, Medi-Cal, In-Home Support, Regional Centers)

Citizen Journey Teams bring together E3 leaders, SMEs, and Fellows from relevant agencies to redesign experiences around these journeys, creating seamless integrated services.

**Why Journey Teams Work:**

| Traditional Approach | Journey Team Approach |
|---------------------|----------------------|
| Citizen navigates multiple agencies | Single coordinated experience |
| Each agency owns a transaction | Team owns the outcome |
| Data stays in silos | Shared data (with consent) |
| Success = processing volume | Success = citizen satisfaction |
| Accountability unclear | Executive Sponsor accountable |

---

## B.5.2 Team Structure and Governance

**Core Team Composition:**

| Role | Source | Responsibility | Time Commitment |
|------|--------|----------------|-----------------|
| **Executive Sponsor** | Undersecretary from lead agency | Champion, resource allocation, barrier removal, final decisions | 4-8 hrs/month |
| **Journey Lead** | Senior Fellow or CDD | Day-to-day leadership, coordination, delivery, team management | Full-time (6-12 months) |
| **Agency Representatives** | CDDs or delegates from each participating agency | Subject matter expertise, agency commitment, implementation authority | 50% (during design/build) |
| **Design Lead** | ODI CalInnovate | User research, service design, prototyping, testing | 50-100% (varies by phase) |
| **Technical Lead** | TMO or agency IT | Architecture, API integration, data sharing, security | 50-100% (varies by phase) |
| **Data Governance** | Data Stewards | Data standards, privacy, sharing agreements, compliance | 25% (ongoing) |
| **Communications Lead** | Agency PIO or TMO | Stakeholder communications, change management, rollout messaging | 25% (varies by phase) |

**Extended Team (Engaged as Needed):**

- Legal counsel (data sharing, liability, regulatory compliance)
- Privacy officer (PIA review, consent management)
- Procurement specialist (vendor management, contracts)
- Labor relations (workforce impact, union coordination)
- Accessibility specialist (WCAG compliance, inclusive design)

**Team Chartering Process:**

1. **Sponsor Selection (Week 1):** Governor's Office or E3 Council designates Executive Sponsor based on lead agency and journey scope
2. **Charter Development (Weeks 2-3):** Sponsor works with TMO to draft charter including:
   - Problem statement and journey scope
   - Participating agencies and commitment levels
   - Success metrics and targets
   - Timeline and major milestones
   - Resource requirements and funding source
   - Decision authority and escalation path
   - Risks and dependencies
3. **Agency Commitment (Week 4):** Each participating agency's E3 leader signs charter, committing staff resources
4. **Kickoff (Week 5):** Full team convenes; roles assigned; operating norms established

**Charter Template Elements:**

```
CITIZEN JOURNEY TEAM CHARTER

Journey Name: _______________
Executive Sponsor: _______________
Journey Lead: _______________
Charter Date: _______________

1. JOURNEY SCOPE
   - Target population: _______________
   - Journey trigger event: _______________
   - Journey endpoints: _______________
   - Out of scope: _______________

2. CURRENT STATE
   - Baseline metrics: _______________
   - Known pain points: _______________
   - Previous improvement attempts: _______________

3. SUCCESS METRICS
   - Metric 1: _____ (baseline: ___, target: ___)
   - Metric 2: _____ (baseline: ___, target: ___)
   - Metric 3: _____ (baseline: ___, target: ___)

4. TIMELINE
   - Discovery complete: _______________
   - Design complete: _______________
   - Pilot launch: _______________
   - Full deployment: _______________

5. TEAM RESOURCES
   - [Agency]: [Name], [Role], [% Time]
   - ...

6. GOVERNANCE
   - Team meetings: [frequency]
   - Sponsor check-ins: [frequency]
   - Escalation path: _______________

7. SIGNATURES
   Executive Sponsor: _______________
   Agency 1 E3 Leader: _______________
   Agency 2 E3 Leader: _______________
   ...
```

---

## B.5.3 Operating Model

**Phase 1: Formation (Month 1)**

*Objective:* Establish team, secure commitments, align on scope

| Activity | Owner | Deliverable |
|----------|-------|-------------|
| Select Executive Sponsor | E3 Council / Governor's Office | Designation memo |
| Draft team charter | Sponsor + TMO | Charter document |
| Secure agency commitments | Sponsor | Signed charter |
| Assign Journey Lead | Sponsor | Named lead + onboarding |
| Convene full team | Journey Lead | Kickoff meeting |
| Establish operating cadence | Journey Lead | Meeting schedule, tools, norms |

**Phase 2: Discovery (Months 2-3)**

*Objective:* Deeply understand citizen experience, quantify current state

| Activity | Owner | Deliverable |
|----------|-------|-------------|
| Citizen interviews (15-25) | Design Lead | Interview notes, quotes |
| Journey mapping workshop | Design Lead | Current-state journey map |
| Staff shadowing (each agency) | Agency Reps | Process observations |
| Data analysis (volumes, times, errors) | Technical Lead | Baseline metrics report |
| Pain point synthesis | Full Team | Prioritized pain points |
| Opportunity identification | Full Team | Opportunity brief |

**Discovery Methods:**

- **Citizen Interviews:** 45-60 minute sessions with recent journey completers; recruit diverse participants; compensate for time
- **Contextual Inquiry:** Observe citizens attempting the journey in real-time (in field offices, online)
- **Staff Interviews:** Understand frontline perspective, workarounds, and ideas
- **Data Mining:** Analyze transaction logs, call center data, complaints, processing times
- **Service Safari:** Team members attempt the journey themselves as "secret shoppers"

**Phase 3: Design (Months 4-5)**

*Objective:* Co-create improved experience, validate with testing

| Activity | Owner | Deliverable |
|----------|-------|-------------|
| Future-state visioning | Full Team | Vision statement |
| Ideation workshops | Design Lead | Solution concepts |
| Prototype development | Design Lead + Tech Lead | Low-fidelity prototypes |
| Citizen testing (2 rounds) | Design Lead | Test findings |
| Technical feasibility assessment | Technical Lead | Feasibility report |
| Data sharing requirements | Data Governance | Data sharing plan |
| Prioritized solution design | Full Team | Approved design brief |

**Design Principles:**

1. **Start with citizen need, not agency process**
2. **Digital first, but not digital only** (maintain accessible channels)
3. **Proactive, not reactive** (push information before citizens ask)
4. **Ask once, reuse** (don't request information already on file)
5. **Show progress** (real-time status visibility)
6. **Fail gracefully** (clear error recovery paths)
7. **Designed with, not for** (citizen co-design throughout)

**Phase 4: Build (Months 6-12)**

*Objective:* Implement changes, deploy incrementally, measure impact

| Activity | Owner | Deliverable |
|----------|-------|-------------|
| Technical implementation | Technical Lead | Working system components |
| API development/integration | Technical Lead | Connected services |
| Data sharing agreements | Data Governance | Executed agreements |
| Staff training | Agency Reps | Trained staff |
| Pilot deployment | Journey Lead | Pilot launch |
| Monitoring and optimization | Full Team | Pilot metrics report |
| Full rollout | Journey Lead | Statewide deployment |
| Knowledge transfer | Journey Lead | Documentation, handoff |

**Implementation Approach:**

- **Incremental deployment:** Start with geographic or demographic subset; expand based on success
- **API-first integration:** Use Service Mesh architecture; build reusable services
- **Parallel operations:** Run old and new systems in parallel during transition
- **Continuous testing:** Ongoing citizen feedback throughout rollout
- **Agile delivery:** 2-week sprints with regular demos and retrospectives

**Phase 5: Measure and Iterate (Ongoing)**

*Objective:* Track outcomes, continuously improve, share learnings

| Activity | Owner | Deliverable |
|----------|-------|-------------|
| Metrics tracking | Technical Lead | Dashboard |
| Citizen feedback collection | Design Lead | Ongoing feedback |
| Quarterly retrospectives | Journey Lead | Improvement backlog |
| Annual journey review | Sponsor | Annual report |
| Knowledge sharing | TMO | Case study, playbook update |

---

## B.5.4 Cross-Agency Accountability

**Challenge:** Journey teams span agencies with different priorities, budgets, and leadership. How do we ensure sustained commitment?

**Accountability Mechanisms:**

1. **Charter Commitments:** Written agency commitments with E3 leader signatures
2. **Sponsor Authority:** Executive Sponsor has escalation path to Governor's Office
3. **E3 Performance:** E3 leaders include journey team performance in their OKRs
4. **TMO Visibility:** TMO tracks all journey teams; reports status to E3 Council
5. **Public Dashboard:** Journey metrics visible on public modernization dashboard

**Escalation Path:**

| Issue Level | Resolution Forum | Timeline |
|-------------|-----------------|----------|
| Team operational issues | Journey Lead | 48 hours |
| Resource/commitment gaps | Executive Sponsor | 1 week |
| Inter-agency conflicts | E3 Council | 2 weeks |
| Strategic disagreements | GovOps Secretary | 2 weeks |
| Political/policy barriers | Governor's Office | As needed |

**When Things Go Wrong:**

- **Missed commitments:** Sponsor discusses with agency E3 leader; documents impact; escalates if unresolved
- **Scope creep:** Journey Lead refers to charter; Sponsor approves or rejects expansions
- **Technical blockers:** Technical Lead escalates to CDT; TMO facilitates resolution
- **Staff resistance:** Agency Reps work with labor relations; apply ADKAR change management
- **Budget shortfalls:** Sponsor requests Breakthrough Fund support or agency reallocation

---

## B.5.5 Success Metrics

| Metric | Definition | Target | Measurement Method |
|--------|------------|--------|-------------------|
| Journey Completion Time | Days from initiation to resolution | 50% reduction | Transaction timestamps |
| Touchpoints Required | Number of agency interactions | 60% reduction | Interaction count |
| Digital Completion Rate | % of journeys completed online | 80%+ | Channel analytics |
| Citizen Satisfaction | Post-journey survey score | +20 points (NPS) | Survey (email/SMS) |
| Error/Rework Rate | % requiring resubmission or correction | <5% | Exception tracking |
| Staff Time per Journey | Hours of staff effort per completion | 40% reduction | Time studies |
| Data Sharing Latency | Time for data to flow between agencies | <24 hours | System logs |

**Measurement Cadence:**

- **Weekly:** Operational metrics (volumes, processing times)
- **Monthly:** Satisfaction surveys, error rates
- **Quarterly:** Comprehensive review, trend analysis
- **Annually:** Full journey assessment, comparison to baseline

---

## B.5.6 Initial Priority Journeys

**Phase 1 Journeys (Year 1):**

| Journey | Lead Agency | Participating Agencies | Estimated Impact | Complexity |
|---------|-------------|----------------------|------------------|------------|
| New Business Formation | Secretary of State | FTB, EDD, ABC, CalOSHA, DFEH | 100K+ businesses/year | High |
| Disaster Recovery | CalOES | HCD, CDI, CalSBA, EDD, DSS | Critical resilience | High |

**Phase 2 Journeys (Year 2):**

| Journey | Lead Agency | Participating Agencies | Estimated Impact | Complexity |
|---------|-------------|----------------------|------------------|------------|
| Workforce Retraining | EDD | CCC, CWDB, DSS, DOR | Economic mobility | Medium |
| New Parent Support | CDPH | DSS, CDSS, FTB, DPH | 400K+ births/year | Medium |
| Senior Transition to Care | CDA | DHCS, DSS, Regional Centers, DOR | Aging population | High |

**Phase 3 Journeys (Year 3+):**

| Journey | Lead Agency | Participating Agencies | Estimated Impact | Complexity |
|---------|-------------|----------------------|------------------|------------|
| Youth Aging Out of Foster Care | CDSS | EDD, DMV, CCC, HCD | Vulnerable population | High |
| Immigrant Integration | GO-Biz | DMV, EDD, DSS, CDPH | 10M+ Californians | High |
| End of Life | CDPH | DSS, DCA, FTB, Courts | Dignity and efficiency | Medium |

---

## B.5.7 Resources and Support

**TMO Support for Journey Teams:**

- Journey team methodology training
- Charter development assistance
- Facilitators for cross-agency workshops
- Technical architecture guidance
- Change management resources
- Dashboard and metrics infrastructure

**ODI Support:**

- User research guidance and tools
- Design thinking facilitation
- Prototype development support
- Accessibility and inclusive design review
- CalAcademy training modules

**Tools and Templates:**

- Journey mapping templates (Miro, Figma)
- Charter template (linked above)
- Interview guides
- Prototype testing protocols
- Metrics dashboard templates
- Case study format
