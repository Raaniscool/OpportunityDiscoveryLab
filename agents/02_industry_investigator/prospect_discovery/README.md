# Agent 02 — Prospect Discovery: US Home Services & Local Trades

**Mission:** Identify 15 real, named US small businesses in home services / local trades that show evidence of a recurring operational problem a small product team could solve with narrow custom software. Rank them by commercial potential and develop five shortlisted pilot proposals.

**Research cutoff:** 2026-11-08. All sources were accessed on or before this date. No outreach was sent, no software was built, and no prospect has confirmed willingness to pay.

## Deliverables

| File | Purpose |
|---|---|
| [prospect_profiles.md](prospect_profiles.md) | 15 named business profiles with location, size evidence, decision-maker, stack, recurring problem, evidence, confidence, and custom-software wedge. |
| [evidence_ledger.md](evidence_ledger.md) | Source registry with dates, evidence grades, bias flags, and what each source supports. |
| [commercial_ranking.md](commercial_ranking.md) | Weighted scoring, ranked shortlist, tier rationale, kill criteria, and sensitivity notes. |
| [shortlisted_proposals.md](shortlisted_proposals.md) | Five pilot proposals: problem, scope, alternatives, complexity, owner questions, rejection risks, and first-prospect recommendation. |

## Method

1. **Start from observed friction, not vendor SEO.** Prioritized first-person operator interviews, trade-press profiles written by or quoting owners, Jobber community posts by named businesses, and active job postings that describe recurring workload.
2. **Require a named US business.** Anonymous forum handles, composite vendor case studies, non-US businesses, and placeholder websites were excluded.
3. **Separate current friction from solved history.** A business that publicly describes a problem it already fixed is lower confidence than one describing an ongoing manual workflow.
4. **Prefer narrow wedges beside existing FSM/accounting tools.** Proposals do not replace Jobber, ServiceTitan, Workiz, QuickBooks, or ZenMaid. They target a specific reconciliation, inspection, pricing, or seasonal-estimating gap.
5. **Grade evidence.** A = primary/official; B = reputable trade press or podcast transcript; C = job board/directory; D = vendor marketing or search-only snippet. Vendor bias is flagged.

## Top 5 ranked prospects

| Rank | ID | Business | Location | Score | Core friction |
|---:|---|---|---|---:|---|
| 1 | P01 | Serene Clean | Western Wisconsin | 88 | Weekly manual KPI, supply-spend, and client-margin spreadsheets beside QBO/Gusto. |
| 2 | P02 | Manning Pool Service | Houston, TX | 85 | Monthly iPad vacuum inspections emailed to a manager who compiles a repair spreadsheet. |
| 3 | P03 | Kroopin's Poopin Scoopin | Westland / Northville, MI | 82 | Manual per-customer time/pricing audits in Excel; seasonal rush pricing and margin control. |
| 4 | P04 | John Owens Services | Petaluma / San Rafael, CA | 81 | ServiceTitan-to-QuickBooks batch reconciliation, inventory accounting, and discrepancy research. |
| 5 | P05 | Ace Pool & Spa | Antioch / Nashville, TN | 79 | Holiday-lighting misquotes, ~$10k inventory exposure, and spreadsheet scheduling/quoting. |

Full ranking: [commercial_ranking.md](commercial_ranking.md). Pilot details: [shortlisted_proposals.md](shortlisted_proposals.md).

## Headline conclusions

- **Best evidence is not always the biggest business.** Serene Clean, Manning, Kroopin's, and Ace have direct operator descriptions of manual workflows. John Owens has strong hiring-based evidence of recurring reconciliation workload.
- **Pool service and cleaning are unusually rich in spreadsheet-adjacent friction.** Monthly inspections, seasonal lighting, supply consumption, and client-margin audits are narrow enough for a small team.
- **ServiceTitan/QuickBooks reconciliation is commercially attractive but harder.** John Owens Scores well because the workload is expensive and recurring, but integration complexity and accounting liability are real.
- **Avoid replacing working FSMs.** The strongest wedges are read-only dashboards, exception queues, audit trails, and quote-to-actuals feedback loops.
- **Several candidates are watchlist-only.** Great Valley's automation goal is from 2022; La Rosa's parts evidence is from 2018; Green Impressions is now inside a PE-backed group; Municipal Backflow already claims custom software and has an owner-identity conflict.

## Limitations

- Headcounts from LinkedIn/ZoomInfo/RocketReach/BBB are estimates or self-reported bands and sometimes conflict. Profiles preserve the conflict instead of choosing a false precise number.
- Job postings prove recurring workload and budget, not necessarily dissatisfaction with current software.
- Podcast/trade-press statements may be dated. CMS refresh dates are not treated as episode dates.
- No primary discovery calls were conducted. Every proposal is contingent on owner validation and includes kill criteria.
