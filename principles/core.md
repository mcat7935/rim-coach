# Core Principles of RIM

These principles are distilled from publicly available material and ongoing interviews with the methodology originator (Akitsugu Tsuchiya / Flying Penguins) and contributors (Akira Motomura).

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

## 8. UX is the full psychological journey, not just UI

Most diagrams limit UX to "the moment of use" (UI / app interaction). RIM expects three regions to all be present:

- **Pre-use**: how the user's psychological state changes leading up to use
- **During-use**: UI experience (the usual scope)
- **Post-use**: how the user *recalls* and returns to the service

A diagram that captures only during-use is treating UX as fixed background rather than as a journey.

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

## More to come (interview in progress)

Still pending:

- "Positive → positive → negative" innovation pattern: more concrete examples and edge cases
- Layout judgment (visual hierarchy, center-of-perspective transmission)
- Granularity calibration (too coarse / too fine / mixed)
- "Core (キモ)" presence judgment beyond what is in §3
