# Pain Point Register: Branch Account Opening (As-Is)
 
**Process map:** as-is map (PDF), four lanes in one pool. Step IDs S1 to S24 as in the as-is step table.
**Nature:** Every pain point is a design hypothesis about the fictional baseline (S). None is a finding from real data. The Sprint 2 dataset will encode these hypotheses, so SQL results will confirm the design, not the real world.
 
## Pain points
 
Box text is the wording shown in the red boxes on the map. The same wording is used here, so the map and this register match.
 
| ID | Pain point (map box text) | Steps | Type | KPIs | Direction for the to-be |
|---|---|---|---|---|---|
| P1 | Customer waits in branch queue | S2 | Waiting | K1, K2 | Start remotely in the app, with no travel or queue |
| P2 | Incomplete form loops back | S6 (from S5), S12 and S13 (from S11) | Rework | K1, K2, K4, K6 | Catch errors at entry, before submission |
| P3 | Data typed in again | S7, S20 | Manual re-keying | K4, K5, K6 | Read data from the verified document, with no retyping |
| P4 | ID checked by eye only | S8 | Control gap | None (see notes) | Platform check against the national ID source and liveness (E1 p.21, items 10.1 to 10.3) |
| P5 | Paper file handed over | S9, S12 | Handoff and waiting | K1 | One digital file and one record |
| P6 | Every file re-checked in full | S10 | Duplicate work | K3, K5, K6 | Risk-based review, with only flagged cases sent on |
| P7 | Manual sanctions search | S14 | Manual task | K1, K6 | Automated screening by the platform, with results sent to the bank (E1 p.21, item 7.5) |
| P8 | Flagged cases wait for senior review | S16 | Waiting | K1 | A review queue with clear criteria and a turnaround target |
 
## Map boxes by step
 
| Step | Box text |
|---|---|
| S2 | P1 Customer waits in branch queue |
| S6 | P2 Incomplete form loops back |
| S7 | P3 Data typed in again |
| S8 | P4 ID checked by eye only |
| S9 | P5 Paper file handed over |
| S10 | P6 Every file re-checked in full |
| S12 | P2 Query sends file back to branch |
| S12 | P5 Paper file handed back |
| S13 | P2 Correction loop back to back office |
| S14 | P7 Manual sanctions search |
| S16 | P8 Flagged cases wait for senior review |
| S20 | P3 Account keyed again in core banking |
 
## Notes for review
 
- **P3 and P6 overlap.** Both involve back-office repetition, one for data entry and one for review. They're kept separate because the fixes differ: P3 is about data flow, and P6 is about review risk.
- **P4 has no KPI.** The brief already notes that fraud outcomes are not measured, so P4 is a control gap, not a KPI.
- **The to-be column cites the regulation only as a design benchmark.** E1 describes what the platform must do. It does not say the branch process is faulty. The as-is problems are the author's hypotheses.
- **The P8 turnaround target is a design choice,** not a regulatory requirement.
## Known gaps in the as-is map
 
- **No selfie-mismatch exit.** At S8, a failed face check passes straight to S9. This is an open design decision and should be resolved before the to-be map.
- **Rejection is not told to the customer.** S19 leads only to S23. The map does not show the customer being informed of a rejection. The regulation requires a customer notice on successful DFI completion (E1 p.9, clause 7), but does not say whether rejections must be notified. This is a known gap in the as-is.
- **Boundary events are approximate.** The boundary events S2-B, S6-B and S13-B are placed on each task's edge. Attachment is approximate in the drawing tool (Lucidchart), so they may not be formally attached in the file.
 
