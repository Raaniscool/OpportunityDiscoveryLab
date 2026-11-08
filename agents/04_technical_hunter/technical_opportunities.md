# 23 Technical Opportunities for Arena

**Research date:** 2026-11-08
**Ranking:** ordered by near-term customer pain, technical evidence, fit with Arena's coding-agent workflow, differentiation, and implementation risk. This is a reasoned priority order, not a measured market-size ranking. Complexity is rough effort for a credible first paid MVP: **S** ≤2 engineer-months, **M** 3–5, **L** 6–12, **XL** >12 or a substantial platform/operations investment. It excludes sales and provider approval delays.

Competitor/alternative lists are deliberately described as **adjacent tools/categories**, not exhaustive or independently validated competitive analyses. Source identifiers resolve in [research_sources.md](research_sources.md).

## Priority ranking at a glance

| Rank | Opportunity | Why it matters | Complexity |
|---:|---|---|---|
| 1 | AppProof: release verification for AI-built apps | Directly addresses “it generated code, but does it work?” | L |
| 2 | Preview Branch Lab: per-change full-stack isolation | Concrete path using deployment and database-branch primitives | M–L |
| 3 | App Capsules: managed runtime for user-owned apps | Strong long-term platform control point; high infra burden | XL |
| 4 | App Steward: ongoing maintenance for generated software | Recurring revenue after the first deploy | L |
| 5 | Roblox Creator CI | Unexpectedly concrete engine-level test/publish API | M |
| 6 | MCP Permission Router | Enterprise governance for tool-using agents | XL |
| 7 | Agent Workflow Benchmark Lab | Buyers need measured reliability on their own workflows | L |
| 8 | MCP Compatibility Monitor | Continuous integration health for a changing tool ecosystem | M |
| 9 | API Connector Compiler | Turn documented APIs into constrained agent capabilities | L |
| 10 | Trace-to-Repro Debug Loop | Convert failed agent/app runs into reviewable fixes | L |
| 11–23 | Remaining vertical and platform bets | Good options after the lifecycle foundation | M–XL |

---

## 01 — AppProof: release verification for AI-built apps

- **Product / problem:** A release gate that converts a user's requirements into editable acceptance checks, builds a preview, tests core user journeys, and returns evidence. It closes the gap between generated output and demonstrated behavior.
- **Technology / competitors:** Playwright Test, accessibility snapshots, API assertions, screenshots, and Trace Viewer artifacts; use Stagehand-like natural-language steps only for uncertain transitions. Adjacent alternatives include Playwright, Stagehand, BrowserStack, and QA-as-a-service vendors.[S01][S02][S03][S05]
- **Feasibility / limits:** Browser traces and test runners are real documented capabilities, but Arena's current sandbox has no installed browser or interactive browser tool. Tests need a remote worker/CI runner. Generated tests need a deterministic oracle; a screenshot similarity score alone cannot prove business correctness.
- **Arena implementation:** Let the user confirm acceptance criteria; generate deterministic test code; deploy to a disposable URL; run tests with isolated credentials; attach trace, screenshots, app commit, and test version; require approval on ambiguous results.
- **Complexity:** **L**. Browser fleet, test flake management, security boundaries, and evidence UX are the hard parts.
- **Customers / monetization:** AI-assisted development teams, app studios, SMBs, and agencies; per app/repository plus metered test/preview runs.
- **Long-term potential:** Becomes the quality/evidence substrate for maintenance, safe migrations, model comparison, and deployment approval. This is the best initial product wedge.

## 02 — Preview Branch Lab: one full-stack preview per change

- **Product / problem:** A PR/agent-edit creates an isolated app deployment and matching database branch, with synthetic seed data and a shareable review link. It avoids testing against production or waiting on shared staging.
- **Technology / competitors:** Vercel deployment creation plus Supabase Branching; Vercel reports deployment readiness/error, while Supabase branches are isolated and data-less by default and can receive migrations, seed data, and Edge Functions.[S08][S09] Direct adjacent alternatives are Vercel previews, Supabase previews, and other hosted preview environments.
- **Feasibility / limits:** Strongly grounded in public APIs and in the Vercel/Supabase connector schemas available to this session, but not executed here. Supabase branch eligibility/plan limits and database behavior must be checked. Vercel's current Arena connector schema lacks some first-deployment bootstrap controls, so projects need an initialized setup or alternate path. Synthetic data and cleanup are required.
- **Arena implementation:** Add a preview orchestrator that maps a source commit to deployment ID, branch DB URL, migration status, test result, TTL/cleanup, and human promotion. Keep production data and secrets out of previews.
- **Complexity:** **M–L**; provider-specific setup, identity, quota, and teardown determine the upper end.
- **Customers / monetization:** Product teams using coding agents, agencies, and internal app teams; per active preview minute/branch or workspace tier.
- **Long-term potential:** The substrate for AppProof and App Steward; likely the fastest practical companion to #1.

## 03 — App Capsules: managed runtime for user-owned apps

- **Product / problem:** A deployable package for each generated app with hosting, database, secret references, logs, backups, rollback, usage limits, export, and a stable URL. Users should not have to understand a full cloud control plane to keep a useful app running.
- **Technology / competitors:** Compose Vercel-style deployment APIs, Supabase branches/services, container/microVM execution such as Cloudflare Sandboxes or E2B, and optionally durable orchestration for long-running actions.[S06][S07][S08][S09][S23] Adjacent alternatives include Vercel, Cloudflare, E2B, and managed app builders.
- **Feasibility / limits:** Each underlying primitive exists; the difficult product is secure multi-tenancy, authorization, network egress, billing, abuse handling, durable storage, recovery, and migrations. A session coding sandbox is not a production tenant runtime.
- **Arena implementation:** Start as a control plane delegating to user-owned Vercel/Supabase projects. Only later consider a hosted worker/sandbox tier with per-app identity, hard resource quotas, egress controls, encrypted secret references, logs, backup/export, and teardown.
- **Complexity:** **XL**.
- **Customers / monetization:** Individuals, consultants, small businesses, and agencies with one-off internal tools; per active app plus compute/database usage.
- **Long-term potential:** Strategic platform bet: a catalog of user-owned, maintainable apps with recurring subscriptions and portability. Do not begin by promising “unlimited free hosting.”

## 04 — App Steward: maintenance subscriptions for generated apps

- **Product / problem:** Monitor a deployed app and its dependencies, run smoke tests/backups, flag broken APIs and schema drift, draft safe upgrades, and prepare rollback-ready repair PRs. The buyer's app works today but is at risk of becoming abandoned.
- **Technology / competitors:** Scheduled workflows (Temporal-like durable execution when needed), dependency scanners, Playwright/API smoke tests, traces, and repository/deployment connectors.[S02][S23][S26][S27] Adjacent alternatives include Dependabot/Renovate for updates, observability tools, and managed maintenance agencies.
- **Feasibility / limits:** A monitor + human-reviewed repair PR is feasible with repository, test, and deployment integrations. Unattended production edits are not: app-specific meaning, expired credentials, breaking migrations, and external API changes defeat generic repair.
- **Arena implementation:** Offer daily/weekly checks; open a repair plan with impacted file, failing test, dependency advisory, and rollback; require approval to merge/deploy; include a “pause maintenance” and export option.
- **Complexity:** **L**.
- **Customers / monetization:** SMBs, agencies, and non-specialist owners of custom apps; per maintained app/month, with higher service tier for faster response.
- **Long-term potential:** Strong recurring revenue and retention if AppProof creates trustworthy baselines. This is a follow-on, not a first feature.

## 05 — Roblox Creator CI: generate, test, and safely publish places

- **Product / problem:** A creator-facing pipeline that builds a Rojo-managed Roblox place, lints/formats Luau, runs engine-level tests against an isolated place/version, captures logs, and promotes only after an explicit approval.
- **Technology / competitors:** Rojo, Roblox Open Cloud Luau Execution, place/asset publishing API, GitHub Actions, Selene/StyLua-style tooling, and Roblox DataModel assertions. Roblox's current docs describe headless Luau execution with logs and results; the API page labels endpoints Stable, caps tasks at five minutes and ten concurrent tasks per place, and documents asynchronous publish operations.[S39][S40][S41][S42] Alternatives include Roblox Studio workflows and creator-built CI scripts.
- **Feasibility / limits:** Unusually well grounded. It can test server-side engine behavior and DataModel interactions but not all client visuals, rendering, network latency, or player experience. The official sample pipeline is archived, warns it is not battle-tested, and requires narrowly scoped Open Cloud keys; use its architecture, not its implementation as production code. Publishing has unsupported instance types.
- **Arena implementation:** Create a Roblox-specific repo template, lint/build/test job, isolated test place, Open Cloud task polling/log collection, signed result artifact, and human-gated publish action. Keep production publish credentials separate from test credentials.
- **Complexity:** **M** for a creator CI product; substantially larger if Arena also hosts game builds or a creator marketplace.
- **Customers / monetization:** Roblox solo creators, small studios, and UGC development teams; subscription per place/team plus execution minutes.
- **Long-term potential:** A focused route into engine-aware agent development and automated balancing/content workflows. Potentially a strong differentiated vertical, pending creator interviews and API access tests.

## 06 — MCP Permission Router: a broker between agents and tools

- **Product / problem:** One controlled gateway that discovers MCP servers/tools, issues narrowly scoped grants, requests approvals for sensitive calls, records redacted audit events, and revokes access.
- **Technology / competitors:** MCP authorization, tool discovery, registry/Inspector, OAuth scopes, policy engine, per-tenant token vault, and pre-tool permission hooks such as those demonstrated by agent SDKs.[S10][S11][S12][S13][S14][S15][S18] Adjacent alternatives include model/agent SDK allowlists and open-source MCP gateways.
- **Feasibility / limits:** Protocol pieces are documented; a trustworthy credential broker requires security engineering, threat modeling, isolation, token rotation, consent UX, incident response, and safe logging. A prompt-level instruction is not an authorization boundary.
- **Arena implementation:** First implement a local or single-tenant broker with explicit tool manifests, allow/deny rules, user approval, short-lived credentials, redaction, and audit export. Do not proxy broad production credentials through a general-purpose coding agent.
- **Complexity:** **XL** for an enterprise-grade gateway; **M** for a narrow single-tenant prototype.
- **Customers / monetization:** Enterprises and SaaS teams enabling agents to use internal tools; per seat, connected server, or governed tool-call volume.
- **Long-term potential:** Could be a core control plane across Arena-built apps and integrations. Security reputation is a gating asset, not an afterthought.

## 07 — Agent Workflow Benchmark Lab

- **Product / problem:** A private, repeatable test suite for an organization's own browser/desktop workflows. Run candidate agent/model versions against seeded tasks and score successful outcomes, harmful side effects, steps, latency, and cost.
- **Technology / competitors:** BrowserGym, WorkArena, deterministic backend graders, screenshots/accessibility trees, and Langfuse-style datasets/experiments.[S26][S46][S47] Adjacent alternatives are open evaluation frameworks and LLM evaluation/observability platforms.
- **Feasibility / limits:** Benchmarks demonstrate how to represent tasks and score outcomes, but every customer needs an environment, fixtures, and domain-specific grader. Some open benchmark stacks require large Docker environments; Arena currently lacks Docker and a browser. A benchmark score is not a guarantee of production reliability.
- **Arena implementation:** Import 5–20 customer workflows, generate a resettable test environment or safe staging copy, define observable completion conditions, replay model/tool versions, and publish a regression comparison with trace artifacts.
- **Complexity:** **L**.
- **Customers / monetization:** Enterprise AI/platform teams, automation vendors, and internal IT; subscription by workflow pack plus evaluation-run usage.
- **Long-term potential:** Generates reusable regression data and is a natural bridge from AppProof to governed autonomous agents.

## 08 — MCP Compatibility Monitor

- **Product / problem:** A CI/hosted service that continuously probes a fleet of MCP servers for changed tool schemas, broken auth, invalid results, missing capabilities, and policy mismatches.
- **Technology / competitors:** MCP Registry discovery, Inspector protocol tests, schema validation, contract snapshots, OAuth checks, and change alerts.[S12][S13][S14][S15] Adjacent tools include the open Inspector and hand-built contract tests.
- **Feasibility / limits:** Inspecting/listing/calling tools is documented. Continuous probing of a user's production server needs authorized test accounts and safe, non-mutating calls; MCP servers may be local, private, or inaccessible to a hosted scanner.
- **Arena implementation:** Start with opt-in servers that expose a health/conformance endpoint; snapshot schemas, test tools against declared fixtures, run permission lint, and require explicit approval before any mutating call.
- **Complexity:** **M**.
- **Customers / monetization:** MCP server publishers, agent-platform teams, and enterprises with many connections; paid server inventory/CI seats and monitoring frequency.
- **Long-term potential:** Could become a trusted “continuous integration for agent capabilities” layer if MCP adoption and tool churn continue.

## 09 — API Connector Compiler: OpenAPI to constrained agent tools

- **Product / problem:** Parse OpenAPI, generate a typed client and carefully scoped agent-facing tool catalog, document operations, build mock tests, and surface OAuth scopes for human review.
- **Technology / competitors:** OpenAPI contracts, code generation, JSON Schema validation, MCP tool definitions, API mocks, and secret vault references.[S10][S13][S19] Alternatives include OpenAPI Generator, custom SDKs, and hand-written MCP wrappers.
- **Feasibility / limits:** OpenAPI is designed for machine-readable API discovery/code generation, but many specs are incomplete or wrong; schemas do not reveal business intent, safe idempotency, or permission policy. Generated connector code still needs validation and vendor API access.
- **Arena implementation:** Import spec; classify read/write/destructive operations; generate calls, test fixtures, and tool descriptions; require an owner to assign scopes and approvals; store secrets outside prompts and generated repositories.
- **Complexity:** **L** for a secure hosted integration product; **M** for a single-spec developer tool.
- **Customers / monetization:** SaaS API teams, integration consultants, internal platform teams, and agent builders; per connector or API-call volume.
- **Long-term potential:** A way to make API-first interaction more reliable than UI-only browsing, while feeding the MCP catalog and permission router.

## 10 — Trace-to-Repro Debug Loop

- **Product / problem:** Turn an app or agent failure into a reproducible case with steps, environment, redacted network/error context, then propose a code change and regression test.
- **Technology / competitors:** Playwright traces, OTel spans, OBI where compatible, GenAI semantic conventions, Langfuse datasets, and repository branches.[S02][S24][S25][S26] Adjacent alternatives include Sentry/observability platforms and AI coding agents.
- **Feasibility / limits:** Trace capture and experiment replay are real capabilities. Reproduction can fail when data, timing, cookies, or external APIs differ; traces can contain sensitive tokens or personal information. Root-cause suggestions are probabilistic.
- **Arena implementation:** Capture a minimal, redacted replay fixture; reconstruct against a fresh branch; ask an agent for hypotheses; verify with a failing test; submit an optional repair PR with original trace and verification result.
- **Complexity:** **L**.
- **Customers / monetization:** Software teams and AI product developers; per event volume/seat or incident-response tier.
- **Long-term potential:** Creates a closed loop between live behavior, durable tests, and maintenance, especially valuable for software produced by agents.

## 11 — Build provenance and software supply-chain evidence

- **Product / problem:** For every generated release, attach an SBOM, dependency findings, build identity/provenance, policy results, and human-readable limitations.
- **Technology / competitors:** OSV version/commit queries, GitHub artifact attestations, SLSA provenance, and package lockfiles.[S27][S28][S29] Adjacent alternatives include GitHub security features and dedicated supply-chain/security scanners.
- **Feasibility / limits:** Public APIs and formats exist. A clean attestation only establishes properties of the build/source; it does not prove the application is bug-free, secure, or free of malicious behavior. Private repository attestation access depends on GitHub plan/permissions.[S28]
- **Arena implementation:** Run package/lockfile scan, generate SBOM and provenance in CI, bind reports to the deployed digest, show false-positive/coverage caveats, and allow customers to export the artifact bundle.
- **Complexity:** **M** for a focused integration; **L** for policy management, private-repo support, and multiple providers.
- **Customers / monetization:** Regulated SMBs, agencies, enterprise procurement, and generated-app operators; per repo/build or paid compliance-report tier.
- **Long-term potential:** Trust differentiation and procurement enablement; position as transparent evidence, never as a universal security certification.

## 12 — Browser task runner with approvals and replay

- **Product / problem:** A user asks for a multi-step web task; Arena executes through a persistent but isolated browser profile, pauses before sensitive actions, and returns a replayable record.
- **Technology / competitors:** Playwright MCP, Stagehand hybrid APIs, OpenAI computer-use tool loops, browser profiles, short-lived sessions, and policy hooks.[S01][S04][S05][S17][S18]
- **Feasibility / limits:** Browser automation can be built, but this session does not expose an interactive browser and has no browser binary. The product additionally needs remote session capacity, secure login/2FA, anti-bot handling, personal-data controls, and user-visible approval. Untrusted page content can manipulate an agent.
- **Arena implementation:** Start with a narrow allowlisted site/workflow; separate read-only from write actions; require confirmation before sending/purchasing/deleting; redact screenshots; provide stop/revoke, replay, and account logout.
- **Complexity:** **XL** for a consumer/general web agent; **L** for one controlled workflow.
- **Customers / monetization:** Small business operators and knowledge workers; per seat/task or workflow pack.
- **Long-term potential:** A broad use case, but higher reliability, legal, privacy, and platform-policy risk than AppProof. Prefer API integrations where available.

## 13 — Local-first AI app shell

- **Product / problem:** Generated mini-apps keep structured records and run selected inference locally, making private/offline tools usable with fewer hosted-server costs.
- **Technology / competitors:** PGlite in WebAssembly with IndexedDB persistence, ONNX Runtime Web via WASM/WebGPU, and a conventional web app shell.[S20][S21]
- **Feasibility / limits:** The primitives are documented. Device memory, WebGPU/operator support, model size, browser quotas, offline sync, conflict resolution, encryption, and backup vary. PGlite in a browser is not a hosted multi-tenant Postgres service.
- **Arena implementation:** Offer as an explicit app template: local database, export/backup, optional sync target, small supported models, device compatibility check, and a clearly labeled “data stays on this device” mode.
- **Complexity:** **M–L**.
- **Customers / monetization:** Privacy-conscious professionals, field staff, consultants, and offline environments; template/app subscription or managed sync add-on.
- **Long-term potential:** Differentiates Arena for privacy-sensitive use cases and can reduce inference/data costs if the workload fits local devices.

## 14 — Database migration rehearsal and recovery lab

- **Product / problem:** Before deploying an app change, create an isolated DB branch, run migrations and seed scripts, test rollback/restore assumptions, and report data loss/lock risk.
- **Technology / competitors:** Supabase Branching, migration files, temporary test data, SQL diffs, deployment status, and backup/export workflows.[S08][S09]
- **Feasibility / limits:** Supabase documents branch-per-change workflows, but branches are data-less by default and production-data cloning needs separate privacy, performance, and plan analysis. SQL success does not prove every real dataset or application query still works.
- **Arena implementation:** Diff schema; seed synthetic representative data; apply migration on branch; run generated invariants/API tests; produce rollback/forward-fix scripts; block automatic production migration until approval.
- **Complexity:** **L**.
- **Customers / monetization:** Teams using Postgres-backed custom applications and agencies; per project/branch or paid migration run.
- **Long-term potential:** High-trust core capability for App Steward and AppProof; may reduce the most damaging class of generated-app failures.

## 15 — WASI extension runtime for user-created plugins

- **Product / problem:** Let users extend an app with constrained, auditable modules rather than arbitrary host-language scripts with full process/filesystem access.
- **Technology / competitors:** Wasmtime Component Model, WASI interfaces, explicit host capabilities, and optional plugin frameworks such as Extism.[S22]
- **Feasibility / limits:** Sandboxed components can receive only granted resources, but correct host design, CPU/memory/time quotas, package provenance, denial-of-service controls, and ABI/version policy are still required. A WebAssembly boundary alone is not a security certification.
- **Arena implementation:** Prototype a single deterministic extension interface (e.g. transform data or validate records); allow read-only inputs and bounded outputs; pin component digest; log calls; prohibit network/file access unless separately granted.
- **Complexity:** **XL** for a general plugin ecosystem; **M** for one narrow extension hook.
- **Customers / monetization:** SaaS makers and advanced users; paid extension runs, professional plugin hosting, or marketplace share.
- **Long-term potential:** A safer user customization layer across App Capsules, but depends on adoption and robust capability design.

## 16 — Agent Flight Recorder and replay

- **Product / problem:** Store a redacted, time-ordered record of prompts, tool calls, approvals, results, and traces so operators can explain or reproduce a failed/high-risk action.
- **Technology / competitors:** OpenTelemetry GenAI conventions, OBI for supported workloads, Langfuse traces/experiments, and immutable object storage.[S24][S25][S26]
- **Feasibility / limits:** Telemetry standards and platforms exist, but capturing full tool input/output creates privacy and secret leakage risk. Replay against live systems can repeat destructive actions; use fixture data and deny writes by default.
- **Arena implementation:** Define an event schema, automatic secret/PII redaction, per-tenant retention, export/deletion, approval events, and safe replay with mocked tools. Add provenance for policy and agent versions.
- **Complexity:** **M–L**.
- **Customers / monetization:** Enterprise agent operators, support teams, and regulated organizations; per trace volume/retention or compliance tier.
- **Long-term potential:** Foundation for audits, debugging, agent benchmarking, and safer upgrades.

## 17 — Verified app/template marketplace

- **Product / problem:** Users publish and license reusable mini-apps, connectors, or workflow templates; each listing includes permissions, dependencies, test coverage, data model, and compatibility results.
- **Technology / competitors:** App Capsules, signed build provenance, sandboxed extensions, AppProof reports, and Stripe Connect for seller onboarding/payouts.[S22][S28][S29][S45] Adjacent alternatives include app/plugin marketplaces and template galleries.
- **Feasibility / limits:** Technically feasible only after identity, runtime isolation, review/moderation, versioning, support, refunds, and abuse processes exist. Stripe notes that a marketplace platform can be merchant of record, pay Stripe/Connect fees, and manage refunds/disputes/negative balances.[S45]
- **Arena implementation:** Begin with curated, non-executable templates; display declared permissions and reproducible verification artifacts; later permit paid executable apps after safety/ownership review.
- **Complexity:** **XL**.
- **Customers / monetization:** Independent creators, agencies, and small businesses; seller subscription plus transaction commission. Economics require interviews and legal review.
- **Long-term potential:** Ecosystem/network effects if users build valuable reusable apps, but a weak starting point without supply, demand, and trust.

## 18 — Windows workflow automation with UI Automation

- **Product / problem:** Automate a narrow, repetitive line-of-business workflow in desktop software lacking a usable API; rely on accessibility/UI Automation selectors instead of screen coordinates when possible.
- **Technology / competitors:** Windows UI Automation, UIA/MSAA selector patterns, Power Automate Desktop, and an approval-capable agent host.[S33][S34][S18]
- **Feasibility / limits:** Microsoft documents the automation interfaces, but Arena's current environment is Linux and has no Windows desktop-control tool. Remote Windows workers, licensing, interactive sessions, application-specific selectors, and manual exception handling are essential. Coordinate-only computer use is fragile.
- **Arena implementation:** Partner or run customer-hosted Windows workers; start with one approved app/workflow; use UIA selectors; log each action; stop before payments/deletions; test against a resettable account.
- **Complexity:** **XL** for a general service; **M–L** for one customer-hosted workflow.
- **Customers / monetization:** Back-office teams with legacy Windows software, especially where manual work is high-volume; per attended desktop/seat or workflow deployment.
- **Long-term potential:** Strong vertical value but poor fit for an unproven Linux-only sandbox; only pursue with a clear design partner.

## 19 — Mobile build, UI test, and release lane

- **Product / problem:** Generate or update a Capacitor app, build native artifacts, test on emulators/devices, and release signed APK/AAB/IPA through an approved pipeline.
- **Technology / competitors:** Capacitor CLI build/signing, Maestro declarative UI tests, Android ADB/emulators, and managed device farms.[S35][S36]
- **Feasibility / limits:** Build/sign commands and UI testing are documented; release requires native toolchains, signing certificates, provisioning profiles, secure keystore storage, and app-store account workflows. Arena's present container has no mobile device farm or signing keys.
- **Arena implementation:** Start with Android debug builds and a test device provider; use secret vault references; automate signing only with user-controlled credentials; require confirmation for store submission.
- **Complexity:** **M–L** for a focused Android flow, **XL** for reliable iOS/Android device coverage and stores.
- **Customers / monetization:** Agencies, indie developers, and teams making internal mobile apps; per build/device-minute/project tier.
- **Long-term potential:** Natural extension of App Capsules if users ask for native distribution; not an MVP before web app proof.

## 20 — Unity/Unreal automated game verification farm

- **Product / problem:** Build game changes, run engine tests and packaged-game smoke tests, capture logs/crash reports, and report reproducible failures to game teams.
- **Technology / competitors:** Unity Test Framework batch mode, Unreal Gauntlet/RunUAT, game build agents, and platform-specific device automation.[S37][S38]
- **Feasibility / limits:** Both engines document command-line test paths. Engine installs, asset-heavy builds, licensing, GPUs, platform SDKs, console/mobile devices, nondeterminism, and artifact size make execution expensive. Headless tests do not prove player feel or visual quality.
- **Arena implementation:** Begin with one engine and one platform; integrate self-hosted/customer workers; build tests from project conventions; attach logs/screenshots/crash dump metadata; require licenses and device permissions to be managed by the customer.
- **Complexity:** **XL** for a multi-engine hosted farm; **L** for one managed CI adapter.
- **Customers / monetization:** Indie and mid-size game studios, tools teams, and outsourcing QA; per runner-hour, project, or seat.
- **Long-term potential:** High-value specialist infrastructure but crowded/operationally heavy; Roblox is the more bounded first game vertical.

## 21 — Accessibility contract and repair verification

- **Product / problem:** Add automated accessibility checks to every generated app, suggest fixes, and preserve keyboard/screen-reader expectations in regression tests.
- **Technology / competitors:** axe-core browser rules, accessible-name locators, keyboard navigation tests, and manual assistive-technology review.[S01][S30]
- **Feasibility / limits:** Automated scanning catches a useful subset; axe-core explicitly says automated checks miss many issues. No automated green badge can certify full WCAG conformance. Browser execution is a current Arena gap.
- **Arena implementation:** Run axe-core on each key page; expose rule IDs, affected elements, remediation suggestions, keyboard path tests, and “manual review required” flags; never claim legal certification.
- **Complexity:** **M** as an AppProof extension; **L** as a standalone managed platform.
- **Customers / monetization:** Agencies, public-sector vendors, and SaaS teams; per app/scan or accessible-release add-on.
- **Long-term potential:** Useful differentiator and practical repair loop, especially when generated UI templates can meet semantic defaults.

## 22 — Structured data to interactive 3D simulator

- **Product / problem:** Convert a spreadsheet/configuration and explicit assumptions into an interactive explainer or training simulator for operations, education, or product configuration.
- **Technology / competitors:** Blender background Python for asset/render pipelines and Three.js WebGPURenderer with WebGL 2 fallback for interactive browser scenes.[S43][S44]
- **Feasibility / limits:** A technical prototype is straightforward for bounded domains. Physics fidelity, geometry quality, accessibility, device/GPU support, and safety-critical validation are domain-specific. Three.js labels WebGPU renderer as evolving/experimental, and a visual scene is not engineering simulation proof.
- **Arena implementation:** Constrain the input schema, generate a parameterized scene, show assumptions and units, test bounds, and add domain-expert review for consequential decisions. Keep the simulation explicitly educational unless verified.
- **Complexity:** **M** for a narrow configurator; **XL** for validated engineering simulation.
- **Customers / monetization:** Training teams, educators, product configurators, and operations consultants; per-seat, simulator template, or custom deployment.
- **Long-term potential:** High-impact visual product niche, but depends on domain expertise rather than a generic “AI 3D model” pitch.

## 23 — WebMCP adoption and compatibility bridge

- **Product / problem:** Help a website expose an agent-readable set of approved client-side actions while maintaining equivalent server/API or MCP paths for agents that cannot use WebMCP.
- **Technology / competitors:** Chrome's WebMCP preview, browser extension APIs, web components, and MCP server/tool adapters.[S10][S13][S16][S31][S32]
- **Feasibility / limits:** Chrome documents WebMCP as early-preview/flagged and Chromium-focused. It is not a settled cross-browser standard or a replacement for MCP transports, prompts, resources, authorization, or API contracts. The implementation could break as the spec evolves.
- **Arena implementation:** Prototype only behind feature detection; keep canonical action definitions in a versioned schema; use a fallback API/MCP adapter; run contract tests in experimental Chromium and do not require customer sites to ship it.
- **Complexity:** **M** for a compatibility SDK; **L** for broad adoption, analytics, and cross-browser support.
- **Customers / monetization:** SaaS vendors, web-platform teams, and browser-agent ecosystems; SDK/support subscription or enterprise licensing.
- **Long-term potential:** Strategic option if sites standardize agent actions; invest lightly until browser support and interface semantics stabilize.

---

## Decision summary

The practical sequence is **#1 AppProof + #2 Preview Branch Lab**, initially on one web stack and with a remote browser worker. Add **#11 provenance** and **#14 migration rehearsal** as evidence components; then build **#4 App Steward** around repeat usage. Treat **#3 App Capsules** as the long-term platform bet and **#5 Roblox CI** as a testable vertical pilot. Do not start with a generic consumer browser agent, app store, or custom multi-tenant sandbox: those have the largest safety, support, and operational surfaces.
