# Responding to Negative Loops

When RIM analysis surfaces a negative element — whether Tsuchiya's specific **canyon** (single missing positive link) or Motomura's full **As-Is negative cycle** (closed all-negative loop) — the question becomes: what to do with it?

The originator's framing: responses to negative loops can be **typified, similar to risk management**.

> "確かに負のループの対処方法そのものは、リスクマネジメントみたいに、型化（軽減、回避、代替、容認みたいな）できると思う"
> — Akitsugu Tsuchiya, Slack 2026-05-08

## Response patterns (risk-management analogue)

### 1. Mitigation (軽減)
Weaken the negative effect without eliminating it. The loop continues but with reduced impact.
- Example: introduce throttling, partial coverage, or fallback mechanisms.

### 2. Avoidance (回避)
Restructure so the negative element no longer appears in the value chain.
- Example: redesign the offering so the problematic step is bypassed entirely.

### 3. Substitution (代替)
Replace the negative element with an alternative mechanism that achieves similar function without the negative dynamics.
- Example: replace human labor at a bottleneck with AI agent + human oversight when the labor is the source of friction.

### 4. Acceptance (容認)
Acknowledge the negative loop, accept its cost, and design surrounding structure to be resilient to it.
- Example: treat a known retention drop as a fixed leak and build acquisition to compensate, while monitoring.

These four are illustrative; additional response types may be added as the methodology matures.

---

## Finding leverage points — Othello metaphor

For a negative cycle (especially Motomura-style all-negative loops), Tsuchiya offered a productive question pattern:

> "赤の部分をオセロの相手石と思って、どこならひっくり返せそうか？そしてひっくり返ると、何連鎖行きそうか？"
> — Akitsugu Tsuchiya, Slack 2026-05-08

Treat each negative node as an opponent's stone on an Othello board. Two questions:

- **Where could we flip?** Which negative node is most accessible to convert into a positive?
- **If flipped, what cascade follows?** How many other negatives would resolve as a consequence?

This converts a daunting all-negative loop into a search for **high-leverage flip points** — connecting Motomura's inductive negative-cycle surfacing to actionable interventions.

Cautionary note (from the same Slack message):
> "とはいえ、ちょっと次の石がひっくり返せそうには思えていない。（課題が山積イバラの道っぽい？）"

When even the flip-search returns "no obvious next stone," the diagram has reached a state where Tsuchiya's mountain-range reframing or external creative input may be more productive than further flip-search.

---

## Finding canyons — Tsuchiya's two approaches

For Tsuchiya's mountain-range variant, finding the canyon (the single missing positive link) can proceed two ways:

### Approach A: Desktop (model-only)
- Inspect the existing RIM model
- Find points where **node-arc continuity has low plausibility** ("here is a success, there is a success, but the connection between them looks suspicious")
- **Hypothesize** a canyon at the suspicious point
- **Confirm** via stakeholder hearing or focused interview

> "ノードとアークの連続性の蓋然性が低い部分、こことここはこう成功してるんだけどその間にギャップがあるみたいなところに、実際には山脈と山脈をつなぐべきところに谷があるのではないかという疑いを持って、『こういう課題があるんじゃないですか』みたいな感じでクライアントにヒアリングする"
> — Akitsugu Tsuchiya, interview 2026-05-16

### Approach B: Research-driven
- When the issue domain is identifiable but specific issues are not yet clear
- Use **UX research / business research methods** to clarify the issues within the domain
- The domain itself is the starting point; the specific canyon emerges from the research

> "明確な課題が見えてなくても課題領域が分かった時に、私は UX リサーチだったりビジネスリサーチという手法を使ってそこの課題を明確にしに行くべき"
> — Akitsugu Tsuchiya, interview 2026-05-16

---

## Partial-knowledge accommodation (important)

Tsuchiya explicitly recommends a non-obvious practice:

> "谷が見つかってないことが悪いわけではなく、谷がありそうな領域というものが特定できていること自体を、RIM を実際ベースにビジネスを検討する時にはポジティブな要素... ネガティブなポイントを書く、もしくはネガティブがありそうな領域というのを RIM モデルの中で書くこと自体を推奨してます。"
> — Akitsugu Tsuchiya, interview 2026-05-16

**RIM models should carry both confirmed negatives and "suspected-negative regions" as legitimate elements.** This is unusual relative to "clean diagram" conventions but reflects honest epistemic state.

Implications for review:
- A model containing only confirmed elements may be **hiding incomplete exploration**
- A model with explicit **"suspected-region" markers** is *closer to the goal*, not further from it
- AI reviewers should not penalize partial-knowledge markers; they should encourage them

---

## Anti-pattern: Othello-endgame (too many negatives chained)

When too many negatives accumulate in a single loop, the diagram demands a single dramatic reversal — like late-game Othello when the opponent dominates the board. Tsuchiya's warning:

> "負の連鎖を繋ぎすぎると、人間は何を発明しないといけないかというのが一つポイントでして、これはある意味オセロで終盤盤面が押されたときと似たような感じで、すべてをひっくり返すような飛躍的イノベーションが義務付けられている、みたいな因果ループ図 = RIM モデルになってしまいます。"
> — Akitsugu Tsuchiya, interview 2026-05-16

When you spot this pattern:
- Flag it: the diagram is **demanding an implausibly large flip**
- Suggest **redesign** to enable multiple smaller staged interventions (= asymptotic approach)
- Apply the Othello flip-search to find *any* high-leverage stone, even if small
- Consider whether the situation truly requires the strategic mismatch the diagram implies, or whether the scope can be reframed
