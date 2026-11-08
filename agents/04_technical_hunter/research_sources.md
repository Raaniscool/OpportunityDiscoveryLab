# Research Sources — Agent 04

**Sources reviewed:** 2026-11-08 unless a version/date is noted. Primary documentation and project repositories were preferred. Source links establish documented functionality or a public code example; they do not prove Arena has integrated or independently executed that functionality. `[Sxx]` identifiers are cited in the other four report files.

## Research method and confidence

1. Looked for primary API specifications, official vendor documentation, and public repositories that contain runnable examples or concrete interfaces.
2. Recorded implementation constraints and lifecycle requirements—not just product names. Examples include Supabase branches being data-less by default, Roblox Luau task limits, Chrome permission requirements, Vercel deployment bootstrap behavior in the available connector, and missing browser/container runtimes in the current Arena session.
3. Classified evidence as **documented elsewhere**, **observed in this session**, or **commercial/product inference**. No provider API was called and no external system was modified in this research task. Code samples were not run unless explicitly stated.
4. Competitor names in `technical_opportunities.md` are adjacent tools/categories drawn from the technical landscape, not a complete feature/pricing/market-share comparison. There are no customer interviews, willingness-to-pay tests, or market-size estimates in this report.
5. Some protocol and browser interfaces are evolving. Re-check the cited pages, API availability, plan restrictions, and terms before implementation. In particular, WebMCP is marked early-preview/flagged; Roblox's current API reference labels Luau Execution endpoints Stable, while its sample repository warns that the example is not battle-tested.

## Primary documentation and repositories

### Browser automation, testing, and agent evaluation

- **[S01] Playwright MCP — Introduction.** Playwright's MCP server exposes browser interaction through structured snapshots and tools. <https://playwright.dev/mcp/introduction>
- **[S02] Playwright Trace Viewer.** Describes trace artifacts with actions, screenshots, DOM snapshots, source locations, and network activity. <https://playwright.dev/docs/trace-viewer>
- **[S03] Playwright Test Projects.** Documents browser/project configuration for running test suites across configured browsers/projects. <https://playwright.dev/docs/test-projects>
- **[S04] microsoft/playwright-mcp — GitHub repository.** Official repository and configuration examples for the Playwright MCP server. <https://github.com/microsoft/playwright-mcp>
- **[S05] Stagehand v3 Quickstart.** Demonstrates natural-language `act`/`observe`/`extract` combined with deterministic Playwright-style code and hosted browser setup. <https://docs.stagehand.dev/v3/first-steps/quickstart>
- **[S17] OpenAI — Computer use tool.** Describes the application-side loop that translates model-requested actions into browser/OS input and returns screenshots. This does not imply Arena exposes such a handler. <https://developers.openai.com/api/docs/guides/tools-computer-use>
- **[S46] ServiceNow/BrowserGym — GitHub repository.** Open framework for web-agent task environments and benchmarks including WebArena and WorkArena; repository cautions it is for research rather than a consumer product. <https://github.com/ServiceNow/BrowserGym>
- **[S47] ServiceNow WorkArena.** Benchmark for common knowledge-work tasks on a ServiceNow environment; useful evidence for task-based evaluation, not a commercial agent reliability guarantee. <https://servicenow.github.io/WorkArena/>

### Deployment, runtime, branching, and orchestration

- **[S06] Cloudflare Sandboxes.** Official overview of container/microVM-backed code execution and Dynamic Workers, including the Worker as a control point for data/network access. <https://developers.cloudflare.com/sandbox/>
- **[S07] E2B Sandbox Auto-resume.** Documents pause/resume lifecycle configuration and preview URLs; auto-resume is not an unlimited-uptime guarantee. <https://docs.e2b.dev/sandbox/auto-resume>
- **[S08] Supabase Branching.** Describes isolated database branches, data-less-by-default behavior, and Git-connected migration/seed/Edge Function workflows. <https://supabase.com/docs/guides/deployment/branching>
- **[S09] Vercel REST API — Create a Deployment.** Documents deployment creation and progression toward ready/error states. The current Arena connector has a narrower parameter surface than the full public API, noted in the feasibility report. <https://vercel.com/docs/rest-api/deployments/create-a-new-deployment>
- **[S23] Temporal — Why Temporal?** Documents durable workflows, retries, timers, event-history replay, and human waits; provides a concrete long-running orchestration model with a separate service burden. <https://docs.temporal.io/evaluate/why-temporal>

### Agent protocols, permissions, and API contracts

- **[S10] Model Context Protocol Specification, 2025-06-18.** Defines MCP protocol primitives and server/client behavior. <https://modelcontextprotocol.io/specification/2025-06-18>
- **[S11] MCP Client Best Practices, 2026-07-28 documentation.** Describes progressive discovery for hosts with many tools, including loading detailed tool schemas on demand. <https://modelcontextprotocol.io/docs/2026-07-28/develop/clients/client-best-practices>
- **[S12] MCP Security Best Practices, 2026-07-28 documentation.** Discusses consent, least privilege, local-server isolation, OAuth/token validation, and credential-safe logging. <https://modelcontextprotocol.io/docs/2026-07-28/tutorials/security/security_best_practices>
- **[S13] MCP Authorization, 2026-07-28 documentation.** Covers authorization flows and implementation responsibilities for MCP clients/servers. <https://modelcontextprotocol.io/docs/2026-07-28/tutorials/security/authorization>
- **[S14] MCP Registry Documentation.** Documents server discovery/registry interfaces. Registry listing is not a security or compatibility endorsement. <https://registry.modelcontextprotocol.io/docs>
- **[S15] modelcontextprotocol/inspector — GitHub repository.** Tooling to inspect/call MCP tools, resources, and prompts over supported transports. <https://github.com/modelcontextprotocol/inspector>
- **[S16] Chrome WebMCP guide.** Describes the browser-facing WebMCP preview; current guide characterizes it as early-preview/flagged and Chromium-focused. <https://developer.chrome.com/docs/modern-web-guidance/guides/webmcp/webmcp>
- **[S18] GitHub Copilot SDK — GitHub repository.** Public, evolving SDK reference for integrating Copilot Agent into applications/services; contains tool/permission integration patterns. This is an implementation example, not a statement about Arena's runtime. <https://github.com/github/copilot-sdk>
- **[S19] OpenAPI Specification v3.1.1.** Defines a machine-readable HTTP API description useful for discovery, code generation, documentation, and testing. Newer versions are linked from the specification page; v3.1.1 is cited for its interface-description principle. <https://spec.openapis.org/oas/v3.1.1.html>

### Local-first computing, extensions, and telemetry

- **[S20] electric-sql/pglite — GitHub repository.** Postgres-compatible engine compiled to WebAssembly, including browser persistence options; not proof of a managed multi-user DB. <https://github.com/electric-sql/pglite>
- **[S21] ONNX Runtime Web — WebGPU execution provider.** Browser inference support and WebGPU/operator/device constraints. <https://onnxruntime.ai/docs/tutorials/web/ep-webgpu.html>
- **[S22] Wasmtime — Component Model.** Describes running components with explicitly granted host capabilities rather than automatic system-resource access. <https://component-model.bytecodealliance.org/running-components/wasmtime.html>
- **[S24] OpenTelemetry eBPF Instrumentation (OBI).** Zero-code telemetry for supported Linux workloads; kernel/BTF and privilege constraints mean it is not universal. <https://opentelemetry.io/docs/zero-code/obi/>
- **[S25] OpenTelemetry GenAI Semantic Conventions repository.** Evolving semantic conventions for GenAI/agent telemetry; pin versions and expect change. <https://github.com/open-telemetry/semantic-conventions-genai>
- **[S26] Langfuse Offline Evaluation.** Datasets, experiments, evaluators, and traces for repeatable evaluation; evaluators still need ground truth/calibration. <https://langfuse.com/docs/evaluation/get-started/offline>

### Security, provenance, and accessibility

- **[S27] OSV API.** Package/version and commit vulnerability queries, including batched queries. <https://google.github.io/osv.dev/api/>
- **[S28] GitHub Artifact Attestations.** GitHub Actions can generate build provenance and SBOM attestations for artifacts. Availability varies by repository/plan and permissions; attestations are evidence about provenance, not proof that software is secure. <https://docs.github.com/en/actions/how-tos/secure-your-work/use-artifact-attestations/use-artifact-attestations>
- **[S29] SLSA Specification v1.2.** Defines tracks/levels and attestation formats for progressively stronger supply-chain properties. <https://slsa.dev/spec/v1.2/>
- **[S30] dequelabs/axe-core — GitHub repository.** Automated accessibility engine for web UI testing; automated findings do not replace manual review or establish full conformance. <https://github.com/dequelabs/axe-core>

### Desktop, browser extension, mobile, game, and 3D APIs

- **[S31] Chrome `sidePanel` API.** Supports contextual extension panel surfaces, subject to extension/runtime permissions. <https://developer.chrome.com/docs/extensions/reference/api/sidePanel>
- **[S32] Chrome `scripting` API.** Documents script/CSS injection and the associated permission model (`scripting` plus host access or active-tab access). <https://developer.chrome.com/docs/extensions/reference/api/scripting>
- **[S33] Microsoft Windows UI Automation.** Windows accessibility and automation framework entry point. <https://learn.microsoft.com/en-us/windows/win32/winauto/entry-uiauto-win32>
- **[S34] Power Automate Desktop — UI elements.** Documents UIA, legacy MSAA, and selector approaches for desktop automation. <https://learn.microsoft.com/en-us/power-automate/desktop-flows/ui-elements>
- **[S35] Maestro Android support.** Describes Android UI testing via ADB and rendered UI interaction; cloud device scaling is a separate execution service. <https://docs.maestro.dev/get-started/supported-platform/android>
- **[S36] Capacitor `cap build`.** Documents signed AAB/APK/IPA build options and certificate/keystore/provisioning inputs. <https://capacitorjs.com/docs/cli/commands/build>
- **[S37] Unity Test Framework — Run tests from the command line.** Shows batch-mode command-line tests and target-platform options. <https://docs.unity3d.com/6000.3/Documentation/Manual/test-framework/run-tests-from-command-line.html>
- **[S38] Unreal Engine Gauntlet.** Documents `RunUAT RunUnreal` test workflows for editor/packaged builds and platform-specific device requirements. <https://dev.epicgames.com/documentation/en-us/unreal-engine/running-gauntlet-tests-in-unreal-engine>
- **[S39] Roblox Open Cloud — Luau Execution.** Documents headless place execution, result/log polling, task-duration and concurrency limits; the API reference currently labels the endpoints Stable. <https://create.roblox.com/docs/cloud/reference/features/luau-execution>
- **[S40] Roblox Open Cloud — Place Publishing.** Documents publishing existing place assets, asynchronous operation polling, required permissions, and unsupported instance types. <https://create.roblox.com/docs/cloud/guides/usage-place-publishing>
- **[S41] Roblox/place-ci-cd-demo — GitHub repository.** Reference Rojo build/lint/format/test/deploy pipeline using Open Cloud Luau execution. Repository is archived and explicitly warns it is not battle-tested. <https://github.com/Roblox/place-ci-cd-demo>
- **[S42] Rojo — GitHub repository.** Source synchronization/build tooling for Roblox place projects. <https://github.com/rojo-rbx/rojo>
- **[S43] Blender Python API — Tips and Tricks.** Documents headless background script execution via `blender --background --python`. <https://docs.blender.org/api/current/info_tips_and_tricks.html>
- **[S44] Three.js WebGPURenderer manual.** Documents the WebGPU renderer, asynchronous initialization, and WebGL 2 fallback; graphics support remains device-dependent/evolving. <https://threejs.org/manual/#webgpurenderer>

### Marketplace economics

- **[S45] Stripe Connect marketplace documentation.** Describes seller onboarding, application fees, payouts, subscriptions, and platform responsibilities including fees, refunds, disputes, and connected-account risk. <https://docs.stripe.com/connect/marketplace>

## Arena session observations (not public sources)

These are direct environment observations made for this report on 2026-11-08; they are not citations to Arena product marketing and do not establish capabilities in a different runtime.

- **[A1] Runtime/repository audit:** Node.js `v22.22.3`, Python `3.11.2`; Docker unavailable; no Chrome/Chromium/Firefox executable on `PATH`; no globally installed Playwright/`@playwright/test`; repository initially had only the root README and no `agents/` deliverables.
- **[A2] Connector inventory:** Supabase and Vercel connectors are enabled. Supabase tool inventory includes project, branch, migration, SQL, secret, and Edge Function operations. Vercel inventory includes project, deployment, environment-variable, webhook, and domain operations. This was an inventory only; no resource was accessed or changed.
- **[A3] Deployment schema limitation:** The Vercel connector's `create_deployment` schema does not expose `projectSettings` or `skipAutoDetectionConfirmation`, constraining the first-deployment bootstrap path. This describes the connector surface available in this session, not the full Vercel REST API.
- **[A4] Egress boundary:** Direct shell egress is limited to GitHub/codeload/API GitHub, npm registry, and PyPI. Provider API access through arbitrary code is not assumed.
- **[A5] Live preview:** Arena exposes a long-lived process/live-preview mechanism; server processes need to bind to `0.0.0.0` and accept the proxied host. No preview was started in this research task.

## Research limits

- Sources were read from official docs/repositories, but APIs, accounts, plans, terms, and rollout status can change.
- No browser, deployment, database, Roblox, mobile, Windows, game-engine, or 3D workflow was run end-to-end.
- No customer research or market/pricing study was performed. All customer segments, monetization paths, ranking, and complexity estimates are product hypotheses to validate.
- Do not interpret a tool's presence in the Arena connector inventory as approval to use production resources; obtain explicit project/user consent and use the least-privilege path.
