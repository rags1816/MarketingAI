# MarketAI™ — B2BMarket AI Strategy Suite
## v3.1.0 — FROZEN RELEASE — 12 July 2026

This package is the frozen baseline of the platform. No further changes will be made
to these files without a new version number. The version stamp appears on the app's
login screen and next to the sidebar wordmark.

## Package contents
- `index.html` — the complete platform (single file, no installation; open in any modern browser)
- `MarketAI_B2BMarket_Handover_Note_v3.1_FINAL.docx` — full product handover guide (features, user journey, architecture, AI providers & costs, QA evidence, limitations, roadmap, checklist)
- `RELEASE_NOTES.md` — this file

## First run
1. Open `index.html` in a browser (internet needed on first load for the React/Babel CDNs).
2. Consultant PIN: `1234` · Admin passcode: `admin1234` — **change the admin passcode before sharing.**
3. No API key is required: the Offline Sandbox generates free template drafts by default.
   Add a Gemini or Claude key in the Admin console only for live AI output.
4. Take the 12-step guided tour from the Homepage; hide all demo data with one click when done.

## v3.x change log (all included in this freeze)

### Reliability
- Blank-project creation fixed (prompt() replaced with in-app modal; lands on Intake Brief).
- All blocking browser dialogs removed — works identically in local, hosted, and embedded/sandboxed environments.
- Report Compiler (Module 33) crash fixed; all 35 modules render-verified on empty, partial and complete projects.
- PowerPoint export fixed: a wrong library-name check made every download fail; the library now loads through three CDN fallbacks (jsDelivr → unpkg → Cloudflare) with honest success/failure notices.
- Word and PowerPoint generators read the correct widget-state keys — data sections and charts no longer silently vanish.

### Experience
- Resumed projects open with a compact sidebar: only the resume-point group expanded; amber "N pending" / green "✓ Done" badges on every group.
- Three-level pending clarity: group badge → module row marker → in-module "Why is this Pending?" explainer with jump-to-draft.
- Report-ready alerting: one-time toast, Executive Dashboard banner with direct download buttons, sidebar "Report Ready" markers, and Partial (N pending) vs Complete labels on all report downloads.
- Demo Mode toggle: CardioCloud demo project and sample reports fully removable and restorable; 12-step tour with progress bar and live sample Word/PPT downloads from the tour card.

### AI & exports
- Offline Sandbox is the default provider; keyless live-provider configs self-heal; drafting and Copilot both fall back gracefully — no API key is ever required.
- Model list refreshed: Claude Sonnet 4.6 / Haiku 4.5 and Gemini 2.0 Flash recommended; legacy models retained.
- Native, editable PowerPoint charts: TAM/SAM/SOM bar chart with computed pipeline values, Porter Five Forces radar, budget doughnut, plus SWOT quadrant, PESTLE matrix, BCG/GE tables.
- Word reports carry matching Word-safe bar visuals; every module's individual Word/Slide export bundles its own chart.

## QA evidence for this freeze
- Full JSX compiles clean (TypeScript parser, control-tested).
- 35/35 modules server-rendered without error on empty, partial and complete projects.
- Settings migration verified: keyless configs self-heal, keyed configs untouched.
- Generated decks passed full OOXML validation; native bar/radar/doughnut chart parts confirmed inside the files; all 39 slides rendered to images and visually inspected; Word bar visuals verified to survive Word conversion.

## Known limitations (unchanged by freeze)
Per-browser localStorage (use admin backup/restore to move data) · API keys stored in the
browser (use the proxy option for shared deployments) · .doc export is Word-compatible HTML,
.pptx is native · draft length capped ~1,000 tokens · cost figures are estimates · first load
requires CDN access.
