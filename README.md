# Lucas Floriano Muller

**Senior full-stack engineer: AI agents, durable workflows and the platforms under them.**
Remote from Florianópolis, Brazil (UTC−3) · 10 years shipping web products · English fluent

- 🤖 Built a streaming tool-calling assistant with **70+ entitlement-gated tools** and human-in-the-loop approval (DealMerge, led a team of 7)
- ⚙️ Long-running AI work as **durable workflows**: Trigger.dev v4, Vercel Workflow DevKit, Inngest, Lambda + SQS
- 🏗️ Monorepo platforms with enforced boundaries, domain events, hybrid search (Typesense + pgvector), CI with per-PR DB branches
- 🛠️ Daily driver: Claude Code + Codex, with my own tooling for agent skills, code review and local infra (below)

**Now:** open to senior/staff remote roles with US & EU teams, and to short AI-automation engagements.
→ [LinkedIn](https://www.linkedin.com/in/lucasflomuller/) · lucasflorianomuller@gmail.com

## Featured projects

| Project | What it is | Stack |
|---|---|---|
| [**GitScope**](https://github.com/lucasflomuller/gitscope-showcase) | Local code-review workspace: guided reading order, symbol navigation, review notes, MCP for agent handoff | Next.js 16 · React 19 · tree-sitter · MCP |
| **Harness Studio** _(coming soon)_ | Desktop home for Codex & Claude Code skills, plugins and MCP servers: forms over raw config, history, safe writes | Electron · React · CodeMirror |
| [**SoupaWhisper**](https://github.com/lucasflomuller/soupawhisper) | Push-to-talk dictation for Wayland/Hyprland with a warm-model daemon | Python · faster-whisper · systemd |
| _more coming: Atlas (spatial code editor), Switchboard (local apps + Cloudflare tunnels control plane)_ | | |

## Experience (short)

| | |
|---|---|
| 2026– | Senior Backend/Data Engineer (contract) · plant-biotech R&D, global agri-science co. |
| 2024– | Lead Engineer · **DealMerge** (CRE deal platform, US) |
| 2025–26 | Senior Full-stack (contract) · **SearchParty** (AI search visibility) |
| 2025 | Sole developer · **BusinessPlan.ai** |
| 2022–25 | Senior Staff Frontend (Toptal) · **Dromo** (embeddable data import) |
| 2021–23 | Lead Full-stack · **Predactiv / ShareThis** |

<details><summary>Full stack & selected work</summary>

## What I build

**AI product engineering**
Tool-calling agent architectures — entitlement-gated tool registries, tool-call repair, loop detection, structured conversation summarisation, entity resolution. RAG with reranking, schema-validated structured output, streaming and resumable UIs, human-in-the-loop approval for writes, AI evals as a first-class test tier, per-generation cost tracking, and multi-provider routing through an AI gateway.
`Vercel AI SDK` · `Claude Agent SDK` · `OpenAI Realtime API` · `Claude Code`

**Durable workflows & background jobs**
Trigger.dev v4 (schema-validated tasks, named queues with concurrency limits, idempotency keys, cron schedulers, machine sizing, realtime progress), Vercel Workflow DevKit (`"use workflow"` / `"use step"` durable steps), Inngest, AWS Lambda + SQS, Celery. DAG scheduling, retry with dependent cascade, debouncing and coalescing, safe concurrent job claiming, cancellation of stale work.

**Platform & monorepo architecture**
Turborepo with mechanically enforced layered package boundaries. Domain events with idempotent post-commit projections, replay and recovery, typed resource IDs, resource-level permission systems with inheritance, entitlement-driven feature gating.

**Data, search & pipelines**
PostgreSQL (Neon, pgvector, partitioned analytics), Snowflake, Redis. Typesense hybrid lexical + vector search with blue-green schema migrations and graceful degradation. Document AI pipelines, schema-driven data import and column matching, ETL with entity resolution, D3 / VISX visualization with native PPTX export.

**Real-time & multimodal**
SSE resumable streams with heartbeats and stall detection, Ably channel fan-out, WebRTC realtime voice, screen capture with perceptual-hash frame deduplication, browser-automation agents.

**Delivery & quality**
CI/CD with per-PR database branches, migration rehearsal and staged production promotion. Playwright end-to-end suites, third-party security assessment (CASA), observability with Sentry and PostHog, architecture documentation as a handoff deliverable.

### Selected work

- **DealMerge** — Owned architecture end to end and led a team of 7 through a ground-up rewrite onto a Turborepo platform (Next.js 16, React 19, tRPC, Drizzle on Neon PostgreSQL, WorkOS, Trigger.dev v4). Built the streaming tool-calling AI assistant with 70+ entitlement-gated tools and auditable human-in-the-loop approval, the domain-events architecture, hybrid Typesense search, the background-job platform running document AI pipelines, and a multi-year NOI/IRR forecasting engine.
- **Plant-biotechnology R&D** — Designed and own in production a governed data-warehouse-to-OLTP reference-data projection: allow-listed sources reconciled and published as a single reviewed snapshot per transaction, so request-path services never touch the warehouse. Also shipped authorization hardening across API and UI, an incremental append-only index for sequence-homology search, and the team's developer-productivity tooling — including a Go CLI/TUI for resumable handoff across a corporate air gap.
- **SearchParty** — Architected the multi-provider AI layer and enforced monorepo boundaries; built an autonomous streaming strategy-document agent, an adaptive interview system on durable Workflow DevKit steps with a cross-participant knowledge loop, and a real-time voice + screen-share experience over WebRTC with perceptual-hash frame deduplication in a Web Worker.
- **BusinessPlan.ai** — Built the entire product solo. Orchestrated long-running plan generation as a dependency graph with transitive-dependent retry and dual-speed generation, plus a dependency-free 14-stage financial engine over 60-month projections as pure, unit-testable functions.
- **Dromo** — Co-owned the embeddable import widget and its performance architecture, built the headless Lambda import pipeline with headless-to-interactive rehydration, cost-tiered column matching (exact → embedding → fuzzy) with cost caps and graceful degradation, and the no-code schema builder.

## Tech

| | |
| --- | --- |
| **Languages** | TypeScript · JavaScript · Python · Go · SQL |
| **Frontend** | React 19 · Next.js · TanStack Start / Router / Query · Svelte / SvelteKit · Tailwind CSS · D3 · VISX |
| **Backend** | Node.js · tRPC · Drizzle · Prisma · Zod · Effect-TS · FastAPI · Django · Flask · SQLAlchemy |
| **Data** | PostgreSQL · pgvector · Neon · Snowflake · Redis · Typesense · MongoDB |
| **AI** | Vercel AI SDK + AI Gateway · Claude Agent SDK · OpenAI Realtime API · Claude Code |
| **Infra** | Trigger.dev · Vercel Workflow DevKit · Inngest · AWS (Lambda, SQS, ECS, S3, Textract) · Docker · Turborepo |
| **Quality** | Playwright · Vitest · AI evals · Sentry · PostHog · CI/CD with per-PR database branches |

</details>
