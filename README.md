# Marketing AI Suite (B2BMarket AI Strategy Suite)

A structured, model-driven suite that takes a user from a raw idea (new
product, new offering, relaunch, or repositioning) to a complete,
board-ready B2B marketing and sales strategy — applying the same governed
methodology as the Category AI / Procure AI suite: **Market Levels → Drivers
→ Strategy → Plan → Execution**.

## What it does

- **Module 0 — Idea & Intake:** 15 guided B2B questions (vertical,
  company-size band, ACV, sales-cycle length, DMU complexity, budget band,
  competitors, goals, constraints) that calibrate every downstream module
- **Modules 1–10 — AI-drafted strategy modules:** Market Intelligence
  (PESTEL, Five Forces, TAM/SAM/SOM), Drivers Analysis, Competitive Position
  (SWOT→TOWS), Marketing Strategy (Porter, Ansoff, STP), Brand Strategy
  (Kapferer, CBBE), Accounts & DMU Segmentation (ICP, ABM tiers, personas),
  Marketing Mix (7Ps), Demand Gen & Channels, Sales Strategy (funnel, SLA,
  enablement), and Plan/Budget/KPIs (SOSTAC)
- **Cascading context:** every module draft is generated from the intake
  brief plus all earlier module outputs, so nothing is drafted in isolation
- **Four decision gates:** market attractiveness, strategic posture, ICP &
  positioning lock, budget envelope — each requiring an explicit decision
  note recorded in the final document
- **Strategy Copilot:** a context-aware in-app chatbot that knows which
  screen the user is on, what's been drafted, and the user's brief
- **Strategy Document assembly:** all modules and gate decisions compiled in
  SOSTAC order, downloadable as Markdown

## Status

v2.0. Currently a single-file React application (`b2bmarket-ai-strategy-suite.jsx`)
running as a Claude artifact. No persistence yet — all state clears on
refresh; users export the Strategy Document as they go. See roadmap in
`METHODOLOGY.md` for planned save/load and export upgrades.

## Tech stack

Single-file React component. AI via Claude (built into the artifact
environment, no key needed) or Gemini (user-supplied key, held in memory
only, never persisted). No external state libraries; styling inline.

## How to run

Currently runs as a Claude artifact preview. For standalone deployment
(outside the artifact sandbox), this would need to move to a hosted React
build with persistent storage — see roadmap.

## Development note

Development assisted by Claude Code (Anthropic) under my direction. The
methodology, product design, and domain expertise reflected in this tool
are my own — see `METHODOLOGY.md` for the original framework.

## Related

See [`METHODOLOGY.md`](./METHODOLOGY.md) for the market-levels framework and
the consulting models this suite applies at each stage.
