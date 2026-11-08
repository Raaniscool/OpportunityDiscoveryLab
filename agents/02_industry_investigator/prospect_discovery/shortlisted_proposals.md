# Shortlisted Pilot Proposals — Top 5 Prospects

Research cutoff: 2026-11-08. These are discovery-contingent proposals, not commitments. No outreach has been sent and no software has been built. Each pilot is designed to sit beside the prospect's existing FSM/accounting tools, not replace them.

---

## Proposal 1 — Serene Clean: Weekly KPI & Supply-Margin Autopilot (P01)

**Problem.** Stephanie Pipkin manually compiles a weekly financial tracking sheet from QuickBooks Online (revenue, expenses, profit, AR, five bank balances). Payroll manager April maintains a weekly per-product tool/supply spreadsheet that Stephanie calls "tedious." Client hourly-rate/margin audits and QBO revenue tagging are also manual. A past supply-misuse issue (disposable toilet wands) cost hundreds per month before tracking caught it.

**Pilot scope (4–6 weeks, read-only).**
1. Connect read-only QBO (P&L, invoices, expenses, tags) and Gusto (payroll journal) exports.
2. Auto-generate the weekly financial sheet: revenue, expenses, profit, AR, bank-balance columns, payroll % of revenue (tech vs management split).
3. Supply-spend module: categorize receipts by product, compute weekly consumption and spend-as-%-of-revenue, flag >4% months and anomalous product velocity.
4. Client-margin module: revenue ÷ logged hours per client, color-grade green/yellow/red against target hourly rate.
5. Deliver a weekly email/PDF + simple dashboard; no write-back to QBO.

**Success metrics.** Reduce weekly compilation time by ≥50%; reproduce April's supply sheet with ≥95% line-item agreement; surface at least one actionable margin/supply anomaly in first month.

**Alternatives the owner already has.** QBO reports + manual Google Sheet; ZenMaid reporting; Fathom/Reach Reporting/ProfitFirst dashboards; a bookkeeper or VA. The wedge is cross-system compilation + anomaly detection, not accounting.

**Complexity.** Medium. QBO/Gusto APIs are mature; main risk is receipt/product categorization and matching supply purchases to consumption. Start with CSV import if API access is delayed.

**Owner discovery questions.**
- Is the Tuesday KPI ritual still manual, and how many minutes does it take?
- Who owns April's supply sheet now, and what columns matter most?
- Would you trust a read-only dashboard, or is spreadsheet control the point?
- What hourly-rate target defines red/yellow/green per client?
- Are supply receipts already tagged in QBO, or do they need categorization?

**Rejection risks.** Owner may value spreadsheet control; QBO/ZenMaid may already cover reporting; supply misuse was a one-time fix; remote owner may delegate to April who prefers the current sheet.

**Pricing hypothesis.** $150–$300/mo or $1.5k–$3k fixed pilot, contingent on measured time savings. Not validated.

---

## Proposal 2 — Manning Pool Service: Inspection-to-Repair Queue (P02)

**Problem.** Each technician completes a monthly Hammerhead vacuum inspection on iPad by the last Thursday. Reports are emailed to a designated address; a manager manually compiles a list and updates a repair spreadsheet. Vacuums cost thousands; parts cost hundreds; hitch/battery/shell failures carry safety and liability risk.

**Pilot scope (4–6 weeks).**
1. Ingest the existing iPad inspection form (email parse or form webhook) into an asset registry keyed by tech/truck designator.
2. Auto-create repair tickets for any "fair/bad" item, with photo/description, priority, and overdue-inspection flags.
3. Track parts/labor cost per asset and repair status; produce a monthly manager queue replacing the manual spreadsheet.
4. Read-only export back to email/CSV; do not replace the FSM or customer-facing door hangers.

**Success metrics.** 100% of monthly inspections captured without manual compilation; repair-ticket creation lag <1 hour; manager spends ≤15 min/month on queue review; zero missed overdue inspections.

**Alternatives.** Skimmer/Jobber/ServiceTitan asset modules; Fleetio/MaintiX-style fleet maintenance; a simple Airtable/Forms automation. The wedge is the specific email→spreadsheet handoff and tech-accountability designator.

**Complexity.** Low–medium. Main risk is form format variability and whether an FSM already has asset work orders. Start with one month's emailed reports as a batch import.

**Owner discovery questions.**
- Is the monthly inspection still emailed and compiled manually in 2026?
- What form/app produces the iPad report, and can it webhook/export?
- Do you already use an FSM asset module? Why does the spreadsheet persist?
- Who decides repair vs replace, and how is tech responsibility tracked?
- Would a per-asset repair history change purchasing or accountability?

**Rejection risks.** Existing FSM may already solve this; monthly cadence may be too low for SaaS; family ownership transition; article is 2022 and workflow may have changed.

**Pricing hypothesis.** $100–$250/mo per branch or $2k–$4k fixed pilot. Not validated.

---

## Proposal 3 — Kroopin's Poopin Scoopin: Customer Margin & Pricing Audit (P03)

**Problem.** Erica Krupin manually pulled the last 10 time entries per customer into Excel to compute average service time and set pricing against a ~$110/man-hour target. Spring rush creates extreme volume (28 missed calls in one day historically; 1,904 Q1 requests in 2026). Pricing, churn, and CAC are tracked in spreadsheets.

**Pilot scope (3–5 weeks, read-only).**
1. Ingest Jobber time entries + invoices/revenue per customer (CSV or API).
2. Compute rolling average service time, effective man-hour rate, and margin flag per yard.
3. Produce a price-increase candidate list (under-target yards) with estimated revenue impact and churn-risk notes.
4. Seasonal capacity view: visits/week vs tech hours, spring-rush load forecast.
5. No changes to Jobber routing, invoicing, or Quo phone workflows.

**Success metrics.** Reproduce Erica's manual audit for ≥100 customers in <1 hour; identify ≥10 under-priced yards; owner accepts ≥3 price-increase recommendations as plausible.

**Alternatives.** Jobber reports + Excel; LMN/SingleOps-style landscape costing; a VA/bookkeeper; Erica's own spreadsheet skill. The wedge is automated per-customer labor-burden pricing across many visits.

**Complexity.** Medium. Jobber API/time-entry export quality is the main risk; yard-size variability and drive time must be handled carefully. Start with CSV export.

**Owner discovery questions.**
- Do you still pull time entries manually to set prices, or has Jobber reporting solved it?
- What man-hour target and churn tolerance should drive recommendations?
- Would you pay for a pricing audit, or is this coaching content you give away?
- How do you want drive time and yard-size outliers treated?
- Is the budget closer to $50/mo, $150/mo, or a one-time audit fee?

**Rejection risks.** Small budget; owner is a coach who may prefer spreadsheets; phone problem already solved by Quo/Nicole; Jobber may add native costing.

**Pricing hypothesis.** $75–$150/mo or $500–$1k one-time audit. Not validated.

---

## Proposal 4 — John Owens Services: ServiceTitan↔QuickBooks Reconciliation Exception Queue (P04)

**Problem.** Active bookkeeper posting requires hands-on ServiceTitan, batch review, inventory/cost accounting, and "troubleshooting ServiceTitan-to-QuickBooks discrepancies." The role exists to research accounting/batching issues and keep financial records accurate across ServiceTitan, QBO, and QuickBooks Desktop.

**Pilot scope (6–8 weeks, read-only).**
1. Ingest ServiceTitan batch/export reports and QBO/Desktop transaction exports.
2. Match invoices/payments/batches across systems; flag missing, duplicate, mismatched, or misclassified items.
3. Inventory/cost variance flags for truck stock and job costs.
4. Produce an exception queue + audit trail for the office manager/bookkeeper; no write-back to either system.

**Success metrics.** Reduce month-end discrepancy research time by ≥30%; catch ≥90% of known discrepancy types in a test month; bookkeeper trusts the queue enough to work from it.

**Alternatives.** ServiceTitan native integration/reports; QBO sync apps; a skilled bookkeeper (the current hiring plan); Ramp/Brex-style expense tools. The wedge is the cross-system exception layer, not core accounting.

**Complexity.** High. ServiceTitan API access, QuickBooks Desktop export, and accounting liability are real barriers. Requires owner/bookkeeper sign-off on matching rules. Start with one month of static exports.

**Owner discovery questions.**
- What are the top 3 recurring ServiceTitan→QBO discrepancy types?
- Is the bookkeeper hire meant to solve this manually, or would tooling help?
- Can we get read-only batch/transaction exports for a test month?
- Who signs off on accounting accuracy, and what liability is acceptable?
- Does ServiceTitan support already offer a reconciliation report you've tried?

**Rejection risks.** ServiceTitan may already solve it; hiring a bookkeeper is the preferred fix; accounting liability; QuickBooks Desktop complexity; 34 vs 51–200 headcount conflict suggests directory noise.

**Pricing hypothesis.** $300–$600/mo or $5k–$10k fixed pilot. Not validated.

---

## Proposal 5 — Ace Pool & Spa: Seasonal Lighting Quote-to-Actuals (P05)

**Problem.** Ace added holiday lighting to bridge the pool offseason (~40% of pools close in winter). Early installs were misquoted because labor time was unpredictable; the company over-bought ~$10,000 of lighting inventory. Alex now uses a spreadsheet for scheduling and quoting light installs.

**Pilot scope (one lighting season, 6–10 weeks build + season-long capture).**
1. Template-based lighting estimates (linear footage, stories, roof pitch, tree vs house, reusable vs new inventory).
2. Inventory allocation/reuse tracker: serialize reusable bulbs/strings, allocate to jobs, track returns/damage.
3. Install-time actuals capture per job; feed back into estimate norms.
4. Crew scheduling board for the pool-closing/lighting overlap window.
5. Margin report per lighting job; no replacement of pool FSM.

**Success metrics.** Reduce quote-to-actual labor variance by ≥25% by season end; track ≥90% of reusable inventory; produce per-job margin for all lighting installs.

**Alternatives.** The existing spreadsheet; Jobber/Housecall Pro quoting; CrewTracker/LMN-style landscape estimating; a seasonal VA. The wedge is reusable-inventory tracking + install-time learning curves specific to holiday lighting.

**Complexity.** Medium. Main risk is seasonal timing (must build before Nov rush) and small data volume. Start with spreadsheet import and a simple mobile actuals form.

**Owner discovery questions.**
- Is the lighting spreadsheet still the system of record in 2026?
- What quote variables caused the worst misquotes?
- How much inventory is reusable vs consumable, and how is it tracked today?
- Would you pay for a seasonal tool, or only per-season?
- Can we capture actuals from crews without slowing installs?

**Rejection risks.** Small team (~6); seasonal-only revenue; owner may be satisfied with spreadsheet; reusable inventory reduces urgency; build timing may miss the season.

**Pricing hypothesis.** $500–$1.5k per season or $100–$200/mo during season. Not validated.

---

## First-prospect recommendation

**Start with P01 Serene Clean.** Highest score, freshest repeated weekly workflow, public owner, and a low-liability read-only wedge. The first call should confirm whether the Tuesday KPI/supply compilation is still painful, who owns it, and whether a read-only dashboard would be trusted over the existing spreadsheet. If Serene declines or the pain is solved, fall back to P02 Manning (clear asset workflow) or P05 Ace (fresh seasonal evidence, but time-sensitive).

## Cross-prospect guardrails

- Do not replace Jobber, ServiceTitan, Workiz, QuickBooks, or ZenMaid.
- Start read-only; earn write-back later.
- Require a named owner and a measurable before/after metric before building.
- Treat all pricing as hypotheses; no prospect has confirmed willingness to pay.
- Kill any pilot where the owner says the current spreadsheet/workaround is intentional control, not pain.
