# Project Requirements: NS&I Core Banking Migration

> **Template Status**: Live | **Version**: 2.4.4 | **Command**: `/arckit:requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.1 |
| **Document Type** | Business and Technical Requirements |
| **Project** | NS&I Core Banking Migration (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2026-02-13 |
| **Last Modified** | 2026-02-13 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-03-15 |
| **Owner** | NS&I Programme Director, Core Banking |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NS&I Digital Programme Board, HM Treasury Sponsor Team, SBS Delivery Lead, Atos Transition Lead, IPA Review Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-13 | ArcKit AI | Initial creation from `/arckit:requirements` command | PENDING | PENDING |
| 1.1 | 2026-02-13 | ArcKit AI | Updated with PAC report (13 Feb 2026) findings: timeline assumption revised (PAC recommends stop targeting March 2028), Atos contract extension details (£474M without competitive bidding), procurement failure history, PAC-specific recommendations | PENDING | PENDING |

## Document Purpose

This document defines the complete business, functional, non-functional, integration, and data requirements for the NS&I Core Banking Migration — the replacement of the Atos legacy core banking platform with SBS SBP Digital Core. Requirements are traceable to stakeholder drivers (ARC-001-STKE-v1.0) and architecture principles (ARC-000-PRIN-v1.0). This document serves as the contractual requirements baseline for SBS delivery, the acceptance criteria framework for programme gates, and the foundation for vendor evaluation, design reviews, and test planning.

### Source Documents

| Document | ID | Status | Key Extractions |
|----------|----|--------|-----------------|
| Stakeholder Drivers & Goals | ARC-001-STKE-v1.0 | DRAFT | 15 drivers, 8 goals, 5 outcomes, 4 conflicts, RACI matrix |
| Architecture Principles | ARC-000-PRIN-v1.0 | DRAFT | 10 principles (P1–P10), constraints, technology standards |
| Risk Register | Not yet created | — | Recommend running `/arckit:risk` |
| Strategic Outline Business Case | Not yet created | — | Recommend running `/arckit:sobc` |

---

## Executive Summary

### Business Context
NS&I (National Savings and Investments) is the UK's state-owned savings bank, serving 24 million customers with over £230 billion in savings products. The core banking platform has been outsourced to Atos since 1999 — a 27-year single-vendor dependency on an ageing, monolithic, on-premises system. The Public Accounts Committee described the modernisation programme as a "full-spectrum disaster" in February 2026, finding that NS&I had no workable plan, no idea of eventual cost, and lacked the skills to deliver.

The Core Banking Migration workstream replaces the Atos legacy platform with SBS (Sopra Banking Software) SBP Digital Core — a cloud-native banking engine. This is classified as "extremely high-risk" by the PAC. The migration must move 24 million customer accounts and £230 billion in assets from one platform to another with zero service disruption, while rebuilding NS&I's internal capability and restoring confidence with Treasury, Parliament, and the public.

### Objectives
- **O1**: Replace the Atos legacy core banking engine with SBS SBP Digital Core (target date under review — PAC recommended NS&I stop targeting March 2028 and develop a realistic bottom-up plan; addresses Goal G-4)
- **O2**: Migrate all 24 million customer accounts with zero data loss and zero service disruption (addresses Goal G-2)
- **O3**: Achieve full regulatory compliance (NCSC CAF, PCI DSS, UK GDPR, FCA, PRA) for the new platform before customer migration (addresses Goal G-7)
- **O4**: Establish a credible, independently validated cost baseline with monthly EVM reporting (addresses Goal G-1)
- **O5**: Build NS&I in-house technical capability to 30% of programme roles by end of 2026 (addresses Goal G-3)

### Expected Outcomes
- **Outcome O-1**: Restored financial credibility — monthly cost variance <5%, NAO confirms reporting adequacy
- **Outcome O-2**: Seamless customer migration — zero P1/P2 incidents, 99.95% uptime maintained, zero data loss
- **Outcome O-3**: Capable and accountable organisation — 50% permanent staff by end of 2027, £15M annual consultant savings
- **Outcome O-4**: Secure and compliant platform — full accreditation across NCSC CAF, PCI DSS, UK GDPR, FCA, PRA
- **Outcome O-5**: Managed vendor transition — complete Atos exit within 12 months of SBS go-live, zero contractual disputes

### Project Scope

**In Scope**:
- SBS SBP Digital Core platform integration, configuration, and deployment on UK sovereign cloud
- Migration of all NS&I savings products to SBS platform (Premium Bonds, Income Bonds, Direct Saver, Investment Account, etc.)
- Data migration of 24 million customer accounts and full transaction history from Atos
- Dual-running period with automated data reconciliation between Atos and SBS platforms
- Managed Atos exit including knowledge transfer and contractual close-out
- Integration with existing payment rails (BACS, Faster Payments, CHAPS), HMRC, and identity verification services
- Premium Bonds prize draw system migration with dedicated parallel-run
- Regulatory accreditation (NCSC CAF, PCI DSS, UK GDPR) for SBS environment
- Observability, audit, and compliance automation for the new platform
- Operational readiness including runbooks, monitoring, and incident management

**Out of Scope**:
- Customer-facing digital channel redesign (covered by Project 002 — Digital Channels & Operations)
- Back-office workflow modernisation (covered by Project 002)
- Programme governance framework and cost control mechanisms (covered by Project 003 — Programme Governance & Assurance)
- NS&I product redesign or new product development (future initiative)
- Third-party vendor selection for ancillary services (covered by separate procurement)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level | Primary Driver (from STKE) |
|-------------|------|--------------|-------------------|---------------------------|
| NS&I Chief Executive | Programme Sponsor | NS&I | Decision maker | SD-3: Delivery and reputation |
| NS&I CTO | Technology Direction | NS&I | Architecture authority | SD-4: Technical excellence |
| NS&I CFO | Financial Oversight | NS&I | Budget approval | SD-7: Budget control |
| Programme Director | Delivery Lead | NS&I | Day-to-day delivery | Multiple |
| NS&I Chief Architect | Design Authority | NS&I | Architecture review | SD-14: Architectural integrity |
| NS&I CISO | Security Approval | NS&I | Security gate owner | SD-6: Security posture |
| NS&I Operations Director | Service Continuity | NS&I | Cutover authority | SD-5: Service continuity |
| NS&I DPO | Data Protection | NS&I | DPIA approval | SD-6 (related) |
| HM Treasury Sponsor | Funding & Oversight | HM Treasury | Quarterly review | SD-1: Cost control and VfM |
| PAC / NAO | Parliamentary Scrutiny | Parliament | Evidence sessions | SD-2: Accountability |
| Atos Transition Lead | Legacy Exit | Atos | Exit planning | SD-8: Managed exit |
| SBS Delivery Lead | Platform Delivery | SBS | Platform delivery | SD-9: Successful deployment |
| NS&I Customers (24M) | End Users | Public | Service recipients | SD-10: Uninterrupted service |
| FCA / PRA | Regulatory Oversight | Regulators | Compliance review | SD-12: Regulatory compliance |
| NCSC | Cyber Security Standards | GCHQ | Security assessment | SD-6 (related) |

---

## Business Requirements

### BR-1: Establish Validated Programme Cost Baseline

**Description**: The programme must establish an independently validated, comprehensive cost baseline for the entire core banking migration within 90 days of programme reset, covering all work packages with explicit assumptions and minimum 20% contingency for novel elements.

**Rationale**: The PAC found NS&I had "no idea of the eventual cost" (SD-2). HM Treasury requires transparent cost forecasting as a condition of the additional £109M funding (SD-1). Without a credible cost baseline, programme decisions cannot be made on an informed basis. Addresses Goal G-1 and Outcome O-1. Aligns with Principle P4 (Realistic Planning and Cost Transparency).

**Success Criteria**:
- Independent cost assurance validation completed within 90 days
- 100% of work packages have allocated budget envelopes with documented assumptions
- Cost baseline reviewed and accepted by HM Treasury sponsor
- Contingency allocations: minimum 20% for novel elements, 10% for established elements

**Priority**: MUST_HAVE

**Stakeholder**: NS&I CFO (Accountable), HM Treasury (Approver)

---

### BR-2: Zero Customer Service Disruption During Migration

**Description**: The migration must maintain uninterrupted service to NS&I's 24 million customers throughout all phases — parallel-run, data migration, cutover, and post-migration stabilisation — with zero P1 or P2 customer-impacting incidents attributable to migration activities.

**Rationale**: NS&I customers depend on continuous access to their savings (SD-10). Any disruption would be national news, damage public trust in government-backed savings, trigger regulatory intervention (SD-12), and provide further ammunition for parliamentary criticism (SD-2). Addresses Goal G-2 and Outcome O-2. Aligns with Principle P3 (Service Continuity Above All).

**Success Criteria**:
- 99.95% uptime maintained for all customer-facing services during migration period
- Zero P1/P2 incidents attributable to migration activities
- Premium Bonds monthly prize draw executed successfully every month without exception
- Customer complaint volumes remain within ±10% of pre-migration baseline
- Zero data integrity errors in migrated customer accounts

**Priority**: MUST_HAVE

**Stakeholder**: NS&I Operations Director (Accountable), NS&I CEO (Escalation)

---

### BR-3: Achieve Full Regulatory Compliance for New Platform

**Description**: The SBS SBP Digital Core platform must achieve full regulatory accreditation across all applicable frameworks (NCSC CAF, PCI DSS, UK GDPR, FCA requirements, PRA SS1/21) before any customer data is migrated to the new platform.

**Rationale**: NS&I operates under multiple overlapping regulatory regimes as both a financial institution and a government agency (SD-6, SD-12). Customer data and financial transactions cannot be processed on the new platform until it meets all standards. Addresses Goal G-7 and Outcome O-4. Aligns with Principles P2 (Data Sovereignty) and P10 (Compliance as Code).

**Success Criteria**:
- NCSC CAF self-assessment: all applicable outcomes at "Achieved" level
- PCI DSS v4.0 certification achieved for SBS cardholder data environment
- DPIA completed and approved before customer data migration
- Zero critical or high security findings unresolved at time of customer migration
- FCA notification submitted and acknowledged for material technology change
- PRA operational resilience self-assessment updated for SBS platform

**Priority**: MUST_HAVE

**Stakeholder**: NS&I CISO (Accountable), DPO (GDPR), FCA/PRA (Regulators)

---

### BR-4: Build NS&I In-House Technical Capability

**Description**: NS&I must achieve a minimum of 30% permanent staff in core programme roles by end of 2026, rising to 50% by end of 2027, with all technology leadership positions filled by NS&I permanent employees.

**Rationale**: The PAC found NS&I "lacked the skills" to deliver (SD-2) and was dependent on £43M of consultants without accountability (SD-15). Architecture Principle P5 (Skills and Capability Ownership) mandates internal capability. Addresses Goal G-3 and Outcome O-3.

**Success Criteria**:
- 30% permanent staff ratio by December 2026
- 50% permanent staff ratio by December 2027
- CTO, Chief Architect, Head of Engineering, Head of Security all filled as permanent NS&I employees
- Knowledge transfer score: 80% of critical domains documented and transferable
- Annual retention rate for permanent technical hires: ≥85%

**Priority**: MUST_HAVE

**Stakeholder**: NS&I CTO (Accountable), HR Director (Delivery), PAC (Scrutiny)

---

### BR-5: Complete Managed Atos Exit with Full Knowledge Transfer

**Description**: Execute the contractual exit from Atos including complete knowledge transfer, documented legacy system behaviours, and verified data extraction, with Atos service levels maintained at contractual SLA throughout the transition and exit completed within 12 months of SBS go-live.

**Rationale**: The Atos relationship spans 27 years with deep institutional knowledge (SD-8). The original contract (awarded 2014, due to expire 2021) has been extended twice without competitive bidding at an additional value of £474.4M (NAO, November 2025), with the extension to March 2028 estimated at £530M to cover unfilled successor contracts. Of five planned successor contracts, one failed and was re-run, one was awarded then terminated, and one was abandoned (NAO). A poorly managed exit risks service disruption (SD-5), knowledge loss, and contractual disputes. In 2025, 750 customer service agents and 350 back-office staff were transferred to a new supplier, but core banking operations remain with Atos. Addresses Goal G-5 and Outcome O-5. Aligns with Principle P7 (Vendor Independence).

**Success Criteria**:
- 100% of critical legacy systems documented (system behaviours, data flows, configuration)
- Atos SLA compliance maintained at 100% throughout transition
- All customer data extracted and migrated with verified integrity (zero data loss)
- Exit costs within agreed contractual envelope (±10%)
- Zero unresolved contractual disputes at exit completion
- Exit completed within 12 months of SBS production go-live

**Priority**: MUST_HAVE

**Stakeholder**: Programme Director (Accountable), NS&I CEO (Escalation), Atos (Delivery partner)

---

### BR-6: Deliver SBS Platform (Timeline Under Review)

**Description**: Complete SBS SBP Digital Core integration, configuration, and testing to achieve full functional, performance, and security accreditation, with all NS&I savings products operational on the new platform. **Note**: The PAC (13 Feb 2026) explicitly recommended NS&I stop targeting March 2028 and instead develop a realistic bottom-up integrated plan — the go-live date is therefore under review pending NS&I's response to PAC recommendations.

**Rationale**: The SBS platform is the technical foundation for the entire modernisation (SD-4, SD-9). The PAC noted "main work has yet to start" on core banking replacement. The PAC Chair warned the "taxpayer is at serious risk of throwing good money after bad" and that any plan must be built from the ground up rather than reverse-engineered around optimistic dates. The Bank of England's RTGS system replacement (£431M, delivered on schedule) was cited as an unfavourable benchmark. Addresses Goal G-4 and Outcome O-2. Aligns with Principle P1 (Cloud-Native by Default).

**Success Criteria**:
- SBS platform achieves "Ready for Live" accreditation (functional, performance, security) — target date to be confirmed via bottom-up integrated plan per PAC recommendation
- 100% of NS&I savings products configured, tested, and operational on SBS
- Performance testing confirms platform handles 150% of peak load (Premium Bonds draw day)
- API-first integration architecture with zero direct database dependencies between modules
- All NS&I product calculations validated against Atos outputs with zero discrepancies

**Priority**: MUST_HAVE

**Stakeholder**: NS&I CTO (Accountable), SBS (Delivery), Programme Director (Milestone owner)

---

### BR-7: Implement Transparent Governance and Reporting

**Description**: Implement monthly Earned Value Management (EVM) reporting, respond to all PAC recommendations within 60 days, and achieve a minimum AMBER IPA delivery confidence rating within 12 months.

**Rationale**: The PAC found a "good news culture" preventing honest reporting (SD-2). HM Treasury requires transparency as condition of continued funding (SD-1). The NAO needs auditable evidence (SD-11). Addresses Goal G-6 and Outcome O-1. Aligns with Principle P4 (Realistic Planning and Cost Transparency).

**Success Criteria**:
- Monthly EVM reports delivered to Treasury with <5% cost variance
- 100% of PAC recommendations responded to within 60 days
- IPA delivery confidence improved from RED to AMBER within 12 months
- NAO confirms governance framework adequacy
- Zero instances of risk suppression identified by audit

**Priority**: MUST_HAVE

**Stakeholder**: NS&I CEO (Accountable), HM Treasury (Reviewer), PAC/NAO (Scrutiny)

---

### BR-8: Transition Consultants to Outcome-Based Contracts

**Description**: Transition 100% of consultant engagements from time-and-materials to outcome-based contracts within 6 months, reducing total consultant spend by 25% by end of 2027.

**Rationale**: The PAC criticised the £43M consultant spend with NS&I "vague on how it holds them to account" (SD-2, SD-15). Outcome-based contracts provide measurable accountability. Addresses Goal G-8 and Outcome O-3.

**Success Criteria**:
- 100% of consultant engagements on outcome-based contracts within 6 months
- 25% reduction in total consultant spend by end of 2027
- All contracts include measurable knowledge transfer requirements
- Quarterly VfM review confirming consultant contribution
- Zero consultant engagements exceeding 12 months without recompetition

**Priority**: SHOULD_HAVE

**Stakeholder**: NS&I CFO (Accountable), Programme Director (Delivery)

---

## Functional Requirements

### User Personas

#### Persona 1: NS&I Platform Operations Engineer
- **Role**: Monitors and operates the core banking platform (SBS and Atos during dual-run)
- **Goals**: Maintain service stability, detect and resolve incidents quickly, perform scheduled maintenance without customer impact
- **Pain Points**: Legacy system fragility, undocumented Atos behaviours, manual monitoring processes, lack of modern observability tooling
- **Technical Proficiency**: High

#### Persona 2: NS&I Product Manager (Savings Products)
- **Role**: Defines product parameters for savings products (interest rates, terms, eligibility rules)
- **Goals**: Configure products quickly, launch rate changes same-day, verify product calculations
- **Pain Points**: Legacy product configuration requires Atos involvement, long lead times for changes, limited self-service
- **Technical Proficiency**: Medium

#### Persona 3: NS&I Finance & Reconciliation Analyst
- **Role**: Reconciles financial data between systems, validates transaction processing, produces regulatory reports
- **Goals**: Automated reconciliation, real-time balance visibility, audit-ready reports
- **Pain Points**: Manual reconciliation processes, data discrepancies between systems, end-of-day batch delays
- **Technical Proficiency**: Medium

#### Persona 4: NS&I Data Migration Engineer
- **Role**: Plans, executes, and validates data migration from Atos to SBS
- **Goals**: Migrate all data accurately, verify integrity at record level, maintain rollback capability
- **Pain Points**: Undocumented legacy data structures, data quality issues in source system, scale (24M accounts)
- **Technical Proficiency**: High

#### Persona 5: Regulatory Compliance Officer
- **Role**: Ensures platform meets FCA, PRA, NCSC, and PCI DSS requirements
- **Goals**: Continuous compliance visibility, automated evidence collection, audit-ready documentation
- **Pain Points**: Manual compliance checks, siloed evidence, regulatory framework complexity
- **Technical Proficiency**: Low–Medium

---

### Use Cases

#### UC-1: Product Configuration Change

**Actor**: NS&I Product Manager

**Preconditions**:
- User authenticated and authorised for product configuration role
- Product exists in SBS product catalogue
- Change request approved through internal governance

**Main Flow**:
1. Product Manager selects savings product from catalogue
2. System displays current product parameters (interest rate, terms, eligibility, limits)
3. Product Manager modifies parameters (e.g., interest rate change from 4.00% to 4.25%)
4. System validates changes against business rules and regulatory limits
5. System shows impact preview (affected accounts count, projected interest cost change)
6. Product Manager submits change for approval
7. Approver reviews and approves
8. System applies change effective from specified date
9. System generates audit trail entry with full before/after detail

**Postconditions**:
- Product parameters updated in SBS
- All affected account calculations reflect new parameters from effective date
- Audit trail records the change, approver, and timestamp

**Alternative Flows**:
- **Alt 5a**: If validation fails (e.g., rate exceeds regulatory limit), system displays specific error and prevents submission
- **Alt 7a**: If approver rejects, change remains pending with rejection reason; Product Manager notified

**Priority**: HIGH

---

#### UC-2: Automated Data Reconciliation (Dual-Run)

**Actor**: NS&I Finance & Reconciliation Analyst (automated with manual oversight)

**Preconditions**:
- Both Atos and SBS platforms operational with synchronised data
- Reconciliation engine configured with matching rules and tolerances

**Main Flow**:
1. System triggers end-of-day reconciliation run (also available on-demand)
2. System extracts account balances, transaction summaries, and product positions from both platforms
3. System performs record-by-record comparison across all 24 million accounts
4. System identifies matched records, mismatched records, and missing records
5. System generates reconciliation report with categorised discrepancies
6. For discrepancies within tolerance, system auto-classifies as "timing differences"
7. For discrepancies outside tolerance, system raises alerts to Reconciliation Analyst
8. Analyst investigates, classifies, and resolves or escalates each discrepancy
9. System maintains reconciliation history for audit

**Postconditions**:
- Reconciliation report available with match rate, discrepancy count, and resolution status
- All out-of-tolerance discrepancies tracked to resolution
- Audit trail of all reconciliation runs and resolutions

**Exception Flows**:
- **Ex 1**: If reconciliation engine fails mid-run, system alerts operations and provides partial results with clear indication of incomplete scope

**Priority**: CRITICAL

---

#### UC-3: Customer Account Migration (Phased)

**Actor**: NS&I Data Migration Engineer (automated with manual oversight)

**Preconditions**:
- Product migration completed and validated for target product type
- SBS platform accredited for the product type being migrated
- Parallel-run reconciliation showing >99.9999% match rate for the product
- Cutover rehearsal for this product type completed successfully
- Rollback procedure tested and validated

**Main Flow**:
1. Migration Engineer initiates migration batch for approved customer cohort
2. System extracts customer data from Atos (accounts, balances, transaction history, standing orders, nominated accounts)
3. System transforms data to SBS schema (applying documented transformation rules)
4. System loads data into SBS platform
5. System performs record-level verification (count, balances, checksums)
6. System generates migration validation report
7. If validation passes, system activates customer accounts on SBS
8. System redirects transaction processing for migrated accounts to SBS
9. System disables migrated accounts on Atos (read-only archive mode)
10. System confirms migration completion and updates migration tracker

**Postconditions**:
- Customer accounts active and operational on SBS
- All historical data preserved and accessible
- Atos accounts in read-only archive mode
- Reconciliation confirms zero data discrepancies post-migration

**Alternative Flows**:
- **Alt 5a**: If verification fails (balance mismatch, missing records), system halts migration for the failed cohort and alerts Migration Engineer
- **Alt 5b**: If rollback is triggered, system reverts to Atos as primary and deactivates SBS accounts for the cohort

**Priority**: CRITICAL

---

### Functional Requirements Detail

#### FR-1: Core Banking Engine — Account Management

**Description**: The SBS platform must support full lifecycle management of all NS&I customer accounts including creation, maintenance, closure, and dormancy processing for all current product types.

**Relates To**: BR-6, UC-1, UC-3

**Acceptance Criteria**:
- [ ] Given a new customer application, when all KYC checks pass, then the system creates a new account with unique identifier, linked customer record, and nominated bank account within 5 seconds
- [ ] Given an existing account, when a customer requests closure, then the system calculates final balance including accrued interest, processes payout to nominated account, and archives the account record
- [ ] Given an account dormant for >15 years, then the system flags for dormancy review per NS&I dormancy policy and blocks further transactions pending review

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-2 (Product Engine), INT-1 (Atos data migration)

---

#### FR-2: Core Banking Engine — Product Engine

**Description**: The SBS platform must support configuration and calculation for all NS&I savings products: Premium Bonds, Income Bonds, Direct Saver, Investment Account, Junior ISA, Direct ISA, Green Savings Bonds, Guaranteed Growth Bonds, and Guaranteed Income Bonds (plus any products active at migration time).

**Relates To**: BR-6, UC-1

**Acceptance Criteria**:
- [ ] Given each NS&I product type, when configured in SBS, then interest/prize calculations match Atos legacy calculations to the penny for a test cohort of 100,000 accounts per product
- [ ] Given a product parameter change (e.g., interest rate), when applied by an authorised Product Manager, then the change takes effect from the specified date and all affected account calculations reflect the new parameters
- [ ] Given the Premium Bonds product, when the monthly prize draw is executed, then the prize allocation algorithm produces results statistically consistent with published odds and the draw completes within the allocated processing window

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-1 (Account Management)

**Assumptions**: SBS SBP Digital Core can be configured for NS&I's product types; fit-gap analysis to confirm before detailed design

---

#### FR-3: Premium Bonds Prize Draw System

**Description**: The SBS platform must execute the monthly Premium Bonds prize draw for all eligible bonds, applying the published prize fund rate and odds, producing auditable and verifiable results, and distributing prizes to winners.

**Relates To**: BR-2, BR-6

**Acceptance Criteria**:
- [ ] Given all eligible Premium Bonds (~£230 billion nominal value), when the monthly draw executes, then every eligible bond has an equal chance of winning and the prize distribution matches the published prize fund rate (±0.01%)
- [ ] Given the draw results, when validated by the independent draw auditor, then the auditor certifies the draw as fair and correctly executed
- [ ] Given the draw results, when prizes are distributed, then all prizes are credited to winners' accounts or payment method within 5 business days
- [ ] Given a system failure during draw processing, when the failure is detected, then the draw can be restarted from a known checkpoint without double-counting or omitting any bonds

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-1, FR-2, NFR-P-2 (throughput for draw-day volumes)

---

#### FR-4: Transaction Processing Engine

**Description**: The SBS platform must process all financial transactions including deposits, withdrawals, interest payments, prize distributions, standing orders, and inter-account transfers with guaranteed ACID properties and full audit trails.

**Relates To**: BR-2, BR-6

**Acceptance Criteria**:
- [ ] Given a customer deposit instruction, when received via any channel (BACS, Faster Payments, debit card, cheque), then the deposit is credited to the correct account with correct value date within the applicable payment scheme timescales
- [ ] Given a withdrawal request, when validated against account balance and product terms, then the withdrawal is processed to the nominated bank account within 3 business days (or as per product terms)
- [ ] Given an interest calculation date, when interest is calculated for all applicable accounts, then interest is credited with penny-accurate precision matching the published rates and compounding rules
- [ ] Given any transaction, when processed, then an immutable audit record is created containing: transaction ID, timestamp, account, amount, type, user/system initiator, and before/after balances

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-1, INT-2 (Payment rails), INT-3 (Card processors)

---

#### FR-5: Regulatory Reporting Engine

**Description**: The SBS platform must generate all mandatory regulatory reports including HMRC tax reporting (R85 exemptions, annual interest certificates), FCA reporting, PRA operational resilience reports, and Bank of England statistical returns.

**Relates To**: BR-3, NFR-C-3

**Acceptance Criteria**:
- [ ] Given the end of the tax year, when annual interest certificate generation is triggered, then the system produces accurate certificates for all accounts with interest earned, in the format required by HMRC
- [ ] Given an FCA data request, when the compliance team initiates the report, then the system produces the requested data within 5 business days in the required format
- [ ] Given each reporting obligation, when the scheduled report date arrives, then the system auto-generates the report and alerts the compliance team for review before submission

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-1, FR-4, DR-6 (Transaction history retention)

---

#### FR-6: Customer Notification Service

**Description**: The system must send notifications to customers for material account events including balance changes, interest payments, prize wins, product changes, rate changes, and regulatory communications, via their preferred channel (email, post, SMS).

**Relates To**: BR-2, SD-10

**Acceptance Criteria**:
- [ ] Given a Premium Bonds prize win, when the draw results are finalised, then the winner is notified via their preferred channel within 2 business days of the draw
- [ ] Given an interest rate change, when the change is published, then all affected customers are notified at least 14 days before the effective date (or as per product terms)
- [ ] Given a customer's communication preferences, when a notification is generated, then the system uses the preferred channel and maintains delivery confirmation records

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-1, INT-5 (GOV.UK Notify)

---

#### FR-7: Data Migration Tooling

**Description**: The programme must implement automated data migration tooling capable of extracting all customer data from the Atos legacy platform, transforming it to SBS schema, loading it into SBS, and performing record-level verification with automated reconciliation.

**Relates To**: BR-5, UC-3

**Acceptance Criteria**:
- [ ] Given the full Atos customer dataset (24 million accounts), when a migration run is executed, then all records are extracted, transformed, and loaded with zero data loss
- [ ] Given a migrated cohort, when post-migration verification runs, then 100% of records match on: account balance, customer details, product parameters, standing orders, and transaction history checksums
- [ ] Given a migration failure for any cohort, when rollback is triggered, then the affected accounts revert to Atos as primary within 30 minutes with no customer impact
- [ ] Given the migration tooling, when run against a test dataset of 1 million accounts, then the migration completes within 4 hours (enabling overnight production windows)

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: INT-1 (Atos data access), DR-3 (Data transformation rules)

---

#### FR-8: Dual-Run Reconciliation Engine

**Description**: During the parallel-run period, the system must continuously reconcile data between Atos and SBS platforms, comparing all account balances, transaction states, and product positions, with automated alerting for discrepancies.

**Relates To**: BR-2, UC-2

**Acceptance Criteria**:
- [ ] Given both platforms are operational, when the daily reconciliation runs, then all 24 million accounts are compared within the overnight processing window (maximum 6 hours)
- [ ] Given a discrepancy outside tolerance (>£0.01 per account), when detected, then the system raises an alert to the reconciliation team within 15 minutes
- [ ] Given the reconciliation results, when reviewed, then the match rate is reported as a percentage with drill-down capability to individual account level
- [ ] Given a target match rate of 99.9999% before customer migration, when the target is reached for a product type, then the product is flagged as eligible for migration

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-7 (Migration tooling), INT-1 (Atos data feeds)

---

#### FR-9: Audit Trail and Compliance Dashboard

**Description**: The SBS platform must maintain immutable audit trails for all state-changing operations and provide a real-time compliance dashboard showing status across all regulatory frameworks.

**Relates To**: BR-3, BR-7, NFR-C-2

**Acceptance Criteria**:
- [ ] Given any state-changing operation (transaction, configuration change, user access, system change), when completed, then an immutable audit record is written containing who, what, when, where, why, and result
- [ ] Given the compliance dashboard, when accessed by an authorised user, then it displays real-time status for: NCSC CAF outcomes, PCI DSS controls, UK GDPR obligations, and FCA/PRA requirements
- [ ] Given an audit query for a specific customer or transaction, when executed, then the system returns a complete chronological audit trail within 30 seconds

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: NFR-C-2 (Audit logging), NFR-M-1 (Observability)

---

#### FR-10: Atos Knowledge Capture System

**Description**: The programme must implement a structured knowledge capture system to document all legacy system behaviours, operational procedures, undocumented configurations, and institutional knowledge held by Atos personnel, in a searchable and version-controlled repository.

**Relates To**: BR-5, SD-8

**Acceptance Criteria**:
- [ ] Given a legacy system component, when knowledge capture is conducted, then the documentation covers: system behaviour, data flows, configuration parameters, known defects, workarounds, and operational procedures
- [ ] Given the knowledge repository, when queried by NS&I staff, then relevant documentation is returned with version history and source attribution
- [ ] Given the knowledge transfer programme, when assessed at quarterly milestones, then coverage of critical system domains is ≥80% by programme end

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: BR-5 (Atos exit), Atos personnel availability

---

#### FR-11: Cutover Orchestration and Rollback

**Description**: The system must provide automated cutover orchestration for each migration phase, with tested rollback capability that can revert to the Atos platform within 30 minutes if cutover fails.

**Relates To**: BR-2, UC-3

**Acceptance Criteria**:
- [ ] Given a cutover plan for a product cohort, when cutover is initiated, then the system executes all migration steps in defined sequence with checkpoint verification at each step
- [ ] Given a cutover failure at any checkpoint, when rollback is triggered, then all affected accounts are reverted to Atos as primary within 30 minutes with zero data loss
- [ ] Given the cutover process, when rehearsed in a production-like environment, then the rehearsal completes successfully at least 3 times before live cutover is approved

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-7, FR-8, NFR-A-2 (Disaster recovery)

---

#### FR-12: Product Calculation Validation Engine

**Description**: The system must provide an automated validation engine that compares SBS product calculations (interest, prizes, fees, penalties) against Atos legacy calculations for a representative sample, confirming penny-level accuracy before migration.

**Relates To**: BR-6, FR-2

**Acceptance Criteria**:
- [ ] Given a test cohort of 100,000 accounts per product type, when SBS and Atos calculations are compared, then 100% of accounts show identical results (to the penny)
- [ ] Given a new product configuration, when validation is run, then discrepancies are identified, classified, and root-caused before the configuration is approved for production
- [ ] Given historical interest payments (last 7 years), when recalculated by SBS, then results match Atos historical records for a random sample of 10,000 accounts per product

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-2, INT-1

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: API Response Time

**Requirement**: All SBS platform APIs must meet the following response time targets under normal load:
- Account enquiry: <200ms (95th percentile)
- Transaction processing: <500ms (95th percentile)
- Product configuration query: <100ms (95th percentile)
- Reporting queries (standard): <5 seconds (95th percentile)
- Reporting queries (complex/ad hoc): <30 seconds (95th percentile)

**Measurement Method**: Application Performance Monitoring (APM) tooling with continuous measurement in production. Aligns with Principle P8 (Observable and Auditable by Design).

**Load Conditions**:
- Normal load: 5,000 concurrent API sessions
- Peak load (Premium Bonds draw day): 50,000 concurrent sessions
- Data volume: 24 million customer accounts, ~500 million annual transactions

**Priority**: MUST_HAVE

---

#### NFR-P-2: Premium Bonds Draw Processing Throughput

**Requirement**: The Premium Bonds prize draw must process all eligible bonds (current nominal value ~£125 billion, ~125 billion individual £1 bonds) within a 12-hour processing window, with checkpoint capability for restart.

**Measurement Method**: Draw processing elapsed time measured during full-volume test runs and production draws.

**Priority**: MUST_HAVE

---

#### NFR-P-3: Data Migration Throughput

**Requirement**: Data migration tooling must be capable of migrating 1 million customer accounts per 4-hour batch window, enabling the full 24 million account migration to be completed in phased overnight windows over a 4-week period.

**Measurement Method**: Migration batch elapsed time, records per second throughput, measured during rehearsals.

**Priority**: MUST_HAVE

---

#### NFR-P-4: Reconciliation Processing

**Requirement**: End-of-day reconciliation of all 24 million accounts between Atos and SBS must complete within a 6-hour overnight window.

**Measurement Method**: Reconciliation elapsed time measured during parallel-run.

**Priority**: MUST_HAVE

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: The SBS platform must achieve 99.95% availability for all customer-impacting services, measured monthly. This equates to a maximum 21.9 minutes unplanned downtime per month.
- Maximum planned downtime: 4 hours per month (off-peak maintenance window: Saturday 02:00–06:00 GMT)
- Maximum unplanned downtime per incident: 30 minutes (auto-recovery target)

**Maintenance Windows**: Saturday 02:00–06:00 GMT (planned); zero-downtime deployments required for all other changes.

**Priority**: MUST_HAVE

**Aligns with**: Principle P3 (Service Continuity Above All)

---

#### NFR-A-2: Disaster Recovery

**RPO (Recovery Point Objective)**: Maximum 1 minute of data loss for financial transactions; zero data loss for completed transactions (synchronous replication).

**RTO (Recovery Time Objective)**: Maximum 4 hours for full service recovery to secondary UK region.

**Backup Requirements**:
- Continuous replication to secondary UK cloud region
- Point-in-time recovery capability for databases (up to 35 days)
- Daily snapshots retained for 90 days; monthly snapshots retained for 7 years
- All backups stored in UK data centres only (Principle P2)

**Failover Requirements**:
- Automatic failover to secondary UK region for infrastructure failures: YES
- Failover time target: <15 minutes for automatic; <4 hours for full DR scenario
- Annual DR test mandatory; results reported to programme board

**Priority**: MUST_HAVE

---

#### NFR-A-3: Fault Tolerance

**Requirement**: The SBS platform must gracefully degrade when individual components fail, maintaining core transaction processing capability.

**Resilience Patterns Required** (Principle P6 — Modular and Loosely Coupled):
- [x] Circuit breaker for all external dependencies (payment rails, identity verification, HMRC)
- [x] Retry with exponential backoff for transient failures
- [x] Timeout on all network calls (default: 5 seconds; configurable per integration)
- [x] Bulkhead isolation for critical resources (transaction processing isolated from reporting)
- [x] Graceful degradation: if reporting services fail, transaction processing continues unaffected
- [x] Queue-based buffering for asynchronous operations (notifications, reconciliation)

**Priority**: MUST_HAVE

---

### Scalability Requirements

#### NFR-S-1: Horizontal Scaling

**Requirement**: The SBS platform must support horizontal scaling without code changes, to handle growth in customer base and transaction volumes.

**Growth Projections**:
- Year 1 (2028): 24 million accounts, ~500 million annual transactions
- Year 3 (2030): 26 million accounts, ~600 million annual transactions
- Year 5 (2032): 28 million accounts, ~700 million annual transactions

**Scaling Triggers**: Auto-scale when CPU >70% or memory >80% sustained for 5 minutes.

**Priority**: SHOULD_HAVE

**Aligns with**: Principle P1 (Cloud-Native by Default)

---

#### NFR-S-2: Data Volume Scaling

**Requirement**: The SBS platform must handle data growth to 50TB over 7 years (including full transaction history, audit logs, and regulatory records).

**Data Archival Strategy**: Hot storage for current year data; warm storage (3 years) for recent history; cold storage (7+ years) for regulatory retention. Aligns with DR-6 (Data Retention).

**Priority**: SHOULD_HAVE

---

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: All administrative and operational access to the SBS platform must use multi-factor authentication via NS&I's enterprise identity provider.

**Multi-Factor Authentication (MFA)**:
- Required for: All administrative users, all operational users, all API management access
- MFA methods: Hardware token (FIDO2) for privileged access; authenticator app for standard access
- Service-to-service: Mutual TLS with certificate rotation

**Session Management**:
- Session timeout: 15 minutes of inactivity for privileged operations; 30 minutes for standard
- Absolute session timeout: 8 hours
- Re-authentication required for: product configuration changes, migration initiation, security setting changes

**Priority**: MUST_HAVE

**Aligns with**: Principle P2 (Data Sovereignty and Security First)

---

#### NFR-SEC-2: Authorisation

**Requirement**: Role-based access control (RBAC) with least privilege principle. No user shall have access beyond what is required for their role.

**Roles**: Platform Administrator, Operations Engineer, Product Manager, Finance Analyst, Migration Engineer, Compliance Officer, Auditor (read-only), Security Administrator.

**Privilege Elevation**: Temporary elevated access via just-in-time (JIT) privilege management with time-limited grants (maximum 4 hours), approval workflow, and full audit trail.

**Priority**: MUST_HAVE

---

#### NFR-SEC-3: Data Encryption

**Requirement**:
- Data in transit: TLS 1.3 mandatory for all connections; no fallback to TLS 1.2 for new services
- Data at rest: AES-256 encryption for all data stores (databases, file storage, backups, logs)
- Key management: Cloud provider KMS with customer-managed keys (CMK); HSM-backed for PCI DSS scope

**Encryption Scope**:
- [x] Database encryption at rest (all databases, including replicas)
- [x] Backup encryption (all backups, including DR copies)
- [x] File storage encryption (all blob/object storage)
- [x] Application-level field encryption for PII and financial data
- [x] Log encryption (audit logs, operational logs)

**Priority**: MUST_HAVE

**Aligns with**: Principle P2 (Data Sovereignty and Security First)

---

#### NFR-SEC-4: Secrets Management

**Requirement**: No secrets (API keys, passwords, certificates, database credentials) stored in code, configuration files, or environment variables. All secrets managed via a dedicated secrets management service.

**Secrets Rotation**: Automatic rotation every 90 days for all credentials; immediate rotation capability for incident response.

**Priority**: MUST_HAVE

---

#### NFR-SEC-5: Vulnerability Management

**Requirement**:
- Dependency scanning in CI/CD pipeline: zero critical/high vulnerabilities in production deployments
- Static application security testing (SAST): every code commit
- Dynamic application security testing (DAST): weekly against staging environment
- Container image scanning: every build
- Penetration testing: annually by NCSC CHECK-approved provider; additionally before each major migration phase

**Remediation SLA**:
- Critical vulnerabilities: 24 hours
- High vulnerabilities: 7 days
- Medium vulnerabilities: 30 days
- Low vulnerabilities: 90 days

**Priority**: MUST_HAVE

**Aligns with**: Principle P10 (Compliance as Code)

---

#### NFR-SEC-6: Network Security

**Requirement**: Defence in depth with network segmentation, WAF, DDoS protection, and UK-only traffic routing for customer data.

- All SBS platform components in private subnets (no direct internet access)
- API Gateway with WAF for all external-facing APIs
- DDoS protection at infrastructure and application layers
- Network segmentation: PCI DSS cardholder data environment (CDE) isolated from general workloads
- All inter-service traffic encrypted (mutual TLS or service mesh)

**Priority**: MUST_HAVE

---

### Compliance and Regulatory Requirements

#### NFR-C-1: UK GDPR and Data Protection

**Applicable Regulations**: UK GDPR, Data Protection Act 2018

**Compliance Requirements**:
- [x] Data subject rights: access, rectification, erasure (where not overridden by financial record retention), portability, restriction, objection
- [x] Consent management and audit trail where consent is the lawful basis
- [x] Privacy by design and by default (minimum data collection, purpose limitation)
- [x] Data breach notification to ICO within 72 hours; to affected individuals without undue delay if high risk
- [x] DPIA completed and approved before customer data migration
- [x] Records of processing activities maintained

**Data Residency**: UK only — all customer and financial data stored and processed in UK data centres. No data transfers outside UK. Aligns with Principle P2.

**Data Retention**: Per DR-6 (7 years for financial records; as per product terms for customer accounts).

**Priority**: MUST_HAVE

---

#### NFR-C-2: Audit Logging

**Requirement**: Comprehensive immutable audit trail for all state-changing operations, meeting financial services and government requirements.

**Audit Log Contents** (for all sensitive operations):
- Who: User/service identity (authenticated identity, not just session)
- What: Action performed (operation type, affected resource)
- When: Timestamp (UTC, millisecond precision)
- Where: System component, source IP, API endpoint
- Why: Business context (request ID, transaction ID, approval reference)
- Result: Success/failure with error details and before/after state

**Log Retention**: 7 years for financial audit logs (immutable, tamper-evident storage). 13 months for operational logs.

**Log Integrity**: Tamper-evident logging with cryptographic chaining. Any modification or deletion of audit records must be detectable and alerted.

**Priority**: MUST_HAVE

**Aligns with**: Principle P8 (Observable and Auditable by Design)

---

#### NFR-C-3: Regulatory Reporting

**Requirement**: The SBS platform must generate all mandatory regulatory reports.

**Report Types**:
- HMRC annual interest certificates: Annually, to HMRC and customers, electronic format
- FCA regulatory returns: As required, to FCA, prescribed format
- PRA operational resilience returns: Annually, to PRA, prescribed format
- Bank of England statistical returns: Monthly/quarterly, to BoE, prescribed format
- PCI DSS compliance reports: Annually, to QSA, SAQ/ROC format
- Internal audit reports: Quarterly, to NS&I Board, internal format

**Priority**: MUST_HAVE

---

#### NFR-C-4: PCI DSS v4.0 Compliance

**Requirement**: The SBS cardholder data environment must achieve PCI DSS v4.0 certification before any card transaction processing.

**Scope**: All components that store, process, or transmit cardholder data, including APIs, databases, and network segments.

**Key Controls**:
- Network segmentation of CDE from general environment
- Encryption of cardholder data at rest and in transit
- Access restricted to business need-to-know
- Vulnerability management programme for CDE components
- Logging and monitoring of all access to CDE
- Annual QSA assessment; quarterly ASV scans

**Priority**: MUST_HAVE

---

#### NFR-C-5: NCSC Cyber Assessment Framework

**Requirement**: The SBS platform must achieve "Achieved" status against all applicable NCSC CAF outcomes across the four objectives: Managing Security Risk, Protecting Against Cyber Attack, Detecting Cyber Security Events, Minimising Impact of Incidents.

**Assessment**: Self-assessment annually; IT Health Check by CHECK provider before go-live and annually thereafter.

**Priority**: MUST_HAVE

---

### Usability Requirements

#### NFR-U-1: Administrative User Experience

**Requirement**: All administrative interfaces (product configuration, operations, reporting, migration tooling) must be usable by NS&I staff with medium technical proficiency without specialist training.

**UX Standards**:
- Consistent with GDS Design System patterns where applicable
- WCAG 2.1 Level AA compliance for all administrative interfaces
- Dashboard-first design for operational monitoring
- Contextual help and tooltips for complex operations

**Priority**: SHOULD_HAVE

---

#### NFR-U-2: Accessibility

**Requirement**: WCAG 2.1 Level AA compliance for all user interfaces (administrative, operational, reporting).

**Accessibility Features**:
- [x] Keyboard navigation for all functions
- [x] Screen reader compatibility (JAWS, NVDA, VoiceOver)
- [x] Sufficient colour contrast ratios
- [x] Resizable text without loss of functionality
- [x] Alternative text for non-text content

**Testing**: Automated accessibility testing in CI/CD pipeline; manual testing with assistive technologies quarterly.

**Priority**: MUST_HAVE (GDS Service Standard requirement)

---

### Maintainability and Supportability Requirements

#### NFR-M-1: Observability

**Requirement**: Comprehensive instrumentation for monitoring, alerting, and troubleshooting across all SBS platform components.

**Telemetry Requirements** (Principle P8):
- **Logging**: Structured JSON logs; centralised aggregation; correlation IDs across all services
- **Metrics**: Prometheus-compatible; RED metrics (Rate, Errors, Duration) for all services; business metrics (transactions/second, active accounts)
- **Tracing**: Distributed tracing with OpenTelemetry across all microservices and integrations
- **Dashboards**: Real-time operational dashboards for service health, SLA compliance, and business metrics
- **Alerts**: SLO-based alerting with tiered severity; alerts link to runbooks; PagerDuty/equivalent integration

**Priority**: MUST_HAVE

---

#### NFR-M-2: Documentation

**Requirement**: Comprehensive documentation for platform operators, developers, and auditors.

**Documentation Types**:
- [x] Architecture documentation (C4 model: context, container, component, code)
- [x] API documentation (OpenAPI 3.0 specifications, auto-generated from code)
- [x] Operational runbooks for all critical procedures
- [x] Troubleshooting guides for known failure modes
- [x] Data dictionary for all data entities and classifications
- [x] Regulatory compliance evidence pack

**Priority**: MUST_HAVE

---

#### NFR-M-3: Deployment and Release Management

**Requirement**: All changes to the SBS platform must be deployed via automated CI/CD pipelines with zero-downtime deployment capability.

- Blue-green or canary deployment patterns for all production changes
- Feature flags for controlled rollout of new functionality
- Automated rollback capability triggered by health check failures
- Maximum deployment time: 30 minutes from approval to production
- All deployments fully auditable (who, what, when, approval reference)

**Priority**: MUST_HAVE

**Aligns with**: Principle P9 (Incremental Delivery with Measurable Value)

---

### Portability and Interoperability Requirements

#### NFR-I-1: API Standards

**Requirement**: All APIs must conform to OpenAPI 3.0+ specification with RESTful design principles.

**API Design Principles** (Principle P6, P7):
- RESTful design with standard HTTP methods
- JSON request/response format (JSON:API or similar standard)
- Versioning via URL path (/v1/, /v2/)
- Consistent error response format with error codes, messages, and correlation IDs
- Rate limiting and throttling for all external-facing APIs
- Open standards preferred: REST, OpenAPI, OAuth 2.0, OIDC, CloudEvents

**Priority**: MUST_HAVE

---

#### NFR-I-2: Vendor Portability

**Requirement**: All data stored in portable formats with documented schemas. No proprietary data formats for customer or financial data. Abstraction layers at key integration points to enable component replacement without full re-platforming.

**Portability Requirements** (Principle P7):
- Data export capability in standard formats (CSV, JSON, XML) for all data entities
- API contracts defined independently of SBS implementation details
- Integration layer (API gateway/ESB) isolating SBS internals from consuming services
- Contractual data portability clause with SBS

**Priority**: SHOULD_HAVE

---

## Integration Requirements

### INT-1: Atos Legacy Platform (Dual-Run)

**Purpose**: Bidirectional data synchronisation during the parallel-run period; data extraction for migration.

**Integration Type**: Real-time event-driven synchronisation + batch data extraction

**Data Exchanged**:
- **From Atos to SBS**: Customer account data, transaction records, product configurations, standing orders, nominated accounts, historical transaction data (full history for migration)
- **From SBS to Atos**: Transaction confirmations during dual-write period (if applicable)

**Integration Pattern**: Event-driven for real-time sync; batch ETL for migration extracts

**Authentication**: Mutual TLS with certificate-based authentication

**Error Handling**: Dead letter queue for failed sync events; automated retry with exponential backoff; manual reconciliation for unresolvable failures

**SLA**: Real-time sync: <5 second latency; batch extraction: 1M records per 4 hours

**Owner**: Programme Director (NS&I), with Atos Technical Lead

**Priority**: MUST_HAVE

---

### INT-2: Payment Rails (BACS, Faster Payments, CHAPS)

**Purpose**: Process customer deposits, withdrawals, and prize distributions via UK payment schemes.

**Integration Type**: Real-time API (Faster Payments) + Batch file transfer (BACS, CHAPS)

**Data Exchanged**:
- **Outbound**: Payment instructions (withdrawals, prize distributions, interest payments)
- **Inbound**: Payment notifications (deposits, direct debits, standing orders)

**Integration Pattern**: SBS platform integrates via payment gateway; BACS via AUDDIS/ARUDD file exchange; Faster Payments via ISO 20022 messaging

**Authentication**: Mutual TLS, SWIFTNet connectivity (for CHAPS)

**SLA**: BACS: within standard BACS processing cycle (3 business days); Faster Payments: <15 seconds; CHAPS: within same-day processing window

**Owner**: NS&I Operations Director

**Priority**: MUST_HAVE

---

### INT-3: Card Payment Processor

**Purpose**: Process debit card deposits and (where applicable) card-linked withdrawals.

**Integration Type**: Real-time API

**Data Exchanged**:
- **Outbound**: Transaction authorisation requests, settlement instructions
- **Inbound**: Authorisation responses, settlement confirmations, chargebacks

**Integration Pattern**: PCI DSS compliant tokenised card processing; SBS platform sends tokenised requests to payment processor; no cardholder data stored in SBS (tokens only)

**Authentication**: Mutual TLS with PCI DSS compliant key management

**SLA**: Authorisation: <3 seconds; settlement: within T+1

**Owner**: NS&I Operations Director

**Priority**: MUST_HAVE

---

### INT-4: HMRC Tax Reporting

**Purpose**: Report customer interest earned and tax information to HMRC.

**Integration Type**: Batch file transfer (annual) + real-time for individual tax queries

**Data Exchanged**:
- **Outbound**: Annual interest certificate data, R85 exemption data
- **Inbound**: Tax status verifications

**Integration Pattern**: Secure file transfer (SFTP) for annual batch; API for real-time queries (where available)

**Authentication**: Government Gateway / HMRC API authentication

**SLA**: Annual return: submitted within HMRC deadlines; real-time queries: <10 seconds

**Owner**: NS&I Finance team

**Priority**: MUST_HAVE

---

### INT-5: GOV.UK Notify

**Purpose**: Send customer notifications (emails, SMS, letters) via the government notification platform.

**Integration Type**: Real-time API

**Data Exchanged**:
- **Outbound**: Notification requests (recipient, template, personalisation data)
- **Inbound**: Delivery status callbacks

**Integration Pattern**: RESTful API integration with GOV.UK Notify service

**Authentication**: API key with IP allowlisting

**SLA**: API call: <2 seconds; email delivery: within 5 minutes; SMS delivery: within 1 minute; letter: within postal SLA

**Owner**: NS&I Customer Services

**Priority**: SHOULD_HAVE

---

### INT-6: Identity Verification Service

**Purpose**: Verify customer identity for new account applications, high-value transactions, and security changes.

**Integration Type**: Real-time API

**Data Exchanged**:
- **Outbound**: Identity verification requests (name, date of birth, address, document references)
- **Inbound**: Verification results (verified/not verified, confidence score, risk flags)

**Integration Pattern**: RESTful API with SBS triggering verification during account onboarding and high-risk operations

**Authentication**: OAuth 2.0 with mutual TLS

**SLA**: Verification response: <10 seconds; availability: 99.9%

**Owner**: NS&I Compliance team

**Priority**: MUST_HAVE

---

### INT-7: Centralised Logging and Monitoring Platform

**Purpose**: Aggregate logs, metrics, and traces from all SBS platform components for operational monitoring, alerting, and audit.

**Integration Type**: Real-time streaming

**Data Exchanged**:
- **From SBS**: Structured logs (JSON), Prometheus metrics, OpenTelemetry traces, audit events
- **To SBS**: Alert notifications, dashboard queries

**Integration Pattern**: Log shipping via agents; metrics via Prometheus scraping; traces via OpenTelemetry collector; all to centralised platform (e.g., ELK/Splunk/Grafana/CloudWatch)

**Authentication**: Service accounts with least-privilege access

**SLA**: Log ingestion: <30 second delay; metrics: <15 second delay; alerts: <1 minute from trigger to notification

**Owner**: NS&I Platform Operations

**Priority**: MUST_HAVE

---

### INT-8: Enterprise Identity Provider

**Purpose**: Authenticate and authorise all administrative and operational users accessing the SBS platform.

**Integration Type**: Real-time API (SAML 2.0 / OIDC)

**Data Exchanged**:
- **From IdP to SBS**: Authentication tokens, user attributes, group memberships
- **From SBS to IdP**: Authentication requests, session management

**Integration Pattern**: SAML 2.0 or OIDC federated authentication; RBAC group-to-role mapping

**Authentication**: Federation trust with NS&I enterprise IdP

**SLA**: Authentication: <2 seconds; availability: 99.99%

**Owner**: NS&I CISO

**Priority**: MUST_HAVE

---

## Data Requirements

### DR-1: Customer Account Data

**Description**: Core customer account records including personal details, account details, product holdings, nominated bank accounts, and communication preferences.

**Key Attributes**:
| Attribute | Type | Required | Classification | Constraints |
|-----------|------|----------|----------------|-------------|
| Customer ID | UUID | Yes | OFFICIAL | Primary key, globally unique |
| Full Name | String(255) | Yes | OFFICIAL (PII) | Not null |
| Date of Birth | Date | Yes | OFFICIAL (PII) | Valid date, >18 years for most products |
| Address | Structured | Yes | OFFICIAL (PII) | UK address validation |
| Email | String(255) | Conditional | OFFICIAL (PII) | Valid format, unique per customer |
| Account Number | String(16) | Yes | OFFICIAL | Unique, NS&I format |
| Product Type | Enum | Yes | OFFICIAL | Valid NS&I product code |
| Balance | Decimal(15,2) | Yes | OFFICIAL | ≥0, currency GBP |
| Nominated Bank Account | Encrypted | Yes | OFFICIAL-SENSITIVE | Sort code + account number, encrypted at rest |

**Data Volume**: 24 million customer records; estimated 40 million account records (customers may hold multiple products)

**Data Classification**: OFFICIAL; PII fields subject to UK GDPR; nominated bank account details classified OFFICIAL-SENSITIVE

**Data Retention**: Active accounts: indefinite while active. Closed accounts: 7 years from closure date.

---

### DR-2: Transaction History

**Description**: Complete record of all financial transactions across all accounts, including deposits, withdrawals, interest payments, prize wins, transfers, and fee assessments.

**Key Attributes**:
| Attribute | Type | Required | Classification | Constraints |
|-----------|------|----------|----------------|-------------|
| Transaction ID | UUID | Yes | OFFICIAL | Primary key, globally unique |
| Account Number | String(16) | Yes | OFFICIAL | Foreign key to account |
| Transaction Type | Enum | Yes | OFFICIAL | Deposit, withdrawal, interest, prize, transfer, fee |
| Amount | Decimal(15,2) | Yes | OFFICIAL | Signed decimal (positive/negative) |
| Value Date | Date | Yes | OFFICIAL | Business date of transaction |
| Processing Timestamp | Timestamp | Yes | OFFICIAL | UTC, millisecond precision |
| Balance After | Decimal(15,2) | Yes | OFFICIAL | Running balance post-transaction |
| Reference | String(255) | Conditional | OFFICIAL | Payment reference, prize draw reference |

**Data Volume**: Estimated 500 million transactions per year; full history migration (~5 billion historical records)

**Access Patterns**: By account number (primary); by date range; by transaction type; by reference

**Data Retention**: 7 years from transaction date (regulatory requirement). Archival to cold storage after 3 years.

---

### DR-3: Data Transformation Rules

**Description**: Documented mapping rules for transforming data from Atos legacy schema to SBS schema, covering all data entities.

**Requirements**:
- Full field-level mapping for all entities (customer, account, transaction, product, standing order)
- Transformation logic documented and version-controlled
- Default value handling for fields that exist in SBS but not in Atos
- Data type conversion rules (e.g., Atos date formats to ISO 8601)
- Character encoding conversion (Atos character set to UTF-8)
- Validation rules applied during transformation (rejected records logged for manual review)

**Data Classification**: OFFICIAL

---

### DR-4: Premium Bonds Holdings

**Description**: Record of all Premium Bonds holdings including bond numbers, purchase dates, eligibility status, and prize history.

**Key Attributes**:
| Attribute | Type | Required | Classification | Constraints |
|-----------|------|----------|----------------|-------------|
| Bond Range Start | String(12) | Yes | OFFICIAL | Valid bond number format |
| Bond Range End | String(12) | Yes | OFFICIAL | Valid bond number format |
| Customer ID | UUID | Yes | OFFICIAL | Foreign key to customer |
| Purchase Date | Date | Yes | OFFICIAL | Determines eligibility (1 calendar month) |
| Nominal Value | Decimal(15,2) | Yes | OFFICIAL | Multiples of £25 (minimum), max £50,000 per person |
| Eligibility Date | Date | Yes | OFFICIAL | Purchase date + 1 calendar month |
| Status | Enum | Yes | OFFICIAL | Active, redeemed, dormant |

**Data Volume**: ~125 billion individual £1 bond units; stored as bond ranges per holding

**Access Patterns**: By customer (holdings); by bond number (prize lookup); by eligibility date (draw inclusion)

**Data Retention**: Active bonds: indefinite. Redeemed bonds: 7 years from redemption.

---

### DR-5: Audit Log Data

**Description**: Immutable audit records for all state-changing operations across the SBS platform.

**Key Attributes**:
| Attribute | Type | Required | Classification | Constraints |
|-----------|------|----------|----------------|-------------|
| Audit ID | UUID | Yes | OFFICIAL | Primary key |
| Timestamp | Timestamp | Yes | OFFICIAL | UTC, millisecond precision |
| Actor | String(255) | Yes | OFFICIAL | Authenticated user/service identity |
| Action | String(100) | Yes | OFFICIAL | Operation type |
| Resource | String(255) | Yes | OFFICIAL | Affected entity |
| Before State | JSON | Conditional | OFFICIAL | State before change |
| After State | JSON | Conditional | OFFICIAL | State after change |
| Result | Enum | Yes | OFFICIAL | Success, failure, partial |
| Correlation ID | UUID | Yes | OFFICIAL | Request chain identifier |

**Data Volume**: Estimated 1 billion audit records per year

**Data Classification**: OFFICIAL; immutable; tamper-evident (cryptographic chaining)

**Data Retention**: 7 years (financial regulatory requirement). Cold storage after 13 months. Never deleted within retention period.

---

### DR-6: Data Retention Policy

**Description**: Retention schedule for all data types in the SBS platform.

| Data Type | Retention Period | Basis | Archive After | Deletion Method |
|-----------|-----------------|-------|---------------|-----------------|
| Customer account data (active) | Indefinite while active | Business requirement | N/A | N/A |
| Customer account data (closed) | 7 years from closure | Financial regulations | 1 year | Secure erasure (NCSC standards) |
| Transaction history | 7 years from transaction date | Financial regulations, HMRC | 3 years to warm, 5 years to cold | Secure erasure |
| Premium Bonds holdings (active) | Indefinite while active | Business requirement | N/A | N/A |
| Premium Bonds holdings (redeemed) | 7 years from redemption | Financial regulations | 1 year | Secure erasure |
| Audit logs | 7 years | Financial regulations, NCSC CAF | 13 months to warm, 3 years to cold | Secure erasure |
| Operational logs | 13 months | Operational requirement | 3 months | Standard deletion |
| Backup data | 90 days (daily), 7 years (monthly) | DR requirements | N/A | Overwritten per rotation |

---

### Data Quality Requirements

**Data Accuracy**: Zero tolerance for financial data discrepancies. Reconciliation must confirm penny-level accuracy for all migrated accounts.

**Data Completeness**: All mandatory fields populated; migration validation rejects records with missing mandatory fields for manual remediation.

**Data Consistency**: Cross-system reconciliation between Atos and SBS during parallel-run; post-migration audit for data integrity.

**Data Timeliness**: Real-time data for transaction processing and balance enquiries; T+0 for reconciliation data; T+1 for reporting data.

**Data Lineage**: Full lineage tracking for migrated data (source system, transformation applied, target location, migration date).

---

### Data Migration Requirements

**Migration Scope**: All customer account data, transaction history (full), product configurations, standing orders, nominated bank accounts, Premium Bonds holdings, and dormancy records from Atos legacy platform.

**Migration Strategy**: Phased migration by product type, starting with lowest-risk products (e.g., Direct Saver), progressing to complex products (Premium Bonds last). Each phase includes: extraction, transformation, loading, verification, parallel-run, and cutover.

**Migration Order**:
1. Direct Saver / Direct ISA (lowest complexity, high volume test)
2. Income Bonds / Investment Account (moderate complexity)
3. Green Savings Bonds / Guaranteed Growth Bonds / Guaranteed Income Bonds (moderate complexity)
4. Junior ISA (requires specific regulatory handling)
5. Premium Bonds (highest complexity, highest risk — last)

**Data Transformation**: Per DR-3 (documented field-level mapping rules)

**Data Validation**: Record-level verification post-migration (count, balance, checksum); reconciliation must achieve 99.9999% match rate before cutover approval

**Rollback Plan**: Atos remains primary until cutover approval; rollback reverts transaction routing to Atos within 30 minutes; SBS data retained for investigation

**Migration Timeline**: 4-week phased migration windows per product type; total migration period: 6–12 months

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: All infrastructure must be deployed in UK sovereign cloud regions only (Principle P2). No data processing or storage outside UK borders.

**TC-2**: SBS SBP Digital Core is the mandated core banking engine. The architecture must work within SBS platform capabilities, extending via APIs rather than core modification where possible.

**TC-3**: The Atos legacy platform cannot be modified to support migration (frozen estate). All integration must work with existing Atos interfaces and data formats.

**TC-4**: Payment rail integrations (BACS, Faster Payments, CHAPS) must comply with UK payment scheme rules and messaging standards (ISO 20022).

**TC-5**: All systems must meet OFFICIAL security classification handling requirements per HMG Security Policy Framework.

**TC-6**: Zero-downtime deployment patterns required for all production changes (Principle P3).

---

### Business Constraints

**BC-1**: The 2028 target go-live for SBS platform was communicated to Parliament but the PAC (13 Feb 2026) explicitly recommended NS&I **stop targeting March 2028** and instead develop a realistic bottom-up integrated plan with credible timelines. This constraint is now under review — NS&I must respond to PAC recommendations within 60 days. Any revised timeline requires Ministerial notification and Treasury approval.

**BC-2**: Total programme budget includes the additional £109M approved in January 2026, subject to parliamentary approval. No additional funding assumed.

**BC-3**: Atos contractual exit must follow the agreed exit schedule. Changes require formal contract variation.

**BC-4**: The Premium Bonds prize draw must run every month without exception. No migration activity may delay, disrupt, or compromise the draw.

**BC-5**: Maximum 3-month delivery cycles (Principle P9). No work package may exceed 3 months without delivering measurable value.

---

### Assumptions

**A-1**: SBS SBP Digital Core can be configured (not custom-coded) to support all current NS&I product types. Fit-gap analysis to validate.

**A-2**: Atos will fulfil knowledge transfer obligations as per the exit contract and retain identified key personnel through the transition period.

**A-3**: UK sovereign cloud infrastructure (AWS UK / Azure UK / GCP europe-west2) will provide sufficient capacity for NS&I workloads.

**A-4**: NS&I can recruit sufficient permanent technical staff within government pay frameworks, potentially using DDaT pay exceptions.

**A-5**: Regulatory frameworks (PCI DSS, NCSC CAF, FCA rules) will not change materially during the migration period. If they do, a 10% compliance contingency budget is reserved.

**A-6**: The existing Atos platform will remain stable and performant throughout the dual-running period (2026–2028).

**A-7**: GOV.UK Notify has sufficient capacity and SLA for NS&I's notification volumes (millions of notifications per month).

**Validation Plan**: A-1 validated through SBS fit-gap analysis (Q2 2026). A-2 validated through Atos exit contract review. A-3 validated through cloud capacity planning exercise. A-4 monitored monthly via recruitment dashboard.

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Programme cost variance | No baseline | <5% monthly | Ongoing | EVM reporting |
| Customer service disruption incidents | 0 (target) | 0 P1/P2 from migration | Throughout migration | Incident management system |
| Permanent staff ratio | ~15% | 30% (2026), 50% (2027) | End of 2026/2027 | HR dashboard |
| IPA delivery confidence | RED (estimated) | AMBER (12 months) | Q1 2027 | IPA quarterly review |
| Atos SLA compliance | Contractual | 100% through transition | Until exit | SLA monitoring |
| Regulatory accreditation | Not started | Full accreditation | Pre-migration (H1 2028) | Accreditation certificates |
| Data migration accuracy | N/A | 99.9999% match rate | Pre-cutover per product | Reconciliation reports |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| SBS platform availability | 99.95% | Uptime monitoring |
| API response time (p95) | <500ms (transactions) | APM tooling |
| Premium Bonds draw completion | Within 12-hour window | Draw processing log |
| Reconciliation match rate | 99.9999% | Reconciliation engine |
| Zero critical security findings at go-live | 0 critical/high | Security scanning |
| Deployment frequency | Weekly or better | CI/CD metrics |
| Mean time to recovery (MTTR) | <30 minutes | Incident tracking |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| SBS contract finalisation | SBS delivery milestones and pricing agreed | Programme Director | Q2 2026 | At Risk | HIGH — blocks all SBS delivery |
| Atos exit plan agreement | Formal exit schedule and KT programme agreed | Programme Director | Q2 2026 | At Risk | HIGH — blocks knowledge transfer |
| Cloud infrastructure provisioning | UK sovereign cloud environment ready for SBS | NS&I CTO | Q3 2026 | On Track | MEDIUM — blocks SBS deployment |
| Fit-gap analysis | SBS product capability confirmed for all NS&I products | Chief Architect | Q2 2026 | Not Started | HIGH — may reveal need for customisation |
| Permanent staff recruitment | Technology leadership positions filled | HR Director | Q4 2026 | Not Started | HIGH — blocks capability target |
| Payment scheme connectivity | BACS/FPS/CHAPS connectivity for SBS approved | Operations Director | Q1 2027 | Not Started | HIGH — blocks transaction testing |
| NCSC engagement | NCSC guidance on cloud security architecture obtained | CISO | Q3 2026 | Not Started | MEDIUM — may delay security design |
| PCI DSS scope agreement | PCI DSS CDE boundary defined for SBS | CISO | Q3 2026 | Not Started | MEDIUM — may delay security assessment |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | SBS requires extensive customisation for NS&I products | MEDIUM | HIGH | Fit-gap analysis before commitment; standard-first approach | Chief Architect |
| R-2 | Key Atos staff depart before knowledge transfer complete | HIGH | HIGH | Retention incentives; documentation-first approach; video walkthroughs | Programme Director |
| R-3 | Government pay scales fail to attract senior technologists | MEDIUM | HIGH | DDaT pay exceptions; non-financial benefits; specialist recruiters | HR Director |
| R-4 | Legacy data quality issues discovered during migration | HIGH | MEDIUM | Early data profiling; remediation workstream; extended testing | Data Migration Lead |
| R-5 | Premium Bonds draw algorithm complexity exceeds SBS capability | LOW | CRITICAL | Early prototype; dedicated draw system if needed | Chief Architect |
| R-6 | "Good news" culture persists despite PAC findings | HIGH | HIGH | Independent assurance; anonymous reporting; NED challenge | NS&I CEO |
| R-7 | Dual-run costs exceed budget due to extended parallel period | MEDIUM | HIGH | Time-bound parallel-run with clear exit criteria per product | NS&I CFO |
| R-8 | Regulatory framework changes during migration | MEDIUM | MEDIUM | Regulatory monitoring; 10% compliance contingency; regulator engagement | CISO |

---

## Requirement Conflicts & Resolutions

### Conflict C-1: Migration Speed vs. Migration Safety

**Conflicting Requirements**:
- **BR-6**: Deliver SBS platform by 2028 (MUST_HAVE)
- **BR-2**: Zero customer service disruption during migration (MUST_HAVE)

**Stakeholders Involved**:
- **HM Treasury (SD-1)** and **PAC (SD-2)**: Want visible progress and results after five years of limited delivery; 2028 is communicated to Parliament
- **NS&I Operations Director (SD-5)**: Requires extended parallel-run, multiple cutover rehearsals, and conservative migration approach to protect 24 million customers

**Nature of Conflict**: The 2028 timeline is ambitious given the programme's history. Thorough testing, extended parallel-run, and multiple rehearsals compress the available implementation time. Rushing migration to meet the deadline could cause customer-impacting incidents.

**Trade-off Analysis**:

| Option | Pros | Cons | Impact |
|--------|------|------|--------|
| **Prioritize Speed** (compress testing) | Meet 2028 deadline; satisfy Treasury/PAC | Higher incident risk; potential regulatory concerns | Treasury satisfied; Operations/CISO alarmed |
| **Prioritize Safety** (extend timeline to 2029) | Thorough testing; lower risk | Miss parliamentary commitment; further PAC criticism | Operations satisfied; Treasury/PAC frustrated |
| **Phase (recommended)** | Early wins demonstrate progress; complex products get adequate time | Requires parallel investment in early and late phases | Both partially satisfied |

**Resolution Strategy**: PHASE

**Decision**: Start migration with low-risk products (Direct Saver, Direct ISA) in H2 2027 to demonstrate capability and build confidence, while giving Premium Bonds (highest complexity) a dedicated extended timeline through H2 2028. If the low-risk migrations succeed, they provide evidence to Treasury/PAC of progress. If issues emerge, there is time to adjust before migrating Premium Bonds.

**Decision Authority**: NS&I CEO (Accountable), with HM Treasury Sponsor approval

**Impact on Requirements**:
- **FR-7 (Migration Tooling)**: Must support phased migration by product type
- **BR-6**: Refined to "SBS platform accreditation by Q2 2028; phased migration through H2 2028"
- **BR-2**: Maintained as absolute — no product migrated until reconciliation achieves 99.9999%

**Stakeholder Management**:
- **Treasury/PAC**: Communicated that phased approach delivers first migrated products in 2027, demonstrating capability before the critical Premium Bonds migration
- **Operations Director**: Confirmed that no product moves until safety criteria are met

---

### Conflict C-2: Vendor Independence vs. SBS Platform Commitment

**Conflicting Requirements**:
- **NFR-I-2**: Vendor portability — abstraction layers, open standards, avoid lock-in (Principle P7)
- **BR-6**: Deliver SBS SBP Digital Core as the strategic platform (programme mandate)

**Stakeholders Involved**:
- **NS&I Chief Architect (SD-14)**: Wants architecture that avoids recreating the Atos single-vendor dependency
- **SBS (SD-9)**: Wants NS&I to fully adopt SBS platform capabilities for optimal performance and supportability

**Nature of Conflict**: Principle P7 mandates vendor independence, but the programme is committing to SBS as the core banking engine. Adding abstraction layers around SBS adds complexity, cost, and risk. Using SBS native capabilities is faster and more supportable but creates deeper dependency.

**Trade-off Analysis**:

| Option | Pros | Cons | Impact |
|--------|------|------|--------|
| **Full abstraction** | Maximum portability; could replace SBS | Significant additional cost; slower delivery; potential performance overhead | Architect satisfied; SBS concerned; CFO alarmed at cost |
| **Native SBS** (minimal abstraction) | Fastest delivery; best performance; SBS optimised | Deep vendor lock-in; repeat of Atos pattern | SBS satisfied; Architect alarmed |
| **Selective abstraction (recommended)** | Protect key boundaries; practical portability; manageable cost | Not fully portable; some SBS dependency remains | Both partially satisfied |

**Resolution Strategy**: COMPROMISE

**Decision**: Apply abstraction at the integration boundary (API Gateway layer between SBS and all consuming services) and at the data layer (data stored in portable formats with documented schemas). Accept SBS as the core banking engine with native usage of its product and transaction capabilities. This protects against full lock-in while pragmatically leveraging SBS capabilities.

**Decision Authority**: NS&I CTO (Accountable), with Chief Architect and SBS agreement

**Impact on Requirements**:
- **NFR-I-1**: API standards apply to all APIs exposed by the integration layer (not SBS internal APIs)
- **NFR-I-2**: Vendor portability focused on integration and data layers; SBS core accepted as strategic dependency
- **New requirement**: Annual vendor dependency risk assessment (aligned with Principle P7)

---

### Conflict C-3: Cost Reduction vs. Capability Building

**Conflicting Requirements**:
- **BR-8**: Reduce consultant spend by 25% by end of 2027 (SHOULD_HAVE)
- **BR-4**: Build 50% permanent staff ratio by end of 2027 (MUST_HAVE)
- **BR-6**: Deliver SBS platform by 2028 (MUST_HAVE)

**Stakeholders Involved**:
- **NS&I CFO (SD-7)**: Wants immediate cost reduction in consultant spend
- **NS&I CTO (SD-4)**: Needs experienced consultants to maintain delivery velocity while building permanent team
- **PAC (SD-2)**: Wants both accountability AND delivery — reducing consultants too fast risks delivery; not reducing them contradicts PAC findings

**Nature of Conflict**: Cutting consultants before permanent replacements are hired and effective would slow delivery. But retaining full consultant levels contradicts the PAC recommendation and costs money. Recruitment takes 3-6 months; onboarding takes 3 months; so effective productivity from permanent staff is 6-9 months away.

**Trade-off Analysis**:

| Option | Pros | Cons | Impact |
|--------|------|------|--------|
| **Immediate 25% cut** | Fast cost savings; PAC headline | Delivery risk; knowledge loss; morale impact | CFO happy; CTO alarmed; delivery at risk |
| **No reduction until 2028** | Delivery protected; orderly transition | Contradicts PAC; costs continue | CTO happy; CFO/PAC unhappy |
| **Graduated reduction (recommended)** | Balanced approach; aligned with recruitment | Neither fully fast nor fully slow | All partially satisfied |

**Resolution Strategy**: PHASE

**Decision**: Graduated reduction — maintain consultant levels for 6 months while accelerating permanent recruitment and paired working. Reduce by 10% at month 6, 15% at month 12, 25% at month 18 (end of 2027). Each reduction contingent on permanent staff being in post and effective.

**Decision Authority**: NS&I CFO (Accountable), with CTO input

**Impact on Requirements**:
- **BR-8**: Refined — "Graduated 25% reduction by end of 2027, contingent on permanent staff readiness"
- **BR-4**: Unchanged — permanent staff targets are the enabler for consultant reduction

---

### Conflict C-4: Regulatory Thoroughness vs. Delivery Timeline

**Conflicting Requirements**:
- **BR-3**: Full regulatory accreditation before customer migration (MUST_HAVE)
- **BR-6**: SBS platform delivery by 2028 (MUST_HAVE)

**Stakeholders Involved**:
- **NS&I CISO (SD-6)**: Requires comprehensive security assessment including NCSC IT Health Check, PCI DSS QSA audit, and penetration testing — each with remediation cycles
- **Programme Director**: Needs accreditation to fit within the delivery timeline without becoming the critical path

**Nature of Conflict**: Security accreditation is inherently sequential — you can't test what isn't built, and remediation cycles are unpredictable. If accreditation reveals significant issues late in the programme, the 2028 go-live is at risk.

**Resolution Strategy**: INNOVATE

**Decision**: Shift security left — integrate security assessment into the design and build process rather than treating it as a late-stage gate. Security architecture review at design stage; automated security scanning in CI/CD (Principle P10); NCSC engagement from Q3 2026; pre-assessment walkthroughs with PCI QSA from Q1 2027; formal assessment in Q4 2027 with 6-month remediation window before migration.

**Decision Authority**: NS&I CISO (Security gate owner), Programme Director (Timeline)

**Impact on Requirements**:
- **NFR-SEC-5**: Strengthened — continuous security scanning throughout development, not just at accreditation time
- **NFR-C-5**: Phased — informal NCSC CAF assessment at design stage, formal at Q4 2027
- **BR-3**: Maintained — no customer migration without full accreditation

---

## Timeline and Milestones

### High-Level Milestones

| Milestone | Description | Target Date | Dependencies |
|-----------|-------------|-------------|--------------|
| Requirements Approval | Stakeholder sign-off on this document | Q1 2026 | Stakeholder review |
| SBS Fit-Gap Analysis Complete | Confirm SBS capability for all NS&I products | Q2 2026 | SBS contract, Product Owner input |
| Atos Exit Plan Agreed | Contractual exit schedule and KT programme | Q2 2026 | Contract negotiation |
| Cost Baseline Validated | Independent cost assurance complete | Q2 2026 (90 days from reset) | Work breakdown structure |
| Cloud Infrastructure Ready | UK sovereign cloud environment provisioned | Q3 2026 | Cloud procurement |
| SBS Platform Integration Starts | Development environment operational | Q3 2026 | Fit-gap, infrastructure |
| 30% Permanent Staff Achieved | Capability target (Milestone 1) | Q4 2026 | Recruitment pipeline |
| SBS Platform Testing Begins | Functional, performance, security testing | Q1 2027 | SBS integration |
| Payment Scheme Connectivity | BACS/FPS/CHAPS operational for SBS | Q1 2027 | Scheme applications |
| First Product Parallel-Run | Direct Saver on parallel-run (Atos + SBS) | Q3 2027 | Product configuration, testing |
| Security Pre-Assessment | NCSC CAF and PCI DSS pre-assessment | Q4 2027 | Platform build |
| First Product Migration (Go-Live) | Direct Saver migrated to SBS | H2 2027 | Parallel-run success |
| SBS Platform Accreditation | Full functional, performance, security accreditation | Q2 2028 | Testing complete, security signed off |
| Premium Bonds Parallel-Run | Premium Bonds on parallel-run | Q2 2028 | All other products migrated |
| Premium Bonds Migration | Premium Bonds fully on SBS | H2 2028 | Extended parallel-run, draw validation |
| Atos Exit Complete | Contractual close-out, decommissioning | H1 2029 | All migrations complete |

---

## Budget

### Cost Estimate

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| SBS Platform Licensing & Services | TBD (subject to contract) | SBP Digital Core licensing, professional services |
| Cloud Infrastructure (3 years) | TBD | UK sovereign cloud hosting, DR region |
| Data Migration & Tooling | TBD | ETL tooling, reconciliation engine, testing |
| Integration Development | TBD | Payment rails, HMRC, identity, monitoring |
| Security & Compliance | TBD | Pen testing, PCI QSA, NCSC assessment |
| Atos Exit Costs | TBD (subject to contract) | Transition support, KT programme, decommissioning |
| NS&I Permanent Staff (recruitment) | TBD | Recruitment fees, onboarding, training |
| Consultants / SI (reducing) | TBD | Outcome-based contracts, knowledge transfer |
| Testing (performance, security, UAT) | TBD | Test environments, tooling, personnel |
| Contingency (20% novel, 10% established) | TBD | Per Principle P4 |
| **Total** | **TBD — subject to BR-1 cost baseline** | Independent validation required |

> **Note**: Budget figures are TBD pending completion of BR-1 (cost baseline establishment). This is deliberate — the PAC found NS&I had "no idea of the eventual cost". Providing unvalidated estimates would undermine credibility. The cost baseline exercise (Goal G-1) will populate these figures within 90 days.

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| NS&I CEO | Programme Sponsor | PENDING | — | |
| NS&I CTO | Technology Direction | PENDING | — | |
| NS&I CFO | Financial Oversight | PENDING | — | |
| NS&I CISO | Security Approval | PENDING | — | |
| NS&I Operations Director | Service Continuity | PENDING | — | |
| NS&I Chief Architect | Architecture Review | PENDING | — | |
| HM Treasury Sponsor | Funding Oversight | PENDING | — | |
| SBS Delivery Lead | Platform Delivery | PENDING | — | |
| Atos Transition Lead | Legacy Exit | PENDING | — | |

### Sign-Off

By signing below, stakeholders confirm that requirements are complete, understood, and approved to proceed to design phase.

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| NS&I CEO (Programme Sponsor) | _________ | |
| NS&I CTO (Technology Direction) | _________ | |
| HM Treasury Sponsor (Funding Oversight) | _________ | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| **Atos** | Incumbent outsourcing partner operating NS&I core banking since 1999 |
| **BACS** | Bankers' Automated Clearing Services — UK payment scheme for direct debits and credits |
| **CAF** | NCSC Cyber Assessment Framework |
| **CDE** | Cardholder Data Environment (PCI DSS scope) |
| **CHAPS** | Clearing House Automated Payment System — UK same-day high-value payments |
| **Dual-Run** | Period where both Atos and SBS platforms operate simultaneously |
| **EVM** | Earned Value Management — cost and schedule performance measurement |
| **Faster Payments** | UK real-time payment scheme |
| **FCA** | Financial Conduct Authority |
| **IPA** | Infrastructure and Projects Authority |
| **KT** | Knowledge Transfer |
| **NAO** | National Audit Office |
| **NCSC** | National Cyber Security Centre |
| **PAC** | Public Accounts Committee |
| **PCI DSS** | Payment Card Industry Data Security Standard |
| **PRA** | Prudential Regulation Authority |
| **SBS** | Sopra Banking Software (formerly known as Sopra Banking Software) |
| **SBP Digital Core** | SBS's cloud-native core banking platform |
| **SS1/21** | PRA Supervisory Statement on Operational Resilience |

### Appendix B: Reference Documents

| Document | ID | Purpose |
|----------|----|---------|
| Architecture Principles | ARC-000-PRIN-v1.0 | Technology standards and constraints |
| Stakeholder Drivers & Goals | ARC-001-STKE-v1.0 | Stakeholder analysis, goals, outcomes, conflicts |
| Risk Register | Not yet created | Recommend `/arckit:risk` |
| Strategic Outline Business Case | Not yet created | Recommend `/arckit:sobc` |

### Appendix C: Requirements Traceability Summary

| Requirement | Stakeholder Driver | Goal | Outcome | Principle |
|-------------|--------------------|------|---------|-----------|
| BR-1 | SD-1, SD-2, SD-7, SD-11 | G-1 | O-1 | P4 |
| BR-2 | SD-5, SD-10, SD-12 | G-2 | O-2 | P3 |
| BR-3 | SD-6, SD-12, SD-14 | G-7 | O-4 | P2, P10 |
| BR-4 | SD-2, SD-3, SD-4, SD-15 | G-3 | O-3 | P5 |
| BR-5 | SD-5, SD-8, SD-4 | G-5 | O-5 | P7 |
| BR-6 | SD-4, SD-6, SD-9, SD-14 | G-4 | O-2 | P1 |
| BR-7 | SD-2, SD-3, SD-11, SD-13 | G-6 | O-1 | P4 |
| BR-8 | SD-2, SD-7, SD-15 | G-8 | O-3 | P5 |
| FR-1 to FR-4 | SD-4, SD-9, SD-10 | G-4 | O-2 | P1, P6 |
| FR-5 | SD-6, SD-12 | G-7 | O-4 | P10 |
| FR-7, FR-8 | SD-5, SD-8 | G-2, G-5 | O-2, O-5 | P3 |
| FR-9 | SD-2, SD-11 | G-6, G-7 | O-1, O-4 | P8 |
| FR-10 | SD-8, SD-4 | G-5 | O-5 | P5 |
| NFR-P-1 to P-4 | SD-5, SD-10 | G-2 | O-2 | P1 |
| NFR-A-1 to A-3 | SD-5, SD-10, SD-12 | G-2 | O-2 | P3 |
| NFR-SEC-1 to SEC-6 | SD-6, SD-12 | G-7 | O-4 | P2 |
| NFR-C-1 to C-5 | SD-6, SD-12 | G-7 | O-4 | P2, P10 |
| NFR-I-1 to I-2 | SD-14 | G-4 | O-2 | P6, P7 |
| NFR-M-1 to M-3 | SD-4, SD-5 | G-4, G-2 | O-2 | P8, P9 |
| INT-1 | SD-5, SD-8 | G-5, G-2 | O-5, O-2 | P7 |
| INT-2 to INT-3 | SD-5, SD-10 | G-2 | O-2 | P6 |
| DR-1 to DR-6 | SD-5, SD-6, SD-10 | G-2, G-7 | O-2, O-4 | P2 |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| *None provided* | — | — | — | — |

> External documents (RFP/ITT documents, legacy system specifications, user research reports) can be placed in `projects/001-core-banking-migration/external/` to enhance future revisions.

---

**Generated by**: ArcKit `/arckit:requirements` command
**Generated on**: 2026-02-13
**ArcKit Version**: 2.4.4
**Project**: NS&I Core Banking Migration (Project 001)
**AI Model**: Claude Opus 4.6
**Generation Context**: Generated from ARC-001-STKE-v1.0 (Stakeholder Drivers) and ARC-000-PRIN-v1.0 (Architecture Principles). No risk register, SOBC, or external documents available.
