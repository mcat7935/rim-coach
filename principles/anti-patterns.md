# Anti-Patterns

Common failure modes in RIM diagrams. Derived from interviews with the methodology originator (Akitsugu Tsuchiya), 2026-05-16 onward, and Slack dialogue with Akira Motomura, 2026-05-07/08.

## 1. Business layer

### 1a. Enumerating behaviors instead of naming the essence
The author lists what users do and how the system behaves, instead of articulating the **abstract, most-characteristic** statement of what the business *is*.

### 1b. Talking about the business while skipping its essence
The diagram references the business but never lands on a sentence that captures its core.

## 2. UX layer

### 2a. UX = UI only
The diagram treats UX as "the screen experience" and fixes pre-use / post-use as immovable background. The user's full psychological journey is missing.

### 2b. Fixing UX before discussing Business/Systemic
The author treats UX as solved (or assumed) and builds Business/System on top of it. UX should remain alive and questionable throughout the diagramming work.

### 2c. UX research without a business question
Conducting UX research / user interviews as the *first* step, ungrounded in a business-structure question that surfaced the need. The default order (Tsuchiya's "royal road") is: Business structure → naturally raises UX question → THEN UX research.

## 3. Systemic layer

### 3a. Role-fusion ("全部 AI で")
Roles among human, system, and AI agent are not separated. The diagram says "AI does this" without specifying what humans still own or what the (non-AI) system makes visible.

### 3b. Confusing AI agents with mere automation
The diagram treats AI as just "more automation," rather than recognizing it as an **intermediate-characteristic (pseudo-autonomous)** actor distinct from both pure systems and humans.

### 3c. Only "user-active" AI use cases
AI is treated only as something the user calls. The **agent-pull** case (AI proactively retrieving information / acting on the user's behalf) is missing entirely.

### 3d. Rigorous-delegation gap for humans
"What we delegate to humans" is implicit or vague, rather than rigorously defined.

### 3e. System present, but visibility unspecified
The diagram shows a non-AI system but does not state what it **makes visible** (it just stores data).

## 4. Process-level (drawing & dialogue)

### 4a. Silo thinking — "it's not my scope"
The most common cause of integration failure. UX designers draw only the UX model, business people draw only the business model, and each assumes "the system folks will take care of the rest."

> "ユーザーエクスペリエンスデザイナーであれば UX モデルが描ければ それ以外は 'it's not my scope' ということにしますし、これはビジネス系の人も同様で、あとは何かシステムの人が何とかするんでしょう、みたいな感じになりがちです。でも私はこれが良くないと思っていて..."
> — Akitsugu Tsuchiya, interview 2026-05-16

This pattern is no longer viable in the 2020s integrated-business era (see `core.md` §14), because modern offerings (e.g., addressing 1:100 supply/demand gaps with AI mechanisms) inherently require all three perspectives.

### 4b. Premise validation gap ("ある事ありき")
Some nodes or arrows in the diagram are **assumed to work / exist** in the modern context, without verification. The diagram proceeds as if those elements are already valid.

> "いくつかのノード、もしくはいくつかの矢印について、現代において それがちゃんと成立するということが分かっていないのに、それがある事ありきでのビジネス、もしくはある事ありきでのユーザー体験モデルみたいなものが提示されていることがほとんどです。"
> — Akitsugu Tsuchiya, interview 2026-05-16

When reviewing, ask of each significant node/arrow: "Is this verified, or assumed?"

### 4c. Era misalignment
The diagram relies on premises that held in earlier eras (1970–80s technical-only innovation, iPhone-era UX-only differentiation) but no longer hold in the 2020s integrated-business context.

See `core.md` §14 for the era criterion.

## 5. Loop-structure pathologies

### 5a. Othello-endgame (too many negatives chained)
The diagram chains so many negative elements together that the only way to make it positive is a single, implausibly large flip — like late-game Othello when the opponent dominates the board.

When you see this:
- Flag that the diagram is **demanding a heroic flip** to become viable
- Suggest restructuring so multiple smaller staged interventions can address the loop
- See `negative-loop-response.md` for the Othello flip-search and response patterns

### 5b. All-positive completion (no negative anywhere)
The diagram shows only positive-to-positive chains with no negative element anywhere. In real-world business contexts, this is almost never accurate.

> "ヒアリングする時に、ポジティブとポジティブとポジティブだけの連鎖が描けるってことはほとんどないはずです。逆に言うとそれが欠けてるのであれば、そのビジネスの成長が指数的に続いているわけなので（現代だとさらに加速）、私の登場の余地は無いと思ってます。"
> — Akitsugu Tsuchiya, interview 2026-05-16

If you see an all-positive loop, the author is likely hiding the negative element (consciously or not), or has not yet identified where the friction lies. Prompt them to look for the friction; if there genuinely is none, the diagram has nothing for RIM to work on.

### 5c. Loop-looks-like-loop-but-isn't (false-positive circulation)
Arrows visually form a loop, but they don't trace a coherent causal chain. The test:

- Can the loop be read as **Actor (S) → Arrow (V) → Property (O)** sentence chains?
- Does the chain make sense when narrated?
- (Even if narratable, evaluate plausibility separately — see `quality-check.md`.)

Note: per Tsuchiya, even loosely plausible chains qualify as "RIM-drawn" at the **inclusion** gate. Quality assessment is separate.

### 5d. Visual no-loop but autonomous mutual chain (false-negative circulation)
With AI agents in play, the absence of a visual loop **does not always mean absence of circulation**. Autonomous nodes (humans, AI agents) may mutually interact in ways that constitute circulation even without a drawn loop.

When you see this pattern, suggest the author draw a **separate** circulation model focused on agent ↔ agent or agent ↔ human interactions.

## 6. AI coaching meta

### 6a. AI declaring "this is abstract / this is concrete"
A RIM-coaching AI that judges abstraction level itself violates the methodology. It must instead **ask the user to judge for themselves** by stepping back and re-examining abstraction in light of their own business essence.

### 6b. AI attempting the last-mile leap
If the structural work in the RIM loop (see `core.md` §10) does not reach the business or social goal, the next step is a **human creative leap**. AI must not attempt to produce that leap, only support the conditions for it.

### 6c. AI returning verdicts instead of questions
AI output that closes off thinking ("the right answer is X") violates the hint-not-answer discipline. All findings should be returned as questions or candidate concerns to the user.

## 7. Practitioner mindset traps

These are not diagram failures per se, but failure modes in how people *approach* RIM.

### 7a. SE / logical-thinker paralysis (要素列挙詰まり)
Logical / SE-style practitioners often **cannot get started** because they want to enumerate all elements first before drawing anything. The diagram never gets written; the practitioner spirals in element-listing.

**Suggested response (per Tsuchiya, 2026-05-16)**: nudge them to **use AI as a conversation partner to surface elements interactively**. This is one of the core use cases for `prompts/starter.md`.

> "システムエンジニア的な、逆にロジカルな人たちっていうのは、結構そもそも手が動かない、要素を洗い出し困っちゃう、みたいなところがある。ここはうまく背中を押せると、特に AI とのインタラクションから要素を洗い出して書くみたいなことができるといいかな。"
> — Akitsugu Tsuchiya, interview 2026-05-16

### 7b. Single-correct-form belief (唯一正解信仰) — "trauma-like" pattern
The practitioner assumes there is a **unique correct way** to draw the RIM and becomes paralyzed by caution. Tsuchiya describes this as **trauma-like**.

Reality:
- **チーム内で伝わればいい** — what matters is whether the team understands the diagram
- **複数の RIM variants が並立する** (`principles/variants.md`) — there is no single canonical form
- The criterion is whether useful points are surfaced (Slack 2026-05-07), not whether the form matches a template

**Suggested response**: in coaching prompts (`prompts/starter.md`), reassure the practitioner that multiple forms are fine. Discourage perfectionism at the early-draft stage.

> "唯一の正解の書き方があるんじゃないかと思って慎重になってしまう、というパターンが失敗パターンとしてあると思います。要はチーム内で伝わればいいので、必ずしも書き方そのものに唯一の正解があるわけではないです。"
> — Akitsugu Tsuchiya, interview 2026-05-16

### 7c. "Why" missing in behavior chains
A specific form of the subdivision trap (§5b detail, but worth naming as a mindset issue): the practitioner writes the behavior chain but does not express **why each step causes the next**. The diagram becomes a sequence list, not a structural model.

Coaching nudge: 「この行動の次の行動を引き起こしている『なぜ』は何ですか？」

## 8. Notation-level anti-patterns (per official RIM spec)

### 8a. Direct actor-to-actor connection
RIM's canonical convention (`principles/notation.md`) is to express structure through **property-to-property propagation (S V O where S, O are properties)**, not actor-to-actor arrows. Actor-to-actor arrows are reserved for cases where property granularity isn't yet resolved.

Coaching nudge: 「この矢印、アクター間を直接繋いでいますが、本来は『アクターの属性 → 相手アクターの属性』の作用として描く方が RIM 流です。属性は何ですか？」

### 8b. Actions only, no propagations (アクション羅列のみ)
The simple-type procedure (`notation.md`) accepts action nodes, but the diagram becomes a sequence-list if all nodes are actions and no continuous propagation (作用) is captured. Recall the methodology distinction: **アクション = intentional single act**, **作用 = automatic continuous propagation** ("water flowing downhill").

Coaching nudge: 「アクションは書けていますが、その結果が自動的に伝播していく作用（『高低差で水が流れる』ような系統的影響）は描かれていますか？」
