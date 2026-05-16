# Layout in RIM Diagrams

Layout is what Tsuchiya identified (2026-05-16) as **the hardest of the methodology dimensions to articulate** — it touches tool selection, XY-coordinate aesthetics, loop perceptibility, color, line weight, density, and multiple human-sense decisions simultaneously.

This file captures the layout principles from interview 2026-05-16. **Tool-specific formal notation documentation should be consulted separately** (the originator's documentation set lives in Flying Penguins' Marketing Contents shared drive; see `interview/questions.md` for the Q6 status entry).

---

## Core paradigm: the mille-feuille pattern applied to layout

There is no clean separation between "auto-layout (AI)" and "manual layout (human)." The realistic flow is **mille-feuille alternation**:

```
[AI: Mermaid-style enumeration + structure visualization (position-less)]
   ↓ skeleton
[Human: XY placement / loop circularity / visual hierarchy / color / density]
   ↓ visual last-mile judgments
[AI: supplementation per human direction]
   ↓
[Human: re-modification]
   ↓ iterate (asymptotic improvement)
```

**Full automation of WHERE each element goes is impractical.** Position-bearing decisions belong to the human; AI supports the surrounding structure work.

> "Mermaid 記法を使って、まず共通要素を洗い出し、かつビジュアライズする部分を AI および MCP で接続したツールでやるのは有用。ただし、それぞれをどこに配置するかまで完全に自動化するのは実は難しい。... 人間が手を入れた上で再修正、もしくは AI が補完するというのが現実的。"
> — Akitsugu Tsuchiya, interview 2026-05-16

This is the same pattern as `core.md` §10 (RIM core working loop) applied to layout specifically. The principle is consistent: **AI supports structure; humans own the visual last-mile.**

---

## XY axis semantic conventions

**There is no single rule, but the following are natural human reading conventions:**

| Axis | Default semantic | Cognitive basis |
|---|---|---|
| **X axis (left → right)** | Time / process flow (left = earlier, right = later, numbers increase) | Reading direction; cultural number convention |
| **Y axis (top → bottom)** | Up = higher abstraction; Up = cause-side (in cause-effect) | General information hierarchy convention |
| **Default flow** | Top-left → bottom-right | Combination of above |

**RIM-specific note**: RIM is a causal-loop notation, so the X axis is **not strictly time**. However, for reader comprehension, **the loop should still start from the top-left or from the left side** — the entry point follows cultural reading conventions even when content is non-linear.

> "RIM に関しては因果ループというように、最終的に時間軸ではないんですけれども、同じところを再帰的（recursive）にループが回ることを大事にする。結果的に実際には時間が逆順してるわけじゃないんですけど、同じ工程を通るというところで、一般的に理解する上では、左上、もしくは左から始まることが大事だと思っている。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## Loop visual hierarchy (the decisive convention)

For distinguishing loops from background causation:

| Layer | Line weight | Color temperature | Cognitive effect |
|---|---|---|---|
| **Node-to-node relationships (background structure)** | **Thin** | **Cool** (black, gray, cool blue) | Recedes |
| **Loop expression (emphasis)** | **Thick** | **Warm** (orange, red) | Stands out |

This convention is consistent across the Tsuchiya / Motomura group's actual diagrams: in Motomura's inductive negative-loop work, thick red loop arrows are drawn over thin gray background arcs (see `principles/variants.md` §2).

> "ノード間をアークで繋ぐ時には細い線で引く。かつその細い線そのものは黒・グレー・寒色青のように、そこまで人間の脳の認知にダイレクトに来ないような弱い色で描く。ループを表現した部分に関しては太い線および暖色（オレンジ・赤）のような太い線で書く。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## Loop shape (less important than visibility)

The **exact shape of a loop matters less than its visual prominence**:
- Large circle: OK
- Polygon / rounded-corner combinations: OK
- Asymmetric / irregular shapes: OK

What matters: **separately from basic cause-effect arrows, a prominent loop is drawn or not**. With the thick+warm convention above, humans recognize it as a loop regardless of geometric form.

> "大きい円とかでもいいですし、角ばった/角丸の組み合わせ的なループでも、人間はループだと感じられる。ベーシックな作用反作用の因果関係を書いた矢印と別に、目立つループが描かれているかどうかが大事。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## Density follows diagram maturity

Density is a function of **diagram maturity stage**, not a static preference:

| Stage | Density | Reason |
|---|---|---|
| Trial-and-error / iteration | **Sparse (wide node spacing)** | Room to add, change, rearrange |
| Finishing | Can tighten | Compactness for overall grasp |
| **Always** | **Single-screen visibility** | Whole diagram cognized at once |

> "試行錯誤している段階では余白がかなり大きい、つまりノードとノード間の距離は大きい方が良い。もちろん常識的範囲で、一画面で視認できることも大事。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## Symmetry (not required, but pattern recognition aids)

Visual symmetry per se is **not required**.

However, when successful patterns emerge, **structural similarity to established industry patterns** (e.g., AIDMA, customer journey, KPI hierarchy) **aids reader comprehension**.

The principle: **"Content differentiates; structure may resemble industry conventions"**

This is consistent with:
- `principles/granularity.md`'s industry-peer-discrimination test (at the content level — should differ)
- The scaffolding patterns in `principles/core.md` §16 (at the structural level — can resemble industry conventions)

> "シンメトリー性に関してはあんまり必要ないと思います。ただ、実際には成功パターン・ポジティブパターンが見つかってきた時に、同じような業界の因果ループ図が似たような構造をしているというのは、可能であれば人の理解の助けになる。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## Fonts

- **Base font**: clear, readable **gothic (sans-serif)** for Japanese diagrams. Western equivalents: sans-serif faces (Inter, Arial, Helvetica, etc.)
- **Loop-related text**: when loops are drawn in prominent colors (orange / red), **use the same color for the loop label text** — visual continuity reinforces the loop boundary at a glance

> "ゴシック体の分かりやすい読みやすいフォントでいいと思います。その上で、ループ等を表現するときには、そのループが目立つ色を使った場合には同じ文字色を使うと良い。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## Tool selection: Miro recommended (as of 2026-05)

**Recommended canonical tool: [Miro](https://miro.com/)**

Reasons:
- **Designer-friendly**: Miro has wide adoption in design communities, which is RIM's primary audience
- **XY semantic preservation**: For Tsuchiya-style mountain-range + canyon (or Motomura-style negative-loop with prominent loop arrows), position carries meaning. Miro MCP exposes explicit layout primitives (`layout_create`, `layout_read`, `diagram_create` with DSL including positions) for AI round-tripping
- **Continuity with originator workflow**: Tsuchiya's `rim-think` (RIM hearing → YAML) and `rim-diagram` (YAML → board) skills route via Miro MCP

**Other tools also work** (the methodology is tool-agnostic):
- **FigJam**: usable but XY position control is currently weaker via MCP
- **draw.io / PowerPoint / hand-drawn whiteboards**: principles apply; manual layout responsibility
- **Mermaid-style position-less notation**: best for the AI-side of the mille-feuille flow (enumeration / structure-only), not for canonical RIM Value Cycle output

The **official RIM notation specification** lives in Flying Penguins' Marketing Contents shared drive (under `社外発信コンテンツ\RIM`). The principles in this file are layout-focused; for the formal notation spec, consult that documentation set directly.

---

## Important methodological note: arrow semantics emerge mid-way

Per Tsuchiya, **the actor's properties and the action/reaction (作用/反作用) on arrows only come up mid-way** through diagramming — not from the start. Strict checking of arrow meaning is a **learned skill (学習過程)** that requires practice.

Implications for layout review:
- Do not penalize draft diagrams for thin arrow semantics — they accumulate over iteration
- After iteration, gently prompt: 「ここに作用/反作用 の区別を入れられそうですか？」
- Do not have AI declare what is "right" arrow semantics — this is mature-practitioner territory

> "新しいシステムを考える時に使う、アクターのプロパティ、そしてプロパティ間の作用/反作用は、途中でしか出てこない。... 矢印に意味を持たせて書くかについてはかなりガッチリチェックする部分は、少し実際には学習過程を経ないと難しい。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## Discipline reminders for AI-coached layout review

- **Position is human territory** (mille-feuille pattern, `core.md` §10)
- **Do not auto-relayout the user's diagram.** Surface concerns, return questions.
- **Loop visibility > loop shape**. Don't push for circles.
- **Density follows maturity**. Don't insist on tight diagrams during iteration.
- **Pattern recognition aids comprehension** — note when industry-pattern alignment could help, but don't enforce.
- **Arrow semantics is learned skill** — don't declare verdicts on arrow meaning depth.
- **Always honor the ultimate goal** (`core.md` §15): the diagram serves the stakeholder's inner revelation (脳内革命); layout is in service of that, not an end in itself.
