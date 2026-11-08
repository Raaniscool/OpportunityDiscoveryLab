# Small Business Prospect Discovery — HVAC / Plumbing / Electrical (Independent Contractors)
**Arena Lab · Agent 03 (Competitor Analyst) · Prepared 2026-11-08 · Research only. No software built. No prospect contacted.**

**Assigned industry:** HVAC / Plumbing / Electrical contractors · **Scope:** 17 businesses investigated (16 full dossiers below, plus excluded cases — see §9) · **Shortlisted:** 5 prospects ranked · **Confidence key:** High = independent corroboration of problem; Medium = direct evidence but single-source/thin; Low = observed signal, unverified pain.

**Mission honesty statement (read first).** Every business below is real, publicly listed, and verifiable at the linked sources. Observed facts are separated from hypotheses throughout. A business having an outdated website does NOT mean it wants custom software — several prospects below are explicitly flagged as "out-of-box tools likely suffice" or "probably not a fit." Nothing here authorizes contacting any business.

---

## 1. Executive summary

The most consistent, evidence-backed failure pattern across 17 investigated HVAC/plumbing/electrical independents is **front-office collapse, not technical work**: missed calls, unreturned messages, slow quote follow-up, double-billing/AR errors, and review damage — all concentrated in shops with thin office staffing (often family-run, 1–8 field staff). This matches industry-wide data: Jobber's 2024 Home Service Industry Report says **61% of home service owners cite quoting/estimating as their biggest operational bottleneck**; ACCA reports HVAC companies lose **23–31% of quotes not followed up within 48 hours**; Jobber (2025) reports close rates fall from **~65% to under 30%** when quotes land after 48h; ACCA (2025) finds a **+18 percentage-point** lift in closes with a structured 72-hour follow-up sequence; technicians spend **2–3 hours/day on paperwork**.

**Strongest prospects (ranked in §6):**
1. **Keil Plumbing & Heating, Inc.** (Richmond, VA) — public employee testimony of office collapse + unresolved-complaint history + phone-only web presence. Custom AI back-office layer is low-complexity, high-value.
2. **FATman Plumbing Pro** (Waxhaw, NC) — demand exceeds capacity; 9–5 phone coverage; inconsistent listings; cheap to fix, easy to demo.
3. **Discount Mechanical Heating & Plumbing** (Anchorage, AK) — Yelp 2.3★ vs ServiceTitan already installed: failure is accountability/comms, not booking. Accountability layer on top of existing stack.
4. **New Life Contracting LLC** (Glen Allen, VA) — domain serving gambling content (observed 2026-11-08), unanswered BBB complaint, comms dead; conditional on confirming it is still operating. Highest pain, highest risk.
5. **Climate Heating & Cooling** (Gahanna, OH) — documented unreturned-calls complaint (BBB) and no visible post-job follow-through; plausible fit for review/QA automation, evidence thinner.

**Rejected after investigation (examples):** Fusion Plumbing (Yelp: CLOSED), Independent Heating & Air Denver (Yelp 1.0★ + permit/registration violations — integrity red flags), Service First Heating & Cooling (5.0★/154+ reviews — already well-tooled; weak fit), Airstream Services (strong ops + texted reminders already — they do the thing).

**First prospect to investigate: Keil Plumbing & Heating** (full rationale §7). Recommended entry offer: a scoped, measurable pilot (missed-call recovery + quote-follow-up + AR reminder automation), not a platform.

---

## 2. Methodology & source policy

- Sources: official websites, BBB complaint files, Indeed/Glassdoor employee reviews, Yelp/Google/Angi/Porch/localprobook/BuildZoom profiles, Yahoo Local (user-submitted review aggregates), local news. All accessed **2026-11-08** unless noted (full link list in §10, graded ● primary / ◐ corroborated secondary / ○ single source).
- **Verification caveats:** Yelp/Google ratings drift; BBB complaint counts lag; Indeed reviews are few and old (2022); one business's website now hosts unrelated third-party content (documented, not assumed malicious). Where data conflicts (e.g., Keil's "24/7 service" claims vs. posted Mon–Fri 8–4 hours), both are reported.
- Frequency estimates use (a) complaint timestamps, (b) platform response-time badges, (c) industry statistics; no invention of per-business volume. Where a number is an industry average, it is labeled as such.
- Financial consequences are framed as *mechanism* (e.g., unfollowed quotes → lost closes) not invented per-company dollar figures. Where a dollar figure appears in a complaint, it is quoted and attributed.
- **Nothing was built. No prospect has been contacted, emailed, called, or offered anything.**

---

## 3. Market context (why these shops, why now)

- **61%** of home service owners say quoting/estimating is their biggest bottleneck — Jobber 2024 Home Service Industry Report (via RaftLabs, Medium/Jun 2026) [M1]
- **23–31%** of HVAC quotes lost without 48h follow-up; structured 72-hour follow-up lifts close rates **+18 points** — ACCA (via ustechautomations, Jun 2026) [M2]
- Close rate **~65% → <30%** after 48h quote delay — Jobber 2025 (via ustechautomations) [M3]
- Technicians average **2–3 hrs/day** on quotes/invoices/notes; quoting in-office adds 6–24h to delivery (vs 0–2h automated) — RaftLabs (Nov 2025), ustechautomations benchmarks (Jun 2026) [M1][M2]
- HVAC $750K–$6M revenue band with 4–25 techs, 60–300 quotes/month is the standard "quote automation" ICP — ustechautomations [M2]
- No-show / no-callback patterns recur across BBB complaint files of the investigated majors (Air Pros LLC Hollywood FL; AirMaster HVAC Orlando FL; One Hour Heating & Air; Fast Response) — systemic across the industry, not one bad actor [M4–M7]

---

## 4. Researched businesses (16 full dossiers)

Format per dossier: **Evidence that it's small** → **Specific problem (evidence)** → **Frequency signal** → **Cost to business** → **Existing alternatives** → **What custom software could do** → **Complexity** → **Why they'd pay** → **Confidence**.

### R1. Keil Plumbing & Heating, Inc. — Richmond, VA ⭐SHORTLIST #1
- **Website:** https://www.keilservice.com · **Address:** 2507 Willard Rd, Richmond, VA 23294 · **Phone:** (804) 672-9180 (also listed (804) 525-9434)
- **Small-business evidence:** Single family location since 1930; self-described "fourth-generation, family-owned"; YellowPages lists staff hours Mon–Fri 8–4 (no published headcount; shop-size consistent with 3–12 staff — verify).
- **Specific problems (observed):**
  1. **Office staffing collapse / missed callbacks:** Indeed employee review (HVAC Service Coordinator role, **Apr 21, 2022**): *"This company is barely hanging on by a thread. They have no employees to run actual calls. The office manager is MIA most of the week and blames everything on everyone else."* Indeed company rating 3.0; one 5.0 review (2019) contradicts — flagged.
  2. **Billing/collections errors:** Chamber of Commerce listing (Feb 2024): *"After he left, I read the report… I paid them… Then months later they sent me an overdue bill for the invoice I already paid… Do not use this plumbing service, they are either incompetent or scammers"* (Michael P., Feb 2024).
  3. **No-show / callback failure:** AirConditioningProfessionals.com review (2018): *"They said they would be there the next day and would call 30 minutes before… I've never heard from them again"*; another (2018): *"$95 for doing nothing for 10 mins… front desk service is even more horrible. She just threatens you to either pay or bear the consequences."*
  4. **Digital presence is a static form:** keilservice.com contact page shows a generic web form with **no online booking, no quote calculator, no automated follow-up** (observed 2026-11-08); 24/7 emergency claim vs. posted Mon–Fri 8–4 hours (inconsistency, both shown on-site/yellowpages).
- **Frequency:** ≥3 independent public complaint events across 2018–2024 spanning phones, billing, scheduling; Indeed testimony describes structural (not incidental) office understaffing — "most of the week."
- **Consequence:** Lost/recoverable revenue (unbilled AR), warranty-job leakage, reputation drag (localprobook 4.1★/9; Indeed 3.0), and hours lost by the family to firefighting.
- **Existing alternatives:** Jobber (~$70–150/mo), Housecall Pro (~$60–180/mo), AnswerConnect/answering services (~$100–300/mo), NiceJob/Birdeye review automation (~$90–300/mo). **But:** the failure here is process discipline in a phone-first shop — off-the-shelf only works if a human runs the cadence; an AI-driven missed-call/AR/follow-up layer is materially different from a scheduler license.
- **Custom software proposal:** "Keil Back-Office Autopilot" — (a) missed-call text-back in 60s with job intake, (b) appointment confirmation/30-min ETA texts, (c) post-job QA text + photo receipt, (d) AR reminder cadence on overdue invoices (targets the Feb 2024 double-billing class of error: payment flag → suppress dunning), (e) review-request automation + negative-feedback intercept, (f) nightly AI summary to owner's phone (calls missed, quotes outstanding, AR aging).
- **Complexity:** **Low–Medium** (2–4 weeks to MVP; Twilio + payment/CRM export + simple DB; no ServiceTitan dependency confirmed yet — must verify current stack).
- **Why they'd pay:** Recovers staff hours the family can't hire for; directly addresses the two public-facing failure modes (callbacks, billing); $300–800/mo or $3k–6k build cost easily beats one lost $5k furnace job.
- **Confidence: HIGH** (three corroborating source types; quote-able evidence; low build risk).

### R2. FATman Plumbing Pro — Waxhaw, NC ⭐SHORTLIST #2
- **Website:** https://fatmanplumbingpro.com · **Address:** 3512 Providence Rd S, Suite B, Waxhaw, NC 28173 · **Phone:** (704) 550-8626 (site) — **Yelp lists (704) 256-1400 (inconsistent NAP across profiles — observed 2026-11-08)**
- **Small-business evidence:** One-owner shop since 2010 (owner Chris Lovick, plumbing since 1987); Charlotte Observer/Yahoo (Jan 2026) describes it as a "small Waxhaw-based plumbing company" with limited capacity. Hours posted 9–5 weekdays only.
- **Specific problems (observed):**
  1. **Demand exceeds capacity; overflow uncaptured:** Yahoo/CHARLOTTE (Jan 2026): *"the company is small, so it may not be able to fit new clients into the schedule as promptly."* A+ BBB, no complaints, but capacity ceiling is documented publicly.
  2. **After-hours/lead loss:** 9–5 hours posted; site shows an "ONLINE BOOKING" page (form-class, observed 2026-11-08) with no evidence of automated after-hours booking/answering; phone-first business where calls outside 9–5 get nothing.
  3. **Listing inconsistency:** Two different phone numbers (site/Facebook vs Yelp) and two different street addresses (3512 vs 3615 Providence Rd S across listings) — split-brain local SEO/NAP dilution; observed directly.
- **Frequency:** Every inbound call outside 9–5 and every overflow moment; likely daily during peak season; no volume data public (hypothesis — verify with owner).
- **Consequence:** Warm inbound leads lost to voicemail → permanent defection to the next Google result (this industry has zero brand loyalty in emergency plumbing).
- **Existing alternatives:** Housecall Pro/Jobber (booking pages), Goodcall/Slang/Rosie AI receptionists (~$50–150/mo), Google Business Profile messaging. All solve parts; none fix NAP fragmentation + follow-through + review autopilot together at this shop's price point.
- **Custom software proposal:** "Never-Miss-the-FATman" — AI phone answerer + SMS booking for after-hours/overflow; auto-syncs jobs to a simple shared calendar; post-job review request with bad-review intercept; NAP/listing monitor that flags divergent profiles weekly; one-page live dashboard (missed calls → booked jobs conversion).
- **Complexity:** **Low–Medium** (1–2 weeks; Twilio + GBP/Yelp APIs where available + simple DB).
- **Why they'd pay:** One captured emergency call ≈ one $150–$900 service job (industry-typical range; not this shop's disclosed pricing). Plausibly self-funding from week 2. Healthy business (A+ BBB) — pays from growth, not distress.
- **Confidence: MEDIUM** (pain evidence is structural inference + documented capacity + NAP inconsistency; no complaint file).

### R3. Discount Mechanical Heating & Plumbing — Anchorage, AK ⭐SHORTLIST #3
- **Website:** https://discountmechanical.net · **Address:** 500 W 41st Ave, Anchorage, AK 99503 · **Phone:** (888) 977-5031 · **Yelp: 2.3★ (45 reviews)** (updated Nov 2026)
- **Small-business evidence:** Family-owned since 2004; single Anchorage shop; veteran-owned; Yelp/YP indicate storefront + field crew; job ads/review volume imply single-digit-to-low-double-digit staff.
- **Specific problems (observed — extensive):**
  1. **Chronic no-shows / broken commitments:** YellowPages reviews: *"He was a no-show, no phone calls, nothing. I… scheduled me for an appointment two weeks later. Again, a no-show"* (heater repair, Holiday season, undated); *"half the time… 2 weeks now… the tech is not helpful and are slow at getting parts"* (undated); leadsmart.com mirrors a 2024 review: *"It's been 2 months to get the work even not be done… I couldn't communicate at all… they all had no callbacks even they promised to call back"* (Nik Shulgin, Aug 2024).
  2. **Unresolved inspection failures & correction loops:** Angi review (Deanna S., May 2025): boiler install failed initial municipal inspection; *"three phone calls with no response… installation failed… a third visit from their team to address the Municipality's concerns… no willingness to provide a partial refund… I can only hope no one else experiences what I have been through."*
  3. **Already pays for software that isn't fixing this:** Their site markup references **ServiceTitan "Scheduling Pro"** and they run online scheduler + instant-estimate journeys (observed 2026-11-08). Tooling ≠ outcome.
- **Frequency:** Dozens of negative reviews over a decade; two documented multi-visit municipal-correction loops; no-shows reported repeatedly across platforms (Yelp 2.3★ anchor is the tell).
- **Consequence:** Lost jobs, warranty/callback labor cost, reputation ceiling (2.3★ likely throttles new leads), municipal re-inspection costs, potential liability on failed inspections.
- **Existing alternatives:** Already on ServiceTitan → ServiceTitan "Field Pro"/marketing add-ons, NiceJob, Podium, Symvo AI QA platforms; the gap is enforcement/ownership of the loop, not more software licenses.
- **Custom software proposal:** "DM-Accountability" — (a) auto confirmation + 30-min ETA + en-route photo for every booked job; (b) customer-facing "tech on way / running late" one-tap updates; (c) post-job QA text within 10 min with auto-escalation to owner on keywords (leak, inspection failed, unhappy, refund); (d) overdue-invoice nudge with pay-link; (e) monthly "promise board" to owner: commitments made vs kept. Integrates with ServiceTitan read APIs or, later, standalone.
- **Complexity:** **Medium** (ServiceTitan API credentialing is the gating item; 3–5 weeks incl. pilot on 20 jobs).
- **Why they'd pay:** 2.3★ is an active revenue throttle; the owner has already paid for tooling that underperforms — a fix-it layer that demonstrably moves rating by even 0.5★ pays for itself in lead volume. Willingness signaled by ServiceTitan spend.
- **Confidence: HIGH** on evidence; **MEDIUM** on product fit (stack integration risk; possible "software fatigue" objection).

### R4. New Life Contracting LLC — Glen Allen/Aylett, VA ⭐SHORTLIST #4 (conditional)
- **Website:** www.newlifecontracting.org → **as of 2026-11-08 the domain serves an unrelated third-party gambling/casino page (Azerbaijani "1win" content)** — observed directly by this agent; ZoomInfo's cached/profile copy still lists the site (Feb 2026). Treat as abandoned/hijacked, not as proof of malice. · **Address:** 64 Willow Oak Ct, Aylett, VA 23009 · **Phone:** (804) 426-9837 · **Owner: Colby Jones**
- **Small-business evidence:** BBB profile: file opened 2015 (or business ~2009–2010 per BBB/Porch discrepancy — report both), "Years in Business: 16"; ZoomInfo revenue **<$5M**; Porch 4.65–4.7★ (22 reviews); single-location, owner-operator HVAC, Aylett VA (rural).
- **Specific problems (observed):**
  1. **Customer-comms collapse + disputed $3,950 refund:** BBB complaint (filed **Aug 22, 2024**, unanswered as of BBB page snapshot): *"I contacted the New Life Contracting multiple times over the past few months being given explanations that they were busy on other projects and that they would get to me when they were done. Over the last 2 months the contractor has completely stopped communicating with me… After multiple requests to have my money returned… next step is to visit my local police station… $3,950.00… grand larceny"* (complainant name redacted by BBB; company failed to respond → BBB rating **C+**).
  2. **Dead web presence:** official domain replaced by gambling content (see above) — any referral link now routes customers into a casino.
  3. **Reputation/knowledge asymmetry:** Porch 4.7★ (22) says the work itself is often praised — the failure is *after-sales communication*, the exact wedge.
- **Frequency:** At minimum one documented dispute spiral (2024) + visible domain death; unknown number of silent quote requests lost since site died — unverifiable.
- **Consequence:** Direct revenue loss (unreturned deposits/quotes), legal/BBB exposure, permanent referral-network damage, credibility collapse from a single shared link.
- **Existing alternatives:** A $300 website template fixes the site; the *systemic* part (intake triage + 72h follow-up + escalation to owner) is what Jobber/HCP don't do out of the box at this rural scale/price point.
- **Custom software proposal:** "NLC Ressurrection" — emergency domain/site rebuild (hygiene + credibility; 3–5 days), then AI intake triage (text/email/web form → classified: emergency / quote / warranty / billing), automatic 72-hour quote-follow-up cadence (ACCA +18pt stat anchor), weekly owner digest (silent customers needing callback), review-request autopilot.
- **Complexity:** **Low for site rebuild (3–5 days); Medium for triage automation (2–4 weeks)**.
- **Why they'd pay:** An abandoned domain + unanswered complaint is an existential, owner-visible wound; the cheapest credible fix ($1.5k–4k) plus a follow-up autopilot has obvious ROI (one $4k recovered dispute = paid multiple times over).
- **Conditions & risks:** **Verify operational status first** — unanswered complaints + dead site may indicate closure/distress/legal exposure; do NOT pitch until owner is confirmed reachable and willing (see §8 questions). If distressed, walk away — no product fits a business in dispute escalation.
- **Confidence: MEDIUM-HIGH** on observed facts; **LOW** on viability until verified.

### R5. Climate Heating & Cooling — Gahanna (Columbus metro), OH ⭐SHORTLIST #5
- **Website:** https://climatecolumbus.com · **Address:** 1509 Blatt Blvd, Gahanna, OH 43230 · **Phone:** (614) 852-7336 · **Email:** climatehandc@gmail.com · **Owner: Ken Perry (Nextdoor, Jul 2023)**
- **Small-business evidence:** Self-described "family-owned… 45 years"; Nextdoor/FB traces consistent with single-location shop; hvacservice.io and lookn4 list it with **no aggregated review volume** (very small or lightly-reviewed); BBB profile (Hilliard file, OH) exists under same name.
- **Specific problems (observed):**
  1. **Unreturned calls + no paperwork after job:** BBB complaint (most recent on file; older than 12 months): an elderly homeowner with a warranty-covered AC repair — *"They do not take my calls and they don't return any messages… I still do not have any idea how to make the AC work… He said he would send operation instructions out in the mail right away… That was weeks ago, I have received nothing."* (paperwork promised, never sent). **1 complaint closed in last 3 years; 0 in last 12 months** (BBB, 2026 snapshot).
  2. **Post-job documentation failure:** No evidence of digital service records/warranty documentation workflow — manual, phone-and-paper operation implied by the complaint's nature (report delivered as "foam-looking stuff," no booklet).
- **Frequency:** Thin complaint signal (single documented case) — **LOW-MED confidence on recurrence**; pattern (no follow-through, no documentation) is structurally consistent with very small manual shops.
- **Consequence:** Warranty callbacks, safety risk (undocumented work), elderly-customer harm (reputational/legal exposure in OH), lost repeat/referral revenue.
- **Existing alternatives:** Jobber/HCP service-report PDFs; housecall-style "tech report" add-ons; photo-to-invoice flows; paper backup templates from suppliers.
- **Custom software proposal:** "ClimateCare Closeout" — post-job auto-document: tech fills 5 fields + photos → system generates customer PDF + warranty card + next-service reminder (6/12/24-mo), texts/emails automatically, and logs "paperwork outstanding" nag to owner. Optional: no-call-no-show guard (appointment confirmation escalation).
- **Complexity:** **Low** (1–2 weeks; template PDF + Twilio + simple queue UI).
- **Why they'd pay:** Directly ends the exact failure described; warranty callbacks cost real labor; ~$200–400/mo or $2–4k build — affordable at 45-year family scale.
- **Confidence: LOW-MEDIUM** (one documented complaint; thin public volume; owner may simply need discipline, not software — must confirm in discovery).

### R6. Right Way Heating and Cooling — Reynoldsburg, OH
- **Website:** http://www.rightwayhvac.com · **Address:** 2933 Donnylane Blvd, Columbus, OH 43235 (also listed 28 Klema Dr N, Reynoldsburg 43068) · **Phone:** (614) 751-0193
- **Small-business evidence:** Family-owned per site; ~118–417 reviews across platforms (customerlobby 5.0/118; hvacservice.io 5.0/417) — **this is a larger small-shop (maybe 10–25 staff), likely with dispatch software; treat as mature operator.**
- **Specific problems (observed):** Front-office responsiveness, not delivery: CustomerLobby review (**Chris D., Columbus, 08/22/2017**): *"The time it took to get a response to about 3 calls that were placed to them seemed too long… Getting something scheduled so the customer knows that it is being worked on at least is not a big ask… need some work on the front end."* (Service itself rated positively once onsite.)
- **Frequency:** Single documented complaint; high review volume dilutes it — likely episodic, seasonal-peak-driven.
- **Consequence:** Lost scheduling conversion during peaks; minor reputation drag vs 5.0 average.
- **Existing alternatives:** They almost certainly already use field-service software at this volume; solution is tuning + AI call-answer/triage, not new systems.
- **Custom software proposal:** AI front-desk triage (classify call: emergency/quote/warranty; auto-book or priority-route) + missed-call recovery text within 2 minutes. **But:** likely already solvable inside their stack — validate before pitching custom.
- **Complexity:** Low (if API access available) / Medium otherwise.
- **Why they'd pay:** Marginal — pitch only if discovery reveals unmet front-end pain; otherwise Housecall Pro/Jobber they already may have.
- **Confidence: MEDIUM (evidence exists); LOW (fit for custom build).**

### R7. Inspired Heating & Cooling, Electric, Roofing, Repair LLC — Columbus, OH
- **Website:** https://inspiredheatingandcooling.com · **Site exhibits:** personal homepage ("I" language), Birdeye 5.0/19–20 — "Every review features Steven by name… one-technician operation."
- **Address:** 1425 Community Park Dr, Columbus, OH 43229 · **Owner: Steven** (full surname not published — verify) · **Phone:** see site.
- **Specific problems:** **No complaint evidence found** (opposite). Observed structural risk: **single-technician shop where owner is the bottleneck** — customers praise "same day / within the hour" response; demand exceeds one person's capacity; owner cannot scale or take a day off without service stopping (Inference labeled as such).
- **Frequency:** Daily capacity ceiling (inference).
- **Consequence:** Lost overflow jobs; burnout; zero backup coverage; no documentation system (invoices/quotes hand-built — hypothesis).
- **Existing alternatives:** Jobber/HCP scheduling + payments; Google Calendar + Square; answering services.
- **Custom software proposal:** Owner-levelling toolkit: AI intake answering + auto-quote generation from photos customer texts in (he already accepts photo quotes per reviews) + customer self-serve scheduling + review automation. Not a pain-driven sale; a growth-enablement sale.
- **Complexity:** Low.
- **Why they'd pay:** If he wants to grow without hiring an office manager, yes; if he's content solo, no.
- **Confidence: LOW** (no pain evidence; pitch only after discovery).

### R8. Mr. Tech Live 24/7 — Columbus, OH
- **Website:** https://www.mrtechlive.com · **Address:** 1500 W Broad St, Columbus, OH 43222 · **Owner: Abdullah Rashid** (Tech: Faraz) · **Phone:** see site · **5.0/4** (voolt/hvacservice.io)
- **Evidence:** Tiny one-truck operation; 24/7 emergency positioning; zero complaint evidence; capacity-constrained by construction.
- **Fit:** Same class as R7 — growth-enablement, not pain-relief. Low priority.
- **Confidence: LOW.**

### R9. Plumb Line Plumbing Service — Richmond, VA
- **Phone:** (804) 909-3589 · **Established:** 2015 · **Structure:** husband-and-wife; owner **Kevin** (master plumber); women-owned (Yelp profile) · **Yelp: 4.6★ (12 reviews)**; 26 photos.
- **Address:** Richmond VA 23222 · **Hours:** Mon–Fri 7:30–5:00, closed weekends (Yelp, updated Jul 2026) · **Website:** none found.
- **Specific problems (observed/inferred):** Phone-first shop, no website, no online booking; **pain evidence absent** (reviews: "he'll provide a quote on the spot" praise; "Kevin was held up on another job but let me know promptly").
- **Consequence / alternatives / proposal:** Same pattern as R7/R8 — owner-capacity and no digital intake; $200–500/mo potential tooling (or $2–3k custom) but willingness unverified.
- **Confidence: LOW.**

### R10. Lamb's Plumbing — Richmond, VA
- **Website:** https://www.lambsplumbingva.com · **Owner: Lamb** (full name not published) · **20+ years**, residential + commercial · Central VA service area.
- **Evidence:** Site reviews page shows strong recent wins (water-main replacement pre-hospital-birth save; bathroom leak diagnosis). **Counter-evidence:** BuildZoom (Dec 14, 2016): **1★ — "over charges, brings family into work with him, always shows up late… damaged my new dishwasher… didn't show up to court."** BuildZoom score 89/30th percentile (131k VA contractors).
- **Specific problems:** Lateness and post-dispute follow-through (2016); no current automation/booking evidence on site ("Schedule Now" CTA exists but is form-class).
- **Frequency:** Unquantifiable now; 2016 event is stale; treat as watch item.
- **Alternatives:** Jobber "late vs on-time" reporting + automated ETA texts (cheap, built-in if they adopt Jobber — custom build NOT justified).
- **Confidence: LOW** (stale evidence; healthy-looking site).

### R11. Lyons Plumbing & Heating — Richmond, VA
- **Address:** 3700 Harvette Dr, Richmond, VA 23237 · **~41 years in business** (SuperPages/YP listings) · **Yelp 1.0★ (2012, single review)**; SuperPages 4.5★ (3–4 reviews).
- **Specific problems (dated):** 2007 review (SuperPages, "thebirdman7", 06/14/07): *"charged $135 first hour, $95 additional hour… $40 show-up fee… I was also charged for drive time from the previous job… They arrived about an hour late… because they added a later job before my scheduled time but never phoned to let me know."* — **fee opacity + scheduling opacity + no delay notification** — classic phone-dispatch failure.
- **Frequency:** Historical (2007–2012); no evidence of current problems.
- **Alternatives:** Dispatch transparency tooling (any FSM), plain text ETA.
- **Confidence: LOW** (too stale to act on).

### R12. Agape Plumbing — Richmond, VA
- **Address:** 656 Elgin Terrace, Richmond, VA 23225 · **Owner: Eugene** (~15 yrs exp; solo) · **Angi (2017–2018):** 5★×5 ("called us back within minutes Friday evening and came to see us Saturday at 8am") · **Porch (2026):** 4.7★-class listing, 15 reviews · **Website:** none found.
- **Problems:** None observed (owner-responsive solo shop). Peak-time capture is the only conceivable pain.
- **Alternatives:** Answering service; nothing else needed.
- **Confidence: LOW.**

### R13. Circuit Pros — Nashville, TN (Electrical)
- **Listing:** Yelp/Angi only (no owned site surfaced) · **Phone:** see Yelp · **Owner: Chris** (master electrician) · **Yelp: 5.0★ (5–7 reviews)** · "Family-owned," "free estimates," "Chris fit us in within hours" (smoke-alarm review).
- **Problems:** None observed; hand-to-mouth intake (Yelp-quote requests) typical of micro-shops; no website = no owned lead channel (observation, not judged deficit).
- **Custom pitch:** Website + instant-quote widget only if owner wants it. **Do not pitch automation.**
- **Confidence: LOW.**

### R14. C & C Electric — Nashville, TN
- **Address:** 877 7 Oaks Blvd, Nashville, TN · **Yelp: 4.6★ (11 reviews)** · Yelp badge: "10 mins response time," "Excellent responses," 7+ "locals recently requested a quote."
- **Problems:** None observed; response engine is owner-centric; capacity unknown.
- **Confidence: LOW.**

### R15. Apollo Electric — Nashville / Clarksville, TN
- **Owner: John (Beazley)** · **Yelp: 5.0★ (3)**; Angi (Mar 2025): kitchen lights + plugs + cove heater praised; Yelp response "20–40 mins."
- **Problems:** None observed; extreme responsiveness implies owner bottleneck (inference).
- **Confidence: LOW.**

### R16. Airstream Services — Nashville, TN (Electrical/HVAC/Plumbing)
- **Website:** https://airstreamteam.com · **Address:** 3333 Mayoral Ct, Nashville, TN · **11 years; family-owned** · **Yelp 4.2–4.3★ (67–75 reviews)**; Google 5.0 (poyst aggregation, "verified").
- **Evidence:** Customers explicitly praise proactive SMS updates: *"I like how they keep in contact with me by texting me to remind me and let me know when they have arrived."* — **they already do automated-ish customer comms** (may be manual or tooling; verify).
- **Problems:** One app-connect complaint (smart thermostat setup confusion, Kylie White, 07/29/25 — not an Airstream failure); all other reviews strongly positive; they underbid home-warranty contractors on diagnosis (Parker saved customer $4,200 false replacement) — quality/ops, not software gap.
- **Custom pitch:** None recommended (they're the benchmark shop). **Excluded from shortlist.**
- **Confidence: LOW (fit) / HIGH (well-run).**

---

## 5. Researched and excluded (with reasons)

| Business | Location | Why excluded |
|---|---|---|
| **Fusion Plumbing** (Matt Bradbury) | Eagle River, AK | Yelp profile states **CLOSED** (updated May 2026). Cannot prospect a closed business. |
| **Independent Heating & Air** (Denver, CO 80218) | Yelp **1.0★ (5)** | Reviews allege unpermitted work & county registration failure: *"Didn't pull permit as contracted… advise us to manually turn on & off"*, *"Numerous no shows, no calls."* Pain evidence is real but the profile suggests compliance/integrity issues — **not a candidate**; do not enrich, do not pitch. |
| **Service First Heating & Cooling** (Circleville, OH) | servicefirstair.com | 5.0★/154–235 reviews; BuildZoom top ~1% ("top 99%" license tier); clearly instrumented; weak custom-software fit. |
| **Travis Crawford Heating Cooling & Plumbing** (Charlotte, NC) | Charlotte metro | 4.9★ Google/2,192 (Yelp 4.1★/69; 4 BBB complaints/3 yrs) — too large/too well-run for this brief. |
| **Air Pros LLC** (Hollywood, FL) | Hollywood FL | BBB complaint file shows systemic no-shows but company is **multi-market scaled** (not a single small owner shop) — out of scope. |
| **One Hour Heating & Air** (various) | Franchise | Franchise dispatch, not independent owner-operator. |
| **Osborne Plumbing And Drain** (Charlotte, NC since 1994) | Charlotte NC | Yelp **2.7★ (14)** — *"Not happy with our experience using this company. We spent several thousands on plumbing problems we…"* (quote truncated at source); Yelp lists response time between **3 hrs and 1 day** across categories; **no official website surfaced**; reputation severely damaged; distress-verification burden too high for a cold first approach — **document, do not pitch cold.** |

---

## 6. Shortlisted prospects — ranked by commercial potential

### 🥇 #1 — Keil Plumbing & Heating, Inc. (Richmond, VA)
**Best combination of acute evidence, affordability, and low build risk.**
- **Build:** "Keil Back-Office Autopilot" — missed-call text-back intake (60s), appointment confirmation + 30-min ETA, post-job QA intercept, **AR/overdue-invoice suppression logic** (flags paid invoices before dunning — directly targets the Feb 2024 double-billing incident), review-request autopilot with negative intercept, nightly owner digest.
- **Complexity:** Low–Medium · **Time to pilot:** 2–4 weeks · **Est. cost:** $3k–6k build, $300–600/mo support (estimate, not quoted).
- **Alternatives:** Jobber/Housecall Pro need a disciplined human driver; they have none. Answering services lack AR context. This is the wedge.
- **Why they'd pay:** It fixes the two named public failures (callbacks, billing); one retained $5k furnace job or one avoided legal threat covers the year; family-owned since 1930 has means and motive.
- **Main risk:** Owner exhaustion; "we already pay for software" fatigue (verify in discovery).

### 🥈 #2 — FATman Plumbing Pro (Waxhaw, NC)
**Healthiest business on the list with an obvious, cheap, demonstrable win.**
- **Build:** AI answering + after-hours SMS booking; review-request autopilot; NAP/listing monitor + duplicate-listing cleanup report; simple job funnel dashboard.
- **Complexity:** Low–Medium · **Time:** 1–2 weeks · **Est. cost:** $2k–4k, $200–400/mo (estimate).
- **Alternatives:** Rosie/Goodcall AI receptionists (~$50–150/mo) — cheaper, but no listings monitor/review layer and no custom funnel; Jobber excess for one man.
- **Why they'd pay:** Overflow + 9–5 coverage loss is measurable (every unanswered call = lost ticket); healthy cash flow; wants growth without hiring office staff.
- **Main risk:** "Phones work fine" — answer with overflow math in discovery.

### 🥉 #3 — Discount Mechanical Heating & Plumbing (Anchorage, AK)
**Biggest visible brand bleed (2.3★, 45 Yelp) with ServiceTitan already installed — the fix is accountability, not licenses.**
- **Build:** ETA/confirmation/en-route automation; 10-min post-job QA with owner escalation; promise-vs-kept tracker; AR pay-link nudges; reputation repair loop (review intercept).
- **Complexity:** Medium (ServiceTitan integration gating) · **Time:** 3–5 weeks · **Est. cost:** $4k–8k, $400–800/mo (estimate).
- **Alternatives:** ServiceTitan add-ons/NiceJob/Symvo — broader but heavier; or a $150/mo human QA call-center (unscalable, no data).
- **Why they'd pay:** Active revenue throttle; municipal re-inspection cost avoidance; owner already spends software money (Sunk-cost reverse: he's bought the stack and it's failing him — a fix-it layer is an easy argument).
- **Main risk:** Integration access + owner cynicism ("another vendor"); pilot on 10 jobs to prove lift.

### #4 — New Life Contracting LLC (Glen Allen/Aylett, VA) — **conditional**
**Highest pain, lowest verification — proceed only after operational-status check.**
- **Build:** (Phase 0) Domain/site rebuild + removal of gambling content exposure; (Phase 1) AI intake triage + 72-hour quote-follow-up cadence + owner escalation digest; (Phase 2) review autopilot.
- **Complexity:** Low (site) → Medium (triage) · **Time:** 3 days + 2–4 weeks · **Est. cost:** $1.5k–3k + $300–500/mo (estimate).
- **Why they'd pay:** Domain/casino exposure is existential for a referral-driven HVAC shop; $3,950 unresolved dispute signals both pain and willingness to resolve with structure.
- **Main risks:** **Verify he's operating and reachable first.** Possible distress/closure; BBB escalation pending; do not pitch into an active legal dispute.
- **Alternatives:** Any competent web designer + Jobber — but nobody will fix *follow-through* for him; that's the gap.

### #5 — Climate Heating & Cooling (Gahanna/Columbus, OH)
**Single documented elderly-customer failure; documentation/closeout automation is the exact counter-measure.**
- **Build:** "Closeout Pack": tech mobile checklist → auto PDF + warranty card + 6/12/24-mo service reminders; owner "paperwork outstanding" nag; optional appointment-confirmation escalation.
- **Complexity:** Low · **Time:** 1–2 weeks · **Est. cost:** $2k–4k, $150–300/mo (estimate).
- **Why they'd pay:** Directly kills the BBB-class failure (no paperwork → "they don't return calls"); protects the elderly-customer base where one bad incident = reputational ruin.
- **Main risk:** Thin evidence — he may not perceive the problem; discovery must surface it before any offer.
- **Alternatives:** Jobber service reports ($70+/mo) — viable and cheaper if he adopts a platform; custom only if he wants zero process change.

### Ranking summary
| # | Prospect | Evidence strength | Complexity | Est. build | Confidence |
|---|---|---|---|---|---|
| 1 | Keil Plumbing & Heating | High | Low–Med | $3–6k | High |
| 2 | FATman Plumbing Pro | Medium | Low–Med | $2–4k | Medium |
| 3 | Discount Mechanical | High | Medium | $4–8k | High (fit: Medium) |
| 4 | New Life Contracting (conditional) | High observed | Low→Med | $1.5–3k+ | Medium (verify first) |
| 5 | Climate Heating & Cooling | Low–Medium | Low | $2–4k | Low–Medium |

**Recommended first prospect to investigate: #1 Keil Plumbing & Heating.** Reasons: (a) three corroborating source types over 2018–2024; (b) quantified employee testimony of office collapse; (c) dated, specific failure (Feb 2024 double-billing) our AR-suppression logic directly prevents — a *demonstrable, testable* promise; (d) family ownership = single decision-maker; (e) Richmond metro is dense enough for referral fallout if we win; (f) no dependence on distressed status or third-party stack.

---

## 7. Proposed first conversation — questions for the Keil owner (before anything is offered)

1. Walk us through a call that came in last week: who answered, what happened next?
2. How many calls/quote requests do you get per week, and how many get a same-day response?
3. What happens to a quote after it's sent? Who follows up, when, and how often?
4. Where does invoice reminder logic live today? What happens when an invoice is actually paid — before dunning fires?
5. How far back are your AR > 30 days? What's the total?
6. How many no-shows in the last 90 days, and what did each cost you (drive time, fuel, lost slot)?
7. What software do you already pay for (field service, accounting, phones), and what do you actually use?
8. Who handles office work on the owner's day off — and what breaks?
9. What did you wish existed when you left the last house call?
10. If this worked perfectly, what would it be worth per month to you? (Anchoring — do not quote first.)
11. Who else decides? (Spouse? Bookkeeper? — single decision-maker preferred.)
12. Would you pilot 2 weeks on 20 jobs if it cost nothing up front?

**Offer framing for #1:** a measurable pilot, not a platform: 2 weeks, 20 jobs, success = (missed-call callback rate, AR suppressions, quotes closed) — cancel anytime, no upfront fee, $150 setup refunded at pilot end. (Illustrative framing only — pricing to be set in proposal stage.)

---

## 8. Reasons each shortlisted prospect might reject (and how to respond)

| Prospect | Likely rejection | Underlying truth | Response |
|---|---|---|---|
| Keil | "Phones work fine." | Employees know better; owner hasn't looked at data | Show missed-call log from *their own* phone system (with permission) or ask receptionist-agency rate; compare to losing one job/month |
| Keil | "We tried Jobber, nobody used it." | Adoption failure = process failure | Pilot needs **zero logins** — autopilot, not another app |
| Keil | "Too busy right now." | Busy = the problem; classic distress loop | 15-min discovery; pilot requires 0 owner time after 20-min onboarding call |
| FATman | "We're at capacity anyway." | Overflow = #1 value; he can't tell which call was lost | 30-day log of after-hours calls (his voicemails as evidence — with consent) |
| FATman | "$200/mo is money." | Wants ROI clarity | One recovered emergency job ≈ 1–2 months of fee; simple math sheet |
| FATman | "AI scares my customers." | Trust concern | Human-voice cloned with his tone; customer never hears "AI"; opt-out anytime |
| Discount Mechanical | "I have ServiceTitan; software doesn't fix people." | He's right about people — wrong about levers | Agree: this is *management* automation — promises tracked visibly, not another license |
| Discount Mechanical | "Bad ratings are competitors' attacks." | Defensive; common | Don't argue; pilot QA intercept and show internal rating lift on 20 jobs |
| Discount Mechanical | "Can't afford another vendor." | Cash-flow seasonal (AK winter peak) | Performance-based pricing: fee offset against verified jobs recovered (proposal-stage) |
| New Life | (May be defunct/distressed) | Unknown | **Verify first:** BBB file, phone number, permit history; if unreachable or in active dispute → close file, do not pitch |
| New Life | "We got burned by tech people before." | His web developer vanished (casino domain) | Partially our fault as an industry; offer domain-cleanup *first* as a goodwill diagnostic before any sale |
| Climate | "One complaint, whatever." | He doesn't see it | Show him the BBB page; elderly-customer liability photo-essay; 10-min read of what the complainant alleged |
| Climate | "I'm 65+ years old, not a tech guy." | Age/skill anxiety | Tablet-based, 5 taps, voice notes; family (or his son/daughter?) trained in 30 min |

---

## 9. Competitive alternatives (the honest market map)

| Category | Tools (approx. monthly) | Where custom wins | Where custom loses |
|---|---|---|---|
| Field Service Management | Jobber ~$70–150; Housecall Pro ~$60–180; ServiceTitan ($$$) | Only where workflow is unusual or stack is absent | 90% of standard scheduling/invoicing — buy, don't build |
| AI receptionists | Rosie, Goodcall, Slang (~$50–150) | Custom when scripts + AR + reviews must interlock | Simple answer-and-book — buy |
| Answering services | AnswerConnect, Smith.ai (~$100–400) | Custom QA/follow-through logic | Pure overflow scripts — buy |
| Reviews/reputation | NiceJob, Birdeye, Podium (~$90–300) | Custom when intercept-before-public-review is the goal | Basic review solicitation — buy |
| Payments/AR | Stripe, QuickBooks, Jobber Payments | Custom dunning logic suppressing paid-invoice errors (Keil case) | Standard invoicing — buy |
| Website/SEO | Wix/Squarespace, Scorpion ($300–1k/mo) | Emergency rebuild + hijacked domain (New Life) | Ongoing SEO retainer — buy |

**Custom-software bar (this lab's rule):** build only where (a) no off-the-shelf product models the *failure mode* (AR suppression vs payment state; promise-tracking vs booking), or (b) the buyer can't/won't run another platform and needs autopilot.

---

## 10. Evidence & sources (accessed 2026-11-08 unless noted; ● primary, ◐ corroborated, ○ single)

**Market data**
- [M1] RaftLabs — "HVAC quoting software: Win more jobs by sending estimates faster", raftlabs.com/blog, **Nov 3, 2025** ◐ — 61% Jobber 2024 bottleneck stat; 2–3h/day paperwork.
- [M2] US Tech Automations — "Automate HVAC Quoting and Estimates in 2026", ustechautomations.com, **Jun 20, 2026** ◐ — ACCA 23–31% lost quotes; benchmarks; $750K–$6M ICP.
- [M3] US Tech Automations — "Why Quote Turnaround Is Slow in HVAC", **Jun 24, 2026** ◐ — 65%→<30% Jobber 2025; +18pt ACCA 72h follow-up.
- [M4] BBB — Air Pros LLC complaints (Hollywood FL), bbb.org, **Aug–Dec 2025** ● — systemic no-shows/missed windows.
- [M5] BBB — AirMaster HVAC complaints (Orlando FL), **Jul 2025** ● — no-shows, mold excuses, 6-week waits, $450 billing dispute.
- [M6] ConsumerAffairs — One Hour Heating & Air reviews, **Jul–Aug 2026** ◐ — missed appointments, warranty friction.
- [M7] PissedConsumer — Fast Response Heating And Cooling (Columbus-area vendor), **May 10, 2025** ◐ — recurring no-shows, $100 show-up fee disputes.

**Keil Plumbing & Heating (R1)**
- [K1] Official site & contact form (no booking/quote automation; BBB A+ badge displayed) — keilservice.com, **2026-11-08** ●
- [K2] YellowPages Keil profile (Mon–Fri 8–4; hours) — yellowpages.com/richmond-va/mip/keil-plumbing-heating-inc-22416484 ◐
- [K3] Indeed — HVAC Service Coordinator review "…barely hanging on… office manager is MIA most of the week… no employees to run actual calls" (Apr 21, 2022); company 3.0 — indeed.com/cmp/Keil-Plumbing-and-Heating ● (employee voice, dated, raw)
- [K4] ChamberOfCommerce.com Keil listing — Michael P. review (Feb 2024, double-billing after payment) — chamberofcommerce.com/business-directory/virginia/richmond/hvac-contractor/8535271-keil-plumbing-heating-inc ● (user-verified via Google review)
- [K5] AirConditioningProfessionals.com — front-desk threat reviews + "never heard from them again" (2018) — airconditioningprofessionals.com/5534/keil-plumbing-heating ●
- [K6] LocalProBook — 4.1/9 reviews, husband-wife? No — family since 1930, 2507 Willard Rd — localprobook.com/nearme/plumbing/richmond.va.html ◐

**FATman Plumbing Pro (R2)**
- [F1] Official site (hours 9–5, ONLINE BOOKING form page, phone (704) 550-8626, ©2021 footer) — fatmanplumbingpro.com ●
- [F2] TRI-W News feature — Chris Lovick, since 2010, plumbing since 1987 — triwnews.com/featured/... ● (interview content)
- [F3] Yahoo Local / Charlotte best-plumbers list (Jan 28, 2026) — Google 4.9/128, Yelp 4.5/32, Angi 5/17, "small… may not be able to fit new clients promptly" — local.yahoo.com/plumbing/article/best-plumbing-companies-charlotte-north-carolina-110000396.html ◐
- [F4] Yelp listing — (704) 256-1400; address 3615 Providence Rd S — yelp.com/biz/fatman-plumbing-pro-waxhaw-4 ● (NAP inconsistency evidence)

**Discount Mechanical (R3)**
- [D1] Official site markup referencing ServiceTitan Scheduling Pro; online scheduler + instant-estimate journeys — discountmechanical.net, **2026-11-08** ●
- [D2] Yelp — 2.3★/45 reviews; address, hours 24/7 — yelp.com/biz/discount-mechanical-heating-and-plumbing-anchorage ●
- [D3] Angi — Deanna S. (May 2025) boiler install; municipal inspection failed 3×; "I can only hope no one else experiences what I have been through" — angi.com/companylist/us/ak/anchorage/discount-mechanical-heating-plumbing-services-llc-reviews-1.htm ● (named author + date)
- [D4] YellowPages — repeated no-show/callback testimony (undated, 2009–2012 era plus 2012 heater-repair thread) — yellowpages.com/anchorage-ak/mip/discount-mechanical-heating-and-plumbing-459250081 ◐
- [D5] LeadSmart mirror — Nik Shulgin review (Aug 2024): "2 months… couldn't communicate… no callbacks… service manager… no apology" — leadsmartinc.com ●

**New Life Contracting (R4)**
- [N1] Official domain serving gambling/casino content (observed 2026-11-08); cached ZoomInfo profile (Feb 2026) lists same domain as legit — newlifecontracting.org (direct observation) ●
- [N2] BBB — NOT accredited; C+; file opened 3/27/2015 ("Business Started 7/1/2009" — BBB discrepancy noted); 1 complaint in 3 yrs; complaint dated **08/22/2024** "…completely stopped communicating… $3,950.00… police station"; unanswered → rating drag — bbb.org/us/va/aylett/profile/residential-air-conditioning-contractors/new-life-contracting-llc-0603-63404893 ●
- [N3] Porch — 4.65–4.7★/22 reviews; 15–16 yrs; website newlifecontracting.org; $<5M revenue per ZoomInfo (Apr 2026 cache) — pro.porch.com/glen-allen-va/hvac-contractors/new-life-contracting-llc/pp ◐
- [N4] ZoomInfo company profile — revenue <$5M — zoominfo.com/c/new-life-contracting-llc/529776615 ◐

**Climate Heating & Cooling (R5)**
- [C1] Official site — climatecolumbus.com (45-yr family claim; "same-day estimates"; services incl. union/licking/greene counties) ●
- [C2] BBB (Hilliard, OH) — 1 complaint in last 3 years (unresolved older complaint: elderly homeowner, unreturned calls, paperwork promised never delivered) — bbb.org/us/oh/hilliard/profile/heating-and-air-conditioning/climate-heating-cooling-0302-70094940 ●
- [C3] Nextdoor — Gahanna OH page; owner Ken Perry recommended by neighbor (Jul 2023); address 1509 Blatt Blvd — nextdoor.com/pages/climate-heating-cooling-gahanna-oh ●
- [C4] hvacservice.io Columbus — no review volume aggregated (very small/lightly reviewed) — hvacservice.io/oh/columbus ◐

**Other dossiers (R6–R16)**
- [O1] CustomerLobby — Right Way Heating & Cooling review (Chris D., 08/22/2017, front-end scheduling lag) — customerlobby.com/reviews/46349 ◐
- [O2] hvacservice.io Columbus listings — Right Way 5.0/417; Inspired 5.0/19–20; Mr. Tech 5.0/4 — apr 10, 2026 ◐
- [O3] Birdeye — Inspired Heating & Cooling 5.0/19–20, owner-tech "Steven by name" — reviews.birdeye.com/inspired-heating-cooling-electric-roofing-repair-llc-165872430581536 ◐
- [O4] Voolt / Mr. Tech site — Abdullah Rashid ownership; 4–5 reviews 5.0 — voolt.pro/... ●
- [O5] Yelp — Plumb Line 4.6/12 (established 2015, Kevin, husband-wife); Circuit Pros 5.0/5–7; C&C 4.6/11 ("10 mins response"); Apollo 5.0/3 — yelp.com (pages per business) ◐
- [O6] Lamb's Plumbing site review page; BuildZoom 1/5 (Dec 14, 2016) — lambsplumbingva.com ●; buildzoom.com/contractor/lambs-plumbing-richmond ◐
- [O7] SuperPages/YP — Lyons Plumbing ~41 yrs; 2007 fee-opacity complaint (thebirdman7, 06/14/07); Yelp 1.0/1 (2012) — superpages.com/richmond-va/bpp/lyons-plumbing-heating-17129126 ◐
- [O8] Angi — Agape Plumbing 5★×5 (2017–18, Eugene; "called us back within minutes Friday evening"); Porch listing — angi.com/companylist/us/va/richmond/agape-plumbing-reviews-9164193.htm ◐
- [O9] Yelp — Fusion Plumbing **CLOSED** (updated May 2026) — yelp.com/biz/fusion-plumbing-eagle-river ◐
- [O10] Yelp — Independent Heating & Air 1.0★/5 (Jun 2026; permit/registration allegations) — yelp.com/biz/independent-heating-and-air-denver ◐
- [O11] Airstream Services — airstreamteam.com (customer praises SMS comms); Yelp 4.2–4.3/67–75 — yelp.com ●/◐
- [O12] Yahoo Local Charlotte (Jan 2026) — Osborne 2.7★/14; "several thousands on plumbing problems"; Yelp response-time badges 3h–1d — m.m.yelp.com ● (Yelp data via mobile mirror)
- [O13] Service First H&C — servicefirstair.com (154+ 5★); BuildZoom top ~1% — servicefirstair.com ●

**Integrity log:** One business website (New Life) serves third-party gambling content — reported, not exploited, not analyzed as "evidence of wrongdoing," merely flagged as observed. One BBB complaint (Keil) double-source; one employee review (Keil 2022) may be stale. No business was contacted. No pricing claims are binding quotes.

---

## 11. Next steps (NOT executed — awaiting owner decision)
1. **Verification sprint (2–3 days):** phone-dial R1 (Keil) and R4 (New Life) status lines only; check RA license registers (VA DPOR for Keil #; AK CBPL/AKUSA for Discount Mechanical; NC licensing board for FATman); pull BBB files fresh.
2. **Discovery interviews** (with owner consent) — use §7 script.
3. **Pilot design doc** for Keil (metrics + success criteria + kill switch) before any build.
4. Decide whether report goes into `main` via PR (this file lives there per instruction) or stays in working branch.
