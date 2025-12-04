# California Enterprise Modernization Plan
## Comprehensive Strategic Plan - Part 2 of 3

**Prepared for:** Governor's Office, Office of Data and Innovation, Government Operations Agency  
**Date:** December 2025  
**Version:** Executive draft v1.0

---

## Table of Contents - Part 2

5. [Technology Architecture](#5-technology-architecture)
6. [Procurement Innovation](#6-procurement-innovation)
7. [Talent Development and Sustainability](#7-talent-development-and-sustainability)

*Note: Part 1 covers Strategic Foundation, E3 Model, Independent Data Governance, and Product-Led Delivery. Part 3 covers Breakthrough Modernization Fund and Implementation Roadmap.*

---

## 5. Technology Architecture

### 5.1 API Management Strategy

**Centralized API Gateway:**

A unified API gateway provides the entry point for all API traffic, enabling consistent security, monitoring, and governance across California's digital services.

**Core Capabilities:**
- Single entry point for all API traffic (internal and external)
- Enforces authentication, authorization, rate limiting, and logging
- Provides analytics on API usage patterns and performance
- Enables A/B testing and canary deployments for continuous improvement
- Supports versioning and backward compatibility

**Developer Portal:**

A comprehensive developer portal democratizes access to California's government services through well-documented, self-service APIs.

**Features:**
- Unified catalog of all state government APIs (searchable by function, agency, data type)
- Interactive API documentation (OpenAPI/Swagger specifications)
- Self-service API key provisioning with approval workflows
- Code samples and SDKs in multiple languages (Python, JavaScript, Java, C#)
- Sandbox environments for testing without production impact
- Support forums and ticketing system for developer assistance
- Usage dashboards showing consumption and performance

**API Classification:**

California establishes three tiers of APIs with appropriate access controls and service levels:

**Public APIs:** Available to any consumer (developers, researchers, businesses, citizens)
- Minimal authentication (API key registration with email verification)
- Generous rate limits (10,000 requests/day per key)
- Published on public developer portal (developer.ca.gov)
- Examples: Business registry lookup, public datasets, geospatial data, licensing information

**Partner APIs:** Available to approved external organizations (contractors, research institutions, local governments)
- OAuth 2.0 authentication with formal approval process
- Moderate rate limits (100,000 requests/day)
- Formal SLA and dedicated support channels
- Examples: Case management systems, benefit eligibility verification, identity verification

**Internal APIs:** Available only to state government systems and authorized staff
- Mutual TLS authentication with certificate management
- High rate limits (1,000,000 requests/day)
- Internal developer portal with additional security documentation
- Examples: PII data access, financial systems, law enforcement databases

**Deployment Target:** 200 APIs published within 2 years (50 public, 50 partner, 100 internal)

### 5.2 Legacy System Modernization

**Strangler Pattern (Preferred Approach):**

California adopts the strangler pattern for legacy modernization, avoiding risky "big bang" replacements in favor of incremental transformation while maintaining operational continuity.

**Process:**
1. **Create API Facade:** Wrap legacy system with API layer providing modern interface to old functionality
2. **Build New Microservice:** Develop cloud-native service replicating one discrete function
3. **Route Intelligently:** Direct new requests to microservice while legacy requests continue to old system
4. **Migrate Gradually:** Incrementally shift functionality to new services based on usage patterns and risk assessment
5. **Decommission Legacy:** Remove legacy system components when usage reaches zero and all functionality migrated

**Benefits:**
- **Lower Risk:** No catastrophic cutover; system remains operational throughout migration
- **Continuous Value:** Users experience improvements incrementally rather than waiting years
- **Course Correction:** Ability to pause, adjust strategy, or pivot based on learnings
- **Service Availability:** Maintains citizen access throughout modernization process
- **Resource Flexibility:** Can accelerate or slow migration based on resource availability and competing priorities

**Sunset Timelines:**

California establishes clear timelines for legacy system retirement based on technical debt and criticality:

- **High technical debt + high criticality:** 2-year maximum lifespan from assessment
- **High technical debt + medium criticality:** 3-year maximum
- **Medium technical debt:** 5-year maximum
- **Automatic review trigger:** Systems exceeding planned lifecycle must justify continuation annually

**Modernization Portfolio Targets:**
- **Year 1:** Complete comprehensive assessment across all departments; decommission 10% of legacy systems (40 systems)
- **Year 2:** Decommission 10% more (20% cumulative); complete API facades for 50 high-priority systems
- **Year 3:** Decommission 10% more (30% cumulative); achieve 50% reduction in legacy technical debt
- **Years 4-5:** Achieve 40% total legacy reduction target while maintaining operational stability

### 5.3 Cloud Strategy

**Hybrid Cloud with On-Premises Redundancy:**

To protect state business operations in the event of internet outage or cloud service disruption, California adopts a hybrid cloud strategy that maintains on-premises redundancy for critical systems.

**Architecture Principles:**

**Cloud-First for New Development:** All new systems deployed to cloud unless specific exception granted based on:
- Data sovereignty requirements (specific statutes mandating on-premises storage)
- Latency requirements incompatible with cloud architecture
- Cost analysis showing on-premises more cost-effective over 5-year horizon
- Security requirements exceeding cloud provider capabilities

**Critical System Redundancy:** Mission-critical systems maintain on-premises backup capability enabling continued operations during cloud outages.

**Hybrid Connectivity:** Secure, redundant connections between cloud and on-premises infrastructure:
- Multiple dedicated interconnects from different providers
- VPN backup connectivity
- Automatic failover between connectivity paths
- Continuous monitoring of connection health

**Multi-Cloud Strategy:** Avoid single cloud vendor lock-in through multi-cloud deployment where feasible:
- Critical applications deployed across multiple cloud providers
- Containerized workloads enabling portability
- Infrastructure-as-Code supporting multi-cloud deployment
- Careful analysis of multi-cloud complexity vs. flexibility benefits

**Critical Systems Requiring On-Premises Redundancy:**

Examples of systems that must maintain on-premises operational capability:

- **Emergency Services:** 911 dispatch, CAL FIRE coordination, emergency management systems, emergency alert systems
- **Law Enforcement:** Criminal justice information systems, arrest and booking systems, warrant management
- **Public Safety:** Prison management systems, probation and parole tracking, sex offender registry
- **Benefits Delivery:** CalFresh, Medi-Cal eligibility, unemployment insurance payments, child support
- **Critical Infrastructure:** Water management systems, power grid coordination, transportation management
- **Financial Systems:** Payroll processing, tax collection, treasury operations, pension management

**Implementation Strategy:**
- **Primary workloads run in cloud** for scalability, elasticity, and cost efficiency
- **Critical data replicated to on-premises systems** in near-real-time (typically < 5 minute lag)
- **On-premises systems capable of maintaining operations** during internet disruption (degraded capacity acceptable)
- **Regular failover testing** (quarterly minimum) to ensure redundancy effectiveness
- **Automated failback** when cloud connectivity restored, with data reconciliation
- **Clear procedures** for manual intervention if automated failover fails

**Cloud Provider Requirements:**
- FedRAMP-certified cloud providers (AWS GovCloud, Microsoft Azure Government, Google Cloud Platform)
- FISMA compliance appropriate to data sensitivity (Moderate or High)
- StateRAMP (California-specific requirements including data residency, audit access, breach notification)
- SLA guarantees: 99.9% uptime for production services, 99.99% for critical systems
- Geographic redundancy within California or western United States where possible

**Cloud-Native Architecture:**

California adopts modern cloud-native patterns to maximize cloud benefits:

- **Containers and Orchestration:** Docker containers managed by Kubernetes enabling portability and scaling
- **Serverless Computing:** AWS Lambda, Azure Functions, or Google Cloud Functions for event-driven workloads
- **Managed Services:** Leverage cloud provider services reducing operational overhead (managed databases, message queues, caching)
- **Infrastructure as Code (IaC):** Terraform or CloudFormation for repeatable, version-controlled infrastructure
- **Automated Backup and Disaster Recovery:** Cloud-native backup with cross-region replication
- **Auto-Scaling:** Automatically adjust capacity based on demand
- **Immutable Infrastructure:** Replace rather than update infrastructure components

**Migration Approach:**
- **Prioritize high-cost, low-complexity workloads first** (quick wins demonstrating value)
- **Use lift-and-shift for initial migration**, then re-architect for cloud-native over time
- **Implement strong cloud governance:** Cost management, security controls, compliance monitoring, tagging standards
- **Data center consolidation** as workloads migrate, reducing facilities costs
- **Hybrid period of 3-5 years** recognizing gradual transition

**Target:** 50% of workloads in cloud by Year 3, with all critical systems maintaining on-premises redundancy

### 5.4 Cybersecurity

**Zero Trust Architecture:**

California transitions from perimeter-based security to Zero Trust, recognizing that threats exist both outside and inside the network.

**Core Principles:**
- **Identity-based access:** Authentication based on user/service identity, not network location
- **Least privilege:** Minimum necessary access for users and systems
- **Assume breach:** Design assuming attackers have network access
- **Verify explicitly:** Authenticate and authorize every access request
- **Continuous verification:** Re-authenticate throughout session, not just at login

**Implementation:**

**Single Federated Identity System:**
- Unified identity management for all state services and employees
- Multi-factor authentication (MFA) required for all accounts
- Risk-based authentication adjusting requirements based on user behavior and context
- Single sign-on (SSO) reducing password fatigue and improving user experience
- Integration with CalHR for employee lifecycle management

**Access Control:**
- Role-based access control (RBAC) with regular access reviews
- Attribute-based access control (ABAC) for fine-grained permissions
- Just-in-time (JIT) access for privileged operations
- Session recording for auditing high-risk actions

**Network Segmentation:**
- Micro-segmentation limiting lateral movement
- Software-defined perimeter (SDP) controlling network access
- East-west traffic inspection (not just north-south)

**Standards Compliance:**

**NIST Cybersecurity Framework:**
- Identify, Protect, Detect, Respond, Recover functions
- Maturity assessment and roadmap for improvement
- Alignment with federal requirements for interoperability

**NIST 800-53 Security and Privacy Controls:**
- Moderate or High baseline depending on data sensitivity
- Continuous monitoring and control assessment
- Documentation of control implementation and effectiveness

**California-Specific SIMM 5300 Requirements:**
- State-specific security and privacy requirements
- Information security program requirements
- Incident reporting obligations

**Data Protection:**

**Encryption:**
- **In Transit:** TLS 1.3 for all network communications (TLS 1.2 minimum)
- **At Rest:** AES-256 encryption for all databases and file storage
- Key management via Hardware Security Modules (HSM) or cloud key management services
- Regular key rotation following NIST guidelines

**PII Protection:**
- Automatic PII detection and classification
- Redaction of PII in logs and error messages
- Tokenization for PII in non-production environments
- Data loss prevention (DLP) tools monitoring PII movement

**Audit Logging:**
- All data access logged with user, timestamp, data accessed, action performed
- Logs retained for 7 years (or longer for high-sensitivity data)
- Centralized log aggregation and analysis
- Tamper-proof log storage
- Regular review of access patterns and anomalies

**Security Operations:**

**24/7 Security Monitoring:**
- Security Information and Event Management (SIEM) aggregating logs from all systems
- Security Operations Center (SOC) staffed 24/7/365
- Automated threat detection using machine learning
- Integration with threat intelligence feeds

**Automated Threat Detection and Response:**
- Intrusion detection and prevention systems (IDS/IPS)
- Endpoint detection and response (EDR)
- User and entity behavior analytics (UEBA)
- Automated response to common threats (e.g., blocking suspicious IPs)

**Incident Response:**
- Documented incident response plan with defined roles and procedures
- Tabletop exercises quarterly testing response procedures
- Forensic capabilities for investigation
- Communication protocols for breach notification
- Post-incident reviews and lessons learned

**Vulnerability Management:**
- Continuous vulnerability scanning of all systems
- Automated patching for non-critical systems
- Expedited patching for critical vulnerabilities (48-hour target)
- Regular penetration testing (annual for critical systems, biennial for others)
- Bug bounty program encouraging responsible disclosure

**Security Awareness:**
- Annual security training required for all employees
- Monthly security tips and phishing simulations
- Specialized training for developers (secure coding) and administrators (hardening)
- Recognition program for security champions

### 5.5 Staff Empowerment for Agentic Data Systems

**Vision:**

Enable California state staff to create AI-powered data workflows using state-approved patterns and shared infrastructure, accelerating data analysis and decision-making while maintaining security, privacy, and quality standards.

**State-Approved Design Patterns:**

California develops and maintains a library of approved agentic design patterns that staff can use to build data workflows safely:

**Data Analysis and Visualization:**
- Automated data quality checking and reporting
- Natural language queries translating to SQL or API calls
- Automated dashboard generation based on data characteristics
- Anomaly detection and alerting

**Document Processing and Extraction:**
- Intelligent form data extraction from PDFs and images
- Document classification and routing
- Summarization of lengthy reports and submissions
- Translation of documents into multiple languages

**Workflow Automation and Case Management:**
- Automated case prioritization based on urgency and complexity
- Intelligent case routing to appropriate staff
- Automated status updates and notifications
- Predictive analytics for case outcomes

**Knowledge Base and Expert Systems:**
- Chatbots answering citizen questions based on policy documents
- Decision support systems incorporating regulations and best practices
- Automated policy impact analysis
- Institutional knowledge capture from retiring staff

**Standards and Guardrails:**

Every agentic design pattern must meet California's requirements for:

**Content Classification:**
- Clear labeling of AI-generated content
- Distinction between AI analysis and human judgment
- Appropriate disclaimers for citizen-facing content

**Accuracy Requirements:**
- Validation thresholds for AI outputs (typically 95%+ accuracy for production use)
- Human review requirements for high-stakes decisions
- Fallback to human judgment when confidence below threshold

**Bias Testing:**
- Documented testing for demographic bias
- Disparate impact analysis where applicable
- Mitigation strategies for identified biases

**Transparency:**
- Explainability of AI decisions (how conclusion reached)
- Data provenance (what data informed the analysis)
- Model cards documenting capabilities and limitations

**Logging and Audit:**
- All AI interactions logged for audit and improvement
- Feedback mechanisms capturing accuracy and usefulness
- Regular review of AI performance and drift

**Version Control:**
- Documented versions of prompts, models, and training data
- Rollback capability when new versions underperform
- A/B testing of model improvements

**Shared Infrastructure:**

California provides shared infrastructure enabling staff to build agentic workflows without individual departments procuring and managing AI systems:

**CDT-Operated Enterprise AI Platform:**
- Centralized access to approved large language models (LLMs)
- Compute resources for training and inference
- Managed services for common AI tasks (OCR, translation, sentiment analysis)
- Unified billing and cost allocation
- Enterprise security and compliance controls

**Departmental Sandboxes:**
- Isolated environments for experimentation and development
- Access to production data copies (anonymized where appropriate)
- Testing framework for validating accuracy and performance
- Promotion pathway from sandbox to pilot to production

**Template Library:**
- Pre-built templates for common use cases
- Customization guidance for department-specific needs
- Community contributions from across state government
- Documentation and training materials

**Deployment Process:**

California establishes a streamlined pathway from idea to production:

1. **Sandbox Development:** Staff build and test agentic workflow in departmental sandbox (days/weeks)
2. **Testing and Validation:** Automated testing validates accuracy, bias, security (1-2 weeks)
3. **Security Scan:** Automated security scanning checks for vulnerabilities and policy compliance (days)
4. **Peer Review:** Review by E3 data governance team ensuring standards compliance (1 week)
5. **Pilot Deployment:** Limited rollout to small user group with monitoring (4-8 weeks)
6. **Production Deployment:** Full rollout with ongoing monitoring and improvement (ongoing)

**Timeline:** Sandbox to production in 8-12 weeks for typical workflow (versus 12-18 months traditional system development)

**Expected Impact:**
- Staff able to automate 20-30% of routine data analysis tasks
- Faster insights enabling more responsive policy and operations
- Reduced backlog of data requests and analysis needs
- Upskilling of workforce in AI literacy and capabilities
- Democratization of data analysis beyond specialized analysts

---

## 6. Procurement Innovation

**Philosophy:** Cheap, scalable, self-supportable solutions over monolithic enterprise systems

California fundamentally rethinks technology procurement, moving away from massive multi-year contracts toward agile, modular approaches that reduce risk, increase competition, and enable innovation.

### 6.1 Modular Contracting

**The Rule:** No IT contract over $10 million or 3 years without legislative waiver

**Rationale:**

Large, monolithic IT contracts consistently underperform or fail outright. California's history includes multiple failed projects exceeding $100M with minimal value delivered. The $10M modular contracting cap forces better outcomes by:

**Reducing Risk:**
- Smaller contracts mean smaller failures
- Failed module does not jeopardize entire system
- Ability to course correct quickly without massive sunk costs
- Natural checkpoints for go/no-go decisions

**Increasing Competition:**
- Lower contract values accessible to small and mid-size vendors
- More innovative vendors can compete without massive corporate infrastructure
- Reduces dominance of large system integrators
- Multiple vendors can work in parallel on different modules

**Reducing Vendor Lock-In:**
- Modular architecture enables vendor replacement for underperforming components
- Competitive pressure maintains quality and cost discipline
- Avoids situation where vendor effectively holds state hostage

**Enabling "Fail Small and Fast":**
- Failed module costs $5M and 6 months, not $200M and 5 years
- Learnings from failed module inform subsequent attempts
- Political and public tolerance for smaller, less catastrophic failures

**Allowing Course Correction:**
- Technology and requirements change during multi-year projects
- Modular approach allows pivoting to new approaches without abandoning entire investment
- Can incorporate new technologies and best practices as they emerge

**Implementation:**

**Executive Order Establishing Cap:**
- Governor issues EO mandating $10M/3-year maximum for IT contracts
- Exceptions require legislative waiver with public justification
- CDT responsible for enforcement through procurement review

**Legislative Waiver Process:**
- Department must justify why project cannot be decomposed
- Technical review by CDT and TMO
- Public hearing demonstrating stakeholder support
- Approval by joint legislative oversight committee
- Enhanced oversight and reporting for waived projects

**CDT Enforcement:**
- All IT contracts over $1M require CDT review and approval
- Procurement checklist verifying modular approach considered
- Rejection of proposals exceeding cap without waiver
- Regular audit of contract portfolio for compliance

**Template Contracts:**
- Pre-negotiated modular contract templates reducing negotiation time
- Standard terms and conditions appropriate to module size
- Simplified approval process for contracts under $5M

**Vendor Prequalification:**
- Established vendor pools for modules under $1M
- Fast-track approval for pre-qualified vendors
- Quarterly refresh of vendor pools based on performance

**Expected Impact:**
- **50% reduction in average contract size** (from $30M average to $15M)
- **30% increase in small business contract awards** (contracts under $5M)
- **40% reduction in project failure rates** (measured by on-time, on-budget completion with stated functionality)
- **25% reduction in procurement cycle time** (due to simpler, smaller procurements)

### 6.2 RFI² (Request for Innovative Ideas) Process

California pioneered RFI² through Executive Order N-04-19, creating an innovative procurement method that asks vendors to design solutions to complex problems rather than bidding on predefined solutions.

**When to Use RFI²:**

RFI² is appropriate for:
- **Complex technical challenges** without obvious solutions (emerging technologies, novel applications)
- **Emerging technology applications** (AI/ML, blockchain, IoT) where best approach unclear
- **Cross-cutting problems** affecting multiple agencies requiring coordinated solutions
- **High uncertainty** requiring experimentation and learning rather than traditional specification
- **Innovation opportunity** where creative approaches could deliver step-change improvements

RFI² is NOT appropriate for:
- Well-defined requirements with proven solutions
- Commodity purchases (hardware, licenses)
- Time-critical needs requiring immediate procurement
- Low-risk, straightforward implementations

**Phase 1: Innovation Concept Papers**

**Step 1: Problem Statement Development (Weeks 1-4)**

**Internal Workshops:**
- Cross-functional team defines problem without prescribing solutions
- Focus on outcomes, not technologies
- Include program staff, IT staff, E3 leaders, citizen representatives

**Problem Statement Contents:**
- Background and context
- Current state challenges (quantified where possible)
- Desired outcomes (specific, measurable)
- Constraints (budget, timeline, regulatory, technical)
- Evaluation criteria (how proposals will be assessed)
- Available data and systems for integration

**Example Problem Statement:**
> **Challenge:** California issues 500,000+ professional licenses annually across 40+ boards and bureaus. Applicants must navigate fragmented systems, submit duplicate information, and wait months for processing. 60% of applications require manual review due to missing or inconsistent data. We seek innovative approaches to create a unified licensing experience that reduces applicant burden by 50%, accelerates processing time by 60%, and improves data quality to 95%+ accuracy.

**Step 2: Innovation Conference (Week 5)**

**Public Event Format:**
- Half-day event bringing together potential vendors, entrepreneurs, researchers, government staff
- Problem statement presentation by agency leadership
- Technical deep-dive on systems and data
- Q&A session addressing vendor questions
- Networking opportunity connecting potential partners
- Virtual participation option for remote attendees

**Promotional Activities:**
- Announcement 8 weeks prior
- Outreach to university research centers, startup accelerators, industry associations
- Social media campaign highlighting innovation opportunity
- Partnerships with Code for America, civic tech community

**Step 3: Concept Paper Solicitation (Weeks 6-15)**

**Solicitation Period:**
- 60-90 day window for submissions (longer for complex challenges)
- Rolling submission to encourage early submissions

**Concept Paper Requirements:**
- 10-15 page limit focusing on ideas, not credentials
- Sections: Problem understanding, Proposed approach, Innovation elements, Feasibility assessment, Team capabilities, Preliminary cost estimate
- Supporting materials: Architecture diagrams, mockups, relevant case studies
- No requirement for detailed pricing (order-of-magnitude sufficient)

**Support for Proposers:**
- Office hours with technical staff answering questions
- Access to sample data and system documentation
- Sandbox environment for testing integration approaches

**Step 4: Evaluation and Selection (Weeks 16-21)**

**Evaluation Panel Composition:**
- Agency subject matter experts (40% weight): Understand problem deeply, assess feasibility
- Technical experts (30% weight): Assess technical approach and innovation
- Breakthrough advisors (20% weight): Evaluate innovation and replicability
- Procurement/legal (10% weight): Ensure compliance and contractibility

**Evaluation Criteria:**
- Problem understanding (15%)
- Innovation and creativity (25%)
- Technical feasibility (20%)
- Implementation approach (20%)
- Team capability (10%)
- Cost reasonableness (10%)

**Selection:**
- Select 2-5 proposals for Phase 2 (sweet spot typically 3)
- More selections if strong proposals and budget allows
- Fewer if proposals lack quality

**Compensation for Phase 1:**
- Modest compensation for selected vendors ($25K-$50K per vendor)
- Recognizes intellectual property contribution
- Builds goodwill and participation

**Phase 2: Proof of Concept Development**

**Step 5: PoC Planning (Weeks 22-26)**

**Refinement Activities:**
- Selected vendors refine approach based on feedback
- Detailed technical planning
- Define success criteria and testing methodology
- Establish 90-day pilot timeline
- Negotiate PoC contract ($250K-$500K typically)

**Success Criteria:**
- Specific, measurable outcomes for pilot
- Technical performance benchmarks
- User acceptance thresholds
- Data quality requirements
- Security and compliance checkpoints

**Step 6: PoC Execution (Months 6-9)**

**Development:**
- Vendors build working prototypes
- Access to production-like environments and data
- Integration with existing systems where needed
- Regular check-ins (weekly) with project team

**Testing:**
- Testing with actual government users (not vendor testers)
- Realistic scenarios and workflows
- Accessibility and usability testing
- Security testing and compliance verification
- Performance and load testing

**Iteration:**
- Bi-weekly demos showing progress
- Feedback incorporation and adjustment
- Problem-solving when challenges emerge
- Documentation of learnings

**Step 7: PoC Evaluation and Contract Award (Months 10-12)**

**Demonstration:**
- Final demonstration to stakeholders
- Live system walkthrough
- User testimonials and feedback
- Performance data presentation
- Cost analysis and ROI projection

**Final Evaluation:**
- Did PoC meet success criteria?
- User acceptance and satisfaction
- Technical performance and reliability
- Security and compliance
- Cost-effectiveness and sustainability
- Scalability to full production

**Contract Award:**
- Award contract for full implementation to best-performing vendor
- Negotiate final scope and pricing
- Alternative: Award to multiple vendors for different modules
- Possibility: No award if no PoC successful (fail small and regroup)

**Budget Allocation:**

Reserve 15-25% of technology modernization budget for RFI² projects recognizing:
- Higher risk tolerance for innovation
- Learning value even from unsuccessful experiments
- Breakthrough potential justifying investment

**Expected RFI² Volume:**
- Year 1: 3-5 RFI² solicitations (pilot phase)
- Year 2: 8-12 solicitations (scaling)
- Year 3+: 10-15 solicitations annually (mature program)

### 6.3 Pre-Qualified Vendor Pools + Small Business Equity

**Challenge:**

Traditional procurement takes 18-24 months from requirement definition to contract award, delaying technology adoption and increasing costs. Small businesses face barriers competing for government contracts due to lengthy, expensive procurement processes.

**Solution:**

Establish pre-qualified vendor pools for common needs, with tiered structure prioritizing small businesses.

**Tiered Vendor Structure:**

**Tier 1: Small Businesses and DVBEs**
- Criteria: <100 employees, <$20M annual revenue
- Includes: Disabled Veteran Business Enterprises (DVBEs), Small Business Enterprises (SBEs), Microbusinesses
- Advantages: First consideration for contracts under $1M, simplified compliance requirements

**Tier 2: Medium Businesses**
- Criteria: 100-500 employees, $20M-$100M revenue
- Includes: Mid-size firms with specialized capabilities
- Advantages: Competitive for contracts $1M-$10M

**Tier 3: Large Enterprises**
- Criteria: 500+ employees, $100M+ revenue
- Includes: Major system integrators and established vendors
- Advantages: Capability for complex, large-scale implementations

**Pool Categories:**

Vendor pools established for common technology needs:

**Cloud Services and Infrastructure:**
- Cloud architecture and migration
- Managed cloud services
- Cloud cost optimization
- Multi-cloud integration

**Agile Software Development:**
- Custom application development
- Mobile app development
- API development and integration
- DevOps and CI/CD

**Data Analytics and Visualization:**
- Business intelligence and dashboards
- Data science and machine learning
- Geospatial analysis and GIS
- Data governance and quality

**Cybersecurity Services:**
- Security assessments and penetration testing
- Security monitoring and SOC services
- Compliance and audit support
- Incident response

**Change Management and Training:**
- Organizational change management
- Training development and delivery
- User adoption and support
- Communication and stakeholder engagement

**User Experience and Design:**
- User research and journey mapping
- Service design and prototyping
- Accessibility testing and remediation
- Design systems and components

**Pool Establishment Process:**

**Annual RFP:**
- Single annual RFP to establish vendor pools
- Vendors pre-qualified based on capabilities, experience, past performance, rates
- Pool valid for 1 year with option to renew

**Qualification Criteria:**
- Demonstrated capability in category
- Relevant experience (3+ projects in category)
- Quality references from clients
- Reasonable and competitive rates
- Financial stability
- Security clearance where applicable

**Task Order Process:**
- Department issues task order to pre-qualified vendor
- Simplified statement of work and pricing
- Competitive bidding among pool vendors for larger task orders
- Direct award to single vendor for smaller task orders (<$250K)
- Award within days/weeks instead of months

**Performance Tracking:**
- Quarterly performance reviews of all vendors
- Metrics: On-time delivery, budget performance, quality, client satisfaction
- Poor performers removed from pool
- High performers highlighted and rewarded with additional opportunities

**Set-Asides and Requirements:**

**Contracts Under $1M:**
- First consideration to Tier 1 vendors (small businesses and DVBEs)
- If no qualified Tier 1 vendor available, open to Tier 2 and 3

**Contracts $1M-$5M:**
- Tier 1 subcontractor requirements (minimum 25% of contract value)
- Encourages large firms to partner with small businesses
- Builds capacity in small business community

**Contracts Over $5M:**
- Small business participation plan required
- Goal: 25% of contract value to Tier 1 vendors
- Mentor-protégé programs encouraging knowledge transfer

**Statewide Goal:**
- 25% of total IT spend to Tier 1 vendors by Year 3
- Reported quarterly with agency-level breakdowns
- Recognition for agencies exceeding goal

**Expected Impact:**
- **60% reduction in procurement cycle time** (from 18-24 months to 2-4 months)
- **40% increase in small business contracts** (from 15% to 25% of total IT spend)
- **30% increase in vendor diversity** (more vendors competing, less concentration)
- **20% cost savings** (increased competition driving down rates)
- **Economic development** (strengthening California's technology ecosystem)

---

## 7. Talent Development and Sustainability

### 7.1 Governor's Innovation Fellowship Program

The Fellowship establishes a continuous pipeline of emerging leaders trained to drive enterprise-wide government modernization.

**Program Structure:**

**Cohort Model:**
- **60 fellows per year** through continuous pipeline
- **6-month cohort duration** with structured curriculum and real-world projects
- **New cohort every 4 months** creating 2-month overlap between cohorts
- **3 cohorts active per year** (Cohorts start in January, May, September)
- **20 fellows per cohort** (optimal size for learning community and project teams)

**Timeline Example:**
- **Cohort 1:** January-June 2026 (20 fellows)
- **Cohort 2:** May-October 2026 (20 fellows, overlaps with Cohort 1 in May-June)
- **Cohort 3:** September 2026-February 2027 (20 fellows, overlaps with Cohort 2 in Sep-Oct)
- **Result:** Continuous pipeline with 60 fellows per year, 40 fellows active at any time

**Program Components:**

**1. Foundational Bootcamp (Weeks 1-2)**

**Executive Presence and Storytelling:**
- Communicating complex ideas simply
- Presenting to executives and elected officials
- Writing concise memos and briefings
- Building credibility and influence

**Innovation Process Foundations:**
- Design thinking and human-centered design
- Rapid prototyping and iterative development
- Systems thinking and complexity navigation
- Lean startup and agile methodologies

**Problem-Solving Workshops:**
- Structured problem definition
- Root cause analysis
- Hypothesis generation and testing
- Data-driven decision making

**Governance and Policy Landscape:**
- California government structure and budgeting
- Legislative process and advocacy
- Administrative law and rulemaking
- Interagency coordination mechanisms

**Statewide Leadership Introductions:**
- Meet agency secretaries, undersecretaries, department directors
- Understand strategic priorities and challenges
- Build relationships for future collaboration

**Cohort Covenant:**
- Shared expectations and accountability
- Peer support and collaboration norms
- Commitment to learning and growth

**2. Leadership Breadth Program (Months 1-3)**

**Listening Sessions:**
- 8-10 sessions with executives across diverse departments
- Exposure to different organizational cultures and challenges
- Mix of large operations (CDCR, DMV, DHCS), policy-focused (ARB, DWR), infrastructure (CALTRANS)
- Questions about challenges, priorities, modernization barriers

**Direct Engagement:**
- Small group discussions with agency leadership
- Shadowing executives in their day-to-day work
- Attending leadership meetings and decision-making forums
- Building understanding of competing priorities and constraints

**3. Innovation Process Training (Months 1-4)**

**Human-Centered Problem Definition:**
- User research methods (interviews, surveys, observation)
- Journey mapping and pain point identification
- Persona development
- Problem framing workshops

**Rapid Ideation and Concept Validation:**
- Brainstorming techniques
- Concept sketching and storyboarding
- Rapid prototyping (paper, digital, service blueprints)
- User testing and feedback incorporation

**Prototype Testing:**
- Testing with government staff (internal users)
- Testing with citizens (external users)
- Usability testing methodologies
- Interpreting feedback and iterating

**Government-Specific Change Management:**
- Understanding bureaucratic culture and resistance
- Building coalitions and securing buy-in
- Navigating procurement and policy constraints
- Communicating change effectively

**Implementation Roadmaps:**
- Phased rollout planning
- Risk identification and mitigation
- Resource requirements and budgeting
- Success metrics and evaluation

**4. Department Embedding (Full 6 Months)**

**Full-Time Placement:**
- Placed in department outside home agency for broader perspective
- Full-time immersion in operations (not side project)
- Office space and system access as regular employee
- Integration into departmental meetings and activities

**Project Ownership:**
- Assigned real business priority, not "make work" project
- Significant impact potential (not peripheral initiative)
- Autonomy and decision-making authority
- Budget and resources as needed

**Relationship Building:**
- Daily interaction with department staff
- Understanding organizational culture from inside
- Building trust and credibility through delivery
- Creating lasting relationships across agency boundaries

**Mentorship:**
- **Departmental Supervisor:** Day-to-day guidance, project oversight, operational support
- **Home Agency Mentor:** Bi-weekly meetings, career guidance, enterprise perspective
- **Cohort Peer:** Weekly peer mentoring, mutual support, shared learning

**Surrogate/Delegate Requirement:**
- Host department provides surrogate for business continuity
- Surrogate learns from Fellow, prepared to sustain work after Fellowship
- Knowledge transfer ensures project sustainability
- Creates multiplier effect (Fellow + Surrogate = 2 trained change agents)

**5. Group Initiatives (Full 6 Months)**

**Team Structure:**
- **4 concurrent initiatives** addressing high-priority cross-agency challenges
- **5 fellows per team** (from 20-fellow cohort: 4 teams of 5 each)
- **Executive sponsor** from Cabinet or GovOps providing direction and removing barriers
- **TMO liaison** providing methodology support and coordination

**Initiative Domains (Examples):**
- Business licensing modernization (cross-agency service integration)
- Data governance and sharing infrastructure (technical and policy framework)
- Customer experience platform (unified citizen portal)
- Procurement modernization (streamlined processes and vendor management)
- Emergency response coordination (disaster preparedness and response)

**Timeline and Deliverables:**

**Month 1-2: Research and Discovery**
- Stakeholder interviews (agencies, staff, citizens)
- Current state analysis
- Best practice research
- Problem definition and scoping

**Month 3-4: Concept Development**
- Ideation and solution design
- Rapid prototyping and testing
- Feasibility assessment (technical, financial, political)
- Refinement based on feedback

**Month 5: Roadmap Development**
- Implementation plan with phases and milestones
- Resource requirements and budget
- Risk assessment and mitigation
- Success metrics and evaluation plan

**Month 6: Presentation and Handoff**
- Executive recommendation document (20-30 pages)
- Implementation roadmap (detailed project plan)
- Identified implementation team (who will carry work forward)
- Presentation to Cabinet and Governor's Office

**Expected Outcomes:**
- Actionable recommendations for enterprise-wide improvements
- 50%+ of group initiatives approved for implementation
- Some initiatives directly transition to Breakthrough Fund projects
- Fellows gain experience leading complex, cross-agency initiatives

### 7.2 Post-Fellowship Engagement

**On-Call Subject Matter Expert Network:**

**Structure:**
- All fellows remain available to ODI for ongoing modernization work
- 5-10 hours/month average time commitment (flexible based on project needs)
- Paid as consulting engagement or detail from home agency
- Quarterly meetings of SME network for knowledge sharing

**Activation:**
- Specific initiatives needing expertise (e.g., former fellow led similar project)
- Departmental requests for support (e.g., fellow embedded in that department)
- Breakthrough Fund project support
- Capacity augmentation during peak periods

**Emergency Response Capacity:**

**Roster:**
- Emergency response roster of fellows from past 3-5 years
- Categorized by expertise (IT systems, data, cybersecurity, operations, communications)
- Pre-authorized for rapid activation

**Activation Scenarios:**
- IT system failures requiring immediate response
- Cybersecurity incidents needing surge capacity
- Natural disaster response coordination
- Pandemic or public health emergency
- Any operational crisis requiring expert support

**Response Protocol:**
- Rapid activation (24-48 hours notice)
- 3-5 fellows assembled based on relevant expertise
- Intensive engagement for duration of crisis (typically 2-6 weeks)
- Full-time detail from home agency or emergency contract
- After-action documentation and lessons learned

**Modernization Advisory Network:**

**Selection:**
- 2-3 alumni per cohort selected for ongoing advisory role
- Based on expertise, interest, and contribution during Fellowship

**Activities:**
- Quarterly meetings providing strategic input to ODI
- Working group participation (data governance council, digital services taskforce)
- Review of statewide modernization roadmap
- Input on Fellowship curriculum and improvements
- Mentoring of current fellows

**Sustainability Model:**

With 6-month cohorts starting every 4 months, California builds sustained capacity:

- **After 12 months:** 40 trained experts (2 cohorts graduated)
- **After 18 months:** 60 trained experts (3 cohorts graduated)
- **After 24 months:** 80 trained experts (4 cohorts graduated)
- **After 36 months:** 120+ trained experts (6+ cohorts graduated)

This creates a self-sustaining pipeline that compounds over time, with trained leaders deployed throughout state government driving continuous modernization.

### 7.3 Executive Duty Statement Integration

**Positioning Fellowship as Desired Qualification:**

As executive positions open or are reclassified, include fellowship participation as "desirable" or "highly valued" qualification.

**Sample Duty Statement Language:**

> **Desirable Qualifications:**  
> Completion of Governor's Innovation Fellowship or equivalent executive leadership development program focused on organizational modernization, cross-functional collaboration, and enterprise perspective. Fellowship graduates bring demonstrated understanding of state government systems, authentic relationships across multiple departments, hands-on experience with change management in complex organizations, and commitment to evidence-based modernization.

**Implementation Phases:**

**Phase 1 (Months 1-6):** Pilot in 10-15 senior positions
- Chief Data Officer and modernization officer roles
- Deputy secretary roles in priority agencies
- Director positions in high-impact departments

**Phase 2 (Months 6-12):** Expand to 20-30 positions
- Positions where enterprise perspective critical
- Cross-functional roles requiring collaboration
- Innovation and transformation leadership roles

**Phase 3 (Years 2-3):** Standardize across 40-50+ executive-level roles
- Routine inclusion in executive position duty statements
- Integration into succession planning
- Recognition as premier leadership development pathway

**Benefits:**

**For Fellows:**
- Competitive advantage in advancement
- Clear career pathway to executive roles
- Recognition of skills and experience
- Return on investment in Fellowship participation

**For State:**
- Leaders with enterprise perspective (not siloed)
- Established relationships enabling collaboration
- Reduced onboarding time (already know state government)
- Continuity of modernization efforts
- Culture of innovation and continuous improvement

### 7.4 Data Governance Teams (Permanent State Staff)

**Purpose:**

Provide sustainable capacity to support Fellows' projects and sustain innovations after Fellows complete assignments. Data governance teams are permanent civil service staff providing ongoing data management, quality, and integration capabilities.

**Blended Expertise Model:**

Effective data governance requires combining domain expertise with technical data skills:

**Domain Specialists:**
- Scientists, engineers, and subject matter experts
- Understand what data means, where it comes from, regulatory requirements
- Apply professional judgment to data quality and interpretation
- Ensure data governance aligns with programmatic needs

**Data Specialists:**
- Data architects, engineers, and analysts
- Build systems, pipelines, and integration infrastructure
- Implement technical data quality controls
- Enable self-service analytics and reporting

**Why Both Are Essential:**
- Domain specialists alone lack technical skills to implement solutions
- Data specialists alone lack context to make correct decisions about data
- Combined expertise delivers effective data governance

**Team Structure:**

**Leadership Tier:**

**Team Director:**
- Classification: Environmental Program Manager I or Senior Civil Engineer
- Salary Range: $9,500-$12,000/month
- Responsibilities: Overall team leadership, strategic direction, resource allocation, agency coordination

**Technical Team Lead:**
- Classification: Senior Environmental Scientist Supervisory or Senior Engineering Geologist
- Responsibilities: Domain standards development, technical quality oversight, cross-departmental collaboration

**Data Operations Lead:**
- Classification: Research Data Supervisor I/II
- Responsibilities: Data infrastructure management, technical architecture, system integration

**Specialist Tier:**

**Domain Standards Leads:**
- Classifications: Senior Environmental Scientist Specialist, Senior Engineering Geologist, Senior Civil Engineer
- Responsibilities: Sector-specific data standards, quality frameworks, regulatory compliance

**Senior Data Architect:**
- Classification: Research Data Specialist III
- Responsibilities: Enterprise data architecture, integration patterns, technical standards

**Journey/Operational Tier:**

**Data Quality Analysts:**
- Classifications: Environmental Scientist Range C, Engineering Geologist Range C/D, Associate Civil Engineer
- Responsibilities: Data quality assessment, validation rules, anomaly investigation

**Data Analysts:**
- Classifications: AGPA (generalist) or Research Data Analyst II (specialist)
- Responsibilities: Analysis, reporting, dashboard development, user support

**Administrative/Support Tier:**

**Program Coordinator:**
- Classification: AGPA
- Responsibilities: Project coordination, documentation, meeting facilitation, training coordination

**Administrative Support:**
- Classification: SSA (Staff Services Analyst)
- Responsibilities: Budget tracking, procurement support, general administration

**Student Assistants:**
- Classification: Student Assistant
- Responsibilities: Data entry, quality checking, research support, learning opportunity

**Standard Team Sizes:**

**Small Department Team (8-10 FTE):**
- 1 Director, 1 Technical Lead, 1 Data Operations Lead
- 2 Specialists, 3-4 Analysts
- 1 Coordinator

**Standard Department Team (13-15 FTE):**
- 1 Director, 1 Technical Lead, 1 Data Operations Lead
- 3-4 Specialists, 5-6 Analysts
- 1 Coordinator, 1 Administrative Support, 1-2 Student Assistants

**Large Department Team (20-25 FTE):**
- 1 Director, 2 Technical Leads, 1 Data Operations Lead
- 5-6 Specialists, 8-10 Analysts
- 2 Coordinators, 1 Administrative Support, 2-3 Student Assistants

**Why Science and Engineering Classifications:**

**Higher Compensation:**
- Professional classifications pay 20-30% more than administrative equivalents
- Essential for recruiting talent with technical degrees and expertise
- Competitive with private sector data roles (though still 20-40% gap)

**Critical Thinking Skills:**
- Scientists and engineers trained in analytical thinking, experimentation, validation
- Apply scientific method to data problems
- Comfortable with uncertainty and complexity

**Domain Expertise:**
- Many government datasets require domain knowledge (environmental, engineering, health, public safety)
- Professional classifications enable hiring experts who understand the data

**Professional Licensure:**
- PE (Professional Engineer) and PG (Professional Geologist) licenses provide accountability
- "Responsible charge" concept ensures quality and professional standards
- Important for data with regulatory or public safety implications

**Classification Alignment:**
- Consistent with how California already organizes technical work
- Leverages existing classification infrastructure
- Reduces HR complexity and approval challenges

**Professional Accountability:**

**Supervisory-Level Authority:**
- Supervisory classifications provide "responsible charge" over data systems and quality
- Similar to engineering supervisors responsible for project quality and safety
- Creates accountability for data governance outcomes

**Licensure (Where Applicable):**
- PE/PG licensure preferred for certain roles (engineering data systems, geospatial analysis)
- Professional ethics and standards applicable to data work
- Continuing education requirements keeping skills current

**Quality Requirements:**
- Classification standards embed scientific and engineering quality expectations
- Performance standards tied to data quality, accuracy, compliance
- Career advancement linked to demonstrated expertise and impact

**Deployment Strategy:**

**Phase 1 (Months 1-12): Pilot Deployment**
- 3-5 pilot departments selected based on Readiness Assessment
- Full team deployment with intensive support from TMO and ODI
- Establish team operating models and best practices
- Document lessons learned for broader rollout

**Phase 2 (Months 13-24): Scaling**
- 15-20 departments receive data governance teams
- Leverage pilot learnings and templates
- Communities of Practice connecting teams across departments
- Shared services (e.g., data infrastructure, training) reducing duplication

**Phase 3 (Months 25-36): Statewide Deployment**
- Complete deployment across all major departments (40-50 total teams)
- Mature operating model and standards
- Self-sustaining communities supporting each other
- Integration with Independent Data Governance Office standards

**Expected Impact:**
- 95%+ data quality for critical datasets (up from 60-70% baseline)
- 80% reduction in data sharing negotiation time (from 18 months to 4-8 weeks)
- 50%+ increase in data-driven decision making (measured by analytics tool usage)
- 300-500 permanent civil service positions created (distributed across departments)
- Sustainable capacity independent of Fellowship program or external consultants

### 7.5 Training Programs

**Digital Accelerators Program:**

**Purpose:** Upskill existing IT staff in modern technologies and methods

**Curriculum:**
- Cloud technologies (AWS, Azure, Google Cloud)
- AI/ML fundamentals and applications
- Agile and DevOps methodologies
- API development and microservices
- Cybersecurity and zero trust
- Data engineering and analytics

**Structure:**
- **Protected learning time:** 20% of work hours dedicated to training
- **Cohort-based learning:** Teams learning together (better retention and application)
- **Hands-on labs:** Real-world scenarios and projects
- **Certification paths:** Industry certifications (AWS Certified, Certified Kubernetes Administrator, etc.)

**Apprenticeship Programs:**
- Junior staff paired with experienced mentors
- Structured learning plans with clear milestones
- Rotation through different technical specialties
- Path to professional certification or advanced roles

**Talent Rotations:**
- 6-12 month rotations across departments or agencies
- Exposure to different technologies and organizational cultures
- Cross-pollination of ideas and best practices
- Building enterprise perspective (similar to Fellowship but for technical staff)

**University Partnerships:**
- Internship programs bringing students into state government
- Capstone projects addressing real government challenges
- Pipeline development (interns becoming full-time employees)
- Research collaborations with universities

**CalAcademy Integration:**

**Purpose:** ODI's CalAcademy provides comprehensive training across innovation methods

**Key Tracks:**
- Human-centered design
- Plain language and communication
- User research methods
- Data literacy and best practices
- Innovation methods and design thinking
- Digital service delivery
- Accessibility and inclusive design

**Requirement for Data Governance Teams:**
- 100% of data governance team members complete foundational tracks within first year
- Annual continuing education requirement (minimum 40 hours/year)
- Specialization tracks for advanced skills

**Target:** 100% of data governance team members trained in foundational competencies by Year 2

**Innovation Ambassadors Network:**

**Purpose:** Peer champions driving cultural change within departments

**Selection:**
- 30-40 per agency (1-2 per major division)
- Nominated by leadership, volunteer interest
- Respected by peers, credible change agents

**Activities:**
- Peer learning sessions (monthly)
- Champions for new tools and practices
- Early adopters providing feedback
- Supporting colleagues through change
- Celebrating innovation and risk-taking

**Support:**
- Quarterly training on change leadership
- Recognition and awards for contributions
- Direct access to E3 leaders for feedback
- Career development opportunities

**Expected Impact:**
- Distributed change leadership (not just top-down)
- Peer influence overcoming resistance
- Faster adoption of innovations
- Culture shift toward continuous improvement

---

*Continued in Part 3: Breakthrough Modernization Fund, Implementation Roadmap*