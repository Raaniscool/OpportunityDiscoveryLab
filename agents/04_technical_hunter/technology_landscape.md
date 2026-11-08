# Technology Landscape for Arena — Agent 04

**Reviewed:** 2026-11-08. This is a technical map, not a claim that Arena has already integrated or production-tested these systems. Source identifiers resolve in [research_sources.md](research_sources.md).

## 1. The technical opening: software needs a lifecycle, not just generation

As coding agents make it cheaper to create an application, value shifts to the mechanics that make it dependable: acceptance criteria, repeatable tests, isolated environments, identity and permissions, data migration, observability, rollback, and support. A generated screen is easy to demo; proving that it saved the right record, kept another tenant's data separate, survived a schema change, and can be recovered is a different problem.

The most promising architecture separates an **agent/control plane** (plans, reviews, asks for permission) from a **constrained execution plane** (builds, tests, deploys, and runs user code). This keeps a model from inheriting ambient credentials or unrestricted host access. It also lets Arena reuse managed providers for browser execution, app hosting, database branches, payments, and telemetry instead of immediately building all infrastructure itself.

## 2. Browser agents and software verification

### Mature building blocks

- **Playwright** provides browser automation and a test runner. Its trace viewer can expose actions, screenshots, DOM snapshots, source locations, and network activity; MCP presents browser interaction through structured snapshots and tools.[S01][S02][S03][S04]
- **Stagehand** demonstrates a hybrid interface: natural-language `act`/`observe`/`extract` for ambiguous steps plus deterministic Playwright-style APIs for repeatable parts; its quickstart demonstrates hosted browser sessions.[S05]
- **BrowserGym and WorkArena** show how to run agents against tasks with measurable outcomes, rather than score only generated text. WorkArena focuses on realistic enterprise-style browser tasks. These are evaluation frameworks/benchmarks, not turnkey commercial reliability guarantees.[S46][S47]
- **Computer-use APIs** require an application-side input handler: the model requests an action, the host maps it to browser/OS input and returns a screenshot. The existence of a computer-use API does not mean Arena exposes the handler or an authenticated browser session.[S17]

### Product implication

Use an evidence pipeline rather than a single “AI says it works” verdict:

1. Parse the user's requested behaviors into explicit, editable acceptance checks.
2. Prefer deterministic assertions, API checks, and accessibility locators where possible; use screenshot/vision judging only as supplemental evidence.
3. Run against a disposable preview with synthetic data and least-privilege credentials.
4. Save a trace, screenshots, test version, environment identifiers, and any unresolved assertions.
5. Label ambiguous outcomes for human review; never turn a probabilistic visual judge into an unconditional production gate.

**Hard dependency:** Arena's current sandbox lacks an installed browser and interactive browser-control surface. A production browser-testing product needs a separately deployed worker/managed browser fleet. Containerized benchmark environments may additionally be large or operationally complex; do not assume they can run inside the present agent container.

## 3. App hosting, isolated sandboxes, and preview environments

- **Vercel deployments** can be created through an API from source or uploaded files and move toward ready/error states.[S09]
- **Supabase Branching** creates isolated branch environments, data-less by default; Git-connected workflows can apply migrations, seed data, and deploy Edge Functions. This is a strong PR-preview primitive but not a safe production-data clone by default.[S08]
- **Cloudflare Sandboxes** provide container/microVM-backed execution and Dynamic Workers; the Worker is a control point for data/network access. Sandboxes and Workers are useful models for running code with explicit boundaries, not proof that Arena has equivalent infrastructure.[S06]
- **E2B** documents pause/resume behavior and preview endpoints for a sandbox lifecycle. Auto-resume is a lifecycle feature, not an unlimited-uptime promise.[S07]
- **Temporal** illustrates durable orchestration: progress, retries, timers, and human waits can survive worker failures. It adds a separate service and its own operational learning curve.[S23]

### Product implication

The simplest credible first release composes existing services: Git branch → preview deployment → database branch → remote browser worker → evidence bundle. Arena should avoid building a general-purpose, multi-tenant container fleet until it has validated the demand and can fund isolation, patching, egress control, abuse mitigation, and 24/7 operations. Branch data must be synthesized or explicitly sanitized; “preview” must not silently mean “copy production data.”

## 4. Agent protocols, connectors, and permissions

- **MCP** standardizes client/server primitives such as tools, resources, prompts, and authorization flows. The specification and registry provide protocol/discovery material; MCP Inspector can inspect and call server capabilities.[S10][S13][S14][S15]
- **Progressive tool discovery** is useful when agents face many tools: discover a subset and load full schemas on demand rather than injecting every tool definition into every prompt.[S11]
- **Security is architecture, not a checkbox.** MCP security guidance emphasizes consent, least privilege, careful OAuth handling, local-server isolation, and avoiding credential leaks. Authorization implementation is a separate concern from merely accepting an MCP tool call.[S12][S13]
- **OpenAPI** describes HTTP APIs in a machine-readable form and can feed client generation, docs, and tests. It does not define the intent of every endpoint or grant authorization to call it.[S19]
- **GitHub Copilot SDK** is a concrete, evolving agent-integration example with permission/tool hooks. Treat it as one implementation option, not as a guarantee that Arena's own runtime exposes those hooks.[S18]
- **WebMCP** is an emerging browser-facing interface for sites to expose client-side tools. Chrome's guide describes it as early-preview/flagged and Chromium-focused; it is not equivalent to MCP's transports, resources, or prompts.[S16]

### Product implication

An agent connector product should produce narrow capability grants, scoped OAuth or user-managed credentials, allow/deny and approval rules, a redacted audit trail, and a revocation path. It should keep the authorization decision outside model-generated instructions. WebMCP is worth prototyping behind a compatibility layer, not using as a hard dependency while it remains early-preview.

## 5. Local-first execution and portable extensions

- **PGlite** runs a Postgres-compatible engine compiled to WebAssembly, with browser persistence through IndexedDB. It can make a prototype/local app useful offline, but it is not evidence of a remotely hosted, multi-user database service.[S20]
- **ONNX Runtime Web** documents browser inference using WebGPU or WASM. WebGPU coverage is operator/model-dependent and local inference depends on device memory and performance.[S21]
- **Wasmtime's Component Model** allows a host to grant explicit capabilities to a WebAssembly component; a component does not automatically receive general system-resource access.[S22]

### Product implication

Local-first apps can reduce server costs and keep some data on-device, with sync only when needed. But offline storage, encryption, conflict resolution, backup, browser quotas, large model downloads, and device heterogeneity are real product work. WASM is useful for constrained extensions or user scripts; do not market “sandboxed” as “risk-free.” The host still needs a narrow capability model, resource limits, dependency controls, and abuse monitoring.

## 6. Evaluation, telemetry, security, and provenance

- **Langfuse** provides datasets, experiments, evaluators, and tracing for repeatable offline evaluation. Evaluation still needs domain-specific ground truth and calibrated graders.[S26]
- **OpenTelemetry eBPF Instrumentation (OBI)** can provide zero-code telemetry for supported Linux workloads, but its kernel/BTF and privilege requirements make it an environment-specific option, not a universal instrument-everything agent.[S24]
- **GenAI semantic conventions** define evolving telemetry vocabulary for AI and agent systems. Pin a version and expect schema changes; don't couple core business logic to a draft telemetry schema.[S25]
- **OSV** exposes package/version and commit vulnerability queries, including batched queries.[S27]
- **GitHub artifact attestations** can bind build provenance and SBOMs to an artifact; **SLSA** defines progressively stronger supply-chain guarantees and attestation formats. An attestation is evidence about a build, not proof that code is safe or bug-free.[S28][S29]
- **axe-core** automates a useful subset of DOM accessibility checks; its maintainers explicitly caution that automated checks cannot discover every accessibility issue. Manual/assistive-technology review remains necessary.[S30]

### Product implication

Arena can create an **evidence bundle**—tests, dependency findings, SBOM/provenance, trace, migration report, accessibility scan—without inventing a misleading universal “safe” badge. Each finding should include what was checked, tool/version, scope, confidence, and what remains untested. Telemetry must redact prompts, tokens, customer data, and screenshots; provide retention controls and deletion.

## 7. Desktop, mobile, games, and 3D pipelines

### Desktop and browser extensions

Windows UI Automation exposes accessibility and automation structures; Power Automate documents UIA/MSAA selector strategies.[S33][S34] Chrome's side-panel and scripting APIs support contextual extension surfaces and page-script injection, but require declared permissions/host access or user-granted `activeTab` access.[S31][S32] This supports products that assist with a user's current page or automate a controlled Windows workflow. It does **not** provide Arena's Linux sandbox with access to the user's desktop or browser.

### Mobile

Maestro drives Android through ADB and can interact with the rendered UI without embedding its test code in the app; hosted device execution is a separate service.[S35] Capacitor documents native Android/iOS builds and signed APK/AAB/IPA outputs, with keystores, certificates, provisioning profiles, and platform toolchains in the release path.[S36] A dependable product needs device/emulator capacity and signing-key management; the current Arena agent container has neither a mobile device farm nor Apple/Android release credentials.

### Games and interactive 3D

- **Unity Test Framework** runs EditMode/PlayMode/platform tests in batch mode.[S37]
- **Unreal Gauntlet** drives editor or packaged-game tests and monitors outcomes; its device deployment requires target-specific implementation.[S38]
- **Roblox Open Cloud** is particularly actionable: current Luau Execution docs describe headless engine execution and log/result retrieval; the API reference marks endpoints Stable, with task and concurrency limits. The separate publishing endpoint has documented instance-type limitations. A Roblox-owned sample pipeline demonstrates Rojo-based build, lint, test, and deployment but is archived and explicitly not battle-tested.[S39][S40][S41][S42]
- **Blender** supports background Python scripts, and **Three.js WebGPURenderer** targets WebGPU with a WebGL 2 fallback. Neither removes the need to validate domain-specific geometry/physics or the experimental/device-dependent parts of the graphics stack.[S43][S44]

### Product implication

These are vertical product bets, not just another UI on a general agent. Roblox is an unusually clear initial game-development niche because the cloud test endpoint runs engine Luau without a conventional desktop click-through test. It validates logic and DataModel interactions, not all client rendering, user experience, latency, or platform-specific behavior. Unity/Unreal/mobile require different toolchains, licenses, artifacts, and device farms; a single “universal game tester” would be a much larger product.

## 8. Monetization and platform economics

Two pricing patterns fit the evidence-backed opportunities:

1. **Developer assurance SaaS:** per app/repository/seat plus metered preview, browser, device, or evaluation runs. Customers pay for saved engineering/release effort; providers' compute costs must be passed through or managed.
2. **Hosted runtime/marketplace:** per active app or resource usage, plus optional templates/plugins. Payments can be handled with Stripe Connect, but marketplace operators may be merchant of record and bear fee, refund, dispute, and connected-account risk.[S45]

The second path has higher strategic value and much higher operational/legal obligations. Avoid revenue projections until interviews reveal repeat usage, deployment frequency, support burden, and willingness to pay.

## 9. Technical conclusions

- Prefer **API-first, deterministic interfaces** for known data operations; use browser automation only when no supported API exists or visual behavior is what needs testing.
- Treat each generated app as a **tenant boundary**: per-app credentials, network policy, resource quota, backup/export, dependency scan, and audit log.
- Use human approval for production deploys, destructive migrations, external writes, and publishing; generate rollback plans before actions.
- Capture reproducible evidence, not just an agent narrative.
- Start narrow: generated web apps and one hosting/database path; then expand into agent lifecycle and verticals such as Roblox.
- Keep WebMCP, full autonomous browser interaction, universal WASM plugins, a consumer app store, and custom cloud isolation as **research/partner-dependent bets**, not current Arena capabilities.
