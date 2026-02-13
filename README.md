# NS&I Digital Modernisation Programme — Architecture Governance

An architecture governance project using [ArcKit](https://github.com/tractorjuice/arc-kit) to design and govern the **National Savings and Investments (NS&I) Digital Modernisation Programme** (formerly "Project Rainbow").

## Background

National Savings and Investments (NS&I) is the UK's state-owned savings bank, an executive agency of HM Treasury, serving approximately 24 million customers with over £230 billion in savings. NS&I outsourced its back-office operations and core banking platform to Atos (formerly Siemens IT Solutions and Services) in 1999.

The digital modernisation programme was launched to replace legacy systems with a cloud-native platform. By end of 2024, the programme had cost an estimated **£3 billion** — **£1.3 billion over budget** — and was described by the Public Accounts Committee as a **"full-spectrum disaster"**. The core banking engine replacement, planned to use SBS (formerly Sopra Banking Software) SBP Digital Core platform, is classified as "extremely high-risk" with main work yet to start and a target go-live of 2028.

This project models a **reference architecture** for how the programme should be delivered, covering core banking migration, digital channel modernisation, and programme governance.

## Programme Workstreams

| ID | Workstream | Description |
|----|-----------|-------------|
| 001 | **Core Banking Migration** | Atos legacy platform to SBS SBP Digital Core. Core ledger, transaction processing, product engine, regulatory reporting. |
| 002 | **Digital Channels & Operations** | Customer-facing digital services, back-office modernisation, contact centre integration. |
| 003 | **Programme Governance & Assurance** | Programme management, cost control, risk management, Treasury oversight, consultant accountability. |

## Regulatory & Compliance Context

| Framework | Description |
|-----------|-------------|
| **GDS Service Standard** | 14-point standard for government digital services |
| **Technology Code of Practice (TCoP)** | Cross-government technology standards |
| **NCSC Cyber Assessment Framework (CAF)** | National cybersecurity standards |
| **PCI DSS** | Payment Card Industry Data Security Standard |
| **FCA Regulations** | Financial Conduct Authority operational resilience |
| **PRA SS1/21** | Operational resilience for financial services |
| **Orange Book** | HM Treasury risk management guidance |
| **Green Book** | HM Treasury appraisal and evaluation |
| **Managing Public Money** | HM Treasury financial management |
| **G-Cloud 14 (RM1557.14)** | Crown Commercial Service cloud procurement |
| **UK GDPR / DPA 2018** | Data protection legislation |
| **HMG Security Policy Framework** | Government security classifications |

## Architecture Artifacts

Generated using ArcKit `/arckit.*` commands.

| Artifact | Command | Status |
|----------|---------|--------|
| Architecture Principles | `/arckit.principles` | Generated |
| Stakeholder Analysis | `/arckit.stakeholders` | Pending |
| Risk Register | `/arckit.risk` | Pending |
| Business Case (SOBC) | `/arckit.sobc` | Pending |
| Requirements | `/arckit.requirements` | Pending |
| Platform Design | `/arckit.platform-design` | Pending |
| Data Model | `/arckit.data-model` | Pending |
| DPIA | `/arckit.dpia` | Pending |
| Wardley Map | `/arckit.wardley` | Pending |
| Cloud Research (AWS) | `/arckit.aws-research` | Pending |
| Cloud Research (Azure) | `/arckit.azure-research` | Pending |
| Secure by Design | `/arckit.secure` | Pending |
| FinOps Strategy | `/arckit.finops` | Pending |
| DevOps Strategy | `/arckit.devops` | Pending |

## Getting Started

```bash
# Start Claude Code in this directory
claude

# Architecture principles are already established
# Follow the dependency order in DEPENDENCY-MATRIX.md for each workstream

# Core Banking Migration (Project 001)
/arckit.stakeholders NS&I Core Banking Migration - Atos to SBS SBP Digital Core platform replacement
/arckit.risk NS&I Core Banking Migration - legacy core banking engine replacement
/arckit.requirements NS&I Core Banking Migration - cloud-native core banking platform

# Digital Channels (Project 002)
/arckit.stakeholders NS&I Digital Channels - customer-facing digital services modernisation
/arckit.requirements NS&I Digital Channels - web, mobile, API and back-office modernisation

# Programme Governance (Project 003)
/arckit.stakeholders NS&I Programme Governance - programme management and Treasury oversight
/arckit.risk NS&I Programme Governance - programme delivery risk and cost control
```

## Key References

- [PAC Report: NS&I Digital Modernisation (Feb 2026)](https://committees.parliament.uk/committee/127/public-accounts-committee/)
- [NAO Report: NS&I Digital Modernisation](https://www.nao.org.uk/)
- [NS&I Official Website](https://www.nsandi.com/)
- [GDS Service Standard](https://www.gov.uk/service-manual/service-standard)
- [Technology Code of Practice](https://www.gov.uk/guidance/the-technology-code-of-practice)
- [NCSC Cyber Assessment Framework](https://www.ncsc.gov.uk/collection/caf)
- [Crown Commercial Service — G-Cloud 14](https://www.crowncommercial.gov.uk/agreements/RM1557.14)
- [SBS (Sopra Banking Software)](https://www.soprabanking.com/)

---

Generated with [ArcKit](https://github.com/tractorjuice/arc-kit) v2.4.4
