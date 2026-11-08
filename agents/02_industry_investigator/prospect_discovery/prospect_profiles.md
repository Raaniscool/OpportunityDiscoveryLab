# Prospect Profiles — US Home Services & Local Trades

Research cutoff: 2026-11-08. Evidence IDs refer to [evidence_ledger.md](evidence_ledger.md). Confidence reflects evidence that the problem is recurring and not already solved, not merely that the business exists.

---

## P01 — Serene Clean

- **Location:** Western Wisconsin (Sparta / Black River Falls / Mindoro area); owner operates remotely from Savannah, GA.
- **Trade:** Residential + commercial cleaning; ~50% commercial.
- **Website:** https://serene-clean.com/
- **Size evidence:** 30+ staff (Maid Summit 2025 speaker bio); owner says 25–30 staff depending on day in June 2026 podcast.
- **Decision-maker:** Stephanie Pipkin, founder/owner. Payroll manager April maintains supply/inventory tracking.
- **Current stack:** QuickBooks Online, Gusto, Google Drive/Sheets, card/bank payment processing; ZenMaid ecosystem/podcast presence (not verified as Serene's scheduling system).
- **Recurring problem:** Weekly manual financial and operational KPI compilation. Stephanie runs a QBO P&L every Tuesday and manually updates a Google Drive financial tracking sheet (revenue, expenses, profit, AR, five bank-account balances). April maintains a weekly per-product tool/supply spreadsheet that Stephanie calls "tedious." Client hourly-rate/margin audits and QBO revenue tagging are also manual.
- **Direct evidence:** "April's got this glorious spreadsheet that breaks down every single week... I know that that's tedious." Disposable toilet-wand misuse was costing "hundreds of dollars... a month" before tracking fixed it. [S01]
- **Frequency / economic signal:** Weekly KPI ritual; monthly supply-spend trend review; quarterly/6-month commercial margin audits. Supplies normally 2–3% of revenue; 4% triggers investigation.
- **Confidence:** High — current, first-person, repeated manual workflow.
- **Custom wedge:** Read-only KPI/supply-margin dashboard that ingests QBO + Gusto + supply receipts, auto-builds the weekly sheet, flags supply anomalies and under-margin clients.
- **Why not just existing tool:** QBO/Gusto already exist; the pain is cross-system compilation and anomaly detection, not core accounting.
- **Risks:** Owner may prefer spreadsheet control; ZenMaid/QBO reporting may already cover part of this; supply misuse was already corrected once.

## P02 — Manning Pool Service

- **Location:** Houston, TX.
- **Trade:** Pool maintenance, repair, renovation; Pentair warranty work.
- **Website:** https://manningpoolservice.com/
- **Size evidence:** 34 employees, ~30 vehicles, ~650 weekly maintenance accounts (PoolPro 2020/2022); $4.5M revenue in 2021.
- **Decision-maker:** Ana Manning, co-owner/COO (author of the inspection article). David Manning and Jeffrey Manning are also named owners in trade press; official site still highlights founders Jeff/Susan.
- **Current stack:** iPad digital inspection reports, designated email inbox, manager-maintained repair spreadsheet, digital door hangers.
- **Recurring problem:** Each technician completes a monthly Hammerhead vacuum inspection on iPad by the last Thursday. Reports are emailed to a designated address; a manager manually compiles a list and updates a spreadsheet of needed repairs. Vacuums cost thousands; parts cost hundreds.
- **Direct evidence:** "The reports are sent to a designated email address where the manager compiles a list and updates the spreadsheet of what needs to be repaired." [S05]
- **Frequency / economic signal:** Monthly inspection cycle across ~30 vehicles/vacuums; asset-life and safety liability (hitch failure, battery corrosion, cracked shells).
- **Confidence:** High for documented workflow; medium for current unmet need because article is 2022 and no follow-up confirms it remains manual.
- **Custom wedge:** Inspection-to-repair queue: parse iPad/form submissions, auto-create repair tickets by asset/tech, track parts/labor, overdue inspections, and damage responsibility.
- **Why not just existing tool:** No FSM/asset module is named; the gap is the email-to-spreadsheet handoff.
- **Risks:** May already use Skimmer/Jobber/ServiceTitan asset features; monthly cadence may be too low for SaaS pricing; family ownership transition.

## P03 — Kroopin's Poopin Scoopin

- **Location:** Westland / Northville / Western Wayne County, MI.
- **Trade:** Pet-waste removal; recurring residential + small commercial.
- **Website:** https://www.poopinscoopin.com/
- **Legal entity:** Kroopin Services LLC.
- **Size evidence:** 1–10 employees (directory); CNBC 2024: one full-time scooper + VA; Quo 2026: two full-time + two part-time field techs, admin, part-time social/events; ~305 backyards/week; ~$250k 2024 revenue, ~$500k 2026 run-rate.
- **Decision-maker:** Erica Krupin, founder/owner. Nicole handles phones/sales; Phalane is accountant.
- **Current stack:** Jobber (since 2019/2020), Quo/OpenPhone, Excel spreadsheets, Google/Meta ads.
- **Recurring problem:** Manual per-customer time and pricing audits. Erica pulled the last 10 time entries for every customer into Excel to compute average service time and set pricing against a ~$110/man-hour target. Spring rush creates extreme call/lead volume; missed calls reached 28 in one day before phone process changes.
- **Direct evidence:** "I went into every single one of my customers, pulled the last 10... entries for their time to get an average... I'd have to look at my spreadsheet." [S08] Quo case study confirms 1,904 Q1 requests and ongoing phone-capacity hiring. [S09]
- **Frequency / economic signal:** Seasonal spring/fall rushes; pricing audits tied to labor burden; LTV ~$1,200 and ~40% close rate cited in podcast.
- **Confidence:** High that manual pricing/time audits occurred; medium that they remain unmet because Quo/Jobber and hiring solved much of the phone problem.
- **Custom wedge:** Route/customer margin audit: ingest Jobber time entries + revenue, compute rolling average service time, flag under-priced yards, model price increases and seasonal capacity.
- **Why not just existing tool:** Jobber handles scheduling/invoicing; the gap is per-customer labor-burden pricing analysis across many visits.
- **Risks:** Small budget; owner is coaching/consulting and may build spreadsheets herself; phone problem partially solved.

## P04 — John Owens Services

- **Location:** Petaluma / San Rafael / Santa Rosa, CA (Marin & Sonoma).
- **Trade:** Plumbing, HVAC, radiant, electrical, boilers.
- **Website:** https://johnowensservices.com/
- **Size evidence:** BBB lists 34 employees; ZipRecruiter employer profile says 51–200 (conflict preserved).
- **Decision-maker:** John Owens, founder/president; Nicole Tolentino, office manager (BBB).
- **Current stack:** ServiceTitan, QuickBooks Online, QuickBooks Desktop.
- **Recurring problem:** Recurring ServiceTitan-to-QuickBooks financial reconciliation workload. Active bookkeeper posting requires hands-on ServiceTitan, batch review, inventory/cost accounting, discrepancy research, and troubleshooting ServiceTitan-to-QuickBooks differences.
- **Direct evidence:** Job description: "Experience troubleshooting ServiceTitan-to-QuickBooks discrepancies... Experience managing a high volume of transactions, vendors, invoices, and batches." [S13, S14]
- **Frequency / economic signal:** Daily/weekly batches, month-end reconciliation, inventory accounting; $30–42/hr bookkeeper role.
- **Confidence:** Medium-high — hiring proves recurring workload and budget, but is not an explicit complaint that software fails.
- **Custom wedge:** ServiceTitan↔QBO reconciliation exception queue: batch matching, missing/duplicate invoice detection, inventory/cost variance flags, audit trail for office manager.
- **Why not just existing tool:** ServiceTitan and QBO are already core; the pain is the reconciliation layer between them.
- **Risks:** ServiceTitan may already offer integration/reports; accounting liability; hiring a bookkeeper may be the preferred solution.

## P05 — Ace Pool & Spa

- **Location:** Antioch / Nashville, TN.
- **Trade:** Pool service + seasonal holiday lighting.
- **Website:** https://acepoolandspaservice.com/
- **Size evidence:** Official team page names ~6 people (owner, admin/billing lead, admin assistant, three junior techs); LinkedIn band 11–50 with 6 employees listed.
- **Decision-maker:** Alex Johnson, owner. Mary heads administration/billing.
- **Current stack:** Spreadsheet for holiday-lighting scheduling/quoting; pool-service software not named.
- **Recurring problem:** Seasonal holiday-lighting expansion caused labor misquotes and inventory over-buying. Alex says they had no formula for install time, misquoted jobs, and bought ~$10,000 of lighting inventory. Now uses a spreadsheet for scheduling and quoting light installs.
- **Direct evidence:** "We had no idea how to quote install time... now he has a spreadsheet for scheduling and quoting light installs." ~$10k inventory estimate. [S17]
- **Frequency / economic signal:** Annual seasonal cycle; ~40% of pools close in winter; lighting projects overlap pool-closing rush.
- **Confidence:** High — 2026 trade-press quotes describe current spreadsheet-based seasonal workflow.
- **Custom wedge:** Seasonal lighting quote-to-actuals: template-based estimates, inventory allocation/reuse tracking, install-time actuals, crew scheduling, margin feedback.
- **Why not just existing tool:** Generic FSM quoting may not capture reusable lighting inventory and install-time learning curves.
- **Risks:** Small team; seasonal revenue; owner may be satisfied with spreadsheet; inventory may be reusable enough to reduce urgency.

## P06 — Great Valley Pool Service

- **Location:** Frazer, PA.
- **Trade:** Pool service, retail, openings/closings, awnings, holiday lighting.
- **Website:** https://www.greatvalleypool.com/
- **Size evidence:** ~25 service trucks, 400+ recurring customers, 1,500+ opening/closing customers (2022 profile); awning division seven-figure revenue.
- **Decision-maker:** Tracy Bond, owner (finance/marketing/HR/retail); Cecil Bond, VP (sales/operations).
- **Current stack:** Online store, text surveys, seasonal retail/lighting operations; core FSM/accounting not named.
- **Recurring problem:** Owner-stated goal to eliminate manual functions and improve real-time tracking for financial accounting and order processing. Seasonal diversification (lighting, awnings, retail) adds order/inventory complexity.
- **Direct evidence:** "Hoping to eliminate many manual functions... better tracking and more efficient real-time updates... specifically over financial accounting and order processing." [S20]
- **Frequency / economic signal:** Continuous order processing across pool service, retail, awnings, and seasonal lighting.
- **Confidence:** Medium — explicit automation goal, but primary quote is from Jan 2022; 2026 article confirms seasonal operations but not the manual gap.
- **Custom wedge:** Order-to-accounting reconciliation across service/retail/seasonal divisions; real-time order status and exception flags.
- **Why not just existing tool:** Multi-division order flow may outgrow a single pool-service or retail system.
- **Risks:** Goal may already be solved; larger/older business may have entrenched systems; evidence age.

## P07 — DFW Turf Solutions

- **Location:** Dallas / Fort Worth, TX (group also expanded to Austin and Atlanta).
- **Trade:** Artificial turf installation (residential + commercial).
- **Website:** https://dfwturf.com/
- **Size evidence:** ZoomInfo 11–50; Datanyze ~20; RocketReach ~10 (conflict preserved). Multi-location rollup.
- **Decision-maker:** Johannes Hock, President (interviewed operator); Bennett Barrier, CEO (directory).
- **Current stack:** Workiz, CallRail, UTM tracking, internal lead database / "lead Bible" spreadsheet.
- **Recurring problem:** Quarterly manual reconciliation between the internal operational system and the marketing "lead Bible" to verify lead source attribution and customer acquisition cost.
- **Direct evidence:** "Quarterly we go through and check those two databases against each other... that probably sounds like a lot of work and a lot of like verification." [S23]
- **Frequency / economic signal:** Quarterly reconciliation; high-ticket installs (~$10k–$20k); CAC can be $500–$1,500.
- **Confidence:** Medium — first-person 2024 interview; current state may have changed with scale/shared services.
- **Custom wedge:** Lead-source reconciliation / CAC audit layer between Workiz, CallRail, and finance spreadsheet.
- **Why not just existing tool:** Workiz + CallRail exist; the gap is cross-system attribution verification.
- **Risks:** Multi-location rollup may centralize ops; ServiceTitan/Aspire migration; quarterly cadence may not justify custom SaaS.

## P08 — Mountain West Air Conditioning & Heating

- **Location:** Washoe Valley / Reno / Sparks / Carson City, NV.
- **Trade:** HVAC, electrical (EV chargers/panels), backup generators.
- **Website:** https://www.mountainwestac.com/
- **Size evidence:** Official team page says 12+ team members; podcast says ended 2024 with 13 employees, ~$4M revenue, targeting $5–6M.
- **Decision-maker:** Andrew Morrell, owner (100% owned, no investors).
- **Current stack:** ServiceTitan (underused), custom spreadsheet for monthly/weekly/daily revenue goals and marketing percentages.
- **Recurring problem:** Owner manually maintains goal/percentage spreadsheets because ServiceTitan is not used to its potential and support is weak for a small customer. Marketing spend attribution and daily capacity planning are spreadsheet-driven.
- **Direct evidence:** "Now we use Service Titan. I don't use it to its potential... small fish, they don't tend to give me great support." Own spreadsheet calculates daily/weekly averages and reverse-engineered revenue goals. [S26]
- **Frequency / economic signal:** Daily call-board review; weekly/monthly goal tracking; marketing budget <$100k on $5–6M revenue.
- **Confidence:** Medium — first-person interview, but episode is Feb 2025 and some needs may be addressed by ServiceTitan coaching/CSR hire.
- **Custom wedge:** Lightweight ServiceTitan-adjacent KPI/goal dashboard and marketing-spend attribution, not a replacement FSM.
- **Why not just existing tool:** ServiceTitan dashboards exist but owner reports underuse/support gap; spreadsheet is the workaround.
- **Risks:** ServiceTitan implementation partner may solve this cheaper; custom dashboard could duplicate native reports; do not attribute John Wilson's material-checklist quote to Andrew.

## P09 — Landscaping by J. Michael

- **Location:** Marshfield, MA (Plymouth County / South Shore).
- **Trade:** Commercial + residential landscape, maintenance, hardscape, irrigation, snow.
- **Website:** https://landscapingbyjmichael.com/
- **Size evidence:** LinkedIn 11–50 employees; directory estimates 11–20.
- **Decision-maker:** Michael Lesher, owner. Role reports to Owner / Finance Manager.
- **Current stack:** QuickBooks Online (required), Excel (formulas/pivots/reconciliations), payroll provider, external accountant.
- **Recurring problem:** Recurring full-cycle bookkeeping and month-end reporting workload; active hire is expected to improve bookkeeping processes and find efficiencies.
- **Direct evidence:** Job posting: "Help improve bookkeeping processes and find ways to make things more efficient"; "Interest in improving workflows or using automation tools." [S29]
- **Frequency / economic signal:** Monthly/quarterly P&L, balance sheet, cash flow; AP/AR; reconciliations; $55k–$62k salary.
- **Confidence:** Medium — hiring-based workload evidence, not an explicit software complaint.
- **Custom wedge:** Month-end close checklist / QBO-Excel reconciliation automation and reporting pack.
- **Why not just existing tool:** QBO + Excel are already used; the gap is process orchestration and reporting.
- **Risks:** New bookkeeper may solve manually; generic accounting automation is crowded; no named FSM integration.

## P10 — Summit View Water

- **Location:** Conway / Tamworth, NH.
- **Trade:** Water treatment / filtration / indoor air quality sales and service.
- **Website:** https://www.summitviewwater.com/
- **Size evidence:** LinkedIn 2–10; official about page names four staff (President, Business Director, Assistant GM, Water Specialist); careers page hiring Administrative Coordinator.
- **Decision-maker:** David A. Sclama, President; Nicole L. Sclama, Business Director (Jobber reply signed Nicole).
- **Current stack:** Jobber, website request forms, spreadsheet exports, custom Sales/Service request field.
- **Recurring problem:** Jobber request pile-up workaround. Office manually enters requests from calls/service notes; unscheduled NEW requests are converted to dated assessments (no time) to trigger emails and clear the request bucket; requests are exported to spreadsheets for sorting.
- **Direct evidence:** "With each request daily, if we are not able to SCHEDULE an appointment, we assign any remaining NEW request as an assessment... Exporting the Requests to a spreadsheet... now have thousands." [S32]
- **Frequency / economic signal:** Daily request triage; thousands of requests since August; admin hiring.
- **Confidence:** Medium-high — named business forum reply + active admin hiring; workaround may be acceptable.
- **Custom wedge:** Jobber request triage dashboard / assessment automation with Sales/Service routing and zero-inbox workflow.
- **Why not just existing tool:** Jobber lacks a contacted/attempted request stage; Bento and other vendors already market this gap.
- **Risks:** Small budget; existing Jobber add-ons (Bento, Adhesion) may solve; workaround already functioning.

## P11 — Team 8 Cleaning & Services

- **Location:** Gilbert / East Valley, AZ.
- **Trade:** Residential + commercial cleaning, junk removal, handyman.
- **Website:** https://azteam8.com/
- **Size evidence:** BBB started 2023; small team (Angelica CEO, Gema Team Coordinator); no verified headcount.
- **Decision-maker:** Angelica Morales, owner.
- **Current stack:** Jobber (clock-in/out, two-way texting).
- **Recurring problem:** Manual arrival and "safe to return" client messages tied to team clock-in/clock-out. Owner says this is becoming difficult as the team grows and handles multiple jobs per day.
- **Direct evidence:** "Currently, I have to send these messages manually, which is becoming difficult to manage as my team grows and handles multiple jobs per day." [S36]
- **Frequency / economic signal:** Multiple jobs per day; customer-experience feature from previous CRM.
- **Confidence:** Medium — named owner complaint, but ~1 year old and a Jobber marketplace workaround (Adhesion Connect) was suggested.
- **Custom wedge:** Jobber timesheet-event → SMS notification automation with branded arrival/completion messages.
- **Why not just existing tool:** Jobber native "on my way" is not the same as clock-in/clock-out automation; Adhesion/Zapier is a partial alternative.
- **Risks:** Very small business; may already have implemented Adhesion Connect; low ACV.

## P12 — Huge Home Pros

- **Location:** San Diego, CA.
- **Trade:** Handyman / home improvement / remodeling.
- **Website:** https://www.hugehome.pro/
- **Size evidence:** BBB started 2022; official team photo shows small crew; Jobber vendor page claims $1.2M revenue and 40 hrs/week saved (vendor claim, not independently verified).
- **Decision-maker:** Greg Schmitt, owner (BBB + official reviews).
- **Current stack:** Jobber, GoHighLevel (Snipey Leads mod), Plaud/AI transcription (forum), Google Calendar.
- **Recurring problem:** Service-agreement administration in Jobber feels "chunky" via recurring jobs. Owner also runs lead-bucket/nurture workflows outside Jobber because request status is insufficient.
- **Direct evidence:** "One of the places I feel like Jobber could improve the most is making service agreements more easy to administrate. It's a little chunky doing the re-occurring job thing." [S39]
- **Frequency / economic signal:** Recurring service agreements; lead follow-up automation.
- **Confidence:** Medium — named owner forum posts, but he is a Jobber coach and may already have solved much via GHL.
- **Custom wedge:** Service-agreement admin layer: contract terms, visit entitlements, renewal/billing status, Jobber recurring-job audit.
- **Why not just existing tool:** Jobber recurring jobs are not a full agreement object; GHL handles leads, not agreements.
- **Risks:** Owner is automation-savvy and may prefer no-code; Jobber may ship native agreements; small ACV.

## P13 — Municipal Backflow

- **Location:** Island Lake, IL (Northern Illinois).
- **Trade:** Backflow testing, repair, installation, regulatory submission.
- **Website:** https://municipalbackflow.com/
- **Size evidence:** D&B 1–24; Buzzfile ~6; Salary.com 6–10 (estimates).
- **Decision-maker:** Conflicting directories: Mike Harbut (D&B/Buzzfile CEO) vs Joanna Stachel (BuildZoom owner). Must verify before outreach.
- **Current stack:** Claims "cutting edge software" developed in-house; QuickBooks invoicing; online scheduling.
- **Recurring problem:** Payment-gated regulatory submission and manual report-copy requests. FAQ says reports are submitted only after payment; additional electronic copies are not automated and must be requested; city/software glitches cause missing-report notices.
- **Direct evidence:** "If you require an additional electronic copy... this is not an automated function you must request it." "A glitch in software / technology... prevented the receiving of the results." [S42]
- **Frequency / economic signal:** Annual testing cycle; billing/submission within 24h claims; customer confusion creates support calls.
- **Confidence:** Low-medium — current FAQ friction, but company already claims custom software and owner identity is unresolved.
- **Custom wedge:** Customer report-copy portal + submission-status tracker integrated with payment gate.
- **Why not just existing tool:** Their own software apparently lacks self-serve copies/status; a narrow portal could reduce support.
- **Risks:** They may prefer extending in-house software; regulatory submission complexity; owner conflict; low headcount.

## P14 — Green Impressions

- **Location:** Sheffield / Sheffield Village, OH.
- **Trade:** Landscape design/build, maintenance, irrigation, pools (Blue Impressions), snow.
- **Website:** https://mygreenimpressions.com/ (legacy greenimpressionslandscape.com returned 500).
- **Size evidence:** Exscape materials say 40+ person team; ZoomInfo lists 23 employees (conflict preserved).
- **Decision-maker:** Now part of Exscape Group (PE-backed, BHMS Investments). Local influencers: Nate Ehasz (fleet manager), Joe Schill / Jim Louth (founders, now group leadership). Economic buyer likely Exscape CEO Bill Dysert / group ops.
- **Current stack:** Historically Boss + HubSpot + spreadsheets; Exscape case study says Aspire rollout and centralized systems replaced patchworked tools.
- **Recurring problem:** Parts/shop management relied on texts to supplier for same-day restock, weekly maintenance emails, and manual forecasting. $4k rotating parts stock consumed every 4–6 weeks.
- **Direct evidence:** "Ehasz texts the owner of the equipment company when they use the parts... Those parts get 100% consumed every four to six weeks." Transitioned from basic spreadsheets to weekly emails. [S47]
- **Frequency / economic signal:** Weekly maintenance communication; 4–6 week parts consumption; 12-month parts forecast.
- **Confidence:** Medium for historical friction; low for current unmet need because Exscape/Aspire may have solved it.
- **Custom wedge:** Parts consignment / maintenance forecast dashboard if Aspire gap remains.
- **Why not just existing tool:** Aspire/CRM rollout may already address; only pursue if group confirms remaining shop-floor gap.
- **Risks:** PE-backed buying process; centralized IT; not a simple owner-buyer; evidence may be pre-integration.

## P15 — La Rosa Landscape Company

- **Location:** Cedarburg, WI.
- **Trade:** Landscape design/build, maintenance, lawn care.
- **Website:** https://www.larosalandscape.com/
- **Size evidence:** LinkedIn band 51–200 with 22 employees listed; RocketReach ~27; Prospeo 21–50 (conflict preserved).
- **Decision-maker:** Mike La Rosa, president/owner.
- **Current stack:** Include business software for assets; manual parts/service-request system; vendor consignment parts.
- **Recurring problem:** No parts/inventory software. Crews create manual service requests based on engine hours; $10k–$20k parts held on consignment with vendor replenishment every two weeks.
- **Direct evidence:** "We use Include business software and our assets are managed through that program... honestly, we use more of a manual system than anything else." [S50]
- **Frequency / economic signal:** Biweekly vendor replenishment; equipment uptime; $10k–$20k parts investment.
- **Confidence:** Low — strong first-person quote but from 2018; current state unknown.
- **Custom wedge:** Parts/consignment inventory + engine-hour service-request log beside Include.
- **Why not just existing tool:** Include manages assets but not parts inventory; manual requests are the gap.
- **Risks:** Eight-year-old evidence; may have adopted fleet/parts software; consignment vendor may already provide portal.
