# rim-coach

> Open observation prompts and coaching scaffolds for **RIM (Recursive Innovation Method)** — a structural design thinking methodology by Akitsugu Tsuchiya / Flying Penguins.

**Status: pre-v1.** Content is being developed via interviews with the originator. Use at your own discretion.

## What is RIM?

RIM (Recursive Innovation Method) integrates three viewpoints — **UX (体験)**, **Business (事業)**, **Development (実装)** — by going back and forth ("Recursive") to surface the value chain (バリュー・チェーン) and the "core" (キモ) of a service, product, or organization.

Originator: **Akitsugu Tsuchiya** (CEO, [Flying Penguins](https://penguins.jp/))

Background reading:
- [「構造で世界は変えられる」 (note.com)](https://note.com/spice_factory/n/n42dfe43e2efb)
- [RIM 公開勉強会 announcement (spice-factory)](https://spice-factory.co.jp/news/20158/)
- [コンセプト作りとプロト検証は同時並行 (popinsight)](https://popinsight.jp/blog/?p=89788)

## What this repository provides

- **`prompts/review.md`** — Observation prompts for reviewing an existing RIM diagram
- **`prompts/starter.md`** — Coaching prompts for when you're stuck starting a RIM diagram
- **`principles/core.md`** — Distilled core principles (from public material)
- **`principles/anti-patterns.md`** — Common failure modes to watch for
- **`examples/`** — Worked examples (good diagrams, common mistakes)

## Design philosophy: hints, not answers

This is **NOT a fully-automated diagram generator**. RIM diagrams require human judgment at the "last mile" — integrating value-cycle insights across UX, business, and development domains.

These prompts are designed as **hints, not answers**: they nudge your thinking without taking the decision from you. AI handles INPUT organization and OUTPUT checking; humans own the integrative value-cycle discovery in the middle.

## Usage

Paste the relevant prompt file into your LLM of choice (Claude, GPT, Gemini, etc.), along with your RIM diagram (text description, image, or board URL where supported).

Example:

```
<contents of prompts/review.md>

---

Here is my RIM diagram: <description or image>
```

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md). No client-confidential material; anonymize before sharing.

## License

MIT — see [LICENSE](./LICENSE).
