# As-Is Step Table: Branch Account Opening
 
**Version:** 1.0, 12 Nov 2026
**Process:** Branch account opening for an individual current account (synthetic, fictional bank).
**Nature:** Design baseline (S). Not a real bank's process. No step depends on the regulation.
**Lanes:** Customer, Branch Staff, Compliance/KYC, IT/Core Banking.
**Map:** as-is-process-map.pdf (same step IDs).
 
| Lane | ID | Step | Type | Next step | Condition | Pain point |
|---|---|---|---|---|---|---|
| Customer | S1 | Decides to open an account | Start event | S2 | | |
| Customer | S2 | Travels to branch and waits in queue | Task | S3 | | P1 |
| Customer | S2-B | Customer leaves queue | Boundary event on S2 | S24 | Interrupting | P1 |
| Customer | S3 | Fills in paper application form and signs | Task | S4 | | |
| Branch Staff | S4 | Checks form completeness and original documents | Task | S5 | | |
| Branch Staff | S5 | Form and documents complete? | Exclusive gateway | S7 / S6 | Yes / No | |
| Customer | S6 | Corrects form or fetches missing documents | Task | S4 | Loop back | P2 |
| Customer | S6-B | Customer does not return | Boundary event on S6 | S24 | Interrupting | P2 |
| Branch Staff | S7 | Scans documents and keys data into application system | Task | S8 | | P3 |
| Branch Staff | S8 | Compares ID photo with customer by eye | Task | S9 | | P4 |
| Branch Staff | S9 | Sends paper file and scans to back office | Task | S10 | | P5 |
| Compliance/KYC | S10 | Receives file, re-checks documents and compares data | Task | S11 | | P3, P6 |
| Compliance/KYC | S11 | Data and documents consistent? | Exclusive gateway | S14 / S12 | Yes / No | |
| Compliance/KYC | S12 | Returns file to branch with a query | Task | S13 | | P2, P5 |
| Branch Staff | S13 | Contacts customer and corrects file | Task | S9 | Loop back | P2 |
| Branch Staff | S13-B | Customer unreachable | Boundary event on S13 | S24 | Interrupting | P2 |
| Compliance/KYC | S14 | Screens customer against sanctions and negative lists (manual search) | Task | S15 | | P7 |
| Compliance/KYC | S15 | Any screening or risk flag? | Exclusive gateway | S18 / S16 | No / Yes | |
| Compliance/KYC | S16 | Escalated review by senior compliance officer | Task | S17 | | P8 |
| Compliance/KYC | S17 | Cleared? | Exclusive gateway | S18 / S19 | Yes / No | |
| Compliance/KYC | S18 | Approves application | Task | S20 | | |
| Branch Staff | S19 | Notifies customer of rejection | Task | S23 | | |
| IT/Core Banking | S20 | Creates customer record and account in core banking, activates | Task | S21 | | P3 |
| Branch Staff | S21 | Notifies customer that the account is active | Task | S22 | | |
| Customer | S22 | Account active | End event | | | |
| Branch Staff | S23 | Application rejected | End event | | | |
| Customer | S24 | Application abandoned | End event | | | |
 
**Counts:** 16 tasks, 4 gateways, 5 start and end events (1 start, 4 end: S22, S23, S24), 3 boundary events.
