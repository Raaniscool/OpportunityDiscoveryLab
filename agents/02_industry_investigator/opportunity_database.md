# Opportunity Database — 16 Ranked Opportunities

Research cutoff: **2026-11-08**. Scores are weighted 1–5 ratings normalized to 100:

`Score = (25×Demand + 20×Spending + 15×Inefficiency + 10×TechChange + 15×Feasibility + 15×Acquisition) / 5`

- **Demand** = strength of evidence that customers have the problem.
- **Spending** = evidence of existing budget / willingness to pay.
- **Inefficiency** = severity of money/time leakage.
- **TechChange** = tailwind from AI, regulation, or platform shifts.
- **Feasibility** = can a small team ship a credible wedge?
- **Acquisition** = can a small team reach buyers cheaply?

Competition intensity and growth are documented per opportunity but not double-counted in the score. Evidence grades: A/B/C/D as in [research_sources.md](research_sources.md).

## Ranking table

| Rank | ID | Opportunity | D | S | I | T | F | A | Score | Evidence | Competition | Growth |
|---:|---|---|---:|---:|---:|---:|---:|---:|---:|---|---|---|
| 1 | O01 | Accounting client-evidence chasing + CAS close | 5 | 4 | 5 | 4 | 4 | 4 | 88 | B | High generic / medium wedge | Medium |
| 2 | O02 | Freight detention/accessorial recovery | 5 | 4 | 5 | 3 | 4 | 4 | 86 | B | Medium | Medium-high |
| 3 | O03 | AI-built-app release-readiness audit | 4 | 4 | 4 | 5 | 4 | 4 | 82 | B | High scanners / medium packaging | High |
| 4 | O04 | Subcontractor bid scope/risk reconciliation | 4 | 4 | 5 | 4 | 3 | 4 | 80 | B | High PM / medium wedge | Medium |
| 5 | O05 | Specialty-clinic prior-auth evidence assembly | 5 | 5 | 5 | 4 | 2 | 2 | 80 | B | High | High |
| 6 | O06 | Agent eval/regression harness for vertical agencies | 4 | 4 | 4 | 5 | 3 | 3 | 76 | B | High | High |
| 7 | O07 | E-commerce returns exception evidence for 3PLs | 4 | 4 | 4 | 4 | 3 | 3 | 74 | B | High portals / medium 3PL | Medium |
| 8 | O08 | Home-services estimate follow-up / revenue recovery | 4 | 3 | 4 | 4 | 4 | 3 | 73 | B | High | Medium |
| 9 | O09 | Property maintenance triage / vendor coordination | 4 | 3 | 4 | 4 | 3 | 4 | 73 | B | High | Medium |
| 10 | O10 | Creator campaign ops, rights, payment reconciliation | 3 | 4 | 4 | 4 | 4 | 3 | 72 | B | High editing / medium ops | High |
| 11 | O11 | Small-manufacturer RFQ/compliance triage | 3 | 4 | 4 | 3 | 3 | 4 | 70 | B | Medium-high | Medium |
| 12 | O12 | IEP compliance and meeting prep | 4 | 3 | 5 | 3 | 3 | 2 | 68 | B | Medium-high | Medium |
| 13 | O13 | Marketplace seller onboarding/catalog compliance | 3 | 4 | 3 | 4 | 3 | 3 | 66 | C/B | High | Medium-high |
| 14 | O14 | Vet medication documentation / inventory compliance | 3 | 3 | 4 | 2 | 3 | 4 | 64 | C/B | Medium | Medium |
| 15 | O15 | Caregiver coordination (B2B2C) | 4 | 2 | 4 | 3 | 3 | 2 | 61 | B/D | Medium | High need, uncertain pay |
| 16 | O16 | Small water-utility compliance reporting | 3 | 2 | 4 | 3 | 3 | 2 | 56 | B/C | Medium | Medium |

---

## O01 — Accounting client-evidence chasing + year-round CAS close

**Score:** 88 · **Evidence:** B · **Competition:** High in generic portals; medium in CAS evidence reconciliation · **Growth:** Medium.

**Buyer.** Owner/partner of 2–50-person CPA or CAS/bookkeeping firm; operations manager.

**Wedge.** Not tax prep. A "missing evidence" loop for monthly CAS closes and tax organizers: ingest email/portal/QBO/Xero, identify missing documents per engagement, draft client reminders, and produce a close packet with unresolved items.

**Why now.** Firms are capacity-constrained and moving to recurring CAS. Karbon prices at $59–$89/user/mo; Soraban sells per-return organizers with $1,000–$4,500 setup; Liscio advertises $19–$49/user/mo tiers [1](https://karbonhq.com/pricing) [1](https://www.soraban.com/tax-organizer-software) [1](https://www.liscio.me/resources/liscio-vs-smartvault). SMB late-payment pain (56% owed money; avg $17,500) pulls accountants into cash-flow advisory [2](https://www.cnbc.com/select/how-to-paid-faster-small-business/).

**Pricing hypothesis.** $299–$999/firm/mo base + $2–$5 per active client engagement; $1,500–$5,000 implementation. Target ACV $6K–$25K.

**Channel.** Accounting Twitter/X, CPA practice-management communities, Karbon/Liscio integration marketplaces, state societies, CAS coaches, outbound to firms advertising CAS.

**Competitors.** Karbon, Liscio, Content Snare, Soraban, SmartVault, Client Hub, QBO/Xero practice tools, offshore staffing.

**Risks.** Incumbents bundle the feature; email/portal integration fragility; trust/security; seasonal churn; firms may prefer human VAs.

**Kill criteria.** <10 paid pilots from 100 targeted firms; average collected revenue uplift <10%; >30% of reminders require manual rewrite; buyers refuse per-engagement meter.

**Validation experiment.** Manually run a 30-day "missing items" service for 5 firms using their existing tools. Measure documents collected, hours saved, and close-cycle time. Sell the report before automating.

---

## O02 — Freight detention/accessorial recovery for small fleets and brokers

**Score:** 86 · **Evidence:** B · **Competition:** Medium · **Growth:** Medium-high.

**Buyer.** Owner of 5–100-truck fleet; broker operations/finance lead; factoring company.

**Wedge.** Recover unpaid detention and accessorials by assembling evidence: ELD/GPS timestamps, rate confirmation terms, dock photos, geofence arrival/departure, and invoice/dispute packets.

**Why now.** ATRI: $15.1B detention cost in 2023; 94.5% of fleets charge detention but <50% of invoices are paid [1](https://truckingresearch.org/2024/09/new-research-documents-substantial-financial-and-safety-impacts-from-truck-driver-detention/). TIA: 22% of brokers lost >$200K to fraud in six months, showing budget for revenue protection [1](https://news.tianet.org/tia-releases-state-of-fraud-in-the-industry-april-2025-report/). MyCarrierPortal starts at $515/mo, proving brokers pay for protection [1](https://www.mycarrierportal.com/features/pricing/).

**Pricing hypothesis.** $99–$499/fleet/mo + 10–20% of recovered accessorials; broker white-label tier.

**Channel.** Fleet associations, factoring companies, ELD marketplaces, freight brokers, Facebook/Reddit fleet groups, DAT/Truckstop ecosystem.

**Competitors.** DockClaim (launch pricing $49/mo, vendor page) [1](https://dockclaim.com/), TMS accessorial modules, factoring back-office tools, manual billing staff.

**Risks.** Low recovery rates; broker relationships damaged by aggressive disputes; ELD data access; contract terms vary; small fleets churn.

**Kill criteria.** Recovery <20% of claimed detention in 60-day pilot; brokers refuse evidence packets; ELD integration cost >$50K per major platform.

**Validation experiment.** Manually reconstruct 100 detention events for 3 fleets and submit invoices. Measure paid rate and days-to-cash.

---

## O03 — AI-built-app release-readiness and security audit

**Score:** 82 · **Evidence:** B · **Competition:** High in scanners; medium in packaged assurance · **Growth:** High.

**Buyer.** AI-native agency, startup CTO, internal IT lead shipping Lovable/Bolt/Replit/Cursor apps.

**Wedge.** A paid release gate: repo scan, config/auth/secrets checks, dependency/license review, basic penetration tests, and a human-readable risk report with fix plan. Not another code generator.

**Why now.** Stack Overflow 2025: 66% frustrated by almost-right AI code; 45% say debugging takes longer [1](https://survey.stackoverflow.co/2025). Veracode: 45% of AI code samples failed security tests [1](https://www.veracode.com/blog/genai-code-security-report). Snyk Team from $25/mo and CodeRabbit $24–$72/user/mo show paid security/review demand [1](https://snyk.io/plans/) [1](https://www.coderabbit.ai/pricing).

**Pricing hypothesis.** $500–$2,500 per audit; $299–$1,999/mo continuous assurance; agency white label.

**Channel.** AI builder communities, agencies, startup Slack/Discord, Product Hunt, security newsletters, partnerships with no-code builders.

**Competitors.** Snyk, CodeRabbit, Sonar, Semgrep, Veracode, GitHub Advanced Security, builder-native checks.

**Risks.** False positives; incumbents bundle; liability if breach occurs after audit; hobbyists won’t pay; builders add native gates.

**Kill criteria.** <10% conversion from 20 agency pitches; buyers demand unlimited rescans at <$99/mo; audit cannot find material issues in >50% of apps.

**Validation experiment.** Sell 10 manual audits at $1,000 each. Track findings severity and whether buyers fix/renew.

---

## O04 — Subcontractor bid scope/risk reconciliation

**Score:** 80 · **Evidence:** B · **Competition:** High in PM/takeoff; medium in scope-gap wedge · **Growth:** Medium.

**Buyer.** Specialty subcontractor estimator/owner; GC preconstruction lead.

**Wedge.** Compare bid invitation, drawings, specs, addenda, and vendor quotes to flag missing scope, exclusions, allowances, and change-order risk before submission.

**Why now.** AGC 2025: 44% plan to increase AI spend, 40% document management, 35% estimating [2](https://www.agc.org/sites/default/files/users/user21902/2025%20Outlook%20Virtual%20Media%20Briefing%20Remarks.pdf). RICS: 45% no AI use, showing low maturity but also integration barriers [1](https://www.rics.org/news-insights/artificial-intelligence-in-construction-report). Buildxact charges $199–$599/mo + $149 AI reviewer, proving estimating budgets [1](https://www.buildxact.com/us/pricing/).

**Pricing hypothesis.** $199–$799/user/mo + per-bid pack; GC-sponsored subcontractor tier.

**Channel.** Trade associations, estimating consultants, Buildxact/Procore ecosystems, LinkedIn construction groups, bid boards.

**Competitors.** Procore, Autodesk, Buildxact, Togal.AI, STACK, PlanSwift, Bluebeam, Sage.

**Risks.** Drawing parsing errors; liability for missed scope; long sales cycles; data confidentiality; incumbents add AI review.

**Kill criteria.** Estimators reject >30% of flags as noise; cannot process addenda reliably; pilot does not reduce bid review time by 25%.

**Validation experiment.** Run 10 live bids through manual reconciliation; compare flagged gaps to estimator notes and post-award change orders.

---

## O05 — Specialty-clinic prior-authorization evidence assembly

**Score:** 80 · **Evidence:** B · **Competition:** High · **Growth:** High.

**Buyer.** Specialty clinic administrator; RCM vendor; billing company.

**Wedge.** One specialty first (e.g., orthopedics, infusion, sleep). Extract clinical criteria from notes, build payer-specific evidence packets, track status, and draft appeals. Human reviews/submits.

**Why now.** AMA 2025: 40 PAs/physician/week, 13 hours/week, 40% dedicated staff, 95% delays [1](https://www.ama-assn.org/press-center/ama-press-releases/ama-survey-prior-authorization-reform-pledge-falls-short-physicians). CAQH: $21B remaining automation savings [1](https://www.dataspring.com/blog/2025-caqh-index-shows-u.s.-healthcare-avoided-258-billion-and-accelerated-automation-interoperability-and-ai-adoption). CMS API deadline Jan 2027 [1](https://www.cms.gov/newsroom/press-releases/cms-finalizes-rule-expand-access-health-information-improve-prior-authorization-process).

**Pricing hypothesis.** $300–$1,000/provider/mo or $3–$10 per authorization; RCM white label.

**Channel.** Specialty societies, RCM vendors, EHR marketplaces, billing companies, healthcare compliance consultants.

**Competitors.** Waystar, Availity, Optum, Cohere Health, Anterior, Rhyme, Infinitus, EHR modules.

**Risks.** HIPAA; EHR integration; payer rules change; liability; long procurement; well-funded incumbents.

**Kill criteria.** Cannot access notes legally; submission accuracy <95%; sales cycle >9 months; no RCM partner.

**Validation experiment.** Partner with one RCM vendor and manually assemble 200 auth packets; measure approval rate and staff hours.

---

## O06 — Agent eval/regression harness for vertical AI agencies

**Score:** 76 · **Evidence:** B · **Competition:** High · **Growth:** High.

**Buyer.** Vertical AI agency founder; head of delivery; enterprise AI platform team.

**Wedge.** Turn client workflows into reusable test suites, golden datasets, regression checks, and client-facing reliability reports. Vertical packs (healthcare admin, legal intake, accounting) rather than generic observability.

**Why now.** LangChain 2026: 57% agents in production; quality top barrier 32%; 89% observability but only 52% offline evals [1](https://www.langchain.com/state-of-agent-engineering). LangSmith Plus $39/seat/mo + usage; Braintrust Pro reported $249/mo + usage [1](https://www.langchain.com/pricing) [1](https://aitrendtool.com/tools/braintrust).

**Pricing hypothesis.** $499–$2,999/workspace/mo + usage; eval-suite setup service $5K–$20K.

**Channel.** LangChain/LangGraph communities, AI agency directories, enterprise AI consultancies, GitHub/OSS distribution.

**Competitors.** LangSmith, Braintrust, Langfuse, Arize, Galileo, Patronus, Humanloop, cloud tools.

**Risks.** Crowded; platforms bundle evals; agencies build scripts; usage costs; proving ROI.

**Kill criteria.** Agencies won’t pay >$500/mo; eval suites require >2 weeks setup per client; no renewal after 3 months.

**Validation experiment.** Sell eval-suite setup to 5 agencies; measure regression catches and client report usage.

---

## O07 — E-commerce returns exception evidence for 3PLs

**Score:** 74 · **Evidence:** B · **Competition:** High in portals; medium in 3PL evidence · **Growth:** Medium.

**Buyer.** 3PL operations director; DTC brand COO; returns processor.

**Wedge.** Capture inspection photos/serials/condition, link to order and policy, recommend refund/deny/restock/dispose, and generate dispute-ready evidence packets.

**Why now.** Radial 2025: 44% cite fraud/abuse as top pain; 91% apparel refunds before inspection; 48% in-house returns [1](https://www.radial.com/wp-content/uploads/2025/10/State-of-Returns_Report_2025_Final.pdf). Loop Returns from $340/mo for 1,000 returns shows paid category [1](https://www.loopreturns.com/pricing/). CBP de minimis changes raise cross-border returns complexity [3](https://www.cbp.gov/sites/default/files/2026-07/260708_bulletin_vol_60_no_18.pdf).

**Pricing hypothesis.** $0.10–$0.50 per return + warehouse base $499–$2,999/mo; fraud analytics add-on.

**Channel.** 3PL associations, WMS marketplaces, Shopify/returns ecosystems, reverse-logistics consultants.

**Competitors.** Loop, Narvar, AfterShip, ReturnGO, Two Boxes, Happy Returns, Optoro, WMS modules.

**Risks.** Warehouse hardware/integration; policy liability; fraud false positives; incumbents add evidence features.

**Kill criteria.** Inspection evidence does not change refund decisions; 3PLs refuse per-return fee; integration >3 months per WMS.

**Validation experiment.** Run a 2-week exception desk for one 3PL; measure disputed refunds avoided and labor per return.

---

## O08 — Home-services estimate follow-up / revenue recovery

**Score:** 73 · **Evidence:** B · **Competition:** High · **Growth:** Medium.

**Buyer.** Owner of 2–50-employee HVAC/plumbing/electrical/cleaning business; office manager.

**Wedge.** Sit on top of Jobber/HCP/QuickBooks: sequence estimate reminders, surface stale high-value estimates, recover missed calls, and request reviews. Lead with booked revenue, not AI.

**Why now.** Invoca 2026: home services 52% of calls answered by a person; 38% of answered calls are leads; 45% of leads convert on the call [1](https://www.invoca.com/reports/the-invoca-home-services-lead-conversion-benchmarks-report-2026). Jobber $49–$199/mo and HCP $59/mo show existing FSM spend [1](https://www.getjobber.com/pricing/) [1](https://www.housecallpro.com/pricing/).

**Pricing hypothesis.** $99–$299/location/mo + 1–3% success fee on recovered jobs.

**Channel.** Jobber/HCP app marketplaces, trade Facebook groups, local BNI/chambers, franchise consultants.

**Competitors.** Jobber/HCP native AI, ServiceTitan, Podium, Chiirp, Workiz, marketing agencies.

**Risks.** Incumbent bundling; low ACV; churn; SMS compliance; attribution disputes.

**Kill criteria.** Recovered revenue <5× fee; FSM API limits; >50% of owners prefer native tools.

**Validation experiment.** Manually follow up 200 stale estimates for 5 shops; measure booked jobs and attribution.

---

## O09 — Property maintenance triage / vendor coordination

**Score:** 73 · **Evidence:** B · **Competition:** High · **Growth:** Medium.

**Buyer.** Mid-size property manager (100–5,000 units); maintenance director.

**Wedge.** AI triage + vendor dispatch layer that integrates with existing PMS, documents emergencies, and scores vendor performance. Do not replace PMS.

**Why now.** Property Meld Ops $2.00/unit/mo with AI triage; MAX On-Call add-on proves per-unit maintenance budgets [1](https://propertymeld.com/pricing/). U.S. property management industry $139.9B in 2026 [1](https://www.ibisworld.com/united-states/industry/property-management/1356).

**Pricing hypothesis.** $1–$2/unit/mo + vendor network fee; minimum $200/mo.

**Channel.** PMS marketplaces (AppFolio/Buildium/Yardi), property-management associations, maintenance consultants.

**Competitors.** Property Meld, Lula, Maintenance Care, AppFolio/Buildium native maintenance, Yardi.

**Risks.** Strong incumbent; emergency liability; vendor network density; PMS integration politics.

**Kill criteria.** Cannot beat Property Meld on price/integration; emergency triage error rate >1%; managers refuse per-unit fee.

**Validation experiment.** Pilot triage for 500 units; measure after-hours cost, resolution time, and tenant satisfaction.

---

## O10 — Creator campaign ops, rights, and payment reconciliation

**Score:** 72 · **Evidence:** B · **Competition:** High in editing; medium in ops · **Growth:** High.

**Buyer.** Talent manager, mid-size creator agency, brand partnerships lead.

**Wedge.** Track deliverables, usage rights, exclusivity, invoices, and payments across campaigns; reconcile brand payments to creator payouts.

**Why now.** IAB: U.S. creator ad spend $37.1B in 2025, +26%; measurement/standardization gaps [2](https://www.iab.com/wp-content/uploads/2025/11/IAB_Creator_Ad_Spend_and_Strategy_Report_2025.pdf). Adobe: 86% of creators use genAI, increasing output volume [1](https://news.adobe.com/news/2025/10/adobe-max-2025-creators-survey).

**Pricing hypothesis.** $99–$499/manager/mo + 0.5–2% of payments or per-campaign fee.

**Channel.** Creator economy newsletters, talent-manager communities, agency partnerships, LinkedIn.

**Competitors.** CreatorIQ, GRIN, Aspire, Captiv8, Lumanu, Karat, Beacons, spreadsheets.

**Risks.** Platform API fragility; small creators won’t pay; enterprise incumbents; rights legal complexity.

**Kill criteria.** Managers won’t pay >$200/mo; reconciliation saves <5 hours/campaign; rights disputes require legal review beyond product scope.

**Validation experiment.** Reconcile 10 real campaigns manually; measure hours saved and payment errors caught.

---

## O11 — Small-manufacturer RFQ/compliance triage

**Score:** 70 · **Evidence:** B · **Competition:** Medium-high · **Growth:** Medium.

**Buyer.** Job-shop owner/estimator; contract manufacturer compliance lead.

**Wedge.** Extract requirements from RFQ emails/drawings, flag missing certs/tolerances/materials, draft quote assumptions, and assemble compliance packets.

**Why now.** NAM Q4 2025: 72.1% need skilled production workers [1](https://nam.org/wp-content/uploads/securepdfs/2025/12/NAM_Q4_2025_Outlook_Write_Up.pdf). Paperless Parts benchmark shows quoting/RFQ pressure [1](https://www.paperlessparts.com/resources/2025-manufacturing-industry-benchmark-report/). FDA traceability deadline Jul 2028 creates compliance tailwind [2](https://www.federalregister.gov/documents/2026/05/28/2026-10603/challenges-and-solutions-in-lot-level-food-traceability-public-meeting-and-request-for-comments).

**Pricing hypothesis.** $299–$999/shop/mo + per-RFQ volume.

**Channel.** Manufacturing associations, Paperless Parts/ProShop ecosystems, trade shows, LinkedIn machining groups.

**Competitors.** Paperless Parts, ProShop, Fulcrum, JobBOSS, E2, ERP vendors.

**Risks.** Drawing accuracy; ITAR/security; ERP integration; shop-floor trust; incumbent quoting AI.

**Kill criteria.** Requirement extraction error >10%; shops refuse cloud upload of drawings; no measurable quote-time reduction.

**Validation experiment.** Process 50 RFQs for 3 shops; compare extracted requirements to estimator notes.

---

## O12 — IEP compliance and meeting prep

**Score:** 68 · **Evidence:** B · **Competition:** Medium-high · **Growth:** Medium.

**Buyer.** Special education director; district compliance officer; co-op.

**Wedge.** Check IEP drafts against state/district rules, assemble meeting evidence, align goals/progress, and flag privacy risks. Human reviews; never auto-submits.

**Why now.** CDT: 57% of sped teachers used AI for IEP/504; 15% fully delegate without review [1](https://cdt.org/wp-content/uploads/2025/10/FINAL-CDT-2025-Hand-in-Hand-Polling-100225-accessible.pdf). Gallup: 60% teachers use AI; weekly users save 5.9 h/wk self-reported [1](https://news.gallup.com/poll/691967/three-teachers-weekly-saving-six-weeks-year.aspx). Census: $842.3B current school spending FY2024 [1](https://www.census.gov/newsroom/press-releases/2026/school-system-finances.html).

**Pricing hypothesis.** $2–$5/student/year district tier; co-op bulk license.

**Channel.** State special-ed associations, co-ops, Frontline/MagicSchool ecosystems, education consultants.

**Competitors.** Frontline, MagicSchool, SchoolAI, Diffit, Brisk, Playground IEP, EmbraceIEP.

**Risks.** FERPA/IDEA; procurement; state specificity; liability; teacher-tool crowding.

**Kill criteria.** No district paid pilot within 6 months; legal review blocks AI drafting; procurement >12 months.

**Validation experiment.** Run compliance checks on 100 anonymized IEPs with a district partner; measure error catch rate and prep time.

---

## O13 — Marketplace seller onboarding/catalog compliance

**Score:** 66 · **Evidence:** C/B · **Competition:** High · **Growth:** Medium-high.

**Buyer.** Marketplace operator; catalog operations lead; distributor.

**Wedge.** Validate seller feeds, map categories, generate missing content, flag compliance issues, and accelerate onboarding.

**Why now.** Mirakl: median onboarding 28 days; Catalog Transformer users 88% higher GMV (vendor claim) [1](https://www.mirakl.com/blog/the-marketplace-revolution-key-insights-from-our-2026-seller-report). Mirakl Platform GMV $14.6B in 2025, +31% [1](https://www.mirakl.com/news/mirakl-momentum-2025-key-results-launch-mirakl-nexus-agentic-commerce/).

**Pricing hypothesis.** Operator base $2K–$10K/mo + per-SKU/per-seller meter.

**Channel.** Mirakl/ChannelEngine/Rithum ecosystems, marketplace consultancies, retail trade groups.

**Competitors.** Mirakl native AI, ChannelEngine, Rithum, Feedonomics, Salsify, Akeneo, Plytix.

**Risks.** Vendor bias; native AI; operator trust; catalog scale; PIM integration.

**Kill criteria.** Onboarding time reduction <30%; operators insist on native tools; per-SKU pricing rejected.

**Validation experiment.** Clean one operator’s 5,000-SKU feed; measure rejection rate and onboarding days.

---

## O14 — Vet medication documentation / inventory compliance

**Score:** 64 · **Evidence:** C/B · **Competition:** Medium · **Growth:** Medium.

**Buyer.** Independent vet practice owner; practice manager; multi-site group.

**Wedge.** Controlled-drug logs, medication documentation, inventory expiry/reorder, and audit packets. Avoid scribes.

**Why now.** FVE 2025: 64% say admin doubled; medication documentation up to 10+ h/wk; >50% unpaid [1](https://fve.org/cms/wp-content/uploads/Admin-burden-report-R13-1.pdf). APPA: $39.8B U.S. vet care/product sales in 2024 (secondary) [1](https://www.petfoodprocessing.net/articles/19810-state-of-us-pet-food-treat-industry-in-2025). VetSnap case study: 5-DVM hospital ~$3,000/yr [1](https://go.vetsnap.com/pricing).

**Pricing hypothesis.** $99–$299/site/mo or $50–$100/DVM/mo.

**Channel.** Vet practice-management communities, state VMA associations, PIMS integrations, consultants.

**Competitors.** VetSnap, CUBEX, Covetrus, IDEXX, Digitail, Pawprints Vetlogs, Pawlytics.

**Risks.** Small EU sample; PIMS integration; controlled-drug rules; low ACV; scribe crowding adjacency.

**Kill criteria.** Practices won’t pay >$150/site/mo; PIMS access blocked; documentation time reduction <30%.

**Validation experiment.** Pilot medication log reconciliation at 5 practices; measure hours saved and audit readiness.

---

## O15 — Caregiver coordination (B2B2C only)

**Score:** 61 · **Evidence:** B for need / D for app market · **Competition:** Medium · **Growth:** High need, uncertain monetization.

**Buyer.** Employer benefits lead; Medicare Advantage plan; home-care agency; health system discharge planner.

**Wedge.** Caregiver task/medication/appointment coordination sold through institutions, not direct consumer subscription.

**Why now.** AARP/NAC: 63M U.S. caregivers, +20M since 2015; complex tasks common; training gaps [1](https://www.aarp.org/press/releases/2025-07-24-new-report-reveals-crisis-point-for-americas-63-million-family-caregivers.html). Consumer apps are mostly free/low-cost: Caring Village official pricing is Free / $14.99 / $24.99 per month [1](https://caringvillage.com/pricing/).

**Pricing hypothesis.** $1–$3/employee/member/mo; agency license $500–$2,000/mo.

**Channel.** Benefits brokers, payer innovation teams, home-care associations, discharge-planning vendors.

**Competitors.** Caring Village, CareZone, Lotsa Helping Hands, Ianacare, Carely, Papa, employer benefit platforms.

**Risks.** Payer procurement; privacy; engagement; proving ROI; free alternatives.

**Kill criteria.** No institutional design partner with paid pilot in 6 months; engagement <20% weekly; payer refuses ROI model.

**Validation experiment.** Run a 90-day employer/payer pilot with 200 caregivers; measure absenteeism, care-plan adherence, and support tickets.

---

## O16 — Small water-utility compliance reporting

**Score:** 56 · **Evidence:** B/C · **Competition:** Medium · **Growth:** Medium.

**Buyer.** Small water-system operator; circuit rider; state association; private water company.

**Wedge.** Compliance calendar, sampling schedule, report assembly, operator knowledge capture, and funding-application support.

**Why now.** EPA DWINSA: $625B 20-year need [1](https://www.epa.gov/dwsrf/epas-7th-drinking-water-infrastructure-needs-survey-and-assessment). CRS: ~50,000 community systems, ~91% small [1](https://www.congress.gov/crs-product/R47315). Waterly prices by flow; Samples add-on <$800/yr to 40% of Rounds [1](https://waterly.com/hot-sauce/).

**Pricing hypothesis.** $500–$2,500/system/year; association bulk license.

**Channel.** State rural water associations, circuit riders, EPA TA grants, conference circuit.

**Competitors.** Waterly, 120Water, Klir, SwiftComply, XC2, free state iWriter tools, consultants.

**Risks.** Low budgets; state specificity; free tools; procurement; liability.

**Kill criteria.** ACV <$1,000; sales cycle >9 months; free state tool covers core need.

**Validation experiment.** Partner with one state association; assemble reports for 10 systems; measure time saved and renewal intent.

---

## Portfolio logic

- **Top 5** combine strong demand evidence with existing spend. O05 scores high on pain but low on feasibility/acquisition; it is a partner-led play, not a solo-founder sprint.
- **O02 and O03** are the best unconventional wedges: measurable money recovery and a new AI-era assurance category.
- **O08/O09** are large but crowded; enter only with a distribution advantage or incumbent integration.
- **O15/O16** are real social needs but weak commercial signals; require institutional payers before investment.
- **Not ranked:** generic productivity, generic creator editing, broad game-dev tools, consumer caregiving subscriptions, and precision-ag analytics for farmers. Evidence shows crowding, weak WTP, or adoption overestimation.
