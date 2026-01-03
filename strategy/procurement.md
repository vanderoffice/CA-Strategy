# California Enterprise Modernization Plan
## Procurement Guide

**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency
**Date:** December 8, 2025
**Version:** Executive Draft v1.5

---

## Table of Contents

8. [Procurement Innovation](#8-procurement-innovation)
    - [8.1 The Agile Procurement Framework](#81-the-agile-procurement-framework)
    - [8.2 Enterprise Vendor Pools (Multi-Award MSA Model)](#82-enterprise-vendor-pools-multi-award-msa-model)
    - [8.3 Modular Contracting](#83-modular-contracting)
    - [8.4 Rapid RFI²: Challenge-Based Procurement](#84-rapid-rfi-challenge-based-procurement)
    - [8.5 Procurement On-Ramps by PDL Stage-Gate](#85-procurement-on-ramps-by-pdl-stage-gate)
    - [8.6 Delegated Ordering Authority](#86-delegated-ordering-authority)
    - [8.7 Challenge Manager Role (TMO)](#87-challenge-manager-role-tmo)
    - [8.8 Small Business Equity](#88-small-business-equity)
    - [8.9 Procurement Automation and Transparency](#89-procurement-automation-and-transparency)
    - [8.10 AI-Era Pricing Expectations](#810-ai-era-pricing-expectations)

---

**Technology Architecture Foundation:**

California's product-led delivery operates within the technology architecture principles established by CDT: API-first design, cloud-native development, security by design, open standards, and modular architecture. Procurement supports these principles through vendor pool selection criteria, contract requirements, and stage-gate reviews.

For complete architecture principles, five architecture domains (API Management, Legacy Modernization, Cloud Strategy, Cybersecurity, Agentic Data Systems), key targets, and governance structures, see [Appendix H: Technology Architecture Details](../appendices/technical-standards.md#appendix-h-technology-architecture-details).

---

## 8. Procurement Innovation

> **Section Summary:** This section establishes California's agile procurement framework, including Enterprise Vendor Pools (contracts in days), the $15M modular contracting cap, Rapid RFI² challenge-based procurement, and delegated ordering authority for E3 leaders. Modern procurement is essential for AI adoption—AI capabilities are evolving rapidly, and California needs contracting mechanisms that can keep pace.

**Philosophy:** Fast, modular, competition-driven procurement that treats contracting as a delivery tool—not a separate process. This is particularly critical as AI transforms what's possible—rigid, slow procurement means missing opportunities to apply AI for efficiency gains and better citizen service.

California's procurement system must operate at the speed of modern product delivery. This means embedding procurement directly into the Product Delivery Lifecycle, using pre-competed vendor pools to eliminate redundant negotiations, and validating solutions through paid prototypes before committing to full contracts.

---

### 8.1 The Agile Procurement Framework

California establishes a unified procurement framework with three integrated components:

| Component | Purpose | Speed |
|-----------|---------|-------|
| **Enterprise Vendor Pools** | Pre-qualified vendors by category, ready for task orders | Contracts in days |
| **Modular Contracting** | $15M cap forcing smaller, manageable contracts | Reduces risk, increases competition |
| **Rapid RFI²** | Challenge-based procurement for uncertain problems | Validated solutions in 8-10 weeks |

These components work together: Vendor Pools provide the "who," Modular Contracting sets the "how much," and Rapid RFI² determines the "what" when solutions aren't obvious.

---

### 8.2 Enterprise Vendor Pools (Multi-Award MSA Model)

**The Problem:** Traditional procurement takes 18-24 months because every contract starts from scratch—legal negotiation, vendor qualification, compliance verification.

**The Solution:** Pre-compete once, order many times.

This proposal recommends that California establish statewide multi-award Master Service Agreements (MSAs) with pre-qualified vendors across common technology categories. Once a vendor is in the pool, departments would issue task orders without re-competing the base contract.

**Pool Categories:**

| Category | Scope |
|----------|-------|
| **Agile Digital Services** | User-centered design, web/mobile development, API integration, DevOps |
| **Data & Analytics** | Data engineering, ML/AI implementation, AI application development, visualization, legacy data migration |
| **Cloud & Platform** | Cloud architecture, platform engineering, identity/payments/document services, AI infrastructure |
| **Cybersecurity** | Security assessments, monitoring, incident response, compliance, AI security evaluation |
| **Change Management** | Training, adoption support, communication, stakeholder engagement, AI literacy programs |

*Note: As AI capabilities mature, the Data & Analytics pool includes vendors qualified to implement AI solutions that comply with Independent Office AI governance standards.*

**Tiered Vendor Structure:**

| Tier | Criteria | Advantage |
|------|----------|-----------|
| **Tier 1: Small/DVBE** | <100 employees, <$20M revenue | First consideration for orders <$1M |
| **Tier 2: Medium** | 100-500 employees, $20M-$100M revenue | Competitive for $1M-$15M |
| **Tier 3: Large** | 500+ employees, $100M+ revenue | Complex, large-scale implementations |

**How It Works:**

1. **Annual Pool Refresh:** DGS conducts single annual RFP per category. Vendors pre-qualified based on capability, experience, rates, past performance.
2. **Task Order Process:** Department issues task order to pool. For orders <$250K: direct award to qualified vendor. For orders $250K-$1M: lightweight competition among 3+ pool vendors. For orders >$1M: documented competition with evaluation criteria.
3. **Performance Tracking:** Quarterly reviews of all vendors. Poor performers removed. High performers highlighted for additional opportunities.

**Speed Targets:**
- Task orders <$500K: Award within **10 business days** of final statement of work
- Task orders $500K-$2M: Award within **20 business days**
- Task orders >$2M: Award within **45 business days**

---

### 8.3 Modular Contracting

**The Recommended Rule:** No single IT contract should exceed **$15 million** or **3 years** without legislative waiver.

*Note: This applies to individual contracts, not programs. A $50M program may consist of multiple $15M contracts with different vendors, enabling competition at each phase. This is the intended design—programs should be structured as multiple modular contracts.*

**Why This Works:**

| Benefit | How |
|---------|-----|
| **Smaller failures** | Failed $8M module ≠ failed $60M program |
| **More competition** | Mid-size firms can bid $10M; they can't bid $60M |
| **Vendor accountability** | Underperformers replaced at next module |
| **Course correction** | Pivot after Module 1 learnings without abandoning investment |
| **Budget flexibility** | Defer later modules if priorities shift; completed modules retain value |

**How a $50M Program Works:**

Instead of one $50M contract with one vendor over 4 years:

| Module | Scope | Budget | Timeline | Vendor Selection |
|--------|-------|--------|----------|------------------|
| **1: Platform** | Infrastructure, auth, API gateway | $12M | Months 1-14 | Best platform expertise |
| **2: Data Migration** | Legacy migration, system integration | $12M | Months 8-20 | Best data expertise (can differ) |
| **3: Applications** | Citizen portal, staff interfaces | $14M | Months 15-28 | Best UX/agile expertise |
| **4: Operations** | Analytics, automation, 2-year O&M | $12M | Months 22-42 | Best value for support |

**Integration Management:**
- Department designates **Integration Architect** (staff or small contract) who defines interface specs, chairs weekly vendor coordination, ensures modules connect
- All contracts require **well-documented APIs**—integration through APIs, not tight coupling
- **Shared dev/test environment** where all vendors work; integration issues caught early

**Waiver Process:**
Projects genuinely requiring >$15M single contract must:
1. Document why modular approach infeasible
2. Pass CDT and TMO technical review
3. Receive joint legislative oversight committee approval
4. Accept enhanced oversight and quarterly public reporting

---

### 8.4 Rapid RFI²: Challenge-Based Procurement

**When to Use:** Problems where the need is clear but the best solution is uncertain. High-uncertainty, cross-agency, or emerging technology challenges where traditional requirements would constrain innovation. **AI applications are ideal candidates for Rapid RFI²**—the field is evolving rapidly, and prototypes demonstrate whether AI solutions actually work for specific government use cases.

**When NOT to Use:** Well-defined requirements with proven solutions, commodity purchases, time-critical needs, low-risk implementations.

**The Core Idea:** Instead of writing detailed specs and evaluating written proposals, issue a Problem Statement and let vendors prove their solution works through paid prototypes. **The code is the proposal.**

**The Rapid RFI² Protocol**

| Phase | Duration | Activity | Output |
|-------|----------|----------|--------|
| **1: Problem Statement** | 2-3 weeks | Agency defines problem, outcomes, constraints, success criteria | Published challenge |
| **2: Concept Papers** | 2 weeks | Pool vendors submit 5-page concept + architecture diagram | 2-3 shortlisted |
| **3: Paid Sprint** | 4-5 weeks | Shortlisted vendors build working prototype ($50K each) | Working code, not slides |
| **4: Evaluation & Award** | 1 week | Live demos; evaluation; contract negotiation | Contract award |

**Total time from problem to contract: 8-10 weeks**

**RFI² Resources:**

| Resource | Location | Contents |
|----------|----------|----------|
| Operational Guide | [Appendix B.1](../appendices/operational-guides.md#b1-rapid-rfi-operational-guide) | Phase-by-phase procedures, example problem statements, evaluation criteria |
| Problem Statement Template | [Template A.7](../appendices/templates.md#a7-rapid-rfi-problem-statement-template) | Standard format for challenge solicitations |
| AI Disclosure Template | [Template A.8](../appendices/templates.md#a8-ai-productivity-disclosure-template) | Required vendor productivity disclosure |

**Risk Reduction Value:**

| Scenario | Traditional Procurement | Rapid RFI² |
|----------|------------------------|------------|
| All approaches fail | $15M+ spent, 2+ years lost | $150K spent, 10 weeks lost |
| Requirements were wrong | Expensive change orders | Pivot before big commitment |
| Vendor can't deliver | Locked in, painful extraction | Validated capability before contract |

---

### 8.5 Procurement On-Ramps by PDL Stage-Gate

Procurement decisions align with Product Delivery Lifecycle gates—no more "procurement as separate process."

| Gate | PDL Stage | Procurement Action | Authority | Typical Value |
|------|-----------|-------------------|-----------|---------------|
| **Gate 0** | Concept Approval | Discovery micro-task orders from pool | E3 CDD | Up to $300K |
| **Gate 1** | Feasibility | Decide: standard task order OR Rapid RFI² | E3 Undersecretary | — |
| **Gate 2** | Alpha Delivery | Sprint-based task orders OR RFI² paid prototypes | E3 Undersecretary + TMO | $500K-$2M |
| **Gate 3** | Beta Delivery | Confirm vendors/frameworks for production; establish modular contract envelope | E3 Undersecretary + TMO | $2M-$15M per module |
| **Gate 4-5** | Go-Live / Benefits | Task orders for enhancements, O&M; benefits review includes vendor performance | Product Team | Varies |

**Key Principle:** At each gate, product teams can **extend, pivot, or terminate** vendor work based on evidence. No commitment beyond current phase until value demonstrated.

---

### 8.6 Delegated Ordering Authority

**Purpose:** Push procurement decisions to product teams while maintaining standards.

| Role | Task Order Limit | Conditions |
|------|------------------|------------|
| **Authorized Product Owner** | Up to $500K | Completed certification training |
| **E3 Chief Deputy Director** | Up to $2M | Within approved project envelope |
| **E3 Undersecretary** | Up to $5M | TMO portfolio review |
| **Above $5M** | — | Full stage-gate governance |

**Training Requirement:**
Staff receiving delegation complete standardized training covering:
- Modular contracting principles
- Rapid RFI² process
- Vendor pool usage
- Small business requirements
- AI-era pricing expectations (see Section 8.10)
- Ethics and compliance

TMO tracks certifications; delegations subject to periodic review based on performance metrics (competition rates, cycle time, small business utilization, audit findings).

---

### 8.7 Challenge Manager Role (TMO)

**Problem:** Agencies want to run Rapid RFI² challenges but lack bandwidth to manage logistics—sandbox provisioning, data sanitization, P-Card payments, vendor coordination.

**Solution:** TMO deploys **Challenge Managers**—specialized staff who handle sprint logistics so agency Product Owners focus on judging outcomes, not running contests.

**Challenge Manager Responsibilities:**
- Coordinate sandbox environment provisioning with CDT
- Manage sanitized data access for prototype development
- Process P-Card/task order payments to prototype vendors
- Facilitate bi-weekly vendor check-ins
- Coordinate evaluation demo logistics
- Document lessons learned for future challenges

**Staffing:** 2-3 Challenge Managers within TMO, scaling based on RFI² volume.

---

### 8.8 Small Business Equity

**Targets:**
- **25% of total IT spend** to Tier 1 vendors (small business + DVBE) by Year 3
- Reported quarterly with agency-level breakdowns

**Mechanisms:**

| Contract Size | Requirement |
|---------------|-------------|
| **<$1M** | First consideration to Tier 1 vendors |
| **$1M-$5M** | Minimum 25% subcontractor value to Tier 1 |
| **>$5M** | Small business participation plan required |

**Rapid RFI² Equity Feature:**
- RFI² solicitations structured to encourage teaming (small business + larger partner)
- Successful RFI² prototype completion earns "fast-track" consideration for next pool refresh
- Builds small business capacity for future competition

---

### 8.9 Procurement Automation and Transparency

**Automation:**
- Standard task order templates embedded in workflow tools
- System integrations auto-pull vendor certifications, small business status, exclusion lists, prior performance
- Guided workflows replace manual documentation assembly

**Transparency:**
- TMO publishes public dashboard showing:
  - Framework usage and task order volume
  - RFI² challenges (active, completed, outcomes)
  - Competition rates and small business participation
  - Average cycle times by procurement type
  - Vendor concentration metrics
- Agency scorecards include procurement metrics alongside service delivery KPIs

---

### 8.10 AI-Era Pricing Expectations

**The Productivity Shift:**

AI-assisted development tools have fundamentally changed software economics. Research demonstrates:

- Developers using AI coding assistants complete tasks [**26-55% faster**](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/) than those without
- [**99% of developers**](https://www.atlassian.com/blog/developer/developer-experience-report-2025) now report time savings from AI tools, with 68% saving more than 10 hours per week
- [**41% of all code**](https://survey.stackoverflow.co/2025/ai) is now AI-generated, with 84% of developers using AI tools regularly
- AI tools automate significant portions of code generation, testing, and documentation that previously required manual effort

These productivity gains represent real cost reductions that vendors are realizing. **California taxpayers should share in these savings.**

**Policy: AI Productivity Disclosure**

All vendor proposals for software development, data engineering, and technology implementation must include:

1. **AI Tool Disclosure:** Identify AI coding assistants, automation tools, and generative AI systems that will be used in delivery (e.g., GitHub Copilot, Claude, Cursor, automated testing frameworks)

2. **Productivity Assumption:** State the assumed productivity gain from AI tools and how this is reflected in pricing. Vendors claiming no productivity benefit must justify why.

3. **Labor Hour Transparency:** For time-and-materials or labor-hour contracts, proposals must:
   - Distinguish between tasks performed with AI assistance vs. manual-only work
   - Apply appropriate rate differentials reflecting AI-augmented productivity
   - Demonstrate that AI efficiency gains are passed through to the State, not retained as margin

**Evaluation Criteria:**

Proposals that ignore AI productivity gains or price as if it were 2019 will receive lower technical scores. Evaluators will assess:

- **Credibility of productivity assumptions:** Does the vendor demonstrate understanding of AI tool capabilities?
- **Pass-through of savings:** Are AI efficiency gains reflected in lower prices, or absorbed as margin?
- **Quality safeguards:** Does the vendor have appropriate review processes for AI-generated code? ([Studies show](https://linearb.io/blog/is-github-copilot-worth-it) AI-generated code can have higher defect rates without proper review)
- **Transparency:** Is the vendor forthcoming about AI tool usage and its impact on delivery?

**Quality and Security Safeguards:**

AI-assisted development introduces specific risks that vendors must address:

- **Code Review Requirements:** All AI-generated code must undergo human review before deployment. "Vibe coding" (accepting AI output without understanding it) is not acceptable for State systems.
- **Security Scanning:** AI-generated code must pass security scanning before deployment
- **Technical Debt Management:** Vendors must demonstrate processes to prevent AI-generated technical debt from accumulating
- **Accountability:** Vendors remain fully responsible for code quality regardless of AI assistance; AI tools do not shift liability

**Rationale:**

The State pays for outcomes, not effort. If AI tools allow a developer to accomplish in 4 hours what previously took 8 hours, California should not pay for 8 hours of labor. Vendors that have invested in AI tooling and workforce training should be rewarded with competitive advantage—but not by charging legacy rates while pocketing AI-driven margin.

This policy:
- **Protects taxpayers** by ensuring public funds reflect current technology economics
- **Rewards innovation** by favoring vendors who effectively leverage AI
- **Maintains quality** by requiring appropriate safeguards for AI-assisted work
- **Creates transparency** so the State understands how its systems are being built

**Verification and Enforcement:**

| Mechanism | Description |
|-----------|-------------|
| **Proposal Review** | Evaluation teams score AI disclosure quality; missing or implausible disclosures reduce technical scores |
| **Contract Provisions** | Task orders include AI disclosure as deliverable requirement; false disclosure = material breach |
| **Audit Rights** | State retains right to review vendor tooling, commit histories, and productivity metrics during contract performance |
| **Sampling Reviews** | TMO conducts random quarterly reviews of 5-10% of active task orders; verifies AI disclosure accuracy |
| **Remedies** | Unsupported productivity claims may result in: (1) price adjustments, (2) reduced scope, (3) exclusion from future pools |

**Acceptable Productivity Ranges:**

| Work Type | Expected AI Benefit | Low Claim Flag |
|-----------|--------------------| ---------------|
| Standard web/mobile development | 25-40% | <10% requires justification |
| Data engineering/ETL | 20-35% | <10% requires justification |
| Legacy system maintenance | 10-25% | <5% requires justification |
| Security/compliance work | 15-30% | <10% requires justification |
| Custom/specialized development | 15-30% | <10% requires justification |

*Note: Vendors claiming minimal AI benefit must provide written justification (security restrictions, highly specialized domain, primarily non-coding work). TMO reviews and may challenge unsupported claims.*

**Transition for Existing Contracts:**

- New task orders under existing frameworks: AI disclosure required immediately
- Contract renewals/extensions: AI disclosure required at renewal
- Existing active task orders: Voluntary disclosure encouraged; not mandatory until next modification

---

### Summary: The New Procurement Model

| Old Model | New Model |
|-----------|-----------|
| 18-24 month procurement cycles | 10 days to 10 weeks depending on complexity |
| Detailed specs written before knowing solution | Problem statements; vendors prove solutions work |
| One giant contract, one vendor | Modular contracts ($15M cap), multiple vendors, competition at each phase |
| Procurement separate from delivery | Procurement embedded in PDL stage-gates |
| Central procurement bottleneck | Delegated authority to trained E3 CDDs and product teams |
| Written proposals evaluated | Working prototypes demonstrated |
| Risk transferred to State at contract signing | Risk validated through paid sprints before commitment |
| 2019 pricing assumptions | AI-era pricing reflecting productivity gains |
| AI adoption waits for annual budget cycles | AI solutions acquired rapidly as capabilities mature |

---

> This document is part of the California Enterprise Modernization recommendation. See also:
> - [Executive Summary](executive-summary.md) — Start here for an overview
> - [Governance Model](governance-model.md) — E3 structure and leadership
> - [Data Governance](data-governance.md) — Independent Office and data sharing
> - [Talent Development](talent-development.md) — Fellowship program and workforce development
> - [Funding & Implementation](funding.md) — Breakthrough Fund structure
> - [Templates](../appendices/templates.md) — Fillable forms and templates
> - [Operational Guides](../appendices/operational-guides.md) — Program guides and frameworks
> - [Technical Appendices](../appendices/technical-standards.md) — Technical standards and architecture
> - [Budget and Governance](../appendices/budget-models.md) — Budget models and change management

---

## Version History

| Version | Date | Description | Author |
|---------|------|-------------|--------|
| Executive Draft v1.2 | December 8, 2025 | Updated framing to proposal/recommendation language; removed "Document Owner" footer line | Brent Vanderburgh |
| Executive Draft v1.1 | December 8, 2025 | Updated version numbering and added document owner | Brent Vanderburgh |
| Executive Draft v1.0 | December 2025 | Initial executive draft incorporating modular contracting, RFI² innovation, and AI-era pricing | Brent Vanderburgh |

---

**Document Version:** Executive Draft v1.5
**Date:** December 8, 2025
**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency

---

*End of California Enterprise Modernization Plan - Procurement Guide*
