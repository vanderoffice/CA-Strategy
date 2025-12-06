---
marp: true
theme: default
paginate: true
footer: "California State Government Modernization Strategy (Rev1G3)"
---

<!-- _class: lead -->

# California State Government Modernization Strategy

## Rev1G3: The "Product-Led" Government

**Prepared for:** Office of Data and Innovation & Governor's Office of Operations
**Version:** Rev1G3 (Product-Led Pivot)

---

# Executive Summary

## From "Project-Centric" to "Product-Led"

- **The Shift:** Moving from massive, temporary IT projects to continuous, user-centric product delivery.
- **The Core Problem:** Misaligned incentives lead to "Megaprojects" that fail and "Use It or Lose It" budgets that prevent agility.
- **The Solution:**
  - **Governance:** E3 Leadership + Life Experience Teams
  - **Delivery:** Modular Contracting (<$10M) + Persistent Teams
  - **Finance:** Technology Working Capital Fund (Revolving)

<!-- note:
- We are pivoting from "Managing IT" to "Delivering Value".
- The E3 leadership structure remains the backbone, but the delivery mechanism changes.
- Key concept: Government as a Platform (GaaP).
-->

---

# The Efficiency Challenge

## The "Megaproject" and "Budget" Traps

- **The Megaproject Trap:** Large contracts (> $50M) take years to procure and are obsolete by launch.
- **The Budget Trap:** Annual appropriations force "rush spending" and prevent long-term product health.
- **The Silo Trap:** Citizens navigate org charts (DMV -> Tax -> Health) instead of life events.
- **Conclusion:** We need structural reform, not just better project management.

<!-- note:
- Private sector has profit motive; we need a different forcing mechanism.
- "Waterfall" procurement is the enemy of modernization.
- Citizens don't care about our org chart.
-->

---

# Governance Architecture

## E3 Leadership + Life Experience Teams

- **Retained:** Undersecretaries (Agency) and Chief Deputies (Dept) provide the "Business Command Chain."
- **New Overlay:** **Life Experience Teams (LETs)**
  - Cross-functional teams organized around journeys (e.g., "Having a Baby," "Disaster Recovery").
  - Authority to direct API standards across agencies.
- **Bureaucracy Control:**
  - **Sunset Clauses:** All E3 roles expire in 3 years if capability not embedded.
  - **Rule of Subtraction:** Create 1 new body, disband 2 existing ones.

<!-- note:
- We keep the E3 structure because we need business-side ownership.
- But we add LETs to break the silos.
- We aggressively manage bureaucratic bloat with sunset clauses.
-->

---

# Technology Architecture

## Service Mesh & API-First

- **Old Model:** Centralized Enterprise Service Bus (ESB) = Bottleneck.
- **New Model:** **Service Mesh** (Smart Endpoints, Dumb Pipes).
- **API-First Mandate:** "If it doesn't have an API, it doesn't exist."
- **Event-Driven:** Systems communicate via asynchronous events (e.g., "ChildBorn") rather than brittle integrations.
- **Identity:** "One Login, One Profile" (Federated Identity).

<!-- note:
- Moving away from the monolith.
- Decentralized but standardized.
- API-first allows the "Life Experience Teams" to compose new services rapidly.
-->

---

# Data Strategy

## Federated Data Mesh

- **Shift:** From centralized "Master Data Management" (too slow) to **Federated Data Mesh**.
- **Principles:**
  - **Domain Ownership:** DMV owns vehicle data; Tax Board owns income data.
  - **Data Products:** Agencies publish clean, documented data via APIs.
  - **The "Ask Once" Promise:** Agencies consume each other's data products instead of asking citizens twice.

<!-- note:
- Building a central database takes 10 years and fails.
- Connecting existing databases via standard APIs takes months.
- Data is a product, not a byproduct.
-->

---

# Procurement Modernization

## Two-Track Model

- **Track A: The Moonshot (RFI²)**
  - For high-uncertainty, complex problems (e.g., GenAI).
  - Problem-based procurement.
- **Track B: The Modular Standard (New Default)**
  - **The Modular Mandate:** No contract > **$10M** or **3 Years**.
  - **Small Business Fast Track:** Simplified purchasing for micro-services (<$250k).

<!-- note:
- We are banning "Megaprojects" without a legislative waiver.
- If a $5M module fails, we scrap it. If a $500M system fails, it's a disaster.
- Fast track brings in startups and innovation.
-->

---

# Workforce & Finance

## Persistent Teams & Revolving Funds

- **Workforce:**
  - **Persistent Product Teams:** Funded to own a product long-term, not just build and leave.
  - **Digital Corps:** Pipeline for early-career tech talent.
  - **Governor's Innovation Fellowship:** Senior private sector talent.
- **Finance:**
  - **Technology Working Capital Fund:** A revolving fund. Agencies borrow for ROI-positive modernization and repay from savings.
  - **Benefit:** Breaks the annual "Use It or Lose It" cycle.

<!-- note:
- You can't build modern software with temporary project teams.
- The Revolving Fund is the economic engine of this strategy.
-->

---

# Performance Measurement

## Measuring Value, Not Just Activity

- **Time to Value (TTV):** Time from policy decision to first working software (< 3 months).
- **Deployment Frequency:** How often do we ship? (Target: Bi-weekly).
- **Life Event Success Rate:** % of users completing cross-agency journeys without help.
- **Modular Health:** % of contracts under $10M cap.

<!-- note:
- Moving beyond "Uptime" and "On Budget".
- Speed and User Outcome are the new north stars.
-->

---

# Implementation Roadmap

## Phased Execution

- **Phase 1: Unblocking (Months 1-6)**
  - Appoint E3 Leaders.
  - Issue **Modular Mandate** ($10M Cap).
  - Establish **Working Capital Fund**.
- **Phase 2: The Mesh (Months 7-18)**
  - Deploy Service Mesh & One Login.
  - Launch first **Life Experience Teams**.
- **Phase 3: Scale (Months 19-36)**
  - Accelerate "Strangler Fig" legacy migration.
  - First "Sunset Review" of E3 roles.

<!-- note:
- Immediate policy changes (Modular Mandate) drive the behavior shift.
- Technical foundation (Mesh) follows.
-->

---

# Call to Action

## Next 90 Days

1.  **Authorize E3 Structure:** Appoint first cohort.
2.  **Seed the Fund:** Appropriate $250M seed capital for the Revolving Fund.
3.  **Issue Executive Order:**
    - Mandate API-First.
    - Cap IT contracts at $10M.
4.  **Launch Pilots:** Form "Disaster Recovery" and "New Parent" Life Experience Teams.

<!-- note:
- We need money (Fund), Power (E3), and Rules (Modular Mandate).
- Action, not just planning.
-->

---

<!-- _class: lead -->

# Appendix

## Rev1G3 Supporting Concepts

- **Service Mesh Architecture**
- **Data Mesh Principles**
- **Modular Contracting Guidelines**
- **Revolving Fund Mechanics**
