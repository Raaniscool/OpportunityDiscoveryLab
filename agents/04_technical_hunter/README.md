# Technical Opportunity Hunter — Agent 04

**Research date:** 2026-11-08
**Scope:** technically specific, commercially plausible products Arena could create or enable—not a proposal to build any of them in this research task.

## Executive recommendation

Arena's most defensible technical opportunity is **not another code generator**. It is the lifecycle layer that turns generated software into something users can safely preview, verify, deploy, recover, and keep working.

The strongest near-term wedge is a combined **AppProof + Preview Branch Lab**: translate a user's acceptance criteria into reviewable deterministic checks; build a change in an isolated preview; provision a disposable database branch with synthetic data; execute browser tests on a remote worker; and return screenshots, traces, schema changes, and a clear pass/fail/needs-human-review result. Playwright documents browser snapshots and rich traces, while Vercel deployments and Supabase branches provide real building blocks for preview workflows.[S01][S02][S08][S09]

This is **technically plausible but not already proven inside Arena**. The current agent sandbox has no browser binary, Playwright installation, Docker, or interactive browser-control tool. A browser-test product therefore needs a remote browser runner or external CI worker; Arena's coding shell alone cannot validate a visual/browser workflow today. See [feasibility_assessments.md](feasibility_assessments.md) for the exact capability boundary.

## Ranked opportunities

The ranking weighs buyer pain, technical evidence, Arena fit, differentiation, and the size of the missing infrastructure. It is an expert prioritization—not a market-size calculation or the result of customer interviews.

1. **AppProof — verified releases for AI-built apps.** Most direct way to reduce the trust gap between “the code was generated” and “the requested behavior works.”
2. **Preview Branch Lab — one isolated full-stack preview per change.** Strong adjacent wedge: Vercel can create deployments; Supabase branches isolate schema/data, but are data-less by default.[S08][S09]
3. **Generated-App Runtime (“App Capsules”).** Important platform bet: persistent hosting, database, secrets, logs, rollback, and export for each user-owned app. Technically buildable with partners; isolation and operations make it a large investment.[S06][S07][S08][S09]
4. **App Steward — maintenance subscriptions for generated apps.** Recurring product for dependency updates, smoke tests, drift detection, backups, and approved repairs; depends on the first three layers.
5. **Roblox Creator CI.** A sharply scoped vertical: Roblox documents headless Luau execution against place versions, result/log polling, and a five-minute task limit; its API reference currently labels the endpoints Stable. A Roblox-owned sample pipeline uses Rojo, lint/format, tests, and publish steps.[S39][S40][S41][S42]
6. **MCP Permission Router.** Enterprise boundary for tool discovery, narrow grants, approvals, audit, and revocation; high-value but security-sensitive.[S10][S11][S12][S13][S14]
7. **Agent Workflow Benchmark Lab.** Run a customer's own browser/desktop tasks against agent/model versions and score outcome, side effects, time, and cost; build on evaluable task environments such as BrowserGym/WorkArena and experiment tracking.[S26][S46][S47]
8. **MCP Compatibility Monitor.** Detect server/tool schema drift, authentication breakage, unsafe scopes, and failed conformance before an agent workflow breaks.[S14][S15]
9. **API Connector Compiler.** Turn OpenAPI contracts into typed client tools and least-privilege agent-facing interfaces, with human approval for OAuth scopes.[S19][S10][S13]
10. **Trace-to-Repro Debug Loop.** Capture a failing run, make it reproducible, propose a code/test fix, and require review before merge.[S02][S24][S25][S26]

The remaining 13 concepts are documented in [technical_opportunities.md](technical_opportunities.md). The strongest long-term product is a connected lifecycle, not 23 unrelated applications.

## What Arena could realistically create

A staged strategy is credible:

- **Start with a repository-backed workflow** that captures explicit requirements, runs static/unit checks, creates a preview deployment, and produces a machine-readable evidence bundle.
- **Add isolated browser execution** using a remote worker/managed browser service. Persist traces and screenshots, but redact secrets and sensitive fields before storage.
- **Add database branching and synthetic seed data** through supported provider integrations. Require explicit human approval for production credentials, migrations, and promotion.
- **Later add managed runtime and maintenance** only after isolation, identity, billing, backups, rate limits, export, and incident response are designed.

Arena's current coding environment can write code, run shell commands, use Git, and expose an HTTP live preview. The available Vercel and Supabase connector schemas offer relevant deployment/database operations, but this session did not call them or alter cloud resources. The Vercel connector also lacks some controls needed for the first-deployment bootstrap path, so an initialized project or alternate setup path is required. These are observed session facts, not a claim that Arena already operates a production hosting platform.

## Unusual, well-grounded vertical bet

**Roblox creator CI is unusually specific and actionable.** The current Roblox Luau Execution documentation says a headless server loads a place and runs a script with DataModel/engine Luau access; clients can poll task completion and logs. Tasks are limited to five minutes and ten concurrent tasks per place. The official publishing guide describes publishing an existing `.rbxl`/`.rbxlx` place through an asynchronous operation, with documented unsupported instance types. The reference CI repository is archived and warns it is a demonstration, not battle-tested; use it as a pipeline example, not as production code.[S39][S40][S41]

## How to use this report

- [technology_landscape.md](technology_landscape.md) maps the technical components and what is mature versus emerging.
- [technical_opportunities.md](technical_opportunities.md) contains **23** product cards. Each covers product, problem, technology, competitors/alternatives, feasibility, limitations, Arena implementation, complexity, customers, monetization, and long-term potential.
- [feasibility_assessments.md](feasibility_assessments.md) separates current Arena capabilities from dependencies that are documented elsewhere but not available or verified here.
- [research_sources.md](research_sources.md) provides the source register and methodology.

## Important boundary

The source work establishes that APIs, runtimes, and reference implementations exist; it does **not** establish customer demand, willingness to pay, Arena production readiness, provider pricing, or actual performance in this sandbox. Those need customer discovery and an instrumented pilot. Citations throughout point to primary documentation, repositories, or public demonstrations rather than market-size claims.
