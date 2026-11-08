# Emerging Markets and AI-Transformation Hypotheses

Research cutoff: **2026-11-08**. This file treats AI transformation as a set of **hypotheses**, not guaranteed outcomes. Each hypothesis includes supporting evidence, counter-evidence, and a validation test. Evidence grades follow [research_sources.md](research_sources.md).

## How to read this file

- **H#** = hypothesis.
- **Confidence** = how strongly current evidence supports the hypothesis (High / Medium / Low).
- **Time horizon** = when a small team could realistically test commercial demand.
- **Arena implication** = what to build or avoid if the hypothesis is true.

---

## H1. AI shifts value from production to assurance, review, and evidence

**Claim.** As AI generates more code, documents, designs, and clinical/administrative drafts, the scarce work becomes checking correctness, assembling evidence, and proving compliance.

**Supporting evidence.**
- Stack Overflow 2025: 66% of developers frustrated by "almost right" AI code; 45% say debugging AI code takes longer [1](https://survey.stackoverflow.co/2025).
- Veracode 2025: 45% of AI code samples failed security tests [1](https://www.veracode.com/blog/genai-code-security-report).
- CDT 2025: 57% of special education teachers used AI for IEP/504 work; 15% fully delegate without review [1](https://cdt.org/wp-content/uploads/2025/10/FINAL-CDT-2025-Hand-in-Hand-Polling-100225-accessible.pdf).
- LangChain 2026: quality is the top barrier to agent adoption (32%); only 52% use offline evals [1](https://www.langchain.com/state-of-agent-engineering).

**Counter-evidence.** Incumbents may bundle assurance into existing platforms (GitHub, EHRs, PMS, IEP systems). Buyers may not pay separately for "checking."

**Confidence / horizon.** High / 0–12 months.

**Arena implication.** Prioritize O03 (AI-built app release audit), O06 (agent eval harness), O05 (prior-auth evidence), O12 (IEP compliance). Avoid generic generation tools.

**Validation test.** Sell a paid audit/report to 10 buyers before building automation. Kill if they only want free scans.

---

## H2. Individuals generating their own software creates a maintenance and security gap

**Claim.** Non-expert builders using Lovable, Bolt, Replit, Cursor, and similar tools will ship apps that need release gates, security checks, dependency updates, and incident response.

**Supporting evidence.**
- Menlo 2025: enterprise genAI spend $37B; coding is a killer use case ($4B) [1](https://menlovc.com/perspective/2025-the-state-of-generative-ai-in-the-enterprise/).
- Veracode 2025: AI-generated code frequently fails security tests [1](https://www.veracode.com/blog/genai-code-security-report).
- Snyk and CodeRabbit already price low-cost security/review tools, proving a paid category exists [1](https://snyk.io/plans/) [1](https://www.coderabbit.ai/pricing).

**Counter-evidence.** App builders may internalize checks; individual builders may have near-zero willingness to pay; agencies may prefer manual QA.

**Confidence / horizon.** Medium / 0–18 months.

**Arena implication.** O03 should target agencies and startups shipping client apps, not hobbyists. Package as "release readiness," not "AI code scanner."

**Validation test.** Offer a $500–$2,000 release audit to 20 AI-native agencies. Kill if conversion <10% or if buyers demand unlimited rescans at consumer pricing.

---

## H3. Low-AI-adoption industries are not automatically good targets

**Claim.** Industries with low AI adoption (construction, water utilities, agriculture, veterinary) have real pain, but adoption barriers are structural: skills, data quality, integrations, budgets, and liability.

**Supporting evidence.**
- RICS 2025: 45% of construction organizations use no AI; 46% cite skills gaps, 37% integration, 30% data quality [1](https://www.rics.org/news-insights/artificial-intelligence-in-construction-report).
- Purdue/CropLife 2025: farm income is the top barrier to precision-ag adoption; data-analysis services are unprofitable for many dealers [1](https://ag.purdue.edu/idaas/_docs/croplife-purdue-precision-dealer-full-report-2025.pdf).
- Peer-reviewed 2026 study: precision-ag dealers consistently overestimate future adoption across 21 survey waves [3](https://onlinelibrary.wiley.com/doi/10.1002/agr.70085).
- CRS: ~91% of ~50,000 community water systems serve ≤10,000 people, implying small staff/budgets [1](https://www.congress.gov/crs-product/R47315).

**Counter-evidence.** Regulatory deadlines and labor shortages can force adoption even in low-maturity sectors.

**Confidence / horizon.** High / 12–36 months.

**Arena implication.** Enter low-adoption sectors through compliance/evidence workflows with human review, not "AI transformation" platforms. O04, O14, O16 are plausible but slower.

**Validation test.** Require a paid pilot with a named operator and a measurable deadline before building.

---

## H4. Regulatory deadlines create temporary, high-urgency software markets

**Claim.** Deadlines convert "nice to have" automation into budgeted projects.

**Supporting evidence.**
- CMS-0057-F: impacted payer prior-auth APIs primarily due Jan 1 2027 [1](https://www.cms.gov/newsroom/press-releases/cms-finalizes-rule-expand-access-health-information-improve-prior-authorization-process).
- ADA Title II web rule: compliance extended to Apr 26 2027 (population ≥50,000) and Apr 26 2028 (smaller entities/special districts) [1](https://www.ada.gov/resources/web-rule-first-steps/).
- FDA food traceability: enforcement delayed to Jul 20 2028 [2](https://www.federalregister.gov/documents/2026/05/28/2026-10603/challenges-and-solutions-in-lot-level-food-traceability-public-meeting-and-request-for-comments).
- CBP de minimis suspension effective Aug 29 2025; statutory repeal Jul 1 2027 [3](https://www.cbp.gov/sites/default/files/2026-07/260708_bulletin_vol_60_no_18.pdf).

**Counter-evidence.** Deadlines slip; large vendors capture compliance budgets; small buyers wait for free government tools.

**Confidence / horizon.** High / 0–24 months.

**Arena implication.** Build deadline-driven wedges: O05 (prior-auth API readiness), O16 (water compliance), O07 (duty-aware returns), and a possible ADA Title II accessibility evidence tool for local governments (not ranked in top 16 due to crowded audit market).

**Validation test.** Confirm the buyer has a budget line and a named deadline owner. Kill if the deadline is repeatedly extended without enforcement.

---

## H5. Money-recovery workflows beat productivity workflows

**Claim.** Products that recover lost revenue (detention, unpaid invoices, returns fraud, missed estimates) are easier to sell than products that save abstract time.

**Supporting evidence.**
- ATRI: $15.1B detention cost in 2023; <50% of detention invoices paid [1](https://truckingresearch.org/2024/09/new-research-documents-substantial-financial-and-safety-impacts-from-truck-driver-detention/).
- Intuit QuickBooks 2025: 56% of small businesses owed money; average $17,500 [2](https://www.cnbc.com/select/how-to-paid-faster-small-business/).
- Radial 2025: 44% cite fraud/abuse as top returns pain; 91% of apparel refunds before inspection [1](https://www.radial.com/wp-content/uploads/2025/10/State-of-Returns_Report_2025_Final.pdf).
- Invoca 2026: home services answer only 52% of calls by a person; 45% of leads convert on the call [1](https://www.invoca.com/reports/the-invoca-home-services-lead-conversion-benchmarks-report-2026).

**Counter-evidence.** Recovery rates may be low; disputes damage relationships; success-fee models attract low-quality customers.

**Confidence / horizon.** High / 0–12 months.

**Arena implication.** O02, O01, O07, O08 should lead with recovered dollars, not "AI efficiency."

**Validation test.** Run a manual recovery pilot and measure collected cash within 60 days. Kill if recovery <20% of claimed leakage.

---

## H6. Vertical AI agencies need industrialized QA, not more agents

**Claim.** Agencies building agents for clients will need repeatable eval suites, regression tests, and client-facing reliability reports.

**Supporting evidence.**
- LangChain 2026: 57% have agents in production; 89% use observability but only 52% offline evals and 37% online evals [1](https://www.langchain.com/state-of-agent-engineering).
- Menlo 2025: 76% of enterprise AI solutions are purchased, implying a large builder/integrator ecosystem [1](https://menlovc.com/perspective/2025-the-state-of-generative-ai-in-the-enterprise/).

**Counter-evidence.** LangSmith, Braintrust, Langfuse, and cloud providers already cover much of this; agencies may build internal scripts.

**Confidence / horizon.** Medium / 0–18 months.

**Arena implication.** O06 should be vertical-specific (e.g., healthcare admin agents, legal intake agents) rather than a generic eval platform.

**Validation test.** Sell eval-suite setup as a service to 5 agencies; productize only if they renew monthly.

---

## H7. Creator economy growth creates ops/rights/payment infrastructure demand

**Claim.** As creator ad spend grows, managers and agencies need campaign operations, usage-rights tracking, and payment reconciliation more than another editing tool.

**Supporting evidence.**
- IAB 2025: U.S. creator ad spend $37.1B, +26%; measurement/standardization gaps [2](https://www.iab.com/wp-content/uploads/2025/11/IAB_Creator_Ad_Spend_and_Strategy_Report_2025.pdf).
- Adobe 2025: 86% of creators use creative genAI, implying output volume is rising [1](https://news.adobe.com/news/2025/10/adobe-max-2025-creators-survey).

**Counter-evidence.** CreatorIQ/GRIN/Lumanu already cover enterprise ops; small creators use spreadsheets and free tools; platform APIs are fragile.

**Confidence / horizon.** Medium / 6–24 months.

**Arena implication.** O10 targets talent managers and mid-size agencies, not individual creators.

**Validation test.** Reconcile 10 real campaigns manually; measure hours saved and payment disputes resolved.

---

## H8. Marketplaces become agent-readable, raising catalog compliance stakes

**Claim.** Agentic commerce and multichannel selling increase the value of clean, compliant, structured product data.

**Supporting evidence.**
- Mirakl 2026 Seller Report: median onboarding 28 days; Catalog Transformer users generate 88% higher GMV (vendor claim) [1](https://www.mirakl.com/blog/the-marketplace-revolution-key-insights-from-our-2026-seller-report).
- Mirakl 2025 results: $14.6B platform GMV, +31% [1](https://www.mirakl.com/news/mirakl-momentum-2025-key-results-launch-mirakl-nexus-agentic-commerce/).

**Counter-evidence.** Mirakl and PIM vendors ship native AI; operators may not pay a third party; GMV lift is correlational.

**Confidence / horizon.** Medium / 6–24 months.

**Arena implication.** O13 should sell to marketplace operators as onboarding/compliance infrastructure, not to individual sellers as a feed tool.

**Validation test.** Run a catalog cleanup pilot for one operator; measure onboarding time and rejection rate.

---

## H9. Caregiving demand grows, but consumer apps remain hard to monetize

**Claim.** The caregiver population is large and growing, but direct consumer subscription is weak; employers, payers, and agencies are more plausible payers.

**Supporting evidence.**
- AARP/NAC 2025: 63M U.S. caregivers, +20M since 2015; complex medical tasks common; training gaps [1](https://www.aarp.org/press/releases/2025-07-24-new-report-reveals-crisis-point-for-americas-63-million-family-caregivers.html).
- Many competing apps are free or low-cost: Caring Village official pricing is Free / $14.99 / $24.99 per month [1](https://caringvillage.com/pricing/).

**Counter-evidence.** Employer benefits and Medicare Advantage supplemental benefits could fund coordination tools.

**Confidence / horizon.** Medium / 12–36 months.

**Arena implication.** O15 is B2B2C only. Do not build a consumer caregiving app first.

**Validation test.** Secure one employer/payer/agency design partner with a paid pilot before product investment.

---

## H10. Some AI-era categories will become commodities or obsolete

**Claim.** Generic prompt wrappers, basic AI writing/design tools, simple meeting summarizers, and undifferentiated chatbots will be bundled into suites or displaced by platform-native features.

**Supporting evidence.**
- Microsoft/Google/Adobe are bundling AI into productivity and creative suites (WTI 2025; Adobe Creators’ Toolkit) [1](https://www.microsoft.com/en-us/worklab/work-trend-index/2025-the-year-the-frontier-firm-is-born) [1](https://news.adobe.com/news/2025/10/adobe-max-2025-creators-survey).
- Jobber/Housecall Pro already ship AI receptionist features [1](https://www.getjobber.com/pricing/) [1](https://www.housecallpro.com/pricing/).
- GDC 2025: 30% of developers view genAI negatively, suggesting trust/quality limits in creative production [1](https://www.gamesradar.com/games/one-in-10-game-developers-were-laid-off-in-the-past-year-gdc-survey-of-3-000-devs-finds-we-set-impossible-goals-and-then-fire-everyone-if-they-prove-to-be-impossible/).

**Counter-evidence.** Niche vertical wrappers with proprietary data/workflows can survive.

**Confidence / horizon.** High / already happening.

**Arena implication.** Avoid generic productivity, generic creator editing, and generic chatbots. Prefer evidence, compliance, recovery, and assurance.

---

## H11. New AI-era services emerge around trust, provenance, and accountability

**Claim.** New service categories will form around AI output: release audits, agent evals, model-risk evidence, content provenance, rights management, and compliance packets.

**Supporting evidence.**
- Veracode/Stack Overflow show code trust gaps [1](https://www.veracode.com/blog/genai-code-security-report) [1](https://survey.stackoverflow.co/2025).
- LangChain shows eval/observability gaps [1](https://www.langchain.com/state-of-agent-engineering).
- IAB shows creator measurement/rights gaps [2](https://www.iab.com/wp-content/uploads/2025/11/IAB_Creator_Ad_Spend_and_Strategy_Report_2025.pdf).
- CDT shows IEP privacy/oversight gaps [1](https://cdt.org/wp-content/uploads/2025/10/FINAL-CDT-2025-Hand-in-Hand-Polling-100225-accessible.pdf).

**Counter-evidence.** Standards may consolidate quickly; buyers may treat assurance as a feature, not a service.

**Confidence / horizon.** Medium-high / 0–24 months.

**Arena implication.** Productize services first (audits, pilots, reports), then automate repeatable steps.

---

## H12. Small water utilities and local governments become compliance-software markets

**Claim.** Small public entities face rising reporting/accessibility obligations but lack staff, creating demand for narrow compliance tools sold through associations.

**Supporting evidence.**
- EPA DWINSA: $625B 20-year drinking-water need [1](https://www.epa.gov/dwsrf/epas-7th-drinking-water-infrastructure-needs-survey-and-assessment).
- CRS: ~50,000 community water systems, ~91% small [1](https://www.congress.gov/crs-product/R47315).
- ADA Title II deadlines: Apr 2027 / Apr 2028 [1](https://www.ada.gov/resources/web-rule-first-steps/).
- Waterly prices by flow; Samples add-on <$800/yr to 40% of Rounds, showing low but real budgets [1](https://waterly.com/hot-sauce/).

**Counter-evidence.** Free state tools (e.g., iWriter), consultants, and very low budgets limit ACV.

**Confidence / horizon.** Medium / 12–36 months.

**Arena implication.** O16 is a slow, association-led play. Do not expect venture-scale growth quickly.

---

## Ranked hypothesis portfolio

| Priority | Hypotheses | Why |
|---:|---|---|
| 1 | H1, H5 | Assurance + money recovery have the clearest near-term ROI. |
| 2 | H4, H6 | Deadlines and agent QA create urgent, testable demand. |
| 3 | H2, H7, H8 | Emerging but commercially plausible with the right buyer. |
| 4 | H3, H9, H12 | Real need, slower adoption, weaker monetization. |
| 5 | H10, H11 | Strategic guardrails: avoid commodities; productize trust services. |

## What would change our mind

- If AI builders ship reliable native release gates, O03 weakens.
- If CMS deadlines slip again or payers block third-party evidence tools, O05 weakens.
- If detention recovery rates stay below 20%, O02 weakens.
- If accounting incumbents bundle CAS evidence chasing at low cost, O01 weakens.
- If creator platforms standardize rights/payment APIs, O10 weakens.
- If employers/payers refuse to fund caregiving coordination, O15 should be killed.
