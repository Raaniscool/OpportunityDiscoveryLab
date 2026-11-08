# Market Solutions: follow-up investigation

Research snapshot: 8 November 2026. Public-source investigation only; no contact, prototype, account access, or client data. This note updates the earlier [prospect register](marketing_agency_prospect_research.md).

## Decision: keep as a discovery candidate, not a qualified software lead

Market Solutions is a real Gothenburg media agency with a recurring reporting service and a documented historical reporting bottleneck. **We could not establish that its image/screenshot work is currently painful, expensive, or unmet.** The most relevant source is a vendor case study, not a recent buyer interview, and Whatagraph already supports image uploads. Downgrade confidence in a custom screenshot-attachment tool from the prior shortlist: **low**. Do not propose or build one on the available evidence.

## Findings and evidence

| What the source says | What it supports—and does not support |
|---|---|
| [Market Solutions' SEO Gothenburg page](https://marketsolutions.se/seo-goteborg/) says it delivers monthly reports on traffic, keyword positions, leads and conversions. Its [LinkedIn advertising page](https://marketsolutions.se/annonsera-pa-linkedin-b2b-marknadsforing/) also describes monthly reports with personal comments and recommendations. | Recurring reporting is a stated service for these offerings. It does not establish how many clients receive it, how it is produced, or how much time is wasted. These are agency marketing claims, not observation of delivery. |
| [Whatagraph's case study](https://whatagraph.com/case-studies/market-solutions) describes a 15-person agency serving 150+ clients at the time, formerly spending 5–10 hours producing a PowerPoint report. After switching to Whatagraph, it claims 30–70% less time per report, varying by source count. | Evidence of historical demand for reporting efficiency and adoption of an established tool; numbers are vendor-published, not independently verified, not current headcount or client count, and not a financial loss. The case provides no reliable event date for the measured workflow. |
| The same case says Karl-Viktor Jorkby believed more time could be saved if some reports did not need additional images and screenshots. It also describes personal commentary and scheduled delivery. | There was residual image-related work **when the case was made**. It does not quantify its duration, frequency, cost, client mix, current relevance, or which part was difficult. Commenting remains valuable human work, not automatically waste. |
| [Whatagraph's own product announcement](https://whatagraph.com/blog/articles/now-you-can-upload-images-to-your-reports) describes uploading JPG, PNG and GIF images via a report widget; [its help documentation](https://help.whatagraph.com/en/articles/6343689-widget-and-header-sizing) discusses image-widget sizing. | A basic image-upload feature already exists. The documents do not establish automatic capture, batch placement, compatibility with the agency's specific formats, or whether its current process is satisfactory. Simply offering upload is unlikely to be differentiated. |
| [Agency contact page](https://marketsolutions.se/en/contact-us/) lists Andreas Sandgren as CEO and co-founder and Karl-Viktor Jorkby as media planner. | Plausible future discovery roles: reporting practitioner first, CEO for budget only if there is a credible need. Purchasing authority and current roles should be reconfirmed; no one was contacted. |
| [Schibsted's 2025 partner article](https://schibstedforbusiness.se/mediebyran-om-schibsteds-nya-ai-losning-native-go-har-forenklat-allt/) quotes co-founder Jonathan Rodriguez McDonagh discussing use of its Native Go AI advertising solution. | Historical willingness to use a partner's AI-enabled tool, **not** evidence of a current need, budget, or willingness to buy AI-assisted custom development. The article is partner marketing. |

## Plausible workflow and rival solutions

**Hypothesis, not an observed present process:** a staff member obtains a client-approved campaign image, prepares/resizes it, adds it to a report via the existing widget, writes or reviews commentary, then approves delivery. The case does not say whether capture, editing, uploading, permissions, review, or some other step is the burden. We do not know whether automation of any step is possible or wanted.

1. **First alternative:** use Whatagraph's existing image widget, resizing guidance, saved templates and scheduled sharing. Determine whether those already solve the actual task.
2. **Second:** agree a repeatable shared-folder naming convention and use an existing presentation or document template. This can be cheaper and easier to maintain than a custom app.
3. **Only if a specific gap survives:** explore a small internal preflight checklist that identifies missing *approved* assets and prompts a human to review the correct report. A sanitized sample could be inspected manually first. Do not assume Whatagraph offers a writable API for this, or automate access to third-party accounts without permission. No implementation estimate is reliable before access and scope are known.

**Risk:** client asset confidentiality, mixing assets between clients, stale or misleading screenshots, unclear ownership, and continuing maintenance. A mandatory human approval step and minimum necessary access would be essential for any future pilot. AI can assist a developer, but cannot guarantee correct report content or compliance.

## Evidence needed before any proposal

- What is the last actual reporting cycle involving extra images? Which precise steps were manual and why?
- How many such reports per month, and how many minutes per report remain after their current Whatagraph setup? Is the work paid, billable or merely a small part of normal service?
- What has the existing image widget, templates, or vendor support already solved? What remains impossible or slow?
- Can they show a **redacted or synthetic** example and authorize its review? Are there restrictions on retaining or processing images?
- Who owns the workflow and signs off spending? Is there enough budget and interest for a small paid trial? What alternatives have they compared?
- What baseline, success criterion and maximum total pilot cost would make a change worthwhile, including their staff time and maintenance?

**Stop rule:** if the agency says the issue is resolved, infrequent, confidential in a way that prevents a safe test, or cheaper to handle in Whatagraph, close the opportunity. If they confirm a material recurring gap, assess configuring the existing platform first; only consider a bounded, paid, reversible pilot after explicit agreement and a realistic cost comparison. There is no evidence today to claim a particular amount of lost revenue, savings, or willingness to pay.
