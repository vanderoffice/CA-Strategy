# California Enterprise Modernization Plan
## Talent Development

**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency
**Date:** January 2026
**Version:** Executive Draft v2.0

---

## Table of Contents

5. [Talent Development and Sustainability](#5-talent-development-and-sustainability)
   - [5.1 California Digital Capability Model](#51-california-digital-capability-model)
   - [5.2 Governor's Innovation Fellowship Program](#52-governors-innovation-fellowship-program)
   - [5.3 Fellowship-to-Technical Executive Pathway](#53-fellowship-to-technical-executive-pathway)
   - [5.4 ODI Transition to Technical Executive Standards Office](#54-odi-transition-to-technical-executive-standards-office)
   - [5.5 Data Steward Network](#55-data-steward-network)
     - [5.5.1 Leveraging Existing Classifications for Digital Leadership](#551-leveraging-existing-classifications-for-digital-leadership)
   - [5.6 Training Programs](#56-training-programs)
   - [5.7 Labor Relations](#57-labor-relations)

---

> **Document Summary:** This document describes California's approach to building sustainable modernization capacity through a three-tier upskilling strategy, the Governor's Innovation Fellowship, and AI-augmented productivity. The key insight: upskilling existing staff and equipping them with AI tools delivers greater ROI than hiring hundreds of new specialists California cannot compete to recruit. For governance structure, see [Governance Model](governance-model.md). For funding and implementation timeline, see [Funding & Implementation](funding.md). For technical executive qualification standards (TEA), see [Executive Accountability](executive-accountability.md).

---

## 5. Talent Development and Sustainability

> **Section Summary:** California's talent strategy prioritizes **upskilling** over hiring. Government upskilling delivers 43% ROI ([Microsoft/ROI Institute](https://wwps.microsoft.com/blog/roi-results-ps-skilling-part3)), while hiring 500 specialists would cost $10-12M in hiring costs alone ([Pluralsight/SHRM](https://www.pluralsight.com/resources/blog/business-and-leadership/tech-industry-skill-development))—in a market where California cannot compete on salary. The strategy: upskill existing knowledge workers through CalAcademy, equip them with AI productivity tools like Claude Code, and hire only 50-100 central specialists for train-the-trainer and oversight. The Governor's Innovation Fellowship produces future technical executives (TEA pipeline), not frontline capacity.

### 5.1 California Digital Capability Model

California's workforce transformation follows a three-tier upskilling strategy, augmented by AI productivity tools. This model is informed by successful implementations including Estonia's distributed digital government (no central digital office) and the UK Government's Copilot trial (26 minutes/day saved per employee—equivalent to 1,130 FTEs).

**The Core Insight:**

| Approach | Cost | Challenge | Outcome |
|----------|------|-----------|---------|
| **Mass hiring (400+ specialists)** | $50-70M annually | California can't compete on salary (25% below private sector) | Chronic vacancies, consultant dependence |
| **Upskill existing staff + AI tools** | $5-10M annually | Culture change, training infrastructure | 40% productivity gain, sustainable capacity |

If you upskill 2,000 existing state employees and equip them with AI tools delivering 40% productivity gains ([Penn Wharton](https://budgetmodel.wharton.upenn.edu/issues/2025/9/8/projected-impact-of-generative-ai-on-future-productivity-growth)), you get output equivalent to 2,800 workers—bypassing a hiring war California cannot win.

#### Three-Tier Upskilling Strategy

**Tier 1: Foundation — Digital Literacy for Knowledge Workers**

| Element | Detail |
|---------|--------|
| **Platform** | CalAcademy (ODI's training platform) |
| **Target Audience** | Staff in knowledge work, policy, data, IT, and public-facing roles |
| **Modules** | AI literacy, data literacy, plain language, human-centered design, accessibility |
| **Progress** | 5,000+ employees trained since January 2024 |
| **Time Commitment** | 8-16 hours per employee (foundational modules) |

**Tier 2: Practitioner — Data Steward Network** (Department-determined ratios)

| Element | Detail |
|---------|--------|
| **Selection** | Each department identifies employees with analytical aptitude |
| **Ratio** | Department determines appropriate steward ratio based on data intensity |
| **Role** | Champion data quality, implement standards, train colleagues |
| **Classification** | Uses existing classifications (no new hiring) |
| **Training** | 40-hour CalAcademy certification |
| **Model** | Australian Data Champions Network ([proven framework](https://www.finance.gov.au/sites/default/files/2024-06/ses-accountabilities-for-data.pdf)) |

**What Data Stewards Do:**
- Own data quality for their unit's critical datasets
- Implement Independent Office of State Data Governance standards
- Train colleagues on data best practices
- Serve as first point of contact for data questions
- Identify opportunities for data sharing and integration

**Why Department-Determined Ratios:**
Departments vary dramatically in data intensity. DMV processes millions of records daily; a small licensing board may handle thousands annually. Fixed ratios (e.g., 1:75) waste resources in low-intensity departments and under-serve high-intensity ones. Departments know their needs.

**Tier 3: Specialist — Central Technical Excellence** (50-100 positions)

| Element | Detail |
|---------|--------|
| **Positions** | 50-100 specialists |
| **Location** | Central teams at TMO + Independent Office of State Data Governance |
| **Classification** | Research Data Specialist/Manager series (existing CalHR classifications) |
| **Role** | Train-the-trainer program development, advanced analytics/AI oversight, central governance |
| **Focus** | Build the trainers, not do the work |

**What Central Specialists Do:**
- Develop CalAcademy curriculum for data governance and AI literacy
- Provide train-the-trainer certification for Data Stewards
- Establish and maintain statewide data standards
- Oversee AI governance and responsible use frameworks
- Provide surge capacity for complex cross-agency projects

#### AI Augmentation Layer: Claude Code Deployment

California has a comprehensive [Claude Code deployment plan](../toolkit/claude-code-deployment/) that integrates with the Digital Capability Model:

| Element | Detail |
|---------|--------|
| **Rollout** | 8-9 month phased deployment with CDT consultation |
| **Risk-Based Approach** | Internal tools → Public websites → Infrastructure → Benefits systems |
| **Technical Controls** | OpenTelemetry logging to state SIEM, SSO integration, permission restrictions |
| **Compliance** | SOC 2 Type II, ISO 27001:2022; data NOT used for training |
| **Cost** | ~$20/user/month for Claude Code Enterprise |

**Impact on Staffing Model:**

| Scenario | Without AI | With Claude Code (40% productivity) |
|----------|------------|-------------------------------------|
| 100 IT developers | 100 FTE output | 140 FTE equivalent output |
| 500 analysts | 500 FTE output | 700 FTE equivalent output |
| 2,000 upskilled staff | 2,000 FTE output | 2,800 FTE equivalent output |

This is why California doesn't need hundreds of new data governance hires. Upskill existing staff, equip them with AI productivity tools, and hire only the specialists needed for training and oversight.

**Productivity Evidence:**

| Source | Finding |
|--------|---------|
| [UK Government Copilot Trial](https://www.theregister.com/2025/06/03/uk_government_study_ai_time_savings/) | 26 min/day saved per employee (1,130 FTE equivalent) |
| [Penn Wharton AI Projections](https://budgetmodel.wharton.upenn.edu/issues/2025/9/8/projected-impact-of-generative-ai-on-future-productivity-growth) | 40% productivity gains in analytical work |
| California [procurement.md](procurement.md) analysis | 26-55% developer productivity gains with AI coding assistants |

---

### 5.2 Governor's Innovation Fellowship Program

> **Key Reframe:** The Fellowship produces **leaders**; upskilling produces **capacity**. The Fellowship is an executive pipeline to TEA-qualified positions, not the primary mechanism for building modernization capacity.

The Fellowship establishes a continuous pipeline of emerging leaders trained to drive enterprise-wide government modernization. Participants in the program are referred to as **Fellows** during their 6-month cohort; graduates become **Senior Fellows** and form an ongoing network of modernization leaders.

**Program Structure:**

| Element | Detail |
|---------|--------|
| **Fellows per year** | 60 (continuous pipeline) |
| **Cohort size** | 20 Fellows |
| **Cohort duration** | 6 months |
| **Cohorts per year** | 3 (start January, May, September) |
| **Active Fellows** | ~40 at any time (overlapping cohorts) |
| **Primary Purpose** | Executive development pipeline (TEA preparation) |

**Program Components:**

| Component | Duration | Focus |
|-----------|----------|-------|
| **Foundational Bootcamp** | Weeks 1-2 | Executive presence, innovation methods, California government landscape, AI literacy |
| **Leadership Breadth** | Months 1-3 | Listening sessions with 8-10 departments; executive shadowing |
| **Innovation Training** | Months 1-4 | Human-centered design, prototyping, change management, AI applications |
| **Department Embedding** | Full 6 months | Real project ownership with mentorship |
| **Group Initiatives** | Full 6 months | Cross-agency team projects with executive sponsors |

*For detailed curriculum, training modules, and deliverable requirements, see [Appendix B.2: Fellowship Program Curriculum](../appendices/operational-guides.md#b2-fellowship-program-curriculum).*

**Expected Outcomes:**
- Fellows gain enterprise perspective required for TEA-qualified positions
- Graduates become Senior Fellows available for advisory capacity and emergency response
- Some initiatives transition to Breakthrough Fund projects
- Builds network of modernization leaders across state government

#### Post-Fellowship Engagement

Upon graduation, Fellows become **Senior Fellows** and join a permanent network:

**On-Call SME Network:**
- 5-10 hours/month average commitment
- Specific initiative support and Breakthrough Fund project consultation
- Quarterly knowledge-sharing meetings

**Emergency Response Capacity:**
- Roster of Senior Fellows from past 3-5 years
- Rapid activation (24-48 hours) for IT failures, cybersecurity incidents, natural disasters
- Voluntary participation—Senior Fellows may opt out based on circumstances

**Sustainability Model:**

| Timeline | Senior Fellow Capacity |
|----------|------------------------|
| After 12 months | 40 Senior Fellows (2 cohorts) |
| After 24 months | 80 Senior Fellows (4 cohorts) |
| After 36 months | 120+ Senior Fellows (6+ cohorts) |

---

### 5.3 Fellowship-to-Technical Executive Pathway

> **See also:** [Executive Accountability](executive-accountability.md) for complete TEA framework and qualification pathways.

**Purpose:**
The Fellowship provides a structured pathway for emerging leaders to develop toward Technical Executive Assignment (TEA) qualification. Fellows with technical backgrounds gain experience and credentials counting toward TEA eligibility.

**How Fellowship Supports TEA Qualification:**

| TEA Pathway | How Fellowship Contributes |
|-------------|---------------------------|
| **Professional Certification** | Protected time and resources for certification prep; CalAcademy offers prep courses |
| **Demonstrated Experience** | 6-month project ownership with documented outcomes; cross-agency leadership |
| **Independent Technical Panel** | Fellows build relationships with CDT, CalHR, and experts who may serve on panels |

**Timeline to TEA:**

| Phase | Activities |
|-------|------------|
| **Year 1: Fellowship** | Complete 6-month cohort, pursue certifications, document outcomes, graduate as Senior Fellow |
| **Years 2-5: Experience** | Continue in technical leadership role, accumulate documented outcomes, maintain network |
| **Year 5+: TEA Positions** | Apply for CIO/CISO/CDO/CTO roles with Fellowship outcomes as part of qualification package |

**Benefits:**

| For the State | For the Fellow |
|---------------|----------------|
| Pipeline of TEA-qualified candidates with enterprise perspective | Clear career pathway to technical executive roles |
| Leaders who understand California government from inside | Recognition of Fellowship investment |
| Built-in network reducing onboarding time | Competitive advantage in executive hiring |

---

### 5.4 ODI Transition to Technical Executive Standards Office

**Purpose:** Ensure cross-administration continuity through standards, not programs.

**Current Administration (2025-2027):**

| Function | Owner | Deliverable |
|----------|-------|-------------|
| Fellowship program administration | ODI | 60 Fellows annually (3 cohorts) |
| CalAcademy operation | ODI | Training platform, curriculum development |
| TEA qualification standards | ODI + CalHR | Published pathways and requirements |
| AI productivity tool deployment | ODI + CDT | Claude Code Enterprise rollout |

**Next Administration (2027+):**

ODI transitions from Fellowship administration to **Technical Executive Standards Office** with core functions:

| Function | Description |
|----------|-------------|
| **TEA Pathway Maintenance** | Keep qualification pathways current with industry standards |
| **Candidate Certification** | Administer TEA qualification process (certifications, panels) |
| **CalAcademy Operation** | Ongoing workforce development including AI tool training |
| **TEA Certification Prep** | Training programs for aspiring technical executives |
| **AI Tool Standards** | Oversee responsible AI deployment across state government |

**What Happens to the Fellowship:**

The Fellowship may continue under TMO or a new entity at the next Governor's discretion. The TEA framework survives regardless—qualification standards are technical and competency-focused, not politically tied to any administration.

**Why This Works:**

| Design Element | Benefit |
|----------------|---------|
| Standards over programs | Outlasts any single administration |
| Technical focus | Apolitical criteria for executive qualification |
| CalAcademy infrastructure | Sustainable training platform |
| AI tool integration | Productivity gains become standard operating procedure |

---

### 5.5 Data Steward Network

**Purpose:** Provide sustainable data governance capacity by embedding stewards within existing units rather than creating large centralized teams.

**Structure:**

| Component | Scale | Cost |
|-----------|-------|------|
| Embedded Data Stewards | Department-determined ratios (existing staff) | Training via CalAcademy |
| Central Specialists | 50-100 positions | $5-10M annually |
| AI Productivity Tools | Deployed to all stewards | ~$20/user/month |

**How the Data Steward Network Works:**

1. **Department Identification:** Each department identifies employees with analytical aptitude for Data Steward role
2. **Ratio Determination:** Departments determine appropriate steward ratio based on data intensity
3. **Training:** Data Stewards complete 40-hour CalAcademy certification
4. **AI Tool Deployment:** Stewards receive Claude Code and other AI productivity tools
5. **Central Specialist Support:** 50-100 central specialists provide train-the-trainer and oversight
6. **TEA Pathway:** Stewards with aspirations can pursue TEA certification prep

**Data Steward Responsibilities:**

| Responsibility | Time Allocation |
|----------------|-----------------|
| Data quality ownership for unit datasets | 30% |
| Implement Independent Office standards | 20% |
| Train colleagues on data practices | 20% |
| Answer data questions (first point of contact) | 15% |
| Identify data sharing opportunities | 15% |

**Central Specialist Functions (50-100 positions):**

| Function | Positions |
|----------|-----------|
| Train-the-trainer program development | 15-25 |
| CalAcademy curriculum development | 10-15 |
| Independent Office of State Data Governance staff | 15-25 |
| Advanced analytics and AI oversight | 10-20 |
| Cross-agency project surge capacity | 10-15 |

**Expected Impact:**

| Metric | Target |
|--------|--------|
| Data quality for critical datasets | 95%+ (up from 60-70% baseline) |
| Data sharing negotiation time | 80% reduction (12-18 months → 4-8 weeks) |
| Data-driven decision making | 50%+ increase (measured by analytics tool usage) |
| Annual operating cost | $5-10M (50-100 central specialists + CalAcademy training) |

---

### 5.5.1 Leveraging Existing Classifications for Digital Leadership

> **Note:** This section addresses competitive compensation for all digital leadership roles. For TEA qualification requirements, see [Executive Accountability](executive-accountability.md).

**The Challenge:**

State technical executives compete against private sector roles paying 30-40% more. Government pay falls approximately 25% below private sector ([Federal News Network](https://federalnewsnetwork.com/pay/2024/11/federal-pay-rates-are-falling-nearly-25-short-of-the-private-sector/)). Individual "Hire Above Minimum" (HAM) rates were **eliminated in October 2024** by CalHR to prevent gender pay gaps.

**CalHR's 6 IT Domains:**

The 2018 IT Classification Consolidation established [6 IT domains](https://www.calhr.ca.gov/about-calhr/divisions-programs/personnel-management/class-specifications/information-technology-class-consolidation/):

| Domain | Description | Leadership Examples |
|--------|-------------|---------------------|
| **Business Technology Management** | IT portfolio, strategy, digital UX, procurement | CIO, CDO |
| **Software Engineering** | Application development, architecture | Chief Architect |
| **System Engineering** | Infrastructure, cloud, database, network | CTO |
| **Information Security Engineering** | Cybersecurity, risk management | CISO |
| **IT Project Management** | Delivery, governance | PMO Director |
| **Client Services** | End-user support, training | Service Delivery Director |

**Three Pathways to Competitive Compensation:**

**Pathway 1: CEA Restricted Zone (Executive Roles)**

For TEA positions requiring licensed engineer or scientist credentials:

| Classification | Salary Range | Requirement |
|----------------|--------------|-------------|
| CEA Level A/B/C | $124K-$256K | Standard appointment |
| **CEA Restricted Zone** | **>$256K** | Licensed engineer/scientist credentials + CEA Delegation Agreement |

**Pathway 2: Classification-Level HAM (Technical Specialists)**

| Classification | Range | Process |
|----------------|-------|---------|
| IT Specialist III | $90K-$148K | Submit Employee Compensation Request |
| IT Manager I/II | $100K-$179K | Demonstrate recruitment difficulty |

**Pathway 3: Research Scientist/Engineer Series (Analytical Roles)**

| Classification | CalHR Series | Range | Best For |
|----------------|--------------|-------|----------|
| Research Data Specialist I/II | [5729](https://www.calhr.ca.gov/state-hr-professionals/pages/5729.aspx) | $62K-$110K | Data governance, AI/ML |
| Research Data Manager | 5729 | $105K-$119K | Data governance leadership |
| Research Scientist | [5576](https://www.calhr.ca.gov/state-hr-professionals/Pages/5576.aspx) | Varies | Domain-specific AI/ML |

---

### 5.6 Training Programs

**CalAcademy — The Foundation:**

ODI's CalAcademy provides comprehensive training across innovation methods and is the primary platform for the Digital Capability Model:

| Track | Target Audience | Hours |
|-------|-----------------|-------|
| AI Literacy for Government | Knowledge workers (Tier 1) | 4-8 |
| Data Literacy and Best Practices | Knowledge workers (Tier 1) | 4-8 |
| Plain Language and Communication | Knowledge workers (Tier 1) | 2-4 |
| Human-Centered Design | Data Stewards (Tier 2) | 8-16 |
| Data Steward Certification | Data Stewards (Tier 2) | 40 |
| Claude Code for State Employees | AI tool users | 4-8 |
| Advanced Analytics | Specialists (Tier 3) | 40+ |

**TEA Certification Preparation:**

For staff aspiring to Technical Executive Assignment positions:

| Certification | Target Role | Training Support |
|--------------|-------------|------------------|
| CISSP, CISM, CISA | CISO | 40-hour prep course + study groups |
| PMP | CIO, CTO | 35-hour prep + exam voucher |
| TOGAF | CIO, CTO | Foundation + Practitioner |
| ITIL Expert | CIO | Full pathway |

**CalAcademy Technical Tracks:**

| Element | Detail |
|---------|--------|
| **Purpose** | Upskill IT staff in modern technologies (AI, cloud, DevOps) |
| **Protected Time** | 20% of work hours for training |
| **Format** | Cohort-based learning with hands-on labs |
| **Certifications** | AWS, Kubernetes, Claude Code, etc. |

**Emerging Technology Accelerator Partners:**

| Partner | Contribution |
|---------|--------------|
| Stanford Institute for Human-Centered AI | AI ethics curriculum, responsible AI frameworks |
| UC Berkeley | Academic partnerships, policy research |
| Mozilla Foundation | Open technology expertise |
| Tech Talent Project | Talent pipeline development |
| U.S. Digital Response | Delivery expertise, civic tech methodology |
| Nava Labs | Service design, human-centered design training |

---

### 5.7 Labor Relations

Successful modernization requires partnership with labor organizations:

| Principle | Implementation |
|-----------|----------------|
| **No Involuntary Separations** | Efficiency gains redirect staff to higher-value work |
| **Early Engagement** | Unions consulted before modernization decisions |
| **Upskilling Priority** | Training programs prepare workers for evolving roles |
| **Classification Coordination** | New positions developed with CalHR and bargaining units |

**AI Tool Deployment and Labor:**
- Claude Code and similar tools augment worker productivity—they do not replace positions
- All AI tool deployment includes training for affected workers
- Union briefings on AI adoption plans and workforce impact

**TEA and Executive Classifications:**
TEA applies only to Career Executive Assignments and exempt positions—not to civil service classifications or represented employees.

For comprehensive guidance, see [Appendix B.4: Labor Relations Strategy](../appendices/operational-guides.md#b4-labor-relations-strategy).

---

> This document is part of the California Enterprise Modernization recommendation. See also:
> - [Executive Summary](executive-summary.md) — Start here for an overview
> - [Executive Accountability](executive-accountability.md) — TEA standards and audit enforcement
> - [Governance Model](governance-model.md) — E3 structure and leadership
> - [Data Governance](data-governance.md) — Independent Office and data sharing
> - [Funding & Implementation](funding.md) — Breakthrough Fund structure
> - [Procurement Guide](procurement.md) — Technology and procurement innovation
> - [Templates](../appendices/templates.md) — Fillable forms and templates
> - [Operational Guides](../appendices/operational-guides.md) — Program guides and frameworks
> - [Technical Appendices](../appendices/technical-standards.md) — Technical standards and architecture
> - [Budget and Governance](../appendices/budget-models.md) — Budget models and change management

---

## Version History

| Version | Date | Description | Author |
|---------|------|-------------|--------|
| Executive Draft v2.0 | January 2026 | Upskilling-first California Digital Capability Model, embedded Data Steward Network, ODI transition framework, AI productivity tool integration | Claude |
| Executive Draft v1.7 | January 2026 | Added Section 5.5.1 Digital Leadership Classifications | Claude |
| Executive Draft v1.6 | January 2026 | Added Section 5.3 Fellowship-to-Technical Executive Pathway | Governor's Innovation Fellow |
| Executive Draft v1.5 | January 2026 | Renumbered sections | Claude |
| Executive Draft v1.4 | January 2026 | Readability improvements | Claude |
| Executive Draft v1.3 | December 2025 | Added Emerging Technology Accelerator partners | Brent Vanderburgh |
| Executive Draft v1.0 | December 2025 | Initial executive draft | Brent Vanderburgh |

---

**Document Version:** Executive Draft v2.0
**Date:** January 2026
**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency

---

*End of California Enterprise Modernization Plan - Talent Development*
