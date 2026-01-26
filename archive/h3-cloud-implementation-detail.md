# H.3 Cloud Strategy - Implementation Details

*Archived from appendices/08-technical-appendices.md*

For strategic principles, see [Appendix H.3](../appendices/technical-standards.md#h3-cloud-strategy-principles).

---

## Multi-Cloud Strategy Details

Avoid single cloud vendor lock-in through multi-cloud deployment where feasible:
- Critical applications deployed across multiple cloud providers
- Containerized workloads enabling portability
- Infrastructure-as-Code supporting multi-cloud deployment
- Careful analysis of multi-cloud complexity vs. flexibility benefits

## Critical Systems Requiring On-Premises Redundancy

Examples of systems that must maintain on-premises operational capability:

- **Emergency Services:** 911 dispatch, CAL FIRE coordination, emergency management systems, emergency alert systems
- **Law Enforcement:** Criminal justice information systems, arrest and booking systems, warrant management
- **Public Safety:** Prison management systems, probation and parole tracking, sex offender registry
- **Benefits Delivery:** CalFresh, Medi-Cal eligibility, unemployment insurance payments, child support
- **Critical Infrastructure:** Water management systems, power grid coordination, transportation management
- **Financial Systems:** Payroll processing, tax collection, treasury operations, pension management

## Implementation Strategy

- **Primary workloads run in cloud** for scalability, elasticity, and cost efficiency
- **Critical data replicated to on-premises systems** in near-real-time (typically < 5 minute lag)
- **On-premises systems capable of maintaining operations** during internet disruption (degraded capacity acceptable)
- **Regular failover testing** (quarterly minimum) to ensure redundancy effectiveness
- **Automated failback** when cloud connectivity restored, with data reconciliation
- **Clear procedures** for manual intervention if automated failover fails

## Cloud Provider Requirements

- FedRAMP-certified cloud providers (AWS GovCloud, Microsoft Azure Government, Google Cloud Platform)
- FISMA compliance appropriate to data sensitivity (Moderate or High)
- StateRAMP (California-specific requirements including data residency, audit access, breach notification)
- SLA guarantees: 99.9% uptime for production services, 99.99% for critical systems
- Geographic redundancy within California or western United States where possible

## Cloud-Native Architecture

California adopts modern cloud-native patterns to maximize cloud benefits:

- **Containers and Orchestration:** Docker containers managed by Kubernetes enabling portability and scaling
- **Serverless Computing:** AWS Lambda, Azure Functions, or Google Cloud Functions for event-driven workloads
- **Managed Services:** Leverage cloud provider services reducing operational overhead (managed databases, message queues, caching)
- **Infrastructure as Code (IaC):** Terraform or CloudFormation for repeatable, version-controlled infrastructure
- **Automated Backup and Disaster Recovery:** Cloud-native backup with cross-region replication
- **Auto-Scaling:** Automatically adjust capacity based on demand
- **Immutable Infrastructure:** Replace rather than update infrastructure components

## Migration Approach

- **Prioritize high-cost, low-complexity workloads first** (quick wins demonstrating value)
- **Use lift-and-shift for initial migration**, then re-architect for cloud-native over time
- **Implement strong cloud governance:** Cost management, security controls, compliance monitoring, tagging standards
- **Data center consolidation** as workloads migrate, reducing facilities costs
- **Hybrid period of 3-5 years** recognizing gradual transition
