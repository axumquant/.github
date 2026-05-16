# Axum Labs

> Agentic AI lab building autonomous systems for fintech and real-time B2B sales operations.

We build multi-agent AI infrastructure where it matters most: production trading systems that compound capital, and live sales workflows that compound revenue. Everything here is original work — designed, built, and deployed in-house.

---

## What we ship

### Axum Labs Trading Platform
Autonomous quantitative trading infrastructure. Full Rust + Python stack with multi-agent strategy evolution, alternative data pipelines (satellite imagery, AIS shipping, regime/sentiment classification), and Nomad-orchestrated deployment. 30+ MCP servers, 15+ specialized agents (signal router, risk governor, position sizer, island discovery/generation/repair, gauntlet validator), and a Tauri desktop client.

### Sales Coach
Real-time AI coaching platform for B2B insurance sales. 12 specialized agents deliver sub-800ms coaching cues during live calls — compliance alerts, objection handling, plan matching, and tonality feedback. Self-healing portal integration via three-layer extraction (CDP network interception → accessibility tree → vision-language model fallback).

- [Chrome Web Store](https://chromewebstore.google.com/detail/sales-coach/oeleifakfnkihkkbeaabgibdoeknnilp)
- [Agency portal](https://portal-three-rose.vercel.app/signup)

---

## Featured Repositories

| Repo | What it is |
|---|---|
| [**sales-coach**](https://github.com/axumquant/sales-coach) | Real-time AI coaching platform — 12-agent orchestrator, FastAPI, Chrome extension, Windows tray client |
| [**axum-labs-studio**](https://github.com/axumquant/axum-labs-studio) | Agency admin portal for Sales Coach — billing, analytics, knowledge-base ingestion, white-label |
| [**site-mapper-agents**](https://github.com/axumquant/site-mapper-agents) | LLM-driven self-healing API discovery — Pydantic AI agents (Architect, Eavesdropper, Healer) adapt to schema changes |
| [**arch-viewer**](https://github.com/axumquant/arch-viewer) | MCP-native codebase analysis — interactive architecture diagrams, Neo4j knowledge graph, 17 Claude Code tools |
| [**cdp-network-interceptor**](https://github.com/axumquant/cdp-network-interceptor) | Chrome DevTools Protocol network capture for MV3 extensions — PII redaction, iframe auto-attach, stale-debugger recovery |
| [**mv3-audio-replay-buffer**](https://github.com/axumquant/mv3-audio-replay-buffer) | Encrypted, durable audio frame buffer for Chrome MV3 service workers — ack-based replay over WebSocket |
| [**devkit**](https://github.com/axumquant/devkit) | Universal B2B/SaaS development foundation — skills, hooks, agents, CI/CD templates |

---

## Stack

**Languages** — Python · Rust · TypeScript · Shell

**AI / Agents** — Multi-agent orchestration · MCP servers · LLM routing (Ollama Cloud, OpenAI, Anthropic) · RAG (Qdrant, Neo4j)

**Backend** — FastAPI · async WebSockets · Supabase Postgres · Redis · ClickHouse · Stripe

**Browser** — Chrome MV3 · CDP network interception · accessibility-tree crawling · VLM fallback

**Frontend** — Next.js 15 · Tauri 2 · responsive sidepanel UIs

**Infra** — Nomad · Railway · Cloudflare · Docker · CI/CD automation

---

## Contact

Norman Beckford — Licensed Medicare Agent, self-taught developer since 2018, building with LLMs since 2022.

- norman@axumquant.com
- [linkedin.com/in/norman-beckford-832711218](https://linkedin.com/in/norman-beckford-832711218)
