# Feasibility Assessments — Arena Agent 04

**Assessment date:** 2026-11-08
**Purpose:** separate (1) what the current Arena coding-agent session can actually do, (2) what public documentation proves exists elsewhere, and (3) what would still need to be engineered before a commercial product. This is not a statement of Arena's entire internal platform roadmap.

## Executive feasibility verdict

**Best credible near-term build:** an **AppProof + Preview Branch Lab** pilot for one web stack, with a remote browser/CI worker and a user-approved provider connection. The workflow can be composed from documented deployments, database branches, browser tests, and evidence artifacts. It cannot be completed using only the present interactive coding sandbox because the sandbox has no browser executable, no Playwright package, no Docker, and no interactive browser-control tool.

**Most evidence-dense vertical:** Roblox Creator CI. Current Roblox docs describe engine-level headless Luau Execution tasks, status/log retrieval, and place publishing; a Roblox-owned example repository shows a Rojo/lint/test/deploy flow.[S39][S40][S41][S42] This is more narrowly feasible than a general computer-use product, but no Roblox API call was made from this session and the pipeline needs an external worker/API credential.

**Largest long-term bet:** App Capsules, a hosted runtime for user-owned generated apps. The technical components exist, but the hard part is not scaffolding a web app: it is multi-tenant isolation, identity, secrets, data durability, billing, abuse prevention, backup/restore, support, and provider cost control.

## Evidence levels

- **A — observed in this session:** runtime, repository, or connector schema was inspected directly. No user cloud resources were modified.
- **B — documented externally:** an official provider/API manual or public repository documents the mechanism or example. The integration was not independently executed here.
- **C — product inference:** architecture, customer, or monetization hypothesis derived from the documented mechanism. Requires an engineering spike and customer validation.

A B-level API is not an Arena capability; a public demo is not a production guarantee.

## Arena capability audit for this session

| Surface | Observed status | Practical consequence |
|---|---|---|
| Coding workspace | Node.js `v22.22.3`, Python `3.11.2`; shell, Git, file editing, web search/fetch are available. Repository initially contained only a top-level README. **A** | Can create repositories, scripts, CI templates, adapters, reports, and run ordinary code. This is not a secure hosted user-code runtime. |
| Browser execution | No Chrome/Chromium/Firefox executable on `PATH`; no global Playwright or `@playwright/test`; no interactive browser-control tool verified. **A** | Can research/write browser test code but cannot claim a real browser test passed in this sandbox. A remote browser/CI service is required for AppProof and browser-agent products. |
| Container isolation | Docker unavailable. **A** | Cannot run Docker-backed BrowserGym/WebArena environments or spin up per-tenant Linux containers here. Do not equate the live preview process with a tenant-isolated sandbox. |
| Live preview | Arena provides a long-lived process/live-preview path. Server must bind to `0.0.0.0` and tolerate the proxied preview host. **Platform instruction observed; no preview server started in this research task.** | Useful for human review of a locally running web app, not a substitute for independent browser automation or production hosting. |
| Network | Direct shell egress is restricted to `github.com`, `codeload.github.com`, `api.github.com`, `registry.npmjs.org`, and `pypi.org`. **A** | Do not assume code in the sandbox can call `apis.roblox.com`, arbitrary customer APIs, or provider REST endpoints. Use supported connectors or an approved deployed worker/egress path. |
| GitHub | `git`/`gh` authentication is configured for repository work. **A** | Supports work in the current Git repository; does not by itself establish an always-on GitHub App, webhook service, or CI integration for customers. |
| Supabase connector | Connector is enabled. The available tool inventory includes project, branch, migration, SQL, secrets, and Edge Function operations. **A: schema inventory only** | These are promising building blocks for a connected workflow. No project listing, branch, SQL, secret, migration, or deployment call was made. User approval, tenant boundaries, plan entitlements, and API effects remain untested. |
| Vercel connector | Connector is enabled. Inventory includes project, deployment, environment-variable, webhook, and domain operations. **A: schema inventory only** | A deployment orchestration prototype can be designed around it; no Vercel resource was read or changed. The connector's `create_deployment` schema does not expose `projectSettings` or `skipAutoDetectionConfirmation`, so a first-deployment bootstrap requiring those controls needs a pre-initialized project or another setup route. |
| Other execution/provider connectors | No browser, Roblox Open Cloud, Windows UI Automation, Android device farm, or Unity/Unreal runner was available in the inspected session. **A** | Code can be generated for these systems; runtime execution and credentials need a provider/worker not demonstrated here. |

## Current-session fit scale

The scores below assess how much of a credible proof can be demonstrated **inside the present Arena coding-agent sandbox alone**. They are not scores for Arena's theoretical ability to fund/deploy the product. `1` = core path cannot run here; `3` = useful code/design proof, but a critical external runtime or connector is unverified; `5` = all core paths are directly demonstrable here. Complexity follows the T-shirt scale in [technical_opportunities.md](technical_opportunities.md).

| Rank | Opportunity | Session fit | External dependency / blocker |
|---:|---|---:|---|
| 1 | AppProof | 2/5 | Remote browser runner required; no browser installed. Code/test scaffolding can be written. |
| 2 | Preview Branch Lab | 3/5 | Supabase/Vercel connectors are available but uncalled; first deployment bootstrap limitation; provider entitlements need checking. |
| 3 | App Capsules | 2/5 | Requires production-grade tenant isolation, runtime, persistence, billing, and operations. |
| 4 | App Steward | 2/5 | Needs scheduled service, source/deploy events, remote tests, safe credential use, and ongoing operation. |
| 5 | Roblox Creator CI | 2/5 | Public APIs exist; no Roblox API egress/connector or creator API key available here. Can write a workflow template only. |
| 6 | MCP Permission Router | 2/5 | Can prototype policy code; secure token broker, OAuth flows, and deployment boundary unverified. |
| 7 | Agent Workflow Benchmark Lab | 1/5 | No browser or Docker; realistic environment setup is an external infrastructure task. |
| 8 | MCP Compatibility Monitor | 3/5 | Can implement schema/contract tests, but cannot probe arbitrary live servers from this network. |
| 9 | API Connector Compiler | 3/5 | Can parse/generate against local specs; hosted OAuth callbacks and arbitrary API calls need approved egress and secret storage. |
| 10 | Trace-to-Repro Debug Loop | 2/5 | Trace formats and code workflow are documented; no live browser/app telemetry to reproduce here. |
| 11 | Supply-chain evidence bundle | 3/5 | Can build report/CI integration; remote OSV/provider integration and signed artifacts not exercised in this session. |
| 12 | Browser task runner | 1/5 | No interactive browser, session manager, or authenticated user profile. |
| 13 | Local-first app shell | 3/5 | Can develop a browser app, but cannot test it in a browser here; persistence/device inference not verified. |
| 14 | Migration/recovery lab | 3/5 | Supabase connector surfaces relevant operations but no database actions were tested; representative data/restore still needed. |
| 15 | WASI plugin runtime | 2/5 | Can code the interface; Wasmtime/isolated runtime and hostile-plugin tests not present. |
| 16 | Agent Flight Recorder | 3/5 | A local event schema and redactor can be built; no production agent traffic/retention service exists in this session. |
| 17 | App/template marketplace | 2/5 | Requires deployed runtime, identity, review, billing/payout operations, and dispute/support handling. |
| 18 | Windows workflow automation | 1/5 | Current host is not a Windows desktop and has no UI Automation control. |
| 19 | Mobile build/test/release | 1/5 | No native SDKs, signing keys, emulator, or device-farm connector verified. |
| 20 | Unity/Unreal QA farm | 1/5 | Engine installations, licenses, GPU/device workers, and build artifacts unavailable. |
| 21 | Accessibility verification | 2/5 | Rules can be integrated in test code; no browser to execute DOM checks, and automated checks do not certify accessibility. |
| 22 | 3D simulator | 2/5 | Can write web code; Blender and graphics/browser runtime not installed or tested. |
| 23 | WebMCP bridge | 1/5 | Requires experimental/flagged Chromium support, absent here; standard is still early-preview. |

## Product feasibility: recommended implementation path

### Phase 0 — Validate the buying problem, not the concept name

Interview app teams, agencies, and non-technical owners who already have AI-generated/custom applications. Ask what currently breaks after generation, whether they deploy it, how often they need previews/repairs, who approves changes, and what evidence would justify paying. Test AppProof and “keep my app working” separately; do not assume one buyer values both.

### Phase 1 — Narrow, provider-backed release evidence

Choose one web stack and one deployment/database path. Require explicit acceptance checks, use a provider-owned preview deployment and synthetic DB branch, run a hosted browser worker, and save traces/screenshots. The first product should report evidence and ask for a human decision, not deploy unreviewed code into production.

**Engineering spike needed:** create a disposable Vercel preview and Supabase branch with test credentials; run a basic seeded flow; verify cleanup, timeouts, errors, and rollback. Current connector inventory suggests an avenue but does not prove the whole path works.

### Phase 2 — Make checks repeatable and safe

Store test specs with the app; separate deterministic checks from visual/model judgments; version fixtures and grader logic; measure flakiness; redact traces; provide immutable links to the app commit/environment. Add OSV/SBOM/provenance and migration results as separate evidence categories, not one “safe” score.[S02][S26][S27][S28][S29]

### Phase 3 — Add recurring maintenance only after reliability exists

Offer scheduled smoke tests, dependency/migration alerts, and repair PRs that require approval. Add Temporal-like durable orchestration only if the workflow genuinely needs resilient retries, long timers, or human waits; a background queue is enough for simpler cases.[S23]

### Phase 4 — Choose a platform or vertical bet

Use observed usage to choose between App Capsules (broad runtime), Roblox Creator CI (bounded engine workflow), or MCP governance (enterprise tool permissions). Each has different buyers and operational requirements; do not conflate them into one roadmap before validating pull.

## High-priority engineering risks and controls

| Risk | Why it matters | Minimum control before paid beta |
|---|---|---|
| Generated test false confidence | A test may pass without verifying the business result, or a model judge may accept a wrong state. | Deterministic assertions for core writes; visible criteria; independent test cases; human review on ambiguous results. |
| Secret/data exposure | Browser traces, logs, screenshots, prompts, and generated code can contain credentials or personal data. | Secret references, least privilege, redaction before storage, per-tenant retention/deletion, no raw token logging. |
| Untrusted generated code | Build and preview jobs execute customer-controlled code. | Separate per-job workers; no ambient host access; tight quotas; network egress allowlist; ephemeral credentials; teardown. |
| Production side effects | Agent may send email, charge money, modify live data, publish a game, or change a deployment. | Preview/test-only credentials by default; explicit approvals and environment labels; prevent auto-promotion. |
| Database migrations | A migration can lock, delete, or corrupt data even if it succeeds in a small synthetic branch. | Synthetic representative fixtures; migration diff; backup/restore proof; staged rollout; human sign-off. |
| Provider coupling/cost | Preview minutes, database branches, and browser workers vary by plan and price. | Meter consumption; provider abstraction only where useful; cost caps; cleanup TTL; no implied unlimited usage. |
| Agent/protocol drift | MCP/WebMCP/telemetry APIs can evolve, causing silent incompatibility. | Pin versions; contract tests; compatibility reports; keep WebMCP experimental behind a fallback. |
| Overclaimed trust/compliance | SBOMs and attestations are useful evidence but do not certify software security. | State exactly what was scanned, versions, coverage gaps, and manual-review requirements. |
| Specialized toolchains | Windows, mobile, game engines, and 3D need host/device-specific workers. | Customer-hosted or licensed dedicated workers; do not pretend Linux shell access provides a device farm. |

## Specific provider integration caveats observed

- **Supabase:** the connector inventory exposes useful project/database branch/migration/SQL/secret/Edge Function operations. The existence of a tool is not evidence that a project was selected, a branch can be created on a customer's plan, data is cloned, or a migration is safe. No connector action was invoked.
- **Vercel:** deployment and project-related connector tools are present. The deployment schema available in the session does not expose `projectSettings` or `skipAutoDetectionConfirmation`; the first deployment may therefore need to be initialized outside that call or use a different setup route. No deployment was created.
- **Roblox:** current official docs describe Luau Execution endpoints as Stable and list finite task/concurrency limits; publishing has asynchronous completion and documented unsupported instance types. No Roblox API call was made, so credentials, authorization, rate limits, availability, and real place behavior remain to be tested.[S39][S40]
- **Browser runtime:** a Playwright or Stagehand script can be authored, but it was not run here. A separate execution host must supply the browser and isolation; Playwright's existence does not mean Arena's shell has it.[S01][S04][S05]

## What would change the ranking

Raise AppProof/Preview Lab if interviews show recurring release pain, users already connect source/deployment/database accounts, and a remote worker can run tests reliably at acceptable cost. Raise Roblox CI if creators confirm they will pay for safer test-place workflows and the Open Cloud API behaves predictably for their place setup. Raise MCP governance if enterprises have concrete approval/audit requirements and can provide a safe test server. Lower App Capsules if users mainly need one-off prototypes or prefer owning their hosting directly.

No market size, price point, conversion rate, performance score, or customer demand has been verified in this research. Those are open questions—not facts to fill with generic AI-market estimates.
