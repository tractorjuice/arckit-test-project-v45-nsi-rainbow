# Risk Register

> **Template Status**: Live | **Version**: 2.4.4 | **Command**: `/arckit:risk`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-RISK-v1.0 |
| **Document Type** | Risk Register |
| **Project** | NS&I Core Banking Migration (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-13 |
| **Last Modified** | 2026-02-13 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-03-13 |
| **Owner** | NS&I Programme Director, Core Banking |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NS&I Programme Board, HM Treasury Sponsor Team, IPA Review Team, NS&I Audit Committee |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-13 | ArcKit AI | Initial creation from `/arckit:risk` command | PENDING | PENDING |

### Source Documents

| Document | ID | Key Extractions |
|----------|----|-----------------|
| Stakeholder Drivers & Goals | ARC-001-STKE-v1.0 | 15 drivers, RACI matrix (risk owners), 4 conflicts (conflict-derived risks), 6 stakeholder risks |
| Requirements | ARC-001-REQ-v1.0 | 60 requirements, 8 identified risks, NFR targets (mitigation benchmarks) |
| Architecture Principles | ARC-000-PRIN-v1.0 | 10 principles (P1–P10), non-compliance creates compliance risks |
| Risk Appetite Statement | Not available | Using NS&I/UK Government default appetite thresholds |

---

## Executive Summary

### Risk Profile Overview

**Total Risks Identified:** 20 risks across 6 categories

| Risk Level | Inherent | Residual | Change |
|------------|----------|----------|--------|
| **Critical** (20-25) | 7 | 2 | ↓ 71% |
| **High** (13-19) | 8 | 5 | ↓ 38% |
| **Medium** (6-12) | 5 | 10 | ↑ (absorbed from higher) |
| **Low** (1-5) | 0 | 3 | ↑ (absorbed from higher) |
| **TOTAL Score** | 296 | 192 | ↓ 35% |

### Risk Category Distribution

| Category | Count | Avg Inherent | Avg Residual | Control Effectiveness |
|----------|-------|--------------|--------------|----------------------|
| **STRATEGIC** | 4 | 17.3 | 11.8 | 32% reduction |
| **OPERATIONAL** | 4 | 16.3 | 10.0 | 39% reduction |
| **FINANCIAL** | 3 | 14.7 | 9.7 | 34% reduction |
| **COMPLIANCE** | 3 | 15.0 | 9.7 | 35% reduction |
| **REPUTATIONAL** | 3 | 16.0 | 10.0 | 38% reduction |
| **TECHNOLOGY** | 3 | 14.3 | 9.0 | 37% reduction |

### Overall Risk Assessment

**Overall Residual Risk Score:** 192/500
**Risk Reduction from Controls:** 35% reduction from inherent risk
**Risk Profile Status:** ⚠️ Concerning

This programme carries a risk profile that is significantly above typical government programmes, reflecting the combination of scale (24M customers, £230bn assets), technical complexity (27-year legacy platform replacement), political scrutiny (PAC "full-spectrum disaster" finding), and organisational capability gaps. The residual risk profile is manageable but requires active executive attention and cannot be delegated.

### Risks Exceeding Appetite

**Number of risks exceeding organisational appetite:** 7 risks

| Risk ID | Title | Category | Residual Score | Appetite | Excess | Escalation |
|---------|-------|----------|----------------|----------|--------|------------|
| R-001 | "Good news" culture persists | STRATEGIC | 16 | 12 | +4 | NS&I Board |
| R-005 | Service disruption during cutover | OPERATIONAL | 12 | 9 | +3 | NS&I CEO |
| R-006 | Premium Bonds draw disrupted | OPERATIONAL | 12 | 9 | +3 | NS&I CEO |
| R-009 | Programme costs exceed funding envelope | FINANCIAL | 12 | 9 | +3 | HM Treasury |
| R-013 | SBS fails regulatory accreditation on time | COMPLIANCE | 12 | 6 | +6 | NS&I CISO |
| R-016 | Further PAC criticism escalates | REPUTATIONAL | 12 | 6 | +6 | NS&I CEO |
| R-017 | Customer data breach during migration | REPUTATIONAL | 12 | 6 | +6 | NS&I CISO |

### Top 5 Critical Risks Requiring Immediate Attention

1. **R-001** (STRATEGIC, Residual 16): "Good news" culture persists despite PAC findings — Owner: NS&I CEO
2. **R-002** (STRATEGIC, Residual 15): NS&I cannot recruit sufficient in-house capability — Owner: NS&I CTO
3. **R-005** (OPERATIONAL, Residual 12): Service disruption during customer migration cutover — Owner: NS&I Operations Director
4. **R-013** (COMPLIANCE, Residual 12): SBS platform fails regulatory accreditation on time — Owner: NS&I CISO
5. **R-016** (REPUTATIONAL, Residual 12): Further PAC/media criticism undermines programme — Owner: NS&I CEO

### Key Findings and Recommendations

**Key Findings:**
- Heavy concentration of critical risks in STRATEGIC and OPERATIONAL categories — reflecting organisational capability gaps and technical complexity
- 7 of 20 risks exceed appetite even after controls — programme cannot proceed without Board and Treasury acceptance
- The single highest residual risk (R-001: culture) is non-technical — no amount of technology controls can mitigate a governance culture problem
- Atos transition creates a cluster of 4 interdependent risks (R-003, R-004, R-005, R-019) — failure of any one cascades to the others
- NS&I CEO owns 5 risks personally — disproportionate concentration that could overwhelm executive bandwidth

**Recommendations:**
1. **URGENT**: Escalate all 7 appetite-exceeding risks to NS&I Board for formal acceptance or additional mitigation
2. **URGENT**: Engage independent culture assessment to address R-001 — the PAC's most fundamental finding
3. **HIGH**: Establish Atos Transition Risk Cluster governance — dedicated steering for the 4 interdependent exit risks
4. **HIGH**: Accelerate permanent recruitment (R-002) with DDaT pay exception requests to Treasury
5. **MEDIUM**: Delegate 2-3 risks from NS&I CEO to reduce concentration; appoint Deputy SRO for risk delegation

---

## A. Risk Matrix Visualization

### Inherent Risk Matrix (Before Controls)

```
                                    IMPACT
              1-Minimal   2-Minor    3-Moderate   4-Major    5-Severe
           ┌───────────┬───────────┬───────────┬───────────┬───────────┐
5-Almost   │           │           │           │  R-001    │  R-005    │
Certain    │    5      │    10     │    15     │  R-003    │  R-006    │
           │           │           │           │    20     │    25     │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
4-Likely   │           │           │  R-011    │  R-002    │  R-009    │
           │    4      │    8      │  R-020    │  R-004    │  R-016    │
           │           │           │    12     │  R-010    │    20     │
L          │           │           │           │    16     │           │
I          ├───────────┼───────────┼───────────┼───────────┼───────────┤
K 3-Possible│          │           │  R-007    │  R-013    │  R-017    │
E          │    3      │    6      │  R-008    │  R-014    │           │
L          │           │           │  R-015    │  R-018    │    15     │
I          │           │           │    9      │  R-019    │           │
H          │           │           │           │    12     │           │
O          ├───────────┼───────────┼───────────┼───────────┼───────────┤
O 2-Unlikely│          │           │  R-012    │           │           │
D          │    2      │    4      │    6      │    8      │    10     │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
  1-Rare   │           │           │           │           │           │
           │    1      │    2      │    3      │    4      │    5      │
           └───────────┴───────────┴───────────┴───────────┴───────────┘

Legend: Critical (20-25)  High (13-19)  Medium (6-12)  Low (1-5)
```

### Residual Risk Matrix (After Controls)

```
                                    IMPACT
              1-Minimal   2-Minor    3-Moderate   4-Major    5-Severe
           ┌───────────┬───────────┬───────────┬───────────┬───────────┐
5-Almost   │           │           │           │           │           │
Certain    │    5      │    10     │    15     │    20     │    25     │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
4-Likely   │           │           │  R-003    │  R-001    │           │
           │    4      │    8      │    12     │    16     │    20     │
L          ├───────────┼───────────┼───────────┼───────────┼───────────┤
I 3-Possible│          │  R-011    │  R-005    │  R-002    │           │
K          │    3      │  R-020   │  R-006    │    15     │    15     │
E          │           │    6      │  R-009    │           │           │
L          │           │           │  R-013    │           │           │
I          │           │           │  R-016    │           │           │
H          │           │           │  R-017    │           │           │
O          │           │           │    9-12   │           │           │
O          ├───────────┼───────────┼───────────┼───────────┼───────────┤
D 2-Unlikely│          │  R-007    │  R-004    │  R-010    │           │
           │    2      │  R-008    │  R-014    │  R-018    │    10     │
           │           │  R-012    │  R-015    │  R-019    │           │
           │           │  R-015    │    6      │    8      │           │
           │           │    4      │           │           │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
  1-Rare   │           │           │           │           │           │
           │    1      │    2      │    3      │    4      │    5      │
           └───────────┴───────────┴───────────┴───────────┴───────────┘

Legend: Critical (20-25)  High (13-19)  Medium (6-12)  Low (1-5)
```

**Risk Movement Analysis:**
- **Critical → High**: R-001 (20→16) — culture change takes time, limited control effectiveness
- **Critical → Medium**: R-005 (25→12), R-006 (25→12) — parallel-run and rehearsals significantly reduce operational risk
- **Critical → Medium**: R-009 (20→12), R-016 (20→12) — governance and cost controls reduce but cannot eliminate
- **High → Medium**: R-004 (16→8), R-010 (16→8), R-018 (12→8), R-019 (12→8) — mitigations effective
- **Medium → Low**: R-012 (6→4) — low inherent risk, good controls

---

## B. Top 10 Risks (Ranked by Residual Score)

| Rank | ID | Title | Category | Inherent | Residual | Owner | Status | Response |
|------|----|-------|----------|----------|----------|-------|--------|----------|
| 1 | R-001 | "Good news" culture persists | STRATEGIC | 20 | 16 | NS&I CEO | Open | Treat |
| 2 | R-002 | Insufficient in-house capability | STRATEGIC | 16 | 15 | NS&I CTO | In Progress | Treat |
| 3 | R-005 | Service disruption during cutover | OPERATIONAL | 25 | 12 | Ops Director | Open | Treat |
| 4 | R-006 | Premium Bonds draw disrupted | OPERATIONAL | 25 | 12 | Ops Director | Open | Treat |
| 5 | R-009 | Programme costs exceed funding | FINANCIAL | 20 | 12 | NS&I CFO | Open | Treat |
| 6 | R-013 | SBS fails regulatory accreditation | COMPLIANCE | 12 | 12 | NS&I CISO | Open | Treat |
| 7 | R-016 | Further PAC/media criticism | REPUTATIONAL | 20 | 12 | NS&I CEO | In Progress | Treat |
| 8 | R-017 | Customer data breach during migration | REPUTATIONAL | 15 | 12 | NS&I CISO | Open | Treat |
| 9 | R-003 | Key Atos staff depart before KT | OPERATIONAL | 20 | 12 | Programme Dir. | In Progress | Treat |
| 10 | R-010 | SBS contract variations escalate costs | FINANCIAL | 16 | 8 | NS&I CFO | Open | Treat |

---

## C. Detailed Risk Register

### Risk R-001: "Good News" Culture Persists Despite PAC Findings

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** NS&I Chief Executive (from STKE RACI: Accountable for governance)
**Action Owner:** Programme Director

#### Risk Identification

**Risk Description:**
NS&I's organisational culture continues to suppress bad news, filter risk reporting, and present over-optimistic progress to senior stakeholders and external bodies. This was the PAC's most fundamental finding — a "good news culture" that prevents decisions being made and disagreements resolved. If this persists, no amount of process improvement will succeed because information reaching decision-makers will be unreliable.

**Root Cause:**
Deeply embedded organisational behaviour reinforced over years; fear of consequences for reporting bad news; lack of psychological safety; senior leaders who do not model honest reporting; absence of independent assurance channels.

**Trigger Events:**
- Programme reports consistently show green/amber status while delivery slips
- Risk register not updated despite obvious deteriorating conditions
- Stakeholders surprised by problems that were known internally weeks earlier
- IPA assessors find material discrepancy between internal reporting and reality

**Consequences if Realized:**
- Decisions made on inaccurate information leading to further programme failure
- Further PAC hearings with even more damaging conclusions
- Loss of Treasury confidence, potential funding withdrawal
- Programme leadership changes (CEO/Programme Director replacement)
- Continued pattern of overcommit and underdeliver

**Affected Stakeholders:**
- **HM Treasury** (SD-1): Cannot make informed funding decisions
- **PAC/NAO** (SD-2, SD-11): Recommendations not implemented despite commitments
- **NS&I CEO** (SD-3): Personal accountability for repeated failure

**Related Objectives:**
- Goal G-6: Demonstrate transparent governance — directly threatened
- Goal G-1: Establish credible cost baseline — undermined by filtered reporting
- Outcome O-1: Restored financial credibility — impossible without honest culture

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | PAC explicitly found this culture exists; organisational cultures are notoriously resistant to change; no evidence yet of meaningful culture shift |
| **Impact** | 5 - Catastrophic | Undermines the entire governance framework; every other risk is harder to manage when reporting is unreliable; programme cancellation becomes possible |
| **Inherent Risk Score** | **20** (Critical) | 4 × 5 = 20 |

#### Current Controls and Mitigations

1. **PAC recommendations requiring honest reporting**
   - Effectiveness: **Weak** — external pressure alone does not change culture
   - Evidence: PAC has been critical for years without culture changing

2. **Independent assurance (IPA quarterly reviews)**
   - Effectiveness: **Adequate** — provides external check but only quarterly snapshot
   - Evidence: IPA reviews do identify gaps, but recommendations can be slow to implement

3. **Architecture Principle P4 (Realistic Planning and Cost Transparency)**
   - Effectiveness: **Weak** — principle exists but no enforcement mechanism yet
   - Evidence: Principle is newly established, untested

**Overall Control Effectiveness:** Weak (reduces risk from 20 to 16 only)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Culture change has not yet started; external pressure creates defensive behaviours not openness |
| **Impact** | 4 - Major | Impact slightly reduced by external checks (IPA, NAO) that provide some independent reality check |
| **Residual Risk Score** | **16** (High) | 4 × 4 = 16 |

**Risk Reduction:** 20% reduction (20 → 16)

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT

**Rationale:** Risk exceeds appetite and is the foundational risk for the entire programme. Cannot be tolerated, transferred, or terminated. Must be actively mitigated through deliberate cultural intervention.

#### Action Plan

1. **Commission independent culture assessment**
   - Owner: NS&I CEO
   - Due Date: 2026-04-30
   - Expected Impact: Establish baseline, identify specific interventions

2. **Appoint independent assurance function with direct Board access**
   - Owner: Programme Director
   - Due Date: 2026-03-31
   - Expected Impact: Bypass filtering — reduce likelihood from 4 to 3

3. **Implement anonymous risk reporting channel**
   - Owner: NS&I Internal Audit
   - Due Date: 2026-03-15
   - Expected Impact: Create safe reporting pathway

4. **Require non-executive director (NED) challenge at every programme board**
   - Owner: NS&I CEO
   - Due Date: 2026-03-01
   - Expected Impact: External challenge embedded in governance

**Target Residual Risk:** Likelihood 3, Impact 4 = 12 (Medium)

---

### Risk R-002: NS&I Cannot Recruit Sufficient In-House Technical Capability

**Category:** STRATEGIC
**Status:** In Progress
**Risk Owner:** NS&I CTO (from STKE RACI: Accountable for capability)
**Action Owner:** NS&I HR Director

#### Risk Identification

**Risk Description:**
Government pay scales cannot attract sufficient senior banking technology professionals, leaving NS&I unable to meet the 30% permanent staff target (BR-4) and remaining dependent on consultants without accountability. The PAC found NS&I "lacked the skills" to deliver. If this risk materialises, NS&I cannot act as an intelligent client, cannot hold SBS or other vendors to account, and will repeat the pattern that created the current crisis.

**Root Cause:**
Civil service pay bands significantly below market for senior banking technology roles (£70-90K vs £120-180K market rate); government recruitment processes slow (3-6 months); NS&I not well-known as a technology employer; London/office location requirements limiting candidate pool.

**Trigger Events:**
- Technology leadership roles remain unfilled after 6 months of advertising
- Successful hires leave within 12 months for better-paying private sector roles
- Consultant-to-permanent conversion rate below 10%
- PAC follow-up hearing finds no improvement in capability

**Consequences if Realized:**
- Programme remains consultant-dependent (contradicting PAC recommendation)
- NS&I cannot evaluate SBS platform quality or hold SBS to account
- Architecture decisions made by consultants with no long-term accountability
- Further PAC criticism, potential Ministerial intervention
- Cost savings from consultant reduction not achieved (BR-8)

**Affected Stakeholders:**
- **PAC** (SD-2): Skills recommendation not implemented
- **NS&I CTO** (SD-4): Cannot build the team needed to deliver
- **Consultants/SIs** (SD-15): Extended engagements without clear exit path

**Related Objectives:**
- Goal G-3: Build in-house capability (30% by 2026, 50% by 2027) — directly threatened
- Outcome O-3: Capable and accountable organisation — at risk

#### Inherent Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Government pay constraints are structural; banking technology talent market is highly competitive; NS&I has no track record of technology recruitment |
| **Impact** | 4 - Major | Cannot be an intelligent client; programme remains vulnerable to the same accountability gap PAC identified |
| **Inherent Risk Score** | **16** (High) | 4 × 4 = 16 |

#### Current Controls

1. **DDaT pay framework exceptions available** — Effectiveness: **Adequate** — but process is slow and exception values still below market
2. **Non-financial benefits (pension, flexible working, mission)** — Effectiveness: **Adequate** — attractive to some candidates but insufficient alone

#### Residual Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Pay exceptions and benefits may attract some candidates; not guaranteed |
| **Impact** | 5 - Severe | If skill gap persists, programme delivery and PAC response both fail |
| **Residual Risk Score** | **15** (High) | 3 × 5 = 15 |

**Primary Response:** TREAT

#### Action Plan

1. **Submit DDaT pay exception requests for all 4 leadership roles** — Owner: HR Director — Due: 2026-03-31
2. **Engage specialist government technology recruiters** — Owner: HR Director — Due: 2026-03-15
3. **Launch NS&I Technology brand campaign** — Owner: HR/Comms — Due: 2026-04-30
4. **Explore secondment pipeline from other government departments** — Owner: CTO — Due: 2026-04-30

**Target Residual Risk:** Likelihood 2, Impact 4 = 8 (Medium)

---

### Risk R-003: Key Atos Staff Depart Before Knowledge Transfer Complete

**Category:** OPERATIONAL
**Status:** In Progress
**Risk Owner:** Programme Director (from STKE RACI: Accountable for Atos exit)
**Action Owner:** Atos Transition Lead (joint)

#### Risk Identification

**Risk Description:**
Critical Atos personnel with unique knowledge of legacy system behaviours, undocumented configurations, and operational workarounds leave or are redeployed before knowledge transfer is complete. Given Atos's own financial restructuring, staff retention is uncertain. An estimated 20-30 individuals hold knowledge that exists nowhere else.

**Root Cause:**
Atos financial pressures leading to restructuring; individuals seeking employment elsewhere before exit completes; knowledge not documented because it was never required to be; 27 years of accumulated tribal knowledge.

**Trigger Events:**
- 3+ critical Atos personnel resign in same quarter
- Knowledge transfer milestones missed for 2 consecutive quarters
- Migration testing reveals undocumented system behaviours that no remaining staff can explain

**Consequences if Realized:**
- Irrecoverable knowledge gaps in legacy system understanding
- Extended parallel-run as team learns by observation rather than transfer
- Data migration errors from misunderstood system behaviours
- Potential service disruption during cutover
- Additional consultant costs to bring in legacy system archaeologists

**Affected Stakeholders:**
- **Atos** (SD-8): Reputation for managed exit at risk
- **NS&I Operations Director** (SD-5): Service continuity threatened
- **NS&I CTO** (SD-4): Technical delivery dependent on legacy knowledge

**Related Objectives:**
- Goal G-5: Managed Atos exit — directly threatened
- Goal G-2: Zero customer incidents — indirectly threatened

#### Inherent Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 5 - Almost Certain | Atos in financial difficulty; staff naturally seek security; 27 years of undocumented knowledge virtually guarantees gaps |
| **Impact** | 4 - Major | Knowledge gaps delay migration, increase testing costs, risk service disruption |
| **Inherent Risk Score** | **20** (Critical) | 5 × 4 = 20 |

#### Current Controls

1. **Atos contractual exit obligations** — Effectiveness: **Adequate** — contractual but enforcement limited if staff leave voluntarily
2. **Knowledge transfer programme initiated** — Effectiveness: **Weak** — early stages, coverage limited

#### Residual Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Contractual obligations help but cannot prevent voluntary departures |
| **Impact** | 3 - Moderate | If caught early, documentation sprints can partially compensate |
| **Residual Risk Score** | **12** (Medium) | 4 × 3 = 12 |

**Primary Response:** TREAT

#### Action Plan

1. **Identify 20-30 critical Atos personnel immediately; negotiate personal retention incentives** — Owner: Programme Director — Due: 2026-03-15
2. **Begin video-recorded system walkthrough programme** — Owner: NS&I Chief Architect — Due: 2026-03-31
3. **Establish documentation sprints (2-week intensive KT sessions per system)** — Owner: Atos Transition Lead — Due: 2026-04-30
4. **Create "legacy system archaeology" contingency contract with specialist firm** — Owner: Programme Director — Due: 2026-05-31

**Target Residual Risk:** Likelihood 3, Impact 3 = 9 (Medium)

---

### Risk R-004: SBS Requires Extensive Customisation for NS&I Products

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** NS&I CTO (from STKE RACI: Accountable for architecture decisions)
**Action Owner:** NS&I Chief Architect

#### Risk Identification

**Risk Description:**
NS&I's unique product set — particularly the Premium Bonds prize draw algorithm, government-backed savings guarantees, and NS&I-specific regulatory requirements — requires significant customisation of the SBS SBP Digital Core platform beyond standard configuration. Extensive customisation increases cost, extends timeline, creates deeper vendor dependency, and introduces technical risk.

**Root Cause:**
NS&I products are unique in the UK market (government-backed, Premium Bonds prize mechanism); SBS platform designed for commercial banking products; fit-gap analysis not yet completed.

**Trigger Events:**
- Fit-gap analysis reveals >20% of NS&I requirements need custom development
- Premium Bonds draw algorithm cannot be implemented in SBS standard product engine
- SBS estimates for customisation exceed £50M or 12 months additional timeline

**Consequences if Realized:**
- Cost overrun of £50-200M for customisation
- Timeline extension of 6-18 months
- Deeper SBS vendor lock-in (contradicting Principle P7)
- Technical risk from untested custom code in production

**Affected Stakeholders:**
- **SBS** (SD-9): Delivery complexity increases; reference implementation value diminished
- **NS&I CFO** (SD-7): Cost escalation
- **NS&I Chief Architect** (SD-14): Architecture integrity compromised

**Related Objectives:**
- Goal G-4: SBS platform accreditation by Q2 2028 — timeline at risk
- Goal G-1: Cost baseline — budget assumptions invalidated

#### Inherent Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | NS&I products are genuinely unique; Premium Bonds has no commercial equivalent; some customisation virtually certain |
| **Impact** | 4 - Major | £50-200M cost impact; 6-18 month delay; increased vendor lock-in |
| **Inherent Risk Score** | **16** (High) | 4 × 4 = 16 |

#### Current Controls

1. **Architecture Principle P7 (Vendor Independence)** — Effectiveness: **Adequate** — provides framework for limiting customisation
2. **Standard-first approach mandated** — Effectiveness: **Adequate** — policy but untested against reality

#### Residual Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | If fit-gap analysis conducted early, customisation scope can be bounded and alternatives explored |
| **Impact** | 4 - Major | Even limited customisation carries significant cost and timeline impact |
| **Residual Risk Score** | **8** (Medium) | 2 × 4 = 8 |

**Primary Response:** TREAT

#### Action Plan

1. **Conduct comprehensive SBS fit-gap analysis for all NS&I products before committing to configuration** — Owner: Chief Architect — Due: 2026-06-30
2. **Prototype Premium Bonds draw on SBS platform early (proof of concept)** — Owner: SBS Delivery Lead — Due: 2026-06-30
3. **If customisation >20%, design dedicated microservice for Prize Draw logic outside SBS core** — Owner: Chief Architect — Due: 2026-09-30

**Target Residual Risk:** Likelihood 2, Impact 3 = 6 (Medium)

---

### Risk R-005: Service Disruption During Customer Migration Cutover

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** NS&I Operations Director (from STKE RACI: Accountable for customer migration go/no-go)
**Action Owner:** Programme Director

#### Risk Identification

**Risk Description:**
The cutover of customer accounts from Atos to SBS causes service disruption — accounts temporarily inaccessible, transactions lost, balances incorrect, or Premium Bonds draw delayed. With 24 million customers and £230 billion in assets, even a brief disruption would be national news.

**Root Cause:**
Unprecedented scale and complexity of migration; dual-platform synchronisation challenges; production environment differences from test; timing criticality for financial transactions.

**Trigger Events:**
- Cutover rehearsal reveals unresolvable issues requiring live workarounds
- Data reconciliation shows >0.0001% discrepancy rate at cutover time
- Atos platform instability during cutover window
- SBS platform performance degradation under full production load

**Consequences if Realized:**
- Customers unable to access accounts (hours to days)
- Financial transactions lost or duplicated
- Premium Bonds draw delayed or cancelled
- National media coverage; parliamentary emergency question
- FCA/PRA regulatory intervention
- Customer compensation claims (estimated exposure £100M+)

**Affected Stakeholders:**
- **NS&I Customers** (SD-10): Direct service impact
- **FCA/PRA** (SD-12): Regulatory concerns about operational resilience
- **PAC** (SD-2): Further evidence of programme failure

**Related Objectives:**
- Goal G-2: Zero customer incidents — directly threatened (MUST_HAVE requirement BR-2)
- Outcome O-2: Seamless customer migration — at risk

#### Inherent Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 5 - Almost Certain | Migration of this scale and complexity has inherent risk; production environments always differ from test; 27-year legacy has undocumented behaviours |
| **Impact** | 5 - Catastrophic | National service disruption; regulatory intervention; programme credibility destroyed |
| **Inherent Risk Score** | **25** (Critical) | 5 × 5 = 25 |

#### Current Controls

1. **Phased migration strategy (low-risk products first)** — Effectiveness: **Strong** — proven approach reduces blast radius
2. **Requirement for 3 cutover rehearsals before live** (FR-11) — Effectiveness: **Strong** — rehearsals identify most issues
3. **30-minute rollback capability** (FR-11) — Effectiveness: **Strong** — limits duration of any disruption
4. **99.9999% reconciliation target before cutover approval** (FR-8) — Effectiveness: **Strong** — high confidence threshold

#### Residual Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Multiple strong controls significantly reduce likelihood but cannot eliminate all production surprises |
| **Impact** | 4 - Major | Even with rollback, brief disruption and reputational damage still possible |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Primary Response:** TREAT

#### Action Plan

1. **Production-scale test environment mandatory** — Owner: CTO — Due: 2026-12-31
2. **Weekend cutover windows with extended monitoring** — Owner: Ops Director — Due: Per migration phase
3. **Customer communication plan for each cutover** — Owner: Customer Services Director — Due: Per migration phase

**Target Residual Risk:** Likelihood 2, Impact 4 = 8 (Medium)

---

### Risk R-006: Premium Bonds Prize Draw Disrupted During Migration

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** NS&I Operations Director
**Action Owner:** Programme Director

#### Risk Identification

**Risk Description:**
The Premium Bonds monthly prize draw — NS&I's highest-profile operation processing ~125 billion £1 bonds — is disrupted, delayed, or produces incorrect results during the migration period. This could occur during the dual-run synchronisation, during the dedicated Premium Bonds migration phase, or during the first draw on the SBS platform.

**Root Cause:**
Premium Bonds draw is computationally intensive, algorithmically complex, and has no commercial equivalent; migration of the draw system requires perfect accuracy; any perception of unfairness would be devastating.

**Trigger Events:**
- Draw processing exceeds the 12-hour window on SBS platform
- Reconciliation between Atos and SBS draw results shows discrepancies
- Draw auditor refuses to certify SBS-generated results
- Draw calculation produces statistically anomalous prize distribution

**Consequences if Realized:**
- National media coverage ("Premium Bonds draw broken by IT project")
- Customer panic about safety of holdings
- Regulatory investigation into draw fairness
- Programme credibility irrecoverably damaged
- Potential legal claims from customers

**Affected Stakeholders:**
- **NS&I Customers** (SD-10): Direct impact on prize draw fairness
- **NS&I CEO** (SD-3): Personal accountability for NS&I's flagship product
- **PAC** (SD-2): "Full-spectrum disaster" narrative reinforced

**Related Objectives:**
- Goal G-2: Zero customer incidents (BR-2) — MUST_HAVE
- FR-3: Premium Bonds Prize Draw System requirements

#### Inherent Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 5 - Almost Certain | The draw is uniquely complex; no off-the-shelf solution exists; any platform migration involves risk of calculation discrepancies |
| **Impact** | 5 - Catastrophic | Premium Bonds is NS&I's flagship; draw failure would be a national story and potentially fatal for the programme |
| **Inherent Risk Score** | **25** (Critical) | 5 × 5 = 25 |

#### Current Controls

1. **Premium Bonds migrated last in phased plan** (REQ migration order) — Effectiveness: **Strong** — team gains experience on simpler products first
2. **Extended parallel-run for Premium Bonds (12 months)** — Effectiveness: **Strong** — long validation period
3. **Independent draw auditor validation** (FR-3) — Effectiveness: **Strong** — external verification before results published
4. **Draw algorithm prototype required early** (Action Plan R-004) — Effectiveness: **Adequate** — planned but not yet implemented

#### Residual Risk Assessment

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Strong controls reduce significantly but complexity means residual risk remains |
| **Impact** | 4 - Major | Even a delayed draw (not incorrect) would be damaging |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Primary Response:** TREAT

#### Action Plan

1. **Dedicated Premium Bonds migration workstream with independent governance** — Owner: Programme Director — Due: 2026-06-30
2. **Shadow draw (SBS calculates alongside Atos, results compared but not used) for 12 months** — Owner: Ops Director — Due: Start H2 2027
3. **SBS draw performance testing at 150% peak volume** — Owner: CTO — Due: Pre-shadow-draw

**Target Residual Risk:** Likelihood 2, Impact 4 = 8 (Medium)

---

### Risk R-007: Legacy Data Quality Issues Discovered During Migration

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** NS&I CTO
**Action Owner:** Data Migration Lead

**Risk Description:** Data profiling of the Atos legacy system reveals significant data quality issues — missing fields, inconsistent formats, orphaned records, duplicates — requiring extensive remediation before migration can proceed. Given 27 years of accumulated data, some quality issues are virtually certain.

**Inherent Assessment:** Likelihood 3 (Possible) × Impact 3 (Moderate) = **9** (Medium)

**Current Controls:** Early data profiling planned (REQ A-4); data transformation rules documented (DR-3); validation rules in migration tooling (FR-7).

**Residual Assessment:** Likelihood 2 (Unlikely) × Impact 2 (Minor) = **4** (Low)

**Response:** TREAT — Begin data profiling immediately on Atos production data; establish data remediation workstream.

---

### Risk R-008: Dual-Run Reconciliation Reveals Systemic Discrepancies

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** NS&I CTO
**Action Owner:** NS&I Finance & Reconciliation Lead

**Risk Description:** Automated reconciliation during the parallel-run reveals systemic discrepancies between Atos and SBS platforms — not timing differences but genuine calculation disagreements — requiring investigation, root-cause analysis, and potentially platform reconfiguration.

**Inherent Assessment:** Likelihood 3 (Possible) × Impact 3 (Moderate) = **9** (Medium)

**Current Controls:** Reconciliation engine with tolerance thresholds (FR-8); product calculation validation engine (FR-12); test cohort of 100,000 accounts per product.

**Residual Assessment:** Likelihood 2 (Unlikely) × Impact 2 (Minor) = **4** (Low)

**Response:** TREAT — Validation engine catches discrepancies before parallel-run; root-cause process established; budget for remediation cycles.

---

### Risk R-009: Programme Costs Exceed Approved Funding Envelope

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** NS&I CFO (from STKE RACI: Accountable for budget)
**Action Owner:** Programme Director

**Risk Description:** Total programme costs exceed the approved funding envelope (including the £109M additional funding confirmed January 2026), requiring further Ministerial and parliamentary approval. Given the programme's £3bn cost history with £1.3bn escalation, further overruns would be politically devastating and may trigger programme cancellation review.

**Inherent Assessment:** Likelihood 4 (Likely) × Impact 5 (Catastrophic) = **20** (Critical)

**Current Controls:** EVM reporting requirement (BR-7); independent cost assurance at gates (BR-1); 20% contingency for novel elements (P4); monthly Treasury reporting. **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 3 (Possible) × Impact 4 (Major) = **12** (Medium)

**Response:** TREAT

**Key Actions:**
1. Establish validated cost baseline within 90 days (BR-1) — Owner: CFO — Due: 2026-05-15
2. Monthly EVM reporting with 5% early warning trigger — Owner: CFO — Ongoing
3. Fixed-price elements in SBS contract where feasible — Owner: Programme Director — Due: 2026-06-30

---

### Risk R-010: SBS Contract Variations Escalate Costs

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** NS&I CFO
**Action Owner:** Programme Director

**Risk Description:** Late-discovered requirements, customisation needs, or scope changes generate SBS contract variations that significantly increase the platform cost beyond contracted amounts. Variations are common in complex platform deployments and can be difficult to resist once the programme is committed.

**Inherent Assessment:** Likelihood 4 (Likely) × Impact 4 (Major) = **16** (High)

**Current Controls:** Standard-first approach; fit-gap analysis planned; change control process; architecture review board authority. **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 2 (Unlikely) × Impact 4 (Major) = **8** (Medium)

**Response:** TREAT — Complete fit-gap analysis before committing to configuration scope; negotiate variation cap in SBS contract.

---

### Risk R-011: Extended Dual-Run Increases Operating Costs

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** NS&I CFO
**Action Owner:** Ops Director

**Risk Description:** The parallel-run period extends beyond planned duration due to reconciliation issues, testing failures, or risk-averse decision-making, increasing the cost of running two platforms simultaneously. Each month of dual-run incurs significant additional operating cost.

**Inherent Assessment:** Likelihood 4 (Likely) × Impact 3 (Moderate) = **12** (Medium)

**Current Controls:** Time-bound parallel-run with clear exit criteria per product (REQ); phased migration reduces dual-run scope progressively. **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 3 (Possible) × Impact 2 (Minor) = **6** (Medium)

**Response:** TREAT — Define maximum parallel-run duration per product; escalation trigger if extended beyond plan.

---

### Risk R-012: Cloud Infrastructure Performance at NS&I Scale

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** NS&I CTO
**Action Owner:** Platform Operations Lead

**Risk Description:** UK sovereign cloud infrastructure does not deliver sufficient performance for NS&I workloads at full production scale (24M accounts, 500M annual transactions, Premium Bonds draw processing).

**Inherent Assessment:** Likelihood 2 (Unlikely) × Impact 3 (Moderate) = **6** (Medium)

**Current Controls:** Cloud capacity planning exercise planned; performance testing at 150% peak volume required (NFR-P-2); auto-scaling design (NFR-S-1). **Effectiveness: Strong.**

**Residual Assessment:** Likelihood 2 (Unlikely) × Impact 2 (Minor) = **4** (Low)

**Response:** TOLERATE — Low residual risk; continue monitoring via performance testing.

---

### Risk R-013: SBS Platform Fails Regulatory Accreditation on Time

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** NS&I CISO (from STKE RACI: Security accreditation gate owner)
**Action Owner:** Security Architecture Lead

**Risk Description:** The SBS platform fails to achieve NCSC CAF, PCI DSS, or other regulatory accreditation within the planned timeline (Q2 2028), delaying customer migration. Security assessment findings require remediation cycles that are unpredictable in scope and duration.

**Inherent Assessment:** Likelihood 3 (Possible) × Impact 4 (Major) = **12** (High)

**Current Controls:** Shift-left security approach (REQ Conflict C-4 resolution); automated security scanning in CI/CD (NFR-SEC-5); NCSC engagement planned; PCI DSS pre-assessment walkthrough. **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 3 (Possible) × Impact 4 (Major) = **12** (Medium)

**Response:** TREAT — Current controls reduce likelihood only marginally because accreditation is inherently sequential. Additional mitigation needed.

**Key Actions:**
1. Engage NCSC for early security architecture guidance — Owner: CISO — Due: 2026-06-30
2. Start PCI DSS QSA pre-assessment walkthrough in design phase — Owner: CISO — Due: 2027-01-31
3. Reserve 6-month remediation window before planned customer migration — Owner: Programme Director — Built into timeline

---

### Risk R-014: UK GDPR Breach During Data Migration

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** NS&I DPO
**Action Owner:** Data Migration Lead

**Risk Description:** Customer personal data is exposed, lost, or mishandled during the data migration between Atos and SBS platforms, constituting a UK GDPR breach requiring ICO notification within 72 hours.

**Inherent Assessment:** Likelihood 3 (Possible) × Impact 4 (Major) = **12** (High)

**Current Controls:** Encryption in transit (TLS 1.3) and at rest (AES-256) per NFR-SEC-3; DPIA requirement before migration (BR-3); data classification applied to all migration streams (P2). **Effectiveness: Strong.**

**Residual Assessment:** Likelihood 2 (Unlikely) × Impact 3 (Moderate) = **6** (Medium)

**Response:** TREAT — Complete DPIA; encrypt all migration pipelines; limit data access to need-to-know.

---

### Risk R-015: Regulatory Framework Changes During Migration

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** NS&I CISO
**Action Owner:** Compliance Officer

**Risk Description:** PCI DSS, NCSC CAF, FCA rules, or PRA requirements change materially during the multi-year migration, requiring rework of already-implemented security or compliance controls.

**Inherent Assessment:** Likelihood 3 (Possible) × Impact 3 (Moderate) = **9** (Medium)

**Current Controls:** Compliance-as-code approach (P10) enabling rapid policy updates; 10% compliance contingency budget (REQ A-5); active regulator dialogue. **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 2 (Unlikely) × Impact 2 (Minor) = **4** (Low)

**Response:** TOLERATE — Low residual risk with contingency budget; continue monitoring regulatory landscape.

---

### Risk R-016: Further PAC/Media Criticism Escalates

**Category:** REPUTATIONAL
**Status:** In Progress
**Risk Owner:** NS&I CEO
**Action Owner:** NS&I Head of Communications

**Risk Description:** The PAC's "full-spectrum disaster" narrative persists or worsens through follow-up hearings, media coverage, or FOI disclosures, undermining political support for the programme and triggering calls for programme cancellation or leadership change. Media amplification creates a self-fulfilling narrative of failure.

**Inherent Assessment:** Likelihood 5 (Almost Certain) × Impact 4 (Major) = **20** (Critical)

**Current Controls:** PAC response within 60-day deadline (BR-7); IPA engagement for independent assessment; honest governance reporting (Goal G-6). **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 3 (Possible) × Impact 4 (Major) = **12** (Medium)

**Response:** TREAT

**Key Actions:**
1. Proactive media strategy: announce early wins (e.g., first product migration) — Owner: Head of Comms — Due: Per milestone
2. Regular informal PAC member briefings (not just formal evidence) — Owner: CEO — Due: Quarterly
3. Publish transparency dashboard showing programme progress — Owner: Programme Director — Due: 2026-06-30

---

### Risk R-017: Customer Data Breach During Migration Becomes Public

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** NS&I CISO
**Action Owner:** NS&I CISO

**Risk Description:** A data breach affecting customer records during the migration becomes public (via ICO notification, FOI, or media leak), causing loss of customer trust in government-backed savings. The dual-platform environment during migration doubles the attack surface.

**Inherent Assessment:** Likelihood 3 (Possible) × Impact 5 (Severe) = **15** (High)

**Current Controls:** Full security architecture per NFR-SEC-1 to SEC-6; dual-platform security monitoring; incident response plan; encryption throughout. **Effectiveness: Strong.**

**Residual Assessment:** Likelihood 3 (Possible) × Impact 4 (Major) = **12** (Medium)

**Response:** TREAT — Cannot reduce impact (a breach is always reputationally damaging). Focus on reducing likelihood through defence in depth.

**Key Actions:**
1. Dedicated security monitoring for dual-platform period — Owner: CISO — Due: Before parallel-run
2. Pen test both platforms during dual-run — Owner: CISO — Due: Quarterly during dual-run
3. Customer breach communication plan pre-prepared — Owner: Head of Comms — Due: 2026-09-30

---

### Risk R-018: Consultant Firms Resist Accountability Framework

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** NS&I CFO
**Action Owner:** Programme Director

**Risk Description:** Consultant firms resist transition from time-and-materials to outcome-based contracts (BR-8), with best consultants leaving for less scrutinised engagements, creating a period of reduced programme capacity during the transition.

**Inherent Assessment:** Likelihood 3 (Possible) × Impact 4 (Major) = **12** (Medium)

**Current Controls:** Graduated transition plan (6-month ramp); positioning as reputational opportunity; premium rates for quality deliverables. **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 2 (Unlikely) × Impact 4 (Major) = **8** (Medium)

**Response:** TREAT — Graduated transition minimises disruption; retain best consultants with clear scope and rates.

---

### Risk R-019: Atos Financial Pressures Impact Service Quality

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** Programme Director
**Action Owner:** NS&I Operations Director

**Risk Description:** Atos's own financial restructuring leads to reduced investment in the NS&I account, degraded service quality, or staff redeployment during the critical transition period. Atos must maintain SLA compliance while transitioning out — but the commercial incentive to invest diminishes as exit approaches.

**Inherent Assessment:** Likelihood 3 (Possible) × Impact 4 (Major) = **12** (Medium)

**Current Controls:** Contractual SLA obligations with financial penalties; joint steering committee; escalation path to Atos UK leadership. **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 2 (Unlikely) × Impact 4 (Major) = **8** (Medium)

**Response:** TREAT — Monitor SLA closely; early escalation if degradation detected; contingency for accelerated self-service if Atos capacity fails.

---

### Risk R-020: Programme Direction Changed by Machinery of Government

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** NS&I CEO
**Action Owner:** NS&I CEO

**Risk Description:** A machinery of government change, Ministerial reshuffle, or policy shift results in changed programme direction, scope reduction, programme pause, or reassignment of NS&I to a different department, disrupting programme continuity.

**Inherent Assessment:** Likelihood 4 (Likely) × Impact 3 (Moderate) = **12** (Medium)

**Current Controls:** Cross-party support for NS&I modernisation; programme embedded in Treasury spending commitments; SBS contract creates commercial commitment. **Effectiveness: Adequate.**

**Residual Assessment:** Likelihood 3 (Possible) × Impact 2 (Minor) = **6** (Medium)

**Response:** TOLERATE — Political risk cannot be controlled; programme designed for incremental value delivery (P9) to demonstrate progress regardless of political changes.

---

## D. Risk Category Analysis

### STRATEGIC Risks

**Total:** 4 (R-001, R-002, R-018, R-020)
**Average Inherent Score:** 17.3 (High)
**Average Residual Score:** 11.3 (Medium)
**Control Effectiveness:** 35% reduction

**Key Themes:** Organisational capability gaps (culture, skills) are the dominant strategic risks. These are harder to mitigate than technical risks because they require behavioural change.

**Category Risk Profile:** ⚠️ Concerning — R-001 and R-002 both exceed appetite; foundational risks for the programme

### OPERATIONAL Risks

**Total:** 4 (R-003, R-005, R-006, R-019)
**Average Inherent Score:** 20.5 (Critical)
**Average Residual Score:** 11.0 (Medium)
**Control Effectiveness:** 46% reduction

**Key Themes:** The Atos transition (R-003, R-019) and customer migration (R-005, R-006) create the highest inherent risk cluster. Strong mitigations (phased migration, rehearsals, rollback) reduce significantly but cannot eliminate.

**Category Risk Profile:** ⚠️ Concerning — R-005 and R-006 exceed appetite; both relate to service continuity

### FINANCIAL Risks

**Total:** 3 (R-009, R-010, R-011)
**Average Inherent Score:** 16.0 (High)
**Average Residual Score:** 8.7 (Medium)
**Control Effectiveness:** 46% reduction

**Key Themes:** Cost overrun risk is well-understood given programme history. Controls (EVM, cost assurance, contingency) are effective but the programme's track record of cost escalation makes this category inherently elevated.

**Category Risk Profile:** ⚠️ Concerning — R-009 exceeds appetite; programme history amplifies political impact of any overrun

### COMPLIANCE/REGULATORY Risks

**Total:** 3 (R-013, R-014, R-015)
**Average Inherent Score:** 11.0 (Medium)
**Average Residual Score:** 7.3 (Medium)
**Control Effectiveness:** 34% reduction

**Key Themes:** Regulatory accreditation timing (R-013) is the main concern. UK GDPR breach risk (R-014) well-controlled through encryption. Regulatory change (R-015) tolerable with contingency.

**Category Risk Profile:** ⚠️ Concerning — R-013 exceeds appetite; accreditation timeline is on the critical path

### REPUTATIONAL Risks

**Total:** 3 (R-016, R-017, R-020)
**Average Inherent Score:** 15.7 (High)
**Average Residual Score:** 10.0 (Medium)
**Control Effectiveness:** 36% reduction

**Key Themes:** The PAC narrative (R-016) and data breach risk (R-017) dominate. Reputational risks are difficult to mitigate because perception is partly outside NS&I's control.

**Category Risk Profile:** ⚠️ Concerning — R-016 and R-017 both exceed appetite; reputational damage is hard to recover from

### TECHNOLOGY Risks

**Total:** 3 (R-004, R-007, R-008, R-012)
**Average Inherent Score:** 10.0 (Medium)
**Average Residual Score:** 5.0 (Low-Medium)
**Control Effectiveness:** 50% reduction

**Key Themes:** Technology risks are the most controllable category. SBS customisation (R-004) is the main concern but manageable through early fit-gap analysis. Data quality (R-007) and reconciliation (R-008) well-addressed by migration tooling requirements.

**Category Risk Profile:** ✅ Acceptable — All technology risks within appetite after controls; good engineering mitigations

---

## E. Risk Ownership Matrix

| Stakeholder | Role | Owned Risks | Critical/High Risks | Total Residual Score | Concentration |
|-------------|------|-------------|---------------------|----------------------|---------------|
| NS&I CEO | Programme Sponsor | R-001, R-016, R-020 | 1 High, 1 Medium, 1 Medium | 34 | ⚠️ High — 3 risks including top-ranked |
| NS&I CTO | Technology Direction | R-002, R-004, R-007, R-008, R-012 | 1 High | 35 | ⚠️ High — 5 risks but most well-controlled |
| NS&I Operations Director | Service Continuity | R-005, R-006 | 2 Medium (exceed appetite) | 24 | Moderate — 2 critical inherent risks |
| NS&I CFO | Financial Oversight | R-009, R-010, R-011, R-018 | 1 Medium (exceeds appetite) | 34 | ⚠️ High — 4 risks |
| NS&I CISO | Security/Compliance | R-013, R-015, R-017 | 2 Medium (exceed appetite) | 28 | Moderate — compliance-heavy |
| Programme Director | Delivery Lead | R-003, R-019 | 0 High | 20 | Moderate — Atos transition cluster |
| NS&I DPO | Data Protection | R-014 | 0 | 6 | Low — single focused risk |

**Risk Concentration Analysis:**
- ⚠️ **NS&I CEO owns 3 risks totaling 34 points** — Consider appointing Deputy SRO to share load
- ⚠️ **NS&I CTO owns 5 risks** — Appropriate given technology programme, but bandwidth concern
- ⚠️ **NS&I CFO owns 4 risks totaling 34 points** — Financial risk cluster needs dedicated PMO support

---

## F. 4Ts Response Framework Summary

| Response | Count | % | Total Residual Score | Key Examples |
|----------|-------|---|----------------------|--------------|
| **TOLERATE** | 3 | 15% | 14 | R-012 (cloud infra), R-015 (reg change), R-020 (MoG change) |
| **TREAT** | 17 | 85% | 178 | R-001 (culture), R-002 (skills), R-005 (cutover), all others |
| **TRANSFER** | 0 | 0% | 0 | None — risks are internal to programme |
| **TERMINATE** | 0 | 0% | 0 | None — all activities essential to programme objectives |
| **TOTAL** | 20 | 100% | 192 | |

**Key Insights:**
- **85% of risks require active treatment** — Reflects the challenging risk environment for this programme
- **No risks transferable** — Programme risks are inherent to NS&I's situation, not insurable or outsourceable
- **No risks terminable** — All activities are essential to the core banking migration
- **Only 15% tolerable** — Very limited risk appetite given PAC scrutiny and customer exposure

---

## G. Risk Appetite Compliance

**Organisational Risk Appetite Thresholds (NS&I / UK Government default):**

| Category | Appetite Level | Threshold Score | Rationale |
|----------|---------------|-----------------|-----------|
| STRATEGIC | Medium | ≤ 12 | NS&I must accept some strategic risk for modernisation but PAC scrutiny limits tolerance |
| OPERATIONAL | Low-Medium | ≤ 9 | 24M customers demand high service continuity; low tolerance for disruption |
| FINANCIAL | Low-Medium | ≤ 9 | PAC criticism of costs demands tight financial control; limited tolerance for overrun |
| COMPLIANCE | Very Low | ≤ 6 | Regulated financial services + government: near-zero tolerance for compliance breach |
| REPUTATIONAL | Very Low | ≤ 6 | Already damaged reputation; further damage could be fatal to programme |
| TECHNOLOGY | Medium | ≤ 12 | Accept technology risk where mitigated by strong engineering controls |

**Compliance Summary:**

| Category | Appetite | Risks Within | Risks Exceeding | Action Required |
|----------|----------|--------------|-----------------|-----------------|
| STRATEGIC | ≤ 12 | 2 (R-018, R-020) | 2 (R-001, R-002) | ⚠️ Board approval for R-001 (16), R-002 (15) |
| OPERATIONAL | ≤ 9 | 0 | 4 (R-003, R-005, R-006, R-019) | ⚠️ CEO approval for all; additional mitigations needed |
| FINANCIAL | ≤ 9 | 2 (R-010, R-011) | 1 (R-009) | ⚠️ Treasury sponsor approval for R-009 (12) |
| COMPLIANCE | ≤ 6 | 2 (R-014, R-015) | 1 (R-013) | ❌ CISO + Board approval for R-013 (12) |
| REPUTATIONAL | ≤ 6 | 0 | 3 (R-016, R-017, R-020) | ❌ CEO + Board approval for all |
| TECHNOLOGY | ≤ 12 | 4 (all) | 0 | ✅ Compliant |

**Overall Appetite Compliance:** ❌ 5 of 6 categories have risks exceeding appetite (11 individual risk exceedances)

**Board/Treasury Approval Required for:** R-001, R-002, R-003, R-005, R-006, R-009, R-013, R-016, R-017, R-019 (10 of 20 risks)

---

## H. Prioritized Action Plan

### Priority 1: URGENT (Residual Score ≥12 or Significantly Exceeds Appetite)

| # | Action | Risk(s) | Owner | Due Date | Expected Impact |
|---|--------|---------|-------|----------|-----------------|
| 1 | Commission independent culture assessment | R-001 | NS&I CEO | 2026-04-30 | Reduce R-001 from 16 to 12 |
| 2 | Submit DDaT pay exception requests for 4 leadership roles | R-002 | HR Director | 2026-03-31 | Reduce R-002 from 15 to 8 |
| 3 | Negotiate Atos key personnel retention incentives | R-003 | Programme Dir. | 2026-03-15 | Reduce R-003 from 12 to 9 |
| 4 | Establish validated programme cost baseline | R-009 | NS&I CFO | 2026-05-15 | Reduce R-009 from 12 to 9 |
| 5 | Engage NCSC for early security architecture guidance | R-013 | CISO | 2026-06-30 | Reduce R-013 from 12 to 9 |
| 6 | Proactive media strategy: announce early wins | R-016 | Head of Comms | Per milestone | Reduce R-016 from 12 to 8 |

### Priority 2: HIGH (Residual Score 8-12, Active Treatment)

| # | Action | Risk(s) | Owner | Due Date | Expected Impact |
|---|--------|---------|-------|----------|-----------------|
| 7 | Conduct SBS fit-gap analysis for all NS&I products | R-004 | Chief Architect | 2026-06-30 | Reduce R-004 from 8 to 6 |
| 8 | Production-scale test environment procurement | R-005, R-006 | CTO | 2026-12-31 | Reduce R-005/R-006 from 12 to 8 |
| 9 | Dedicated security monitoring for dual-platform period | R-017 | CISO | Before parallel-run | Reduce R-017 from 12 to 8 |
| 10 | Fixed-price elements in SBS contract | R-010 | Programme Dir. | 2026-06-30 | Reduce R-010 from 8 to 6 |

### Priority 3: MEDIUM (Routine Monitoring, Low-Cost Controls)

| # | Action | Risk(s) | Owner | Due Date | Expected Impact |
|---|--------|---------|-------|----------|-----------------|
| 11 | Begin data profiling on Atos production data | R-007 | Data Migration Lead | 2026-04-30 | Maintain R-007 at 4 |
| 12 | Define maximum parallel-run duration per product | R-011 | Ops Director | 2026-06-30 | Maintain R-011 at 6 |
| 13 | Regulatory change monitoring process | R-015 | Compliance Officer | Ongoing | Maintain R-015 at 4 |

---

## I. Integration with SOBC

**How this Risk Register feeds into Strategic Outline Business Case (SOBC):**

### SOBC Strategic Case (Part A)
- **"Why Now?" section** uses strategic risks to demonstrate urgency:
  - R-001 (culture): The longer the programme delays, the harder culture change becomes
  - R-019 (Atos financial pressures): Atos platform stability may deteriorate if transition is delayed
  - R-020 (MoG change): Political window for programme commitment may close

### SOBC Economic Case (Part B)
- **Risk-adjusted costs** use financial risks + HM Treasury optimism bias:
  - R-004 (SBS customisation): Add 15% contingency for platform costs (£TBD)
  - R-009 (cost overrun): 20% contingency for novel elements per P4
  - R-010 (contract variations): Cap variation costs in contract negotiation
  - R-011 (extended dual-run): Budget for maximum dual-run duration, not planned duration

### SOBC Management Case (Part E - Risk Management)
- **Full risk register** included as Annex to Management Case Part E
- **Top 10 risks** with mitigation plans highlighted in narrative
- **Risk ownership matrix** demonstrates clear accountability (Orange Book Principle A)
- **Monitoring framework** shows ongoing risk management capability
- **11 risks require Board/Treasury approval** — documented for transparent governance

### SOBC Recommendation
- **Concerning risk profile** (5 of 6 categories exceed appetite) should influence:
  - Option selection: prefer SBS standard over customisation where possible
  - Phasing strategy: low-risk products first to de-risk before Premium Bonds
  - Governance: independent assurance and culture change are prerequisites, not optional

---

## J. Monitoring and Review Framework

### Review Schedule

| Risk Level | Review Frequency | Reviewed By | Escalated To | Report Format |
|------------|------------------|-------------|--------------|---------------|
| **Critical (20-25)** | Weekly | Risk Owner + Programme Director | NS&I Programme Board | Dashboard + narrative |
| **High (13-19)** | Bi-weekly | Risk Owner | Steering Committee | Dashboard |
| **Medium (6-12)** | Monthly | Risk Owner | Programme Director | Status update |
| **Low (1-5)** | Quarterly | Action Owner | Risk Owner | Exception only |

### Key Risk Indicators (KRIs)

**Leading Indicators:**
- Permanent staff recruitment pipeline volume (R-002): <3x candidates per role → risk increasing
- Atos critical personnel headcount (R-003): any departure → escalate immediately
- SBS fit-gap analysis progress (R-004): delayed beyond Q2 2026 → risk increasing
- Monthly cost variance (R-009): >5% → early warning trigger
- Security scan findings trend (R-013, R-017): increasing critical findings → risk increasing

**Lagging Indicators:**
- IPA delivery confidence rating (R-001, R-016): RED maintained → risk materialised
- Cutover rehearsal results (R-005, R-006): failure → risk materialised
- Reconciliation match rate (R-008): <99.99% → risk materialised

### Escalation Criteria

**Automatic Escalation Triggers:**
1. Any risk increases by 5+ points → Programme Board
2. Any new Critical risk (score 20-25) identified → Programme Board + Treasury
3. Any risk exceeds appetite with no approved mitigation plan → NS&I CEO
4. Any mitigation action delayed >1 month → Steering Committee
5. 3+ risks in same category exceed appetite → Category risk owner + Board

### Risk Register Maintenance

**Risk Register Owner:** Programme Director
**Update Frequency:** Monthly (full register); weekly (critical/high risks)
**Version Control:** Major version on quarterly review; minor version on monthly updates

---

## K. Orange Book Compliance Checklist

- ✅ **A. Governance and Leadership**: All 20 risks have named owners from senior stakeholder RACI matrix; escalation paths defined to NS&I Board and HM Treasury; risk appetite thresholds set and monitored
- ✅ **B. Integration**: Risks linked to stakeholder goals (G-1 to G-8), requirements (BR/FR/NFR), and architecture principles (P1-P10); risk register feeds into SOBC Management Case
- ✅ **C. Collaboration and Best Information**: Risks sourced from stakeholder analysis (4 conflict-derived risks), requirements analysis (8 risk items), and principle compliance assessment
- ✅ **D. Risk Management Processes**: Systematic identification across 6 categories; consistent 5×5 assessment; 4Ts response framework; inherent and residual risk tracked with justification
- ✅ **E. Continual Improvement**: Monthly/quarterly review schedule; KRIs defined; escalation triggers; action plan with dates and owners

---

## Appendix A: Risk Assessment Scales

### Likelihood Scale (1-5) — Calibrated for NS&I Programme

| Score | Rating | Probability | NS&I Context |
|-------|--------|-------------|--------------|
| 1 | Rare | < 5% | Exceptional; has not occurred in similar government programmes |
| 2 | Unlikely | 5-25% | Could happen; controls largely prevent |
| 3 | Possible | 25-50% | Reasonable chance; has happened in similar programmes |
| 4 | Likely | 50-75% | More likely than not; programme history suggests this will occur |
| 5 | Almost Certain | > 75% | Expected to occur; structural factors make it near-inevitable |

### Impact Scale (1-5) — Calibrated for NS&I Programme

| Score | Rating | Financial | Schedule | Stakeholder/Political |
|-------|--------|-----------|---------|-----------------------|
| 1 | Negligible | < £5M | < 1 month | Internal concern only |
| 2 | Minor | £5-20M | 1-3 months | Minor Treasury/PAC interest |
| 3 | Moderate | £20-100M | 3-6 months | Parliamentary question; PAC follow-up |
| 4 | Major | £100-500M | 6-12 months | PAC hearing; Ministerial briefing; national media |
| 5 | Catastrophic | > £500M | > 12 months | Programme cancellation; Ministerial direction; customer impact |

---

## Appendix B: Stakeholder-Risk Linkage

| Stakeholder | Driver (from ARC-001-STKE-v1.0) | Risk ID(s) | Category | Total Score |
|-------------|--------------------------------|------------|----------|-------------|
| HM Treasury | SD-1: Cost control and VfM | R-009, R-010, R-011 | FINANCIAL | 26 |
| PAC | SD-2: Accountability and transparency | R-001, R-016 | STRATEGIC/REPUTATIONAL | 28 |
| NS&I CEO | SD-3: Delivery and reputation | R-001, R-016, R-020 | STRATEGIC/REPUTATIONAL | 34 |
| NS&I CTO | SD-4: Technical excellence | R-002, R-004, R-007, R-008 | STRATEGIC/TECHNOLOGY | 31 |
| Ops Director | SD-5: Service continuity | R-005, R-006, R-003 | OPERATIONAL | 36 |
| NS&I CISO | SD-6: Security posture | R-013, R-014, R-015, R-017 | COMPLIANCE/REPUTATIONAL | 34 |
| NS&I CFO | SD-7: Budget control | R-009, R-010, R-011, R-018 | FINANCIAL/STRATEGIC | 34 |
| Atos | SD-8: Managed exit | R-003, R-019 | OPERATIONAL | 20 |
| SBS | SD-9: Successful deployment | R-004, R-005, R-006 | TECHNOLOGY/OPERATIONAL | 32 |
| Customers | SD-10: Uninterrupted service | R-005, R-006, R-017 | OPERATIONAL/REPUTATIONAL | 36 |

**Stakeholder Conflicts → Risks:**

| Conflict (from ARC-001-STKE-v1.0) | Risk(s) Created | Mitigation Approach |
|------------------------------------|-----------------|---------------------|
| C-1: Speed vs Safety | R-005, R-006, R-009 | Phased migration (REQ Conflict C-1 resolution) |
| C-2: Vendor Independence vs SBS | R-004 | Selective abstraction at integration layer |
| C-3: Cost Reduction vs Capability | R-002, R-018 | Graduated consultant reduction |
| C-4: Regulatory vs Timeline | R-013 | Shift-left security approach |

---

## Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Risk Register Owner** | Programme Director | | |
| **Senior Responsible Owner** | NS&I CEO | | |
| **Treasury Sponsor** | HM Treasury Sponsor Team | | |
| **Audit Committee Chair** | NS&I Audit Committee | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HM Treasury Orange Book (2023) | Risk management guidance | HM Treasury | 5 principles, 4Ts framework, risk assessment methodology | gov.uk |
| ARC-001-STKE-v1.0 | Stakeholder Drivers | ArcKit | 15 drivers, RACI matrix, 4 conflicts, 6 stakeholder risks | `projects/001-core-banking-migration/` |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | 60 requirements, 8 risks, NFR targets | `projects/001-core-banking-migration/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | 10 principles (P1-P10), compliance requirements | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit:risk` command
**Generated on**: 2026-02-13
**ArcKit Version**: 2.4.4
**Project**: NS&I Core Banking Migration (Project 001)
**AI Model**: Claude Opus 4.6
