# Axum Labs

> Agentic AI lab building autonomous systems for fintech and real-time B2B sales operations.

We design and ship multi-agent AI infrastructure where it matters most: production trading systems that compound capital, and live sales workflows that compound revenue. Original work, shipped end-to-end.

---

## Products

### Sales Coach
Real-time AI coaching platform for B2B insurance sales. **13 specialized agents** deliver live coaching cues — compliance & SOA disclosure tracking, objection handling, plan matching, research, and tonality feedback — under a **sub-800ms end-to-end latency budget**. Self-healing carrier-portal integration: a three-layer perception stack (**CDP network interception → DOM/selector mapping → vision-language-model fallback**) plus an event-driven healer that auto-repairs when carrier APIs change. Real-time voice runs through a Rust (axum + tokio) WebSocket service streaming to Deepgram, with PII/PHI redaction in-Rust.

- **Landing page:** [portal-three-rose.vercel.app](https://portal-three-rose.vercel.app)
- **Chrome extension:** [Chrome Web Store →](https://chromewebstore.google.com/detail/sales-coach/oeleifakfnkihkkbeaabgibdoeknnilp)
- **Status:** Public beta, validating with early-access agencies
- Source: proprietary — commercial product

#### Live shots from a Medicare enrollment session

<img src="./screenshots/hero-coaching-panel.png" alt="Sales Coach v1.8.9 docked beside a SunFire Medicare enrollment portal — live script with phase tracking, call notes, and permission-to-record prompts" />

<sub><b>The coaching panel in action</b> — Sales Coach v1.8.9 docked beside SunFire's Medicare enrollment portal. The live script tracks call phases (Intro → Qualify → Needs → Research → Presentation → Enrollment), while call notes and permission-to-record prompts update in real time.</sub>

<table>
  <tr>
    <td width="50%"><img src="./screenshots/plan-match-research.png" alt="Plan Match and AI Research cards — ranked carrier plans with one-click SOB, agent surfacing supplemental Vision/Dental/Hearing coverage" /></td>
    <td width="50%"><img src="./screenshots/ancillary-rebuttals.png" alt="Ancillary cross-sell and Rebuttals cards — real-time objection handling with a credibility stack" /></td>
  </tr>
  <tr>
    <td align="center"><sub><b>Plan Match + AI Research</b> — ranked carrier plans with one-click SOB, and an agent that surfaces supplemental coverage (Vision, Dental, Hearing) mid-call.</sub></td>
    <td align="center"><sub><b>Ancillary + Rebuttals</b> — cross-sell prompts and real-time objection handling, from a credibility stack to no-pressure-close scripts.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./screenshots/compliance-coaching.png" alt="Compliance, Tonality, and Coaching cards — recording-notice tracking, live tonality metrics, real-time coaching cues" /></td>
    <td width="50%"><img src="./screenshots/card-system.png" alt="Modular card system — Enrollment, Script, Notes, Plan Match, Research, Ancillary, Coaching Cues, Compliance, Rebuttals, Tonality, Psychology, Transcript" /></td>
  </tr>
  <tr>
    <td align="center"><sub><b>Compliance + Tonality + Coaching</b> — recording-notice & disclosure tracking, live tonality metrics, and coaching cues delivered as the call unfolds.</sub></td>
    <td align="center"><sub><b>Modular card system</b> — each specialist agent renders as a card the rep toggles on demand: Enrollment, Script, Notes, Plan Match, Research, Ancillary, Coaching, Compliance, Rebuttals, Tonality, Psychology, Transcript.</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./screenshots/ai-training.png" alt="AI roleplay training — practice calls against AI personas that score the rep on discovery, objection handling, compliance, and tonality" /></td>
    <td width="50%"><img src="./screenshots/diagnostics.png" alt="Built-in diagnostics — Deepgram STT health checks and multi-carrier portal readiness for SunFire, EnrollHere, Heartland, UHOne" /></td>
  </tr>
  <tr>
    <td align="center"><sub><b>AI roleplay training</b> — reps practice against AI personas and get scored on discovery, objection handling, compliance, and tonality before they ever touch a live call.</sub></td>
    <td align="center"><sub><b>Built-in diagnostics</b> — Deepgram STT health checks and multi-carrier portal readiness (SunFire, EnrollHere, Heartland, UHOne…).</sub></td>
  </tr>
</table>

### Axum Labs Trading Platform
Autonomous quantitative trading infrastructure. Rust + Python: **Rust compute kernels** (PyO3/maturin), **island-model evolutionary strategy discovery**, and a **9-stage statistical validation gauntlet** (walk-forward, Deflated Sharpe, CPCV, Monte-Carlo) that rejects overfit strategies before any capital is risked. **30+ strategy archetypes**, 20+ specialized agents, 30+ MCP servers, and 80+ Nomad jobs; alternative-data pipelines (satellite imagery, AIS shipping, sentiment / regime classification).

- **Architecture overview:** [github.com/axumquant/axum-trading-platform](https://github.com/axumquant/axum-trading-platform)
- Source: proprietary — commercial product

### Axum Labs Studio
Autonomous AI web agency platform. A coordinated agent swarm takes a client brief and delivers a deployed, monitored website end-to-end. Intake agent extracts brand guidelines, browser operator generates designs via headless Playwright, copywriter QA enforces tone, debug engineer validates in sandbox, and an MCP deployer ships to Shopify or Wix through a Rust gateway. Four-tiered memory (Postgres, Redis, Mem0/Qdrant, Neo4j) lets agents learn from every engagement.

- **Architecture overview:** [github.com/axumquant/axum-labs-studio-overview](https://github.com/axumquant/axum-labs-studio-overview)
- Source: proprietary — commercial product

### Public Architecture Overviews
Deep architecture write-ups for the proprietary products above — no source, full design.

| Repo | What's inside |
|---|---|
| [**axum-trading-platform**](https://github.com/axumquant/axum-trading-platform) | Hero README + architecture diagram + `docs/ARCHITECTURE.md` — discovery loop, 9-stage validation gauntlet, agent separation-of-powers |
| [**axum-labs-studio-overview**](https://github.com/axumquant/axum-labs-studio-overview) | README + Engineering Highlights — agent swarm, Rust MCP gateway (Universal Commerce Protocol), four-tier shared memory |

---

## Open-Source Infrastructure

The reusable building blocks underneath the products above. All original work, all production-tested.

| Repo | What it is |
|---|---|
| [**site-mapper-agents**](https://github.com/axumquant/site-mapper-agents) | LLM-driven self-healing API discovery — Pydantic AI agents (Architect, Eavesdropper, Healer) adapt to schema changes |
| [**arch-viewer**](https://github.com/axumquant/arch-viewer) | MCP-native codebase analysis — interactive architecture diagrams, Neo4j knowledge graph, 17 Claude Code tools |
| [**cdp-network-interceptor**](https://github.com/axumquant/cdp-network-interceptor) | Chrome DevTools Protocol network capture for MV3 extensions — PII redaction, iframe auto-attach, stale-debugger recovery |
| [**mv3-audio-replay-buffer**](https://github.com/axumquant/mv3-audio-replay-buffer) | Encrypted, durable audio frame buffer for Chrome MV3 service workers — ack-based replay over WebSocket |
| [**agentic-browser-lab**](https://github.com/axumquant/agentic-browser-lab) | Multi-agent browser automation — Perceiver + Planner + Interviewer agents (Pydantic AI) in a Chrome MV3 extension |
| [**devkit**](https://github.com/axumquant/devkit) | Universal B2B/SaaS development foundation — skills, hooks, agents, CI/CD templates |

---

## Stack

**Languages** — Python · Rust · TypeScript · Shell

**AI / Agents** — Multi-agent orchestration · MCP servers · LLM routing (Ollama Cloud, OpenAI, Anthropic) · RAG (Qdrant, Neo4j)

**Backend** — FastAPI · async WebSockets · Supabase Postgres · Redis · ClickHouse · Stripe

**Browser** — Chrome MV3 · CDP network interception · DOM/selector mapping · VLM fallback

**Voice** — Rust (axum + tokio) WebSocket STT · Deepgram · in-Rust PII redaction

**Frontend** — Next.js 16 · Tauri 2 · responsive sidepanel UIs

**Infra** — Nomad · Railway · Cloudflare · Docker · CI/CD automation

---

## Contact

Norman Beckford — Licensed Medicare Agent who taught himself to build the software his industry wouldn't. Started learning to code in 2018, building on LLMs since 2022.

- n.beck10010@gmail.com
- [linkedin.com/in/norman-beckford-832711218](https://linkedin.com/in/norman-beckford-832711218)
