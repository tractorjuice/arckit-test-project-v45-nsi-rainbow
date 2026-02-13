# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an **ArcKit architecture governance project** — not a software codebase. It generates architecture documents (markdown) for the **National Savings and Investments (NS&I) Digital Modernisation Programme** (formerly "Project Rainbow").

There is no build system, test suite, or application code. All work is done through ArcKit slash commands that generate governance artifacts.

## NS&I Programme Context

### Organisation Background

**National Savings and Investments (NS&I)** is the UK's state-owned savings bank, backed by HM Treasury. Established 160 years ago, NS&I serves approximately **24 million customers** and manages over **£230 billion** in savings products (Premium Bonds, Income Bonds, Direct Saver, etc.). NS&I is both an executive agency of the Chancellor of the Exchequer and an arm's-length body of HM Treasury.

### The Digital Modernisation Programme

NS&I's digital modernisation programme (originally codenamed "Project Rainbow") was designed to replace legacy back-office operations and the core banking platform. The programme has been the subject of significant scrutiny from the Public Accounts Committee (PAC) and the National Audit Office (NAO).

**Key facts (as of February 2026):**
- Programme cost: **estimated £3bn** by end of 2024, with costs increasing by **£1.3bn** since inception
- Additional funding: **£109m** confirmed by government in January 2026 (pending parliamentary approval)
- Consultant spend: **£43m** on external consultants, with accountability concerns
- Core banking replacement: **main work yet to start** — classified as "extremely high-risk" by PAC
- Target go-live for SBS Digital Core: **2028**

### Current State (Legacy)

- **Core banking platform**: Provided by **Atos** (formerly Siemens IT Solutions and Services) under an outsourcing contract since **1999**
- **Back-office operations**: Outsourced to Atos since 1999
- **Technology stack**: Legacy on-premises systems, monolithic architecture
- **Known issues**: Ageing platform, limited digital capabilities, dependency on single outsourcing partner

### Target State

- **Core banking engine**: **SBS** (formerly Sopra Banking Software) **SBP Digital Core** platform — cloud-native
- **Architecture approach**: Cloud-native, microservices, API-first
- **Target delivery**: 2028 for core banking replacement

### PAC / NAO Findings (February 2026)

The PAC report described the programme as a **"full-spectrum disaster"**:
- NS&I has **no workable plan** after five years
- NS&I **lacks the skills** to deliver the programme
- NS&I has **no idea of the eventual cost**
- NS&I was **unable to tell the PAC how much had been spent** to date
- A **"good news" culture** means decisions are not being made and disagreements not resolved
- NS&I was **"over-confident"** about delivery capabilities with little evidence
- HM Treasury **should have intervened earlier** after serious setbacks
- The core banking engine replacement is an **"extremely high-risk element"**
- £43m spent on consultants with NS&I being **"vague on how it holds them to account"**

### Key Stakeholders

| Stakeholder | Role | Relevance |
|-------------|------|-----------|
| **NS&I Board** | Programme owner | Strategic direction, delivery accountability |
| **HM Treasury** | Sponsoring department | Funding, oversight, intervention |
| **Public Accounts Committee (PAC)** | Parliamentary scrutiny | Cost accountability, value for money |
| **National Audit Office (NAO)** | Independent audit | Programme cost and delivery assessment |
| **Atos** | Incumbent outsourcing partner | Legacy core banking, back-office operations (since 1999) |
| **SBS (Sopra Banking Software)** | New platform vendor | SBP Digital Core cloud-native platform |
| **NS&I Customers (24M)** | End users | Service continuity, digital experience |
| **UK Taxpayers** | Funders | Value for money, risk exposure |
| **Infrastructure & Projects Authority (IPA)** | Programme assurance | Delivery confidence assessment |
| **Geoffrey Clifton-Brown MP** | PAC Chair | Parliamentary accountability |

### Three Programme Workstreams

This project is organised into three workstreams:

| Project ID | Workstream | Scope |
|------------|-----------|-------|
| **001** | **Core Banking Migration** | Atos legacy platform → SBS SBP Digital Core. Database migration, core ledger, transaction processing, product engine, regulatory reporting. The "extremely high-risk" element. |
| **002** | **Digital Channels & Operations** | Customer-facing digital services (web, mobile, API), back-office workflow modernisation, document management, customer contact centre integration. |
| **003** | **Programme Governance & Assurance** | Programme management framework, cost control, risk management, Treasury oversight, consultant accountability, PAC recommendations, skills and capability development. |

## How to Work in This Repository

### ArcKit Slash Commands

All artifacts are produced via `/arckit.*` commands. The recommended execution order follows the 12-tier dependency hierarchy in `DEPENDENCY-MATRIX.md` (M=Mandatory, R=Recommended, O=Optional):

| Tier | Phase | Key Commands |
|------|-------|-------------|
| 0 | Foundation | `plan`, `principles` |
| 1 | Strategic Context | `stakeholders` |
| 1.5 | Risk Assessment | `risk` |
| 2 | Business Justification | `sobc` |
| 3 | Requirements | `requirements` |
| 3.5 | Strategic Planning | `platform-design`, `strategy` |
| 4 | Detailed Design | `data-model`, `dpia`, `research`, `wardley`, `roadmap`, `diagram`, `adr`, `datascout`, `data-mesh-contract` |
| 5 | Procurement | `sow`, `dos`, `gcloud-search`, `gcloud-clarify`, `evaluate` |
| 6 | Design Reviews | `hld-review`, `dld-review` |
| 7-8 | Implementation & Operations | `backlog`, `trello`, `servicenow`, `devops`, `mlops`, `finops`, `operationalize` |
| 9-10 | Quality & Compliance | `traceability`, `analyze`, `principles-compliance`, `service-assessment`, `tcop`, `ai-playbook`, `atrs`, `secure`, `mod-secure`, `jsp-936` |
| 11-12 | Reporting & Publishing | `story`, `pages` |

The most-consumed artifacts are `requirements` (37 commands), `principles` (21 commands), and `stakeholders` (22 commands).

### Key Conventions

- **Document IDs**: Format `ARC-{PROJECT_ID}-{TYPE}-v{VERSION}.md` (e.g., `ARC-001-REQ-v1.0.md`). Multi-instance types use `ARC-{PID}-{TYPE}-{NUM}-v{VERSION}.md`. Generate with `.arckit/scripts/bash/generate-document-id.sh`.
- **Type codes**: PRIN, STKE, REQ, RISK, SOBC, STRAT, PLAT, DATA, DPIA, RSCH, SOW, EVAL, TRAC, ANLZ, BKLG, SRVN, DVOP, MLOP, FNOP, OPER, RDMP, TCOP, AIPL, ATRS, SECD, MSBD, JSP9, SVCA, STRY. Multi-instance: ADR, DIAG, WARD, DMC.
- **Global artifacts** (principles) go in `projects/000-global/`
- **Project-specific artifacts** go in `projects/{PROJECT_ID}/` with subdirectories: `decisions/`, `diagrams/`, `wardley-maps/`, `data-contracts/`, `reviews/`, `external/`, `vendors/`, `final/`
- **Templates**: Default templates are provided by the ArcKit plugin. Custom overrides in `.arckit/templates/` or `.arckit/templates-custom/` take precedence. Always read the relevant template before generating a document.
- **Version** is in the `VERSION` file (currently 2.4.4) — include in generated document metadata
- **External documents**: Commands auto-discover user-provided files (vendor HLDs, policy docs, pen test reports) from `projects/{project}/external/`, `projects/{project}/vendors/{vendor}/`, and `projects/000-global/policies/`. These enhance output but are never required.

### Autonomous Agents

Research-heavy commands (`/arckit.research`, `/arckit.datascout`, `/arckit.aws-research`, `/arckit.azure-research`, `/arckit.gcp-research`) delegate to autonomous agents that run in isolated context windows via the Task tool.

### MCP Integration

The ArcKit plugin bundles MCP servers for AWS Knowledge and Microsoft Learn for cloud research via `/arckit.aws-research` and `/arckit.azure-research`.

### Generated Artifacts (This Project)

Global architecture principles have been established. Per-workstream artifacts should be generated following the dependency order in `DEPENDENCY-MATRIX.md`.

| Artifact | Location | Status |
|----------|----------|--------|
| Architecture Principles | `projects/000-global/ARC-000-PRIN-v1.0.md` | Generated |
| Core Banking — all others | `projects/001-core-banking-migration/` | Pending |
| Digital Channels — all others | `projects/002-digital-channels/` | Pending |
| Programme Governance — all others | `projects/003-programme-governance/` | Pending |

## UK Government & Financial Services Context

### Regulatory Frameworks

| Framework | Description | Relevance |
|-----------|-------------|-----------|
| **GDS Service Standard** | 14-point standard for government digital services | All customer-facing services |
| **Technology Code of Practice (TCoP)** | Cross-government technology standards | All technology decisions |
| **NCSC Cyber Assessment Framework (CAF)** | National cybersecurity standards | Core banking security |
| **HMG Security Policy Framework** | Government security classifications | Data handling, OFFICIAL-SENSITIVE |
| **PCI DSS** | Payment Card Industry Data Security Standard | Card transaction processing |
| **FCA Regulations** | Financial Conduct Authority requirements | Customer protection, operational resilience |
| **PRA Supervisory Statement SS1/21** | Operational resilience for financial services | Core banking availability |
| **Orange Book** | HM Treasury risk management guidance | Programme risk framework |
| **Green Book** | HM Treasury appraisal and evaluation | Business case methodology |
| **Managing Public Money** | HM Treasury financial management | Cost control, VfM |
| **G-Cloud 14 (RM1557.14)** | Crown Commercial Service cloud procurement | Cloud service procurement |
| **Digital Outcomes and Specialists (DOS)** | CCS digital services procurement | Specialist and consultancy procurement |
| **UK GDPR / Data Protection Act 2018** | Data protection legislation | Customer data handling |
| **Public Records Act 1958** | Records management obligations | Document retention |

### Key References

- NS&I is classified as an **Executive Agency and NDPB** of HM Treasury
- Security classification: **OFFICIAL** (with OFFICIAL-SENSITIVE for financial data)
- Data residency: **UK only** (sovereign cloud requirements)
- Dual-running period: Legacy Atos platform must operate alongside new SBS platform during migration
- 24 million customers — service continuity is paramount
- Premium Bonds: NS&I's flagship product, prize draw system must have zero downtime during migration
