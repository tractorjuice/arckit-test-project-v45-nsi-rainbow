# Architecture Principles

## Document Control

| Field | Value |
|-------|-------|
| Document ID | ARC-000-PRIN-v1.0 |
| Document Type | Architecture Principles |
| Project | Global (All Workstreams) |
| Classification | OFFICIAL |
| Status | DRAFT |
| Version | 1.0 |
| Created Date | 2026-02-13 |
| Last Modified | 2026-02-13 |
| Review Cycle | Quarterly |
| Next Review Date | 2026-05-13 |
| Owner | NS&I Chief Technology Officer |
| Reviewed By | PENDING |
| Approved By | PENDING |
| Distribution | NS&I Digital Programme Board, HM Treasury, Programme Delivery Teams |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-13 | ArcKit | Initial principles definition | PENDING | PENDING |

---

## 1. Purpose

These architecture principles establish the foundational guidelines for the NS&I Digital Modernisation Programme across all three workstreams: Core Banking Migration, Digital Channels & Operations, and Programme Governance & Assurance. They reflect lessons from the programme's challenges and the PAC's recommendations, ensuring future decisions are grounded in sound architectural practice.

## 2. Principles

### P1: Cloud-Native by Default

**Statement**: All new systems and services must be designed as cloud-native from the outset, leveraging managed services, containerisation, and serverless patterns where appropriate.

**Rationale**: NS&I's legacy Atos-hosted on-premises platform has been a constraint on agility and cost control for over 25 years. The migration to SBS SBP Digital Core represents a once-in-a-generation opportunity to adopt modern cloud-native patterns. Designing for cloud-native ensures scalability, resilience, and reduced operational overhead.

**Implications**:
- All new services must be deployable to UK sovereign cloud (AWS UKCloud / Azure UK / GCP europe-west2)
- No new on-premises infrastructure procurement
- Containerised workloads preferred over virtual machines
- Managed database services preferred over self-hosted
- Infrastructure as Code (IaC) mandatory for all environments

### P2: Data Sovereignty and Security First

**Statement**: All customer data must remain within UK borders, processed in UK-based data centres, and protected to standards commensurate with financial services and government requirements.

**Rationale**: NS&I handles financial data for 24 million customers and operates as an executive agency of HM Treasury. Data sovereignty is a legal requirement under UK GDPR and a practical necessity given the OFFICIAL security classification. PCI DSS compliance is mandatory for payment processing.

**Implications**:
- UK-only data residency for all customer and financial data
- Encryption at rest (AES-256) and in transit (TLS 1.3) mandatory
- NCSC CAF compliance for all systems
- PCI DSS certification for payment processing components
- Annual penetration testing and security assessment
- Data classification applied to all data stores and APIs

### P3: Service Continuity Above All

**Statement**: No change to the programme may compromise service to NS&I's 24 million customers. The Premium Bonds prize draw, savings operations, and customer access must be maintained throughout the migration.

**Rationale**: NS&I's customers depend on uninterrupted access to their savings. The PAC report highlighted risks to customers if the programme is unsuccessful. A failed migration could undermine public trust in government-backed savings.

**Implications**:
- Dual-running period: Atos legacy and SBS platforms must coexist
- Phased migration with rollback capability at every stage
- Zero-downtime deployment patterns (blue-green, canary)
- Comprehensive data reconciliation between legacy and new platforms
- Premium Bonds prize draw system requires dedicated migration plan with extended parallel-run
- Customer communication plan for every migration phase

### P4: Realistic Planning and Cost Transparency

**Statement**: All programme plans must be evidence-based, independently validated, and accompanied by transparent cost forecasts with clear assumptions and contingency.

**Rationale**: The PAC found NS&I had "no workable plan after five years" and "no idea of its eventual cost". HM Treasury acknowledged it should have intervened earlier. This principle directly addresses the programme's most critical governance failure.

**Implications**:
- All cost estimates must include contingency (minimum 20% for novel elements, 10% for established)
- Independent cost assurance at each programme gate
- Monthly cost reporting to HM Treasury with variance analysis
- No new work packages approved without approved budget envelope
- Earned Value Management (EVM) for all major deliverables
- Quarterly IPA delivery confidence assessments

### P5: Skills and Capability Ownership

**Statement**: NS&I must develop and retain sufficient in-house technical capability to act as an intelligent client, make informed technology decisions, and hold delivery partners to account.

**Rationale**: The PAC found NS&I "lacked the skills to deliver" the programme and was "vague on how it holds consultants to account" despite spending £43m on external consultancy. Over-reliance on third parties without internal expertise creates an accountability vacuum.

**Implications**:
- Minimum 30% of programme roles filled by NS&I permanent staff
- Technology leadership positions (CTO, Chief Architect, Head of Engineering) must be permanent NS&I employees
- Knowledge transfer requirements in all consultancy contracts with measurable outcomes
- Internal architecture review board with authority to approve or reject designs
- Mandatory skills assessment and development plan for all programme staff
- Consultant contracts must include defined deliverables, not just time-and-materials

### P6: Modular and Loosely Coupled Architecture

**Statement**: Systems must be composed of independently deployable, loosely coupled modules communicating through well-defined APIs and event-driven interfaces.

**Rationale**: NS&I's monolithic legacy platform creates tight coupling that makes change risky, slow, and expensive. The move to SBS SBP Digital Core must not recreate monolithic dependencies. Modularity enables incremental delivery, independent scaling, and reduced blast radius of failures.

**Implications**:
- API-first design for all inter-system communication
- Event-driven architecture for asynchronous workflows
- Each module must be independently deployable and testable
- No direct database sharing between modules
- API versioning and backwards compatibility policy
- Circuit breaker and bulkhead patterns for resilience

### P7: Vendor Independence and Interoperability

**Statement**: Architecture decisions must avoid unnecessary lock-in to any single vendor, platform, or technology. Interfaces must use open standards where available.

**Rationale**: NS&I's 25-year single-vendor dependency on Atos demonstrated the risks of excessive lock-in. While the SBS partnership is strategic, the architecture must ensure that individual components can be replaced or augmented without re-platforming the entire estate.

**Implications**:
- Open standards preferred (REST, OpenAPI, OAuth 2.0, OIDC, CloudEvents)
- Data stored in portable formats with documented schemas
- Abstraction layers at key integration points
- Multi-cloud capability where practical (primary + DR)
- Contractual data portability clauses with all vendors
- Regular assessment of vendor dependency risk

### P8: Observable and Auditable by Design

**Statement**: All systems must be instrumented for observability (metrics, logs, traces) and provide a complete audit trail of all state-changing operations.

**Rationale**: The PAC found a "good news culture" where problems were not surfaced. Technical observability is the architectural counterpart to cultural transparency. Financial services regulation and government accountability require comprehensive audit trails.

**Implications**:
- Centralised logging and monitoring platform
- Distributed tracing across all microservices
- Real-time dashboards for programme and service health
- Immutable audit logs for all financial transactions
- Alerting thresholds aligned with SLAs
- Quarterly observability reviews

### P9: Incremental Delivery with Measurable Value

**Statement**: The programme must deliver value incrementally through small, measurable releases rather than large, high-risk big-bang deployments.

**Rationale**: The programme's history of over-confidence and delayed delivery demonstrates the risks of large-scale waterfall approaches. Incremental delivery reduces risk, provides earlier feedback, and enables course correction.

**Implications**:
- Maximum 3-month delivery cycles for all workstreams
- Each release must deliver measurable business value (not just technical capability)
- Feature flags for controlled rollout
- A/B testing capability for customer-facing changes
- Regular retrospectives with actionable outcomes
- Stop/pivot decisions at each increment boundary

### P10: Compliance as Code

**Statement**: Regulatory and policy compliance requirements must be codified, automated, and continuously validated rather than manually assessed.

**Rationale**: NS&I operates under multiple overlapping regulatory frameworks (FCA, PRA, PCI DSS, NCSC CAF, GDS, TCoP). Manual compliance checking is slow, error-prone, and doesn't scale. Automating compliance reduces risk and accelerates delivery.

**Implications**:
- Policy-as-code for infrastructure compliance (e.g., Open Policy Agent, AWS Config Rules)
- Automated security scanning in CI/CD pipelines
- Compliance dashboards with real-time status
- Automated PCI DSS evidence collection
- GDS Service Standard assessment integrated into delivery process
- TCoP alignment validated at architecture review gates

---

## 3. Principle Dependencies

```
P1 (Cloud-Native) ──→ P2 (Data Sovereignty) ──→ P3 (Service Continuity)
       │                                                    │
       ▼                                                    ▼
P6 (Modular) ──────→ P7 (Vendor Independence) ──→ P9 (Incremental Delivery)
       │                                                    │
       ▼                                                    ▼
P8 (Observable) ───→ P10 (Compliance as Code) ──→ P4 (Cost Transparency)
                                                            │
                                                            ▼
                                                   P5 (Skills Ownership)
```

## 4. Application

These principles apply to all three programme workstreams:
- **001 Core Banking Migration**: P1, P2, P3, P6, P7 are primary drivers
- **002 Digital Channels**: P1, P3, P6, P8, P9 are primary drivers
- **003 Programme Governance**: P4, P5, P8, P9, P10 are primary drivers

All principles apply across all workstreams; the above highlights where each principle has the greatest impact.

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-02-13
**ArcKit Version**: 2.4.4
**Project**: NS&I Digital Modernisation Programme (Global)
**Model**: Claude Opus 4.6
