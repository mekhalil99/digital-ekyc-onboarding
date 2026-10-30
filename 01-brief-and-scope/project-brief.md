# Project Brief: Nile Bank, Digital eKYC Onboarding
 
**Status:** Approved, v1.0, 30 Oct 2026
**Nature of this project:** Independent portfolio case study. Nile Bank is fictional. All people and data are synthetic. Values marked **(S)** are synthetic assumptions, not findings. Source IDs (E1, E2...) refer to the evidence register in section 6.
 
## 1. Problem statement
 
Opening a current account at Nile Bank means a branch visit, paper forms, manual data entry and back-office KYC checks. In the synthetic baseline, **30% (S)** of applicants abandon before the account is active, only **70% (S)** of applications are right first time, and the median account takes **3 days (S)** to open.
 
The Central Bank of Egypt (CBE) issued regulations for the Digital Financial Identity (DFI) platform (E1) on 23 Aug 2026 (E2). They allow identity to be verified electronically through an approved platform, so remote account opening is now possible. The bank has no defined target process, requirements or measures for adopting it. This project defines them.
## 2. Scope
 
| In | Out |
|---|---|
| Individual retail customers (scope decision, see A3) | Corporate customers |
| One product: a current account in EGP | Savings and other products (a future extension) |
| Remote opening in the mobile app via the DFI platform | Authenticating financial transactions with the DFI. The regulation requires additional CBE approval for this (E1 p.12, "Third: Electronic Authentication"). |
| Exceptions: ID scan fails, selfie mismatch, data mismatch, compliance flag, customer abandons | Banking Agent channel (the fallback is modelled as a branch visit only) |
| Bank-side manual review and branch fallback | Licensing procedure and cybersecurity controls (E1 Sections 4 and 7) |
| The branch process as the baseline | Real integrations or software build |
 
## 3. Stakeholders
 
| Stakeholder | Interest | Influence |
|---|---|---|
| Applicant (individual customer) | Fast, simple, trustworthy opening | Medium |
| Branch staff | Workload and role change | Medium |
| Back-office KYC and compliance officer | Risk decisions, manual review volume | High |
| Digital channel product owner | App journey, drop-off | High |
| IT and core banking | Integration, account creation | Medium |
| Fraud and risk officer | Fraud losses, false accepts | High |
| Customer support and complaints | Failed-flow queries | Low |
| Senior management (sponsor) | Cost, growth, regulatory fit | High |
| DFI platform operator (external) | Verification service quality | Medium |
| CBE (external regulator) | Compliance with the regulations | High |
 
Influence ratings are the author's assumptions.
 
## 4. Assumptions
 
| ID | Assumption |
|---|---|
| A1 | Nile Bank is a fictional mid-size Egyptian retail bank. Data and people are synthetic. |
| A2 | All KPI values are synthetic. The baseline is the branch process and the target is the digital process. |
| A3 | Individuals only is a scope decision. The CBE text refers only to individuals (E1 pp.1-2). A law-firm commentary states the circular does not apply to juridical entities (E2). It is not an explicit CBE exclusion. |
| A4 | If a customer cannot be identified electronically, or the platform cannot read the document data, the customer is directed to a branch or Banking Agent to complete verification (E1 p.12, "Second: Electronic Identity Verification Requirements", clause 4). |
| A5 | The 23 Aug 2026 date is the issue date per E2. The regulation PDF itself shows no date (E1). No transition period is stated in E1. |
| A6 | Records are kept for "legally prescribed" periods (E1 p.18). No specific retention period is modelled. |
| A7 | Fully loaded staff cost is assumed at EGP 150 per hour (S). It is used only to keep K5 and K6 consistent. |
| A8 | Any step that depends on the regulation cites a page number. Where it cannot, it is marked "assumption, to verify". |
 
## 5. KPIs (all synthetic)
 
| ID | KPI | Definition | Baseline (branch) | Target (digital) | Rationale |
|---|---|---|---|---|---|
| K1 | Time to open an account | Median elapsed time from application start to account active | 3 days | 0.5 day | Removes back-office queueing and manual entry. Exceptions still take longer. |
| K2 | Application drop-off rate | Share of started applications not completed | 30% | 18% | No branch visit or paper forms. Remaining losses sit at ID and selfie capture. |
| K3 | % needing manual review | Share of applications sent to bank-side review | 100% | 15% | Branch applications get a full manual check today. Only flagged cases go to review. |
| K4 | First-time-right rate | Share of applications with no rework | 70% | 90% | Data comes from the verified document, not retyping. |
| K5 | Cost per account opened | Staff, overhead and platform cost per active account (EGP) | 450 | 150 | Staff time falls sharply. A per-verification platform fee is added. |
| K6 | Staff hours per application | Branch and back-office hours per application | 1.5 | 0.3 | Staff time is spent only on exceptions. |
 
Consistency check: at the A7 rate, K6 gives EGP 225 baseline and EGP 45 target staff cost. The rest of K5 is overhead and the platform fee.
 
## 6. Evidence register
 
| ID | Source | Type | Verified by author | Used for |
|---|---|---|---|---|
| E1 | Central Bank of Egypt, *Regulations Governing the Services of the Digital Financial Identity Platform for Identifying Bank Customers and Verifying Their Identities Electronically in the Arab Republic of Egypt* (English PDF) | Primary | Yes, read in full | Regulatory facts, cited by page |
| E2 | Adsero (Egyptian law firm), commentary on the CBE circular, 7 Sep 2026 | Secondary | Yes, opened | Issue date, individuals only, pending EMLCU procedures |
| E3 | Biometric.vision blog on Egypt's DFI and eKYC, 25 Sep 2026 | Secondary, vendor (sells biometric products) | Yes, opened | Vendor design suggestions only (audit-trail fields, consent evidence); not CBE requirements |
 
Only sources the author has opened and checked are listed or used.
 
## 7. Limitations
 
- Every KPI value is invented. The method, definitions and traceability are the contribution, not the numbers.
- No KPI measures fraud outcomes or false accepts. K3 improves if more applications are auto-approved, so it should be read together with the routing rules.
- The synthetic digital cohort is not guaranteed to meet every target. Drop-off may concentrate at ID and selfie capture.
- The problem rests on the synthetic baseline and the regulation (E1). No external evidence of drop-off is used.
