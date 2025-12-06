# California Enterprise Modernization Plan
## Part 1 Continuation: Sections 3-4

**Date:** December 2025  
**Version:** Executive draft v1.0

---

## 3. Independent Office of State Data Governance

### 3.1 Constitutional Model and Precedent

The Independent Office of State Data Governance follows California's Little Hoover Commission model: cross-branch appointments, staggered terms, statutory authority, and independence from any single agency.

**Why Independence Matters:**
- E3 leaders need enforceable data sharing authority, not just coordination roles
- Single-agency governance (e.g., within GovOps) lacks legitimacy across other cabinet agencies
- Legislative/judicial branches require data too; executive-only governance excludes them
- Political transitions shouldn't reset data governance; institutional continuity essential

### 3.2 Board Composition (9 Members Minimum)

**Required Seats:**
1. Governor appointment #1
2. Governor appointment #2  
3. Senate Rules Committee appointment
4. Assembly Speaker appointment
5. Judicial Council appointment
6. UC Regents representative
7. CSU Board representative
8. **Public seat (REQUIRED)** - citizen perspective, accountability
9. **Breakthrough partner / digital industry representative (REQUIRED)** - private sector expertise, co-learning

**Chief Technical Officer Requirement:**  
Each board seat must have an assigned Chief Technical Officer (CTO) who provides technical expertise, reviews standards, and advises their appointing member. CTOs ensure board decisions are technically sound and implementable.

**Term Structure:**
- Staggered 3-year terms
- Survives administration transitions
- Cross-branch legitimacy

### 3.3 Authority and Responsibilities

**Binding Powers:**
- Set statewide data standards (schemas, formats, quality rules)
- Approve/mandate data sharing frameworks
- Convene all branches for policy development
- Enforce compliance through budget/procurement mechanisms

**Key Functions:**
- Develop statewide data architecture
- Resolve inter-agency data disputes
- Protect privacy while enabling sharing
- Annual reporting to Legislature

### 3.4 Data Sharing Agreement Templates

**Why Four Template Types Matter:**

Data sharing negotiations currently take 18 months because every agreement is custom. Standardized templates reduce this to 4-8 weeks by providing pre-approved legal language, technical specifications, and risk mitigation approaches for common scenarios.

**Template 1: Public Data Exchange**
- **Use Case:** Sharing non-sensitive data between state agencies for operational purposes (e.g., business registry data, public facility locations, aggregate statistics)
- **Key Features:** Simple MOU, minimal restrictions, attribution requirements, update frequency specified
- **Approval Time:** 2-4 weeks (department-level approval sufficient)
- **Example:** DMV shares aggregate vehicle registration data with Air Resources Board for emissions modeling

**Template 2: Confidential Data with Limited PII**
- **Use Case:** Sharing data containing some PII but not highly sensitive (e.g., permit applications, licensing records, low-risk health data)
- **Key Features:** Data Use Agreement (DUA), access controls, audit logging, breach notification procedures, retention limits
- **Approval Time:** 4-6 weeks (requires Chief Deputy Director + data governance team review)
- **Example:** Occupational Safety shares workplace injury reports with Public Health for epidemiological analysis (PII minimized)

**Template 3: Sensitive Data Requiring Enhanced Protection**
- **Use Case:** Highly sensitive PII or protected classes (criminal justice, child welfare, mental health, financial information)
- **Key Features:** Enhanced DUA, role-based access, encryption requirements, independent privacy review, limited retention, strict purpose limitation
- **Approval Time:** 6-8 weeks (requires Undersecretary + Independent Office privacy review)
- **Example:** Corrections shares inmate release data with Social Services for reentry support program eligibility

**Template 4: Cross-Branch or External Entity Sharing**
- **Use Case:** Sharing between executive/legislative/judicial branches or with federal/local governments, academic institutions, or (rarely) private entities
- **Key Features:** Formal inter-branch agreement, explicit statutory authority cited, strict purpose limitation, public transparency requirements, sunset clauses
- **Approval Time:** 8-12 weeks (requires Independent Office board approval)
- **Example:** Executive branch shares arrest data with Judicial Council for pretrial release research; or sharing Medi-Cal data with federal HHS for program oversight

**Benefits of Templates:**
- **Speed:** 90% reduction in negotiation time
- **Legal clarity:** Pre-vetted language reduces risk
- **Consistency:** Similar use cases treated similarly
- **Transparency:** Public can see standard terms
- **Scalability:** New agreements use proven patterns

---

## 4. Product-Led Delivery Framework

### 4.1 Service Mesh Architecture

**Vision:** Replace monolithic point-to-point integrations with service mesh where every system exposes APIs and discovers services through a catalog.

**API Standards:**
- RESTful APIs with OpenAPI 3.0+ specs
- OAuth 2.0 authentication
- Agency API catalogs for discovery
- Semantic versioning, backward compatibility
- Rate limiting and monitoring

**Implementation:**
1. Pilot with high-value cross-agency services
2. Mandate for all new procurements
3. Retrofit legacy with API wrappers
4. TMO maintains statewide catalog

### 4.2 Citizen Journey Teams

**Organizing Around Life Events:**

Traditional government organizes around agencies. Citizens experience life events that require multiple agencies:
- Having a baby (Health, Vital Records, Social Services, Tax)
- Starting a business (Secretary of State, Tax, Licensing, Permitting)
- Disaster recovery (Emergency Services, Housing, Insurance, Small Business)

Citizen Journey Teams bring together E3 leaders, SMEs, and Fellows from relevant agencies to redesign experiences around these journeys, creating seamless integrated services.

### 4.3 Modular Contracting with California Context

**California's Procurement Evolution:**

California Department of Technology (CDT) has pioneered modern procurement approaches since 2022:
- **Modular Partnership:** Breaking large systems into vendor-independent modules
- **Challenge-Based (RFI²):** Problem statements instead of prescriptive specs
- **eVAQ:** Pre-qualified vendor pools for rapid task orders
- **Modern RFP:** Phased approach with down-selection and negotiation

**The $10 Million Contract Cap:**

The E3 plan establishes $10M as maximum IT contract value to force modularization and reduce risk.

**How $40M Project Works Under $10M Cap:**

**Scenario:** Department needs new case management system estimated at $40M over 3 years.

**Traditional Approach (Single $40M Contract):**
- One vendor, one contract, all-or-nothing
- 18-24 month procurement cycle
- High risk: vendor failure = project failure
- Limited competition: only large system integrators can bid
- Change orders expensive and time-consuming

**Modular Approach (Four $10M Contracts):**

**Contract 1 ($10M): Core Platform**
- Procure foundational infrastructure: database, authentication, user management, API gateway
- Award to vendor with best platform expertise
- Deliverable: Working platform ready for module integration
- Timeline: Months 1-12

**Contract 2 ($10M): Data Migration and Integration**
- Migrate legacy data to new platform
- Build APIs connecting to related systems
- Award to vendor with data migration expertise (may be different vendor)
- Deliverable: Legacy data migrated, systems integrated via APIs
- Timeline: Months 7-18 (overlaps with Contract 1)

**Contract 3 ($10M): User-Facing Applications**
- Build citizen-facing portal and mobile app
- Build staff case management interfaces
- Award to vendor with UX/UI and agile development expertise
- Deliverable: Working applications for citizens and staff
- Timeline: Months 13-24 (after platform ready)

**Contract 4 ($10M): Advanced Features and Support**
- Add analytics, reporting, workflow automation
- Provide 2-year operations and maintenance
- Award to best-value vendor for ongoing support
- Deliverable: Enhanced capabilities and sustained operations
- Timeline: Months 19-36

**Managing Overhead and Integration:**

**Challenge:** Multiple vendors increase coordination costs and integration complexity.

**Mitigation Strategies:**

1. **Integration Architect (Department Staff or Small Contract):**
   - Dedicated technical lead ensures modules integrate properly
   - Defines interface specifications before module procurements
   - Reviews vendor designs for compatibility
   - Chairs weekly vendor coordination meetings

2. **API-First Architecture:**
   - All contracts require well-documented APIs
   - Integration through APIs (not tight coupling) reduces coordination
   - Modules can be tested independently before integration

3. **Phased Procurement:**
   - Later contracts benefit from lessons learned in earlier contracts
   - Vendor performance in Contract 1 informs Contract 2-4 vendor selection
   - Requirements refined based on actual platform capabilities

4. **Shared Development Environment:**
   - Department provides unified dev/test environment
   - All vendors work in same environment
   - Integration issues detected early

**Cost Overrun Protection:**

**Traditional Approach Risk:**
- $40M contract has cost overruns
- Vendor submits $15M change order
- Department has no leverage (sunk cost, vendor lock-in)
- Total cost: $55M (38% overrun)

**Modular Approach Protection:**
- Contract 1 has cost overruns
- Department caps overruns at $2M (keeps within $10M envelope or adjusts scope)
- Contracts 2-4 not yet awarded; can adjust scope or budget
- If Contract 1 vendor performs poorly, select different vendors for 2-4
- Total cost controlled to original $40M by scope adjustments across contracts

**Phased Funding Management:**

California budget process requires multi-year appropriations for projects over $5M.

**Year 1 Budget:** $15M appropriated
- Contract 1: $10M awarded and underway
- Contract 2: $5M initial funding, full award pending Year 2 appropriation

**Year 2 Budget:** $15M appropriated  
- Contract 2: Remaining $5M funded
- Contract 3: $10M awarded

**Year 3 Budget:** $10M appropriated
- Contract 4: $10M awarded

**Benefit:** If budget constraints emerge or project priorities shift, future contracts can be delayed, descoped, or cancelled without forfeiting sunk costs in completed modules. Completed modules (Contracts 1-2) still provide value even if Contracts 3-4 are deferred.

**Small Business Participation:**

Modular contracting enables small firms to compete:
- Small firms cannot bid $40M contracts but CAN bid $10M modules
- Contracts 1-3 could go to small/medium vendors
- Contract 4 (O&M support) ideal for small local firms
- Increased competition drives better pricing and innovation

### 4.4 RFI²: Request for Innovative Ideas

California CDT has established RFI² (challenge-based procurement) where departments state problems and vendors propose solutions.

**E3 Expansion of RFI²:**
- Mandatory for all E3-funded projects over $2M
- TMO provides RFI² template and facilitation
- ODI CalInnovate supports problem definition through user research
- Pilot competitions before production awards reduce risk

**Process:**
1. Problem definition (user research, success metrics)
2. Vendor concept papers (5-10 pages)
3. Down-select to 2-3 finalists
4. Paid pilots with real data
5. Award to best-performing pilot

---

*Continued in Part 2: Technology Architecture, Procurement Innovation, Talent Development*  
*Continued in Part 3: Breakthrough Modernization Fund, Implementation Roadmap*
