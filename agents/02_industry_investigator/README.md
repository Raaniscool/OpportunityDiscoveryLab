# Agent 02 — Industry Investigator

**Mission:** Identify industries and niches where a small, fast product team (Arena) could create substantial commercial value. Research only — no products are built here.

**Research cutoff:** 2026-11-08. All sources were accessed on or before this date. Forecasts are labeled as forecasts; vendor claims are labeled as vendor claims.

## Deliverables

| File | Purpose |
|---|---|
| [industry_analysis.md](industry_analysis.md) | 22 industry profiles, each with market size, customers, spending, problems, competitors, opportunities, product ideas, monetization, barriers, competition, growth, and evidence quality. |
| [emerging_markets.md](emerging_markets.md) | AI-transformation hypotheses, new/obsolete categories, AI-era services, personal-software maintenance, low-adoption sectors, and regulatory triggers. |
| [opportunity_database.md](opportunity_database.md) | 16 ranked opportunities with buyer, wedge, pricing hypothesis, channel, competitors, risks, evidence grade, kill criteria, and a validation experiment. |
| [research_sources.md](research_sources.md) | Source registry with dates, evidence grades, bias flags, and what each source supports. |

## Method

1. **Start from pain, not TAM.** For each industry we looked for surveys, transaction data, government statistics, or observed pricing that show customers already spend money or lose money on a specific workflow.
2. **Triangulate.** A market-size report alone is not enough. We paired size anchors with demand evidence (e.g., AMA prior-auth survey + CAQH transaction data + competitor pricing).
3. **Grade evidence.** A = government/official statistics or audited transaction data; B = large independent survey, peer-reviewed study, or primary vendor dataset with clear methodology; C = vendor survey, small sample, secondary reporting, or pricing page; D = low-quality market report, anecdote, or unverified claim. Vendor bias is flagged.
4. **Score opportunities.** Weighted 1–5 scores, normalized to 100:
   - Demand evidence 25%
   - Existing spending / willingness to pay 20%
   - Severity of inefficiency 15%
   - Technology/regulatory change 10%
   - Small-team feasibility 15%
   - Customer acquisition 15%
   Competition intensity and growth are documented separately, not double-counted in the score.
5. **Prefer wedges.** A large market with entrenched incumbents is not automatically attractive. We rank narrow, evidence-backed entry points above broad "AI for X" platforms.

## Top 10 ranked opportunities

| Rank | ID | Opportunity | Score | Evidence |
|---:|---|---|---:|---|
| 1 | O01 | Accounting client-evidence chasing + year-round CAS bookkeeping | 88 | B |
| 2 | O02 | Freight detention/accessorial recovery for small fleets | 86 | B |
| 3 | O03 | AI-built-app release-readiness and security audit | 82 | B |
| 4 | O04 | Subcontractor bid scope/risk reconciliation | 80 | B |
| 5 | O05 | Specialty-clinic prior-authorization evidence assembly | 80 | B |
| 6 | O06 | Agent eval/regression harness for vertical AI agencies | 76 | B |
| 7 | O07 | E-commerce returns exception evidence for 3PLs | 74 | B |
| 8 | O08 | Home-services estimate follow-up / revenue recovery | 73 | B |
| 9 | O09 | Property maintenance triage and vendor coordination | 73 | B |
| 10 | O10 | Creator campaign ops, rights, and payment reconciliation | 72 | B |

Full ranking and kill criteria: [opportunity_database.md](opportunity_database.md).

## Headline conclusions

- **Most attractive industries:** accounting/CAS, freight brokerage/small fleets, AI-built software assurance, construction subcontracting, and healthcare administrative workflows. They combine recurring pain, existing budgets, and measurable money leakage.
- **Best unconventional wedges:** detention invoice recovery, AI-generated app release audits, returns exception evidence, and small water-utility compliance reporting.
- **Avoid as first products:** generic productivity apps, generic creator tools, broad game-development tools, and consumer caregiving apps without a payer. Large user counts do not imply willingness to pay.
- **AI transformation is a hypothesis, not a guarantee.** The strongest near-term opportunities are assurance, compliance, evidence assembly, and reconciliation around AI output — not replacing entire professions.

## Limitations

- Market sizes are directional. Government statistics, IBISWorld estimates, and vendor forecasts use different definitions and should not be summed.
- Several demand surveys are vendor-sponsored (Invoca, Radial, Mirakl, Karbon, Soraban, VMS, Fleetio, DockClaim). They are useful but biased toward proving the problem.
- Pricing pages change frequently. Prices are snapshots accessed 2026-11-08 unless a publication date is given.
- No primary customer interviews were conducted. Every opportunity includes a validation experiment and kill criteria before product investment.
