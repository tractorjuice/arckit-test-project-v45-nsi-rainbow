# Stakeholder Drivers & Goals Analysis: NS&I Core Banking Migration

> **Template Status**: Live | **Version**: 2.4.4 | **Command**: `/arckit:stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | NS&I Core Banking Migration (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2026-02-13 |
| **Last Modified** | 2026-02-13 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-03-13 |
| **Owner** | NS&I Programme Director, Core Banking |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NS&I Digital Programme Board, HM Treasury Sponsor Team, IPA Review Team, SBS Delivery Lead |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-13 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |
| 1.1 | 2026-02-13 | ArcKit AI | Updated with PAC report (13 Feb 2026) and NAO report (14 Nov 2025) specifics: named individuals (Dax Harkins, Matt Smith, David Goldstone), vendor ecosystem, staff transfers, Atos contract extension details, PAC recommendations | PENDING | PENDING |

---

## Executive Summary

### Purpose
This document identifies all stakeholders with power or interest in the NS&I Core Banking Migration — the replacement of the 27-year-old Atos legacy core banking platform with SBS (Sopra Banking Software) SBP Digital Core. For each stakeholder, it documents their underlying drivers (motivations, fears, pressures), maps these to measurable SMART goals, and defines the business outcomes that prove success. The analysis provides full traceability from individual stakeholder concerns through to programme KPIs.

### Key Findings
The Core Banking Migration has an unusually complex stakeholder landscape driven by three reinforcing dynamics: (1) intense parliamentary and public scrutiny following the PAC's "full-spectrum disaster" assessment; (2) a technically unprecedented migration of 24 million customer accounts from a 27-year-old monolithic platform to a cloud-native alternative with zero tolerance for service disruption; and (3) a trust deficit between NS&I, HM Treasury, Parliament, and the public that means every decision will be questioned. The dominant tension is between **speed** (Treasury and PAC want results after five years of limited progress) and **safety** (Operations, Security, and Regulators demand zero-risk migration for 24 million customers and £230 billion in savings). A secondary conflict exists between **vendor dependency reduction** (a core programme driver) and the practical reality that SBS becomes the new critical vendor.

### Critical Success Factors
- **CSF-1**: Uninterrupted service to 24 million customers throughout the migration, including Premium Bonds prize draw continuity
- **CSF-2**: Transparent, evidence-based cost reporting that satisfies PAC, NAO, and Treasury requirements
- **CSF-3**: Successful parallel-run of Atos and SBS platforms with automated data reconciliation proving zero data loss
- **CSF-4**: Demonstrable build-up of NS&I in-house technical capability (minimum 30% permanent staff on programme)
- **CSF-5**: Development of a realistic, bottom-up integrated delivery plan with credible timelines and costs — the PAC (13 Feb 2026) explicitly recommended NS&I **stop targeting March 2028** and instead build a plan from the ground up rather than reverse-engineering around optimistic dates

### Stakeholder Alignment Score
**Overall Alignment**: MEDIUM

While all stakeholders share the overarching goal of replacing the legacy platform, significant tensions exist on pace, cost, risk appetite, and accountability. The PAC scrutiny creates pressure for speed that conflicts with the methodical approach required for a safe migration. Atos (as incumbent) and SBS (as successor) have competing commercial interests during the dual-running period. Internal NS&I stakeholders are navigating between a mandate for change and a culture that the PAC described as "good news" oriented. Resolving these tensions requires explicit governance, honest reporting, and phased delivery that demonstrates early wins without compromising safety.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Dax Harkins (NS&I Chief Executive) | Executive Agency Head | HIGH | HIGH | Programme board chair, monthly 1:1 with Treasury sponsor |
| NS&I Chief Technology Officer | Technology Leadership | HIGH | HIGH | Architecture review authority, weekly steering |
| NS&I Chief Finance Officer | Finance & Budgets | HIGH | HIGH | Monthly cost assurance, EVM reporting |
| Matt Smith (Programme SRO) | Senior Responsible Owner | HIGH | HIGH | Programme board, Treasury reporting, PAC evidence |
| Programme Director (Core Banking) | Programme Delivery | HIGH | HIGH | Daily stand-ups, weekly steering, gate reviews |
| NS&I Chief Architect | Architecture & Design | MEDIUM | HIGH | Architecture review board, design authority |
| NS&I Chief Information Security Officer | Security & Compliance | HIGH | HIGH | Security gate reviews, threat modelling sign-off |
| NS&I Operations Director | Live Service Operations | HIGH | HIGH | Dual-run planning, cutover rehearsal authority |
| NS&I Data Protection Officer | Data Protection & GDPR | MEDIUM | HIGH | DPIA reviews, data migration sign-off |
| NS&I Customer Services Director | Customer Experience | MEDIUM | HIGH | Customer communication plan, testing scenarios |
| NS&I HR Director | People & Capability | MEDIUM | MEDIUM | Skills strategy, recruitment, knowledge transfer |
| NS&I Internal Audit | Governance & Assurance | HIGH | MEDIUM | Quarterly audits, control effectiveness reviews |
| NS&I Product Owners (Savings Products) | Business Requirements | MEDIUM | HIGH | Product-by-product migration requirements |
| NS&I Delivery Teams (Engineering) | Build & Test | LOW | HIGH | Sprint ceremonies, technical decisions |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| HM Treasury Sponsor Team | HM Treasury | Sponsoring department | HIGH | HIGH |
| David Goldstone (HMT Advisor) | HM Treasury | Programme oversight advisor (appointed Dec 2025) | HIGH | HIGH |
| Public Accounts Committee (PAC) | Parliament | Parliamentary scrutiny | HIGH | HIGH |
| National Audit Office (NAO) | Independent auditor | Audit & assurance | HIGH | HIGH |
| Geoffrey Clifton-Brown MP | PAC Chair | Political accountability | HIGH | HIGH |
| Infrastructure & Projects Authority (IPA) | Cabinet Office | Programme assurance | HIGH | MEDIUM |
| Atos (UK & Ireland) | Incumbent vendor | Legacy platform operator | HIGH | HIGH |
| SBS (Sopra Banking Software) | New platform vendor | SBP Digital Core delivery | HIGH | HIGH |
| PA Consulting | Consultancy | Recovery plan authors (commissioned July 2024) | MEDIUM | HIGH |
| Capgemini | Consultancy / SI | Delivery partner | MEDIUM | HIGH |
| EY | Consultancy | Advisory services | MEDIUM | HIGH |
| IBM | Technology / SI | Technology delivery | MEDIUM | HIGH |
| Sopra Steria | Technology / SI | Delivery partner (related to SBS parent group) | MEDIUM | HIGH |
| Actica Consulting | Consultancy | Specialist advisory | LOW | HIGH |
| NS&I Customers (24 million) | Public | End users / beneficiaries | LOW | HIGH |
| UK Taxpayers (via Parliament) | Public | Funders | LOW | MEDIUM |
| Financial Conduct Authority (FCA) | Regulator | Consumer protection | HIGH | MEDIUM |
| Prudential Regulation Authority (PRA) | Regulator | Operational resilience | HIGH | MEDIUM |
| Information Commissioner's Office (ICO) | Regulator | Data protection | MEDIUM | MEDIUM |
| National Cyber Security Centre (NCSC) | GCHQ | Cyber security standards | HIGH | MEDIUM |
| Crown Commercial Service (CCS) | Cabinet Office | Procurement compliance | MEDIUM | LOW |

### Stakeholder Power-Interest Grid

```
                              INTEREST
                  Low                         High
            ┌─────────────────────┬─────────────────────┐
            │                     │                     │
            │   KEEP SATISFIED    │   MANAGE CLOSELY    │
            │                     │                     │
   High     │  • FCA              │  • Dax Harkins (CEO)│
            │  • PRA              │  • NS&I CTO         │
            │  • NCSC             │  • NS&I CFO         │
            │  • IPA              │  • Matt Smith (SRO) │
            │  • Internal Audit   │  • Programme Dir.    │
            │                     │  • HM Treasury      │
            │                     │  • D. Goldstone (HMT)│
            │                     │  • PAC / NAO        │
   P        │                     │  • CISO             │
   O        │                     │  • Ops Director     │
   W        │                     │  • Atos             │
            │                     │  • SBS              │
   E        ├─────────────────────┼─────────────────────┤
   R        │                     │                     │
            │      MONITOR        │    KEEP INFORMED    │
            │                     │                     │
   Low      │  • CCS              │  • NS&I Customers   │
            │  • UK Taxpayers     │  • Customer Svcs Dir│
            │                     │  • Product Owners   │
            │                     │  • Delivery Teams   │
            │                     │  • DPO              │
            │                     │  • HR Director      │
            │                     │  • PA Consulting    │
            │                     │  • Capgemini / EY   │
            │                     │                     │
            └─────────────────────┴─────────────────────┘
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| Dax Harkins (NS&I CEO) | HIGH | HIGH | Manage Closely | Weekly programme board, monthly Treasury liaison |
| Matt Smith (Programme SRO) | HIGH | HIGH | Manage Closely | Programme board, Treasury reporting, PAC evidence sessions |
| David Goldstone (HMT Advisor) | HIGH | HIGH | Manage Closely | Monthly programme reviews, cost assurance, Treasury reporting |
| NS&I CTO | HIGH | HIGH | Manage Closely | Weekly steering, architecture review board chair |
| NS&I CFO | HIGH | HIGH | Manage Closely | Monthly EVM reviews, cost assurance gates |
| Programme Director | HIGH | HIGH | Manage Closely | Daily stand-ups, weekly steering, gate owner |
| NS&I CISO | HIGH | HIGH | Manage Closely | Security design reviews, penetration test sign-off |
| NS&I Operations Director | HIGH | HIGH | Manage Closely | Dual-run planning, cutover rehearsal authority |
| HM Treasury Sponsor | HIGH | HIGH | Manage Closely | Monthly progress reports, quarterly deep-dives |
| PAC / Geoffrey Clifton-Brown MP | HIGH | HIGH | Manage Closely | Formal evidence sessions, written submissions |
| NAO | HIGH | HIGH | Manage Closely | Audit access, evidence pack maintenance |
| Atos | HIGH | HIGH | Manage Closely | Joint steering committee, SLA management, exit planning |
| SBS | HIGH | HIGH | Manage Closely | Joint delivery governance, contract milestones |
| FCA | HIGH | MEDIUM | Keep Satisfied | Regulatory notification, compliance evidence |
| PRA | HIGH | MEDIUM | Keep Satisfied | Operational resilience submissions |
| NCSC | HIGH | MEDIUM | Keep Satisfied | IT Health Check submissions, CAF self-assessment |
| IPA | HIGH | MEDIUM | Keep Satisfied | Quarterly delivery confidence reviews |
| Internal Audit | HIGH | MEDIUM | Keep Satisfied | Quarterly audit programme, control reviews |
| NS&I Customers (24M) | LOW | HIGH | Keep Informed | GOV.UK updates, Premium Bonds comms, service alerts |
| Customer Services Director | MEDIUM | HIGH | Keep Informed | Customer impact assessments, comms planning |
| Product Owners | MEDIUM | HIGH | Keep Informed | Sprint reviews, product migration workshops |
| DPO | MEDIUM | HIGH | Keep Informed | DPIA reviews, data migration governance |
| HR Director | MEDIUM | MEDIUM | Keep Informed | Skills assessment updates, recruitment progress |
| Delivery Teams | LOW | HIGH | Keep Informed | Sprint ceremonies, technical brown bags |
| PA Consulting | MEDIUM | HIGH | Keep Informed | Recovery plan delivery, knowledge transfer milestones |
| Capgemini / EY / IBM / Sopra Steria | MEDIUM | HIGH | Keep Informed | Delivery milestones, knowledge transfer checkpoints |
| CCS | MEDIUM | LOW | Monitor | Procurement compliance checks at contract events |
| UK Taxpayers | LOW | MEDIUM | Monitor | NAO reports, PAC publications |

**Quadrant Interpretation:**
- **Manage Closely** (High Power, High Interest): Key decision-makers requiring active engagement — this is an unusually large group given the programme's political profile
- **Keep Satisfied** (High Power, Low Interest): Regulators and assurance bodies who intervene only when standards are not met
- **Keep Informed** (Low Power, High Interest): Operational stakeholders and customers who experience the impact of decisions
- **Monitor** (Low Power, Low Interest): Oversight bodies engaged only at procurement or audit events

---

## Stakeholder Drivers Analysis

### SD-1: HM Treasury — Cost Control and Value for Money

**Stakeholder**: HM Treasury Sponsor Team

**Driver Category**: FINANCIAL / RISK

**Driver Statement**: Contain programme costs within the approved funding envelope, demonstrate value for money for the additional £109m funding, and prevent further cost escalation that would require Ministerial and parliamentary approval.

**Context & Background**:
The programme has already cost an estimated £3bn by end of 2024, with costs increasing by £1.3bn since inception. HM Treasury confirmed £109m in additional funding in January 2026 (pending parliamentary approval). Treasury was criticised by the PAC for not intervening earlier after serious setbacks. The Treasury sponsor team is under pressure to demonstrate they are now exercising effective oversight. Any further cost overrun would trigger a Ministerial Direction or programme cancellation review.

**Driver Intensity**: CRITICAL

**Enablers**:
- Monthly Earned Value Management (EVM) reporting with variance analysis
- Independent cost assurance at each programme gate
- Fixed-price elements in the SBS contract where feasible
- Early warning triggers at 5% and 10% cost variance thresholds

**Blockers**:
- Scope creep driven by undiscovered legacy complexity
- SBS contract variations for requirements not anticipated at contract award
- Extended dual-running period increasing parallel operating costs
- Consultant costs continuing without clear deliverables

**Related Stakeholders**: NS&I CFO (aligned), PAC/NAO (aligned on scrutiny), SBS (potential conflict on contract variations)

---

### SD-2: Public Accounts Committee — Accountability and Transparency

**Stakeholder**: PAC / Geoffrey Clifton-Brown MP (Chair)

**Driver Category**: RISK / COMPLIANCE

**Driver Statement**: Ensure NS&I can demonstrate a credible, costed plan for completing the core banking migration, with honest reporting on progress, risks, and costs, and clear accountability for decisions and spend.

**Context & Background**:
The PAC's February 2026 report (published 13 February 2026) described the programme as a "full-spectrum disaster". PAC Chair Sir Geoffrey Clifton-Brown stated: *"It is perhaps unsurprising that this upbeat name [Project Rainbow] was retired as aptly our report finds it has been a full-spectrum disaster"* and warned that *"the taxpayer is at serious risk of throwing good money after bad"*. Specific findings: NS&I has "no workable plan" after five years; NS&I "lacks the skills" to deliver; NS&I has "no idea of the eventual cost"; NS&I was "bullishly confident" despite poor delivery record; a "good news culture" prevents honest reporting; and £43m was spent on consultants with NS&I "vague on how it holds them to account". The PAC made six overarching recommendations including: (1) stop targeting March 2028 and develop a realistic bottom-up integrated plan; (2) within six months submit a resource management strategy including consultant use; (3) improve supplier and contract management for the multi-supplier model; and (4) Treasury must clarify how it will assess the integrated plan and what lessons it has learned. NS&I must respond to these recommendations within 60 days. The Bank of England's Real-Time Gross Settlement (RTGS) system replacement — delivered for £431 million on schedule — was cited as an unfavourable benchmark. Future evidence sessions are expected as the programme progresses.

**Driver Intensity**: CRITICAL

**Enablers**:
- Transparent, evidence-based progress reporting
- Clear cost baseline with assumptions documented
- Demonstrable skills build-up within NS&I
- Honest risk reporting (no "good news" filtering)

**Blockers**:
- Cultural resistance to admitting problems or delays
- Complexity of legacy systems making accurate cost estimation difficult
- Consultant firms resisting accountability mechanisms
- NS&I leadership defensiveness about past decisions

**Related Stakeholders**: NAO (aligned — provides evidence to PAC), HM Treasury (aligned on oversight), NS&I CEO (tension — must respond to criticism whilst delivering)

---

### SD-3: NS&I Chief Executive — Programme Delivery and Organisational Reputation

**Stakeholder**: NS&I Chief Executive

**Driver Category**: STRATEGIC / PERSONAL / RISK

**Driver Statement**: Deliver the core banking migration successfully to restore NS&I's credibility with Treasury, Parliament, and the public, while demonstrating that the organisation has the capability and governance to manage complex technology programmes.

**Context & Background**:
The CEO bears ultimate accountability for the programme as head of the executive agency. The PAC's findings represent a severe reputational blow. The CEO must balance responding to parliamentary criticism with maintaining team morale and delivery momentum. There is a personal career dimension: failure to turn the programme around could result in replacement. Success would demonstrate government agencies can deliver complex technology transformation.

**Driver Intensity**: CRITICAL

**Enablers**:
- Strong Programme Director with authority to make decisions
- Rebuilt relationship with Treasury based on honest reporting
- Early visible wins (e.g., successful migration of a low-risk product)
- Culture change programme addressing "good news" bias

**Blockers**:
- Inherited programme debt (decisions made before current leadership)
- PAC scrutiny creating defensive behaviours
- Difficulty recruiting top technical talent into government pay scales
- Atos contractual complexities during exit/transition

**Related Stakeholders**: HM Treasury (accountability relationship), PAC (scrutiny relationship), NS&I CTO (delivery partnership)

---

### SD-4: NS&I Chief Technology Officer — Technical Excellence and Modernisation

**Stakeholder**: NS&I CTO

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Deliver a modern, cloud-native core banking platform that positions NS&I for the next 20+ years, while building a capable in-house technology team that reduces dependency on external consultants.

**Context & Background**:
The CTO must replace a 27-year-old monolithic platform with a modern cloud-native alternative. This is the most technically complex element of the programme — classified as "extremely high-risk" by the PAC. The CTO must also address the skills gap identified by the PAC, building an internal team capable of being an intelligent client to SBS and other vendors. The tension between speed of delivery and architectural quality is acute.

**Driver Intensity**: CRITICAL

**Enablers**:
- SBS SBP Digital Core platform maturity and UK deployment readiness
- Architecture principles established (ARC-000-PRIN-v1.0)
- Ability to recruit experienced banking technology leaders
- Cloud infrastructure already available (UK sovereign regions)

**Blockers**:
- Legacy platform complexity not fully documented
- SBS platform may require significant customisation for NS&I products
- Government pay scales limiting recruitment of senior technologists
- Pressure for speed conflicting with thorough architecture

**Related Stakeholders**: Chief Architect (delivery partnership), SBS (technical partnership), Atos (legacy knowledge dependency)

---

### SD-5: NS&I Operations Director — Service Continuity During Migration

**Stakeholder**: NS&I Operations Director

**Driver Category**: OPERATIONAL / RISK

**Driver Statement**: Maintain 99.95% uptime for all customer-facing services and zero disruption to the Premium Bonds prize draw throughout the entire migration period, including the dual-running phase and cutover.

**Context & Background**:
NS&I serves 24 million customers managing £230 billion in savings. Any service disruption would be national news, damage public trust in government-backed savings, and trigger immediate parliamentary questions. The Premium Bonds monthly prize draw is NS&I's most high-profile operation — any failure would be catastrophic reputationally. The Operations Director must plan for a dual-running period where both Atos legacy and SBS platforms operate simultaneously, with data synchronisation between them.

**Driver Intensity**: CRITICAL

**Enablers**:
- Extended parallel-run period (minimum 6 months for core products)
- Automated data reconciliation between Atos and SBS platforms
- Comprehensive cutover rehearsals (minimum 3 full rehearsals before go-live)
- Rollback capability at every migration stage

**Blockers**:
- Legacy system documentation gaps
- Atos knowledge holders leaving or being redeployed during transition
- Complexity of synchronising real-time financial transactions between platforms
- Testing environments that do not accurately reflect production scale

**Related Stakeholders**: NS&I Customers (directly impacted), Customer Services Director (frontline), Atos (legacy operations), SBS (new platform readiness)

---

### SD-6: NS&I CISO — Security Posture During Transformation

**Stakeholder**: NS&I Chief Information Security Officer

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure the migration maintains or improves NS&I's security posture throughout the transition, with no security incidents, continuous compliance with NCSC CAF and PCI DSS, and the new platform achieving security accreditation before go-live.

**Context & Background**:
The migration period is a period of elevated security risk. Two platforms running simultaneously means double the attack surface. Data migration between platforms creates temporary exposure. New cloud-native infrastructure requires different security controls than the legacy on-premises environment. The CISO must satisfy NCSC, PCI DSS, and government security classification requirements simultaneously.

**Driver Intensity**: HIGH

**Enablers**:
- Security architecture designed into SBS platform from the outset
- NCSC engagement on cloud security patterns
- Automated security scanning in CI/CD pipelines (Compliance as Code — Principle P10)
- Dedicated security testing budget and timeline

**Blockers**:
- Dual-platform attack surface during transition
- Data in transit between Atos and SBS environments
- Legacy platform security posture degrading as Atos transitions out
- Shortage of security professionals with banking and government experience

**Related Stakeholders**: NCSC (standards), PRA (operational resilience), FCA (customer data protection), DPO (GDPR)

---

### SD-7: NS&I CFO — Budget Control and Financial Accountability

**Stakeholder**: NS&I Chief Finance Officer

**Driver Category**: FINANCIAL / COMPLIANCE

**Driver Statement**: Establish a credible cost baseline for the core banking migration, implement Earned Value Management reporting, and demonstrate to Treasury and NAO that every pound spent delivers measurable progress toward go-live.

**Context & Background**:
The PAC found NS&I was "unable to tell the PAC how much had been spent" to date and had "no idea of the eventual cost". The CFO must rebuild financial credibility. The additional £109m funding has explicit conditions. The NAO will be tracking spend against outcomes. The £43m spent on consultants without clear accountability has created particular sensitivity around advisory and professional services expenditure.

**Driver Intensity**: CRITICAL

**Enablers**:
- Granular work breakdown structure with cost accounts
- Independent cost assurance at each gate
- Fixed-price milestones in SBS and SI contracts where feasible
- Real-time financial dashboard accessible to Treasury

**Blockers**:
- Historical cost data is incomplete or inconsistent
- Sunk costs creating political pressure to continue regardless of VfM
- Difficulty in accurately costing legacy system decommissioning
- Consultant contracts structured as time-and-materials without caps

**Related Stakeholders**: HM Treasury (aligned), NAO (audit), PAC (scrutiny), Programme Director (delivery cost accountability)

---

### SD-8: Atos — Managed Exit and Contractual Obligations

**Stakeholder**: Atos (UK & Ireland)

**Driver Category**: FINANCIAL / OPERATIONAL / RISK

**Driver Statement**: Execute a commercially acceptable exit from the NS&I outsourcing contract, fulfil knowledge transfer obligations, maintain service levels during the transition period, and protect Atos's reputation as a responsible transition partner.

**Context & Background**:
Atos has operated NS&I's core banking and back-office operations since 1999 — a 27-year relationship. The company is also navigating its own financial restructuring. The original contract (awarded 2014, due to expire 2021) has been extended twice — first to 2024, then to March 2028 — both **without competitive bidding**, at an additional value of **£474.4 million** (NAO, November 2025). The NAO estimates the Atos extension to cover unfilled successor contracts costs approximately **£530 million**. In 2025, **750 customer service agents** and **350 back-office staff** were transferred from Atos to a new supplier, but core banking operations remain with Atos. Atos must maintain service levels during the transition period while simultaneously supporting knowledge transfer to NS&I and SBS. There is an inherent tension: Atos has deep institutional knowledge that NS&I needs, but Atos's commercial incentive diminishes as the exit approaches. Key personnel may leave or be redeployed. Of the five successor contracts originally planned to replace the Atos deal, the NAO found that two were awarded as planned, one procurement initially failed and was re-run, one was awarded but subsequently terminated, and one was abandoned due to disagreement on terms.

**Driver Intensity**: HIGH

**Enablers**:
- Clear exit plan with defined milestones and service levels
- Contractual incentives for knowledge transfer quality
- Retention packages for key Atos personnel during transition
- Joint governance committee for transition issues

**Blockers**:
- Atos financial pressures potentially impacting service investment
- Key Atos staff seeking alternative employment as exit approaches
- Undocumented legacy system behaviours known only to Atos operators
- Potential contractual disputes over exit obligations and costs

**Related Stakeholders**: NS&I Operations Director (service levels), NS&I CTO (knowledge transfer), SBS (successor platform)

---

### SD-9: SBS (Sopra Banking Software) — Successful Platform Deployment

**Stakeholder**: SBS (Sopra Banking Software)

**Driver Category**: STRATEGIC / FINANCIAL / OPERATIONAL

**Driver Statement**: Deliver a successful SBP Digital Core deployment for NS&I that serves as a flagship UK government reference implementation, demonstrating the platform's capability for large-scale, regulated financial services in a sovereign cloud environment.

**Context & Background**:
The NS&I deployment is one of the largest and most high-profile banking platform migrations in the UK. Success would be a significant reference for SBS in the government and public sector banking market. Failure would be equally visible. SBS must deliver a platform capable of handling 24 million accounts, £230 billion in assets, and NS&I's unique product set (especially Premium Bonds). The 2028 target go-live is ambitious given the programme's history.

**Driver Intensity**: HIGH

**Enablers**:
- SBP Digital Core platform maturity for NS&I's product types
- UK cloud region availability (sovereign deployment)
- NS&I committing to standard platform configuration where possible
- Adequate time for integration testing and parallel-run

**Blockers**:
- NS&I products requiring significant platform customisation
- Scope creep from late-discovered legacy requirements
- NS&I's internal decision-making delays
- Regulatory requirements unique to NS&I as a government-backed entity

**Related Stakeholders**: NS&I CTO (technical partnership), NS&I Chief Architect (design decisions), Atos (data migration source)

---

### SD-10: NS&I Customers — Uninterrupted Service and Improved Experience

**Stakeholder**: NS&I Customers (24 million)

**Driver Category**: CUSTOMER / RISK

**Driver Statement**: Continue to access savings products, manage accounts, and receive Premium Bonds prizes without disruption, while benefiting from improved digital services once the migration is complete.

**Context & Background**:
NS&I customers include a broad demographic, from digitally confident younger savers to elderly customers who rely on telephone and postal services. Many hold Premium Bonds (NS&I's flagship product) and expect the monthly prize draw to operate flawlessly. Customer trust in NS&I is high because it is government-backed — any service failure would disproportionately damage that trust. Customers are largely unaware of the technical migration happening behind the scenes, and that is the desired state.

**Driver Intensity**: HIGH

**Enablers**:
- Transparent customer communication for any changes to service
- Comprehensive regression testing of all customer journeys
- Phased migration starting with lowest-risk products
- Enhanced digital services available post-migration as a tangible benefit

**Blockers**:
- Migration causing temporary service degradation
- Data migration errors affecting account balances or transaction history
- Channel disruptions (web, phone, post) during cutover
- Poor communication about changes to familiar interfaces

**Related Stakeholders**: Customer Services Director (frontline support), Operations Director (service levels), Product Owners (product functionality)

---

### SD-11: National Audit Office — Audit Assurance and Evidence

**Stakeholder**: NAO

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Obtain sufficient audit evidence that the core banking migration is being delivered with appropriate governance, cost control, and risk management, and that the additional £109m funding is being spent effectively.

**Context & Background**:
The NAO provides independent audit evidence to the PAC. The NAO's previous assessment contributed to the PAC's "full-spectrum disaster" finding. The NAO will continue to monitor the programme and is likely to produce a follow-up report. The NAO needs access to accurate cost data, risk registers, governance records, and delivery evidence. They will assess whether NS&I has addressed the PAC's recommendations.

**Driver Intensity**: HIGH

**Enablers**:
- Open-book access to programme data, costs, and decisions
- Well-maintained programme documentation and decision logs
- Regular self-assessment against PAC recommendations
- Honest risk reporting with evidence of mitigating actions

**Blockers**:
- Incomplete historical records
- "Good news" culture filtering information before it reaches auditors
- Programme complexity making it difficult to assess true progress
- Staff turnover losing institutional knowledge of decisions

**Related Stakeholders**: PAC (consumes NAO evidence), HM Treasury (audit relationship), NS&I Internal Audit (aligned)

---

### SD-12: FCA / PRA — Regulatory Compliance and Operational Resilience

**Stakeholder**: Financial Conduct Authority / Prudential Regulation Authority

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure the core banking migration does not compromise consumer protection, financial stability, or operational resilience requirements, and that the new platform meets all regulatory standards before NS&I customers are migrated to it.

**Context & Background**:
Although NS&I is government-backed and not a bank in the traditional sense, it operates within the financial services regulatory perimeter for customer protection. The PRA's Supervisory Statement SS1/21 on operational resilience sets expectations for important business services to remain within impact tolerances. The FCA expects firms to ensure continuity of service and protection of customer data during technology changes. A failed migration affecting 24 million customers would be a systemic event.

**Driver Intensity**: HIGH

**Enablers**:
- Regulatory engagement early in the migration planning
- Operational resilience self-assessment aligned with SS1/21
- Customer impact assessment for each migration phase
- Regulatory notification protocol for material changes

**Blockers**:
- Regulatory requirements evolving during the multi-year migration
- Dual-running period creating complexity for regulatory reporting
- New platform requiring new regulatory reporting capabilities
- Resource constraints at regulators for dedicated NS&I oversight

**Related Stakeholders**: NS&I CISO (security compliance), NS&I DPO (data protection), NS&I Operations Director (resilience)

---

### SD-13: IPA — Programme Delivery Confidence

**Stakeholder**: Infrastructure & Projects Authority

**Driver Category**: RISK / COMPLIANCE

**Driver Statement**: Assess and report on the delivery confidence of the core banking migration programme, providing independent assurance to Cabinet Office and Treasury that appropriate controls, capabilities, and plans are in place.

**Context & Background**:
The IPA conducts delivery confidence assessments for major government programmes. The core banking migration is classified as a Government Major Project. The IPA's assessment directly influences Treasury funding decisions and Ministerial confidence. A RED or RED/AMBER rating would trigger intervention. The programme's history suggests the current rating is likely unfavourable, making improvement a priority.

**Driver Intensity**: MEDIUM

**Enablers**:
- Clear, evidence-based delivery plan with realistic milestones
- Demonstrated capability improvements (skills, governance, tools)
- Honest risk management with credible mitigations
- Previous IPA recommendations demonstrably addressed

**Blockers**:
- Programme history making assessors sceptical
- Difficulty demonstrating progress before SBS platform milestones
- IPA assessors unfamiliar with banking platform migration complexity
- Short assessment windows insufficient for complex programme evaluation

**Related Stakeholders**: HM Treasury (consumes IPA assessments), NS&I CEO (accountable), Programme Director (evidence provider)

---

### SD-14: NS&I Chief Architect — Architectural Integrity

**Stakeholder**: NS&I Chief Architect

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Ensure the SBS integration architecture adheres to established principles (modularity, vendor independence, observability, compliance as code), avoiding recreation of monolithic dependencies and enabling long-term platform evolution.

**Context & Background**:
The Chief Architect must ensure that the migration to SBS does not simply replace one monolithic dependency (Atos) with another (SBS). The architecture principles (ARC-000-PRIN-v1.0) established clear direction on cloud-native, modular, observable, and vendor-independent design. The practical challenge is balancing these aspirations with SBS's platform capabilities and NS&I's delivery timeline. Every customisation of the SBS platform increases cost, risk, and lock-in.

**Driver Intensity**: HIGH

**Enablers**:
- Architecture review board with authority to approve/reject designs
- Architecture principles document (ARC-000-PRIN-v1.0) as decision framework
- SBS platform extensibility through APIs rather than core customisation
- Independent architecture assurance at programme gates

**Blockers**:
- Pressure to customise SBS platform for legacy product behaviours
- Time pressure reducing architecture review thoroughness
- SBS proprietary components creating new vendor dependencies
- Legacy integration patterns being replicated out of familiarity

**Related Stakeholders**: NS&I CTO (architecture direction), SBS (platform architecture), Programme Director (delivery timeline)

---

### SD-15: David Goldstone (HM Treasury Advisor) — Programme Oversight and Recovery

**Stakeholder**: David Goldstone, HM Treasury Programme Advisor (appointed December 2025)

**Driver Category**: STRATEGIC / RISK / COMPLIANCE

**Driver Statement**: Provide independent Treasury-level oversight of programme delivery, cost control, and risk management, ensuring NS&I develops a credible recovery plan and that the additional £109M funding delivers measurable progress.

**Context & Background**:
David Goldstone was appointed by HM Treasury in December 2025 as a dedicated programme advisor — a direct response to the NAO's November 2025 finding that Treasury "found it challenging to understand the costs and progress being made". His appointment signals Treasury's escalation of direct intervention. Goldstone's role is to provide Treasury with an independent line of sight into programme reality, cutting through the "good news culture" the PAC identified. He is effectively Treasury's eyes and ears inside the programme. His assessments will directly influence whether Treasury approves further funding requests or triggers programme cancellation review.

**Driver Intensity**: HIGH

**Enablers**:
- Unfettered access to programme data, financials, and risk registers
- Direct reporting line to HM Treasury (independent of NS&I management)
- Authority to commission independent reviews and audits
- Access to IPA delivery confidence reviews

**Blockers**:
- NS&I "good news" culture filtering information before it reaches Goldstone
- Lack of reliable programme data (NS&I unable to explain total spending to PAC)
- Potential tension between advisory role and NS&I management authority
- Compressed timeline to demonstrate value before next Treasury review

**Related Stakeholders**: HM Treasury Sponsor Team (reporting line), Dax Harkins (NS&I CEO), Matt Smith (Programme SRO), PAC (ultimate accountability)

---

### SD-16: System Integrators / Consultants — Delivery and Accountability

**Stakeholder**: PA Consulting, Capgemini, EY, IBM, Sopra Steria, Actica Consulting

**Driver Category**: FINANCIAL / OPERATIONAL

**Driver Statement**: Deliver contracted programme milestones while demonstrating clear value for money and measurable knowledge transfer to NS&I permanent staff, operating under enhanced accountability frameworks in response to PAC criticism of the £43m consultant spend.

**Context & Background**:
The PAC found NS&I was "vague on how it holds [consultants] to account" despite spending £43m on external advisory services. The NAO identified six named consultancies involved in the programme: **PA Consulting** (commissioned July 2024 for the programme recovery plan), **Capgemini**, **EY**, **IBM**, **Sopra Steria**, and **Actica Consulting**. Going forward, all consultant engagements must have defined deliverables (not just time-and-materials), measurable knowledge transfer outcomes, and clear accountability. The PAC recommended that within **six months** NS&I must submit a resource management strategy including consultant use. The consultant community has a reputational interest in the programme succeeding — but also a commercial interest in extended engagements. PA Consulting's recovery plan (commissioned July 2024) is the basis for the current programme reset.

**Driver Intensity**: MEDIUM

**Enablers**:
- Outcome-based contracts with defined deliverables and milestones
- Knowledge transfer requirements with measurable success criteria
- Paired working model (consultant + NS&I permanent staff)
- Regular value-for-money reviews

**Blockers**:
- Shift from time-and-materials to outcome-based contracts reducing flexibility
- Knowledge transfer competing with delivery deadlines
- Consultant retention when accountability scrutiny increases
- NS&I lacking in-house capability to properly define deliverables

**Related Stakeholders**: NS&I HR Director (skills transfer), NS&I CFO (cost accountability), PAC (scrutiny)

---

## Driver-to-Goal Mapping

### Goal G-1: Establish Credible Programme Cost Baseline

**Derived From Drivers**: SD-1, SD-2, SD-7, SD-11

**Goal Owner**: NS&I CFO

**Goal Statement**: Establish an independently validated, comprehensive cost baseline for the core banking migration within 90 days, including all work packages, contingency allocations, and assumptions, and maintain monthly cost reporting with less than 5% variance from forecast.

**Why This Matters**: The PAC found NS&I had "no idea of the eventual cost". Without a credible cost baseline, Treasury cannot assure Parliament that funding is adequate, and programme decisions cannot be made on an informed basis. This goal directly addresses the most damaging PAC finding.

**Success Metrics**:
- **Primary Metric**: Independent cost assurance validation within 90 days of programme reset
- **Secondary Metrics**:
  - Monthly cost variance less than 5% against forecast
  - 100% of work packages with allocated budget envelopes
  - Quarterly NAO confirmation of cost reporting adequacy

**Baseline**: No validated programme cost baseline exists (PAC finding)

**Target**: Complete cost baseline validated by IPA-approved independent assurer, with monthly EVM reporting operational

**Measurement Method**: Independent cost assurance review (external firm appointed by Treasury), monthly EVM reports reviewed by CFO and Treasury sponsor

**Dependencies**:
- Complete work breakdown structure for all migration workstreams
- SBS contract details finalised with pricing for all phases
- Atos exit costs quantified and agreed
- Consultant cost data consolidated from all engagement managers

**Risks to Achievement**:
- Legacy system complexity making accurate estimation impossible without detailed discovery
- SBS contract variations not yet identified inflating estimates mid-programme
- Political pressure to present optimistic figures undermining credibility

---

### Goal G-2: Achieve Zero Customer-Impacting Incidents During Migration

**Derived From Drivers**: SD-5, SD-10, SD-12

**Goal Owner**: NS&I Operations Director

**Goal Statement**: Complete the entire core banking migration — including parallel-run, data migration, and cutover — with zero P1 or P2 customer-impacting incidents and maintenance of 99.95% uptime for all customer-facing services.

**Why This Matters**: NS&I's 24 million customers must not be affected by the behind-the-scenes technology change. Any service disruption would be national news, erode public trust, trigger regulatory intervention, and provide further ammunition for parliamentary criticism. The Premium Bonds prize draw is especially high-profile.

**Success Metrics**:
- **Primary Metric**: Zero P1/P2 customer-impacting incidents attributable to migration activities
- **Secondary Metrics**:
  - 99.95% uptime maintained across all customer channels
  - Premium Bonds prize draw executed successfully every month without exception
  - Customer complaint volumes remain within ±10% of pre-migration baseline
  - Zero data integrity errors in migrated customer accounts

**Baseline**: Current Atos platform uptime (to be established, estimated 99.9%)

**Target**: 99.95% uptime during migration; zero P1/P2 incidents from migration; zero data loss

**Measurement Method**: Real-time service monitoring platform; automated data reconciliation reports; customer complaint tracking system; Premium Bonds draw audit reports

**Dependencies**:
- Comprehensive test environments that replicate production scale
- Minimum 3 full cutover rehearsals before live migration
- Automated data reconciliation tooling operational before parallel-run
- Rollback procedures tested and rehearsed for every migration phase

**Risks to Achievement**:
- Undocumented legacy system behaviours causing unexpected failures
- Production-scale testing environments unavailable due to cost constraints
- Atos knowledge holders unavailable during critical cutover periods
- Data reconciliation revealing discrepancies requiring manual resolution

---

### Goal G-3: Build In-House Technical Capability

**Derived From Drivers**: SD-2, SD-3, SD-4, SD-15

**Goal Owner**: NS&I CTO (with HR Director)

**Goal Statement**: Achieve minimum 30% NS&I permanent staff in core programme roles by end of 2026, rising to 50% by end of 2027, with all technology leadership positions (CTO, Chief Architect, Head of Engineering, Head of Security) filled by NS&I permanent employees.

**Why This Matters**: The PAC found NS&I "lacked the skills" to deliver and was dependent on consultants without accountability. Architecture Principle P5 (Skills and Capability Ownership) mandates internal capability. Without in-house expertise, NS&I cannot be an intelligent client, cannot hold vendors to account, and will repeat the dependency pattern that created the current crisis.

**Success Metrics**:
- **Primary Metric**: Percentage of programme roles filled by NS&I permanent staff (target: 30% by end-2026, 50% by end-2027)
- **Secondary Metrics**:
  - All four technology leadership positions filled permanently
  - Knowledge transfer score (measured via assessment) — target: 80% of critical knowledge domains documented and transferable
  - Staff retention rate for permanent technical hires — target: 85% annual retention

**Baseline**: Current permanent staff ratio estimated at <15% of programme roles

**Target**: 30% by December 2026; 50% by December 2027; 100% of technology leadership roles permanent

**Measurement Method**: Monthly HR dashboard; quarterly skills assessment; knowledge transfer milestone reviews; exit interview analysis

**Dependencies**:
- Government Digital and Data profession pay frameworks (potential constraint)
- Recruitment pipeline established with specialist agencies
- Knowledge transfer requirements contractually mandated with consultants
- Retention packages approved by NS&I Board and Treasury

**Risks to Achievement**:
- Government pay scales uncompetitive for senior banking technology professionals
- Recruitment timelines exceeding 6 months for specialist roles
- Consultants prioritising delivery over knowledge transfer
- New permanent staff lacking programme context and requiring extended onboarding

---

### Goal G-4: Complete SBS Platform Integration and Accreditation

**Derived From Drivers**: SD-4, SD-6, SD-9, SD-14

**Goal Owner**: NS&I CTO

**Goal Statement**: Complete SBS SBP Digital Core integration, configuration, and testing to achieve full functional, performance, and security accreditation by Q2 2028, with all NS&I products operational on the new platform.

**Why This Matters**: The SBS platform is the technical foundation for the entire modernisation. Until it is integrated, tested, and accredited, no customer migration can occur. The PAC noted that "main work has yet to start" on the core banking replacement. This goal represents the central delivery milestone.

**Success Metrics**:
- **Primary Metric**: SBS platform achieves "Ready for Live" accreditation (functional, performance, security)
- **Secondary Metrics**:
  - 100% of NS&I products configured and tested on SBS platform
  - Performance testing confirms platform handles peak load (Premium Bonds draw day volumes)
  - Security accreditation achieved (NCSC CAF, PCI DSS, penetration test)
  - API-first integration architecture with zero direct database dependencies

**Baseline**: SBS platform not yet integrated (main work not started per PAC)

**Target**: Full platform accreditation by Q2 2028; all products operational by Q3 2028

**Measurement Method**: Programme gate reviews; independent technical assurance; NCSC IT Health Check; PCI DSS QSA assessment; performance test reports

**Dependencies**:
- SBS contractual commitment to platform delivery milestones
- NS&I product requirements baselined and change-controlled
- Test environments provisioned and operational
- Security architecture reviewed and approved by CISO and NCSC

**Risks to Achievement**:
- SBS platform requiring significant customisation for NS&I-specific products (especially Premium Bonds)
- Requirements volatility from late-discovered legacy behaviours
- Performance at NS&I scale (24M accounts, £230bn) exceeding SBS's proven deployments
- Security accreditation requiring remediation cycles that impact the timeline

---

### Goal G-5: Execute Managed Atos Exit with Full Knowledge Transfer

**Derived From Drivers**: SD-5, SD-8, SD-4

**Goal Owner**: Programme Director

**Goal Statement**: Complete the contractual exit from Atos including full knowledge transfer, documented legacy system behaviours, and clean data extraction, with Atos service levels maintained at contractual SLA throughout the transition period and exit completed within 12 months of SBS go-live.

**Why This Matters**: The Atos relationship has been the backbone of NS&I operations for 27 years. A poorly managed exit could jeopardise service continuity, lose critical institutional knowledge, and create contractual disputes that further escalate costs. Atos's own financial pressures add complexity.

**Success Metrics**:
- **Primary Metric**: Atos SLA compliance maintained at 100% throughout transition
- **Secondary Metrics**:
  - Knowledge transfer completion: 100% of critical systems documented
  - Data extraction: All customer data migrated with zero data loss (verified by reconciliation)
  - Exit costs within agreed contractual envelope (±10%)
  - Zero unresolved contractual disputes at exit completion

**Baseline**: Atos operating under current SLA framework

**Target**: Complete exit within 12 months of SBS production go-live; zero service degradation during transition

**Measurement Method**: Monthly SLA reports; knowledge transfer milestone reviews; data reconciliation audits; contractual milestone tracking

**Dependencies**:
- Atos exit plan agreed and contractually binding
- Key Atos personnel retained through transition (retention mechanisms)
- Data extraction tools and formats agreed with SBS
- NS&I in-house team ready to absorb transferred knowledge

**Risks to Achievement**:
- Atos financial pressures reducing investment in transition quality
- Key Atos personnel departing before knowledge transfer complete
- Undocumented system behaviours only discoverable during migration
- Contractual disputes over exit responsibilities and costs

---

### Goal G-6: Demonstrate Transparent Governance and PAC Compliance

**Derived From Drivers**: SD-2, SD-3, SD-11, SD-13

**Goal Owner**: NS&I Chief Executive

**Goal Statement**: Respond to all PAC recommendations within 60 days, implement an auditable governance framework that satisfies NAO and IPA requirements, and achieve a minimum AMBER IPA delivery confidence rating within 12 months.

**Why This Matters**: The programme's credibility depends on demonstrating that NS&I has heard and acted on parliamentary criticism. The PAC response is a formal government commitment. The IPA rating directly influences Treasury funding decisions and Ministerial confidence. Moving from the current (likely RED) to AMBER would signal meaningful improvement.

**Success Metrics**:
- **Primary Metric**: IPA delivery confidence rating (target: AMBER within 12 months; AMBER/GREEN within 24 months)
- **Secondary Metrics**:
  - 100% of PAC recommendations responded to within 60 days
  - NAO confirmation of governance framework adequacy
  - Monthly risk reporting with zero instances of risk suppression identified by audit
  - Quarterly honest progress assessment published to programme board

**Baseline**: IPA rating estimated RED or RED/AMBER (based on PAC findings)

**Target**: AMBER within 12 months; AMBER/GREEN within 24 months

**Measurement Method**: IPA quarterly reviews; NAO engagement feedback; PAC correspondence tracking; internal audit of risk reporting completeness

**Dependencies**:
- Culture change programme addressing "good news" bias
- Risk reporting framework with escalation triggers
- Programme board terms of reference updated to require challenge
- Independent assurance function with direct Board access

**Risks to Achievement**:
- Cultural change requiring longer than 12 months to embed
- New problems emerging that overshadow governance improvements
- IPA assessors applying higher standards given programme history
- Staff fearful of honest reporting due to blame culture

---

### Goal G-7: Achieve Regulatory Compliance for New Platform

**Derived From Drivers**: SD-6, SD-12, SD-14

**Goal Owner**: NS&I CISO (with DPO)

**Goal Statement**: Achieve full regulatory compliance for the SBS platform across NCSC CAF, PCI DSS, UK GDPR, FCA, and PRA requirements before any customer data is migrated, with ongoing compliance automation thereafter.

**Why This Matters**: The SBS platform cannot receive customer data or process transactions until it meets all regulatory requirements. Given the dual-running period, both platforms must be compliant simultaneously. Architecture Principle P10 (Compliance as Code) mandates automated compliance validation.

**Success Metrics**:
- **Primary Metric**: Full regulatory accreditation achieved before customer data migration
- **Secondary Metrics**:
  - NCSC CAF self-assessment: all outcomes at "Achieved" level
  - PCI DSS certification achieved for SBS environment
  - DPIA completed and approved by ICO (if required)
  - Zero critical or high security findings unresolved at go-live

**Baseline**: SBS platform not yet deployed; no compliance assessment initiated

**Target**: Full accreditation 6 months before customer migration; automated compliance dashboards operational

**Measurement Method**: NCSC CAF self-assessment; PCI DSS QSA audit; DPIA register; security vulnerability scanning; compliance dashboard metrics

**Dependencies**:
- SBS platform deployed to testing environment for assessment
- Security architecture design approved by CISO
- NCSC engagement for cloud security guidance
- PCI DSS scope defined for SBS environment

**Risks to Achievement**:
- SBS platform security architecture not meeting UK government standards
- PCI DSS scope expansion during assessment
- Remediation cycles extending the accreditation timeline
- Regulatory requirements changing during the multi-year programme

---

### Goal G-8: Deliver Consultant Accountability Framework

**Derived From Drivers**: SD-2, SD-7, SD-15

**Goal Owner**: NS&I CFO (with Programme Director)

**Goal Statement**: Transition 100% of consultant engagements from time-and-materials to outcome-based contracts with defined deliverables, measurable KPIs, and knowledge transfer requirements within 6 months, reducing total consultant spend by 25% by end of 2027.

**Why This Matters**: The PAC was particularly critical of the £43m spent on consultants with NS&I being "vague on how it holds them to account". This goal directly addresses that finding and demonstrates fiscal responsibility.

**Success Metrics**:
- **Primary Metric**: 100% of consultant engagements on outcome-based contracts within 6 months
- **Secondary Metrics**:
  - 25% reduction in total consultant spend by end of 2027
  - Knowledge transfer score: 80% of critical domains covered
  - Quarterly VfM review confirming consultant contribution
  - Zero consultant engagements exceeding 12 months without recompetition

**Baseline**: £43m spent on consultants (cumulative); mix of T&M and outcome-based contracts

**Target**: 100% outcome-based; 25% spend reduction; measurable KT outcomes

**Measurement Method**: Contract register audit; monthly spend reports; knowledge transfer assessments; quarterly VfM reviews

**Dependencies**:
- Procurement and legal capacity to restructure existing contracts
- Clear deliverable definitions requiring in-house domain expertise
- NS&I permanent staff available to receive knowledge transfer
- HR and procurement alignment on paired working model

**Risks to Achievement**:
- Consultant firms resistant to outcome-based models for uncertain scope
- NS&I lacking expertise to define measurable deliverables
- Best consultants leaving for less scrutinised engagements
- Transition period causing temporary productivity loss

---

## Goal-to-Outcome Mapping

### Outcome O-1: Restored Financial Credibility

**Supported Goals**: G-1, G-6, G-8

**Outcome Statement**: NS&I can demonstrate to Treasury, PAC, and NAO that the core banking migration has a validated cost baseline, monthly variance within 5%, and that every major expenditure category can be justified with evidence of value delivered.

**Measurement Details**:
- **KPI**: Monthly cost variance (actual vs. forecast)
- **Current Value**: Unknown (no credible baseline exists)
- **Target Value**: Less than 5% variance; zero unexplained cost categories
- **Measurement Frequency**: Monthly
- **Data Source**: EVM reporting system, financial ledger, contract management system
- **Report Owner**: NS&I CFO

**Business Value**:
- **Financial Impact**: Prevention of further cost escalation; potential £50M+ saving through improved cost control and consultant accountability
- **Strategic Impact**: Restored Treasury confidence enabling continued funding; improved IPA rating
- **Operational Impact**: Evidence-based decision-making on programme trade-offs
- **Customer Impact**: Indirect — programme viability protects customer service continuity

**Timeline**:
- **Phase 1 (Months 1–3)**: Cost baseline established and independently validated; EVM reporting operational
- **Phase 2 (Months 4–6)**: First quarterly NAO review confirms reporting adequacy; consultant contracts restructured
- **Phase 3 (Months 7–12)**: Consistent <5% variance demonstrated; IPA acknowledges improvement
- **Sustainment (Year 2+)**: Cost management embedded as BAU; Treasury reporting automated

**Stakeholder Benefits**:
- **HM Treasury**: Confidence to approve future funding tranches
- **PAC**: Evidence that their recommendations have been acted upon
- **NAO**: Auditable cost data for future reports
- **NS&I CFO**: Personal credibility and career protection

**Leading Indicators**:
- Work breakdown structure completeness (target: 100% within 60 days)
- Number of cost accounts with assigned budget (target: 100%)
- EVM data quality score (target: >95% accuracy)

**Lagging Indicators**:
- NAO assessment of cost reporting (target: "adequate")
- IPA delivery confidence movement (target: RED → AMBER)
- PAC response acceptance (target: no further hearings on cost)

---

### Outcome O-2: Seamless Customer Migration

**Supported Goals**: G-2, G-4, G-5

**Outcome Statement**: All 24 million NS&I customer accounts are migrated from the Atos legacy platform to SBS SBP Digital Core with zero data loss, zero service interruption, and customer satisfaction maintained at or above pre-migration levels.

**Measurement Details**:
- **KPI**: Customer-impacting incidents during migration
- **Current Value**: Baseline to be established (current Atos incident rate)
- **Target Value**: Zero P1/P2 incidents attributable to migration; customer satisfaction maintained
- **Measurement Frequency**: Real-time monitoring; monthly satisfaction surveys
- **Data Source**: Service monitoring platform, incident management system, customer feedback
- **Report Owner**: NS&I Operations Director

**Business Value**:
- **Financial Impact**: Avoidance of compensation costs, regulatory fines, and reputational damage (estimated exposure: £100M+ in worst case)
- **Strategic Impact**: Demonstrated government capability to deliver complex technology transformation
- **Operational Impact**: Modern platform enabling future service improvements and cost reduction
- **Customer Impact**: Uninterrupted service with post-migration improvements in digital experience

**Timeline**:
- **Phase 1 (2026)**: SBS platform integration and testing; parallel-run planning; cutover rehearsals begin
- **Phase 2 (2027)**: Parallel-run with automated reconciliation; staged product migration (low-risk first)
- **Phase 3 (2028)**: Full customer migration; Premium Bonds migration; Atos decommissioning
- **Sustainment (2029+)**: SBS platform optimisation; deferred digital experience improvements

**Stakeholder Benefits**:
- **NS&I Customers**: Uninterrupted service, improved digital experience post-migration
- **NS&I Operations Director**: Proven migration methodology, modern operational tooling
- **Atos**: Clean contractual exit, reputation as responsible transition partner
- **SBS**: Flagship reference implementation in UK government banking

**Leading Indicators**:
- Cutover rehearsal success rate (target: 3/3 successful before live)
- Parallel-run data reconciliation accuracy (target: 99.9999%)
- Test coverage for customer journeys (target: 100% of critical paths)

**Lagging Indicators**:
- Post-migration incident rate (target: same or better than pre-migration)
- Customer satisfaction score (target: ≥ pre-migration baseline)
- Data integrity audit (target: zero discrepancies in migrated accounts)

---

### Outcome O-3: Capable and Accountable Organisation

**Supported Goals**: G-3, G-6, G-8

**Outcome Statement**: NS&I has built a permanent technology team capable of operating as an intelligent client, holding vendors to account, and making informed technology decisions independently — addressing the core PAC finding that NS&I "lacks the skills" to deliver.

**Measurement Details**:
- **KPI**: Permanent staff ratio in programme roles
- **Current Value**: Estimated <15%
- **Target Value**: 50% by end of 2027
- **Measurement Frequency**: Monthly
- **Data Source**: HR information system, programme resource plan
- **Report Owner**: NS&I HR Director

**Business Value**:
- **Financial Impact**: Reduced consultant dependency saving estimated £15M annually from 2028
- **Strategic Impact**: NS&I established as a credible digital delivery organisation
- **Operational Impact**: Institutional knowledge retained; reduced key-person risk
- **Customer Impact**: Indirect — better technology decisions lead to better customer services

**Timeline**:
- **Phase 1 (Months 1–3)**: Technology leadership positions advertised; recruitment pipeline established
- **Phase 2 (Months 4–6)**: First permanent hires in post; paired working model operational; 30% ratio trajectory
- **Phase 3 (Months 7–12)**: 30% permanent ratio achieved; knowledge transfer milestones at 50%
- **Sustainment (Year 2+)**: 50% ratio achieved; consultant spend reduced by 25%; self-sustaining capability

**Stakeholder Benefits**:
- **PAC**: Evidence that accountability recommendation has been implemented
- **NS&I CTO**: Capable team to deliver and operate modern platform
- **Consultants/SIs**: Clear exit path with defined knowledge transfer
- **NS&I CEO**: Organisational credibility restored

**Leading Indicators**:
- Recruitment pipeline volume (target: 3x candidates per role)
- Time-to-hire for technology roles (target: <90 days)
- Paired working coverage (target: 100% of critical roles)

**Lagging Indicators**:
- Annual staff retention rate (target: 85%)
- Knowledge transfer assessment scores (target: 80% coverage of critical domains)
- IPA capability assessment (target: "adequate" or above)

---

### Outcome O-4: Secure and Compliant Platform

**Supported Goals**: G-4, G-7

**Outcome Statement**: The SBS SBP Digital Core platform achieves full security accreditation and regulatory compliance, meeting NCSC CAF, PCI DSS, UK GDPR, FCA, and PRA requirements, with automated compliance monitoring providing continuous assurance.

**Measurement Details**:
- **KPI**: Regulatory accreditation status
- **Current Value**: Not started (platform not yet deployed)
- **Target Value**: Full accreditation across all frameworks 6 months before customer migration
- **Measurement Frequency**: Quarterly assessment cycles
- **Data Source**: Compliance management system, security scanning tools, regulatory correspondence
- **Report Owner**: NS&I CISO

**Business Value**:
- **Financial Impact**: Avoidance of regulatory fines and enforcement action (PCI DSS fines: up to £500K per incident; ICO fines: up to £17.5M)
- **Strategic Impact**: Demonstrated compliance as a competitive advantage for NS&I's reputation
- **Operational Impact**: Automated compliance reducing manual audit burden by estimated 60%
- **Customer Impact**: Enhanced protection of customer data and financial assets

**Timeline**:
- **Phase 1 (2026)**: Security architecture design; NCSC engagement; PCI DSS scope definition
- **Phase 2 (2027)**: Platform security testing; NCSC CAF assessment; PCI DSS pre-assessment
- **Phase 3 (H1 2028)**: Full accreditation achieved; automated compliance dashboards operational
- **Sustainment (2028+)**: Continuous compliance monitoring; annual re-certification

**Stakeholder Benefits**:
- **NCSC**: Confidence in UK government cloud security posture
- **FCA/PRA**: Assurance that consumer protection standards are met
- **ICO**: GDPR compliance demonstrable
- **NS&I CISO**: Career-defining platform security programme

**Leading Indicators**:
- Security architecture review sign-off (target: Q2 2026)
- Vulnerability scan findings closure rate (target: >95% within SLA)
- Compliance automation coverage (target: 80% of controls automated)

**Lagging Indicators**:
- Formal accreditation certificates received
- Zero critical/high security findings at go-live
- First annual re-certification passed without material findings

---

### Outcome O-5: Managed Vendor Transition

**Supported Goals**: G-5, G-4

**Outcome Statement**: The transition from Atos to SBS is completed within agreed timelines and costs, with all institutional knowledge captured, data migrated with verified integrity, and no contractual disputes requiring legal escalation.

**Measurement Details**:
- **KPI**: Knowledge transfer completion percentage and data migration integrity
- **Current Value**: Knowledge transfer not started; data migration not started
- **Target Value**: 100% knowledge transfer; 100% data migration with zero discrepancies
- **Measurement Frequency**: Monthly knowledge transfer reviews; continuous data reconciliation
- **Data Source**: Knowledge management system, data reconciliation platform, contract management
- **Report Owner**: Programme Director

**Business Value**:
- **Financial Impact**: Exit costs controlled within contractual envelope (avoid £50M+ dispute exposure)
- **Strategic Impact**: Clean transition enabling full focus on SBS platform optimisation
- **Operational Impact**: Institutional knowledge preserved; operations team self-sufficient
- **Customer Impact**: No customer impact from vendor transition — seamless behind the scenes

**Timeline**:
- **Phase 1 (2026)**: Atos exit plan agreed; knowledge transfer programme initiated; data extraction approach designed
- **Phase 2 (2027)**: Knowledge transfer milestones at 70%; data extraction tooling operational; parallel-run data sync
- **Phase 3 (2028)**: Knowledge transfer complete; full data migration; Atos service wind-down
- **Sustainment (2029)**: Atos exit complete; all decommissioning finished; contractual close-out

**Stakeholder Benefits**:
- **Atos**: Clean contractual exit; reputation protected; final payments received
- **SBS**: Full operational data; no legacy dependencies remaining
- **NS&I Operations**: Complete system documentation; self-sufficient operations team
- **NS&I CFO**: Exit costs controlled; no open contractual liabilities

**Leading Indicators**:
- Knowledge transfer milestones achieved on schedule (target: 100%)
- Atos key personnel retention during transition (target: 90% of identified critical staff)
- Data extraction test runs successful (target: 100% accuracy on test data)

**Lagging Indicators**:
- Atos SLA compliance through to exit (target: 100%)
- Post-exit operational incidents attributable to knowledge gaps (target: zero)
- Contractual close-out achieved without dispute (target: yes)

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| HM Treasury | SD-1 | Cost control and VfM | G-1 | Cost baseline within 90 days | O-1 | Restored financial credibility |
| PAC | SD-2 | Accountability and transparency | G-1 | Cost baseline within 90 days | O-1 | Restored financial credibility |
| PAC | SD-2 | Accountability and transparency | G-6 | PAC compliance and IPA rating | O-1 | Restored financial credibility |
| PAC | SD-2 | Accountability and transparency | G-3 | Build in-house capability | O-3 | Capable and accountable organisation |
| NS&I CEO | SD-3 | Delivery and reputation | G-6 | PAC compliance and IPA rating | O-1 | Restored financial credibility |
| NS&I CEO | SD-3 | Delivery and reputation | G-3 | Build in-house capability | O-3 | Capable and accountable organisation |
| NS&I CTO | SD-4 | Technical excellence | G-4 | SBS platform accreditation | O-2 | Seamless customer migration |
| NS&I CTO | SD-4 | Technical excellence | G-3 | Build in-house capability | O-3 | Capable and accountable organisation |
| Ops Director | SD-5 | Service continuity | G-2 | Zero customer incidents | O-2 | Seamless customer migration |
| Ops Director | SD-5 | Service continuity | G-5 | Managed Atos exit | O-5 | Managed vendor transition |
| CISO | SD-6 | Security during transformation | G-7 | Regulatory compliance | O-4 | Secure and compliant platform |
| CISO | SD-6 | Security during transformation | G-4 | SBS platform accreditation | O-4 | Secure and compliant platform |
| NS&I CFO | SD-7 | Budget control | G-1 | Cost baseline within 90 days | O-1 | Restored financial credibility |
| NS&I CFO | SD-7 | Budget control | G-8 | Consultant accountability | O-1 | Restored financial credibility |
| Atos | SD-8 | Managed exit | G-5 | Managed Atos exit | O-5 | Managed vendor transition |
| SBS | SD-9 | Successful deployment | G-4 | SBS platform accreditation | O-2 | Seamless customer migration |
| Customers | SD-10 | Uninterrupted service | G-2 | Zero customer incidents | O-2 | Seamless customer migration |
| NAO | SD-11 | Audit assurance | G-1 | Cost baseline within 90 days | O-1 | Restored financial credibility |
| NAO | SD-11 | Audit assurance | G-6 | PAC compliance and IPA rating | O-1 | Restored financial credibility |
| FCA / PRA | SD-12 | Regulatory compliance | G-7 | Regulatory compliance | O-4 | Secure and compliant platform |
| FCA / PRA | SD-12 | Regulatory compliance | G-2 | Zero customer incidents | O-2 | Seamless customer migration |
| IPA | SD-13 | Delivery confidence | G-6 | PAC compliance and IPA rating | O-1 | Restored financial credibility |
| Chief Architect | SD-14 | Architectural integrity | G-4 | SBS platform accreditation | O-4 | Secure and compliant platform |
| Consultants / SIs | SD-15 | Delivery and accountability | G-8 | Consultant accountability | O-3 | Capable and accountable organisation |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: **Speed vs. Safety** — HM Treasury (SD-1) and PAC (SD-2) want visible progress and cost control after five wasted years, but NS&I Operations Director (SD-5) and CISO (SD-6) require methodical, low-risk migration to protect 24 million customers.
  - **Resolution Strategy**: Phased delivery (Principle P9) — start with low-risk products (e.g., Direct Saver) to demonstrate rapid progress while reserving Premium Bonds and complex products for later phases when the team has proven the migration methodology. Treasury sees early wins; Operations maintains safety.

- **Conflict 2**: **Vendor Independence vs. Platform Commitment** — Architecture Principle P7 mandates vendor independence, but the programme is committing to SBS as the strategic core banking platform, creating a new single-vendor dependency.
  - **Resolution Strategy**: Apply vendor independence at the integration layer — use open standards (REST, OpenAPI, CloudEvents) for all interfaces around SBS, ensuring that ancillary services can be sourced independently. Accept SBS as the core engine while avoiding lock-in in channels, integration, data, and operations tooling.

- **Conflict 3**: **Cost Reduction vs. Capability Building** — CFO (SD-7) wants to reduce consultant spend by 25%, but CTO (SD-4) needs experienced consultants to deliver while building in-house capability, and reducing spend too quickly could impact delivery.
  - **Resolution Strategy**: Graduated reduction — maintain current consultant levels for 6 months while accelerating permanent recruitment and knowledge transfer, then reduce by 10% at month 6, 15% at month 12, and reach 25% reduction by end of 2027. Paired working model ensures knowledge transfers before consultants depart.

- **Conflict 4**: **Atos Exit Speed vs. Knowledge Retention** — NS&I wants to reduce Atos dependency as quickly as possible (cost and strategic drivers), but rushing the exit risks losing critical institutional knowledge that exists only in Atos personnel's heads.
  - **Resolution Strategy**: Contractual retention incentives for identified Atos key personnel (estimated 20–30 individuals) through the transition, with milestone-based payments tied to knowledge transfer completion rather than tenure. Document-first approach: no system can be decommissioned until its behaviours are documented and validated.

**Synergies**:

- **Synergy 1**: PAC's accountability driver (SD-2) and NAO's assurance driver (SD-11) are perfectly aligned — satisfying NAO's evidence requirements automatically generates the transparency PAC demands.

- **Synergy 2**: CTO's modernisation driver (SD-4) and Chief Architect's integrity driver (SD-14) reinforce each other — both want a well-architected cloud-native platform rather than a like-for-like lift-and-shift.

- **Synergy 3**: Operations Director's continuity driver (SD-5) and SBS's success driver (SD-9) are aligned — both need thorough testing, successful parallel-run, and clean cutover. A failed migration hurts both equally.

- **Synergy 4**: CFO's accountability driver (SD-7) and the consultant accountability driver (SD-15) create mutual benefit — outcome-based contracts give CFO cost control and give quality consultants a clearer scope to deliver against.

---

## Communication & Engagement Plan

### Stakeholder-Specific Messaging

#### HM Treasury Sponsor Team

**Primary Message**: "We have established a validated cost baseline, independent assurance, and monthly EVM reporting. The programme is now governed with the transparency and rigour that Treasury expects."

**Key Talking Points**:
- Cost baseline independently validated with documented assumptions and contingency
- Monthly EVM reports showing earned value against spend
- Early warning triggers at 5% and 10% variance — no surprises
- Consultant spend restructured with outcome-based contracts

**Communication Frequency**: Monthly progress report; quarterly deep-dive; ad hoc for material changes

**Preferred Channel**: Formal written report with supporting data; face-to-face quarterly

**Success Story**: "NS&I delivered the first product migration (Direct Saver) on time and within budget, with reconciliation showing zero data discrepancies."

---

#### PAC / Geoffrey Clifton-Brown MP

**Primary Message**: "NS&I has heard the Committee's findings. We have responded to every recommendation with specific, measurable actions, and we are implementing them with independent verification."

**Key Talking Points**:
- Every PAC recommendation mapped to a specific action, owner, and deadline
- Independent cost assurance and IPA review in place
- In-house capability build underway — 30% permanent staff target for 2026
- "Good news" culture addressed through independent assurance and escalation triggers

**Communication Frequency**: Formal PAC response within 60 days; evidence sessions as required

**Preferred Channel**: Treasury Minute (formal); written evidence; oral evidence sessions

**Success Story**: "IPA delivery confidence improved from RED to AMBER within 12 months, with NAO confirming governance framework is now adequate."

---

#### NS&I Operations Director

**Primary Message**: "Service continuity is the non-negotiable priority. The migration plan includes extended parallel-run, automated reconciliation, full cutover rehearsals, and rollback at every stage."

**Key Talking Points**:
- Minimum 6-month parallel-run for core products; 12 months for Premium Bonds
- Automated data reconciliation with 99.9999% accuracy target
- Three full cutover rehearsals before any live migration
- Rollback procedures tested for every migration phase

**Communication Frequency**: Weekly migration planning; daily during cutover periods

**Preferred Channel**: Working sessions; operational dashboards; incident bridge

**Success Story**: "Third cutover rehearsal completed in 4 hours with zero issues; reconciliation confirmed 100% data accuracy across 500,000 test accounts."

---

#### Atos

**Primary Message**: "We value 27 years of partnership. The exit plan is designed to be commercially fair, operationally smooth, and reputationally positive for both organisations."

**Key Talking Points**:
- Clear exit milestones with agreed timelines and costs
- Retention incentives for key personnel through transition
- Knowledge transfer structured as a collaborative programme, not an adversarial extraction
- Atos's operational excellence during transition will be publicly acknowledged

**Communication Frequency**: Fortnightly joint steering; weekly operational

**Preferred Channel**: Joint governance committee; contract management meetings

**Success Story**: "Atos successfully supported the first product migration with zero service disruption, demonstrating exemplary partnership during transition."

---

#### SBS (Sopra Banking Software)

**Primary Message**: "NS&I is committed to making this deployment a flagship success for SBP Digital Core. We will work in genuine partnership, standardise where possible, and ensure adequate time for thorough testing."

**Key Talking Points**:
- NS&I will adopt standard SBS configuration where possible, minimising customisation
- Adequate testing timeline — no pressure to skip quality gates
- Joint architecture governance to ensure platform integrity
- Success here creates a major UK government reference for SBS

**Communication Frequency**: Weekly delivery governance; monthly executive steering

**Preferred Channel**: Joint delivery board; product configuration workshops; executive meetings

**Success Story**: "SBS SBP Digital Core passed performance testing at 150% of NS&I peak volumes, confirming platform scalability for the UK's largest savings institution."

---

#### NS&I Customers (24 million)

**Primary Message**: "Your savings are safe. We are upgrading our systems behind the scenes to give you a better digital experience. You do not need to take any action."

**Key Talking Points**:
- Savings and Premium Bonds are unaffected — government-backed guarantee unchanged
- Improved digital services coming in 2028/2029
- Any changes to how you access your account will be communicated well in advance
- Customer service channels remain fully available

**Communication Frequency**: As needed for material changes; post-migration for new features

**Preferred Channel**: GOV.UK page; Premium Bonds newsletter; email; post for non-digital customers

**Success Story**: "NS&I customers now have a modern, faster online experience with new features including real-time balance updates and improved Premium Bonds prize checker."

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| NS&I Operations Team | Managing Atos-hosted monolithic platform | Operating cloud-native SBS platform with DevOps practices | HIGH | MEDIUM | 12-month transition with training, paired working, gradual handover |
| NS&I Customer Services | Atos-provided tools and processes | New CRM and service tools integrated with SBS | HIGH | MEDIUM | Early involvement in requirements; parallel-run for familiarisation |
| NS&I Product Owners | Products defined by legacy system constraints | Products on configurable modern platform | MEDIUM | LOW | Product migration workshops; new feature opportunities as incentive |
| NS&I Finance Team | Limited programme cost visibility | EVM reporting with real-time dashboards | MEDIUM | LOW | Training on EVM; dashboards designed for their needs |
| NS&I Delivery Teams | Consultant-heavy, waterfall-influenced delivery | Agile delivery with permanent staff core | HIGH | MEDIUM | Agile coaching; gradual transition; mixed teams during handover |
| Atos Service Teams | Long-term stable relationship with NS&I | Managed exit over 2–3 years | HIGH | HIGH | Fair exit terms; retention incentives; recognition of contribution |
| External Consultants | T&M contracts with limited accountability | Outcome-based contracts with KT requirements | HIGH | HIGH | Premium rates for quality deliverables; clear scope; reputational opportunity |

### Change Readiness

**Champions** (Enthusiastic supporters):
- **NS&I CTO** — Sees this as a career-defining opportunity to modernise NS&I
- **NS&I Chief Architect** — Professionally motivated by cloud-native modernisation
- **SBS Delivery Team** — Commercially and reputationally motivated for success
- **NS&I Product Owners** — See new platform as enabling long-deferred product improvements

**Fence-sitters** (Neutral, need convincing):
- **NS&I Operations Team** — Supportive of modernisation but worried about stability during transition; need to see successful rehearsals
- **NS&I Customer Services** — Concerned about new tools and processes; need early involvement and training
- **NS&I Finance Team** — Supportive of transparency but wary of additional reporting burden; need efficient tooling
- **HM Treasury** — Supportive of modernisation but sceptical given history; need early evidence of improved governance

**Resisters** (Opposed or sceptical):
- **Atos operational staff** — Facing job uncertainty and organisational change; mitigate through retention packages and honest communication about timelines
- **Some consultants** — Outcome-based contracts reduce revenue certainty; mitigate by positioning quality delivery as reputational opportunity
- **Long-serving NS&I staff** — May be attached to familiar legacy processes; mitigate through involvement in design, recognition of legacy knowledge value

---

## Risk Register (Stakeholder-Related)

### Risk R-1: "Good News" Culture Persists

**Related Stakeholders**: NS&I CEO, Programme Director, HM Treasury, PAC

**Risk Description**: Despite PAC criticism, NS&I's organisational culture continues to suppress bad news, filter risk reporting, and present over-optimistic progress, undermining governance and stakeholder trust.

**Impact on Goals**: G-6 (Governance and PAC compliance), G-1 (Cost baseline credibility)

**Probability**: HIGH

**Impact**: HIGH

**Mitigation Strategy**: Independent assurance function with direct Board access; anonymous risk reporting channel; external NED challenge on programme board; NAO observer status at steering committees

**Contingency Plan**: If culture change is not evident within 6 months, Treasury to mandate external programme director with authority to restructure reporting lines

---

### Risk R-2: Key Atos Personnel Depart Before Knowledge Transfer

**Related Stakeholders**: Atos, NS&I Operations Director, NS&I CTO

**Risk Description**: Critical Atos staff with unique knowledge of legacy system behaviours leave or are redeployed before knowledge transfer is complete, creating irrecoverable knowledge gaps.

**Impact on Goals**: G-5 (Managed Atos exit), G-2 (Zero customer incidents)

**Probability**: HIGH

**Impact**: HIGH

**Mitigation Strategy**: Identify 20–30 critical Atos personnel immediately; negotiate contractual retention incentives tied to knowledge transfer milestones; begin documentation sprints now (before SBS platform is ready); video-record system walkthroughs

**Contingency Plan**: If key personnel depart, engage specialist legacy system archaeology firm; extend parallel-run period to allow learning-by-observation

---

### Risk R-3: SBS Platform Requires Extensive Customisation

**Related Stakeholders**: SBS, NS&I CTO, NS&I Chief Architect, Programme Director

**Risk Description**: NS&I's unique products (especially Premium Bonds prize draw) require significant SBS platform customisation, increasing cost, delivery time, and creating new vendor lock-in.

**Impact on Goals**: G-4 (SBS accreditation), G-1 (Cost baseline)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Conduct SBS fit-gap analysis for every NS&I product before committing to platform configuration; adopt SBS standard where possible; isolate NS&I-specific logic in extension modules rather than core customisation; contractually cap customisation scope

**Contingency Plan**: If customisation exceeds threshold (>20% of core), reassess SBS platform suitability for Premium Bonds specifically and consider a dedicated microservice for prize draw logic

---

### Risk R-4: Recruitment Fails to Meet Capability Targets

**Related Stakeholders**: NS&I CTO, NS&I HR Director, PAC

**Risk Description**: Government pay scales cannot attract sufficient senior banking technology professionals, leaving NS&I unable to meet the 30% permanent staff target and remaining consultant-dependent.

**Impact on Goals**: G-3 (In-house capability), G-8 (Consultant accountability)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Use Digital, Data and Technology (DDaT) profession pay framework exceptions; offer non-financial benefits (pension, flexible working, mission-driven work); engage specialist government recruitment agencies; consider secondments from other departments

**Contingency Plan**: If recruitment targets missed by >20%, negotiate with Treasury for enhanced pay bands citing programme risk; extend consultant contracts but with accelerated knowledge transfer requirements

---

### Risk R-5: Regulatory Requirements Change During Migration

**Related Stakeholders**: FCA, PRA, NCSC, NS&I CISO

**Risk Description**: Regulatory frameworks (PCI DSS, NCSC CAF, FCA rules) change during the multi-year migration, requiring rework of security architecture or compliance controls already implemented.

**Impact on Goals**: G-7 (Regulatory compliance), G-4 (SBS accreditation)

**Probability**: MEDIUM

**Impact**: MEDIUM

**Mitigation Strategy**: Maintain active dialogue with all regulators; adopt a compliance-as-code approach (Principle P10) that enables rapid policy updates; build regulatory change monitoring into programme governance; design for the most stringent interpretation

**Contingency Plan**: Maintain 10% contingency in security/compliance budget for regulatory change; negotiate with regulators for transitional provisions during migration period

---

### Risk R-6: Parallel-Run Data Reconciliation Reveals Systemic Issues

**Related Stakeholders**: NS&I Operations Director, NS&I Customers, NAO

**Risk Description**: Automated data reconciliation during the parallel-run period reveals systemic discrepancies between Atos and SBS platforms that cannot be resolved without manual intervention, delaying migration and potentially exposing historical data integrity issues.

**Impact on Goals**: G-2 (Zero customer incidents), G-4 (SBS accreditation)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Begin data quality assessment on Atos platform immediately (before SBS integration); establish data remediation workstream; define acceptable reconciliation tolerances with actuarial input; automate reconciliation reporting

**Contingency Plan**: If systemic issues found, extend parallel-run and establish dedicated data remediation team; engage NAO early to manage audit expectations; communicate transparently with Treasury about impact on timeline

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Programme budget approval (>£10M) | NS&I CFO | HM Treasury | NS&I CEO, Programme Director | PAC (via reports), NAO |
| Programme budget allocation (<£10M) | Programme Director | NS&I CFO | NS&I CTO, Product Owners | HM Treasury |
| Architecture decisions (strategic) | Chief Architect | NS&I CTO | SBS, CISO, Ops Director | Programme Board |
| Architecture decisions (component) | Solution Architects | Chief Architect | SBS, relevant Product Owner | Programme Director |
| SBS contract variations | Programme Director | NS&I CEO | NS&I CFO, CCS, Legal | HM Treasury |
| Security accreditation (go/no-go) | NS&I CISO | NS&I CTO | NCSC, PCI QSA, DPO | Programme Board, FCA, PRA |
| Customer migration (go/no-go) | Ops Director | NS&I CEO | CISO, CTO, Customer Svcs | HM Treasury, FCA, PRA, Customers |
| Atos exit milestones | Programme Director | NS&I CEO | Atos, Ops Director, CFO | HM Treasury |
| Consultant engagement/renewal | Programme Director | NS&I CFO | NS&I CTO, HR Director | PAC (aggregate reporting) |
| Requirements prioritisation | Product Owners | Programme Director | Chief Architect, End Users | SBS, Delivery Teams |
| Risk escalation (>programme level) | Programme Director | NS&I CEO | NS&I Board, HM Treasury | IPA, PAC (if material) |

### Escalation Path

1. **Level 1 — Programme Delivery**: Programme Director and Product Owners resolve day-to-day delivery decisions, SBS integration issues, and team resource allocation (response: within 2 working days)
2. **Level 2 — Programme Steering Committee**: NS&I CTO chairs; resolves scope changes, technical trade-offs, inter-workstream dependencies, and budget reallocation within approved envelope (response: within 5 working days; meets weekly)
3. **Level 3 — NS&I Programme Board**: NS&I CEO chairs; resolves strategic direction, major contract decisions, significant risk escalations, and budget requests exceeding approved envelope (response: within 10 working days; meets monthly)
4. **Level 4 — HM Treasury Sponsor**: Treasury Sponsor Team; resolves funding approvals, Ministerial briefings, and programme continuation decisions (response: as required; formal quarterly review)
5. **Level 5 — Ministerial / Parliamentary**: Chancellor's office; for decisions requiring Ministerial Direction or parliamentary approval (exceptional circumstances only)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| NS&I Chief Executive | PENDING | — | PENDING |
| NS&I CTO | PENDING | — | PENDING |
| NS&I CFO | PENDING | — | PENDING |
| Programme Director | PENDING | — | PENDING |
| HM Treasury Sponsor | PENDING | — | PENDING |
| Atos Transition Lead | PENDING | — | PENDING |
| SBS Delivery Lead | PENDING | — | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (NS&I CEO) | | | |
| Programme Director | | | |
| HM Treasury Sponsor | | | |

---

## Appendices

### Appendix A: Stakeholder Interview Summaries

#### Interview with HM Treasury Sponsor Team — PENDING

**Key Points**:
- To be conducted as part of programme reset activities
- Focus: funding conditions, reporting requirements, oversight expectations

**Follow-up Actions**:
- Schedule introductory meeting with Treasury sponsor team
- Agree monthly reporting format and content

---

#### Interview with PAC Clerk — PENDING

**Key Points**:
- To be conducted following formal PAC response submission
- Focus: evidence requirements, future hearing expectations

**Follow-up Actions**:
- Submit Treasury Minute within 60-day deadline
- Prepare evidence pack for potential follow-up hearing

---

#### Interview with Atos UK Managing Director — PENDING

**Key Points**:
- To be conducted as part of exit planning
- Focus: exit timeline, knowledge transfer approach, key personnel retention

**Follow-up Actions**:
- Initiate formal exit planning discussions
- Identify critical Atos personnel for retention

---

#### Interview with SBS UK Country Director — PENDING

**Key Points**:
- To be conducted as part of delivery planning
- Focus: platform readiness, customisation approach, UK deployment model

**Follow-up Actions**:
- Arrange SBS platform deep-dive for NS&I architecture team
- Begin fit-gap analysis for NS&I product set

---

### Appendix B: Survey Results

Stakeholder surveys to be conducted as part of programme reset. Recommended approach:
- Anonymous online survey to all programme staff (NS&I, Atos, SBS, consultants)
- Focus: confidence in programme delivery, perception of governance, cultural readiness
- Repeat quarterly to track change

---

### Appendix C: References

| Reference | Document |
|-----------|----------|
| Architecture Principles | ARC-000-PRIN-v1.0 |
| PAC Report (Feb 2026) | "NS&I Digital Modernisation Programme" — Public Accounts Committee |
| NAO Assessment | National Audit Office assessment of NS&I programme costs and governance |
| PRA SS1/21 | Supervisory Statement on Operational Resilience |
| NCSC CAF | Cyber Assessment Framework |
| PCI DSS v4.0 | Payment Card Industry Data Security Standard |
| GDS Service Standard | 14-point standard for government digital services |
| Technology Code of Practice | Cross-government technology standards |
| HM Treasury Orange Book | Risk Management — Principles and Concepts |
| HM Treasury Green Book | Appraisal and Evaluation in Central Government |
| Managing Public Money | HM Treasury guidance on financial management |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| *None provided* | — | — | — | — |

> External documents (org charts, governance structures, existing stakeholder maps) can be placed in `projects/001-core-banking-migration/external/` to enhance future revisions of this analysis.

---

**Generated by**: ArcKit `/arckit:stakeholders` command
**Generated on**: 2026-02-13
**ArcKit Version**: 2.4.4
**Project**: NS&I Core Banking Migration (Project 001)
**AI Model**: Claude Opus 4.6
