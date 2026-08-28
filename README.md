# Lucas Floriano

**Senior full-stack engineer — AI-native systems, TypeScript, platform architecture.**

Fully remote from Florianópolis, Brazil · UTC−3 · [LinkedIn](https://www.linkedin.com/in/lucasflomuller/)

Ten years building web products, and the last several shipping AI-native systems in production: tool-calling agents with evals and audit trails, long-running work orchestrated as durable workflows, real-time voice and screen-share AI, and the platform architecture underneath them. I own systems end to end — from monorepo boundaries and domain-event pipelines through CI/CD and third-party security assessments — have led teams of up to 7, and work with Claude Code as a daily driver.

---

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

---

## Experience

**Full-time**

| Years | Role | Where |
| --- | --- | --- |
| 2024–present | Lead Engineer | **DealMerge** — commercial real estate deal management platform · Remote (US) |
| 2021–2023 | Lead Full-stack Engineer | **Predactiv (ShareThis)** — data-as-a-service · Remote (US) |
| 2018–2021 | Software Engineer | **Jungle Devs** — product agency · Florianópolis, Brazil |
| 2016–2018 | Systems Analyst | **BrasilRad** — medical physics · Florianópolis, Brazil |

**Contract**

| Years | Role | Where |
| --- | --- | --- |
| 2026–present | Senior Backend / Data Engineer | Plant-biotechnology R&D, global agri-science company (confidential) · Remote |
| 2025–2026 | Senior Full-stack Engineer | **SearchParty** — AI search visibility (AEO) platform · Remote (US) |
| 2025 | Sole Developer | **BusinessPlan.ai** — AI business planning platform · Remote (US) |
| 2022–2025 | Senior Staff Frontend Engineer | **Dromo** (via Toptal) — embeddable customer data-import platform · Remote (US) |

### Selected work

- **DealMerge** — Owned architecture end to end and led a team of 7 through a ground-up rewrite onto a Turborepo platform (Next.js 16, React 19, tRPC, Drizzle on Neon PostgreSQL, WorkOS, Trigger.dev v4). Built the streaming tool-calling AI assistant with 70+ entitlement-gated tools and auditable human-in-the-loop approval, the domain-events architecture, hybrid Typesense search, the background-job platform running document AI pipelines, and a multi-year NOI/IRR forecasting engine.
- **Plant-biotechnology R&D** — Designed and own in production a governed data-warehouse-to-OLTP reference-data projection: allow-listed sources reconciled and published as a single reviewed snapshot per transaction, so request-path services never touch the warehouse. Also shipped authorization hardening across API and UI, an incremental append-only index for sequence-homology search, and the team's developer-productivity tooling — including a Go CLI/TUI for resumable handoff across a corporate air gap.
- **SearchParty** — Architected the multi-provider AI layer and enforced monorepo boundaries; built an autonomous streaming strategy-document agent, an adaptive interview system on durable Workflow DevKit steps with a cross-participant knowledge loop, and a real-time voice + screen-share experience over WebRTC with perceptual-hash frame deduplication in a Web Worker.
- **BusinessPlan.ai** — Built the entire product solo. Orchestrated long-running plan generation as a dependency graph with transitive-dependent retry and dual-speed generation, plus a dependency-free 14-stage financial engine over 60-month projections as pure, unit-testable functions.
- **Dromo** — Co-owned the embeddable import widget and its performance architecture, built the headless Lambda import pipeline with headless-to-interactive rehydration, cost-tiered column matching (exact → embedding → fuzzy) with cost caps and graceful degradation, and the no-code schema builder.

---

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

---

## Side projects

- **Mononono** — venture-grade monorepo platform for launching products fast: a 6-layer architecture (Foundation → Platform → Kernel → UI → App → Tooling) with mechanically enforced dependency direction and a documented ADR and invariant regime.
- **CodeCanvas** — spatial code visualization: an infinite 2D canvas with semantic zoom from folder blocks to syntax-highlighted source, PixiJS WebGL rendering and d3-hierarchy layout.
- **Parlor** — mental math training app with prerequisite-based skill trees, an SM-2 spaced-repetition variant and a gamified XP layer.
- **Truco Marker** — real-time multiplayer score tracker: room-based sync over SSE pub/sub with polling fallback, optimistic UI with server reconciliation, Web Audio synthesis.
- **HabitMint** — self-hosted habit tracker with a reward-currency gamification system and a contribution-style activity chart.
- [**soupawhisper**](https://github.com/lucasflomuller/soupawhisper) — push-to-talk voice dictation for Wayland/Hyprland using faster-whisper.

---

## Elsewhere

Portuguese (native) · English (fluent — has worked in all-English companies since 2018).

Open to senior and staff engineering roles with US and EU companies — fully remote from Brazil.

[LinkedIn](https://www.linkedin.com/in/lucasflomuller/) · [lucasflorianomuller@gmail.com](mailto:lucasflorianomuller@gmail.com)
