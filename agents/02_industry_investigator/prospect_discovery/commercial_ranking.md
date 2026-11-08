# Commercial Ranking — US Home Services Prospects

Research cutoff: 2026-11-08. Scores are research judgments, not validated willingness to pay. No prospect has been contacted.

## Scoring model

Weighted 1–5 ratings, normalized to 100:

`score = (25*E + 20*S + 15*V + 10*R + 15*F + 15*A) / 5`

| Criterion | Weight | Meaning |
|---|---:|---|
| E — Demand evidence | 25% | First-person, named, current/recent evidence of recurring friction. |
| S — Existing spend / ability to pay | 20% | Headcount, revenue, active hiring, asset value, or software budget signals. |
| V — Severity / economic leakage | 15% | Money, time, liability, or customer-experience cost of the problem. |
| R — Recurrence / frequency | 10% | Daily/weekly/monthly cadence vs one-time or seasonal-only. |
| F — Small-team feasibility | 15% | Narrow wedge, read-only/integration-friendly, low regulatory liability. |
| A — Buyer accessibility | 15% | Named owner, public contact path, independent buying authority. |

Half-point ratings are allowed. Scores rounded to nearest integer.

## Ranked table

| Rank | ID | Business | E | S | V | R | F | A | Score | Tier |
|---:|---|---|---:|---:|---:|---:|---:|---:|---:|---|
| 1 | P01 | Serene Clean | 5 | 4 | 5 | 4 | 4 | 4 | 88 | Shortlist |
| 2 | P02 | Manning Pool Service | 5 | 4 | 4 | 4 | 4 | 4 | 85 | Shortlist |
| 3 | P03 | Kroopin's Poopin Scoopin | 5 | 3 | 4 | 5 | 4 | 3.5 | 82 | Shortlist |
| 4 | P04 | John Owens Services | 4 | 5 | 4 | 4 | 3 | 4 | 81 | Shortlist |
| 5 | P05 | Ace Pool & Spa | 5 | 3 | 4 | 3 | 4 | 4 | 79 | Shortlist |
| 6 | P06 | Great Valley Pool Service | 4 | 4 | 4 | 4 | 3 | 3.5 | 76 | Discovery |
| 7 | P08 | Mountain West HVAC | 4 | 4 | 3 | 4 | 3 | 4 | 74 | Discovery |
| 8 | P10 | Summit View Water | 4 | 2 | 3 | 5 | 4 | 4 | 71 | Discovery |
| 9 | P07 | DFW Turf Solutions | 4 | 4 | 3 | 2 | 4 | 3 | 70 | Discovery |
| 10 | P09 | Landscaping by J. Michael | 3 | 4 | 3 | 4 | 4 | 3 | 69 | Discovery |
| 11 | P11 | Team 8 Cleaning & Services | 4 | 2 | 2 | 5 | 4 | 4 | 68 | Watchlist |
| 12 | P12 | Huge Home Pros | 3 | 3 | 3 | 4 | 3 | 4 | 65 | Watchlist |
| 13 | P14 | Green Impressions | 4 | 4 | 3 | 4 | 3 | 1 | 65 | Watchlist |
| 14 | P15 | La Rosa Landscape | 2 | 3 | 3 | 4 | 4 | 3 | 60 | Watchlist |
| 15 | P13 | Municipal Backflow | 3 | 3 | 3 | 4 | 2 | 2 | 56 | Watchlist |

Tiebreak: P12 ranks above P14 because Huge Home Pros has an independent owner-buyer, while Green Impressions is inside a PE-backed group with centralized buying.

## Tier rationale

### Shortlist (P01–P05)
- **Serene Clean:** Best combination of current first-person evidence, weekly cadence, named owner, and a read-only wedge beside QBO/Gusto. Supply leakage and client-margin audits have direct dollar signals.
- **Manning Pool Service:** Clear monthly inspection→email→spreadsheet handoff, 34 employees, expensive assets, and a co-owner who authored the workflow description. Feasible narrow asset/repair queue.
- **Kroopin's Poopin Scoopin:** Very strong 2026 evidence of manual pricing/time audits and seasonal volume. Lower ability to pay than larger trades, but high recurrence and owner accessibility.
- **John Owens Services:** Strongest budget signal (active $30–42/hr bookkeeper hire, 34+ employees, ServiceTitan/QBO stack). Lower feasibility because reconciliation touches accounting liability and ServiceTitan may already have native tools.
- **Ace Pool & Spa:** Fresh 2026 evidence of seasonal misquotes, ~$10k inventory, and spreadsheet quoting/scheduling. Small team and seasonal cadence cap ACV, but wedge is concrete.

### Discovery (P06–P10)
- **Great Valley:** Explicit automation goal and multi-division order flow, but primary evidence is 2022. Needs current-state validation.
- **Mountain West:** Owner complains ServiceTitan is underused and maintains goal spreadsheets, but a ServiceTitan implementation partner may be the better first solution.
- **Summit View Water:** Daily Jobber request workaround and admin hiring, but small budget and existing add-ons (Bento/Adhesion) compete.
- **DFW Turf:** Quarterly lead-source reconciliation is real but infrequent; multi-location rollup may centralize or replace systems.
- **Landscaping by J. Michael:** Active bookkeeper hire with process-improvement mandate, but hiring-based evidence is weaker than an operator complaint.

### Watchlist (P11–P15)
- **Team 8:** Clear manual notification pain, but very small and a marketplace workaround was already suggested.
- **Huge Home Pros:** Automation-savvy owner; service-agreement gap is real but he may solve with GHL/Jobber updates.
- **Green Impressions:** Good friction evidence, but PE-backed parent and Aspire rollout likely change the buying process.
- **La Rosa:** Strong quote, but 2018 evidence; current state unknown.
- **Municipal Backflow:** Already claims custom software; owner identity conflict; regulatory submission complexity.

## Kill criteria before building

| Prospect | Kill if… |
|---|---|
| P01 Serene Clean | Owner refuses read-only QBO/Gusto access; QBO/ZenMaid reports already produce the weekly sheet; supply tracking is now fully delegated and no longer tedious. |
| P02 Manning | They already use an FSM/asset module that ingests inspections; monthly cadence is too low to pay; repair spreadsheet is maintained by vendor software. |
| P03 Kroopin's | Jobber reports already compute per-customer labor burden; owner prefers coaching/spreadsheet control; budget cannot support >$100/mo or a small pilot fee. |
| P04 John Owens | ServiceTitan native integration/reconciliation already solves the discrepancy workflow; bookkeeper hire is the preferred solution; accounting liability is unacceptable. |
| P05 Ace Pool & Spa | Lighting season is too short to justify software; spreadsheet is adequate; inventory reuse removes urgency; owner will not share quote/actual data. |
| P06–P15 | Current-state interview shows the problem is solved, anonymous/unverified, or buying authority is centralized elsewhere. |

## Sensitivity notes

- If ServiceTitan ships/confirmed native batch reconciliation, P04 drops below P05.
- If Manning confirms an existing asset/inspection module, P02 drops to Discovery.
- If Serene's owner says the spreadsheet ritual is intentional control rather than pain, P01 drops sharply.
- If Kroopin's confirms a budget under ~$100/mo, P03 drops despite strong evidence.
- If Ace's lighting revenue is material and multi-month, P05 could rise above P04.
- Great Valley could enter the shortlist if a 2026 interview confirms the manual accounting/order gap remains.

## First-prospect recommendation

**Start discovery with P01 Serene Clean.** It has the highest score, the freshest repeated weekly workflow, a public owner, and a low-liability read-only wedge. The goal of the first call is not to sell software; it is to confirm whether the weekly KPI/supply compilation is still painful, who owns it, and whether a read-only dashboard would be trusted over the existing spreadsheet.
