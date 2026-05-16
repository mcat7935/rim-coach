# rim-coach

> **Open observation prompts and coaching scaffolds for RIM (Recursive Innovation Method / 再帰的イノベーション 企画方式)** — a structural-design planning method by Akitsugu Tsuchiya / Flying Penguins.

## ⚠️ Status: Work-in-Progress (WIP / 未完成)

This repository is an **ongoing methodology elicitation** — not a finished canonical reference.

- **Methodology definitions are still being articulated and refined** by the originator. Concepts, naming, and notation in this repo reflect current best understanding (as of 2026-05) and **will continue to update**.
- The full English-abbreviation expansions for the 3 stages (**RsIM / SDIM / BSM**) are not yet formally published.
- Some sections explicitly note "TBD" or "judgment pending."
- The official RIM specification owners are Flying Penguins; this repo is an open coaching layer aligned with that specification.

**Intended audience**: collaborators, research partners, design-method practitioners actively engaging with the methodology. Not yet positioned as a self-serve introduction for first-time learners.

If you want canonical methodology authority, refer to Flying Penguins directly. This repo aims to *coach the practice*, not to *define the method*.

## What is RIM?

RIM (Recursive Innovation Method) integrates three viewpoints — **UX (体験)**, **Business (事業)**, **Development (実装)** — by going back and forth ("Recursive") to surface the value chain (バリュー・チェーン) and the "core" (キモ) of a service, product, or organization.

Originator: **Akitsugu Tsuchiya** (CEO, [Flying Penguins](https://penguins.jp/))

Background reading:
- [「構造で世界は変えられる」 (note.com)](https://note.com/spice_factory/n/n42dfe43e2efb)
- [RIM 公開勉強会 announcement (spice-factory)](https://spice-factory.co.jp/news/20158/)
- [コンセプト作りとプロト検証は同時並行 (popinsight)](https://popinsight.jp/blog/?p=89788)

## What this repository provides

### Prompts (copy-paste into your LLM)
- **`prompts/review.md`** — Observation prompts for reviewing an existing RIM diagram
- **`prompts/starter.md`** — Coaching prompts for when you're stuck starting a RIM diagram

### Principles (the methodology, distilled)
- **`principles/core.md`** — Foundational principles + the RIM core working loop + the decisive "inner revelation" success criterion (§15)
- **`principles/three-stages.md`** — RsIM (分析/発想) → SDIM (発想/飛躍) → BSM (伝達) three-stage structure
- **`principles/notation.md`** — Official notation: actor / property / arc; S have O / S V O; 標準型 / シンプル型 procedures
- **`principles/variants.md`** — Tsuchiya RIM (mountain + canyon) vs Motomura inductive (negative-cycle); coexistence and choice
- **`principles/negative-loop-response.md`** — Risk-management-style response patterns + Othello flip-search + canyon discovery
- **`principles/granularity.md`** — Granularity = abstraction level for competitive differentiation; industry-peer-discrimination test, subdivision-trap, mixed-granularity diagnostics
- **`principles/layout.md`** — Layout principles: XY semantic conventions, loop visibility (thick-warm vs thin-cool), shape flexibility, density-by-maturity, symmetry, fonts, mille-feuille AI-human pattern applied to layout
- **`principles/quality-check.md`** — Pattern recognition + 5 plausibility-check techniques + mille-feuille flow + expert-consultation discipline
- **`principles/anti-patterns.md`** — Common failure modes (Business / UX / Systemic / Process / Loop-structure / AI-coaching meta / Practitioner mindset traps)
- **`principles/theoretical-background.md`** — Simon → Krippendorff → Design Enablement → RIM lineage (open theoretical bridge, still under collaborative development)

### Process documentation
- **`interview/questions.md`** — The questions used to derive these principles, with status tracking and the interview discipline

### Examples (placeholder)
- **`examples/`** — Worked examples (good diagrams, common mistakes) — to be added

## Design philosophy: hints, not answers

This is **NOT a fully-automated diagram generator**. RIM diagrams require human judgment at the "last mile" — integrating value-cycle insights across UX, business, and development domains.

These prompts are designed as **hints, not answers**: they nudge your thinking without taking the decision from you. AI handles INPUT organization and OUTPUT checking; humans own the integrative value-cycle discovery in the middle.

## Recommended tool: Miro

We recommend **[Miro](https://miro.com/)** as the canonical board tool for RIM diagrams. Reasons:

- Designers (RIM's primary audience) already use it widely
- XY positioning carries semantic meaning in RIM (mountain-range + canyon model); Miro's explicit layout primitives support this precisely
- The methodology originator's own `rim-think` / `rim-diagram` workflows route through Miro via MCP
- Round-trip with AI (AI generates DSL → human edits positions → AI supplements) works cleanly in Miro

FigJam, draw.io, PowerPoint, or hand-drawn whiteboards can also work — the principles in this repository are tool-agnostic — but for new users we suggest starting with Miro for the smoothest path.

## Usage

Paste the relevant prompt file into your LLM of choice (Claude, GPT, Gemini, etc.), along with your RIM diagram (text description, image, or Miro board URL).

Example:

```
<contents of prompts/review.md>

---

Here is my RIM diagram: <description, image, or Miro board URL>
```

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md). No client-confidential material; anonymize before sharing.

## License

MIT — see [LICENSE](./LICENSE).
