# KPI Dashboard Framework

**Purpose:** Standard structure for performance measurement across the modernization initiative, ensuring consistent metrics and reporting.

---

### **2.1 Dashboard Structure**

**Four-Tier Hierarchy:**

**Tier 1: Statewide Strategic KPIs**

- **Audience:** Governor, Legislature, Public
- **Update Frequency:** Quarterly
- **Visualization:** High-level trends and progress toward targets

**Tier 2: Operational KPIs**

- **Audience:** IT and Program Managers
- **Update Frequency:** Monthly
- **Visualization:** Detailed performance metrics by system/service

**Tier 3: Transformation Progress KPIs**

- **Audience:** E3 Leaders, TMO
- **Update Frequency:** Monthly
- **Visualization:** Program health indicators

**Tier 4: Organizational Change KPIs**

- **Audience:** HR, Change Management, E3 Leaders
- **Update Frequency:** Quarterly
- **Visualization:** Cultural indicators and adoption metrics

---

### **2.2 KPI Template**

**For Each Metric:**

**Metric Name:** [Short, descriptive title]

**Definition:** [Precise definition of what is being measured]

**Rationale:** [Why this metric matters and what it tells us]

**Calculation Method:**

- **Formula:** [Mathematical formula or data source]
- **Example:** Digital Service Adoption = (# Transactions Available Digitally / Total # Transactions) × 100%

**Data Sources:**

- **Primary:** [Where data comes from]
- **Frequency:** [How often data is collected]
- **Owner:** [Who is responsible for data accuracy]

**Targets:**

- **Baseline:** [Current or starting value]
- **Year 1 Target:** [Realistic improvement]
- **Year 3 Target:** [Stretch goal]
- **Year 5 Target:** [Aspirational but achievable]

**Measurement Frequency:**

- **Data Collection:** [How often measured]
- **Reporting:** [How often published to dashboards]

**Visualization Guidance:**

- **Chart Type:** [Line graph, bar chart, gauge, etc.]
- **Color Coding:**
  - Green: Meeting or exceeding target
  - Yellow: Within 10% of target (at risk)
  - Red: More than 10% below target (intervention needed)

**Accountability:**

- **Owner:** [Position responsible for achieving target]
- **Escalation:** [Who to notify if metric is Red for 2+ consecutive periods]

**Example KPI - Digital Service Adoption Rate:**

**Metric Name:** Digital Service Adoption Rate

**Definition:** Percentage of citizen-facing government transactions that can be completed entirely online without in-person visit or phone call

**Rationale:** Measures progress toward digital-first government. Higher adoption reduces cost, increases citizen convenience, and enables 24/7 service access.

**Calculation Method:**

- **Formula:** (# Services Fully Digital / Total # Citizen-Facing Services) × 100%
- **Service Inventory:** Maintained by TMO, validated by agencies quarterly
- **Fully Digital Definition:** Citizen can complete entire transaction online from any device without human assistance

**Data Sources:**

- **Primary:** Service inventory database (TMO maintained)
- **Validation:** Agency quarterly certification of service status
- **Frequency:** Quarterly census of all services

**Targets:**

- **Baseline (Year 0):** 38% (estimated; confirm with actual inventory)
- **Year 1 Target:** 45%
- **Year 2 Target:** 55%
- **Year 3 Target:** 65%
- **Year 5 Target:** 75%

**Measurement Frequency:**

- **Data Collection:** Quarterly service inventory update
- **Reporting:** Published to public dashboard within 2 weeks of quarter end

**Visualization Guidance:**

- **Chart Type:** Line graph showing quarterly progress with target line
- **Drill-Down:** Bar chart by agency showing each agency's adoption rate
- **Color Coding:**
  - Green: ≥ quarterly target
  - Yellow: Within 5 percentage points of target
  - Red: >5 percentage points below target

**Accountability:**

- **Owner:** Each Agency Undersecretary for E3 (for their agency)
- **Statewide Aggregation:** TMO Director
- **Escalation:** If statewide rate is Red for 2 consecutive quarters, escalate to Executive Technology Council

---

### **2.3 Dashboard Visualization Standards**

**Public-Facing Dashboard (Citizen Audience):**

**Design Principles:**

- Simple, clean visual design (no clutter)
- Accessible (WCAG 2.1 AA compliant, screen reader friendly)
- Mobile-responsive (50%+ of traffic will be mobile)
- Plain language (no jargon or acronyms without explanation)
- Fast loading (<3 seconds on average connection)

**Required Components:**

1. **Overview Section:** Headline metrics (digital adoption %, CSAT score, cost savings)
2. **Progress Tracker:** Visual showing completion toward strategic goals
3. **Recent Wins:** Highlight 3-5 recent improvements citizens will notice
4. **Agency Scorecards:** Drill-down into each agency's performance
5. **About/Methodology:** Explain what's being measured and why

**Update Schedule:** Weekly data refresh (automated from source systems)

**Internal Dashboard (E3 Leaders/TMO):**

**Additional Components:**

- Budget and financial tracking (spending vs. plan)
- Resource allocation (staff, contractors)
- Risk register with status
- Dependency tracking between projects
- Detailed technical metrics (API performance, system uptime, security incidents)
- Project portfolio health (on track, at risk, delayed by count and $)

**Update Schedule:** Daily or real-time where possible

**Technology Platform:**

- **Options:** Tableau, PowerBI, Domo, or open-source (Grafana, Apache Superset)
- **Requirements:** Cloud-hosted, API integration with data sources, role-based access control, export capabilities

---

### **2.4 Reporting Cadence**

**Weekly:**

- **Automated Alerts:** Email to E3 leaders flagging metrics in Red status
- **TMO Internal Review:** Review all metrics, identify trends, prepare for weekly leadership briefing

**Monthly:**

- **E3 Council Dashboard Review:** Standing agenda item at monthly E3 Council meetings
- **Detailed Reports:** By agency and by major initiative, circulated to stakeholders

**Quarterly:**

- **Public Dashboard Update:** Published to Envision 2026 portal or modernization website
- **Executive Report:** Narrative report to Governor, Agency Secretaries, Legislature (see template below)
- **Statewide Town Hall:** TMO Director presents results in public webinar, Q&A

**Annually:**

- **Comprehensive Performance Report:** Detailed analysis of full year, trends, successes, challenges
- **Benchmarking:** Compare California performance to other states and best practices
- **Strategic Review:** Assess whether KPIs still align with goals; recommend changes

---

### **2.5 Quarterly Executive Report Template**

**California State Government Modernization**  
**Quarterly Performance Report - Q[X] [Year]**

**Prepared by:** Transformation Management Office  
**Date:** [Date]  
**Distribution:** Governor, Agency Secretaries, Legislative Leadership

---

**Executive Summary (1 Page)**

**Headline Results:**

- [3-5 key accomplishments this quarter]
- [Major metrics: digital adoption %, CSAT, legacy reduction %, cost savings]

**Challenges:**

- [1-3 significant obstacles encountered]
- [Mitigation actions taken]

**Decisions Needed:**

- [List any decisions requiring executive intervention]

**Next Quarter Priorities:**

- [3-5 key focus areas]

---

**Progress Against Strategic KPIs (2-3 Pages)**

**For Each Tier 1 KPI:**

- Current value vs. target
- Trend (improving, stable, declining)
- Analysis: What's driving performance?
- Actions taken this quarter
- Outlook for next quarter

[Include charts showing trends over time]

---

**Financial Summary (1 Page)**

**Budget Performance:**

- Approved budget: $[X]M
- Spent to date: $[Y]M ([Z]% of budget)
- Projected year-end spending: $[A]M
- Variance explanation

**Return on Investment:**

- Cost savings achieved to date: $[B]M
- Cost avoidance: $[C]M
- Projected 5-year ROI: [X]%

---

**Project Portfolio Health (1-2 Pages)**

**Portfolio Overview:**

- Total active projects: [N]
- Total investment: $[X]M
- Status breakdown:
  - On Track: [N] projects ($[X]M)
  - At Risk: [N] projects ($[Y]M)
  - Delayed: [N] projects ($[Z]M)

**Completions This Quarter:**

- [List 3-5 major projects completed]
- [Impact of each]

**Projects At Risk:**

- [List projects in Red status]
- [Brief description of issues and mitigation plans]

---

**Risk Assessment (1 Page)**

**Top 5 Risks:**

For each:

- **Risk Description:** [What could go wrong]
- **Impact:** [High/Medium/Low]
- **Probability:** [High/Medium/Low]
- **Mitigation:** [What we're doing about it]
- **Owner:** [Who is responsible]

---

**Success Stories (1 Page)**

**Highlight 2-3 transformations that demonstrate tangible citizen or operational impact:**

**Example:**
**Title:** DMV Appointment Scheduling Goes Digital

**Challenge:** 2 million+ citizens wait in line annually for DMV appointments; average wait time 90 minutes

**Solution:** Deployed online appointment scheduling system; integrated with driver's license renewal and Real ID processing

**Results:**

- 65% of appointments now scheduled online
- Average wait time reduced to 22 minutes
- Citizen satisfaction increased from 58% to 82%
- Cost per appointment reduced from $18 to $7

**Quote:** "I was able to schedule my Real ID appointment on my phone during lunch and was in and out in 15 minutes. Huge improvement!" - Maria S., Los Angeles

---

**Upcoming Quarter Milestones (1 Page)**

**Major Deliverables:**

- [List 5-10 significant milestones expected next quarter]
- [Include go-lives, pilot completions, major procurements]

**Governance Activities:**

- Executive Technology Council meetings and decisions
- E3 Council priorities
- Innovation Fellowship cohort rotations

**Risks to Watch:**

- [3-5 potential challenges on the horizon]

---

**Appendices**

- Detailed KPI tables (all metrics)
- Project portfolio complete list
- Acronym glossary
