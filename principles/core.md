# Core Principles of RIM

These principles are distilled from publicly available material and ongoing interviews with the methodology originator (Akitsugu Tsuchiya / Flying Penguins) and contributors (Akira Motomura).

## Canonical sources (公用語の所在)

Where to look for the canonical Japanese terminology, by layer:

| Layer | Canonical source | Notes |
|---|---|---|
| **UX** | `principles/core.md` §8 — 3フェーズ整理（利用前 / 利用中 / 利用後想起） | This file is authoritative for UX-layer naming. |
| **Business** — constituents, cycle naming, decomposition | `curriculum/lecture_outline_v0.1.md` | Do **not** re-define business constituents in `core.md`. Reference `lecture_outline` instead. |
| **Systemic** — constituents, sub-layer decomposition, cycle naming | `curriculum/lecture_outline_v0.1.md` | Same policy as Business. `core.md` §6 and §20 contain summary references but the authoritative naming lives in `lecture_outline`. |

When a conflict arises, `lecture_outline_v0.1.md` wins for Business/Systemic, and this file (`core.md` §8) wins for UX. (Set 2026-05-17.)

---

## 1. Structure has circulation (循環)

Any structure that "works" has a circulation — feedback loops, recurring cycles. RIM captures these as causal relationships, in measurable and reproducible form.

> "うまくいく構造には必ず循環があります。その循環を因果関係として捉え、計測し再現できる形にすること"
> — Akitsugu Tsuchiya, [note article](https://note.com/spice_factory/n/n42dfe43e2efb)

## 2. Three viewpoints, recursively integrated

RIM integrates three viewpoints — **UX (体験)**, **Business (事業)**, **Systemic / Technology (実装)** — by going back and forth ("Recursive") until they cohere.

> "UX × 事業 × 開発の3つの視点を、行ったり来たり（Recursive）しながら統合する"
> — RIM 公開勉強会 [announcement](https://spice-factory.co.jp/news/20158/)

## 3. Value chain / "core" visibility

The goal is to surface the value chain (バリュー・チェーン) and the "core" (キモ) of the business/service/product — what actually generates value.

> "何がこのサービス・事業の価値を生み出しているのかという『バリュー・チェーン』が明らかになり、事業やサービスの『キモ』となる部分を浮き彫りにします"

## 4. Relationships, not lists

Elements are integrated via relationships shown in diagrams, not via flat lists of items.

> "言葉ではなく図や関係性で整理"

## 5. Where RIM does NOT apply

Topics requiring interpretive room — values, culture, MVV (Mission/Vision/Values) — are better expressed in language than in structure.

> "価値観や文化のように解釈の余白が必要な領域、例えばMVVは言葉の方が適しています"

---

## 6. Review structure: 3 perspectives, with Systemic decomposed

When reviewing a RIM diagram, work through three perspectives. **Order is not fixed** (see §11); the review prioritizes coverage and quality over sequence.

1. **Business (事業)** — does the author understand the *essence* of the business?
2. **UX (体験)** — is the *full psychological journey* captured (pre-use, during-use, post-use recall)?
3. **Systemic (テクノロジー)** — the hardest layer. Decompose further into three sub-layers:
   - **3a. 従業員としての人間 (Human as employee)** — is what to delegate to humans defined rigorously?
   - **3b. 会社が提供するシステム (Company-provided system, non-AI)** — what is made visible by the system? (Turing-machine + database, no autonomy)
   - **3c. 中間的特性: 疑似的な自主性をもつ AI (Intermediate-characteristic: pseudo-autonomous AI agent)** — are both (i) user-active use and (ii) agent-pull (AI proactively retrieving/acting) modes considered?

Only Systemic carries an internal three-layer decomposition. UX and Business do not, in this model.

> "UX, ビジネス、システミック（システミックだけは複雑）、その中に、従業員としての人間、会社が提供するシステム、そして、中間的特性（疑似的な自主性をもつAI）があるのだと。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## 7. "Essential" = abstract + most-characteristic

When checking whether the author grasps the essence (especially at the Business layer):

- **"Understanding the essence"** = able to articulate the *most characteristic* and *abstract* statement about the business.
- **"Not understanding"** = enumerating user behaviors or system mechanics in a flat list.

> "もっとも特徴を表していて、かつ抽象的なことを言えてる人が本質的だと思っています。それに対してユーザーの行動とかシステムの挙動みたいなものをつらつらしゃべっている場合には、それはあまり本質的ではない。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## 8. UX is the full psychological journey, not just UI — the 3-Phase framing (3フェーズ整理)

Most diagrams limit UX to "the moment of use" (UI / app interaction). RIM expects all three phases of the UX journey to be present. This framing is named **3フェーズ整理 (3-Phase framing)** and is the canonical Japanese terminology for the UX layer.

| Phase (canonical JA) | English gloss | What this phase captures |
|---|---|---|
| **利用前** | Pre-use | How the user's psychological state changes leading up to use (期待・欲求・不安 などの立ち上がり) |
| **利用中** | During-use | UI experience — the usual scope (期待の充足／裏切り) |
| **利用後想起** | Post-use recall | How the user *recalls* the service and returns to it (信頼・記憶・想起確率) |

A diagram that captures only 利用中 is treating UX as fixed background rather than as a journey. The 利用後想起 phase is the one most commonly missing, and it is the phase that explains *why a service is re-used*.

**Canonical terminology rule (2026-05-17)**: Within RIM materials, use **利用前 / 利用中 / 利用後想起** as the phase names, and **3フェーズ整理** as the framework name. Lecture-specific glosses (e.g., 「利用後（次回利用想起）」) are acceptable for accessibility but the canonical short form is **利用後想起**.

> "私はその利用後どうやって次思い出すか、や、その利用までに人間の心理状態でどういう変化が起きたかみたいなことを気にしながら UX を描くので、私自身はそういうものも含めてすべて UX だと思ってる。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## 9. AI coaching discipline: hints, not answers — never judge abstraction

**Decisive design principle for any RIM-coaching AI**: do **not** judge whether a statement is "abstract enough" or "too concrete" yourself. Instead, ask the user to step back and decide for themselves:

> "もう少し抽象度を上げて、自社ビジネスにとって本質的か考えてみてください"

This preserves the human's ownership of the "last mile" of integrative judgment, which is where RIM's value lives. AI's job is to nudge with questions, not to declare verdicts.

> "AI 自身がそれが抽象的か具体的すぎるかみたいなことを判断してもらうというよりも、ユーザーに対して『あなたはもう少しそれを抽象度を上げて、かつ自分のところのビジネスにとって本質的かどうか』みたいなことを質問してもらう、っていうのは AI コーチングとして非常に有用だと思いました。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## 10. Core working loop of RIM

This is the central operational loop of RIM:

```
[Initial model at some abstraction level]
   ↓
[Detect a node/arc whose plausibility (蓋然性) feels suspicious]
   ↓
[Switch perspective: describe a separate model from another view
 (Business / UX / Systemic)]
   ↓
[Integrate the new model with the original → produce a Value-Cycle Model
 (バリューサイクルモデル) where the value chain is now visible]
   ↓ loop (asymptotic / continuous improvement)
[When the integrated value cycle does NOT reach the business goal or
 social goal]
   ↓
[Human: make a leap-of-faith insight = creative, innovative last-mile work]
```

This loop is what Tsuchiya calls the **asymptotic / continuous-improvement approach** of RIM and "what I most want people to learn."

> "視点を切り替えてビジネスだったりシステミックだったりっていう側面でより別のモデルを記述する、そしてその記述したモデルをともと(元)のモデルを統合してバリューサイクルが明らかになったバリューサイクルモデルを書く、っていうことそのものが、RIM の特に私が漸近的とか持続的改善アプローチとしてみんなに勉強して欲しいと思っているものです。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## 11. The starting point is not important

Common assumption: "start with X first" (often UX research, in design-thinking orthodoxy). RIM rejects this:

- The **starting point is not important** for RIM
- What matters is detecting plausibility-suspicious nodes/arcs and switching perspective
- A common-sense default is **Business first** (because business structure naturally raises UX questions: "do users really take that behavior?")
- BUT: when the UX team is strong, starting from a UX journey model is fine; when Systemic concerns surface, deepen there
- Variation by **problem abstraction level** is normal

Anti-pattern to avoid: doing UX research *first*, ungrounded in a business question. Tsuchiya:

> "本来論的には、そこ(課題)が見えてからユーザーリサーチやユーザーインタビューは私はするべきだと思っています。"
> — Akitsugu Tsuchiya, interview 2026-05-16

## 12. Last-mile leap is the human's creative territory

After all the structural work (loop in §10) is done, if the integrated value cycle still does not reach the business or social goal:

- The next step requires a **leap-of-faith insight** that the integrated structure has informed but does not produce
- This leap is **what is left to humans** as last-mile creative / innovative work
- AI must **not** attempt to produce this leap. AI may surface concerns, distill structure, decompose plausibility — but the leap itself belongs to the human

> "これが終わった上で、実際のビジネス目標とか社会のゴールというところに到達しない時に、ここまでの議論を踏まえて飛躍的発想をする、ということが最後人間に残されたラストワンマイル/クリエイティブ/イノベーティブな部分だと私は思ってます。"
> — Akitsugu Tsuchiya, interview 2026-05-16

This is the **load-bearing discipline** for any RIM-coaching AI: support the structural work, never substitute the human leap.

## 13. Canyon (峡谷) — the precise shape of "negative" in the mountain-range model

The "negative" element in `positive → positive → negative` is not just any problem; it is **structurally a canyon (峡谷)** — a specific missing connection between two peaks (strengths) that should be connected.

Mountain-range image:

```
Peak A (strength 1) ── [?] ── Peak B (strength 2)
                       ↑
                    Canyon = the link that would close
                             a positive value loop if filled
                           = the asymptotic-innovation target
```

Innovation = finding the canyon between two valuable peaks that, once bridged, creates the next value loop.

> "山頂と山頂を繋ぐような連峰の中で、実際にはここをもう一つ繋ぎたいんだけどネガティブ=谷になっている部分を見つけるというのが、イノベーションの源泉、もしくは本質的なところの源泉だと思っています。"
> "山と山（成功しているポイント＋それが生んだ効果＋そこへのアプローチ）を描き、それを（山脈）ループにするのに、1つ欠落している負のポイント（峡谷）を見つける方が、漸近的イノベーションで考えやすいのかな、と思っています。"
> — Akitsugu Tsuchiya, interview 2026-05-16 / Slack 2026-05-07

See `principles/negative-loop-response.md` for how to find and respond to canyons.

## 14. "現代において" — the integrated-business-era criterion

When validating premises ("does this node/arrow hold in the current context?"), the criterion is **era-fit**, not a checklist.

Three eras:

| Era | What single-perspective alone could win | Modern judgment |
|---|---|---|
| **1970–80s** | Technical innovation alone (e.g., "submitting data" was itself innovation) | Insufficient today |
| **iPhone era** | UX alone (UX-driven differentiation was enough) | Insufficient today |
| **2020s onward** | None — business has become **"総合格闘技 (Mixed Martial Arts)"** requiring UX × Business × Systemic together (e.g., Uber: UX × revenue mechanism × driver platform) | Required |

The question: **"Is this premise from a single-perspective era, or does it hold up in the 2020s integrated-business context?"** Modern conditions (AI capability, 1:100 supply/demand gaps, role redistribution) often invalidate yesterday's assumptions.

> "1970年とか80年代であれば技術論だけで世の中が良くなっていたと思ってます。... iPhone の登場とかでユーザー体験が重視されて、ユーザー体験を考えられるだけで勝負できていた。それに対して、AI の登場とか関係なく 2020 年代ぐらいに入ってから、かなりビジネスというのが総合格闘技感が高まったと思っています。例えば Uber みたいなものが、UX で戦いながらも、それをちゃんとお金に還元する仕組みまでセットにしたっていう、そういう部分が必要になってきたという認識です。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## 15. The "core (キモ)" of RIM — inner revelation (核心)

> **RIM の 核心 とは、それを見た関係者が 革新 性と 確信 を得られることにある。**
> *(Three Japanese homophones: 核心 / 革新 / 確信 — all read* kakushin *)*
> — Akitsugu Tsuchiya, interview 2026-05-16

**The single most decisive criterion for whether RIM is "working":**

When the RIM model is drawn — its loop structures, its agent-human chains — the stakeholders viewing it experience an **inner revolution (脳内での革命)**. They think: **「あ、本当は我々はこれを目指してたんだ」** ("Ah, this is what we were truly aiming for"). Tsuchiya describes the felt experience as: **「自社のビジネスが一歩前に、認知の面で進んだ感」** ("a sense that one's own business has advanced one step forward, on the cognitive plane") — close in spirit to an *aha experience*.

This is what Tsuchiya calls **the core (核心) of his structural design**.

### Decomposition of "attractive (魅力的)"

1. **Transmitted (伝わる)**: The model communicates to the stakeholder as language and visual structure.
2. **Conviction (納得感 / 確信)**: Not just understanding ("got it"), but a particular feeling — "not ordinary; we were aiming for this."
3. **Inner revolution (脳内での革命 / 革新)**: A reform-level mental shift — **not** a wholesale-overturn revolution (革命のシーン), but a **reform-meaning revolution** where the stakeholder's view of "what we are doing" updates. In English: **"innovation has happened."**

> "結局、描けたループ構造みたいなものや、描けたエージェントと人との連鎖構造みたいなものに、関係者が魅力的だと思うかどうか。... 『あ、本当は我々はこれを目指してたんだ』と思えるような脳内での革命、いわゆる英語で言うとイノベーションが起きたと思えるかどうかが、私はこの RIM であり、私の考える構造デザインの核心だと思ってます。"
> — Akitsugu Tsuchiya, interview 2026-05-16

### Why this section is decisive for AI-coached RIM

This criterion is a **mental state in human stakeholders** — it cannot be judged by AI. AI's role is to **set up the conditions** for this revolution, by:

- Surfacing structural concerns (Checks A–J in `prompts/review.md`)
- Returning questions, never verdicts
- Helping the human navigate the structural work
- **Stepping aside completely** at the moment of revelation/leap

This is the **ultimate grounding** for:
- §9 (Hints, not answers — never judge abstraction)
- §12 (Last-mile leap belongs to the human)
- The entire OSS posture: AI supports the structural conditions, humans own the revelation.

> The diagram's success criterion is not "is it well-formed" but "**does it produce the inner revelation in the stakeholders**" — and only humans can have that revelation.

This is why rim-coach exists as **coaching prompts that nudge with questions**, not as a "validator" or "generator." A generator that produced a beautiful but non-revelatory diagram would have failed.

---

## 16. Granularity = abstraction level for competitive differentiation

Granularity is **not** about node count. It is about **abstraction level**, specifically:

> The ideal granularity is the **most abstract level at which the company's specific competitive characteristic (差別化された強み) is still expressed**.

This is the **same dimension** as the essence judgment in §7. Granularity, abstraction level, and essence are three names for the same thing.

> "適切な粒度っていうのは...ノード数ではなく私は抽象度の問題だと思っています。... 競合する他社との違い、うちの会社はここに強みを持ってるんだっていうものが表現されている範囲で、もっとも抽象的な状態...が私も書く上では理想だと思ってます。"
> — Akitsugu Tsuchiya, interview 2026-05-16

### Quick tests

| Test | Sign of failure |
|---|---|
| **Too coarse — industry-peer-discrimination test** | At this abstraction, the same industry's competitors would have an indistinguishable RIM. Example: if 楽天市場 vs Amazon become indistinguishable, the diagram is no longer recognizably about *this* company. |
| **Too fine — 細分化の罠 (subdivision trap)** | Humans appear only as 行動の連鎖 (behavior chains); systems appear only as 機能の羅列 (function enumerations), at worst UI-operation + behavior enumerations. |
| **Mixed (hardest)** | The actor decomposition is not **MECE** (Mutually Exclusive, Collectively Exhaustive) at an appropriate abstraction; a "**property**" (属性) suddenly appears far from the actor's other properties; the actions between elements do not read as natural Japanese sentences. |

See `principles/granularity.md` for the full Q7 treatment, including practical scaffolding patterns.

---

## 17. Applicability boundary — refined: intent-unification vs interpretation-divergence

§5 (from public material) says "MVV-like values topics → use language not structure." This is correct but coarse. The refined criterion (from interview 2026-05-16):

The applicability boundary is **not about subject matter** (MVV vs not). It is about **purpose**:

| Purpose | Recommended tool |
|---|---|
| **意志統一 (alignment across viewers)** | **RIM (structural)** — including for MVV-like topics, if alignment is the goal |
| **解釈発散 (preserving interpretive room for each viewer)** | Language |
| **Design: aesthetic / look-and-feel / brand impression** | Language → connected to **意匠 (visual design)** directly |
| **Design: operational rules (brand guidelines, etc.)** | Hierarchical structure (RIM-like is OK) |

Structural design ≠ all of design. Brand identity (aesthetic) is better handled via language + direct visual coupling; brand guidelines (operational rules) benefit from hierarchical structure.

> "意志の統一のためには RIM を使う。逆に余白を残し、それぞれの人の解釈可能性の発散みたいなことになる時には、言語の方が向いている。... ブランディングとかユーザーに与える印象、look and feel も含めたブランドデザインなのも、言語で扱いつつそれを意匠と直接接続するみたいな形のほうがいい。ただし、ブランドガイドラインみたいなものを作る時には、hierarchical な運用ルールなどを定義することは非常に重要。"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## 18. Layout — summary (full treatment in `layout.md`)

Layout is a mille-feuille domain (AI supports structure visualization; human owns position-bearing decisions). Quick conventions:

| Dimension | Convention |
|---|---|
| **X axis** | Time / flow (left → right) |
| **Y axis** | Up = higher abstraction or cause-side |
| **Loop visibility** | Thick + warm color (background = thin + cool) |
| **Loop shape** | Flexible (prominence > shape) |
| **Density** | Sparse during iteration, tighter at finishing, always one-screen |
| **Symmetry** | Not required; industry-pattern resemblance aids comprehension |
| **Font** | Gothic / sans-serif; loop labels match loop color |
| **Starting position of loop** | Top-left or left (follow reading direction even for non-time content) |

**Discipline**: AI must not auto-relayout. Position is human territory; arrow semantics is learned skill.

For full Q6 treatment: see `principles/layout.md`.

For the official RIM formal notation specification, see Flying Penguins' Marketing Contents shared drive (path noted in `interview/questions.md`).

---

## 19. Three stages of RIM: RsIM → SDIM → BSM

Per the official RIM PDF (2026-03 release), RIM operates in three phases:

- **RsIM (分析／発想)** — continuous-innovation exploration, the AI-coachable core. All checks in `prompts/review.md` support this phase.
- **SDIM (発想)** — discontinuous-innovation phenomenon. **Same as §15** (inner revelation / 脳内革命 / カクシン). Triggered by jumping the *deductive-thinking wall (演繹的発想の壁)* via analogy thinking and inclusive thinking.
- **BSM (伝達)** — narrative conversion for executives/investors. Out of rim-coach scope (future separate skill).

For full treatment: `principles/three-stages.md`.

## 20. Official 3-layer naming (canonicalized 2026-05-16)

| Layer | English | Japanese | Cycle |
|---|---|---|---|
| 1 | UX | UX / 体験 | UX Satisfaction Cycle |
| 2 | Business | Business / 事業 | Business Growth Cycle |
| 3 | **Systemic** | システミック | **Self(-Organization) Growth Cycle** ✱ |

✱ Naming update from legacy "Product Evolution Cycle" → "Self(-Organization) Growth Cycle" reflects modern reality where systemic-layer growth subject is the **organization itself** (人 + システム + AI エージェントの連鎖), per Tsuchiya 2026-05-16.

Notation, layer-exchange structure, and modeling procedures: see `principles/notation.md`.

## 21. Theoretical lineage (Simon → Krippendorff → Design Enablement → RIM)

RIM is grounded in:
- Simon's design definition (1969) — design as state-transition
- Krippendorff's project concept — narrative-based forward motion in participatory design
- Design Enablement (FP/SF orbit) — Pulling / Pushing / Demonstrating organizational model
- Motomura's second-order cybernetic reading — SDIM as narrative re-direction

For full treatment: `principles/theoretical-background.md`.

---

## More to come

- Formal English-abbreviation expansions for RsIM / SDIM / BSM (originator to confirm)
- Action/Reaction (作用/反作用) formal color conventions
- Loop polarity notation (reinforcing / balancing)
