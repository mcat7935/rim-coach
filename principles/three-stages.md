# Three Stages of RIM: RsIM → SDIM → BSM

RIM (Recursive Innovation Method / 再帰的イノベーション 企画方式) is structured as three phases per the official RIM specification (Flying Penguins, 2026-03 release).

> ⚠️ **WIP / 未完成ノート**: The full English-abbreviation expansions for RsIM / SDIM / BSM are not yet formally published by the originator. This page documents the abbreviations, their phase positions, and their functions. If canonical expansions are later established, this file will be updated.

---

## Overall flow (from official RIM PDF, 2026)

```
[RsIM: 分析／発想]  Analysis / Ideation
   = 連続的イノベーション探索ゾーン (continuous-innovation exploration zone)
   = AI-coachable core territory
   ↓
[If breakthrough is needed, jump the 演繹的発想の壁 (deductive-thinking wall):]
   ↓
[SDIM: 発想]  Ideation (discontinuous-innovation exploration zone)
   = phenomenon, not a method
   = second-order cybernetic shift / 脳内革命 / カクシン moment
   ↓
[Once a Value Cycle is found and stable:]
   ↓
[BSM: 伝達]  Business Story Model — narrative for executives/investors
   = separate skill territory, future scope
```

---

## RsIM (分析／発想) — the core methodology

This is the **central concern of rim-coach**.

- Synthesizes multiple perspectives (UX × Business × Systemic) into a common model
- Iterates: detect plausibility-suspicious node/arc → switch perspective → write a separate model → integrate into Value Cycle Model (see `core.md` §10)
- The "**continuous innovation exploration**" zone
- All of `prompts/review.md`'s Checks support RsIM work

This is what most RIM coaching addresses, and what AI can most concretely support.

---

## SDIM (発想 / 飛躍的) — phenomenon, not method

SDIM is a **phenomenon**, not a method. It cannot be performed on demand.

It occurs when RsIM-driven understanding deepens to the point of producing a **discontinuous insight** — multiple traditions converge on this same phenomenon:

| Tradition / framing | Term |
|---|---|
| Tsuchiya (interview Q10, 2026-05-16) | **脳内革命 / 核心 / カクシン (innovation = conviction = core)** |
| Motomura (Slack 2026-05-07, interview reference) | **セカンドオーダーサイバネティクス的 飛躍** (second-order cybernetic leap) |
| Krippendorff (via `theoretical-background.md`) | **ナラティブの方向再定義** (narrative re-direction) |
| RIM PDF (Page 9, 2026-03 release) | **演繹的発想の壁** を超える / 飛躍的イノベーション |

All four describe **the same phenomenon**.

**Triggers / facilitators** (per RIM PDF Page 9, 13):
- **アナロジー思考** (analogy thinking)
- **インクルーシブ思考** (inclusive thinking)
- Continued deepening of RsIM structural work until the wall is jumped

**Implication for AI coaching**:
- AI **cannot cause** SDIM. The leap belongs to the human (last-mile, `core.md` §12).
- AI **can** set up the **structural conditions** that make SDIM possible (RsIM support via review prompts).
- AI **can** recognize patterns suggesting the user is approaching the wall and gently suggest analogy / inclusive thinking moves.
- AI **must not** declare "this is the breakthrough" — only the stakeholder can verify the 脳内革命.

---

## BSM (伝達) — separate scope, future skill

BSM converts a completed RIM model into a **narrative form** for executives, investors, and external stakeholders.

**Input**: A completed, settled RIM Value Cycle Model.

**Output**: A Business Story Model covering:
- 何を提供するか (what to provide)
- どう提供するか (how)
- どんな価値をもたらすのか (what value)
- なぜ取り組むのか (why — links to vision / MVV)
- どうやって永続化するのか (how to sustain)

**Scope note**: **BSM is NOT covered by rim-coach core**. It will be implemented as a separate Claude Code skill (provisional name: `rim-bsm`) in a future release. AI is expected to be particularly strong at BSM because narrative generation is an LLM-friendly domain (Tsuchiya, 2026-05-16).

---

## Why this matters for RIM coaching design

The three-stage structure clarifies what AI can and cannot do:

| Stage | AI's role | Human's irreducible role |
|---|---|---|
| **RsIM** | Active support: surface concerns, decompose plausibility, return hints, accumulate know-how across iterations | Last-mile structural judgment, choice of perspective switches, value-cycle synthesis |
| **SDIM** | Set up conditions (via RsIM support), recognize wall-approach signals, suggest analogy/inclusive thinking | **The leap itself** — only the stakeholder can have the 脳内革命 |
| **BSM** | Strong potential for AI-driven first drafts of narrative | Validation, edit for stakeholder fit, final story ownership |

All three honor the discipline established in `core.md` §9, §12, §15.
