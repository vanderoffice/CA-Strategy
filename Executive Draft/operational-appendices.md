# California Enterprise Modernization Plan
## Operational Appendices

**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency
**Date:** December 2025
**Version:** Executive Draft v1.0

---

> This document is part of the California Enterprise Modernization recommendation. See also:
> - [Recommendation Brief](recommendation-brief.md) — Executive summary and recommended actions
> - [Strategy Document](strategy-document.md) — Governance, delivery framework, talent, and implementation
> - [Procurement Guide](procurement-guide.md) — Technology and procurement innovation
> - [Technical Appendices](technical-appendices.md) — Standards, assessments, and reference materials

---

## Table of Contents

- [Appendix A: Sample Templates and Frameworks](#appendix-a-sample-templates-and-frameworks)
  - A.1 E3 Position Description Template
  - A.2 Data Sharing Agreement Template (Type 3: Moderate Sensitivity)
  - A.3 OKR Template
  - A.4 Project Stage-Gate Template
  - A.5 Delegated Ordering Authority Template
  - A.6 Standard Agile Task Order Template
  - A.7 Rapid RFI² Problem Statement Template
  - A.8 AI Productivity Disclosure Template
  - A.9 Rapid RFI² Operational Guide
  - A.10 Fellowship Program Curriculum
  - A.11 Breakthrough Fund Sustainability Model

---

## Appendix A: Sample Templates and Frameworks

### A.1 E3 Position Description Template

**Position Title:** Undersecretary for Efficiency and Effectiveness

**Department/Agency:** [Agency Name]

**Reports to:** Agency Secretary

**Salary Range:** [Based on negotiated executive compensation]

**Position Summary:**
The Undersecretary for Efficiency and Effectiveness serves as the Agency's senior leader for technology modernization, business process optimization, data governance, and operational effectiveness. This position holds explicit authority over technology investments, data sharing mandates, and performance management across all departments within the Agency.

**Essential Functions:**

1. **Strategic Leadership (30%)**
   - Define agency-wide modernization vision and roadmap
   - Set performance targets for digital service adoption, legacy system reduction, cost efficiency
   - Represent agency on Statewide E3 Council
   - Serve as primary voting member of Independent Data Governance Office councils

2. **Technology Governance (25%)**
   - Approve technology architectures, vendor selections, major procurements over $5M
   - Enforce enterprise architecture standards and API-first requirements
   - Oversee cloud migration and data center consolidation
   - Direct service mesh architecture implementation

3. **Data Governance (20%)**
   - Chair Agency Data Governance Council
   - Approve data sharing agreements
   - Ensure CCPA compliance and ethical AI use
   - Mandate data quality standards and master data management

4. **Performance Management (15%)**
   - Define and track agency-level KPIs
   - Conduct quarterly reviews with Chief Deputy Directors
   - Publish transparent performance dashboards
   - Report progress to Agency Secretary and Governor's Office

5. **Team Leadership (10%)**
   - Oversee Governor's Innovation Fellows in agency
   - Identify candidates for Chief Deputy Director positions
   - Sponsor training and culture change initiatives
   - Build coalition for modernization across agency

**Required Qualifications:**

**Preferential Hiring:**
- Completion of Governor's Innovation Fellowship with demonstrated delivery of measurable modernization outcomes

**OR**

**Alternative Path:**
- 10+ years progressive technology leadership experience in large, complex organizations (5,000+ employees, $500M+ budget)
- Proven track record delivering digital transformation initiatives on time and budget
- 5+ years executive management experience with P&L or operational responsibility

**Additional Requirements:**
- Deep understanding of technology architecture, data governance, and agile delivery methods
- Exceptional change management and stakeholder engagement skills
- Understanding of government operations, procurement, policy development, and budget processes
- Executive presence and ability to influence Cabinet-level leadership
- Demonstrated ability to build and lead cross-functional teams
- Strong analytical and problem-solving capabilities

**Desirable Qualifications:**
- Government experience (state, federal, or large local)
- Formal education in computer science, engineering, business, or public administration
- Professional certifications (PMP, TOGAF, ITIL, Agile/Scrum)
- Experience with California state government systems and culture

**Authorities:**
- Final approval on technology investments exceeding $5M
- Authority to mandate cross-department data sharing within agency
- Ability to reassign resources across departments for strategic initiatives
- Direct escalation path to Agency Secretary for barrier removal
- Voting authority in Independent Data Governance Office board decisions
- Sign-off requirement for all IT contracts over $1M

**Performance Metrics:**
- Digital service adoption rate (target: 75% by Year 5)
- Legacy system reduction (target: 40% by Year 5)
- Cost savings and avoidance (target: $50M+ annually by Year 3)
- Citizen satisfaction score (target: 85%+ by Year 5)
- Data sharing agreements executed (target: 10+ annually)
- API publication and adoption (target: 50+ APIs by Year 3)

**Compensation:**
- Base salary competitive with private sector for equivalent executive role
- Performance bonuses tied to achievement of modernization KPIs
- Professional development budget for continuous learning
- Standard executive benefits package

---

### A.2 Data Sharing Agreement Template (Type 3: Moderate Sensitivity)

**CALIFORNIA STATE GOVERNMENT DATA SHARING AGREEMENT**

**Agreement Number:** DSA-[YYYY]-[###]

**Effective Date:** [Date]

**Parties:**
- **Data Provider:** [Agency/Department Name]
- **Data Consumer:** [Agency/Department Name]

**1. PURPOSE AND SCOPE**

**1.1 Purpose:**
This agreement enables [Data Consumer] to access [describe data] from [Data Provider] for the purpose of [specific use case with legal authority citation].

**1.2 Legal Authority:**
[Cite specific statutes, regulations, or executive orders authorizing data sharing]

**1.3 Scope:**
This agreement covers the following data elements:
- [Specific fields/tables/datasets]
- [Refresh frequency: real-time, daily, weekly, monthly]
- [Historical depth: current only, 1 year, 5 years, all available]

**2. DATA ELEMENTS AND SPECIFICATIONS**

**2.1 Data Elements:**
[Detailed list of fields, data types, formats]

**2.2 Data Quality Standards:**
Provider warrants that shared data meets the following quality standards:
- Accuracy: 98%+ verified correct
- Completeness: 95%+ of required fields populated
- Timeliness: Updated within [timeframe]
- Consistency: Aligned with master data definitions

**2.3 Technical Specifications:**
- **Delivery Method:** [API, SFTP, direct database access]
- **Data Format:** [JSON, XML, CSV, other]
- **Encryption:** [TLS 1.3 in transit, AES-256 at rest]
- **Authentication:** [OAuth 2.0, mutual TLS, API key]

**3. SECURITY AND PRIVACY**

**3.1 Privacy Impact Assessment:**
A Privacy Impact Assessment has been completed and approved by both parties' privacy officers. [Reference PIA document number]

**3.2 Security Controls:**
- Data encryption in transit and at rest
- Access restricted to authorized users only (role-based access control)
- Audit logging of all data access (retained for 7 years)
- Annual security reviews and penetration testing
- Immediate breach notification (within 24 hours)

**3.3 CCPA Compliance:**
Both parties warrant compliance with California Consumer Privacy Act:
- Data minimization: Only data necessary for stated purpose
- Purpose limitation: Data used only for stated purpose
- Retention limits: Data retained only as long as legally required
- Citizen rights: Support for access, correction, deletion requests

**3.4 Prohibited Uses:**
Data Consumer shall NOT:
- Share data with third parties without written consent
- Use data for purposes other than stated above
- Combine data with other sources in ways that increase privacy risk
- Sell or commercialize the data

**4. ROLES AND RESPONSIBILITIES**

**4.1 Data Provider Responsibilities:**
- Maintain data quality per standards in Section 2.2
- Provide technical support for integration issues
- Notify Consumer of data schema changes (30 days advance notice)
- Maintain security controls per Section 3.2
- Respond to data quality issues within [SLA timeframe]

**4.2 Data Consumer Responsibilities:**
- Use data only for stated purpose
- Maintain security controls per Section 3.2
- Report data quality issues promptly
- Comply with all privacy and security requirements
- Train staff on appropriate data use

**4.3 Data Steward Contacts:**

**Provider:**
- Name: [Name]
- Title: [Title]
- Email: [Email]
- Phone: [Phone]

**Consumer:**
- Name: [Name]
- Title: [Title]
- Email: [Email]
- Phone: [Phone]

**5. TERM AND TERMINATION**

**5.1 Term:**
This agreement is effective [Start Date] and continues for [Duration: 1 year, 3 years, ongoing] unless terminated earlier per Section 5.2.

**5.2 Termination:**
Either party may terminate with 60 days written notice. Immediate termination allowed for:
- Material breach of security or privacy provisions
- Legal prohibition on data sharing
- Change in legal authority supporting agreement

**5.3 Post-Termination:**
Upon termination, Data Consumer shall:
- Cease accessing data immediately
- Securely delete or return all copies of data
- Certify completion of deletion within 30 days
- Exception: May retain data if legally required with documentation

**6. DISPUTE RESOLUTION**

**6.1 Escalation Path:**
- Level 1: Data Stewards attempt resolution (5 business days)
- Level 2: Department Chief Deputy Directors for E3 (10 business days)
- Level 3: Agency Undersecretaries for E3 (15 business days)
- Level 4: Independent Data Governance Office CDO (final resolution)

**6.2 Amendment Process:**
Amendments require written consent of both parties' authorized signatories and review by legal counsel.

**7. COMPLIANCE AND AUDIT**

**7.1 Compliance Monitoring:**
Both parties shall maintain records demonstrating compliance with this agreement, including:
- Access logs
- Data quality reports
- Security incident reports
- Privacy assessment updates

**7.2 Audit Rights:**
Each party may audit the other's compliance annually with 30 days notice. Independent Data Governance Office may audit at any time.

**8. SIGNATURES**

**Data Provider:**

Signature: ___________________________
Name: [Name]
Title: [Title - must be Agency Undersecretary or delegated authority]
Date: ___________________________

**Data Consumer:**

Signature: ___________________________
Name: [Name]
Title: [Title - must be Agency Undersecretary or delegated authority]
Date: ___________________________

**Approved:**

Independent Office of State Data Governance
Signature: ___________________________
Name: [Chief Data Officer Name]
Date: ___________________________

---

### A.3 OKR Template

**Statewide Objective (Example: Year 1, Quarter 2)**

**Objective:** Establish foundational E3 governance and demonstrate early value

**Key Result 1:** Deploy Undersecretary positions in 4 priority agencies with onboarding complete
- **Measure:** 4 positions filled and onboarded by June 30, 2026
- **Owner:** GovOps, ODI
- **Status:** [In Progress / On Track / At Risk / Completed]
- **Current Score:** [0.0 - 1.0]

**Key Result 2:** Launch 10 pilot projects with at least 3 showing measurable improvements
- **Measure:** 3+ pilots demonstrating 20%+ efficiency gains or citizen satisfaction improvements
- **Owner:** TMO
- **Status:** [In Progress / On Track / At Risk / Completed]
- **Current Score:** [0.0 - 1.0]

**Key Result 3:** Achieve 500 employees enrolled in Digital Accelerators program
- **Measure:** 500 enrollments across all tracks
- **Owner:** CDT, CalHR
- **Status:** [In Progress / On Track / At Risk / Completed]
- **Current Score:** [0.0 - 1.0]

**Overall Objective Score:** [Average of Key Result scores]

**Lessons Learned:**
[What worked well? What didn't? What would we do differently?]

**Next Quarter Implications:**
[How does this quarter's performance inform next quarter's priorities?]

---

### A.4 Project Stage-Gate Template

**Gate 0: Concept Approval**

**Requirements:**
- Problem statement and business need
- Alignment with E3 priorities
- Rough order of magnitude cost estimate
- Preliminary benefits estimate
- Executive sponsor identified

**Approval Authority:** Chief Deputy Director for E3 (department level) or Undersecretary (agency level)

**Outputs:** Project charter, assigned project manager

---

**Gate 1: Feasibility**

**Requirements:**
- Detailed business case with cost-benefit analysis
- Stakeholder analysis and engagement plan
- Technology options analysis
- Risk assessment
- Resource requirements (staff, budget, timeline)
- Preliminary architecture (if IT project)

**Approval Authority:** Undersecretary for E3 (projects over $5M require TMO portfolio review)

**Outputs:** Approved business case, budget allocation

---

**Gate 2: Design Approval**

**Requirements:**
- Detailed design documentation
- Architecture review board approval (if IT project)
- Independent Data Office compliance review (if data sharing involved)
- Security and privacy review
- Procurement strategy
- Change management plan
- Testing and acceptance criteria

**Approval Authority:** Undersecretary for E3, TMO (for cross-agency dependencies), Architecture Review Board (technical), Independent Data Office (data governance)

**Outputs:** Approved detailed design, procurement authorization

---

**Gate 3: Implementation Readiness**

**Requirements:**
- Vendor selection completed (if applicable)
- Detailed project plan with milestones
- Resource assignments finalized
- Training plan developed
- Communication plan finalized
- Risk mitigation plans in place
- Success metrics and monitoring defined

**Approval Authority:** Undersecretary for E3, TMO

**Outputs:** Implementation authorization, project kickoff

---

**Gate 4: Go-Live Approval**

**Requirements:**
- Testing completed successfully (unit, integration, user acceptance)
- Training completed
- Documentation finalized
- Cutover plan approved
- Rollback plan in place
- Support model established
- Performance baseline captured

**Approval Authority:** Undersecretary for E3, Chief Deputy Director, Department Director (if major system)

**Outputs:** Go-live authorization, production deployment

---

**Gate 5: Benefits Realization**

**Requirements:**
- Post-implementation review completed (90 days after go-live)
- Benefits realization measurement against baseline
- Lessons learned documented
- Sustainability plan in place
- Handoff to operations completed
- Project closure report

**Approval Authority:** E3 Undersecretary, TMO

**Outputs:** Project closure, benefits documented for Breakthrough Fund reporting

---

### A.5 Delegated Ordering Authority Template

**CALIFORNIA STATE GOVERNMENT DELEGATED ORDERING AUTHORITY**

**Document Number:** DOA-[YYYY]-[###]

**Effective Date:** [Date]

**Delegated Official:**
- Name: [Name]
- Title: [Title]
- Department: [Department]
- Agency: [Agency]

**1. SCOPE OF AUTHORITY**

**1.1 Delegation Level:**
- [ ] **Product Owner Level:** Task orders up to $500K
- [ ] **E3 Chief Deputy Director Level:** Task orders up to $2M
- [ ] **E3 Undersecretary Level:** Task orders up to $5M

**1.2 Authorized Framework Categories:**
- [ ] Agile Digital Services
- [ ] Data & Analytics
- [ ] Cloud & Platform
- [ ] Cybersecurity
- [ ] Change Management
- [ ] All Categories

**1.3 Limitations:**
- Authority valid only for task orders under pre-qualified Enterprise Vendor Pools
- Must comply with modular contracting principles ($15M cap per contract)
- Small business requirements must be met (Tier 1 first consideration for <$1M)
- AI-era pricing expectations apply to all software development task orders

**2. CONDITIONS AND REQUIREMENTS**

**2.1 Training Completion:**
The delegated official has completed required training in:
- [ ] Modular contracting principles (Date: _______)
- [ ] Rapid RFI² process (Date: _______)
- [ ] Vendor pool usage (Date: _______)
- [ ] Small business requirements (Date: _______)
- [ ] AI-era pricing expectations (Date: _______)
- [ ] Ethics and compliance (Date: _______)

**2.2 Project Envelope:**
This delegation applies within the following approved project envelope:
- Project Name: [Project Name]
- Total Approved Budget: $[Amount]
- Budget Period: [Start Date] to [End Date]
- TMO Portfolio ID: [ID Number]

**3. OVERSIGHT AND REPORTING**

**3.1 Reporting Requirements:**
- All task orders logged in TMO portfolio system within 5 business days of award
- Quarterly summary report to supervising E3 Undersecretary
- Immediate notification of any task order modifications exceeding 10% of original value

**3.2 Performance Metrics:**
Delegation subject to periodic review based on:
- Competition rates (target: 80%+ of eligible orders competitively awarded)
- Cycle time (target: meeting speed targets in Section 6.2)
- Small business utilization (target: 25%+ to Tier 1 vendors)
- Audit findings (zero material findings)

**3.3 Revocation:**
This delegation may be revoked for:
- Material audit findings
- Pattern of non-compliance with requirements
- Failure to meet performance metrics
- Organizational changes affecting delegated official's role

**4. SIGNATURES**

**Delegated Official:**

Signature: ___________________________
Name: [Name]
Title: [Title]
Date: ___________________________

**Delegating Authority:**

Signature: ___________________________
Name: [Name]
Title: [E3 Undersecretary / E3 Chief Deputy Director]
Date: ___________________________

**TMO Acknowledgment:**

Signature: ___________________________
Name: [TMO Director or Designee]
Date: ___________________________

---

### A.6 Standard Agile Task Order Template

**CALIFORNIA STATE GOVERNMENT AGILE TASK ORDER**

**Task Order Number:** TO-[Framework]-[YYYY]-[###]

**Framework:** [Agile Digital Services / Data & Analytics / Cloud & Platform / Cybersecurity / Change Management]

**Issuing Department:** [Department Name]

**1. BASIC INFORMATION**

| Field | Value |
|-------|-------|
| **Task Order Title** | [Descriptive Title] |
| **Vendor** | [Vendor Name from Pool] |
| **Vendor Tier** | [ ] Tier 1 (Small/DVBE) [ ] Tier 2 (Medium) [ ] Tier 3 (Large) |
| **Period of Performance** | [Start Date] to [End Date] |
| **Total Value** | $[Amount] |
| **Procurement Type** | [ ] Standard On-Ramp [ ] RFI² Sprint Award |
| **PDL Gate** | [ ] Gate 0 [ ] Gate 1 [ ] Gate 2 [ ] Gate 3 [ ] Gate 4-5 |

**2. PROBLEM STATEMENT AND OUTCOMES**

**2.1 Problem Statement:**
[Clear, concise description of the problem to be solved. Focus on outcomes, not technologies. 2-3 paragraphs maximum.]

**2.2 Success Metrics:**

| Metric | Current Baseline | Target | Measurement Method |
|--------|-----------------|--------|-------------------|
| [Metric 1] | [Value] | [Value] | [How measured] |
| [Metric 2] | [Value] | [Value] | [How measured] |
| [Metric 3] | [Value] | [Value] | [How measured] |

**3. SCOPE OF WORK**

**3.1 In Scope:**
- [Specific deliverable or activity 1]
- [Specific deliverable or activity 2]
- [Specific deliverable or activity 3]

**3.2 Out of Scope:**
- [Explicitly excluded item 1]
- [Explicitly excluded item 2]

**3.3 Sprint Cadence:**
- Sprint Duration: [2 weeks / 3 weeks / 4 weeks]
- Sprint Reviews: [Day/Time]
- Retrospectives: [Frequency]

**4. TEAM AND COLLABORATION EXPECTATIONS**

**4.1 Vendor Team:**
| Role | Name | Hours/Week |
|------|------|------------|
| [Role] | [Name] | [Hours] |

**4.2 State Team:**
| Role | Name | Availability |
|------|------|--------------|
| Product Owner | [Name] | [Hours/week] |
| Technical Lead | [Name] | [Hours/week] |
| SME | [Name] | [As needed] |

**4.3 Collaboration Requirements:**
- Daily standups: [Time/Platform]
- Sprint planning: [Day/Time]
- Access to State systems: [List systems and access level]
- Working location: [Remote / Hybrid / On-site requirements]

**5. DELIVERABLES AND ACCEPTANCE CRITERIA**

| Deliverable | Due Date | Acceptance Criteria |
|-------------|----------|---------------------|
| [Deliverable 1] | [Date] | [Specific, measurable criteria] |
| [Deliverable 2] | [Date] | [Specific, measurable criteria] |
| [Deliverable 3] | [Date] | [Specific, measurable criteria] |

**6. PERFORMANCE MEASURES AND REPORTING**

**6.1 Progress Reporting:**
- Weekly status reports due [Day]
- Sprint demos with recorded demonstrations
- Monthly executive summary to E3 CDD

**6.2 Quality Metrics:**
- Code coverage: [Target %]
- Defect rate: [Target]
- User acceptance: [Target %]

**7. AI TOOL DISCLOSURE** *(Required per Section 6.10)*

**7.1 AI Tools to Be Used:**

| Tool | Purpose | Productivity Impact |
|------|---------|---------------------|
| [e.g., GitHub Copilot] | [Code generation] | [Estimated % efficiency gain] |
| [e.g., Claude] | [Documentation] | [Estimated % efficiency gain] |

**7.2 Quality Safeguards:**
- [ ] All AI-generated code will undergo human review before deployment
- [ ] Security scanning will be performed on all code including AI-assisted code
- [ ] Technical debt monitoring process is in place
- [ ] Vendor retains full accountability for code quality

**7.3 Pricing Reflection:**
[Brief statement of how AI productivity gains are reflected in the proposed pricing]

**8. COMMERCIAL TERMS**

**8.1 Pricing:**

| Cost Element | Amount |
|--------------|--------|
| Labor | $[Amount] |
| Other Direct Costs | $[Amount] |
| **Total Fixed Price / NTE** | **$[Amount]** |

**8.2 Payment Terms:**
- [ ] Fixed Price: Payment upon acceptance of deliverables
- [ ] Time and Materials: Monthly invoicing against actuals
- [ ] Milestone-Based: [List milestones and payment amounts]

**8.3 Modification Process:**
- Scope changes require written approval from [Authority Level]
- Changes >10% of task order value require TMO notification

**9. SIGNATURES**

**State Authorized Representative:**

Signature: ___________________________
Name: [Name]
Title: [Title]
Date: ___________________________

**Vendor Authorized Representative:**

Signature: ___________________________
Name: [Name]
Title: [Title]
Date: ___________________________

---

### A.7 Rapid RFI² Problem Statement Template

**CALIFORNIA STATE GOVERNMENT RAPID RFI² CHALLENGE**

**Challenge Number:** RFI2-[YYYY]-[###]

**Sponsoring Agency:** [Agency Name]

**Sponsoring Department:** [Department Name]

**Challenge Manager:** [Name, TMO]

---

**1. THE CORE PROBLEM**

**1.1 Current State:**
[Describe the current situation in concrete, quantified terms. What is broken? How bad is it? Who is affected?]

*Example: "Staff spend 40% of time manually re-keying data from PDF forms into the case management system. This creates a 6-week backlog in benefits issuance affecting 50,000 Californians monthly."*

**1.2 Impact:**
- **Citizens affected:** [Number and description]
- **Staff time consumed:** [Hours/FTEs]
- **Cost of current state:** [$ annually]
- **Risk if unaddressed:** [Consequences of inaction]

---

**2. TARGET METRICS (Success Definition)**

| Metric | Current | Target | How Measured |
|--------|---------|--------|--------------|
| [Primary metric] | [Value] | [Value] | [Method] |
| [Secondary metric] | [Value] | [Value] | [Method] |
| [Quality metric] | [Value] | [Value] | [Method] |

*Example: "Reduce processing time from 45 days to <5 days" or "Achieve 90% auto-adjudication rate"*

---

**3. CONSTRAINTS**

**3.1 Technical Constraints:**
- Must integrate with: [List systems and APIs]
- Must comply with: [Standards - e.g., State Technology Standards, SIMM 5300]
- Data restrictions: [PII handling, data residency requirements]

**3.2 Operational Constraints:**
- Budget envelope: $[Amount] for prototype phase; $[Amount] for production
- Timeline: Prototype must be demonstrable within [X] weeks
- Users: Solution must work for [describe user population and skill levels]

**3.3 Policy Constraints:**
- Regulatory requirements: [List applicable regulations]
- Accessibility: WCAG 2.1 AA minimum
- Language support: [Required languages]

---

**4. THE CHALLENGE**

*[Write a clear, compelling challenge statement that invites innovation without prescribing solutions]*

> "We are looking for a partner to prototype a solution that demonstrates how **[user group]** can achieve **[target metric]** within **[constraints]**. We are not prescribing the technology stack, provided it adheres to State Technology Standards (Appendix H). We welcome innovative approaches including but not limited to [suggest areas of potential innovation without mandating them]."

---

**5. EVALUATION CRITERIA ("FLY-OFF" JUDGING)**

Prototypes will be evaluated by the E3 Undersecretary and Product Team based on:

| Criterion | Weight | Description |
|-----------|--------|-------------|
| **User Experience** | [X]% | Usability score from actual staff testers; intuitive workflow; accessibility compliance |
| **Technical Viability** | [X]% | Successful integration with legacy systems; API functionality; security posture |
| **Performance** | [X]% | Speed, accuracy, and reliability against target metrics |
| **Scalability** | [X]% | Ability to scale to production volumes; maintainability |
| **Innovation** | [X]% | Creative approaches; potential for broader application |

---

**6. TIMELINE**

| Phase | Duration | Dates |
|-------|----------|-------|
| Problem Statement Published | — | [Date] |
| Concept Papers Due | 2 weeks | [Date] |
| Shortlist Announced | +3 days | [Date] |
| Paid Prototype Sprint | 4-5 weeks | [Start] - [End] |
| Fly-Off Demonstrations | 1 day | [Date] |
| Award Announcement | +3 days | [Date] |

---

**7. PROTOTYPE SPRINT SUPPORT**

The State will provide shortlisted vendors with:

- **Sandbox Environment:** [Description of technical environment]
- **Sanitized Data:** [Description of test data available]
- **System Access:** [APIs, documentation, technical contacts]
- **Prototype Funding:** $50,000 per shortlisted vendor
- **Challenge Manager Support:** [Name], TMO - logistics coordination

---

**8. SUBMISSION REQUIREMENTS**

**Concept Paper (5 pages maximum):**
1. Problem Understanding (1 page): Demonstrate you understand the challenge
2. Proposed Approach (2 pages): High-level solution concept and technical approach
3. Innovation Elements (1 page): What's novel about your approach
4. Team Capabilities (1 page): Relevant experience and team composition

**Required Attachments:**
- Technical Architecture Diagram (1 page)
- Team resumes (key personnel only)

**Submission Deadline:** [Date and Time]

**Submit To:** [Email/Portal]

---

**9. CONTACT INFORMATION**

**Challenge Manager:** [Name]
**Email:** [Email]
**Office Hours:** [Dates/Times for Q&A sessions]

---

### A.8 AI Productivity Disclosure Template

**AI PRODUCTIVITY DISCLOSURE**
*(Required for all software development, data engineering, and technology implementation proposals)*

**Vendor:** [Vendor Name]

**Proposal/Task Order Reference:** [Reference Number]

**Date:** [Date]

---

**1. AI TOOLS TO BE USED**

| Tool Name | Vendor/Provider | Purpose | Work Types Assisted |
|-----------|-----------------|---------|---------------------|
| [e.g., GitHub Copilot] | [GitHub/Microsoft] | [Code generation, completion] | [Development, testing] |
| [e.g., Claude] | [Anthropic] | [Documentation, code review] | [Documentation, analysis] |
| [e.g., Cursor] | [Cursor] | [AI-native IDE] | [All development work] |
| [e.g., Custom automation] | [Internal] | [Test generation] | [QA, testing] |

---

**2. PRODUCTIVITY ASSUMPTIONS**

**2.1 Overall Productivity Impact:**

We estimate AI tools will provide approximately **[X]%** overall productivity improvement on this engagement, based on:
- [Basis for estimate - e.g., internal benchmarks, industry studies, prior project data]

**2.2 Productivity by Work Type:**

| Work Type | Estimated AI Productivity Gain | Justification |
|-----------|-------------------------------|---------------|
| Routine code generation | [X]% | [Explanation] |
| Testing and QA | [X]% | [Explanation] |
| Documentation | [X]% | [Explanation] |
| Complex architecture | [X]% | [Explanation] |
| User research/design | [X]% | [Explanation] |

**2.3 Vendors Claiming No/Minimal AI Benefit:**

If claiming <10% productivity benefit, explain why:
- [ ] Work is primarily non-coding (specify: _____________)
- [ ] Security/compliance restrictions prevent AI tool use
- [ ] Highly specialized domain where AI tools are not effective
- [ ] Other (explain): _________________________________

---

**3. PRICING REFLECTION**

**3.1 How AI Productivity Is Reflected in This Proposal:**

[Provide a clear statement explaining how AI efficiency gains are passed through to the State. For example:]

- "Our proposed labor hours reflect AI-assisted productivity. Without AI tools, this work would require approximately [X] hours; with AI assistance, we estimate [Y] hours."
- "Our blended rate of $[X]/hour reflects AI-augmented delivery, compared to our standard rate of $[Y]/hour for manual-only work."
- "We have applied a [X]% efficiency factor to development tasks, reducing the total proposal by $[Amount]."

**3.2 Rate Structure:**

| Role | Standard Rate (Manual) | AI-Assisted Rate | Difference |
|------|----------------------|------------------|------------|
| [Senior Developer] | $[X]/hr | $[Y]/hr | [Z]% reduction |
| [Developer] | $[X]/hr | $[Y]/hr | [Z]% reduction |
| [QA Engineer] | $[X]/hr | $[Y]/hr | [Z]% reduction |

---

**4. QUALITY AND SECURITY SAFEGUARDS**

**4.1 Code Review Process:**

- [ ] All AI-generated code undergoes human review before commit
- [ ] Code review checklist specifically addresses AI-generated code patterns
- [ ] Senior developer sign-off required for AI-assisted modules

Describe your review process: [Brief description]

**4.2 Security Scanning:**

- [ ] Static Application Security Testing (SAST) on all code
- [ ] Dependency vulnerability scanning
- [ ] AI-specific security checks for prompt injection, data leakage

Security tools used: [List tools]

**4.3 Technical Debt Management:**

- [ ] Code quality metrics tracked (complexity, maintainability index)
- [ ] Regular refactoring scheduled to address AI-generated debt
- [ ] Documentation standards enforced for AI-assisted code

Describe your approach: [Brief description]

**4.4 Accountability Statement:**

**We confirm that [Vendor Name] retains full responsibility for all deliverables regardless of AI assistance. AI tools are productivity aids; they do not transfer liability or reduce our accountability for code quality, security, performance, or compliance.**

---

**5. CERTIFICATION**

I certify that the information provided in this AI Productivity Disclosure is accurate and complete to the best of my knowledge. I understand that materially false statements may result in proposal rejection or contract termination.

**Authorized Representative:**

Signature: ___________________________

Name: [Name]

Title: [Title]

Date: ___________________________

---

### A.9 Rapid RFI² Operational Guide

This appendix provides detailed operational guidance for executing Rapid RFI² challenges. For the strategic overview, see [Section 6.4: Rapid RFI²](procurement-guide.md#64-rapid-rfi-challenge-based-procurement).

---

**Phase 1: Problem Statement (Weeks 1-3)**

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

**Phase 2: Concept Papers (Weeks 4-5)**

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

**Phase 3: Paid Prototype Sprint (Weeks 6-10)**

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

**Phase 4: Evaluation & Award (Week 11)**

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

---

### A.10 Fellowship Program Curriculum

This appendix provides detailed curriculum for the Governor's Innovation Fellowship Program. For the program overview, see [Section 7.1: Governor's Innovation Fellowship Program](strategy-document.md#71-governors-innovation-fellowship-program).

---

**1. Foundational Bootcamp (Weeks 1-2)**

**Executive Presence and Storytelling:**
- Communicating complex ideas simply
- Presenting to executives and elected officials
- Writing concise memos and briefings (1-page format)
- Building credibility and influence without formal authority
- Practice sessions with feedback from experienced leaders

**Innovation Process Foundations:**
- Design thinking and human-centered design principles
- Systems thinking and complexity navigation
- Lean startup methodology adapted for government
- Agile methodologies and iterative development
- Evidence-based decision making

**Problem-Solving Workshops:**
- Structured problem definition techniques
- Root cause analysis (5 Whys, fishbone diagrams)
- Rapid prototyping and iterative development
- Data-driven decision making frameworks
- Hands-on exercises with real government challenges

**Governance and Policy Landscape:**
- California government structure (executive, legislative, judicial)
- State budget process and fiscal calendar
- Legislative process and effective advocacy
- Administrative law and rulemaking procedures
- Interagency coordination mechanisms and challenges

**Statewide Leadership Introductions:**
- Sessions with agency secretaries and undersecretaries
- Department director panels by domain (health, transportation, public safety)
- Understanding strategic priorities and modernization challenges
- Building relationships for future collaboration

**Cohort Covenant:**
- Establishing shared expectations and mutual accountability
- Peer support and collaboration norms
- Commitment to learning, growth, and candid feedback
- Confidentiality agreements for sensitive discussions

---

**2. Leadership Breadth Program (Months 1-3)**

**Listening Sessions:**
- 8-10 sessions with executives across diverse departments
- Department mix includes:
  - Large operations: CDCR, DMV, DHCS, EDD
  - Policy-focused: ARB, DWR, CDPH
  - Infrastructure: Caltrans, DGS, CDT
  - Regulatory: DCA, DFPI, DIR
- Focus areas: challenges, priorities, modernization barriers, what's working
- Documented insights shared with cohort

**Direct Engagement:**
- Small group discussions with agency leadership (5-8 fellows per session)
- Executive shadowing (minimum 2 half-days per fellow)
- Attendance at leadership meetings and decision-making forums
- Understanding competing priorities, political constraints, stakeholder dynamics
- Reflection sessions to process and synthesize learnings

---

**3. Innovation Process Training (Months 1-4)**

**Human-Centered Problem Definition:**
- User research methods: interviews, surveys, contextual observation
- Journey mapping and pain point identification
- Persona development for different user types
- Problem framing workshops with real department challenges
- Synthesizing research into actionable insights

**Rapid Ideation and Concept Validation:**
- Brainstorming and ideation techniques (How Might We, Crazy 8s)
- Concept sketching and storyboarding
- Rapid prototyping methods:
  - Paper prototypes for workflows
  - Digital mockups for interfaces
  - Service blueprints for process redesign
- User testing and feedback incorporation
- Pivot vs. persevere decision frameworks

**Prototype Testing:**
- Testing with government staff (internal users)
- Testing with citizens (external users)
- Usability testing methodologies
- Accessibility testing (WCAG compliance)
- Interpreting feedback and iterating designs
- Documenting learnings for handoff

**Government-Specific Change Management:**
- Understanding bureaucratic culture and sources of resistance
- Building coalitions across organizational boundaries
- Securing executive sponsorship and maintaining engagement
- Navigating procurement and policy constraints creatively
- Communicating change effectively to diverse audiences
- Managing stakeholder expectations

**Implementation Roadmaps:**
- Phased rollout planning (pilot → scale → sustain)
- Risk identification and mitigation strategies
- Resource requirements and realistic budgeting
- Success metrics and evaluation plans
- Sustainability planning beyond Fellowship

---

**4. Department Embedding (Full 6 Months)**

**Full-Time Placement:**
- Placed in department outside home agency for enterprise perspective
- Full-time immersion in department operations
- Integration into departmental discovery and planning meetings
- Physical presence in department (hybrid arrangements as needed)

**Project Ownership:**
- Assigned real business priority (not "make work" project)
- Significant impact potential with measurable outcomes
- Autonomy and decision-making authority within scope
- Budget and resources as needed for project success
- Direct access to department director for escalation

**Relationship Building:**
- Daily interaction with department staff at all levels
- Understanding organizational culture from inside
- Building trust and credibility through delivery
- Creating lasting relationships across agency boundaries
- Developing political awareness and navigation skills

**Mentorship Structure:**
- **Departmental Supervisor:** Day-to-day guidance, project oversight, operational support, performance feedback
- **Home Agency Mentor:** Bi-weekly meetings, career guidance, enterprise perspective, advocacy
- **Cohort Peer:** Weekly peer mentoring, mutual support, shared learning, accountability

**Surrogate/Delegate Requirement:**
- Host department designates surrogate for business continuity
- Surrogate works alongside Fellow, learning approach and methods
- Knowledge transfer ensures project sustainability post-Fellowship
- Creates multiplier effect: Fellow + Surrogate = 2 trained change agents
- Surrogate may become candidate for future cohorts

---

**5. Group Initiatives (Full 6 Months)**

**Team Structure:**
- **4 concurrent initiatives** addressing high-priority cross-agency challenges
- **5 fellows per team** (from 20-fellow cohort: 4 teams of 5 each)
- **Executive sponsor** from Cabinet or GovOps:
  - Provides strategic direction
  - Removes barriers
  - Champions findings
- **TMO liaison:**
  - Provides methodology support
  - Coordinates across initiatives
  - Connects to enterprise resources

**Initiative Domain Examples:**
- Business licensing modernization (cross-agency service integration)
- Data governance and sharing infrastructure (technical and policy framework)
- Customer experience platform (unified citizen portal)
- Procurement modernization (streamlined processes, vendor management)
- Emergency response coordination (disaster preparedness, interagency protocols)
- Workforce development (talent pipeline, skills modernization)

**Timeline and Deliverables:**

**Month 1-2: Research and Discovery**
- Stakeholder interviews (agencies, staff, citizens, advocates)
- Current state analysis and process mapping
- Best practice research (other states, federal, international)
- Problem definition and scoping
- Deliverable: Research synthesis and problem statement

**Month 3-4: Concept Development**
- Ideation and solution design sessions
- Rapid prototyping and user testing
- Feasibility assessment (technical, financial, political, legal)
- Refinement based on stakeholder feedback
- Deliverable: Concept brief with prototype

**Month 5: Roadmap Development**
- Implementation plan with phases and milestones
- Resource requirements and budget estimates
- Risk assessment and mitigation strategies
- Success metrics and evaluation plan
- Governance and accountability structure
- Deliverable: Draft implementation roadmap

**Month 6: Presentation and Handoff**
- Executive recommendation document (20-30 pages)
- Implementation roadmap (detailed project plan)
- Identified implementation team (who will carry work forward)
- Presentation to Cabinet and Governor's Office
- Formal handoff to implementing entity
- Deliverable: Final report and Cabinet presentation

---

### A.11 Breakthrough Fund Sustainability Model

This appendix provides a detailed worked example of how the Breakthrough Fund sustainability model operates. For the strategic overview, see [Section 8.3: Feedback Loop and Sustainability Model](strategy-document.md#83-feedback-loop-and-sustainability-model).

---

**Worked Example: Business Licensing Automation**

**Step 1: Project Delivers Measurable Savings**

A Breakthrough Fund investment of $3M modernizes business licensing across three agencies:
- Processing time reduced from 45 days to 3 days
- Staffing reduced from 20 FTE to 8 FTE through automation
- Staff reassigned to higher-value work (compliance, outreach)

**Savings Calculation:**
- 12 FTE positions no longer needed for processing
- Average loaded cost per FTE: $100,000/year
- **Annual cost reduction: $1.2M**

---

**Step 2: Department Budget Adjusted**

Following validation of sustained savings (typically 1 fiscal year of demonstrated performance):
- Department baseline budget reduced by $1.2M
- Reduction implemented in subsequent fiscal year
- Staff reassignment or attrition managed through normal HR processes

---

**Step 3: Fixed 25% Diverted to Breakthrough Fund**

Per policy, 25% of realized savings flow back to the Breakthrough Fund:
- 25% of $1.2M = **$300K diverted to Breakthrough Fund annually**
- 75% of $1.2M = **$900K returns to General Fund**

This continues for the life of the project (typically 5-7 years before system refresh required).

---

**Step 4: Reinvestment Creates Next Generation Projects**

The $300K annual contribution funds new modernization:
- Year 1: $300K available
- Year 2: $600K cumulative (if no new projects funded)
- Years 3-5: As more projects mature, contributions compound

**Portfolio Effect:**

| Year | Active Projects | Annual Savings Generated | 25% to Fund | Cumulative Fund Growth |
|------|-----------------|-------------------------|-------------|------------------------|
| 1 | 5 pilots | $2M | $500K | $500K |
| 2 | 10 projects | $6M | $1.5M | $2M |
| 3 | 18 projects | $12M | $3M | $5M |
| 4 | 25 projects | $20M | $5M | $10M |
| 5 | 30 projects | $30M | $7.5M | $17.5M |

---

**Self-Sustainability Threshold**

The fund becomes self-sustaining when annual reinvestment inflows equal or exceed annual investment needs:

- **Target annual investment capacity:** $15-20M (10-15 new projects per year)
- **Required annual savings generation:** $60-80M (to produce $15-20M at 25%)
- **Estimated time to self-sustainability:** 5-7 years from initial $100M capitalization

At self-sustainability:
- Private sector partners can exit or continue
- General Fund contribution no longer required
- Fund operates as permanent modernization engine

---

**Risk Factors and Mitigation**

| Risk | Mitigation |
|------|------------|
| Projects don't deliver savings | Stage-gate process kills underperformers early |
| Savings not captured in budget | TMO tracks savings; automatic budget adjustment policy |
| Departments resist budget reduction | Savings reinvested in department priorities; not purely extractive |
| Political pressure to redirect funds | Statutory protection for 25% diversion; transparent reporting |

---

## Version History

| Version | Date | Description |
|---------|------|-------------|
| Executive Draft v1.0 | December 2025 | Initial executive draft with templates A.1-A.11 |

---

**Document Version:** Executive Draft v1.0
**Date:** December 2025
**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency

---

*End of California Enterprise Modernization Plan - Operational Appendices*
