# Backlog, MoSCoW and RICE: Digital Account Opening (MVP)
 
**Project:** Nile Bank digital account opening case study. Fictional bank, synthetic data.
**Nature:** Synthetic. All reach figures, shares, impact levels, confidence levels and efforts are assumptions (S), not findings.
**Scope:** Individual current account, opened in the mobile app through the DFI platform.
 
## How to read this file
 
Start with the **Plain language summary**. It lists what the digital process must do, in one line each. The table after it shows how the team ranked those items and why.
 
**Codes used in this file:**
- **P1 to P8 (pain points):** problems in today's branch process.
- **R1 to R13 (requirements):** what the digital process must do.
- **K1 to K6 (KPIs):** the measures used to judge success.
- **E1 to E3 (evidence):** the sources. E1 is the Central Bank of Egypt regulation.
## Plain-language summary
 
| Requirement | What it means | Fixes |
|---|---|---|
| R1 | Customer starts the account in the app, with no branch visit | P1 |
| R2 | Check the applicant is an individual before the application starts | Scope |
| R3 | Check form entries as the customer types them, before submission | P2 |
| R4 | Read details from the verified ID document instead of retyping | P3 |
| R5 | Check identity against the national ID source, with a liveness check | P4 |
| R6 | If the electronic check fails, send the customer to a branch or agent | Regulation (E1) |
| R7 | If the face check fails, send the case to senior compliance review | P4, P8 |
| R8 | Screen applicants automatically against sanctions lists | P7 |
| R9 | Send only flagged applications to manual review | P6 |
| R10 | Run a manual review queue with clear criteria and a target turnaround | P8 |
| R11 | Use one digital case file for the branch and back office | P5 |
| R12 | Create the core banking account from the approved record, with no rekeying | P3 |
| R13 | Let the customer resume a half-finished application later | P1, P2 |
 
## Scales
- **Reach:** applications per quarter that reach the step the item changes. Baseline 100,000 a quarter (400,000 a year, synthetic). Shares are stated per item.
- **Impact:** scored on the highest KPI moved. 3 = moves a KPI directly. 2 = moves a KPI through a chain of steps. 1 = protects a control or requirement without moving a KPI. 0.5 = improves experience only. 0.25 = minor.
- **Confidence:** 100% = stated in the primary source (E1), with page reference. 80% = follows from E1 or a design logic stated in one sentence. 50% = design idea without a source.
- **Effort:** analysis and design time, in person-weeks (S). Not a delivery estimate.
- **Score:** Reach × Impact × Confidence ÷ Effort.
## Backlog, with MoSCoW and RICE
 
| Rank | ID | Requirement | Pain point | KPI | MoSCoW | Reach (share) | Impact | Confidence | Effort | Score | Source |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | R3 | Form validation at entry | P2 | K4 | Must | 100,000 (100%) | 2 | 80% | 0.5 | 320,000 | Design |
| 2 | R1 | Start the application in the app, with no branch visit | P1 | K1, K2 | Must | 100,000 (100%) | 3 | 80% | 1 | 240,000 | Design |
| 2 | R4 | Read data from the verified ID document, not retyped | P3 | K4, K6 | Must | 100,000 (100%) | 3 | 80% | 1 | 240,000 | E1 p.21, item 10.1 |
| 2 | R8 | Automatic negative-list screening, results sent to the bank | P7 | K1, K6 | Must | 100,000 (100%) | 3 | 80% | 1 | 240,000 | E1 p.21, item 7.5 |
| 2 | R9 | Risk-based routing: only flagged applications go to manual review | P6 | K3, K5, K6 | Must | 100,000 (100%) | 3 | 80% | 1 | 240,000 | Design |
| 6 | R11 | One digital case file shared by branch and back office | P5 | K1 | Must | 100,000 (100%) | 2 | 80% | 1 | 160,000 | Design |
| 7 | R12 | Create the core banking account from the approved record, without rekeying | P3 | K5, K6 | Must | 70,000 (70%) | 3 | 80% | 1.5 | 112,000 | Design |
| 8 | R2 | Check the applicant is an individual before the application starts | None | None | Must | 100,000 (100%) | 1 | 50% | 0.5 | 100,000 | Scope decision (A3) |
| 9 | R13 | Customer can resume a left application later | P1, P2 | K2 | Could | 30,000 (30%) | 3 | 50% | 0.5 | 90,000 | Candidate, no source |
| 10 | R5 | Identity check against the national ID source, with liveness detection | P4 | None | Must (control) | 100,000 (100%) | 1 | 100% | 1.5 | 66,667 | E1 p.21, items 10.1 to 10.3 |
| 11 | R10 | Manual review queue with clear criteria and a turnaround target | P8 | K1 | Must | 20,000 (20%) | 2 | 80% | 0.5 | 64,000 | Design |
| 12 | R6 | Failed electronic check directs the customer to a branch or agent | P2 | K2 | Must (control) | 15,000 (15%) | 1 | 100% | 0.5 | 30,000 | E1 p.12, clause 4 |
| 13 | R7 | Failed face check goes to senior compliance review | P4, P8 | K1 | Must (control) | 5,000 (5%) | 1 | 80% | 0.5 | 8,000 | Author decision |

## Sensitivity check
- **R2** drops to 60,000 if confidence falls by 20 points. It crosses the line, so it is fragile.
- **R12** drops to 84,000 if effort rises from 1.5 to 2 weeks. It falls below R2 and R13, so it is fragile.
- **R13** drops to 54,000 at 30% confidence. It is fragile, and it is the only item cut.
