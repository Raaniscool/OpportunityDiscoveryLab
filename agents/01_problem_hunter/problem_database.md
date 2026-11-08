# Problem database — Agent 01: Problem Hunter

**Research cutoff: 2026-11-08 UTC. 32 distinct problems. Research only; no product development.**

These are observed problems with candidate responses, **not 32 validated businesses**. Prices are proposed USD validation anchors, **not observed willingness to pay, current competitor prices or forecasts**. Frequencies are qualitative, not incidence estimates. Current-solution lists combine tools named in inspected material with established alternatives; their current features/pricing have not been exhaustively audited. A suspected gap does not establish competitors lack it.

Confidence separates **pain evidence / commercial opportunity**: H = strong, M = moderate, L = weak; not numerical probabilities. Difficulty includes integrations, operations, trust and regulation, not only code. Each title states the problem description; who, evidence, severity, alternatives, limitations and response hypotheses follow. See [method/limitations](README.md#method-and-evidence-limits) and [source register](research_sources.md). S-identifiers are unique; numeric direct-link citation labels repeat because searches restart numbering.

## Index

- [P01 — Subcontractor insurance evidence goes stale between renewals](#p01)
- [P02 — Micro-sellers abandon cross-border sales over safety paperwork](#p02)
- [P03 — Restaurant allergen records drift after supplier or recipe changes](#p03)
- [P04 — Allergy shoppers cannot trust unchanged packaging or app records](#p04)
- [P05 — Patients and clinics cannot locate the stalled prior-authorization step](#p05)
- [P06 — Family care handoffs lack a reliable shared action record](#p06)
- [P07 — Disaster claimants reconcile possessions and replacement receipts manually](#p07)
- [P08 — IEP accommodation evidence is fragmented across classrooms and revisions](#p08)
- [P09 — Therapists cannot easily validate payment-documentation completeness](#p09)
- [P10 — Service merchants collect chargeback evidence too late or in the wrong form](#p10)
- [P11 — Construction changes proceed without authorized price approval](#p11)
- [P12 — Repair-shop parts pass catalog filters but still arrive unsuitable](#p12)
- [P13 — Truck detention pay is denied when notices or timestamps are missing](#p13)
- [P14 — Freezer sample records diverge from physical reality](#p14)
- [P15 — Review teams need defensible complex extraction and duplicate decisions](#p15)
- [P16 — Historical handwriting blocks family-history research despite OCR](#p16)
- [P17 — 3D-print beginners cannot distinguish similar failure causes](#p17)
- [P18 — Game localization lacks runtime context and breaks after changes](#p18)
- [P19 — Blind users can read some PDFs but cannot use layouts or forms](#p19)
- [P20 — Tool-using agents can mistake hostile content for authorized instructions](#p20)
- [P21 — CI-only browser flakes consume debugging time and erode test trust](#p21)
- [P22 — Security scanners disagree about affected dependency versions](#p22)
- [P23 — Offboarding needs proof across sessions, accounts, licenses and ownership](#p23)
- [P24 — Hiring clients cannot separate real freelancers from generic/deceptive applications](#p24)
- [P25 — Craft creators struggle to document copied patterns across marketplaces](#p25)
- [P26 — AI-authorship disputes lack fair process evidence](#p26)
- [P27 — Familiar voices no longer authenticate emergency money requests](#p27)
- [P28 — Home sewists waste effort assembling or mis-scaling PDF patterns](#p28)
- [P29 — Home bakers struggle to keep recipe costs current with prices and labor](#p29)
- [P30 — Tenancy deposit disputes lack comparable inspection evidence](#p30)
- [P31 — Noise-sensitive diners cannot predict usable venues by time and table](#p31)
- [P32 — Occasional groups dislike subscription economics for expense splitting](#p32)

<a id="p01"></a>
## P01 — Subcontractor insurance evidence goes stale between renewals

- **Who / buyer:** Small general contractors; buyer: operations/finance lead.
- **Evidence:** Coordinator reports spending the day chasing certificates. Other contractors describe spreadsheets and automation. Property managers with AppFolio explicitly dispute that this is painful. Sources: [3](https://www.reddit.com/r/ConstructionManagers/comments/1om1rn7/new_pm_here_am_i_crazy_or_is_tracking_sub/) (S01); [5](https://www.reddit.com/r/PropertyManagement/comments/1pgesg6/is_coi_tracking_actually_a_pain_point_for_smaller/) (S02); [4](https://www.reddit.com/r/GeneralContractor/comments/1ul6bxl/how_do_you_handle_subcontractor_coi_and_license/) (S03).
- **Frequency / severity:** Onboarding and policy renewals across active subs; recurring staff burden. No reliable average hours or uninsured-loss rate.
- **Current solutions:** Sheets/scripts, broker service, Procore, AppFolio, houndDog/JobTread and dedicated COI vendors.
- **Why a gap may remain / counterevidence:** Narrow gap: correcting incomplete documents and follow-up in poorly served firms, not missing expiry reminders. Some solve it cheaply already.
- **Potential product/service (hypothesis):** Broker-assisted collection service: extract dates/limits, flag missing endorsements, request corrections and record expert approval. A certificate alone does not establish coverage.
- **Potential monetization (untested):** Proposed $100–400/month per small GC or broker-distributed per-vendor service; verify whether broker already includes it.
- **Estimated technical / delivery difficulty:** High: OCR moderate; endorsements, contractual requirements, cancellation status and liability hard.
- **Confidence:** Pain H; commercial M. Multiple accounts, substantial incumbent/counterevidence.
- **AI trajectory:** Better document models reduce rekeying; fake AI-generated certificates increase provenance need. Coverage still requires authoritative verification.
- **Next validation:** Interview 8 GCs and 3 brokers; inspect redacted correction threads and compare complete current workflows.

<a id="p02"></a>
## P02 — Micro-sellers abandon cross-border sales over safety paperwork

- **Who / buyer:** Handmade physical-goods sellers with meaningful EU demand; buyer: shop owner.
- **Evidence:** Sellers report stopping EU shipping or confusion; others find compliance manageable after setup. Official FAQ confirms a substantive responsible-person role; comment interpretations are not legal advice. Sources: [2](https://www.reddit.com/r/EtsySellers/comments/1n620wc/uk_sellers_how_are_you_handling_eu_sales/) (S04); [1](https://www.reddit.com/r/EtsySellers/comments/1iuzxqe/gpsr_what_are_you_doing_about_it/) (S05); [3](https://webgate.ec.europa.eu/safety/consumers/consumers_safety_gate/obligationsForBusinesses/documents/Q&A.pdf) (S06).
- **Frequency / severity:** Initial setup, new SKUs/materials/markets. Severe if profitable export channel closes; no prevalence measured.
- **Current solutions:** Etsy guidance, responsible-person agencies, consultants, manual technical files or avoiding EU sales.
- **Why a gap may remain / counterevidence:** Expert setup and repeated listing/document updates may exceed low-volume export profit. Actual service coverage and prices need quotes.
- **Potential product/service (hypothesis):** Category-specific expert-reviewed documentation and listing-maintenance service, partnering with a legitimate EU responsible person; start with one low-risk craft category.
- **Potential monetization (untested):** Proposed setup fee plus $15–50/month maintenance, representative fee separate; viable only where export profit supports it.
- **Estimated technical / delivery difficulty:** High: jurisdiction, materials risk and legal responsibility dominate coding.
- **Confidence:** Pain H; commercial M. Multiple seller accounts, but some rationally should not export.
- **AI trajectory:** AI can draft/translate evidence-linked files, not invent risk analysis or replace accountable legal entities. Marketplace bundling could eliminate wedge.
- **Next validation:** Get agency quotes and anonymized EU gross-margin data from 10 sellers; qualified product-safety professional reviews service boundary.

<a id="p03"></a>
## P03 — Restaurant allergen records drift after supplier or recipe changes

- **Who / buyer:** Independent restaurants/caterers; buyer: owner, chef or food-safety manager.
- **Evidence:** Operators describe folders/internal guides. FSA guidance calls for accurate information and supplier-change checks. One operator reports few requests, weakening convenience-only demand. Sources: [4](https://www.reddit.com/r/restaurantowners/comments/15vju5a/do_allergy_labels_on_your_menu_help_or_does_it/) (S07); [3](https://www.gov.uk/government/publications/allergen-information-for-non-prepacked-foods-best-practice/allergen-information-for-non-prepacked-foods-best-practice) (S08); [1](https://www.food.gov.uk/business-guidance/precautionary-allergen-labelling) (S09).
- **Frequency / severity:** Recipe updates/substitutions, potentially each delivery; mistakes can be medically severe. No restaurant error rate measured.
- **Current solutions:** Ingredient binders, recipe cards, matrices and recipe-management platforms.
- **Why a gap may remain / counterevidence:** Storing a matrix does not ensure substituted labels were checked and affected dishes/staff guidance updated. This is a workflow inference, not a measured software failure rate.
- **Potential product/service (hypothesis):** Human-approved change-control service: compare photographed labels to specifications, trace affected dishes and require chef review. Track cross-contact separately.
- **Potential monetization (untested):** Proposed $50–150/location/month through food-safety consultants.
- **Estimated technical / delivery difficulty:** High: ingredient versions, recipe dependencies, staff adoption and safety validation.
- **Confidence:** Pain M–H; commercial M. Strong official workflow basis; limited recent firsthand operator pain.
- **AI trajectory:** Vision can flag differences but failure to detect an allergen must never imply safe. Kitchen practices still need human controls.
- **Next validation:** Observe deliveries in 5 kitchens; test existing recipe-tool propagation and willingness to pay for reviewed exceptions.

<a id="p04"></a>
## P04 — Allergy shoppers cannot trust unchanged packaging or app records

- **Who / buyer:** Households managing multiple food allergies; buyer: household or care sponsor.
- **Evidence:** Consumer reports dairy-free cheese changing to cashew in similar packaging. Fig user reports database/physical-label mismatch; others insist on checking every purchase. Sources: [8](https://www.reddit.com/r/nutallergy/comments/1iz6pxs/urgent_bettergoods_ingredient_change/) (S10); [9](https://www.reddit.com/r/FoodAllergies/comments/1kerg8k/best_or_most_efficient_way_to_check_allergen/) (S11).
- **Frequency / severity:** Every grocery purchase; missed change potentially serious. No population incident rate established.
- **Current solutions:** Physical labels, Fig, manufacturer calls, avoidance and minimally processed food.
- **Why a gap may remain / counterevidence:** Barcode databases can lag formulations; uncommon allergens and cross-contact remain uncertain. A scanner cannot infer undisclosed ingredients.
- **Potential product/service (hypothesis):** Private package-change journal comparing actual label photos with previously reviewed packages, highlighting differences and drafting manufacturer questions—not safe-to-eat advice.
- **Potential monetization (untested):** Proposed $20–40/year family plan; sponsored access may work better.
- **Estimated technical / delivery difficulty:** High: label OCR, formulation versions and safety-sensitive uncertainty.
- **Confidence:** Pain H; commercial L–M. Urgent concrete accounts, trust/liability and existing apps substantial.
- **AI trajectory:** Vision makes package-level comparison cheaper; hallucinated reassurance makes autonomous recommendations unacceptable.
- **Next validation:** With allergy organization, compare difference-highlighting against careful reading on reviewed historical labels.

<a id="p05"></a>
## P05 — Patients and clinics cannot locate the stalled prior-authorization step

- **Who / buyer:** US chronic-medication patients and small specialty clinics; buyer: clinic or benefit sponsor.
- **Evidence:** Patient reports one of two medicines approved with no visible request for the other. Clinicians describe repeated effort; AMA survey commentary corroborates burden but is an advocacy source. Sources: [1](https://www.reddit.com/r/HealthInsurance/comments/1i8gq4v/how_are_prior_authorizations_for_medications_you/) (S12); [2](https://www.reddit.com/r/FamilyMedicine/comments/1ka7kvu/how_is_prior_authorization_affecting_your_ability/) (S13); [3](https://www.ama-assn.org/about/leadership/it-time-make-prior-authorization-reform-reality) (S14).
- **Frequency / severity:** New prescriptions, plan switches and renewals; delays may interrupt treatment. No per-clinic baseline established.
- **Current solutions:** CoverMyMeds, EHR tools, pharmacy calls, patient portals and manual advocates.
- **Why a gap may remain / counterevidence:** Status fragmented across organizations; a portal cannot fix an unsent form, wrong benefit pathway or unreachable staff.
- **Potential product/service (hypothesis):** Human-operated closed-loop renewal/status concierge for one specialty: document receipt, responsible party and next action, with clinician-approved submissions.
- **Potential monetization (untested):** Proposed clinic retainer or per-completed-case fee, employer sponsorship alternative. No approval guarantees or desperation-based pricing.
- **Estimated technical / delivery difficulty:** Very high: PHI controls, payer access, permissions and organizational cooperation.
- **Confidence:** Pain H; commercial M. Strong evidence, crowded market and unclear access.
- **AI trajectory:** AI summarizes correspondence and missing evidence; insurer AI can add opposing friction. Never fabricate clinical justifications.
- **Next validation:** Shadow 20 consented cases; determine which delays can change without payer integration and compare current vendors.

<a id="p06"></a>
## P06 — Family care handoffs lack a reliable shared action record

- **Who / buyer:** Families sharing elder/disability care; buyer: lead caregiver, agency or sponsor.
- **Evidence:** Caregivers describe lists, pill sorters and notebooks. Existing-app recommendations are common; many maker replies are promotion, not independent validation. Sources: [1](https://www.reddit.com/r/CaregiverSupport/comments/1n9kxm1/are_there_any_family_care_coordination_apps/) (S15); [2](https://www.reddit.com/r/AgingParents/comments/1pqm37o/how_are_you_handling_a_shared_medication_log_with/) (S16); [1](https://apps.apple.com/us/app/medisafe-medication-management/id573916946) (S17).
- **Frequency / severity:** Daily handoffs and medication events. Errors potentially serious; empty compartment/checked box does not prove ingestion.
- **Current solutions:** Home notebook, pill sorter, group chat, Cozi/AnyList, Medisafe and care-specific apps.
- **Why a gap may remain / counterevidence:** Gap is shared adoption and responsibility, not another calendar. Remote entries may not reflect physical administration; notebooks often work.
- **Potential product/service (hypothesis):** Accessible care-station workflow plus assisted setup: acknowledged handoff tasks and printable history. Explicitly distinguish reported administration from verified ingestion; never change dosing.
- **Potential monetization (untested):** Proposed $5–10/family/month or agency bundle; setup/training might be more valuable.
- **Estimated technical / delivery difficulty:** High: offline consistency, accessibility, permissions, safety and onboarding.
- **Confidence:** Pain H; commercial L–M. Many working substitutes, payer unclear.
- **AI trajectory:** Voice-to-structured logs reduce effort; summaries must preserve contradictory source entries rather than silently reconcile medications.
- **Next validation:** Observe 6 shared-care households; verify recording consistency actually beats their notebook.

<a id="p07"></a>
## P07 — Disaster claimants reconcile possessions and replacement receipts manually

- **Who / buyer:** Insured fire/flood households; buyer: claimant, restoration firm or authorized claims professional.
- **Evidence:** Claimants describe matching receipts to inventory IDs, actual cash value and recoverable depreciation; others report very long contents inventories. Accounts are unverified and policy-specific. Sources: [3](https://www.reddit.com/r/Insurance/comments/1d78f6d/house_fire_contents_advice_for_receipt/) (S18); [1](https://www.reddit.com/r/homeowners/comments/19d7quf/if_my_house_burnt_down_insurance_on_contents/) (S19).
- **Frequency / severity:** Episodic per household, repeated across claims portfolio; work may continue months after loss.
- **Current solutions:** Insurer spreadsheets, photos, restoration inventories, public adjusters and receipt folders.
- **Why a gap may remain / counterevidence:** Capture is only the beginning: linking replacement purchases and tracking unclaimed items is ongoing stressful clerical work.
- **Potential product/service (hypothesis):** Assisted contents reconciliation retaining original photos/receipts, draft rows with provenance, replacement links and insurer-compatible exports. Never invent possessions or prices.
- **Potential monetization (untested):** Proposed $100–500 fixed admin package or professional per-case license. Claim-proceeds-based fees may trigger regulation; review first.
- **Estimated technical / delivery difficulty:** High: matching, insurer formats, privacy and insurance-adjusting boundary.
- **Confidence:** Pain H; commercial M. Concrete workflows; lawful channel and insurer acceptance untested.
- **AI trajectory:** Multimodal models lower sorting cost; human confirmation/source retention matter more than fluent descriptions. Capture alone is commoditizing.
- **Next validation:** Interview 5 claimants and 3 licensed professionals; manually reconcile redacted historical claim and check accepted exports.

<a id="p08"></a>
## P08 — IEP accommodation evidence is fragmented across classrooms and revisions

- **Who / buyer:** Special-education teachers/families; buyer: school or advocacy practice.
- **Evidence:** Teachers describe per-student used/refused/absent spreadsheets and service logs. Separate thread disputes amendments/notice; neither side’s legal correctness is established. Sources: [1](https://www.reddit.com/r/specialed/comments/18ybeb5/documenting_refusal_to_use_accommodations/) (S20); [5](https://www.reddit.com/r/specialed/comments/1ljm2uj/amendments_made_to_iep_without_parental/) (S21).
- **Frequency / severity:** Daily support/assessment logs and annual/amended plans; consequential for student support and disputes.
- **Current solutions:** eSped/service logs, gradebooks, paper forms, parent email and district IEP systems.
- **Why a gap may remain / counterevidence:** Plan storage may not make daily implementation/changes visible; teachers already face logging burdens and local rules vary.
- **Potential product/service (hypothesis):** Low-friction evidence capture and meeting pack linking observations to exact plan versions and showing unresolved discrepancies. Do not automate eligibility or consent.
- **Potential monetization (untested):** Proposed school license or advocate per-case fee; direct-family payment could exclude highest-need users.
- **Estimated technical / delivery difficulty:** High: student privacy, integrations, permissions, accessibility and educational/legal nuance.
- **Confidence:** Pain M–H; commercial L–M. Workflow clear, budget and incumbent gap unclear.
- **AI trajectory:** AI extracts obligations and compares revisions with source citations; must not decide an accommodation should be removed.
- **Next validation:** Interview teachers, families and district privacy staff separately; check whether workflow reduces total logging effort.

<a id="p09"></a>
## P09 — Therapists cannot easily validate payment-documentation completeness

- **Who / buyer:** Small US insurance-taking therapy practices; buyer: owner or billing service.
- **Evidence:** Therapist asks about conflicting audit advice; replies discuss progress-note omissions. Counterthread describes eligibility/other-insurance recoupments that documentation checks cannot prevent. Sources: [1](https://www.reddit.com/r/therapists/comments/1pl6ntb/question_about_insurance_audits_clawbacks_and/) (S22); [4](https://www.reddit.com/r/therapists/comments/1s9ri4g/opened_my_own_practice_and_current_supervisor_is/) (S23).
- **Frequency / severity:** Notes every session; audits episodic. Financial stakes serious, average audit/clawback rates not verified.
- **Current solutions:** EHR templates, AI scribes, billers, payer manuals, training and chart audits.
- **Why a gap may remain / counterevidence:** More generated text is not validation of payer-specific rules, time consistency or signatures. Some uncertainty is substantive payer dispute.
- **Potential product/service (hypothesis):** Evidence-linked pre-billing completeness review, initially through qualified billing service. Flag omissions; never manufacture medical necessity or rewrite clinical history.
- **Potential monetization (untested):** Proposed $40–100/clinician/month or outsourced monthly chart review.
- **Estimated technical / delivery difficulty:** High: PHI, versioned payer rules, clinical review and false assurance.
- **Confidence:** Pain H; commercial M. Repeated confusion, but audit-prevention claims unsupported.
- **AI trajectory:** AI compares fields against cited rules; generic generated notes can increase boilerplate and contradictions. Expert review is more durable.
- **Next validation:** Qualified biller labels 30 redacted charts against 3 payer manuals through consented practices; distinguish fixable omissions from eligibility risk.

<a id="p10"></a>
## P10 — Service merchants collect chargeback evidence too late or in the wrong form

- **Who / buyer:** Cleaning/repair/appointment businesses; buyer: owner or processor partner.
- **Evidence:** Shop and cleaning-service posters report losing despite photos/messages. Replies emphasize reason codes and include businesses that win; issuer decisions cannot be guaranteed. Sources: [1](https://www.reddit.com/r/smallbusiness/comments/18ij1tb/the_customer_filed_a_chargeback_for_a_large/) (S24); [5](https://www.reddit.com/r/smallbusiness/comments/1m47umh/dont_use_stripe_if_youre_in_the_cleaning_business/) (S25).
- **Frequency / severity:** Unpredictable; single loss can matter. One first dispute after two years suggests subscription frequency risk.
- **Current solutions:** Processor portals, signed agreements, photos, fraud screening and recovery specialists.
- **Why a gap may remain / counterevidence:** Disconnected evidence may omit explicit scope/acceptance or fail to address dispute reason. Better presentation cannot reverse all liability rules.
- **Potential product/service (hypothesis):** At-service consent/completion capture plus human-reviewed reason-specific dispute packet linked to originals; legal review of terms required.
- **Potential monetization (untested):** Proposed $25–75/case administrative fee or vertical add-on, no recovery guarantee.
- **Estimated technical / delivery difficulty:** Medium–high: payments integration, retention and changing rules.
- **Confidence:** Pain H; commercial M. Loss evidence strong; incremental recovery and frequency unproven.
- **AI trajectory:** AI organizes evidence; issuer automation can neutralize generic narratives. Authentic pre-dispute capture is the potential advantage.
- **Next validation:** Payments expert reviews 20 historical cases, including well-documented losses, to isolate addressable omissions.

<a id="p11"></a>
## P11 — Construction changes proceed without authorized price approval

- **Who / buyer:** Small contractors/homeowners; buyer: contractor operations lead.
- **Evidence:** Homeowner reports rejected emailed quote later billed; contractor describes unpaid verbally approved work. Newer account reports extra charge after completion. Two-sided conflict, not legal determination. Sources: [3](https://www.reddit.com/r/HomeImprovement/comments/p4hsw4/contractor_charging_us_for_change_orders_we_didnt/) (S26); [5](https://www.reddit.com/r/Homebuilding/comments/1uy0yv3/siding_contractor_completed_work_and_now/) (S27).
- **Frequency / severity:** Each scope change; payment/schedule stakes high. No incidence estimate.
- **Current solutions:** Signed change orders, email/text, PM suites and e-signature tools.
- **Why a gap may remain / counterevidence:** Gap is capturing a field decision before work with scope, price and actual approver—not producing a form afterward. Intentional disputes may persist.
- **Potential product/service (hypothesis):** Mobile/managed approval workflow: photo/voice draft linked to original scope; explicit authorized price/time approval before crew release; exception log.
- **Potential monetization (untested):** Proposed $30–100/company/month or trade-specific operations service.
- **Estimated technical / delivery difficulty:** Medium–high: mobile reliability, authority rules, audit trails and integration.
- **Confidence:** Pain H; commercial M. Bilateral evidence, crowded feature space.
- **AI trajectory:** AI flags possible scope changes in consented messages and drafts requests; silence is not approval and AI cannot certify enforceability.
- **Next validation:** Ask 8 remodelers for last disputed change/current tool; separate workflow friction from customer refusal.

<a id="p12"></a>
## P12 — Repair-shop parts pass catalog filters but still arrive unsuitable

- **Who / buyer:** Independent repair/body shops; buyer: shop or distributor.
- **Evidence:** Shop owner describes return economics; separate discussion describes hours lost to wrong part, alongside users reporting good online accuracy. Sources: [1](https://www.reddit.com/r/Autobody/comments/1qxrrkz/be_careful_with_parts_geek/) (S28); [2](https://www.reddit.com/r/cars/comments/15r40m5/i_really_try_to_support_my_local_auto_parts_store/) (S29).
- **Frequency / severity:** At ordering/returns; may block repair bay. Individual costs/delays not averages.
- **Current solutions:** VIN catalogs, OEM numbers, counter staff, manual photos and local exchanges.
- **Why a gap may remain / counterevidence:** Trim/options and catalog errors defeat simple filters; supplier terms also drive loss and cannot be solved by AI.
- **Potential product/service (hypothesis):** Assisted pre-order exception check using VIN/options, licensed OEM references and removed/replacement-part photos, with supplier responsibility record.
- **Potential monetization (untested):** Proposed distributor-funded service or $50–150/shop/month; data licensing could overwhelm economics.
- **Estimated technical / delivery difficulty:** Very high: authoritative fitment/data rights harder than image similarity.
- **Confidence:** Pain M–H; commercial L–M. Real accounts, unresolved data access.
- **AI trajectory:** Vision can flag connector/mount differences but plausible appearance never establishes mechanical compatibility.
- **Next validation:** Analyze 50 returns by root cause; obtain catalog rights and distributor interest before development.

<a id="p13"></a>
## P13 — Truck detention pay is denied when notices or timestamps are missing

- **Who / buyer:** Owner-operators/small carriers; buyer: carrier owner or dispatcher.
- **Evidence:** Driver reports six-hour wait with denial after missing signed time-out. Brokers describe timely-notice/tracking/signature conditions. FMCSA project corroborates measurement importance, not recoverable market size. Sources: [1](https://www.reddit.com/r/Truckers/comments/1rib6o6/owneroperators_how_much_are_you_losing_to_pay/) (S30); [3](https://www.reddit.com/r/FreightBrokers/comments/11l261o/what_are_your_rules_for_detention/) (S31); [3](https://www.fmcsa.dot.gov/research-and-analysis/impact-driver-detention-time-safety-and-operations) (S32).
- **Frequency / severity:** Delayed pickups/deliveries, repeated across fleet; no national recovery rate inferred.
- **Current solutions:** BOL annotations, dispatch messages, ELD/GPS, TMS records and manual claims assistance.
- **Why a gap may remain / counterevidence:** Scattered proof and contract-specific notice conditions can invalidate waiting evidence. GPS alone does not establish payment entitlement.
- **Potential product/service (hypothesis):** Contract-aware detention admin service: extract rate-confirmation terms, prompt notices, preserve approved timestamps/refused signatures and prepare broker-ready packets.
- **Potential monetization (untested):** Proposed $15–40/truck/month or legally reviewed per-case admin fee; no automatic bond escalation.
- **Estimated technical / delivery difficulty:** High: ELD access, offline/geofence reliability, contract interpretation and broker acceptance.
- **Confidence:** Pain H; commercial M. Two-sided operational evidence, incremental collection unproven.
- **AI trajectory:** AI extracts terms and coordinates records cheaply; authentic timestamps and broker cooperation remain scarce inputs.
- **Next validation:** Interview 6 carriers/4 brokers; review 30 historical claims, especially complete-evidence denials, against broker acceptance criteria.

<a id="p14"></a>
## P14 — Freezer sample records diverge from physical reality

- **Who / buyer:** Academic wet labs/shared facilities; buyer: lab manager or PI.
- **Evidence:** Lab users describe spreadsheets, location codes and sometimes memory; another asks how to migrate a large existing collection into searchable locations. Sources: [1](https://www.reddit.com/r/labrats/comments/qfiarz/how_do_you_keep_track_of_your_samples_in_the_80/) (S33); [2](https://www.reddit.com/r/labrats/comments/y8ebej/really_stumped_on_how_to_physically_digitally/) (S34).
- **Frequency / severity:** Each retrieval/put-away and staff transition; lost time/sample risk plausible, unquantified.
- **Current solutions:** Excel, Access, Labcollector, LIMS, barcode/FluidX tubes and rack maps.
- **Why a gap may remain / counterevidence:** Inventory platforms do not fix unlabelled legacy boxes; continued scan discipline and cold-workflow usability determine accuracy.
- **Potential product/service (hypothesis):** Inventory-recovery/migration service: scan boxes, map legacy IDs with uncertainty, label locations and implement low-friction check-in/out.
- **Potential monetization (untested):** Proposed paid freezer audit/setup plus maintenance; physical services may beat stand-alone SaaS.
- **Estimated technical / delivery difficulty:** High: tiny/frosted labels, legacy identifiers, physical work and tracking reliability.
- **Confidence:** Pain M–H; commercial M. Independent but older accounts; freshness and procurement need checking.
- **AI trajectory:** Vision reduces transcription but cannot identify obscured contents or substitute for handling procedures.
- **Next validation:** Observe 2 labs and a core facility; audit mismatches in one consented freezer and compare existing LIMS setup services.

<a id="p15"></a>
## P15 — Review teams need defensible complex extraction and duplicate decisions

- **Who / buyer:** Graduate/evidence-review teams; buyer: PI, institution or commissioned-review firm.
- **Evidence:** Researchers praise Covidence/Rayyan yet describe extraction/scale constraints. Zotero user reports 10,214 duplicates; support warns automatic merging loses distinctions. Sources: [3](https://www.reddit.com/r/AskAcademiaUK/comments/1k0jppk/systematic_review_software/) (S35); [3](https://forums.zotero.org/discussion/114183/fusion-duplicated-files) (S36).
- **Frequency / severity:** Project-based, potentially thousands of records; researcher time, no representative baseline.
- **Current solutions:** Covidence, Rayyan, EPPI Reviewer, Zotero, spreadsheets and librarians.
- **Why a gap may remain / counterevidence:** Existing tools solve much screening. Complex extraction and study-vs-publication identity still need auditable decisions, not generic summaries.
- **Potential product/service (hypothesis):** Assisted review-operations service with quoted source spans, schemas, reversible duplicate proposals and adjudication queue.
- **Potential monetization (untested):** Proposed per-review fee or institutional seats; free tools constrain student prices.
- **Estimated technical / delivery difficulty:** High: recall validation, tables, identity and reproducibility.
- **Confidence:** Pain M–H; commercial M. Direct requests, strong incumbent praise.
- **AI trajectory:** AI reduces triage/extraction effort but false exclusions can miss evidence. Human methodological oversight remains essential.
- **Next validation:** Benchmark against an adjudicated review with librarian supervision and compare niche extraction to incumbent AI features.

<a id="p16"></a>
## P16 — Historical handwriting blocks family-history research despite OCR

- **Who / buyer:** Genealogists/archive researchers; buyer: individual or archive.
- **Evidence:** Users request help reading a will and bad handwriting. Transkribus recommended; users report corrections and invented readings in general AI outputs. Sources: [2](https://www.reddit.com/r/Genealogy/comments/1kka0b2/is_there_ai_capable_of_reading_really_bad_hand/) (S37); [3](https://www.reddit.com/r/Genealogy/comments/1b0japc/a_service_to_read_old_handwritten_documents_a/) (S38).
- **Frequency / severity:** Each unfamiliar script/document; recurring enthusiast need, episodic casual use.
- **Current solutions:** Transkribus, script tutorials, professional paleographers, volunteers and general models.
- **Why a gap may remain / counterevidence:** Names/scripts/damage remain ambiguous; fabricated names contaminate family trees.
- **Potential product/service (hypothesis):** Expert-assisted transcription with line/word image alignment, alternate readings and escalation, specialized by script/region.
- **Potential monetization (untested):** Proposed per-page credits or expert review; hobbyist willingness/archive rights untested.
- **Estimated technical / delivery difficulty:** Medium–high: interface moderate, difficult scripts and expert supply hard.
- **Confidence:** Pain H; commercial M. Direct service requests, strong specialist incumbent.
- **AI trajectory:** Better vision cheapens first pass; provenance and expert adjudication more durable than raw OCR.
- **Next validation:** Paleographer blind-scores licensed documents; ask paying genealogists about premium for uncertain-name review.

<a id="p17"></a>
## P17 — 3D-print beginners cannot distinguish similar failure causes

- **Who / buyer:** Hobbyists/print farms; buyer: user or printer support team.
- **Evidence:** Posters try materials/settings without resolution; replies diagnose Z offset, flow or surface issues and note inadequate photo angles. Sources: [2](https://www.reddit.com/r/3Dprinting/comments/1aim9dr/help_diagnosing_a_first_layer_issue/) (S39); [1](https://www.reddit.com/r/FixMyPrint/comments/rsjrh8/diagnosing_first_layer_problems/) (S40).
- **Frequency / severity:** Per failed/calibration print; material/time waste, unquantified. Newer auto-calibrating printers may reduce need.
- **Current solutions:** FixMyPrint, manufacturer support, calibration guides, slicer tests and camera monitoring.
- **Why a gap may remain / counterevidence:** One symptom has multiple causes; generic advice encourages changing many variables without controlled tests.
- **Potential product/service (hypothesis):** Printer-aware guided diagnosis combining settings/logs/requested photos, suggesting one safe reversible test at a time.
- **Potential monetization (untested):** Proposed per-session support fee or manufacturer license; household subscription weak.
- **Estimated technical / delivery difficulty:** High: device diversity, causal ambiguity and safe configuration changes.
- **Confidence:** Pain M–H; commercial L–M. Historical recurrence, free support/hardware progress undermine wedge.
- **AI trajectory:** Vision narrows hypotheses; experiments establish causes. Better printers may eliminate much of the problem.
- **Next validation:** Compare supervised troubleshooting with free guides across actual failures on old/new printers.

<a id="p18"></a>
## P18 — Game localization lacks runtime context and breaks after changes

- **Who / buyer:** Indie/mid-sized studios/localization agencies; buyer: producer.
- **Evidence:** Developer describes substantial custom context/string tooling. Another reports mistranslated mechanics and overflow. Crowdin reply describes existing screenshot/glossary support. Sources: [3](https://www.reddit.com/r/gamedev/comments/1knbv6w/what_do_your_localizationtranslation_tech_stacks/) (S41); [2](https://www.reddit.com/r/GameDevelopment/comments/1rj2pnc/why_translating_our_skill_trees_and_ui_almost/) (S42).
- **Frequency / severity:** Each content update/locale release; rework and comprehension stakes, revenue effect unverified.
- **Current solutions:** Crowdin, Lokalise, context CSVs, glossaries, engine localization and human LQA.
- **Why a gap may remain / counterevidence:** Potential gap is capturing runtime context, changed mechanics and actual-build overflow without custom engineering, not basic translation management.
- **Potential product/service (hypothesis):** Engine-specific QA service capturing string-to-scene context, changed terminology and layout exceptions with translator-ready evidence/human review.
- **Potential monetization (untested):** Proposed per-release package or $100–500/studio/month; agencies potential channel.
- **Estimated technical / delivery difficulty:** High: engine integration, dynamic text, screenshots and locale validation.
- **Confidence:** Pain H; commercial M. Detailed developer account, incumbent scope uncertain.
- **AI trajectory:** Raw AI translation gets cheap; contextual verification matters more. Multimodal triage must not silently rewrite design intent.
- **Next validation:** Interview 5 studios/3 LQA agencies; inspect shipped rework and compare runtime coverage to current integrations.

<a id="p19"></a>
## P19 — Blind users can read some PDFs but cannot use layouts or forms

- **Who / buyer:** Blind students/workers and issuers; buyer: employer, university or publisher.
- **Evidence:** Blind community recommends multiple scanned-PDF workarounds; another user distinguishes readable PDFs from difficulty editing/filling forms. Sources: [3](https://www.reddit.com/r/Blind/comments/1mexedk/how_do_you_read_scanned_pdf_documents/) (S43); [2](https://www.reddit.com/r/Blind/comments/ykxwds/accessible_pdf_editing_program/) (S44).
- **Frequency / severity:** Each inaccessible document; can block work/study. Prevalence unmeasured.
- **Current solutions:** JAWS OCR, FineReader, Voice Dream, Acrobat/Word conversion and institutional accommodations.
- **Why a gap may remain / counterevidence:** OCR alone does not assure reading order, tables or form controls. Existing tools already work well for basic scans.
- **Potential product/service (hypothesis):** Validated accessible document-operation service: structured conversion plus navigable forms, tested by screen-reader users and preserving original content.
- **Potential monetization (untested):** Proposed institutional per-document service/retainer, not charging individuals for access barriers.
- **Estimated technical / delivery difficulty:** Very high: layout semantics, editing, privacy and assistive-technology QA.
- **Confidence:** Pain H; commercial M. Firsthand task barriers, differentiation/procurement uncertain.
- **AI trajectory:** Multimodal models recover structure but may alter numbers/content. Faithful comparison and user testing essential.
- **Next validation:** Pay blind testers to complete real permitted forms; compare task completion, not merely OCR, against current remediation services.

<a id="p20"></a>
## P20 — Tool-using agents can mistake hostile content for authorized instructions

- **Who / buyer:** Organizations deploying agents with sensitive tools; buyer: security/platform lead.
- **Evidence:** Public project requests adversarial CI for hidden instructions/unauthorized writes. Security reporting describes an exfiltration demonstration; neither establishes widespread incident frequency. Sources: [1](https://github.com/esharif20/finance-agent/issues/142) (S45); [2](https://thehackernews.com/2026/07/public-github-issue-could-trick-github.html) (S46).
- **Frequency / severity:** Potential at every untrusted-input boundary; severe with broad permissions, frequency unknown.
- **Current solutions:** Least privilege, sandboxing, approvals, red teams, scanners and guardrails.
- **Why a gap may remain / counterevidence:** Content filters cannot guarantee authorization; valid tool calls can combine into unauthorized cross-context data flow.
- **Potential product/service (hypothesis):** Independent permission/data-flow review and recurring regression service for one agent workflow, with deterministic policy enforcement.
- **Potential monetization (untested):** Proposed assessment fee plus regression retainer; service-led enterprise sale.
- **Estimated technical / delivery difficulty:** Very high: adaptive threats, instrumentation and adversarial reliability.
- **Confidence:** Pain M; commercial M. Credible risk, limited direct buyer evidence, crowded market.
- **AI trajectory:** More capable agents increase permission risk; better models may reduce failures but do not replace authorization boundaries.
- **Next validation:** Interview 5 deployed-agent owners; only run scoped authorized synthetic-data assessments, compare existing controls.

<a id="p21"></a>
## P21 — CI-only browser flakes consume debugging time and erode test trust

- **Who / buyer:** Web engineering/QA teams; buyer: engineering manager.
- **Evidence:** Playwright report includes local-pass/CI-timeout logs; GROWI automated issue records retry success after visibility timeout, not a proven root cause. Sources: [1](https://github.com/microsoft/playwright/issues/34075) (S47); [2](https://github.com/growilabs/growi/issues/12031) (S48).
- **Frequency / severity:** Affected CI runs; reruns/intermittent blocking. No team-wide average cost inferred.
- **Current solutions:** Playwright traces/retries, screenshots, locator fixes, CI tuning and observability tools.
- **Why a gap may remain / counterevidence:** Retries hide symptoms; traces require environment/history correlation. Some intermittent failures are real regressions.
- **Potential product/service (hypothesis):** Trace-review service grouping signatures and proposing reproducible evidence-linked hypotheses; never automatically suppress tests.
- **Potential monetization (untested):** Proposed team subscription or CI add-on; must beat current assistants/observability.
- **Estimated technical / delivery difficulty:** High: traces, causal discrimination, repository security and longitudinal data.
- **Confidence:** Pain H; commercial M. Concrete repeated reports; commoditization high.
- **AI trajectory:** Agents inspect traces/fix tests; longitudinal evidence and validated fixes more durable than summarization.
- **Next validation:** Analyze 50 permitted failed runs against built-in traces and current coding-agent triage.

<a id="p22"></a>
## P22 — Security scanners disagree about affected dependency versions

- **Who / buyer:** AppSec/supply-chain teams; buyer: security lead.
- **Evidence:** Full issue follow-up identifies OSS Index source and closes the version-range report. Earlier comparison report historical. Not evidence of an unfixed current Dependency-Track defect. Sources: [1](https://github.com/DependencyTrack/dependency-track/issues/5319) (S49); [2](https://github.com/DependencyTrack/dependency-track/issues/2259) (S50).
- **Frequency / severity:** Scans/advisory updates; staff distraction plausible, actual impact unmeasured.
- **Current solutions:** Suppressions, advisory comparisons, upstream corrections and VEX workflows.
- **Why a gap may remain / counterevidence:** Package-identity/feed conflicts need defensible investigation; broad suppression creates security risk.
- **Potential product/service (hypothesis):** Evidence-linked advisory reconciliation comparing identity/ranges/provenance; propose reviewer-approved expiring dispositions.
- **Potential monetization (untested):** Proposed per-team retainer/integration; generic CVE explanations unlikely to command premium.
- **Estimated technical / delivery difficulty:** Very high: ecosystems, feeds, version logic and false-negative safety.
- **Confidence:** Pain H; commercial M. Technical evidence, fixed historical cases and incumbents.
- **AI trajectory:** AI collects/explains evidence, not declares safety from similarity. Deterministic ranges and timestamps required.
- **Next validation:** AppSec reviewers label resolved noisy findings; compare existing VEX/reachability tools and upstream fixes.

<a id="p23"></a>
## P23 — Offboarding needs proof across sessions, accounts, licenses and ownership

- **Who / buyer:** SMB IT/MSPs; buyer: IT manager or MSP.
- **Evidence:** Practitioners enumerate many tasks; others describe working scripts and identity provisioning. Complexity better evidenced than unmet need or incidents. Sources: [1](https://www.reddit.com/r/sysadmin/comments/170okqm/offboarding_process/) (S51); [2](https://www.reddit.com/r/sysadmin/comments/p6suth/how_do_you_guys_manage_provisioning_onoffboarding/) (S52).
- **Frequency / severity:** Each departure/contract end; missed-access exposure potentially serious, rate unknown.
- **Current solutions:** Identity provisioning, PowerShell, M365, tickets and SaaS-management tools.
- **Why a gap may remain / counterevidence:** Long-tail accounts/handover might escape automation, but that specific gap remains a hypothesis.
- **Potential product/service (hypothesis):** MSP-delivered verification with per-system evidence, unresolved items and approved ownership transfer.
- **Potential monetization (untested):** Proposed per-offboard fee or MSP bundle; generic checklist unlikely to justify spend.
- **Estimated technical / delivery difficulty:** High: discovery, permissions, integration upkeep and destructive-action safeguards.
- **Confidence:** Pain M; commercial L–M. Procedure discussion, working alternatives.
- **AI trajectory:** Agents discover clues and draft checks; deletion/transfer requires explicit scoped approval.
- **Next validation:** Audit 10 completed offboardings with permission; stop if identity tools cover meaningful gaps.

<a id="p24"></a>
## P24 — Hiring clients cannot separate real freelancers from generic/deceptive applications

- **Who / buyer:** Businesses hiring specialists; buyer: hiring manager.
- **Evidence:** Clients report applicant floods/suspicious experience and ask for project-specific or video responses. Fraud/identity/geographic allegations unverified; do not profile by region. Sources: [2](https://www.reddit.com/r/Upwork/comments/1oihf1b/any_other_clients_struggling_with_upwork_lately/) (S53); [1](https://www.reddit.com/r/Upwork/comments/1peb61i/upwork_used_to_be_good_now_it_a_cesspool_of_fake/) (S54).
- **Frequency / severity:** Each hiring round; repeated review/interview burden, validated fraud rate absent.
- **Current solutions:** Platform checks, work history, referrals, interviews and paid work samples.
- **Why a gap may remain / counterevidence:** Fluent prose/portfolios do not establish competence; video can be manipulated. Platform access/fairness constrain screening.
- **Potential product/service (hypothesis):** Accessible paid project-specific work-sample/reference-verification service with human evaluation, not AI-prose classification.
- **Potential monetization (untested):** Proposed $100–500/shortlist engagement, buyer-funded; compensate substantive candidate tasks.
- **Estimated technical / delivery difficulty:** High: valid assessment, privacy, accommodations and platform dependence.
- **Confidence:** Pain H; commercial M. Multiple buyer complaints, independent-service advantage unproven.
- **AI trajectory:** AI increases application volume; demonstrated reasoning/reference provenance matter more. Static tests face capable agents.
- **Next validation:** Interview 6 hiring clients; compare consented paid sample with interviews on effort, quality and candidate burden.

<a id="p25"></a>
## P25 — Craft creators struggle to document copied patterns across marketplaces

- **Who / buyer:** Pattern designers/visual creators; buyer: established seller or collective.
- **Evidence:** Knitter alleges copied pattern with AI-modified imagery; replies report removal. Other discussion distinguishes disclosed AI art from actual policy violations. No adjudicated infringement. Sources: [2](https://www.reddit.com/r/knitting/comments/1w2onru/my_free_design_on_ravelry_got_stolen/) (S55); [3](https://www.reddit.com/r/Etsy/comments/1kg786y/art_clearly_ai/) (S56).
- **Frequency / severity:** Reposts/relistings; ongoing monitoring plausible, revenue loss unverified.
- **Current solutions:** Reverse-image search, community tips, platform IP reporting and manual dossiers.
- **Why a gap may remain / counterevidence:** Modified imagery makes search harder; notices need rights and careful matching, not an AI detector.
- **Potential product/service (hypothesis):** Creator-controlled similarity monitoring with human-reviewed evidence and original publication links; no automatic accusations.
- **Potential monetization (untested):** Proposed collective funding or $10–30/month for commercial catalogs; free creators may not pay.
- **Estimated technical / delivery difficulty:** High: marketplace access, near duplicates, rights and false allegations.
- **Confidence:** Pain M–H; commercial L–M. Concrete but narrow sample.
- **AI trajectory:** AI cheapens copying and detection; provenance/rights checks more durable than classifying AI content.
- **Next validation:** Interview 8 designers/IP professional; inspect successful/failed notices and lawful monitoring access.

<a id="p26"></a>
## P26 — AI-authorship disputes lack fair process evidence

- **Who / buyer:** Students, schools/universities; buyer: institution.
- **Evidence:** Parent reports grades reduced after detector screenshots. Jisc 2026 says detection improving but mixed authorship/model changes complicate judgment; blanket useless-detector claims unsupported. Sources: [2](https://www.reddit.com/r/Parenting/comments/1npbirw/teen_falsely_accused_of_using_ai/) (S57); [3](https://nationalcentreforai.jiscinvolve.org/wp/2026/10/15/ai-detection-and-assessment-an-update-for-2026/) (S58).
- **Frequency / severity:** Contested assignments; consequential for grades/trust. Representative false-accusation rate absent.
- **Current solutions:** Detectors, drafts/version history, oral defense and assessment redesign.
- **Why a gap may remain / counterevidence:** Final-text probability is not proof of prohibited assistance; histories incomplete/stageable. Surveillance and accessibility burdens matter.
- **Potential product/service (hypothesis):** Institutional appeal/process workflow: optional draft provenance, AI-use declarations, oral-explanation rubric and human decision record; never certify authorship.
- **Potential monetization (untested):** Proposed institution license/training service; do not charge accused students to prove innocence.
- **Estimated technical / delivery difficulty:** High: LMS/docs integration, privacy, pedagogical validity and contestability.
- **Confidence:** Pain H; commercial M. Specific allegation and sector analysis, process tools already emerging.
- **AI trajectory:** Co-creation shifts value toward permitted process/demonstrated understanding. Better detection may reduce, not settle, disputes.
- **Next validation:** Interview integrity staff/student representatives; test fair appeal process on anonymized cases before monitoring.

<a id="p27"></a>
## P27 — Familiar voices no longer authenticate emergency money requests

- **Who / buyer:** Older adults/families; buyer: family, bank or senior-support sponsor.
- **Evidence:** FTC warns cloned voices can support emergency scams and advises callbacks. Reddit silent-call cloning speculation is rebutted as possible autodialer, not accepted incident proof. Sources: [1](https://consumer.ftc.gov/consumer-alerts/2023/03/scammers-use-ai-enhance-their-family-emergency-schemes) (S59); [3](https://www.reddit.com/r/Scams/comments/1fx2i5w/ai_voice_cloning_scam/) (S60).
- **Frequency / severity:** Possibly rare but high-stakes; no verified incidence/loss statistics here.
- **Current solutions:** Known-number callback, family verification plan, education, call screening and bank controls.
- **Why a gap may remain / counterevidence:** Panic defeats remembered advice; acoustic detectors unreliable/unavailable. Free callback habits already address much need.
- **Potential product/service (hypothesis):** Sponsor-funded verification setup/rehearsal with known-contact tree and independent-channel confirmation, not a perfect voice-clone detector.
- **Potential monetization (untested):** Proposed bank sponsorship or one-time family setup; household subscription weak.
- **Estimated technical / delivery difficulty:** Medium workflow; very high if real-time deepfake detection promised, which is not recommended.
- **Confidence:** Pain M–H; commercial L. Official warning, weak direct paid demand.
- **AI trajectory:** Better synthesis increases ambiguity; authentication should use independent channels, not synthetic-artifact detection.
- **Next validation:** Senior-support partner evaluates comprehension/rehearsal against free callback education.

<a id="p28"></a>
## P28 — Home sewists waste effort assembling or mis-scaling PDF patterns

- **Who / buyer:** Home sewists/pattern designers; buyer: hobbyist or publisher.
- **Evidence:** Users describe taping/printing frustration and projector tradeoffs. Recent poster reports oversized test square; replies explain reader/scaling/paper settings. Sources: [1](https://www.reddit.com/r/sewing/comments/1b5sg3p/i_hate_pdf_patterns/) (S61); [3](https://www.reddit.com/r/sewing/comments/1q37odk/pdf_pattern_help/) (S62).
- **Frequency / severity:** Each pattern; mis-scaled cutting wastes fabric/time. Failure rate unmeasured.
- **Current solutions:** Exact-scale Acrobat printing, A0 shops, tracing, projectors and vector editors.
- **Why a gap may remain / counterevidence:** Printer/paper settings vary; projector calibration/sizing add barriers. Simple instructions work for many.
- **Potential product/service (hypothesis):** Guided print/projection preflight bundled with pattern sales, verifying test square before full cut/print.
- **Potential monetization (untested):** Proposed one-time utility or publisher license; weak recurring household value.
- **Estimated technical / delivery difficulty:** Medium: PDF geometry/device workflows; body-fit prediction separate and harder.
- **Confidence:** Pain H; commercial L–M. Direct recurring-task complaints, free/cheap substitutes.
- **AI trajectory:** Vision might verify calibration with known reference; deterministic scale checks matter more than generated advice.
- **Next validation:** Observe 10 setups; compare improved instructions alone and ask publishers about support savings.

<a id="p29"></a>
## P29 — Home bakers struggle to keep recipe costs current with prices and labor

- **Who / buyer:** Cottage-food bakers; buyer: owner.
- **Evidence:** Bakers recommend spreadsheets, CakeBoss/CakeCost. Seller claims re-entry pain while promoting calculator; low-weight promotional evidence, not independent demand. Sources: [3](https://www.reddit.com/r/AskBaking/comments/xa2gak/profit_from_home_bakery/) (S63); [1](https://www.reddit.com/r/cottage_industry/comments/1lf07mu/i_built_a_bakery_pricing_spreadsheet_that_finally/) (S64).
- **Frequency / severity:** Recipes, price updates, quotes; potential underpricing, no measured margin loss.
- **Current solutions:** Shared ingredient spreadsheets, CakeBoss, CakeCost and bookkeeping/POS.
- **Why a gap may remain / counterevidence:** Plausible gap is setup, conversions, yield and labor/packaging, not missing arithmetic. Existing databases already solve much.
- **Potential product/service (hypothesis):** Assisted costing setup and receipt-price refresh for narrow bakery type; no unqualified tax/food-law advice.
- **Potential monetization (untested):** Proposed $50–200 setup plus optional review, not assumed subscription.
- **Estimated technical / delivery difficulty:** Medium: receipt/units need checking; training dominates.
- **Confidence:** Pain M; commercial L. Existing solutions praised, older/promotional evidence.
- **AI trajectory:** AI lowers receipt entry but cannot know wastage/labor or clearing price. Commodity AI could erase software wedge.
- **Next validation:** Inspect 6 bakers’ tools; stop if one-hour spreadsheet training suffices.

<a id="p30"></a>
## P30 — Tenancy deposit disputes lack comparable inspection evidence

- **Who / buyer:** Renters/small property managers; buyer: manager or tenant-support partner.
- **Evidence:** Managers recommend before/after photos, invoices and forms; tenants report photos helping recover deductions. Allegations/outcomes not independently adjudicated. Sources: [2](https://www.reddit.com/r/PropertyManagement/comments/1pwjerb/new_property_manager_here_what_do_you_include_in/) (S65); [3](https://www.reddit.com/r/madisonwi/comments/1mpgnay/mpm_security_deposit/) (S66).
- **Frequency / severity:** Each turnover; significant to affected tenants, prevalence unknown.
- **Current solutions:** Phone photos, checklists, Leonardo 24/7, inspection systems, tenant advice/courts.
- **Why a gap may remain / counterevidence:** Unmatched angles/missing dates/scattered invoices hinder comparison. Photos cannot decide ordinary wear or lawful deductions.
- **Potential product/service (hypothesis):** Guided matched-room capture and neutral dossier linking inspections/invoices/disputes; qualified local legal partners only.
- **Potential monetization (untested):** Proposed per-turnover fee or sponsored tenant tool; renter subscription weak.
- **Estimated technical / delivery difficulty:** Medium–high: image alignment, authenticity, storage and jurisdiction boundaries.
- **Confidence:** Pain H; commercial M. Both sides evidence need, established tools may suffice.
- **AI trajectory:** Vision aligns/flags changes for review, never assigns liability. Synthetic photos increase provenance need.
- **Next validation:** Compare 20 turnovers to current inspection tools; involve tenant advocates to prevent biased automated deductions.

<a id="p31"></a>
## P31 — Noise-sensitive diners cannot predict usable venues by time and table

- **Who / buyer:** People with hearing/auditory-processing/sensory sensitivities; buyer: diner, venue or accessibility sponsor.
- **Evidence:** App/Play reviews praise discovery but complain about accuracy, stale/sparse data and usability. Local diner asks for quiet places. Current Play release notes claim search/estimated-level improvements; old complaints may be partly fixed. Sources: [2](https://apps.apple.com/us/app/soundprint-find-a-quiet-place/id971189322?see-all=reviews) (S67); [1](https://play.google.com/store/apps/details/?id=com.soundprint&hl=en-GB) (S68); [2](https://www.reddit.com/r/Cleveland/comments/1tyknv6/best_quiet_restaurant_in_lakewood_area/) (S69).
- **Frequency / severity:** Every outing; may lead to abandoned meals/social plans. Willingness to pay unestablished.
- **Current solutions:** SoundPrint, local advice, off-peak visits, patios and mainstream reviews.
- **Why a gap may remain / counterevidence:** Time/table/crowd variability and device/tolerance differences defeat a single average. Dense trusted local coverage is hard.
- **Potential product/service (hypothesis):** Venue-confirmed quiet seating/slots with recent user verification, starting one city; publish uncertainty, not inferred precise decibels.
- **Potential monetization (untested):** Proposed sponsor funding or disclosed venue verification fee; paid placement must not influence assessments.
- **Estimated technical / delivery difficulty:** High operations/data difficulty, moderate app difficulty.
- **Confidence:** Pain H; commercial L–M. Cross-platform direct reviews, positive incumbent evidence, network challenge.
- **AI trajectory:** AI extracts sensory clues/freshness, not actual sound. Existing estimated-level features reduce novelty.
- **Next validation:** Interview 10 diners/5 venues; compare verified slots with SoundPrint/free local advice without building app.

<a id="p32"></a>
## P32 — Occasional groups dislike subscription economics for expense splitting

- **Who / buyer:** Travel/family groups and roommates; buyer: trip organizer.
- **Evidence:** Trustpilot complaints describe caps/delays and poor annual value for occasional use; positive travel reviews also present. Exact current entitlements not independently verified. Sources: [1](https://www.trustpilot.com/review/splitwise.com) (S70).
- **Frequency / severity:** Bursty trips or ongoing roommates; annoyance, not generally high-severity loss.
- **Current solutions:** Splitwise free/Pro, Tricount, Sheets and other split apps.
- **Why a gap may remain / counterevidence:** Annual/per-person pricing may mismatch usage. Preference for free alternatives is negative paid-demand evidence.
- **Potential product/service (hypothesis):** Per-trip receipt reconciliation/group closeout service; do not build generic splitter just because people dislike paywalls.
- **Potential monetization (untested):** Proposed small organizer-paid trip fee; low confidence against free alternatives.
- **Estimated technical / delivery difficulty:** Low–medium ledger; receipts/currency raise difficulty, payment custody adds regulation and is excluded.
- **Confidence:** Pain H as annoyance; commercial L. Review-selection bias/price resistance dominate.
- **AI trajectory:** AI itemization commoditizes; incumbents can add it. Avoid custody.
- **Next validation:** Ask 10 organizers to choose a real trip fee versus free Tricount/Sheets; stop if they only want free.
