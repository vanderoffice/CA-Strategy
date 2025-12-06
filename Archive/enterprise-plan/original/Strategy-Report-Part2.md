# California State Government Modernization Strategy
## Comprehensive Strategy Report - Part 2: Procurement, Workforce, Performance & Change Management

---

## Section 4: Data Strategy & Governance

### 4.1 Statewide Data Governance Framework

**Three-Tier Council Structure:**

**Tier 1: Statewide Data Governance Council**
- **Chair:** Statewide Chief Data Officer (ODI)
- **Members:** Agency Data Officers from all agencies (8-12 members), representatives from CDT, Department of Finance, Legislative Analyst's Office
- **Meeting Cadence:** Monthly
- **Responsibilities:**
  - Set statewide data policies, standards, and strategic priorities
  - Approve cross-agency data sharing frameworks and master data definitions
  - Resolve inter-agency data conflicts and prioritization disputes
  - Review and approve high-impact data initiatives
  - Report quarterly to Executive Technology Council

**Tier 2: Agency Data Governance Teams**
- **Chair:** Agency Data Officer (reports to Undersecretary for E3)
- **Members:** Department Data Stewards, key technical leads, legal/privacy officers
- **Meeting Cadence:** Bi-weekly
- **Responsibilities:**
  - Implement statewide policies within agency context
  - Coordinate cross-department data sharing within agency
  - Develop agency-specific data standards and definitions
  - Manage agency data catalog and metadata
  - Escalate issues to Statewide Council

**Tier 3: Department Data Operations**
- **Lead:** Department Data Steward (reports to Chief Deputy Director for E3)
- **Members:** Database administrators, analysts, application owners
- **Meeting Cadence:** Weekly operational meetings
- **Responsibilities:**
  - Execute data governance policies operationally
  - Ensure data quality through validation and cleansing
  - Maintain department data assets and documentation
  - Respond to data sharing requests
  - Report compliance and quality metrics

### 4.2 Data Sharing Agreement Templates

**Challenge:** California agencies currently require 18 months on average to negotiate data sharing agreements due to legal, privacy, security, and technical concerns being addressed case-by-case.

**Solution:** Pre-approved standardized templates reduce negotiation to 30 days.

**Template Types:**

**Type 1: Intra-Agency Data Sharing**
- **Use Case:** Departments within same agency sharing data
- **Legal Review:** Pre-approved by Agency legal counsel
- **Privacy Assessment:** Simplified (same agency privacy policies apply)
- **Security:** Standard intra-agency controls
- **Approval Process:** Agency Data Officer approval, 7-day turnaround

**Type 2: Inter-Agency Data Sharing (Low Sensitivity)**
- **Use Case:** Public or low-sensitivity data (demographics, geographic, aggregate statistics)
- **Legal Review:** Pre-approved template, minimal customization needed
- **Privacy Assessment:** Not required (no PII)
- **Security:** Standard API security (OAuth 2.0, TLS)
- **Approval Process:** Both Agency Data Officers, 14-day turnaround

**Type 3: Inter-Agency Data Sharing (Moderate Sensitivity)**
- **Use Case:** PII for program eligibility, service coordination (common scenario)
- **Legal Review:** Pre-approved template with customizable purpose/scope sections
- **Privacy Assessment:** Streamlined Privacy Impact Assessment (PIA) template
- **Security:** Enhanced controls (data encryption, audit logging, access restrictions)
- **Approval Process:** Agency Data Officers + Statewide CDO review, 30-day turnaround

**Type 4: Inter-Agency Data Sharing (High Sensitivity)**
- **Use Case:** Health records, criminal justice data, child welfare, highly confidential information
- **Legal Review:** Detailed legal analysis required, template provides framework
- **Privacy Assessment:** Full PIA required, ethics review for AI/ML use
- **Security:** Maximum controls (data minimization, purpose limitation, strict access controls)
- **Approval Process:** Full governance review, 60-90 day turnaround (still 75% faster than current average)

**Template Components:**

All templates include standard sections:
- **Purpose and Scope:** What data, for what use case, legal authority
- **Data Elements:** Specific fields/tables, refresh frequency, historical depth
- **Security and Privacy:** Technical controls, audit requirements, breach notification
- **Roles and Responsibilities:** Data provider, consumer, steward obligations
- **Term and Termination:** Duration, renewal process, termination rights
- **Dispute Resolution:** Escalation path, amendment process

**Implementation Support:**
- Online portal for agreement initiation and tracking
- Automated routing to appropriate reviewers
- Template selection wizard based on use case
- Status dashboard showing all agreements and approval stages
- Repository of executed agreements (searchable by agency, data type, purpose)

### 4.3 Master Data Management (MDM)

**Entities Requiring Master Data:**

**Citizen/Individual:**
- Unique identifier (not SSN due to security concerns; state-issued ID)
- Core demographic attributes (name, date of birth, address)
- Program participation (which agencies/services)
- Consent and privacy preferences
- **Challenge:** Same person represented differently across 400+ systems
- **Solution:** MDM system providing golden record with cross-references to legacy IDs

**Business/Organization:**
- Unique identifier (Federal EIN or state business ID)
- Legal name, DBA names, organizational structure
- Licensing, permits, registrations across agencies
- Compliance status, tax standing
- **Challenge:** Businesses interact with multiple agencies (tax, labor, environmental, licensing)
- **Solution:** Unified business profile reducing redundant data collection

**Geographic:**
- Standardized address format (USPS compliant)
- Geospatial coordinates (latitude/longitude)
- Administrative boundaries (county, city, district, ZIP)
- Parcel identifiers, building permits
- **Challenge:** Address variations and errors prevent data integration
- **Solution:** Address validation and geocoding service

**MDM Implementation Approach:**

**Phase 1: Design (Year 1)**
- Select MDM platform (commercial: Informatica, IBM; or open-source: Talend)
- Define data models for each entity type
- Establish data quality rules and matching algorithms
- Pilot with one entity type (recommend starting with businesses—lower privacy sensitivity than citizens)

**Phase 2: Deploy (Years 2-3)**
- Implement MDM platform in cloud environment
- Load data from 10-20 key source systems
- Train data stewards on MDM processes
- Provide APIs for accessing golden records
- Begin retiring duplicate datasets

**Phase 3: Scale (Years 3-5)**
- Integrate all major systems with MDM
- Mandate MDM use for all new systems
- Achieve 95%+ match rates on core entities
- Measure data quality improvements

**Data Quality Metrics:**

**Completeness:** Percentage of required fields populated
- **Target:** 95% for critical fields, 80% for optional fields

**Accuracy:** Percentage of values verified correct through validation
- **Target:** 98% for MDM golden records

**Timeliness:** Lag between source system update and MDM reflection
- **Target:** < 24 hours for batch systems, < 5 minutes for real-time

**Consistency:** Agreement between MDM and source systems
- **Target:** 99% consistency for synchronized fields

### 4.4 Privacy and Ethics Framework

**CCPA Compliance:**

**Core Requirements:**
- Right to know what personal information is collected
- Right to delete personal information
- Right to opt-out of sale (not applicable to government, but disclosure still required)
- Right to non-discrimination for exercising privacy rights

**Implementation:**

**Automated Consent Management:**
- Citizen portal for viewing what data government holds
- Self-service options to correct inaccuracies
- Consent preferences for data sharing (beyond legally mandated uses)
- Deletion requests workflow (with exceptions for legal retention requirements)

**Privacy Impact Assessments (PIAs):**
- **Required For:** All new systems collecting PII, any AI/ML using personal data, changes to data sharing practices
- **Process:** Standardized PIA template, review by privacy officer and legal counsel, publication of results (with security-sensitive details redacted)
- **Approval:** Required before system deployment or data practice change

**Data Minimization:**
- **Principle:** Collect only data necessary for specific purpose
- **Implementation:** Data collection justification required in procurement, architecture reviews verify compliance, periodic audits identify unnecessary data collection

**Ethics Framework for AI/ML:**

**Algorithmic Accountability:**
- Document all AI/ML models used in decision-making (eligibility determinations, risk assessments, resource allocation)
- Explainability requirements: Models must provide human-understandable reasoning
- Bias testing: Evaluate model performance across demographic groups, correct disparate impact
- Human review: High-stakes decisions (parole, benefit denial) require human oversight, not solely algorithmic

**Example:** CDCR risk assessment tools predicting recidivism must:
- Disclose factors influencing score
- Be tested for racial/socioeconomic bias
- Allow individuals to challenge scores
- Require human judgment in release decisions

---

## Section 5: Procurement Modernization

### 5.1 The RFI² (Request for Innovative Ideas) Process - Detailed Methodology

California pioneered RFI² through Governor Newsom's Executive Order N-04-19 in January 2019, creating an innovative procurement method that asks vendors to design solutions to complex problems rather than bidding on predefined solutions.

**Legal Authority:**
- Public Contract Code Section 6611 (Information Technology Goods and Services)
- Executive Order N-04-19 (expedited procurement for emergency response, later expanded)
- Two-phase approach authorized under existing contracting law

**When to Use RFI²:**

**Ideal Scenarios:**
- **Complex technical challenges without obvious solutions:** Example—Using AI to predict infrastructure failures
- **Emerging technology applications:** Example—Blockchain for credential verification
- **Cross-cutting problems affecting multiple agencies:** Example—Unified citizen identity management
- **Market innovation needed:** Example—Novel approaches to fraud detection
- **High uncertainty requiring experimentation:** Example—Quantum computing for cryptography

**Not Appropriate For:**
- Commodity purchases (laptops, standard software licenses)
- Well-defined requirements with known solutions
- Urgent procurements requiring immediate action
- Low-dollar, low-complexity purchases

**Budget Allocation Recommendation:**
Reserve 15-25% of technology modernization budget for RFI² projects, focusing on highest-impact, highest-uncertainty challenges.

**Phase 1: Innovation Concept Papers**

**Step 1: Problem Statement Development (Weeks 1-4)**

Internal workshops with agency subject matter experts, frontline workers, and California Breakthrough Project advisors to define the problem without prescribing solutions.

**Problem Statement Components:**
- **Background and Context:** Why is this a priority? What's the current state?
- **Desired Outcomes:** What would success look like? (Measurable)
- **Constraints:** Budget range, timeline, regulatory requirements
- **Evaluation Criteria:** How will concepts be assessed? (Typically: Innovation potential 40%, Feasibility 30%, Cost-effectiveness 20%, Vendor qualifications 10%)

**Example Problem Statement (GenAI for Bill Analysis):**
"The Department of Finance analyzes 2,500+ bills per legislative session, requiring staff to read lengthy documents, research precedents, and draft preliminary analyses under tight deadlines. This process is labor-intensive and limits depth of analysis. We seek innovative generative AI solutions that can: (1) Extract key provisions from bills, (2) Identify fiscal impacts and policy implications, (3) Generate preliminary draft analyses for staff review, (4) Learn from past analyses to improve recommendations. Solution must comply with state data privacy requirements and provide explainable outputs."

**Step 2: Innovation Conference (Week 5)**

Public event bringing together potential vendors, entrepreneurs, researchers, and government stakeholders.

**Format:**
- Morning: Problem statement presentation by agency, Q&A with government experts
- Afternoon: Breakout sessions for different solution approaches, networking
- Virtual participation option for remote attendees

**Goals:**
- Educate market about the problem and government context
- Generate excitement and participation
- Enable collaboration (vendors may form teams)
- Clarify expectations and answer questions before proposals

**Step 3: Concept Paper Solicitation (Weeks 6-15)**

RFI² solicitation published on state procurement portal, typically allowing 60-90 days for submissions.

**Concept Paper Requirements (Typically 10-15 pages):**
- **Executive Summary:** High-level solution approach
- **Technical Approach:** How will you solve the problem? What technologies, methods, processes?
- **Innovation Description:** What's novel about your approach versus existing solutions?
- **Feasibility Assessment:** Evidence this can work (prior implementations, research, prototypes)
- **Team Qualifications:** Relevant experience, key personnel, partnerships
- **Cost Estimate:** Rough order of magnitude for Proof of Concept and full implementation
- **Timeline:** How long to demonstrate and deploy?

**Evaluation Process (Weeks 16-20):**

**Evaluation Panel:**
- Agency subject matter experts (40% of panel)
- Technical experts from CDT or ODI (30% of panel)
- California Breakthrough Project advisors or external experts (20% of panel)
- Procurement and legal representatives (10% of panel)

**Scoring:**
Each evaluator scores proposals independently using standardized rubric, then panel meets to discuss and reach consensus on top candidates.

**Selection:**
Typically select 2-5 proposals (not just one) to advance to Phase 2. Multiple vendors provide competitive pressure and risk mitigation if one approach fails.

**Step 4: Concept Paper Awards (Week 21)**

Selected vendors receive modest compensation for Phase 1 participation (typically $25K-$50K per vendor to develop Proof of Concept). This is critical—compensating vendors for innovation effort encourages high-quality participation.

**Phase 2: Proof of Concept Development**

**Step 5: Proof of Concept Planning (Weeks 22-26)**

Selected vendors work with agency to refine approach and define success criteria for demonstration.

**PoC Plan Components:**
- **Scope:** What specific capabilities will be demonstrated?
- **Data:** What test data will be used? (Agency typically provides sanitized/anonymized data)
- **Environment:** Where will PoC run? (Vendor environment, state cloud, hybrid)
- **Timeline:** 90-day development period typical
- **Success Criteria:** Quantitative metrics (accuracy, speed, cost) and qualitative factors (usability, maintainability)
- **Evaluation Process:** Who will test, what scenarios, how will results be assessed?

**Step 6: PoC Development (Weeks 27-39)**

Vendors build working prototypes while agency provides support:
- Access to subject matter experts for questions
- Test data and realistic scenarios
- Feedback on interim demonstrations
- Technical infrastructure if needed

**Regular check-ins (biweekly) ensure vendors stay on track and agencies can course-correct if needed.**

**Step 7: PoC Evaluation (Weeks 40-44)**

**Demonstration:**
- Vendors present live demos to evaluation panel and stakeholders
- Real-world scenario testing with agency staff
- Performance measurement against success criteria
- Q&A about approach, costs, scalability, and risks

**Evaluation Criteria:**
- **Technical Performance (40%):** Does it work? How well versus requirements?
- **Usability (20%):** Can agency staff actually use this?
- **Cost-Effectiveness (15%):** ROI versus current process or alternative solutions
- **Scalability and Maintainability (15%):** Can this grow? Can we support it long-term?
- **Vendor Capability (10%):** Can this vendor deliver at scale?

**Step 8: Implementation Contract Award (Week 45+)**

**Award Options:**

**Single Award:** One vendor clearly superior—award full implementation contract

**Multiple Awards:** Different vendors excel at different aspects—award contracts for different components or pilot deployments in different contexts

**No Award:** None meet requirements—return to market with revised approach or abandon initiative

**Contract Structure:**
- **Base Period:** Initial implementation (6-12 months)
- **Option Years:** Ongoing operation and enhancement (3-5 years typical)
- **Performance Metrics:** Payment tied to achieving outcomes, not just effort
- **Transition Plan:** If contract ends, vendor must support transition to different solution

**RFI² Success Examples:**

**Wildfire Detection and Response (2019):**
- **Problem:** Rapid wildfire spread requires faster detection and response
- **Concept Papers Received:** 131 submissions from tech companies, universities, nonprofits
- **Selected:** 2 vendors for PoC
  - Technosylva: Cloud-based wildfire behavior prediction and simulation ($383,000 contract)
  - Another vendor: Early detection using sensors and AI
- **Outcome:** Deployed in 4 counties, contributed to faster emergency response

**Middle-Mile Broadband Initiative (2023-2024):**
- **Problem:** 10,000 miles of fiber optic cable needed to connect underserved areas
- **RFI² Use:** Solicit innovative construction approaches and community partnerships
- **Outcome:** Secured contracts for 83% of network (8,300+ miles) through collaborative vendor relationships

**GenAI for Bill Analysis (2024-2025):**
- **Problem:** Department of Finance needs to analyze thousands of bills efficiently
- **Phase 1:** Concept papers due January 2025
- **Phase 2:** PoC development April-July 2025
- **Expected Outcome:** Contract award Fall 2025 for production deployment

### 5.2 Traditional RFI/RFP/RFQ Staged Approach

For more conventional procurements, use a structured progression from market research to vendor selection.

**Stage 1: RFI (Request for Information)**

**Purpose:** Market research and vendor education before committing to specific requirements

**When to Use:**
- Exploring new technology category (e.g., "What citizen engagement platforms exist?")
- Unclear which vendors can meet needs
- Want to understand cost ranges and implementation approaches
- Refining requirements before formal RFP

**Process:**
- **Duration:** 30-45 days from publication to response deadline
- **Vendor Effort:** 10-20 hours typically (keep response burden low to maximize participation)
- **Agency Effort:** 20-30 hours (writing RFI, reviewing responses, vendor meetings)
- **Participants:** Cast wide net (10-20 vendors), including small businesses and new market entrants

**RFI Content:**
- Background on agency mission and current challenges
- High-level description of needs (not detailed requirements)
- Questions about vendor capabilities, approaches, and experience
- Request for cost estimates (rough order of magnitude)
- Clarification that RFI is non-binding, no contract awards from RFI alone

**RFI Evaluation:**
- Not scored formally—informational only
- Identify qualified vendors for future RFP
- Refine requirements based on market feedback
- Adjust budget expectations based on cost information
- May conduct one-on-one vendor meetings for deeper dives

**Benefits:**
Organizations using RFI first finalize vendor selection 23 days faster on average and reduce procurement cycles by 30-45 days overall.

**Stage 2: RFP (Request for Proposal)**

**Purpose:** Formal competitive procurement with detailed requirements

**When to Use:**
- After RFI qualification (narrow to 3-5 vendors)
- Requirements are well-defined
- Seeking best value (not just lowest cost)
- Complex solutions requiring detailed proposals

**Process:**
- **Duration:** 60-90 days from publication to response deadline
- **Vendor Effort:** 60-80 hours plus demos and presentations
- **Agency Effort:** 100-150 hours (writing RFP, evaluation, vendor demos, negotiations)

**RFP Content:**
- Detailed requirements (functional, technical, performance, security)
- Evaluation criteria and weights (typically: Technical approach 40%, Cost 30%, Experience 20%, Vendor qualifications 10%)
- Contract terms and conditions
- Statement of work and deliverables
- Implementation timeline and milestones
- SLA requirements and performance metrics

**Agile Contracting Language:**

Traditional government contracts are rigid, but modern development requires flexibility. Include:

**Iterative Development:**
"Solution shall be delivered incrementally using agile methodology with 2-week sprints. Agency and vendor will collaborate on prioritization through product owner role. Requirements may be refined based on user feedback during development."

**Scope Adjustments:**
"Contract allows up to 20% scope modification without formal amendment process. Changes must maintain overall budget and timeline while improving outcomes. Mutual agreement required."

**Performance-Based Payments:**
"Payments tied to delivery of working software in production, not hours worked. Each sprint deliverable must pass user acceptance testing before invoice approval."

**RFP Evaluation:**

**Technical Evaluation (Done First, Before Seeing Costs):**
Evaluation panel scores proposals against criteria using standardized scoresheet. Demos and presentations allow vendors to showcase solutions. Reference checks verify past performance.

**Cost Evaluation (Done After Technical):**
Evaluate total cost of ownership (licensing, implementation, training, ongoing support) not just initial price. Identify any unrealistic low-ball bids.

**Best Value Determination:**
Combine technical and cost scores using pre-defined weights. Highest scoring vendor wins, not necessarily lowest cost.

**Stage 3: RFQ (Request for Quote)**

**Purpose:** Price competition when requirements are fully defined

**When to Use:**
- Commodity purchases (hardware, standard software)
- Requirements completely specified, no ambiguity
- Price is primary differentiator
- Minimal evaluation needed beyond cost and compliance

**Process:**
- **Duration:** 15-30 days
- **Vendor Effort:** Minimal (price quote and compliance certification)
- **Agency Effort:** 10-20 hours

**RFQ Content:**
- Precise specifications (model numbers, quantities, delivery dates)
- Pass/fail compliance requirements
- Award to lowest responsive, responsible bidder

**Use Sparingly:** Most government IT needs are complex enough to require RFP, not RFQ.

### 5.3 Additional Modern Procurement Methods

**Modular Contracting:**

Break large projects into smaller, manageable components:
- **Example:** Instead of one $50M contract for entire case management system, separate contracts for:
  - $5M: Core database and workflow engine
  - $5M: Citizen-facing portal
  - $5M: Mobile applications
  - $5M: Analytics and reporting
  - $5M: Integration with legacy systems

**Benefits:**
- Reduces "too big to fail" syndrome
- Increases competition (small businesses can bid on components)
- Enables faster delivery (parallel development)
- Contains risk (failure of one component doesn't doom entire initiative)

**Challenge-Based Procurement:**

Define problems and outcomes, let vendors propose solutions:
- **Example:** "Reduce permit processing time by 50% while maintaining quality" rather than "Build permit system with these features"
- Vendors innovate on approach, not just execute specifications
- Similar philosophy to RFI² but can be used for smaller procurements

**Rapid Prototyping Contracts:**

Require 90-day pilots before full commitment:
- **Structure:** Award 3-5 vendors small contracts ($50K-$100K each) to build prototypes
- After 90 days, evaluate results and award implementation contract to most successful
- **Benefits:** "Try before you buy" dramatically reduces risk
- **Trade-off:** Longer initial timeline, but far less risk of failed large implementation

**Pre-Qualified Vendor Pools:**

Create California Technology Marketplace with pre-vetted vendors:
- **Process:** Annual or biannual solicitation for vendor qualifications across categories (cloud services, AI/ML, cybersecurity, etc.)
- Vendors undergo thorough evaluation once (financials, security, references, capabilities)
- Agencies can quickly procure from pool without full RFP process
- **Benefits:** Eliminate repetitive qualification, accelerate timelines, ensure baseline quality

**Hybrid RFP Process:**

California DGS authorizes under Public Contract Code Section 6611:
- **Stage 1:** Pre-qualify 2+ contractors based on qualifications, award contracts for proposal development
- **Stage 2:** Pre-qualified contractors submit detailed proposals, best value wins implementation contract
- Contractors may be paid for both stages
- **Benefits:** Compensates vendors for proposal effort, enables more detailed proposals, combines competition with early contractor involvement

---

## Section 6: Workforce Development & Talent Management

### 6.1 Skills Gap Analysis

California completed IT Classification Consolidation in 2018, consolidating 36 IT job classes into 9 to create clearer career paths and improve recruitment. However, skills gaps persist.

**Current State Challenges:**

**Critical Skills Deficits:**
- **Cloud Architecture and DevOps:** 70% of IT staff lack hands-on cloud experience (AWS, Azure, GCP)
- **AI/ML Capabilities:** 85% have minimal AI/ML knowledge despite growing need for intelligent automation
- **Cybersecurity Expertise:** 22 of 37 GAO high-risk areas involve skills gaps
- **API Design and Microservices:** Traditional developers skilled in monolithic systems
- **Data Science and Analytics:** Shortage of staff who can extract insights from data
- **Agile/Scrum Methodologies:** Waterfall culture dominates despite agile mandates

**Workforce Demographics:**
- Large cohort of Baby Boomer IT workers approaching retirement (40% eligible within 5 years)
- Knowledge loss risk as experienced staff retire
- Difficulty recruiting younger talent due to compensation gaps (private sector pays 20-40% more)

**Hiring Challenges:**
- Lengthy recruitment timelines (6-12 months from requisition to onboarding)
- Classification restrictions limiting flexibility
- Remote work policies less generous than private sector
- Benefits strong but not valued by younger workers as much as flexibility and mission

### 6.2 Digital Accelerators Program

Modeled on successful programs like GDIT's training of 20,000+ employees in AI, zero trust, 5G, and digital engineering.

**Curriculum Design:**

**Track 1: Cloud Fundamentals (All IT Staff)**
- Duration: 40 hours over 8 weeks
- Content: Cloud concepts, AWS/Azure/GCP basics, infrastructure-as-code, security
- Delivery: Mix of online modules and hands-on labs
- Certification: AWS Cloud Practitioner or Azure Fundamentals
- **Target: 100% of IT staff (2,000-3,000 employees) within Year 2**

**Track 2: DevOps and Automation (Developers and Infrastructure)**
- Duration: 80 hours over 12 weeks
- Content: CI/CD pipelines, containerization (Docker/Kubernetes), monitoring, GitOps
- Delivery: Instructor-led with project-based learning
- Certification: AWS DevOps Engineer or Kubernetes Administrator
- **Target: 50% of developers and infrastructure staff (500-800 employees) within Year 3**

**Track 3: AI/ML for Government (Analysts and Developers)**
- Duration: 60 hours over 10 weeks
- Content: Machine learning concepts, Python/TensorFlow, ethics and bias, government use cases
- Delivery: Mix of theory and practical projects using state data
- Certification: AWS ML Specialty or Google ML Engineer
- **Target: 30% of technical staff (400-600 employees) within Year 4**

**Track 4: Data Engineering and Analytics (Data Professionals)**
- Duration: 70 hours over 12 weeks
- Content: Data pipelines, ETL, SQL advanced, visualization (Tableau/PowerBI), governance
- Delivery: Hands-on with state datasets
- Certification: AWS Data Analytics or Databricks certification
- **Target: 100% of data professionals (300-500 employees) within Year 2**

**Track 5: Cybersecurity (All IT Staff + Specialized Track)**
- Duration: 40 hours foundational + 80 hours specialized
- Content: Zero Trust, NIST frameworks, threat detection, incident response
- Delivery: Simulated attack scenarios and red team exercises
- Certification: Security+ (foundational), CISSP (advanced)
- **Target: 100% foundational within Year 1, 200+ advanced certifications within Year 3**

**Track 6: Agile and Product Management (Leaders and PM)**
- Duration: 40 hours over 6 weeks
- Content: Agile principles, Scrum, product ownership, user stories, retrospectives
- Delivery: Simulation and role-playing exercises
- Certification: Certified Scrum Master or Product Owner
- **Target: 100% of project managers and tech leaders (300-400 employees) within Year 2**

**Delivery Model:**

**Blended Learning:**
- 40% self-paced online modules (flexibility for staff schedules)
- 40% instructor-led virtual sessions (live interaction and Q&A)
- 20% hands-on labs and projects (practical application)

**Protected Learning Time:**
Mandate 20% of work hours (equivalent to 1 day per week) allocated to training and development:
- Supervisors cannot assign competing deadlines during learning time
- Performance evaluations include learning participation and completion
- Career advancement requires continuous skill development

**Vendor Partnerships:**
- AWS, Microsoft Azure, Google Cloud provide training credits and certification vouchers
- Coursera, LinkedIn Learning, Pluralsight provide online content
- Local universities (UC, CSU) provide instructors and curriculum development

**Budget:**
- **Year 1:** $10M (curriculum development, platform licenses, initial cohorts)
- **Years 2-3:** $25M/year (peak training delivery)
- **Years 4-5:** $15M/year (ongoing sustainment and new hire onboarding)

### 6.3 Governor's Innovation Fellowship Integration

**Fellowship Overview:**
6-month delivery-focused program (not traditional leadership development) where Fellows dedicate 80% of time to priority projects improving efficiency, service delivery, and customer experience.

**Current Structure:**
- New cohorts every 4 months with overlapping knowledge transfer
- Fellows receive training from ODI, CalAcademy, private sector partners (California Breakthrough Project), and academia
- Placed in agencies and departments to work on specific transformation initiatives

**E3 Integration Strategy:**

**Fellowship as E3 Talent Pipeline:**

**During Fellowship (Months 1-6):**
- Fellows placed with Undersecretaries or Chief Deputy Directors (when positions exist) or in departments prioritized for E3 deployment
- Projects aligned with E3 modernization priorities (legacy migration, API development, process automation, data governance)
- Mentorship from California Breakthrough Project advisors
- Exposure to multiple aspects of transformation (technology, procurement, change management)

**Post-Fellowship Transition:**
- Fellows demonstrating strong delivery outcomes receive preferential hiring consideration for E3 positions
- Structured transition: Fellowship → temporary assignment in E3 role → permanent hire
- Cohort model ensures continuous pipeline (3 cohorts per year = 30-60 candidates annually)

**Preferential Hiring Framework:**

**Criteria for Preferential Consideration:**
1. **Delivery Results:** Successfully completed Fellowship project with measurable outcomes
2. **Technical Capability:** Demonstrated skills in modernization technologies (cloud, APIs, data, automation)
3. **Change Management:** Effectively navigated government culture and built stakeholder support
4. **Leadership Potential:** Ability to influence without direct authority
5. **Cultural Fit:** Alignment with E3 values (citizen-centric, evidence-based, collaborative)

**Hiring Process:**
1. E3 position opens → Fellows who meet criteria are invited to apply
2. Streamlined interview process (Fellows already vetted during Fellowship)
3. 30-day placement decision (versus 6-12 months for external hires)
4. Fellows receive priority over external candidates of similar qualifications

**Benefits:**
- **For California:** Pre-vetted talent with demonstrated delivery capability and government context knowledge
- **For Fellows:** Career path beyond temporary assignment, competitive compensation, mission-driven work
- **For E3 Program:** Accelerated staffing avoiding lengthy recruitment

**Target Metrics:**
- 50% of E3 positions filled by Innovation Fellows within Years 2-3
- 90% retention rate of Fellows hired into E3 roles after 2 years
- Average time-to-hire reduced from 9 months to 2 months for Fellows

### 6.4 Additional Workforce Strategies

**Apprenticeship Programs:**

Model: DOD SkillBridge 180-day civilian apprenticeships

**California Implementation:**
- Partner with private sector tech companies (Google, Salesforce, Oracle, etc.) to host government employees for 3-6 month rotations
- Employees learn cutting-edge practices and bring knowledge back to government
- Companies gain insight into government challenges, potentially informing future product development
- **Target:** 50-100 participants per year

**Public-Private Talent Rotations:**

**Inbound:** Private sector technologists on loan to government (1-2 year assignments)
- Example: Silicon Valley engineers working on CDCR modernization or CalHHS data integration
- Compensation: Employer continues salary, or California provides competitive compensation
- Benefits: Fresh perspectives, technical expertise, industry best practices

**Outbound:** Government employees on temporary assignment to private companies
- Learn modern development practices, product management, customer experience design
- Return to government with new skills and networks
- **Target:** 20-30 exchanges per year

**Competitive Compensation:**

**Challenge:** Government IT salaries lag private sector by 20-40%

**Strategies:**
- **E3 Position Premium:** Undersecretary and Chief Deputy Director roles compensated at executive levels (competitive with private sector VP/Director roles)
- **Retention Bonuses:** For critical skills (cybersecurity, AI/ML, cloud architects) provide 10-20% bonuses
- **Recruitment Incentives:** Sign-on bonuses for hard-to-fill positions ($10K-$25K)
- **Performance Bonuses:** Tie 10-15% of compensation to achievement of KPIs

**Total Compensation Messaging:**
While base salary may be lower, emphasize:
- **Pension:** CalPERS defined benefit plan (private sector typically 401k only)
- **Healthcare:** Excellent coverage with low employee premiums
- **Work-Life Balance:** Fewer hours than private sector "grind culture"
- **Mission:** Public service impact and meaningful work
- **Stability:** Recession-resistant employment

**Remote Work and Flexibility:**

**Post-Pandemic Reality:** Talent expects flexibility

**California Policy:**
- **Hybrid Standard:** 3 days in office, 2 days remote for most IT positions
- **Full Remote Options:** For roles not requiring physical presence (developers, data analysts)
- **Geographic Flexibility:** Recruit statewide, not just Sacramento area
- **Results-Based Management:** Focus on outcomes, not hours at desk

---

*This completes Part 2 covering Data Strategy, Procurement, and Workforce. Part 3 will continue with Performance Measurement, Change Management, and Implementation Planning.*